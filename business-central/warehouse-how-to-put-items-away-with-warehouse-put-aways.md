---
title: Så här inför du artiklar med dist.lager artikelinförsel
description: Lära dig mer om olika sätt att använda distributionslagerinförslar när du vill föra in inlevererade artiklar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/24/2023
ms.custom: bap-template
ms.search.forms: '7352, 7333'
---
# Föra in artiklar med lagerartikelinförsel

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du ta emot objekt och lägga undan dem med någon av fyra metoder, enligt beskrivningen i följande tabell.

|Metod|inkommande behandling|Begär inleverans|Begär artikelinförsel|Komplexitetsnivå (mer information på [Warehouse Management – översikt](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bokföra inleverans och lagerinförsel från orderraden|||Ingen tilldelad distributionslageraktivitet.|  
|B|Bokföra inleverans och lagerinförsel från ett lagerinförseldokument||Aktiverat|Grundläggande: Order för order|  
|A|Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument|Aktiverat||Grundläggande: Konsoliderad inleverans-/utleveransbokföring för flera order.|  
|D|Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument|Aktiverat|Aktiverat|Avancerat|  

Läs mer i [Inkommande distributionslagerflöde](design-details-inbound-warehouse-flow.md).

I den här artikeln hänvisas till metod D i tabellen och det antas att mottagning redan har skett. Läs mer på [Ta emot artiklar](warehouse-how-receive-items.md).

När lagerstället ställs in krävs både inleverans- och artikelinförselbearbetning för distributionslagret använder du funktionen för distributionslagerdokument för artikelinförsel för att styra hur artiklar införs. När du bokför en distributionslagerinleverans uppdateras källdokument som inköp, inkommande överföringar eller försäljningsreturorder. Den inlevererade kvantiteten bokförs i artikeltransaktioner och raderna för de inlevererade artiklarna skickas till artikelinförselfunktionen i distributionslagret.

Beroende på värdet i fältet **Använd artikelinförselkalkylark** i **Lagerställekort**, görs raderna antingen tillgängliga för artikelinförselkalkylarket eller används för att generera artikelinförseldokumenten omedelbart. Läs mer på [Ställa in lagerstyrning](warehouse-setup-warehouse.md).  

Förutom standardsätten att skapa artikelinförslar i distributionslagret, som beskrivs i den här artikeln, kan du skapa en artikelinförsel från den relaterade bokförda distributionslagerinleveransen. Detta är användbart om har tagit bort artikelinförselrader, eller om du bestämmer dig för att inte använda artikelinförselkalkylarket, kan du skapa eller på nytt skapa artikelinförselanvisningar för bokförda inleveransrader.

## Zon och lagerplatskoder

Vid lagerställen som är inställt på dirigerad artikelinförsel och plockning, följande inställningar är krävs för att bestämma den bästa platsen att föra in artiklarna:  

* En artikelinförselmall skapas. Mer information finns i [Skapa artikelinförselsmallar](warehouse-how-to-set-up-put-away-templates.md).  
* Vikten, volymen och särskilda lagerkrav för artikeln eller lagerställeenheten definieras.
* Kapaciteten, typ av lagerplats och lagerplatsordning definieras för lagerplatserna.  

Lagerplatsordning används när mer än en lagerplats matchar kriterierna i artikelinförselmallen. Om både villkoren i artikelinförselmallen och lagerplatsordningen är samma för fler än en lagerplats väljs den lagerplats som har högst nummer.

## Så här skapar du artikelinförseldokumenten i bulk med artikelinförselkalkylarket  

Du kan skapa artikelinförseldokumenten för flera inleveranser samtidigt på sidan för **artikelinförselkalkylarket**.  

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artikelinförselkalkylarket** och väljer sedan relaterad länk.  
2. Välj åtgärden **Hämta dist.lager dokument**. Sidan **Artikelinförselval** öppnas.  

    Listan innehåller alla bokförda inleveranser som är färdiga att föras in, inklusive sådana som har skapats för vilka artikelinförselinstruktioner redan har skapats. Dokument med artikelinförselrader som är klara och registrerade visas inte i den här listan.  
3. Välj de dokument som du vill arbeta med. Du kan arbeta med rader från flera dokument samtidigt.  

    > [!NOTE]  
    >  Om du försöker välja ett inleverans- eller intern artikelinförseldokument, som du redan har skapat instruktioner för alla rader [!INCLUDE[prod_short](includes/prod_short.md)]] får du information om att det inte finns någonting att hantera.  

4. Fyll i fältet **Sorteringsmetod** för att sortera raderna.  

    > [!NOTE]  
    >  Hur raderna sorteras i förslaget överförs inte automatiskt till artikelinförselinstruktionen. Samma möjligheter för sortering och lagerplatsordning finns dock. Du kan återskapa radsortering som du planerar i kalkylarket när du skapar artikelinförselinstruktioner, eller genom att sortera artikelinförselinstruktionerna.

5. Fyll i fältet **Ant. att hantera**. Välj åtgärden **Fyll i auto. ant. att hantera** eller fyll i fälten manuellt.  
6. Du kan redigera raderna manuellt efter behov. Du kan ta bort rader om exempelvis vissa artiklar måste föras in på en lagerplats som ligger långt bort från övriga artiklars lagerställen.  

    > [!NOTE]  
    > När du tar bort rader tas de bara bort från det här kalkylbladet. De tas inte bort från urvalet av artikelinförslar.  

7. Välj åtgärden **Skapa artikelinförsel**. Sidan **Skapa dokument** öppnas, där kan du lägga till ytterligare information i artikelinförseln som du skapar.  

    * Du kan fördela artikelinförseln till en särskild anställd.  
    * Du kan sortera instruktionsraderna för artikelinförsel som du gjorde i kalkylarket eller genom att använda funktionen Lagerplatsordning. När du sorterar efter lagerplatsordning, visas *Ta* rader visas först, eftersom de flesta inleveranslagerställen har rankningen 0. Raderna *Placera* visas sist, med början med de lagerplatser med lägst lagerplatsordning. Om du har strukturerat distributionslagret så att lagerställen med liknande lagerplatsordning ligger bredvid varandra slipper personalen gå så mycket om du sorterar raderna på det här sättet.  
    * Du kan välja att inte visa de rader som [!INCLUDE[prod_short](includes/prod_short.md)]] skapade när den konverterade en stor måttenhet till mindre måttenheter genom att välja den arkiverade **Sätt brytenhetsfilter**. Mer information finns i [Aktivera automatisk volymnedbrytning med dirigerad artikelinförsel och plockning](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    * Du kan välja att inte låta fältet **Ant. att hantera** fyllas i automatiskt för artikelinförselinstruktionerna.  
    * Du kan välja att skriva ut dokumentet omedelbart.  

8. Välj **OK** för att skapa artikelinförsel.  

## Att skapa en artikelinförsel från en bokförd inleveransen

Om man använder både bearbetning av artikelinförsel och inleverans för lagerstället, måste du ta bort artikelinförselrader. Om du använder dirigerad artikelinförsel och plockning och har bestämt dig för att inte använda artikelinförselförslaget, kan du skapa eller på nytt skapa artikelinförselanvisningar för bokförda inleveransrader.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bokförda distributionslagerinleveranser** och väljer sedan relaterad länk.  
2. Välj en bokförd inleverans att föra in.  
3. Välj åtgärden **Kort**.  

    Om fältet **Dokumentstatus** är tomt har inleveransen inte förts in alls. Annars visar det här fältet om inleverans är del- eller färdig artikelinförsel.  

4. Om inleveransen har införts delvis eller inte alls väljer du åtgärden **Skapa artikelinförsel**.  
5. Fyll i fälten på efter behov och välj sedan knappen **OK**.  

## Att införa artiklar

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Lagerartikelinförsel** och väljer sedan relaterad länk.

2. Öppna dist.lager artikelinförsel som är klara att hantera.  
3. Om distributionslagret kräver det anger du ditt användar-ID när du börjar arbeta med artikelinförsel.  

    Du kan sortera Artikelinförselrader efter flera villkor, till exempel efter artikel, hyllnummer eller förfallodatum. Sortering kan hjälpa till att optimera processen för artikelinförsel, till exempel:

    * Om raderna för Ta och Placera för varje inleveransrad inte visas direkt efter varandra och det är så du vill att de ska visas, kan du sortera raderna genom att välja **Artikel** i fältet **Sorteringsmetod**.  
    * Om lagerplatsordning återspeglar lagrets fysiska layout, använd sorteringsmetoden **Lagerplatsordning** för att organisera arbetet efter lagerplatser.

4. Utför åtgärder.

    Om en lagerplatskod är obligatorisk för lagerställena, blir varje inleveransrad minst två rader i dist.lager artikelinförsel, enligt följande.  

    * Den första raden, med **Ta** i fältet **Åtgärdstyp**, anger var artiklarna finns i inleveransområdet. Du kan inte ändra zon- och lagerplatsfältet på den här raden.  
    * Nästa rad, med fältet **Plats** i **Åtgärdstyp**, anger var du måste placera artiklarna i distributionslager. Om du har fått ett stort antal artiklar på en enda inleveransrad, kanske artiklarna måste föras in på flera lagerställen, så det finns en Plats rad för varje lagerplats. 

    > [!NOTE]
    > Om du måste placera artiklar för en rad på flera lagerställen, t.ex. om den utsedda lagerplatsen är full, använder du funktionen **Dela rad**, på snabbfliken **Rader**. Åtgärden skapar en rad för återstående antal att hantera.

5. När du har placerat alla artiklarna på lagerställen enligt anvisningarna, välj åtgärden **Registrera artikelinförsel**.  

## Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
