---
title: Schemalägga projekt att köras automatiskt
description: Schemalagda aktiviteter hanteras av jobbkön. Dessa jobb kör rapporter och kodenheter. Du kan ange att jobb ska köras en gång eller återkommande.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '672, 673, 674, 671'
ms.date: 10/01/2021
ms.author: edupont
---
# Använda jobbköer för att schemalägga uppgifter

Med sidan Jobbkötransaktioner kan användarna schemalägga och köra specifika rapporter och kodenheter. Du kan ange att jobb ska köras en gång eller återkommande. Exempelvis vill du kanske köra rapporten **Salesperson * Sales Statistics** veckovis i syfte att spåra en säljares säljaktivitet varje vecka, eller också kanske du vill köra codeunit **Delegate Approval Requests** dagligen i syfte att förhindra att dokument ansamlas.

Sidan **Projektkötransaktioner** fönstret visas alla aktuella jobb. Om du lägger till en ny jobbkötransaktion som du vill tidsplanera måste du ange en del information. Till exempel:

* Den objekttyp som du vill köra, t. ex. en rapport eller codeunit. Du måste ha behörighet att köra den aktuella rapporten eller codeunit.
* Objektets namn och objekt-ID. 
* Parametrar för att ange beteendet för jobbkötransaktionen. Du kan t.ex lägga till en planeringsparameter om att endast skicka bokförda försäljningsorder. 
* När och hur ofta jobbkötransaktionen ska köras.

> [!IMPORTANT]  
> Om du tilldelas behörighetsuppsättningen SUPER som följer med [!INCLUDE[prod_short](includes/prod_short.md)] har du behörighet att köra alla artiklar som licensen medger. Om du har rollen Delegerad admin kan du skapa och schemalägga jobbkötransaktioner, men endast administratörer och licensierade användare kan köra dem. Användare med enhetslicensen kan inte skapa eller köra jobbköer.

När jobbköer är inställda och körs kan status ändras enligt följande inom varje återkommande period:

* **Stoppad**  
* **Klar**  
* **Pågående**  
* **Fel**  
* **Avslutad**  

När ett projekt har slutförts korrekt, tas det bort från listan över jobbkötransaktioner, om det inte är ett återkommande projekt. Om det är ett återkommande projekt justeras fältet **tidigaste starttiden** till att visa nästa gång projektet förväntas köras.  

## Övervaka status eller fel i jobbkön

Data som skapas när en jobbkö genereras lagras i databasen, så att du kan felsöka jobbköfel.  

För varje jobbkötransaktion kan du visa och ändra statusen. När du skapar en jobbkötransaktion anges dess status som **Stoppad**. Du kan exempelvis ange statusen som **Klar** och åter som **Stoppad**. I annat fall uppdateras information om status automatiskt.

I följande tabell beskrivs värdena i fältet **Status**.

| Status | Description |
|--|--|
| Klar | Jobbkötransaktionen är redo att köras. |
| Pågående | Jobbkötransaktionen pågår. Det här fältet uppdateras medan jobbkön körs. |
| Stoppad | Standardstatusen för jobbkötransaktionen när den skapas. Välj åtgärden **Ställ in statusen som Klar** för att ändra statusen till **Klar**. Välj åtgärden **Stoppa** om du vill återställa till **Stoppad**. |
| Fel | Något gick fel. Välj **Visa fel** för att visa felmeddelandet. |
| Slutförd | Jobbkötransaktionen har slutförts. |

> [!Tip]  
> Jobbkötransaktioner stoppades när ett fel inträffar. Det kan till exempel vara problem när en post ansluter till en extern tjänst, till exempel en bankfeed. Om tjänsten inte är tillgänglig för tillfället och jobbkötransaktionen inte kan ansluta visas ett felmeddelande i transaktionen och den stoppas. Du måste starta om jobbkötransaktionen manuellt. Men fälten **Maximalt antal försök** och **Kör fördröjning igen (sek.)** kan du undvika problemet. Fältet **Maximalt antal försök** låter dig ange hur många gånger jobbkötransaktionen kan misslyckas innan den slutar att försöka köras. Fältet **Kör fördröjning igen (sek.)** låter dig ange hur lång tid, i sekunder, mellan försöken. Kombinationen av dessa två fält kan behålla jobbkötransaktionen tills den externa servicen blir tillgänglig.

### Så här visar du status för ett projekt

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **jobbkötransaktioner** och välj sedan relaterad länk.
2. På sidan **jobbkötransaktioner** väljer du en jobbkötransaktion, och väljer sedan åtgärden **loggposter**.  

> [!TIP]
> Du kan också visa statusen för jobbkötransaktioner genom att använda Application Insights i Microsoft Azure för mer djupgående analys baserad på telemetri. Mer information finns i [Övervaka och analysera telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) och [Analysera spårningstelemetri för jobbkölivscykel](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) i utvecklar- och administrationsinnehållet för [!INCLUDE [prod_short](includes/prod_short.md)].

## Visa schemalagda uppgifter

På sidan **schemalagda uppgifter** i [!INCLUDE [prod_short](includes/prod_short.md)] visas vilka uppgifter som är klara att köras i jobbkön. På sidan visas också information om det företag som varje aktivitet har konfigurerats för att köras i. Endast aktiviteter som är markerade som tillhör den aktuella miljön kan dock köras.  

Om det aktuella företaget exempelvis finns i en miljö som är en kopia av en annan miljö stoppas alla schemalagda aktiviteter. Använd sidan **Schemalagda uppgifter** för att visa vilka uppgifter som är klara att köras i jobbkön.  

> [!NOTE]
> Interna administratörer och licensierade användare kan schemalägga aktiviteter så att de körs. Delegerade administratörer kan konfigurera och schemalägga aktiviteter så att de körs, men endast licensierade användare kan köra dem.

## Min jobbködel

I **Min jobbködel** i ditt rollcenter visas de jobbköer som du har inlett men som ännu inte slutfört. Som standard visas inte delen, så du behöver lägga till den i ditt rollcenter. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).  

Delen visar följande information:

* Vilka dokument med ditt ID i fältet **Tilldelat användar-ID** so behandlas eller står i kö, inklusive de dokument som bokförs i bakgrunden. 
* Om det uppstod ett fel vid bokföring av ett dokument eller i jobbkötransaktionen. 

Delen Min jobbkö ger dig också möjlighet att makulera en dokumentbokföring.

### Så här kan du visa ett fel från delen Min jobbkö

1. På en transaktion med statusen **fel**, väljer du åtgärden **Visa felet**.
2. Granska felmeddelande och lös problemet.

## Exempel på vad som kan schemaläggas med hjälp av en jobbkö

### Schemalägg rapporter

Du kan schemalägga en rapport eller batch-jobb att köras vid ett visst datum och en viss tidpunkt. Planerade rapporter och batch-jobb anges i jobbkön och behandlas vid den planerade tid, på liknande sätt som andra jobb. Du väljer alternativet **Schemalägg** när du har valt åtgärden **Skicka till**, och anger sedan information om t. ex. skrivare, tid och datum samt frekvens.  

Mer information finns i [Schemalägg en rapport för körning](ui-work-report.md#ScheduleReport)

### Schemalägg synkronisering mellan [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)]

Om du har integrerat [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)] kan jobbkön schemalägga när data ska synkroniseras. Beroende på vilken riktning och vilka regler du definierat kan jobbkötransaktionen skapa poster i ett program för att matcha poster i den andra. Ett bra exempel är när du registrerar en kontakt i [!INCLUDE[crm_md](includes/crm_md.md)] en jobbkötransaktion kan du ange den kontakten åt dig i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer finns i [Schemalägga en synkronisering mellan Business Central och Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### Schemalägg bokföring av försäljnings- och inköpsorder

Med hjälp av jobbkötransaktioner kan du schemalägga affärsprocesser så att de körs i bakgrunden. Till exempel är bakgrundsuppgifter användbara när då flera användare bokför försäljningsorder samtidigt, men endast en order kan behandlas i taget. Mer information finns i [Så här konfigurerar du bakgrundsbokföring med jobbköer](ui-batch-posting.md#to-set-up-background-posting-with-job-queues)

## Övervaka jobbkön med telemetri

Som administratör kan du använda [Application Insights](/azure/azure-monitor/app/app-insights-overview) för att samla in och analysera telemetri som du kan använda för att identifiera problem. Mer information finns i [Övervaka och analysera telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) i innehållet för utvecklare och administration.  

## Se även

[Administration](admin-setup-and-administration.md)  
[Ställa in Business Central](setup.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Analysera spårningstelemetri för livscykel för jobbkö](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]