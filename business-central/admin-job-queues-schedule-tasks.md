---
title: Schemalägga projekt att köras automatiskt
description: Schemalagda aktiviteter hanteras av jobbkön. Dessa jobb kör rapporter och kodenheter. Du kan ange att jobb ska köras en gång eller återkommande.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/12/2021
ms.author: edupont
ms.openlocfilehash: 29b5b3f633b0fd9fcac648f0bf7149b87ae0b20d
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013952"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Använda jobbköer för att schemalägga uppgifter

Med jobbköer i [!INCLUDE[prod_short](includes/prod_short.md)] kan användarna schemalägga och köra specifika rapporter och kodenheter. Du kan ange att jobb ska köras en gång eller återkommande. Exempelvis vill du kanske köra rapporten **Salesperson * Sales Statistics** veckovis i syfte att spåra en säljares säljaktivitet varje vecka, eller också kanske du vill köra codeunit **Delegate Approval Requests** dagligen i syfte att förhindra att dokument ansamlas eller på annat sätt blockerar arbetsflödet.

Sidan **Jobbkötransaktioner** fönstret visas alla aktuella jobb. Om du lägger till en ny jobbkötransaktion som du vill schemalägga, måste du ange information om typen av objekt du vill köra, till exempel en rapport eller kodenhet för objekttypen, namnet och objekt-ID för objektet som ska köras. Du kan också lägga till parametrar för att ange beteendet för jobbkötransaktionen. Du kan t.ex lägga till en planeringsparameter om att endast skicka bokförda försäljningsorder. Du måste ha behörighet att köra en viss rapport eller kodenhet, annars returneras ett fel när jobbkön körs.  
> [!IMPORTANT]  
> Om du använder behörighetsuppsättningen SUPER som följer med demolicensen för [!INCLUDE[prod_short](includes/prod_short.md)] har du och dina användare behörigheter att köra alla artiklar som licensen medger. Detta räcker fortfarande inte för delegerad administratör eller användare med enhetslicens, som inte kan skapa hela jobbköer.

En jobbkö kan ha många transaktioner, som är de projekt som dokumentkön hanterar och kör. Information i transaktionen anger vilken rapport eller kodenhet som körs, när och hur ofta transaktionen körs, i vilken kategori projekt löper, och hur det körs.  

När jobbköer är inställda och körs kan status ändras enligt följande inom varje återkommande period:

* **Stoppad**  
* **Klar**  
* **Pågående**  
* **Fel**  
* **Avslutad**  

När ett projekt har slutförts korrekt, tas det bort från listan över jobbkötransaktioner, om det inte är ett återkommande projekt. Om det är ett återkommande projekt justeras fältet **tidigaste starttiden** till att visa nästa gång projektet förväntas köras.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Så här visar du status eller fel i jobbkön

Data som skapas när en jobbkö körs lagras i databasen, så att du kan felsöka jobbköfel.  
För varje jobbkötransaktion kan du visa och ändra statusen. När du skapar en jobbkötransaktion anges dess status som **Stoppad**. Du kan exempelvis ange statusen som **Klar** och åter som **Stoppad**. I annat fall uppdateras information om status automatiskt.

I följande tabell beskrivs värdena i fältet **Status**.

| Status | Beskrivning |
|--|--|
| Klar | Anger att jobbkötransaktionen är redo att köras. |
| Pågående | Anger att jobbkötransaktionen pågår. Det här fältet uppdateras medan jobbkön körs. |
| Stoppad | Standard. Anger statusen för jobbkötransaktionen när den skapas. Välj åtgärden **Ställ in statusen som Klar** för att ändra statusen till **Klar**. Välj åtgärden **Stoppa** eller **Gör uppehåll** om du vill ändra statusen tillbaka till **Stoppad**. |
| Fel | Anger att det finns ett fel. Välj **Visa fel** för att visa felmeddelandet. |
| Avslutad | Anger att jobbkötransaktionen har slutförts. |

### <a name="to-view-status-for-any-job"></a>Så här visar du status för ett projekt
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **jobbkötransaktioner** och välj sedan relaterad länk.
2. På sidan **jobbkötransaktioner** väljer du en jobbkötransaktion, och väljer sedan åtgärden **loggposter**.  

> [!TIP]
> Med [!INCLUDE [prod_short](includes/prod_short.md)] online kan du även visa statusen för jobbkötransaktioner genom att använda Application Insights i Microsoft Azure. Mer information finns i [Analysera spårningstelemetri för livscykel för jobbkö](/dynamics365smb-devitpro\dev-itpro\administration\telemetry-job-queue-lifecycle-trace) i [!INCLUDE [prod_short](includes/prod_short.md)]-hjälpen för utvecklare och IT-proffs.

## <a name="the-my-job-queue-part"></a>Min jobbködel
I **Min jobbködel** i ditt rollcenter visas de jobbköer som du har inlett men som ännu inte slutfört. Som standard visas inte delen, så du behöver lägga till den i ditt rollcenter. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).  

I den här delen kan du se dokument med ditt ID i fältet **Tilldelat användar-ID** so behandlas eller står i kö, inklusive de som är relaterade till bakgrundsbokföring. Här ser du snabbt om det har uppstått ett fel i bokföringen av ett dokument, eller om det finns fel i en jobbkötransaktion. Delen ger dig också möjlighet att makulera en dokumentbokföring, om den inte körs.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Så här kan du visa ett fel från delen Min jobbkö
1. På en transaktion med statusen **fel**, väljer du åtgärden **Visa felet**.
2. Granska felmeddelande och lös problemet.


## <a name="examples-of-what-can-be-scheduled-using-job-queue"></a>Exempel på vad som kan schemaläggas med hjälp av en jobbkö

### <a name="schedule-reports"></a>Schemalägg rapporter

Du kan schemalägga en rapport eller batch-jobb att köras vid ett visst datum och en viss tidpunkt. Planerade rapporter och batch-jobb anges i jobbkön och behandlas vid den planerade tid, på liknande sätt som andra jobb. Du väljer alternativet **Schemalägg** när du har valt åtgärden **Skicka till**, och anger sedan information om t.ex. skrivare, tid och datum samt frekvens.  

Mer information finns i [Schemalägg en rapport för körning](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between-prod_short-and-prod_short"></a>Schemalägg synkronisering mellan [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)]

Om du har integrerat [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)] kan du använda jobbkön för att schemalägga när du vill synkronisera data för de poster som du har sammankopplat i de två företagsapparna.. Beroende på den riktning och de regler som du har definierat för integreringen kan synkroniseringsjobbet också skapa nya poster i målappen som matchar dem i källan. Om t.ex. en säljare skapar en ny kontakt i [!INCLUDE[crm_md](includes/crm_md.md)] kan synkroniseringsschemat skapa kontakten för den kopplade säljaren i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer finns i [Schemalägga en synkronisering mellan Business Central och Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-the-posting-of-sales-and-purchase-orders"></a>Schemalägg bokföring av försäljnings- och inköpsorder

Jobbköer är ett effektivt verktyg som schemalägger körning av affärsprocesser i bakgrunden, till exempel när flera användare prövar att bokföra försäljningsorder, men endast en order kan behandlas i taget.  

Mer information finns i [Så här konfigurerar du bakgrundsbokföring med jobbköer](ui-batch-posting.md#to-set-up-background-posting-with-job-queues)

## <a name="see-also"></a>Se även

[Administration](admin-setup-and-administration.md)  
[Ställa in Business Central](setup.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Analysera spårningstelemetri för livscykel för jobbkö](/dynamics365smb-devitpro\dev-itpro\administration\telemetry-job-queue-lifecycle-trace)  
