---
title: Stämma av betalningar genom att använda automatisk koppling
description: Beskriver hur du använder funktionen automatisk koppling när du använder utbetalningar eller inbetalningar till deras relaterade öppna transaktioner och stämma av betalningar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.search.form: 389, 1290, 1294, 1287
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8c4d11dd4e031388ea5ec28bb8a181122b50b470
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9074594"
---
# <a name="reconcile-payments-using-automatic-application"></a>Stämma av betalningar genom att använda automatisk koppling

Sidan **Betalningsavstämningsjournal** anger betalningar, antingen inkommande eller utgående, som har registrerats som transaktioner på ditt onlinebankkonto eller en betaltjänst, och som du kan koppla till deras motsvarande öppna kund-, leverantörs- och bankkontotransaktioner. Raderna i journalen kan fyllas i genom att importera ett kontoutdrag som ett bankflöde eller en bankfil, eller genom att manuellt ange transaktioner som du gör på din betaltjänst.

> [!NOTE]
> Sidan erbjuder automatiska matchningsfunktioner som ska användas för betalningar till deras relaterade öppna transaktioner baserat på matchning av data på en kontoutdragsrad (journalrad) och data på en eller flera öppna transaktioner. Observera att du kan skriva över de föreslagna automatiska applikationerna och du kan välja att inte använda automatiska applikationer alls. Mer information finns i steg 7.

En betalningsavstämningsjournal är relaterad till ett bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] som återspeglar det onlinebankkonto där betalningstransaktionerna registreras. Eventuella öppna bankkontotransaktioner som relateras till kopplade kund- eller leverantörsreskontratransaktionerna kommer att avslutas när du väljer **Bokför betalningar och stäm av bankkonton**. Detta betyder att bankkontot stäms av automatiskt för betalningar som du bokför med journalen.

Du kan importera banktransaktioner som .csv-bankfiler eller i andra format som din bank tillhandahåller. Om du vill aktivera import av kontoutdrag som en bankfeed måste du först aktivera en särskild avsedd bankintegreringstjänst och sedan länka bankkontot till dess relaterade onlinebankkonto. Betalningsavstämningsjournalen hittar sedan automatiskt bankfeeder, när du väljer åtgärden **Importera banktransaktioner**. Dessutom kan du konfigurera ett bankkonto att automatiskt importera nya kontoutdragfeeder varje timme. Transaktioner för utbetalningar som redan har bokförts som kopplade och/eller avstämda kommer inte att importeras. Du kan använda tjänsten Envestnet Yodlee Bank Feeds för detta, som är förinstallerad i vissa landsversioner av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Ställ in tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md). Du kan också kontakta din Microsoft-partner för att få hjälp med att uppfylla dina affärs- eller landskrav.

Med åtgärden **Mappa text till konto** kan du skapa mappningar mellan text på betalningar och specifika debet-, kredit- och balanskonton så att sådana betalningar bokförs på de angivna kontona när du bokför betalningsavstämningsjournalen. Detta lämpar sig exempelvis för återkommande inbetalningar eller kostnader, till exempel frekventa inköp av bilbränsle eller bankavgifter och ränta, som regelbundet visas på bankutdraget och inte behöver ett relaterat affärsdokument. (se steg 10 nedan). Mer information finns i [Mappa text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Journalrader kanske inte har någon föreslagen koppling. Detta kan bero på olika skäl, till exempel ett dokument som saknas eller på att en kund har betalat för mycket så att det finns ett överskjutande belopp efter det att betalningen har tillämpats på en annan journalrad. I sådana fall kan du använda åtgärden **Överför differens till konto** för att skapa och bokföra den saknade redovisningstransaktionen, till exempel för en återbetalning, som behövs för att koppla betalningen till. (se steg 11 nedan) Mer information finns i [Så här stämmer du av betalningar som inte kan kopplas.](receivables-how-reconcile-payments-cannot-apply-auto.md).

Du använder funktionen **Koppla automatiskt**, antingen automatiskt när du importerar en bankfil eller feed med betalningstransaktioner eller när du aktiverar den, för att koppla betalningar till deras motsvarande öppna transaktioner baserat på en matchning av text på en bankutdragsrad (journalrad) med text i en eller flera öppna transaktioner. Denna automatisering baseras på regler som du definierar på sidan **Regler för betalningskoppling**, där du också definierar om ett kopplingsförslag kräver granskning. Mer information finns i [Konfigurera regler för automatiska betalningskopplingar](receivables-how-set-up-payment-application-rules.md).

På journalrader där en betalning har kopplats automatiskt till en eller flera öppna transaktioner har fältet **Matchningssäkerhet** ett värde mellan **Låg**, **Medel** eller **Hög** som anger kvaliteten för den datamatchning som den föreslagna betalningskopplingen baseras på.

Vissa betalningsansökningar kräver att du granskar dem enligt definitionen i den använda matchningsregeln, till exempel rader med **låg** matchningssäkerhet. Andra rader kräver granskning och manuella ändringar från din sida eftersom det finns ett värde i fältet **Differens**. Om du vill granska en eller flera betalningskopplingar väljer du fältet **Rader att granska** eller **Rader med differens** längst ned. Sidan **Granskning av betalningskoppling** öppnas och visar all relevant information om kunden eller leverantören som betalningen tillämpas på, matchande information och åtgärder för att bearbeta raden, till exempel åtgärden **Acceptera koppling**. (Se steg 7 och 8 nedan.)

För varje journalrad som representerar en betalning på sidan **Betalningsavstämningsjournal** kan du öppna sidan **Betalningskoppling** för att visa alla öppna kandidattransaktioner för betalningen och för att visa detaljerad information för varje transaktion om datamatchningen som en betalningskoppling baseras på. Här kan du koppla manuellt betalningar eller koppla om betalningar som kopplades automatiskt till fel transaktion. (se steg 10 nedan). Mer information finns i [Granska och koppla betalningar efter automatisk koppling](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Du kan starta banktransaktionsimporten samtidigt som du öppnar sidan **Betalningsavstämningsjournal** för en befintlig journal. Följande procedurer beskriver hur du importerar banktransaktioner till sidan **Betalningsavstämningsjournal** när du har skapat en ny journal.

## <a name="to-reconcile-payments-using-automatic-application"></a>Så här stämmer du av betalningar genom att använda automatisk koppling

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **betalningsavstämningsjournal** och väljer sedan relaterad länk.
2. Om du vill arbeta i en ny betalningsavstämningsjournal väljer du åtgärden **Ny journal**.
3. På sidan **Betalningsbankkontolista** väljer du det bankkonto som du vill stämma av betalningar för och väljer sedan knappen **OK**.
   Sidan **Betalningsavstämningsjournal** öppnas förberett för det valda bankkontot.
4. Välj åtgärden **Importera banktransaktioner**.
   Om bankkontot för den valda journalen inte är inställd för import av banktransaktioner visas en dialogruta för att fylla i de relevanta fälten.
5. På sidan **Välj en fil att importera** väljer du den fil som innehåller banktransaktionerna för betalningarna du vill avstämma, och väljer sedan knappen **Öppna**.  
6. Om tjänsten Envestnet Yodlee Bank Feeds är aktiverad anger du det datumintervall när kontoutdragen ska importeras på sidan **Kontoutdragsfilter**.

    Sidan **Betalningsavstämningsjournal** fylls i med rader för betalningar som representerar banktransaktioner i det importerade bankkontoutdraget.

     På rader för betalningar som har kopplats automatiskt till sina relaterade öppna transaktioner har fältet **Matchningssäkerhet** har ett värde mellan **Låg** och **Hög** som anger kvaliteten för de data som matchar de som den föreslagna betalningskopplingen baseras på. Dessutom fylls fälten **Kontonamn**, **Kontotyp** och **Kontonr.** i med information om den kund eller leverantör som betalningen gäller.

    Automatiska kopplingar, matchande egenskaper samt huruvida rader kräver granskning definieras av regler som du kan redigera för att justera resultaten. Mer information finns i [Konfigurera regler för automatiska betalningskopplingar](receivables-how-set-up-payment-application-rules.md).

7. Om du vill granska, acceptera/ta bort eller manuellt ändra flera betalningsansökningar som har ett värde i fältet **Differens** väljer du åtgärden **Rader med differens** längst ned.

    Sidan **Granskning av bvetalningskoppling** öppnas och visar den första kopplingen att granska. Nästa koppling att granska visas på sidan när du bearbetar den föregående. All relevant information om den kund eller leverantör som betalningen gäller, matchande information samt de åtgärder som ska bearbeta raden, exempelvis åtgärderna **Godkänn koppling** och **Koppla manuellt**.

8. Om du vill granska, acceptera/ta bort eller manuellt ändra flera betalningskopplingar som ska granskas, väljer du åtgärden **Rader att granska** längst ned i enlighet med betalningskopplingsregeln. Samma upplevelse som beskrivs för steg 8 presenteras

9. Om du vill ändra en autmatisk koppling väljer du en journalrad och sedan åtgärden **Koppla manuellt** för att koppla om eller koppla betalningen manuellt på sidan **Betalningskoppling**. Mer information finns i [Granska och koppla betalningar efter automatisk koppling](receivables-how-review-apply-payments-auto-application.md).

10. Välj en inte kopplad journalrad för en återkommande inbetalning eller kostnad, till exempel ett bilbensinköp, och välj sedan åtgärden **Mappa text till konto** action. Mer information finns i [Mappa text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

    Välj åtgärden **Koppla manuellt** när du har slutfört en mappningen av betalningstext till konton.

    När en mappning text-till-konto skapas kommer det resulterande automatiska betalningsprogrammet att innehålla **Mappning text-till-konto** i fältet **Matchningssäkerhet**.

11. Om du har en journalrad utan någon föreslagen koppling, detta eftersom det inte finns någon redovisningstransaktion som den kan kopplas till, väljer du åtgärden **Överför differens till konto** för att skapa och bokföra den saknade redovisningstransaktionen som behövs för att koppla betalningen till. Mer information finns i [Stämma av betalningar som inte kan kopplas](receivables-how-reconcile-payments-cannot-apply-auto.md).

10. När inga fler rader kräver granskning och fältet **Differens** är tomt på alla rader väljer du åtgärden **Bokför** och sedan något av följande alternativ:

    - **Bokföra betalningar och stämma av bankkonton** – om du vill bokföra betalningar som tillämpas och stänga de relaterade bankkontotransaktionerna som avstämts.
    - **Bokför endast betalningar** – om du bara vill bokföra betalningar som används, men låta de relaterade bankkontotransaktionerna vara öppna. Det krävs att du stämmer av bankkontot separat, till exempel: Mer information finns i [Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md).
    - **Testrapport** – om du vill granska resultatet av bokföringen innan du bokför. Rapporten **bankkontoutdrag** öppnas och visar samma fält som längst ned på sidan **avstämning av betalningsjournal**.

När du bokför betalningsavstämningsjournalen stängs de kopplade transaktionsnotorna och de relaterade kund-, leverantörs- eller redovisningskontona uppdateras. För betalningar på journalrader som baseras på text-till-konto-mappning uppdateras de angivna kund-, leverantörs- och redovisningskontona. För alla journalrader skapas bankkontotransaktioner. Eventuella öppna bankkontotransaktioner som relateras till kopplade kund- eller leverantörsreskontratransaktionerna kommer att avslutas när du väljer åtgärden **Bokför betalningar och stäm av bankkonton**. Detta betyder att bankkontot stäms av automatiskt för betalningar som du bokför med journalen.

Du kan jämföra värdet i fältet **Saldo på bankkonto efter bokföring** tillsammans med värdet i fältet **Kontoutdragets slutsaldo** för att spåra när bankkontot har stämts av baserat på betalningar som du bokför.

> [!NOTE]  
>   Om du inte vill stämma av bankkontot från **Betalningsavstämningsjournal** måste du använda sidan **Bankkontoavstämning**. Mer information finns i [Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]