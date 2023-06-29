---
title: 'Arbeta med avropsorder, försäljning eller inköpsorder'
description: Du kan använda avropsorder om en kund har avtalat att köpa stora antal som ska levereras i flera mindre leveranser under en bestämd tidsperiod. Detsamma gäller för inköp.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '507, 509, 6620, 6622, 6623, 9303, 9310'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="work-with-blanket-sales-orders-or-blanket-purchase-orders"></a><a name="work-with-blanket-sales-orders-or-blanket-purchase-orders"></a>Arbeta med avropsorder, försäljning eller inköpsavropsorder

En avropsorder utgör ramen för en långsiktig överenskommelse mellan företaget och en kund. På samma sätt använder du inköpsavropsorder för att hantera långsiktiga avtal mellan dig och leverantören.

En avropsorder skapas vanligtvis om en kund har lovat att köpa stora antal som ska levereras i flera mindre leveranser under en bestämd tidsperiod. Avropsorder gäller vanligtvis bara en artikel med förbestämda leveransdatum. Huvudanledningen till att en avropsorder används i stället för en försäljningsorder är att de antal som anges på en avropsorder inte påverkar artikeldispositionen och därmed kan användas som ett förslag för övervakning, prognostisering och planering.

På avropsordern kan varje separat leverans anges som en orderrad som sedan kan omvandlas till en försäljningsorder vid leveransen.

Ett exempel på en situation där en avropsorder kan användas är om en kund beställer 1 000 enheter av en artikel och vill att 250 artiklar åt gången ska levereras en gång i veckan under den kommande månaden.

> [!NOTE]
> Inköpsavropsorder fungerar på samma sätt som en försäljningsavropsorder. Den här dokumentationen visar endast försäljningsavropsorder.

## <a name="to-create-a-blanket-sales-order"></a><a name="to-create-a-blanket-sales-order"></a>Så här skapar du en avropsorder

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsavropsorder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Låt fältet **Orderdatum** vara tomt. När separata försäljningsorder skapas från avropsordern anges orderdatum för försäljningsordern som det aktuella arbetsdatumet.
5. På snabbfliken **Rader** skapar du separata rader för varje utleverans. Om kunden t. ex. beställer 1 000 enheter jämnt fördelade över fyra veckor skapar du fyra separata rader med 250 enheter på varje rad.  

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a><a name="to-create-a-sales-order-from-a-blanket-sales-order"></a>Så här skapar du en försäljningsorder från en avropsorder

1. Om du vill skapa en order för någon av raderna i försäljningsavropsorder tar du bort antalet i fältet **Levereras antal** för alla de rader som du INTE vill leverera just nu.  
2. När du vill börja skapa order väljer du åtgärden **Skapa order** och väljer sedan **Ja**. Du får ett meddelande om att avropsordern har tilldelats ett ordernummer. Observera att avropsordern inte har tagits bort.  
3. Välj knappen **OK**.  
4. På snabbfliken **Rad** väljer du åtgärden **Ej bokförda rader** och sedan väljer du åtgärden **Order**.  
5. På sidan **Försäljningsrader** väljer du önskad försäljningsorde, väljer åtgärden **Rad** och väljer sedan åtgärden **Visa dokument** action.  

Följande gäller försäljningsorder, när de har skapats från försäljningsavropsorder:  

- När avropsordern har omvandlats till en försäljningsorder innehåller försäljningsordern alla raderna från avropsordern. De rader där antalet i fältet **Levereras antal** togs bort visas, men fältet **Antal** är tomt för dessa rader. Du kan låta de här raderna vara kvar eller redigera eller ta bort dem.  
- Det är viktigt att komma ihåg att antalet på en försäljningsorderrad inte får vara större än antalet på den associerade avropsorderraden. Om detta sker går det inte att bokföra försäljningsordern.  
- När försäljningsordern bokförts som levererad och/eller fakturerad uppdateras fälten **Utlevererat antal** och **Fakturerat antal** på den relaterade avropsordern.  
- Avropsordernumret och radnumret registreras som försäljningsradernas egenskaper när de skapas från en avropsorder.  
- Om en försäljningsorder inte skapas direkt från en avropsorder men ändå är relaterad till den kan du skapa en koppling mellan försäljningsordern och avropsordern genom att skriva in numret på den associerade avropsordern i fältet **Avropsordernr** på försäljningsorderraden.  
- När du har skapat en eller flera försäljningsorder för hela antalet på avropsorderraden, kan inga andra försäljningsorder skapas för samma rad. Användare förhindras från att ange ett antal i fältet **antal. att utleverera**. Om du senare behöver lägga till ytterligare antal på en avropsorder kan du öka värdet i fältet **Antal** och sedan skapa ytterligare order.  
- Den fakturerade försäljningsavropsordern finns kvar i systemet tills den tas bort, antingen genom att enskilda avropsorder tas bort eller att batch-jobbet **Ta bort faktrd förs.avropsord.** körs.  
- Om en kund dessutom har registrerats som en kontakt i modulen Marknadsföring, och om en interaktionsmallkod har angetts för avropsorder på sidan **Marknadsföringsinställning** registreras en interaktion i tabellen Interaktionslogg när du väljer **Skriv ut** för att skriva ut avropsordern.

## <a name="to-view-the-status-of-a-blanket-sales-order"></a><a name="to-view-the-status-of-a-blanket-sales-order"></a>Så här visar du status för en avropsorder

Du kan visa statusen för en försäljningsavropsordern på sidan **Statistik för försäljningsavropsorder**. Detta kan vara praktiskt när du börjar fakturera ordern som skapats utifrån försäljningsavropsorder.  

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsavropsorder** och väljer sedan relaterad länk.  
2.  Markera en försäljningsavropsorder och välj åtgärden **statistik**.  
3.  På sidan **Statistik för försäljningsavropsorder** på snabbfliken **Inköpsorderstatistik** visas översiktsinformation om hela ordern baserat på den totala kvantiteten i de olika **antalsfälten** på avropsorderraderna.  

- På snabbfliken **Fakturering** visas översiktsinformation som baseras på den totala kvantiteten i fälten för **Ant. att fakturera** på försäljningsavropsorderraderna.  
- På snabbfliken **Leverans** visas översiktsinformation som baseras på den totala kvantiteten i fälten för **Ant. att inlevereras** på försäljningsavropsorderraderna.  
- På snabbfliken **Förskottsbetalning** visas översiktsinformation om eventuella förskottsbetalda belopp.  
- På snabbfliken **Leverantör** visas viss grundläggande information om leverantören.

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a><a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a>Så här väljer du att visa ej bokförda och bokförda försäljningsavropsorderrader

Kopplingen mellan avropsordern, försäljning och den ursprungliga försäljningsordern och eventuella övriga försäljningsdokument, bibehålls när du har bokfört som en lista över bokförda och ej bokförda fakturarader för försäljningsorder.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsavropsorder** och väljer sedan relaterad länk.
2. Öppna den avropsorder för försäljning som du vill visa.
3. Om du vill visa transaktioner som inte har bokförts väljer du åtgärden **Rad** ocgh sedan **Ej bokförda rader**. Välj något av följande alternativ:  

|Alternativ|Description|
|--|--|
|**Order**|Anger öppna order som är associerade till den markerade raden.|
|**Fakturor**|Anger öppna fakturor som är associerade till den markerade raden. Öppna fakturor kan associeras manuellt till en avropsorder genom att avropsordernumret anges på försäljningsfakturaraden.|
|**Returorder**|Anger öppna returorder som är associerade till den markerade raden.|
|**Kreditnota**|Anger öppna kreditnotor som är associerade till den markerade raden.|

4. Om du vill visa transaktioner som inte har bokförts väljer du åtgärden **Rad** och sedan åtgärden **Bokförda rader**. Välj något av följande alternativ:  

|Alternativ|Description|
|---|----|
|**Utleveranser**|Bokförda leveranser som är associerade till den markerade raden.|
|**Fakturor**|Bokförda fakturor som är associerade till den markerade raden.|
|**Returinleveranser**:|Bokförda returinleveranser som är associerade till den markerade raden.|
|**Kreditnota**|Bokförda kreditnotor som är associerade till den markerade raden.|

5. På sidan **Försäljningsrader** väljer du åtgärden **Visa dokument** för att visa transaktionen.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Skapa monteringsorder för avrop](assembly-how-to-create-blanket-assembly-orders.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
