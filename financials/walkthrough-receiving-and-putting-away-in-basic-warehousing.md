---
title: "Genomgång: Inleverera och införa utflöde i grundläggande lagerkonfigurationer | Microsoft Docs"
description: "I Dynamics 365 kan de ankommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 52b017591b389c883e8a0bbeb35c1e3a3a9e7377
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Genomgång: Inleverera och införa utflöde i grundläggande lagerkonfigurationer
I [!INCLUDE[d365fin](includes/d365fin_md.md)], kan de inkommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.  

|Metod|Ankommande behandling|Lagerplatser|Inleveranser|Artikelinförslar|Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokföra inleverans och lagerinförsel från orderraden|INTER|||2|  
|B|Bokföra inleverans och lagerinförsel från ett lagerinförseldokument|||X|3|  
|L|Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument||X||6-4-5|  
|D|Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument||INTER|INTER|6-4-5|  

Mer information finns i [Designdetaljer: Ingående distributionslagerflöde](design-details-inbound-warehouse-flow.md).  

Efterföljande genomgången visar metod B i föregående tabellen.  

## <a name="about-this-walkthrough"></a>Om den här genomgången  
För grundläggande lagerkonfiguration där lagerstället har konfigurerats att kräva artikelinförselbearbetning men inte mottagningsbearbetning, använder du fönstret **Lagerinförsel** för att registrera och bokföra artikelinförsel- och mottagningsinformation för dina ankommande källdokument. Det ankommande källdokumentet kan vara en inköpsorder, försäljningsreturorder, ankommande överföringsorder eller produktionsorder vars utflöde är klart för artikelinförsel.

> [!NOTE]
> Även om inställningarna kallas **Begär plockning** och **Begär artikelinförsel**, kan du fortfarande bokföra inleveranser och utleveranser direkt från affärskälldokument på platser där du markerar dessa kryssrutor.  

I den här genomgången tas följande uppgifter upp.  

-   Lägger upp lagerstället SILVER för lagerinförsel.  
-   Lägger upp lagerstället SILVER för lagerplatshantering.  
-   Definierar en standardlagerplats för artikeln LS-81. (LS-75 redan inställd i CRONUS.)  
-   Skapa en inköpsorder för leverantör 10000 på 40 högtalare.  
-   Kontrollera att införsel-lagerplatserna förinställs av inställningarna.  
-   Släppa inköpsordern för lagerhantering.  
-   Skapa en lagerinförsel som baseras på ett släppt källdokument.  
-   Kontrollera att införsel-lagerplatserna hämtas från inköpsorder.  
-   Registrering av lagerrörelsen till lagret och samtidigt bokföra inköpsinleveransen för källinköpsorder.  

## <a name="roles"></a>Roller  
Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:  

-   Dist.lagerchef  
-   Inköpsagent  
-   Lagerarbetare  

## <a name="prerequisites"></a>Förutsättningar  
För att kunna utföra den här genomgången behöver du:  

-   CRONUS Sverige AB installerad  
-   Gör dig själv till distributionslageranvändare på lagerstället SILVER med följande steg:  

    1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Dist.lager personal** och välj sedan relaterad länk.  
    2.  Välj fältet **Användar-ID** och välj ditt eget användarkonto i fönstret **Användare**.  
    3.  Ange SILVER i fältet **Lagerställekod**.  
    4.  Välj fältet **Standard**.  

## <a name="story"></a>Situation  
Alicia, inköpsagenten i CRONUS, skapar en inköpsorder för 10 enheter av artikeln LS-75 och 30 enheter av artikeln LS-81 från leverantör 10000 som ska levereras till distributionslagret SILVER. När leveransen inlevereras till lagret placerar Anders, lagerarbetaren, artiklarna i standardlagerplatser som definieras för artiklarna. När Anders bokför artikelinförseln, bokförs artiklarna som inlevererade till lagret och som tillgängligt för försäljning eller andra behov.  

## <a name="setting-up-the-location"></a>Lägger upp lagerstället  
 Inställningen av fönstret **Lagerställekort** definierar företagets lagerflöden.  

### <a name="to-set-up-the-location"></a>Så här lägger du upp lagerställen  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.  
2.  Öppna lagerställekortet SILVER.  
3.  Markera kryssrutan **Begär artikelinförsel**.  

    Fortsätt med att lägga upp en standardlagerplats för de två artikelnumren för att styra var de ska föras in.  

4.  Välj åtgärden **Lagerplatser**.  
5.  Markera den första raden för lagerplatsinnehållet S-01-0001, och välj sedan åtgärden **innehåll**.  

    Lägg märke till att i fönstret **Lagerplatsinnehåll** har artikeln LS-75 redan lagts upp som innehåll i lagerplatsen S-01-0001.  

6.  Välj åtgärden **Ny**.  
7.  Markera fälten **Fast** och **Standard**.  
8.  I fältet **Verifikationsnr.** anger du LS-81.  

## <a name="creating-the-purchase-order"></a>Skapar inköpsordern  
Inköpsorder är den vanligaste typen för inkommande källdokumentet.  

### <a name="to-create-the-purchase-order"></a>Skapa inköpsordern  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsorder** och välj sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3.  Skapa en inköpsorder för leverantör 10000 på arbetsdatumet (23 januari) med följande inköpsorderrader.  

    |Artikel|Lagerställekod|Lagerplatskod|Antal|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|SILVER|S-01-0001|10|  
    |LS-81|SILVER|S-01-0001|30|  

    > [!NOTE]  
    >  Lagerplatskod anges automatiskt i överensstämmelse med inställningar som du har utfört i avsnittet ”Skapa lagerplatsen”.  

    Fortsätt med att meddela lagret att inköpsordern är klar för lagerhantering när leverans anländer.  

4.  Välj åtgärden **Släppa**.  

    Leverans av högtalare från leverantör 10000 har anlänt till SILVERLAGRET, och Anders fortsätter att föra in dem.  

## <a name="receiving-and-putting-the-items-away"></a>Ta emot och föra in artiklar i lagret  
I fönstret **Lagerinförsel** kan du hantera alla ingående distributionslageraktiviteter för ett särskilt källdokument, t.ex en inköpsorder.  

### <a name="to-receive-and-put-the-items-away"></a>Så här tar du emot och för in artiklar  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerinförslar** och välj sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3.  Välj fältet **Källdokument** och sedan **Inköpsorder**.  
4.  Välj fältet **Källnr.** markera raden för köpet från leverantör 10000 och välj sedan knappen **OK**.  

    Alternativ: Välj **Hämta källdokument** och välj sedan inköpsorder på fliken **Åtgärder** i gruppen **Funktioner**.  

5.  Välj åtgärden **Fyll i auto. ant. att hantera**.  

    Alternativt, ange 10 respektive 30 i fältet **Ant. att hantera** på de två lagerinförselraderna.  

6.  Välj åtgärden **bokför**, välj åtgärden **inleverera**, och välj sedan **OK**-knappen.  

    De 40 högtalarna har nu registrerats som införda på lagerplatser S-01-0001 och en positiv artikeltransaktion skapas som återspeglar den bokförda inköpsinleveransraden.  

## <a name="see-also"></a>Se även  
 [Så här: Införa artiklar med lagerartikelinförslar](warehouse-how-to-put-items-away-with-inventory-put-aways.md)   
 [Så här: Ställa in grundläggande dist.lager med operationsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Så här: Flytta komponenter till ett operationsområde i grundläggande lagerkonfiguration](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Så här: Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md)   
 [Så här flyttar du artiklar ad hoc i grundläggande lagerkonfiguration](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Designdetaljer: Ankommande distributionslagerflöde](design-details-inbound-warehouse-flow.md)   
 [Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

