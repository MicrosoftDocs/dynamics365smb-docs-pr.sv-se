---
title: Försäkra anläggningstillgångar
description: Du tilldelar en eller flera anläggningstillgångar till en försäkringspolicy genom att bokföra försäkringstransaktionerna från sidan **Försäkringsjournal**.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'policy, coverage'
ms.search.form: '5647, 5644, 5653, 5651, 5655, 5652, 5645, 5656, 5646, 5648, 9275'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Försäkra anläggningstillgångar

 **Använd sidan Försäkringskort** när du vill skapa ett försäkringsbrev som täcker en eller flera anläggningstillgångar. Du kan koppla en anläggningstillgång till ett försäkringsbrev eller flera anläggningstillgångar till ett försäkringsbrev.

Du tilldelar en anläggningstillgång till en försäkringspolicy genom att bokföra försäkringstransaktionerna från sidan **Försäkringsjournal**.

Dessutom kan du tilldela en anläggningstillgång till en försäkringspolicy och skapa försäkringstransaktioner när du bokför dess anskaffningskostnad. Du bokför en anskaffningskostnad från anläggningstillgångsjournalen med **Försäkringsnr.** ifyllt. Du måste aktivera växlingsknappen **Automatisk försäkringsbokf** . på **sidan Anl.inställningar** . Mer information finns i [Skaffa en anläggningstillgång med hjälp av en redovisningsjournal](fa-how-acquire.md#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal) för anläggningstillgångar.

Om växlingsknappen Automatisk försäkringsbokf **. på** sidan Anl.inställningar **inte är aktiverad skapas rader på sidan Försäkringsjournal** när du bokför anskaffningar från anläggningstillgångsjournalen **.**  Du måste bokföra raderna manuellt.

> [!WARNING]  
> Om du inte aktiverar växlingsknappen **Automatisk försäkringsbokf** . på sidan **Anl.inställningar** bör försäkringsjournalen baseras på en journalmall utan nummerserie. Det är därför att de infogade verifikationsnumren från anläggningstillgångjournalraden annars kommer i konflikt med försäkringsjournalens nummerserie. För mer information om journalmallar och journaler, se [Så här ställer du in allmän information om anläggningstillgångar](fa-how-setup-general.md).

När du har kopplat en anläggningstillgång till ett försäkringsbrev **innehåller** fältet Försäkrad **på anläggningstillgångskortet Ja**. När du säljer anläggningstillgången stängs växlingsknappen av automatiskt.

## Så här skapar eller ändrar du ett försäkringskort

När du får information om ändringar av försäkringsbeloppet måste du ange den nya informationen på sidan **försäkringskort** så att försäkringsbrevet analyseras korrekt.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Försäkring** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny** för att skapa ett nytt kort för en försäkringspolicy. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Alternativt markerar du försäkringspolicym som du vill ändra och väljer sedan åtgärden **Redigera**.

## För att koppla en anläggningstillgång till ett försäkringsbrev genom att bokföra från försäkringsjournalen

Du tilldelar en anläggningstillgång till ett försäkringsbrev genom att bokföra från försäkringstransaktionerna.  

Efterföljande procedur beskriver hur du skapar en försäkringsjournalrad manuellt. Om växlingsknappen **Automatisk** försäkringsbokföring **är aktiverad på sidan Anl.inställningar** skapas försäkringsjournalrader automatiskt när du bokför anskaffningskostnader. I så fall är allt du måste göra att bokföra journalen.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Försäkringsjournaler** och väljer sedan relaterad länk.  
2. Öppna den relevanta journalen och fyll i journalraderna som behövs.  
3. För att skapa flera anläggningstillgångar till ett försäkringsbrev skapar du journalrader med samma värdet i fältet**Försäkringsnr.** och olika värden i fältet **Anl.nr**.  
4. Välj åtgärden **Bokföra**.  

    > [!NOTE]  
    > Transaktionerna från en försäkringsjournal bokförs endast i försäkringstransaktionerna.  

## Om du vill uppdatera försäkringvärdet för en anläggningstillgång

Du kan använda batch-jobbet **Indexera försäkring** när du vill uppdatera värdet för den anläggningstillgång som är försäkrad.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Indexera försäkring** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs.

    > [!NOTE]  
    >   I fältet **Indextal** anger du en minskning av 5 %, till exempel som 95, medan du anger en ökning med 2 % som 102.  
3. Välj **OK**.  

   Batch-jobbet beräknar det nya beloppet som en procentsats av det totala försäkringsvärdet på sidan **Försäkringsstatistik** och en rad i försäkringsjournalen skapas.  
4. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Försäkringsjournaler** och väljer sedan relaterad länk.  
5. Öppna relevant försäkringsjournal, granska de skapade värdena och bokför dem i försäkringstransaktionerna.  

## Att bevaka försäkringsskydd

[!INCLUDE[prod_short](includes/prod_short.md)] ger dedikerade rapporter och statistiksidor för användning vid analys av försäkringsbrev och om anläggningstillgångarna är över- eller underförsäkrade.  

### Översikt över försäkringar

Få en översikt över försäkringsbreven genom att skriva ut rapporten **Försäkringslista** rapport. Rapporten visar alla försäkringsbrev och de viktigaste fälten på försäkringskortet visas.  

### Försäkringsskydd

Om du vill se vilka försäkringsbrev som täcker varje tillgång och till vilket belopp kan du förhandsgranska eller skriva ut rapporten **Försäkring med totalvärde**.  

#### Över-/undertäckning

Du kan kontrollera om anläggningstillgångar är över- eller underförsäkrade på följande sätt:  

* Sidan **Försäkringsstatistik** visas. Ett positivt belopp i fältet **Över-/underförsäkrad** innebär att anläggningstillgången är överförsäkrad. Ett negativt belopp innebär att tillgången är underförsäkrad.  
* Sidan **Anl.statistik** visas. Välj fältet **Totalt försäkrat värde** för att visa sidan **Försäkringstransaktioner**.  
* Rapporten **Över/underförsäkringsskydd**.  
* Rapporten **Försäkringsanalys**.  

### Oförsäkrade anläggningstillgångar

Om du vill kontrollera om du har glömt att koppla en anläggningstillgång till ett försäkringsbrev kan du skriva ut eller förhandsgranska **rapporten Försäkring - oförsäkrade** anl. Den här rapporten visar anläggningstillgångar för vilka belopp inte har bokförts i försäkringstransaktionerna.  

## Så här visar du försäkringstransaktioner

Du kan visa de transaktioner som du har gjort i försäkringstransaktionerna.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Försäkring** och väljer sedan relaterad länk.  
2. Välj aktuellt försäkringsbrev och klicka på åtgärden **Försäkringstransaktioner.**.  

## Så här visar du det försäkrade totalvärdet för en anläggningstillgång:

En matrissida visar de försäkringsvärden som registreras för varje försäkringsbrev för varje anläggningstillgång som härrör från bokförda försäkringsrelaterade belopp.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Försäkring** och väljer sedan relaterad länk.  
2. Välj aktuellt försäkringsbrev och klicka på åtgärden **Försäkrat totalvärde per anl.**.  
3. Fyll i fälten om det behövs.  
4. Välj åtgärden **Visa matris**.  
5. Välj ett värde i matrisen för att visa de underliggande försäkringstransaktionerna.  

## Så här rättar du försäkringstransaktioner

Om en anläggningstillgång har tilldelats fel försäkringsbrev kan du korrigera den genom att skapa två grupperingstransaktioner från försäkringsjournalen.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Försäkringsjournaler** och väljer sedan relaterad länk.  
2. Skapa en journalrad för anläggningstillgången och det korrekta försäkringsbrevet där värdet i fältet **Belopp** är positivt.  
3. Skapa en annan journalrad för anläggningstillgången och det felaktiga försäkringsbrevet där värdet i fältet **Belopp** är negativt.  
4. Välj åtgärden **Bokföra**.  

Anläggningstillgången tas bort från det felaktiga försäkringsbrevet på den andra raden. Tillgången kopplas till rätt försäkringsbrev på den första raden i journalen.  

## Se även

[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]