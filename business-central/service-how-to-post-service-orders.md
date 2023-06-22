---
title: Så här bokför du serviceorder
description: 'När du har skapat en serviceorder, fyllt i all nödvändig information och gjort eventuella ändringar kan du bokföra serviceordern.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="post-service-orders-and-credit-memos" />Bokföra tjänsteorder och kreditnotor
När du har skapat en serviceorder, fyllt i all nödvändig information och gjort eventuella ändringar kan du bokföra serviceordern. Ordern måste innehålla åtminstone en serviceartikelrad och en servicerad innan du kan bokföra den. Om ordern innehåller mer än en servicerad bokförs alla rader samtidigt.  

Om du har ett stort antal serviceorder kan spara du tid genom att använda ett batch-jobb för att bokföra dem samtidigt. Du kan köra batch-jobbet från en serviceorder.

> [!Tip]
> Innan du bokför ett servicedokument kan det vara praktiskt att använda åtgärden **Testrapport** om du vill kontrollera om några fel eller någon bristfällig information. Om det finns fel, måste du korrigera det. Du kan sedan skriva ut en ny testrapport för att verifiera åtgärdningen och bokföra dokumentet.

## <a name="to-post-a-service-order" />Så här bokför du serviceorder
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.  
2. Öppna relevant serviceorder.  
3. På sidan **serviceordern** väljer du något av följande.  

    |**Åtgärd**|**Resultat**|  
    |------------------|----------------|  
    |**Testrapport** | Alla delar av dokumentet kontrolleras och resultatet presenteras i en rapport. Om rapporten påvisar något fel eller saknad information måste du korrigera det. Därefter kan du skriva ut en ny testrapport.|  
    |**Bokför** | Ordern bokförs, men ingen leverans eller faktura skrivs ut.|  
    |**Bokför och skriv ut** | Ordern bokförs och en leverans (om ordern levereras utan att faktureras) eller en faktura (om ordern faktureras) skrivs ut.|  
    |**Bokför batch-jobb** | Bokför flera serviceorder samtidigt, en gång.|  

4. När du bokför ordern måste du ange ett av följande alternativ för hur du vill bokföra ordern.  

    |**Bokföringsalternativ**|**Resultat**|  
    |------------------------|----------------|  
    |**Leverera** | Varuleveransen bokförs.|  
    |**Fakturera** | Artiklar som redan levererats faktureras.|  
    |**Leverera och fakturera** | Artiklarna faktureras och levereras.|  
    |**Leverera och förbruka** | Leverans och förbrukning bokförs för ordern. Alla relevanta antal på serviceraden/-raderna på ordern och i det serviceleveransdokument som tidigare bokförts uppdateras.|  

Du kan bokföra förbrukningen endast om raden innehåller ett antal som inte har levererats men fakturerats eller förbrukats.  

När ordern bokförs skapas motsvarande transaktioner och bokförda dokument automatiskt. Dessutom uppdateras alla relevanta fält i serviceorderdokumentet.  

## <a name="to-batch-post-service-orders" />Så här batch-bokför du serviceorder
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Bokför batch**.  
3.  Du kan skapa ett filter för att välja ut vissa ordernummer eller intervaller av ordernummer för det batch-jobb som ska köras.  
4.  Välj **OK** när du vill starta batchjobbet.  

## <a name="to-post-a-service-credit-memo" />Så här bokför du servicekreditnotor
När du har skapat en servicekreditnota och fyllt i den, kan du bokföra kreditnotan. Om fel eller saknad information upptäcks i kreditnotan under bokföringen avbryts processen och ett felmeddelande visas.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekreditnotor** och väljer sedan relaterad länk.  
2. Skapa en ny servicekreditnota. Välj åtgärden **Ny**.  
3. Fyll i följande obligatoriska fält.  
4. Välj åtgärden **Bokföra**. Om du vill skriva ut kreditnotan samtidigt som du bokför den klickar du på åtgärden **Bokför och skriv ut** i stället.  
5. Välj **Testrapport** för att testa en kreditnota innan du bokför dem. När du kör rapporten, verifieras bokföringsdatum som har angetts i dokumentet.  
6. Bokför flera servicekreditnotor samtidigt. Kör batch-jobbet **batch-bokför servicekreditnotor**. Det kan vara en fördel om du har ett stort antal kreditnotor som ska bokföras.  

> [!NOTE]  
>  Det är viktigt att all nödvändig information har angetts i kreditnotorna innan du batch-bokför dem. Annars kan det hända att de inte bokförs. När batch-bokföringen är klar visas ett meddelande som anger hur många servicekreditnotor som har bokförts.  

## <a name="to-post-consumption-from-a-service-order" />Så här bokför du förbrukning från en serviceorder
Nedan beskrivs hur du bokför artiklar, resurstimmar och/eller kostnader som har använts för en specifik serviceoperation som du inte debiterar kunden för. Observera att du bara kan bokföra förbrukade artiklar, timmar och/eller kostnader för en bokförd leverans som inte innehåller några bokförda fakturor eller bokförd förbrukning.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.  
2. Öppna serviceorder som du vill bokföra förbrukning för.  
3. Välj serviceartikel. Välj åtgärden **Servicerader**.  
4. Leta upp transaktionerna och ange antal förbrukning som ska bokföras för kunden i fältet **Ant. att förbruka**. Antalet kan inte vara större än det antal som redan har levererats och återstående antal som fortfarande inte har fakturerats efter delfakturering av leveransen.  

    > [!NOTE]  
    >  Om du vill att förbrukning ska registreras kopplat till rätt projekt fyller du i fälten **Projektnr**, **Projektaktivitetsnr** och **Projektradtyp** på serviceraden.  

5. Välj raderna att bokföra och välj sedan åtgärden **bokför**. Välj **Förbrukning** i det fönster som visas.  

Nu bokförs servicen som delvis eller helt förbrukad, beroende på värdet i fältet **Ant. att förbruka**. Motsvarande transaktioner skapas också. Dessutom uppdateras alla tidigare bokförda serviceleveransdokument kronologiskt med de förbrukade antalen. Alla relevanta antal uppdateras på serviceraden/-raderna på ordern.  

## <a name="to-post-shipments-from-service-orders" />Så här bokför du utleveranser från serviceorder
När du har angett detaljerad information för en service kan du justera och bokföra antalen artiklar som använts, tidsåtgång och uppkomna kostnader. Detta innebär att nödvändiga ändringar utförs via [!INCLUDE[prod_short](includes/prod_short.md)] så att du kan se det nya läget i lagret och aktuell status av behandlingen av den specifika ordern.  

I följande procedur beskrivs hur du bokför leveransen av serviceradartiklar på lagerställen som inte kräver lagerhantering.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk. 2. På sidan för den markerade serviceordern klickar du på **Åtgärder**, **Order**, **Servicerader**.  
3. PÅ sidan **Servicerader** letar du upp transaktionerna och anger det antal som ska bokföras i fältet **Ant. att utleverera**.  

   > [!NOTE]  
   >  Innan du anger ett antal för utleverans måste du bestämma dig för om du vill bokföra leveransen helt eller delvis. Om du väljer att leverera helt måste värdet i fältet **Ant. att utleverera** vara lika med värdet i fältet **Antal**. Om du bokför en delleverans måste du ange den antal som du vill leverera först. Om du redan har levererat en del av servicen på ordern noterar du värdet i fältet **Utlevererat antal**. Du kan inte ange ett högre värde i fältet **Ant. att utleverera** än det antal enheter som ännu inte har levererats.  

4. Välj åtgärden **Bokföra**. Välj knappen **Leverera** på sidan som visas.

[!INCLUDE[prod_short](includes/prod_short.md)] skapar transaktioner (i garantireskontra, artikeltransaktioner, servicereskontra eller redovisning), skapar bokförda serviceleveransdokumentet och alla relevanta fält på serviceraderna i serviceordern uppdateras.  

Om lagerstället kräver distributionslagerhantering sker leverans och flytt av serviceradartiklar på samma sätt som övriga källdokument. Den enda skillnaden är att serviceradartiklar kan förbrukas antingen externt eller internt och därför kräver två olika släppfunktioner.  

Om du vill veta mer om fraktservicerader i avancerade lagerkonfigurationer går du till plocka artiklar för Distributionslagerutleverans](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

## <a name="to-undo-posted-consumption" />Så här ångrar du bokförd förbrukning
Du kan ångra förbrukning på en serviceorder. Till exempel om den bokförs av misstag.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokförda serviceleveranser** och väljer sedan relaterad länk.  
2. Öppna den bokförda serviceutleverans som den felaktiga förbrukningen har bokförts för.  
3. Välj åtgärden **Serviceutleveransrader**.  
4. Välj de rader som innehåller den felaktiga förbrukningen och välj sedan åtgärden **ångra förbrukning**.  

 En balanserande serviceleveransrad infogas, med negativa värden i antalsfälten för den/de markerade raden/raderna infogas automatiskt.  
  
> [!NOTE]  
>  Du kan inte ångra serviceförbrukning om:  

>    * Tjänsteordern har stängts.  
>    * Den har bokförts i modulen projekt, så att det finns projekttransaktioner som är kopplade till artikeln.  

## <a name="to-post-service-lines" />Så här bokför du servicerader
Om du behöver arbeta med en serviceorder under en längre period utan att bokföra den kanske du behöver bokföra några av de servicerader som är kopplade till ordern för att t. ex. hålla lagret uppdaterat. Du kan då bokföra genom att ange de relevanta antalen på den/de rad(-er) som ska bokföras. Du kan välja att bokföra raderna var för sig eller välja att bokföra flera rader åt gången.  

Nedan beskrivs hur du bokför leveransen direkt från en serviceorder i lagerställen utan lagerhantering. Om lagerstället är inställt på lagerhantering görs leveransbokföringen i ett annat distributionslagerdokument, beroende på inställningen av lagerställe.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.  
2. Öppna serviceordern och välj sedan åtgärden **Servicerader**.  
4. På de rader som du vill bokföra fyller du i fälten **Ant. att utleverera**, **Ant. att fakturera** och/eller **Ant. att förbruka**, beroende på hur du ska bokföra raden/raderna.  
5. Välj åtgärden **Bokföra**.

## <a name="see-also" />Se även
[Bokföra tjänstehantering](service-service-posting.md)  
[Skapa en tjänsteorder](service-how-to-create-service-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
