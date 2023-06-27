---
title: Inleverera och införa i avancerad lagerstyrning
description: De inkommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a>Genomgång: Inleverera och införa utflöde i avancerade lagerkonfigurationer

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

I [!INCLUDE[prod_short](includes/prod_short.md)] sker mottagning och införsel med någon av fyra metoder, enligt beskrivningen i följande tabell.

|Metod|inkommande behandling|Begär inleverans|Begär artikelinförsel|Komplexitetsnivå (mer information på [Warehouse Management – översikt](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bokföra inleverans och lagerinförsel från orderraden|||Ingen tilldelad distributionslageraktivitet.|  
|B|Bokföra inleverans och lagerinförsel från ett lagerinförseldokument||Aktiverat|Grundläggande: Order för order|  
|A|Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument|Aktiverat||Grundläggande: Konsoliderad inleverans-/utleveransbokföring för flera order.|  
|D|Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument|Aktiverat|Aktiverat|Avancerat|  

Läs mer i [Inkommande distributionslagerflöde](design-details-inbound-warehouse-flow.md).

Efterföljande genomgången visar metod D i föregående tabellen.  

## <a name="about-this-walkthrough"></a>Om den här genomgången

För avancerad lagerkonfigurationer där lagerstället har konfigurerats att kräva mottagningsbehandling, förutom artikelinförselbehandling, använder du sidan **Dist.lager inleverans** för att registrera och bokföra kvittot med artiklar för flera inkommande order. När lagerinleveransen bokförs, skapas en eller flera av artikelinförseldokument för att instruera lagerarbetare att ta det mottagna artikeln och placera dem på avsedda ställen enligt lagerplatsinställning eller i andra lagerställen. Den specifika placering av artiklarna registreras, när lagerartikelinförseln är registrerade. Det inkommande källdokumentet kan vara en inköpsorder, försäljningsreturorder, inkommande överföringsorder eller montering eller produktionsorder vars utflöde är klart för artikelinförsel. Om kvittot skapas från en inkommande beställning, kan mer än en inkommande källdokument hämtas för kvittot. Genom att använda den här metoden, kan du registrera många artiklar som inlevereras från olika inkommande beställningar med ett kvitto.  

I den här genomgången tas följande aktiviteter upp:  

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

-   CRONUS installerad.  
-   Om du vill Ange dig själv som distributionslagerpersonal på lagerstället VIT följer du de här stegen:  

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **distributionslagerpersonal** och väljer sedan relaterad länk.  
2.  Välj fältet **Användar-ID** och välj ditt eget användarkonto på sidan **Användare**.  
3.  Ange WHITE i fältet **Lagerställekod**.  
4.  Välj fältet **Standard**.  

## <a name="story"></a>Situation

Ellen, lagerchef på CRONUS skapar två inköpsorder för tillbehörsartiklar från leverantörerna 10000 och 20000 som ska levereras till distributionslagret VIT. När leveranserna inlevereras till lagret använder Sammy, som är ansvarig för att ta emot artiklar från leverantörer 10000 och 20000, ett filter för att skapa inleveransrader för inköpsorder som inlevereras från de två leverantörerna. Sammy bokför artiklar som inlevererade till lagret i en lagerinleverans och artiklarna blir tillgängliga till försäljning eller andra behov. Anders lagerarbetaren, tar artiklarna från mottagande lagerstället och för in dem. Han flyttar alla enheter i sina standardlagerställen, utom 40 av 100 inlevererade gångjärn, som han flyttar till monteringsavdelningen genom att dela, artikelinförselraden. När Anders registrerar artikelinförsel, uppdateras lagerställesinnehållen, och artiklarna blir tillgängliga för plockning från lagret.  

## <a name="reviewing-the-white-location-setup"></a>Granska konfigurationen av VITA platsen

Inställningen av sidan **Lagerställekort** definierar företagets lagerflöden.  

### <a name="to-review-the-location-setup"></a>Om du vill granska lagerställekonfigurationen

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
2.  Öppna lagerställekortet VIT.  
3.  Observera på snabbfliken **Dist.lager** att kryssrutan **dirigerad artikelinförsel och plockning** är markerad.  

    Det betyder att lagerstället ställts in för den högsta komplexitetsnivån, reflekterat av faktumet att alla kryssrutor för lagerhantering på snabbfliken är markerade.  

4.  Observera att på snabbfliken **Lagerställen** att lagerställen anges i fälten **Inlevns lagerställeskod** och **Utlevns lagerställeskod**.  

Det betyder att, när du skapar en distributionslagerinleverans, den här lagerställeskoden kopieras till huvudet på den distributionslagerinleveransdokument som standard, och till raderna i de resulterande distributionslagerartikelinförslar.  

## <a name="creating-the-purchase-orders"></a>Skapa inköpsorder

Inköpsorder är den vanligaste typen för inkommande källdokumentet.  

### <a name="to-create-the-purchase-orders"></a>Så här Skapa inköpsorder

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3.  Skapa en inköpsorder för leverantör 10000 på arbetsdatumet (23 januari) med följande inköpsorderrader.  

    |Artikel|Lagerställekod|Antal|  
    |----------|-------------------|--------------|  
    |70200|VIT|100 STYCK|  
    |70201|VIT|50 STYCK|  

    Fortsätt med att meddela lagret att inköpsordern är klar för lagerhantering när leverans anländer.  

4.  Välj åtgärden **Frisläpp**. Statusen ändras från öppen till släppt.

    Fortsätt att skapa den andra inköpsordern.  

5.  Välj åtgärden **Ny**.  
6.  Skapa en inköpsorder för leverantör 20000 på arbetsdatumet (23 januari) med följande inköpsorderrader.  

    |Artikel|Lagerställekod|Antal|  
    |----------|-------------------|--------------|  
    |70100|VIT|10 CAN|  
    |70101|VIT|12 CAN|  

    Välj åtgärden **Frisläpp**. Statusen ändras från öppen till släppt.

    Leveranserna av artiklar från leverantörer 10000 och 20000 har anlänt till det VITA lagret, och Sammy börjar behandla inköpsleveranserna.  

## <a name="receiving-the-items"></a>Ta emot artiklarna

På sidan **Dist.lager inleverans** kan du hantera flera inkommande order för källdokument, t.ex en inköpsorder.  

### <a name="to-receive-the-items"></a>Så här inlevererar du artiklarna
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Dist.lager inleveranser** och väljer sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3.  Ange WHITE i fältet **Lagerställekod**.  
4.  Välj **Åtgärder** i gruppen **Funktioner** och välj åtgärden **Filter för att hämta urspr.dok**.  
5.  Ange **ACCESSORY** i fältet **Kod**.  
6.  I fältet **Beskrivning** anger du **Leverantörer 10000 och 20000**.  
7.  Välj åtgärden **Ändra**.  
8.  På snabbfliken **inköp** i fältet **Inköpsleverantörsnrfilter** anger du **10000&#124;20000**.  
9. Välj åtgärden **Kör**. lagerinleveransen är fylld med fyra rader som representerar inköpsorderrader för de angivna leverantörerna. Fältet **Ant. att inlevereras** är fyllt, eftersom du inte valde kryssrutan **Fyll inte i ant. att hantera** på sidan **Filter att hämta ursprungsdok.**.  
10. Alternativt om du vill använda ett filter på det sätt som beskrivs tidigare i det avsnitt, välj åtgärden **Hämta källdokument** och välj sedan inköpsorder från leverantörerna i fråga.  
11. Välj **Bokföra** och sedan **Bokföra inleverans** och sedan knappen **Ja**.  

    Positiva artikeltransaktioner skapas som återspeglar de bokförda inköpsleveranserna av utrustning från leverantörerna 10000 och 20000, och artiklar är klara att föras in i distributionslagret från den mottagande lagerstället.  

## <a name="putting-the-items-away"></a>Föra in artiklar i lagret

På sidan **Dist.lager artikelinförsel** kan du hantera artikelinförslar för ett specifikt distributionslagerinleveransdokument som täcker flera källdokument. Som alla dist.lageraktivitetdokument representeras varje artikel på dist.lager artikelinförsel av en taganderad och en platsrad. I följande procedur är lagerställeskoden på hämtningsraderna standardlagerstället för inleveranser vid lagerställe VIT, W-08-0001.  


### <a name="to-put-the-items-away"></a>Så här för du in artiklarna
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **artikelinförsel** och väljer sedan relaterad länk.  
2.  Välj det enda distributionslagerinförseldokumentet i listan, och välj sedan åtgärden **Redigera**.  

    Distributionslagerinförseldokumentet öppnas med totalt åtta Ta- eller Placerarader för de fyra inköpsorderrader.

    Lagerarbetaren har fått informationen att 40 gångjärn behövs i monteringavdelningen, och han fortsätter att dela upp den enda placeraraden för lagerstället W-02-0001 i monteringavdelningen där distributionslagerarbetaren placerar den delen av de inlevererade gångjärnen.  

3.  Välj den andra raden på sidan **Dist.lager artikelinförsel** fönstret, raden Plats för artikel 70200.  
4.  I fältet **Antal att hantera** ändra värdet från 100 till 60.  
5.  På snabbfliken **Rader** väljer du **Funktioner** och sedan **dela rad**. En ny rad infogas för artikel 70200 med 40 i fältet **Ant. att hantera**.  
6.  Ange W-02-0001 i fältet **lagerställeskod**. Fältet **Zonkod** fylls i automatiskt.  

    Som standard är fältet **Zonplatskod** på försäljningsraderna dolt, så du måste visa det. För att göra detta måste du anpassa sidan. Mer information finns i [Så här börjar du anpassa en sida genom den anpassningsbanderollen](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

    Fortsätt med att registrera artikelinförseln.  

7.  Välj åtgärden **Registrera artikelinförsel** och sedan knappen **Ja**.  

    Mottagna tillbehör utgör nu artikelinförsel i artikelns standardlagerställen, och 40 gångjärn placeras i monteringavdelningen. De inlevererade artiklarna är nu tillgängliga för plockning till intern efterfrågan, till exempel monteringsorder eller till extern efterfrågan, till exempel försäljningsutleveranser.  

## <a name="see-also"></a>Se även
 [Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Designdetaljer: inkommande distributionslagerflöde](design-details-inbound-warehouse-flow.md)   
 <!-- [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)    -->
 [Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
