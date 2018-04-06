---
title: "Använda automatisk koppling för att stämma av betalningar | Microsoft Docs "
description: "Beskriver hur du använder funktionen automatisk koppling när du använder utbetalningar eller inbetalningar till deras relaterade öppna transaktioner och stämma av betalningar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 79e7b23efb22f606351840ad613de9537fe30289
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="reconcile-payments-using-automatic-application"></a>Stämma av betalningar genom att använda automatisk koppling
Fönstret **Betalningsavstämningsjournal** anger betalningar, antingen inkommande eller utgående, som har registrerats som transaktioner på ditt onlinebankkonto och som du kan koppla till deras motsvarande öppna kund-, leverantör- och bankkontotransaktioner. Raderna i journalen fylls i genom att importera kontoutdraget från banken som en bankfeed eller fil.

En betalningsavstämningsjournal är relaterad till ett bankkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)] som återspeglar det onlinebankkonto där betalningstransaktionerna registreras. Eventuella öppna bankkontotransaktioner som relateras till kopplade kund- eller leverantörsreskontratransaktionerna kommer att avslutas när du väljer **Bokför betalningar och stäm av bankkonton**. Detta betyder att bankkontot stäms av automatiskt för betalningar som du bokför med journalen.

Om du vill aktivera import av bankutdrag som en bankfeed måste du först skapa och aktivera tjänsten Envestnet Yodlee bankfeeder och sedan länka bankkontot till dess relaterade onlinebankkonto. Betalningsavstämningsjournalen hittar sedan automatiskt bankfeeder, när du väljer åtgärden **Importera banktransaktioner**. Dessutom kan du konfigurera ett bankkonto att automatiskt importera nya kontoutdragfeeder varje timme. Transaktioner för utbetalningar som redan har bokförts som kopplade och/eller avstämda kommer inte att importeras. Mer information finns i [Konfigurera du bankfeedtjänsten Envestnet Yodlee](bank-how-setup-bank-statement-service.md).

Med åtgärden **Mappa text till konto** kan du skapa mappningar mellan text på betalningar och specifika debet-, kredit- och balanskonton så att sådana betalningar bokförs på de angivna kontona när du bokför betalningar i betalningsavstämningsjournalen. Se steg 8. Mer information finns i [Mappa text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Liknande funktioner finns för att stämma av överskottbelopp på Betalningsavstämningsjournaler på en ad hoc-basis. Mer information finns i [Stämma av betalningar som inte kan kopplas](receivables-how-reconcile-payments-cannot-apply-auto.md).

Du använder funktionen **Koppla automatiskt**, antingen automatiskt när du importerar en bankfil eller feed med betalningstransaktioner eller när du aktiverar den, för att koppla betalningar till deras motsvarande öppna transaktioner vid en matchning av data på en journalrad med data i en eller flera öppna transaktioner.

På journalrader där en betalning har kopplats automatiskt till en eller flera öppna transaktioner har fältet **Matchningssäkerhet** ett värde mellan Låg och Hög som anger kvaliteten för de data som matchar dem som den föreslagna betalningskopplingen baseras på. Dessutom fylls fälten **Kontotyp** och **Kontonr.** med information om den kund eller leverantör som betalningen gäller. Om du har ställt in en text-till-konto-mappning kan den automatiska kopplingen ge ett matchningssäkerhetsvärde på **Hög – text-till-konto-mappning**.

För varje journalrad som representerar en betalning i fönstret **Betalningsavstämningsjournal** kan du öppna fönstret **Betalningskoppling** för att visa alla öppna kandidattransaktioner för betalningen och för att visa detaljerad information för varje transaktion om datamatchningen som en betalningskoppling baseras på. Här kan du koppla manuellt betalningar eller koppla om betalningar som kopplades automatiskt till fel transaktion. Mer information finns i [Granska och koppla betalningar efter automatisk koppling](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
>   Du kan starta banktransaktionsimporten samtidigt som du öppnar fönstret **Betalningsavstämningjournal** för en befintlig betalningsavstämningjournal i fönstret **Betalningsavstämningjournaler**. Följande procedurer beskriver hur du importerar banktransaktioner till fönstret **Betalningsavstämningsjournal** när du har skapat en ny journal.

## <a name="to-reconcile-payments-using-automatic-application"></a>Så här stämmer du av betalningar genom att använda automatisk koppling
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Betalningsavstämningsjournaler** och välj sedan relaterad länk.
2. Om du vill arbeta i en ny betalningsavstämningsjournal väljer du åtgärden **Ny journal**.
3. I fönstret **Betalningsbankkontolista** väljer du det bankkonto som du vill stämma av betalningar för och väljer sedan knappen **OK**.
   Fönstret **Betalningsavstämningsjournal** öppnas förberett för det valda bankkontot.
4. Välj åtgärden **Importera banktransaktioner**.
   Om bankkontot för den valda journalen inte är inställd för import av banktransaktioner visas en dialogruta för att fylla i de relevanta fälten.
5. I fönstret **Välj en fil att importera** väljer du den fil som innehåller banktransaktionerna för betalningarna du vill avstämma, och väljer sedan knappen **Öppna**.  
6. Om kontoutdragtjänsten är aktiverad anger du intervallet när kontoutdragen importeras i fönstret **kontoutdragfilter**.

    Fönstret **Betalningsavstämningsjournal** fylls i med rader för betalningar som representerar banktransaktioner i det importerade bankkontoutdraget.

    På rader för betalningar som har kopplats automatiskt till sina relaterade öppna transaktioner har fältet **Matchningssäkerhet** har ett värde mellan **Låg** och **Hög** som anger kvaliteten för de data som matchar de som den föreslagna betalningskopplingen baseras på. Dessutom fylls fälten **Kontotyp** och **Kontonr.** med information om den kund eller leverantör som betalningen gäller.
7. Välj en journalrad och välj sedan åtgärden **Koppla manuellt** för att granska, koppla om eller koppla betalningen manuellt i fönstret **Betalningskoppling**. Mer information finns i [Granska och koppla betalningar efter automatisk koppling](receivables-how-review-apply-payments-auto-application.md).

    När du har slutfört en manuell koppling innehåller fältet **Matchningssäkerhet** på journalraden som du har bearbetat manuellt **Accepterat**.
8. Välj en inte kopplad journalrad för en återkommande inbetalning eller kostnad, till exempel ett bilbensinköp, och välj sedan åtgärden **Mappa text till konto** action. Mer information finns i [Mappa text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).
9. Välj åtgärden **Koppla manuellt** när du har slutfört en mappningen av betalningstext till konton.
10. När du tycker att alla betalningar på journalraderna har kopplats eller angetts till direktbokföring korrekt, väljer du åtgärden **Bokför**.

När du bokför betalningsavstämningsjournalen stängs de kopplade transaktionsnotorna och de relaterade kund-, leverantörs- eller redovisningskontona uppdateras. För betalningar på journalrader som baseras på text-till-konto-mappning uppdateras de angivna kund-, leverantörs- och redovisningskontona. För alla journalrader skapas bankkontotransaktioner. Eventuella öppna bankkontotransaktioner som relateras till kopplade kund- eller leverantörsreskontratransaktionerna kommer att avslutas när du väljer åtgärden **Bokför betalningar och stäm av bankkonton**. Detta betyder att bankkontot stäms av automatiskt för betalningar som du bokför med journalen.

Du kan jämföra värdet i fältet **Saldo på bankkonto efter bokföring** tillsammans med värdet i fältet **Kontoutdragets slutsaldo** för att spåra när bankkontot har stämts av baserat på betalningar som du bokför.

> [!NOTE]  
>   Om du inte vill stämma av bankkontot från **Betalningsavstämningsjournal** måste du använda fönstret **Bankkontoavstämning**. Mer information finns i [Stämma av bankkonton separat](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Se även
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

