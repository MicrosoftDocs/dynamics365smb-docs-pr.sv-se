---
title: Stämma av betalningar genom att använda automatisk koppling
description: Beskriver hur du stämmer av betalningar genom automatisk koppling när du använder utbetalningar eller inbetalningar till relaterade öppna transaktioner.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '389, 1290, 1294, 1287'
ms.date: 06/22/2022
ms.author: bholtorf
---
# Stämma av betalningar genom att använda automatisk koppling

På sidan **Betalningsavstämningsjournal** anges betalningar, antingen inkommande eller utgående, som har registrerats som transaktioner på ditt bankkonto online eller på en betalningstjänst. Du kan koppla betalningar till relaterade öppna kund-, leverantörs- och bankkontotransaktioner. Fyll i journalen genom att importera ett kontoutdrag som ett bankflöde eller en bankfil, eller genom att manuellt ange transaktioner som du gör på din betalningstjänst.

> [!NOTE]
> Sidan erbjuder automatiska matchningsfunktioner som ska användas för betalningar till deras relaterade öppna transaktioner baserat på matchning av data på en kontoutdragsrad (journalrad) och data på en eller flera öppna transaktioner. Observera att du kan skriva över de föreslagna automatiska applikationerna och du kan välja att inte använda automatiska applikationer alls. Mer information finns i steg 7.

En betalningsavstämningsjournal är relaterad till ett bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)]. Bankkontot representerar det bankkonto online som betalningstransaktionerna registreras på. Eventuella öppna bankkontotransaktioner som relateras till kopplade kund- eller leverantörsreskontratransaktionerna kommer att avslutas när du väljer **Bokför betalningar och stäm av bankkonton**. Bankkontot stäms av automatiskt för betalningar som du bokför med journalen.

Om du använder sidan **Betalningsavstämningsjournal** för att registrera och koppla kundbetalningar kan du ställa in journalen på att använda en viss nummerserie. Efteråt kan du ange nummerserien i fältet **Nummerserie för betalningsavstämning** på ett bankkonto. Genom att använda en dedikerad nummerserie kan du göra det enklare att identifiera transaktioner som har bokförts genom journalen.

På samma sätt som andra journaler kan du, när du korrigerar bokförda transaktioner, återföra transaktioner som bokfördes genom betalningsavstämningsjournalen från sidan **Bokförd redovisningsjournal**. Du kanske till exempel vill återföra transaktioner för betalningar som du har kopplat till fel kund. Du måste först ta bort kopplingen till de bokförda kundreskontratransaktionerna. Sedan kan du använda åtgärden **Återför register** på sidan **Bokförd redovisningsjournal** för att återföra journalen som bokförde betalningen. Alternativt kan du gå till sidan **Bokförda redovisningsjournaler** och använda åtgärden **Kopiera valda rader till journal** för att återföra specifika rader från journalen med bokförda betalningsavstämningar. 

När du använder automatisk koppling identifierar [!INCLUDE[prod_short](includes/prod_short.md)] banktransaktioner som redan har bokförts, vilket förhindrar dubbel bokföring.

Du kan importera banktransaktioner som .csv-bankfiler eller i andra format som din bank tillhandahåller. Om du vill importera kontoutdrag som en bankfeed måste du först aktivera en särskild avsedd bankintegreringstjänst och sedan länka bankkontot till dess relaterade onlinebankkonto. Betalningsavstämningsjournalen hittar sedan automatiskt bankfeeder, när du väljer åtgärden **Importera banktransaktioner**. Dessutom kan du konfigurera ett bankkonto att automatiskt importera nya kontoutdragfeeder varje timme. Transaktioner för utbetalningar som redan har bokförts som kopplade och/eller avstämda kommer inte att importeras. Du kan använda tjänsten Envestnet Yodlee Bank Feeds för att hämta dessa transaktioner, som är förinstallerad i vissa landsversioner av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Ställ in tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md). Alternativt kan en Microsoft-partner hjälpa dig att uppfylla dina affärs- eller landskrav.

Med åtgärden **Mappa text till konto** kan du skapa mappningar mellan text på betalningar och specifika debet-, kredit- och balanskonton så att sådana betalningar bokförs på de angivna kontona när du bokför betalningsavstämningsjournalen. Mappning lämpar sig exempelvis för återkommande inbetalningar eller kostnader, till exempel frekventa inköp av bilbränsle eller bankavgifter och ränta, som regelbundet visas på bankutdraget och inte behöver ett relaterat affärsdokument. (Se steg 10). Mer information finns i [Mappa text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Det kan hända att journalrader saknar förslag på koppling, vilket kan inträffa av olika skäl. Till exempel eftersom ett dokument saknas eller att en kund har betalat för mycket och det finns ett överskjutande belopp efter det att betalningen har tillämpats på en annan journalrad. I sådana fall kan du använda åtgärden **Överför differens till konto** för att skapa och bokföra den saknade redovisningstransaktionen, till exempel för en återbetalning, som behövs för att koppla betalningen till. (Se steg 11) Mer information finns i [Så här stämmer du av betalningar som inte kan kopplas.](receivables-how-reconcile-payments-cannot-apply-auto.md).

Du använder funktionen **Koppla automatiskt**, antingen automatiskt när du importerar en bankfil eller feed med betalningstransaktioner eller när du aktiverar den, för att koppla betalningar till deras motsvarande öppna transaktioner baserat på en matchning av text på en bankutdragsrad (journalrad) med text i en eller flera öppna transaktioner. Denna automatisering baseras på regler som du definierar på sidan **Regler för betalningskoppling**, där du också definierar om ett kopplingsförslag kräver granskning. Mer information finns i [Konfigurera regler för automatiska betalningskopplingar](receivables-how-set-up-payment-application-rules.md).

På journalrader där en betalning har kopplats automatiskt till en eller flera öppna transaktioner har fältet **Matchningssäkerhet** ett värde mellan **Låg**, **Medel** eller **Hög** som anger kvaliteten för den datamatchning som den föreslagna betalningskopplingen baseras på.

Vissa betalningsansökningar kräver att du granskar dem enligt definitionen i den använda matchningsregeln, till exempel rader med **låg** matchningssäkerhet. Andra rader kräver granskning och manuella ändringar från din sida eftersom det finns ett värde i fältet **Differens**. Om du vill granska en eller flera betalningskopplingar väljer du fältet **Rader att granska** eller **Rader med differens** längst ned. Sidan **Granskning av betalningskoppling** öppnas och visar all relevant information om kunden eller leverantören som betalningen tillämpas på, matchande information och åtgärder för att bearbeta raden, till exempel åtgärden **Acceptera koppling**. (Se steg 7 och 8)

För varje journalrad som representerar en betalning på sidan **Betalningsavstämningsjournal** kan du öppna sidan **Betalningskoppling** för att visa alla öppna kandidattransaktioner för betalningen och för att visa detaljerad information för varje transaktion om datamatchningen som en betalningskoppling baseras på. Här kan du koppla manuellt betalningar eller koppla om betalningar som kopplades automatiskt till fel transaktion. (Se steg 10) Mer information finns i [Granska och koppla betalningar efter automatisk koppling](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Du kan starta banktransaktionsimporten samtidigt som du öppnar sidan **Betalningsavstämningsjournal** för en befintlig journal. Följande procedurer beskriver hur du importerar banktransaktioner till sidan **Betalningsavstämningsjournal** när du har skapat en ny journal.

## Så här stämmer du av betalningar genom att använda automatisk koppling
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **betalningsavstämningsjournal** och väljer sedan relaterad länk.
2. Om du vill arbeta i en ny betalningsavstämningsjournal väljer du åtgärden **Ny journal**.
3. På sidan **Betalningsbankkontolista** väljer du det bankkonto som du vill stämma av betalningar för och väljer sedan knappen **OK**.
   Sidan **Betalningsavstämningsjournal** öppnas förberett för det valda bankkontot.
4. Välj åtgärden **Importera banktransaktioner**.
   Om bankkontot för den valda journalen inte har lagts upp för import av banktransaktioner hjälper [!INCLUDE[d365fin](includes/d365fin_md.md)] dig att göra det.
5. På sidan **Välj en fil att importera** väljer du den fil som innehåller banktransaktionerna för betalningarna du vill avstämma, och väljer sedan knappen **Öppna**.  
6. Om tjänsten Envestnet Yodlee Bank Feeds är aktiverad anger du det datumintervall när kontoutdragen ska importeras på sidan **Kontoutdragsfilter**.

    Sidan **Betalningsavstämningsjournal** fylls i med rader för betalningar som representerar banktransaktioner i det importerade bankkontoutdraget.

     På rader för betalningar som har kopplats automatiskt till relaterade öppna transaktioner indikerar fältet **Matchningssäkerhet** kvaliteten för de data som matchar de som den föreslagna betalningskopplingen baseras på. Dessutom visar fälten **Kontonamn**, **Kontotyp** och **Kontonr.** information om den kund eller leverantör som betalningen gäller.

    Automatiska kopplingar, matchande egenskaper samt huruvida rader som kräver granskning kontrolleras av regler. Du kan redigera reglerna för att justera resultaten. Mer information finns i [Konfigurera regler för automatiska betalningskopplingar](receivables-how-set-up-payment-application-rules.md).

7. Om du vill granska, acceptera/ta bort eller manuellt ändra flera betalningsansökningar som har ett värde i fältet **Differens** väljer du åtgärden **Rader med differens** längst ned.

    Sidan **Granskning av betalningskoppling** öppnas och visar den första kopplingen att granska. Nästa koppling att granska visas på sidan när du bearbetar den föregående. Granskningen inkluderar information om den kund eller leverantör som betalningen gäller, matchande information samt de åtgärder som ska bearbeta raden, exempelvis åtgärderna **Godkänn koppling** och **Koppla manuellt**.

8. Om du vill granska, acceptera eller ta bort eller manuellt ändra flera betalningskopplingar som regeln har ställts in på att granska, väljer du åtgärden **Rader som ska granskas**. 

9. Om du vill ändra en autmatisk koppling väljer du en journalrad och sedan åtgärden **Koppla manuellt** för att koppla om eller koppla betalningen manuellt på sidan **Betalningskoppling**. Mer information finns i [Granska och koppla betalningar efter automatisk koppling](receivables-how-review-apply-payments-auto-application.md).

10. Välj en inte kopplad journalrad för en återkommande inbetalning eller kostnad, till exempel ett bilbensinköp, och välj sedan åtgärden **Mappa text till konto** action. Mer information finns i [Mappa text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

    Välj åtgärden **Koppla manuellt** när du har slutfört mappningen av betalningstext till konton.

    När en mappning text-till-konto skapas kommer det resulterande automatiska betalningsprogrammet att innehålla **Mappning text-till-konto** i fältet **Matchningssäkerhet**.

11. Om du har en journalrad utan någon föreslagen koppling, detta eftersom det inte finns någon redovisningstransaktion som den kan kopplas till, väljer du åtgärden **Överför differens till konto** för att skapa och bokföra den saknade redovisningstransaktionen som behövs för att koppla betalningen till. Mer information finns i [Stämma av betalningar som inte kan kopplas](receivables-how-reconcile-payments-cannot-apply-auto.md).

12. När inga fler rader kräver granskning och fältet **Differens** är tomt på alla rader väljer du åtgärden **Bokför** och sedan något av följande alternativ:

    - **Bokföra betalningar och stämma av bankkonton** – om du vill bokföra betalningar som tillämpas och stänga de relaterade bankkontotransaktionerna som avstämts.
    - **Bokför endast betalningar** – om du bara vill bokföra betalningar som används, men låta de relaterade bankkontotransaktionerna vara öppna. Det krävs att du stämmer av bankkontot separat, till exempel: Mer information finns i [Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md).
    - **Testrapport** – om du vill granska resultatet av bokföringen innan du bokför. Rapporten **bankkontoutdrag** öppnas och visar samma fält som längst ned på sidan **avstämning av betalningsjournal**.

När du bokför en betalningsavstämningsjournal stängs de kopplade öppna transaktionerna. Kund-, leverantörs- eller redovisningskontona uppdateras. För betalningar på journalrader som baseras på text-till-konto-mappning uppdateras de angivna kund-, leverantörs- och redovisningskontona. För alla journalrader skapas bankkontotransaktioner. Eventuella öppna bankkontotransaktioner som relateras till kopplade kund- eller leverantörsreskontratransaktionerna kommer att avslutas när du väljer åtgärden **Bokför betalningar och stäm av bankkonton**. Detta betyder att bankkontot stäms av automatiskt för betalningar som du bokför med journalen.

Du kan jämföra värdet i fältet **Saldo på bankkonto efter bokföring** tillsammans med värdet i fältet **Kontoutdragets slutsaldo** för att spåra när bankkontot har stämts av baserat på betalningar som du bokför.

> [!NOTE]  
>   Om du inte vill stämma av bankkontot från **Betalningsavstämningsjournal** måste du använda sidan **Bankkontoavstämning**. Mer information finns i [Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md).

## Se även

[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
