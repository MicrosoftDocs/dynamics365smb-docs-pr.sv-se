---
title: Plockning och leverans i grundläggande distributionslagerkonfiguration
description: I Business Central kan de utgående processerna för plockning och utleverans utföras på följande fyra sätt beroende på lagerkomplexitetsnivå.
author: jill-kotel-andersson
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 8f938adf6a7629c4f9aedde32c4f8f10cb6f20e6
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8513399"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Genomgång: Plockning och leverans i grundläggande lagerkonfiguration

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

I [!INCLUDE[prod_short](includes/prod_short.md)] kan de utgående processerna för plockning och utleverans utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.  

|Metod|inkommande behandling|Lagerställen|Plockningar|Utleveranser|Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokföra plockning och utleverans från orderraden|INTER|||2|  
|B|Bokföra plockning och utleverans från ett lagerplockningdokument||X||3|  
|L|Bokföra plockning och utleverans från ett distributionslagerutleveransdokument|||X|6-4-5|  
|D|Bokföra plockning från ett distributionslagerplockningdokument och bokföra leveransen från ett distributionslagerutleveransdokument||INTER|INTER|6-4-5|  

Mer information finns i [Designdetaljer: utgående distributionslagerflöde](design-details-outbound-warehouse-flow.md).  

Efterföljande genomgången visar metod B i föregående tabellen.  

## <a name="about-this-walkthrough"></a>Om den här genomgången

För grundläggande lagerkonfigurationer där lagerstället har konfigurerats att kräva plockningsbearbetning men inte leveransbearbetning, använder du sidan **Lagerplockning** för att registrera och bokföra plocknings- och leveransinformation för dina utgående källdokument. Det utgående källdokumentet kan vara en försäljningsorder, inköpsreturorder, utgående överföringsorder eller produktionsorder med komponentbehov.  

I den här genomgången tas följande aktiviteter upp:  

- Lägger upp lagerstället SYD för lagerplockning.  
- Skapa en försäljningsorder för kund 10000 på 30 Amsterdam-lampor.  
- Släppa försäljningsordern för lagerhantering.  
- Skapa en lagerplockning som baseras på ett släppt källdokument.  
- Registrering av lagerrörelsen från lagret och samtidigt bokföra försäljningsutleveransen för källförsäljningsorder.  

## <a name="roles"></a>Roller

Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:  

- Dist.lagerchef  
- Orderhandläggare  
- Lagerarbetare  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a>Situation

Ellen, lagerchefen i CRONUS, ställer in lagret SYD för grundläggande plockning där lagerarbetare behandlar utgående beställningar var för sig. Susan, orderhandläggaren, skapar en försäljningsorder för 30 enheter av artikeln 1928-S att levereras till kund 10000 från distributionslagret SYD. Anders, lagerarbetaren, måste kontrollera att leveransen förbereds och levereras till kunden. Anders hanterar alla uppgifter som är involverade på sidan **Lagerplockning** som automatiskt pekar på lagerställena där 1928-S lagras.

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a>Ställer in lagerplatskoder
När du har skapat ett lagerställe måste du lägga till två lagerplatser.

#### <a name="to-setup-the-bin-codes"></a>Ställa in lagerplatskoder

1. Välj åtgärden **Lagerplatser**.
2. Skapa två lagerplatser med koderna *S-01-0001* och *S-01-0002*.

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a>Skapa en distributionslagerarbetare på lagerstället SYD

För att kunna använda den här funktionen måste du lägga till dig själv till lagerstället som distributionslagerarbetare. 

#### <a name="to-make-yourself-a-warehouse-employee"></a>Så här skapar du en distributionslagerarbetare

  1. Välj den ![Glödlampa som öppnar funktionen Berätta först.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **distributionslagerpersonal** och väljer sedan relaterad länk.  
  2. Välj fältet **Användar-ID** och välj ditt eget användarkonto på sidan **Distributionslagerarbetare**.
  3. I fältet **Lagerställekod** väljer du SYD.  
  4. Välj fältet **Standard** och sedan knappen **Ja**.  

### <a name="making-item-1928-s-available"></a>Göra punkt 1928-S tillgänglig

Gör artikeln 1928-S tillgänglig på lagerstället SYD, genom att följa nedanstående steg:  

  1. Välj den ![Glödlampa som öppnar funktionen Berätta andra.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artikeljournaler** och väljer sedan relaterad länk.  
  2. Öppna standardjournalen och skapa sedan två artikeljournalrader med följande information om arbetsdatumet (23 januari).  

        |Transaktionstyp|Artikelnummer|Lagerställekod|Lagerställeskod|Antal|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Positiv antalsjust.|1928-S|SYD|S-01-0001|20|  
        |Positiv antalsjust.|1928-S|SYD|S-01-0002|20|  

        Som standard är fältet **Lagerplatskod** på försäljningsraderna dolt, så du måste visa det. För att göra detta måste du anpassa sidan. Mer information finns i [Så här börjar du anpassa en sida genom den anpassningsbanderollen](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

  3. Välj **Åtgärder**, sedan **Bokföring** och sedan väljer du **Bokför**.  
  4. Tryck på knappen **Ja**.  

## <a name="creating-the-sales-order"></a>Skapar försäljningsreturordern

Försäljningsorder är den vanligaste typen för utgående källdokumentet.  

### <a name="to-create-the-sales-order"></a>Så här skapar du försäljningsreturordern

1. Välj den ![Glödlampa som öppnar funktionen Berätta tredje.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Skapa en försäljningsorder för kund 10000 på arbetsdatumet (23 januari) med följande försäljningsorderrad.  

    |Artikel|Lagerställekod|Antal|  
    |----|-------------|--------|  
    |1928-S|SYD|30|  

     Fortsätt med att meddela lagret att försäljningsordern är klar för lagerhantering.  

4. Välj åtgärden **Släppa**.  

    Anders fortsätter att plocka och leverera de sålda artiklarna.  

## <a name="picking-and-shipping-items"></a>Plocka och leverera artiklar

På sidan **Lagerplockning** kan du hantera alla utgående distributionslageraktiviteter för ett särskilt källdokument, t.ex en försäljningsorder. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a>Plocka och utleverera artiklar så här

1. Välj den ![Glödlampa som öppnar funktionen Berätta fjärde.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **lagerplockning** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  

    Kontrollera att fältet **Nr.** fälten på snabbfliken **Allmänt** fylls i.
3. Välj fältet **Källdokument** och sedan **Försäljningsorder**.  
4. Välj fältet **Ursprungsnr.**, markera raden för försäljningen till kund 10000 och välj sedan knappen **OK**.  

    Välj alternativt åtgärden **Hämta källdokument** och välj sedan försäljningsordern.  
5. Välj åtgärden **Fyll i auto. ant. att hantera**.  

    Alternativt, ange 10 respektive 20 i fältet **Ant. att hantera** på de två lagerplockningsraderna.  
6. Välj åtgärden **bokför**, välj **leverera**, och välj sedan **OK**-knappen.  

    De 30 Amsterdam-lamporna har nu registrerats som plockade från lagerställen S-01-0001 och S-01-0002, och en negativ artikeltransaktion skapas som återspeglar den bokförda leveransen.  

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
