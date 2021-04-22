---
title: Plockning och leverans i grundläggande lagerkonfiguration | Microsoft Docs
description: I Business Central kan de utgående processerna för plockning och utleverans utföras på fyra sätt med hjälp av olika funktioner beroende på lagerkomplexitetsnivå.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 68b35b6c007dd22c964bd616b1d59df2841db411
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772085"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Genomgång: Plockning och leverans i grundläggande lagerkonfiguration

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

I [!INCLUDE[prod_short](includes/prod_short.md)] kan de utgående processerna för plockning och utleverans utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.  

|Metod|inkommande behandling|Lagerställen|Plockningar|Utleveranser|Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokföra plockning och utleverans från orderraden|INTER|||2|  
|B|Bokföra plockning och utleverans från ett lagerplockningdokument||X||3|  
|L|Bokföra plockning och utleverans från ett distributionslagerutleveransdokument|||X|6-4-5|  
|D|Bokföra plockning från ett distributionslagerplockningdokument och bokföra leveransen från ett distributionslagerutleveransdokument||INTER|INTER|6-4-5|  

Mer information finns i [Designdetaljer: utgående distributionslagerflöde](design-details-outbound-warehouse-flow.md).  

Efterföljande genomgången visar metod B i föregående tabellen.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="about-this-walkthrough"></a>Om den här genomgången

För grundläggande lagerkonfigurationer där lagerstället har konfigurerats att kräva plockningsbearbetning men inte leveransbearbetning, använder du sidan **Lagerplockning** för att registrera och bokföra plocknings- och leveransinformation för dina utgående källdokument. Det utgående källdokumentet kan vara en försäljningsorder, inköpsreturorder, utgående överföringsorder eller produktionsorder med komponentbehov.  

I den här genomgången tas följande aktiviteter upp:  

- Lägger upp lagerstället SILVER för lagerplockning.  
- Skapa en försäljningsorder för kund 10000 på 30 högtalare.  
- Släppa försäljningsordern för lagerhantering.  
- Skapa en lagerplockning som baseras på ett släppt källdokument.  
- Registrering av lagerrörelsen från lagret och samtidigt bokföra försäljningsutleveransen för källförsäljningsorder.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a>Roller

Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:  

- Dist.lagerchef  
- Orderhandläggare  
- Lagerarbetare  

## <a name="prerequisites"></a>Förutsättningar

För att kunna utföra den här genomgången behöver du:  

- För [!INCLUDE[prod_short](includes/prod_short.md)] online är detta ett företag som bygger på den **Avancerade utvärderingen av utvärdering – fullständiga exempeldata** i en begränsad miljö. För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, CRONUS International Ltd. installerat.  
- Gör dig själv till distributionslageranvändare på lagerstället SILVER med följande steg:  

  1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Distributionslagerpersonal** och välj sedan tillhörande länk.  
  2. Välj fältet **Användar-ID** och välj ditt eget användarkonto på sidan **Användare**.  
  3. Ange SILVER i fältet **Lagerställekod**.  
  4. Välj fältet **Standard**.  

- Gör artikeln LS-81 tillgänglig på platsen SILVER, genom att följa nedanstående steg:  

  1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Dist.lager artikeljournaler** och välj sedan relaterad länk.  
  2. Öppna standardjournalen och skapa sedan två artikeljournalrader med följande information om arbetsdatumet (23 januari).  

        |Transaktionstyp|Artikelnummer|Lagerställekod|Lagerställeskod|Antal|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Positiv antalsjust.|LS-81|SILVER|S-01-0001|20|  
        |Positiv antalsjust.|LS-81|SILVER|S-01-0002|20|  

  3. Välj åtgärden **Bokföra** och sedan knappen **Ja**.  

## <a name="story"></a>Situation

Ellen, lagerchefen i CRONUS, ställer in lagret SILVER för grundläggande plockning där lagerarbetare behandlar utgående beställningar var för sig. Susan, orderhandläggaren, skapar en försäljningsorder för 30 enheter av artikeln LS-81 att levereras till kund 10000 från SILVERLAGRET. Anders, lagerarbetaren, måste kontrollera att leveransen förbereds och levereras till kunden. Anders hanterar alla uppgifter som är involverade på sidan **Lagerplockning** som automatiskt pekar på lagerställena där LS-81 lagras.  

## <a name="setting-up-the-location"></a>Lägger upp lagerstället

Inställningen av sidan **Lagerställekort** definierar företagets lagerflöden.  

### <a name="to-set-up-the-location"></a>Så här lägger du upp lagerställen

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Platser** och välj sedan tillhörande länk.  
2. Öppna lagerställekortet SILVER.  
3. Markera fältet **Kräver plockning** på kryssrutan **Dist.lager**.  

## <a name="creating-the-sales-order"></a>Skapar försäljningsreturordern

Försäljningsorder är den vanligaste typen för utgående källdokumentet.  

### <a name="to-create-the-sales-order"></a>Så här skapar du försäljningsreturordern

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan tillhörande länk.  
2. Välj åtgärden **Ny**.  
3. Skapa en försäljningsorder för kund 10000 på arbetsdatumet (23 januari) med följande försäljningsorderrad.  

    |Artikel|Lagerställekod|Antal|  
    |----|-------------|--------|  
    |LS_81|SILVER|30|  

     Fortsätt med att meddela lagret att försäljningsordern är klar för lagerhantering.  

4. Välj åtgärden **Släppa**.  

    Anders fortsätter att plocka och leverera de sålda artiklarna.  

## <a name="picking-and-shipping-items"></a>Plocka och leverera artiklar

På sidan **Lagerplockning** kan du hantera alla utgående distributionslageraktiviteter för ett särskilt källdokument, t.ex en försäljningsorder. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a>Plocka och utleverera artiklar så här

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **lagerplockning** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  

    Kontrollera att fältet **Nr.** fälten på snabbfliken **Allmänt** fylls i.
3. Välj fältet **Källdokument** och sedan **Försäljningsorder**.  
4. Välj fältet **Ursprungsnr.**, markera raden för försäljningen till kund 10000 och välj sedan knappen **OK**.  

    Välj alternativt åtgärden **Hämta källdokument** och välj sedan försäljningsordern.  
5. Välj åtgärden **Fyll i auto. ant. att hantera**.  

    Alternativt, ange 10 respektive 20 i fältet **Ant. att hantera** på de två lagerplockningsraderna.  
6. Välj åtgärden **bokför**, välj **leverera**, och välj sedan **OK**-knappen.  

    De 30 högtalarna har nu registrerats som plockade från lagerställen S-01-0001 och S-01-0002, och en negativ artikeltransaktion skapas som återspeglar den bokförda leveransen.  

## <a name="see-also"></a>Se även

[Plocka artiklar med lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Plocka artiklar för utleverans från dist.lager](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Ställa in grundläggande dist.lager med verksamhetsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Flytta komponenter till ett verksamhetsområde i grundläggande lagerkonfigurationer](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md)  
[Flytta artiklar ad hoc i grundläggande lagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Designdetaljer: utgående distributionslagerflöde](design-details-outbound-warehouse-flow.md)  
[Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]