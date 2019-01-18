---
title: "Inleverera och införa utflöde i avancerad lagerstyrning | Microsoft Docs"
description: "I Business Central kan de inkommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktioner beroende på lagerkomplexitetsnivå."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 651ec85ead0859b5be34e624c47331292958e4db
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a>Genomgång: Inleverera och införa utflöde i avancerade lagerkonfigurationer
I [!INCLUDE[d365fin](includes/d365fin_md.md)], kan de inkommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.  

|Metod|Ankommande behandling|Lagerplatser|Inleveranser|Artikelinförslar|Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokföra inleverans och lagerinförsel från orderraden|INTER|||2|  
|B|Bokföra inleverans och lagerinförsel från ett lagerinförseldokument|||X|3|  
|L|Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument||X||6-4-5|  
|D|Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument||INTER|INTER|6-4-5|  

Mer information finns i [Designdetaljer: Ingående distributionslagerflöde](design-details-inbound-warehouse-flow.md).  

Efterföljande genomgången visar metod D i föregående tabellen.  

## <a name="about-this-walkthrough"></a>Om den här genomgången  
För avancerad lagerkonfigurationer där lagerstället har konfigurerats att kräva mottagningsbehandling, förutom artikelinförselbehandling, använder du sidan **Dist.lager inleverans** för att registrera och bokföra kvittot med artiklar för flera ankommande order. När lagerinleveransen bokförs, skapas en eller flera av artikelinförseldokument för att instruera lagerarbetare att ta det mottagna artikeln och placera dem på avsedda ställen enligt lagerplatsinställning eller i andra lagerplatser. Den specifika placering av artiklarna registreras, när lagerartikelinförseln är registrerade. Det ankommande källdokumentet kan vara en inköpsorder, försäljningsreturorder, ankommande överföringsorder eller montering eller produktionsorder vars utflöde är klart för artikelinförsel. Om kvittot skapas från en ankommande beställning, kan mer än en ankommande källdokument hämtas för kvittot. Genom att använda den här metoden, kan du registrera många artiklar som inlevereras från olika inkommande beställningar med ett kvitto.  

I den här genomgången tas följande uppgifter upp.  

-   Ställa in VIT lagerställe för mottagning och införsel.  
-   Skapa och släppa två inköpsorder för fullständig lagerhantering.  
-   Skapa och bokför ett distributionslagerinleveransdokument för åtskilliga inköpsorderrader från vissa leverantörer.  
-   Registrering av en lagerartikelinförsel för de inlevererade artiklarna.  

## <a name="roles"></a>Roller  
Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:  

-   Dist.lagerchef  
-   Inköpsagent  
-   Mottagande personal  
-   Lagerarbetare  

## <a name="prerequisites"></a>Förutsättningar  
För att kunna utföra den här genomgången behöver du:  

-   CRONUS Sverige AB installerad  
-   Om du vill Ange dig själv som distributionslagerpersonal på lagerstället VIT följer du de här stegen:  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Dist.lager personal** och välj sedan relaterad länk.  
2.  Välj fältet **Användar-ID** och välj ditt eget användarkonto på sidan **Användare**.  
3.  Ange WHITE i fältet **Lagerställekod**.  
4.  Välj fältet **Standard**.  

## <a name="story"></a>Situation  
Ellen, lagerchef på CRONUS skapar två inköpsorder för tillbehörsartiklar från leverantörerna 10000 och 20000 som ska levereras till distributionslagret VIT. När leveranserna inlevereras till lagret använder Sammy, som är ansvarig för att ta emot artiklar från leverantörer 10000 och 20000, ett filter för att skapa inleveransrader för inköpsorder som inlevereras från de två leverantörerna. Sammy bokför artiklar som inlevererade till lagret i en lagerinleverans och artiklarna blir tillgängliga till försäljning eller andra behov. Anders lagerarbetaren, tar artiklarna från mottagande lagerplatsen och för in dem. Han flyttar alla enheter i sina standardlagerplatser, utom 40 av 100 inlevererade gångjärn, som han flyttar till monteringsavdelningen genom att dela, artikelinförselraden. När Anders registrerar artikelinförsel, uppdateras lagerplatsinnehållen, och artiklarna blir tillgängliga för plockning från lagret.  

## <a name="reviewing-the-white-location-setup"></a>Granska konfigurationen av VITA platsen  
Inställningen av sidan **Lagerställekort** definierar företagets lagerflöden.  

### <a name="to-review-the-location-setup"></a>Om du vill granska lagerställekonfigurationen  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Platser** och välj sedan relaterad länk.  
2.  Öppna lagerställekortet VIT.  
3.  Observera på snabbfliken **Dist.lager** att kryssrutan **dirigerad artikelinförsel och plockning** är markerad.  

    Det betyder att lagerstället ställts in för den högsta komplexitetsnivån, reflekterat av faktumet att alla kryssrutor för lagerhantering på snabbfliken är markerade.  

4.  Observera att på snabbfliken **Lagerplatser** att lagerplatser anges i fälten **Inlevns lagerplatskod** och **Utlevns lagerplatskod**.  

Det betyder att, när du skapar en distributionslagerinleverans, den här lagerplatskoden kopieras till huvudet på den distributionslagerinleveransdokument som standard, och till raderna i de resulterande distributionslagerartikelinförslar.  

## <a name="creating-the-purchase-orders"></a>Skapa inköpsorder  
Inköpsorder är den vanligaste typen för inkommande källdokumentet.  

### <a name="to-create-the-purchase-orders"></a>Så här Skapa inköpsorder  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsorder** och välj sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3.  Skapa en inköpsorder för leverantör 10000 på arbetsdatumet (23 januari) med följande inköpsorderrader.  

    |Artikel|Lagerställekod|Antal|  
    |----------|-------------------|--------------|  
    |70200|VIT|100 STYCK|  
    |70201|VIT|50 STYCK|  

    Fortsätt med att meddela lagret att inköpsordern är klar för lagerhantering när leverans anländer.  

4.  Välj åtgärden **Släppa**.  

    Fortsätt att skapa den andra inköpsordern.  

5.  Välj åtgärden **Ny**.  
6.  Skapa en inköpsorder för leverantör 20000 på arbetsdatumet med följande inköpsorderrader.  

    |Artikel|Lagerställekod|Antal|  
    |----------|-------------------|--------------|  
    |70100|VIT|10 CAN|  
    |70101|VIT|12 CAN|  

    Välj åtgärden **Släppa**.  

    Leveranserna av artiklar från leverantörer 10000 och 20000 har anlänt till det VITA lagret, och Sammy börjar behandla inköpsleveranserna.  

## <a name="receiving-the-items"></a>Ta emot artiklarna  
På sidan **Dist.lager inleverans** kan du hantera flera inkommande order för källdokument, t.ex en inköpsorder.  

### <a name="to-receive-the-items"></a>Så här inlevererar du artiklarna  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Dist.lager inleveranser** och välj sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3.  Ange WHITE i fältet **Lagerställekod**.  
4.  Välj åtgärden **Filter för att hämta urspr.dok.**.  
5.  Ange **ACCESSORY** i fältet **Kod**.  
6.  I fältet **Beskrivning** anger du **Leverantörer 10000 och 20000**.  
7.  Välj åtgärden **Ändra**.  
8.  På snabbfliken **inköp** i fältet **Inköpsleverantörsnrfilter** anger du **10000&#124;20000**.  
9. Välj åtgärden **Kör**. lagerinleveransen är fylld med fyra rader som representerar inköpsorderrader för de angivna leverantörerna. Fältet **Ant. att inlevereras** är fyllt, eftersom du inte valde kryssrutan **Fyll inte i ant. att hantera** på sidan **Filter att hämta ursprungsdok.**.  
10. Alternativt om du vill använda ett filter på det sätt som beskrivs tidigare i det avsnitt, välj åtgärden **Hämta källdokument** och välj sedan inköpsorder från leverantörerna i fråga.  
11. Välj åtgärden **Bokföra inleverans** och sedan knappen **Ja**.  

    Positiva artikeltransaktioner skapas som återspeglar de bokförda inköpsleveranserna av utrustning från leverantörerna 10000 och 20000, och artiklar är klara att föras in i distributionslagret från den mottagande lagerplatsen.  

## <a name="putting-the-items-away"></a>Föra in artiklar i lagret  
På sidan **Dist.lager artikelinförsel** kan du hantera artikelinförslar för ett specifikt distributionslagerinleveransdokument som täcker flera källdokument. Som alla dist.lageraktivitetdokument representeras varje artikel på dist.lager artikelinförsel av en taganderad och en platsrad. I följande procedur är lagerplatskoden på hämtningsraderna standardlagerplatsen för inleveranser vid lagerställe VIT, W-08-0001.  

### <a name="to-put-the-items-away"></a>Så här för du in artiklarna  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artikelinförslar** och välj sedan relaterad länk.  
2.  Välj det enda distributionslagerinförseldokumentet i listan, och sedan, på **Startsida** fliken, i **Hantera** grupp, välj **Redigera**.  

    Distributionslagerinförseldokumentet öppnas med totalt åtta Ta- eller Placerarader för de fyra inköpsorderrader.

    Lagerarbetaren har fått informationen att 40 gångjärn behövs i monteringavdelningen, och han fortsätter att dela upp den enda placeraraden för lagerplatsen W-02-0001 i monteringavdelningen där han placerar den delen av de inlevererade gångjärnen.  

3.  Välj den andra raden på sidan **Dist.lager artikelinförsel** fönstret, raden Plats för artikel 70200.  
4.  I fältet **Antal att hantera** ändra värdet från 100 till 60.  
5.  På snabbfliken **Rader** väljer du **Funktioner** och sedan **dela rad**. En ny rad infogas för artikel 70200 med 40 i fältet **Ant. att hantera**.  
6.  Ange W-02-0001 i fältet **lagerplatskod**. Fältet **Zonkod** fylls i automatiskt.  

    Fortsätt med att registrera artikelinförseln.  

7.  Välj åtgärden **Registrera artikelinförsel** och sedan knappen **Ja**.  

    Mottagna tillbehör är nu införda i artikelns standardlagerplatser, och 40 gångjärn placeras i monteringavdelningen. De inlevererade artiklarna är nu tillgängliga för plockning till intern efterfrågan, till exempel monteringsorder eller till extern efterfrågan, till exempel försäljningsutleveranser.  

## <a name="see-also"></a>Se även  
 [Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Designdetaljer: Ankommande distributionslagerflöde](design-details-inbound-warehouse-flow.md)   
 [Genomgång: Inleverera och införa utflöde i grundläggande lagerkonfigurationer](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)   
 [Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)

