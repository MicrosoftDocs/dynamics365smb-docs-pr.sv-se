---
title: Schemalägga projekt att köras automatiskt
description: Lär dig använda jobbkötransaktioner för att köra rapporter och codeunit.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 08/24/2023
ms.custom: bap-template
ms.search.form: '672, 673, 674, 671'
---
# Använda jobbköer för att schemalägga uppgifter

Använd sidan **Jobbkötransaktioner** för att schemalägga och köra specifika rapporter och kodenheter. Du kan ange att jobb ska köras en gång eller återkommande. Exempelvis vill du kanske köra rapporten **Salesperson * Sales Statistics** veckovis i syfte att spåra en säljares säljaktivitet varje vecka, eller också kanske du vill köra codeunit **Delegate Approval Requests** dagligen i syfte att förhindra att dokument ansamlas.

Sidan Projektkötransaktioner fönstret visas alla aktuella jobb. Om du lägger till en ny jobbkötransaktion som körs på ett schema måste du ange en del information. Som exempel:

* Den objekttyp som ska köras, t.ex. en rapport eller codeunit. Du måste ha behörighet att köra den aktuella rapporten eller codeunit.
* Objektets namn och objekt-ID.
* Parametrar för att ange beteendet för jobbkötransaktionen. Du kan t.ex lägga till en planeringsparameter om att endast skicka bokförda försäljningsorder.
* När och hur ofta jobbkötransaktionen ska köras.

> [!IMPORTANT]  
> Om du tilldelas behörighetsuppsättningen SUPER som följer med [!INCLUDE[prod_short](includes/prod_short.md)] har du behörighet att köra alla artiklar som licensen medger. Om du har rollen Delegerad admin kan du skapa och schemalägga jobbkötransaktioner, men endast administratörer och licensierade användare kan köra dem.

När jobbköer är inställda och körs kan status ändras enligt följande inom varje återkommande period:

* **Stoppad**  
* **Klar**  
* **Pågående**  
* **Fel**  
* **Avslutad**  
* **Stoppad på grund av inaktivitet**

> [!NOTE]
> Statusen **Stoppad på grund av inaktivitet Inactivity** används främst för jobbkötransaktioner som schemalägger synkronisering mellan [!INCLUDE [prod_short](includes/prod_short.md)] och en annan app, t.ex. [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Mer information om den här statusen finns i [Om tidsgränser för inaktivitet](/dynamics365/business-central/admin-scheduled-synchronization-using-the-synchronization-job-queue-entries#about-inactivity-timeouts).

När ett projekt har slutförts korrekt, tas det bort från listan över jobbkötransaktioner, om det inte är ett återkommande projekt. Om det är ett återkommande projekt justeras fältet **tidigaste starttiden** till att visa nästa gång jobbet ska köras.  

## Tidigaste startdatum

Värdet i fältet **Tidigaste startdatum/starttid** på sidan **Transaktionskort för jobbkö** visar nästa gång projektet ska köras. Det finns flera faktorer som kan påverka om en jobbköpost verkligen körs vid den tidpunkten.

De vanligaste faktorerna är antalet jobbkötransaktioner i en miljö och det totala antalet schemalagda aktiviteter. För att skydda prestandanivåer finns det driftsgränser. Om du har många transaktioner i kön och till exempel om en av dem misslyckas eller om transaktionerna bara tar längre tid än förväntat, kanske nästa jobb inte startar vid den förväntade tidpunkten. Om du har kodmoduler som genererar 100 000 eller fler schemalagda aktiviteter bör du undersöka om du verkligen behöver alla dessa aktiviteter. Du kan öppna listan över alla schemalagda aktiviteter på sidan **Schemalagda aktiviteter**.

Mer information om hur du övervakar status för jobbkötransaktioner finns i [Så här visar du status för alla projekt](#to-view-status-for-any-job). Mer information om driftsbegränsningar finns i [Asynkrona aktivitetsgränser](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#Task).

## Övervaka status eller fel i jobbkön

Data som jobbkön genererar lagras så att du kan felsöka fel.  

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
> För mer djupgående analys baserad på telemetri kan du välja Application Insights i Microsoft Azure för att granska statusen för jobbkötransaktioner. För att lära dig mer om telemetri, gå till [Övervaka och analysera telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) och [Analysera spårningstelemetri för livscykel för jobbkö](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

## Visa schemalagda uppgifter

På sidan **schemalagda uppgifter** i [!INCLUDE [prod_short](includes/prod_short.md)] visas vilka uppgifter som är klara att köras i jobbkön. På sidan visas också information om det företag som varje aktivitet har konfigurerats för att köras i. Endast aktiviteter som är markerade som tillhör den aktuella miljön kan dock köras.  

Om det aktuella företaget exempelvis finns i en miljö som är en kopia av en annan miljö stoppas alla schemalagda aktiviteter. Använd sidan **Schemalagda uppgifter** för att visa vilka uppgifter som är klara att köras i jobbkön.  

> [!NOTE]
> Interna administratörer och licensierade användare kan schemalägga aktiviteter så att de körs. Delegerade administratörer kan konfigurera och schemalägga aktiviteter så att de körs, men endast licensierade användare kan köra dem.

## Min jobbködel

I **Min jobbködel** i ditt rollcenter visas de jobbköer som du har inlett men som ännu inte slutfört. Som standard visas inte delen, så du behöver lägga till den i ditt rollcenter. Om du vill veta mer om anpassning, gå till [Anpassa arbetsyta](ui-personalization-user.md).  

Delen visar följande information:

* Vilka dokument med ditt ID i fältet **Tilldelat användar-ID** so behandlas eller står i kö, inklusive de dokument som bokförs i bakgrunden. 
* Om det uppstod ett fel vid bokföring av ett dokument eller i jobbkötransaktionen. 

Delen Min jobbkö ger dig också möjlighet att makulera en dokumentbokföring.

### Så här kan du visa ett fel från delen Min jobbkö

1. På en transaktion med statusen **fel**, väljer du åtgärden **Visa felet**.
2. Granska felmeddelandet och lös problemet.

## Exempel på vad du kan schemalägga med jobbkötransaktioner

### Schemalägg rapporter

Du kan schemalägga en rapport eller batch-jobb att köras vid ett visst datum och en viss tidpunkt. Planerade rapporter och batch-jobb anges i jobbkön och behandlas vid den planerade tid, på liknande sätt som andra jobb. Du väljer alternativet **Schemalägg** när du har valt åtgärden **Skicka till**, och anger sedan information om t. ex. skrivare, tid och datum samt frekvens.  

Om du vill veta mer om schemaläggning går du till [Schemaläggning av en rapport som ska köras](ui-work-report.md#ScheduleReport)

### Schemalägg synkronisering mellan [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)]

Om du har integrerat [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)] kan jobbkön schemalägga när data ska synkroniseras. Beroende på vilken riktning och vilka regler du definierat kan jobbkötransaktionen skapa poster i ett program för att matcha poster i den andra. Ett bra exempel är när du registrerar en kontakt i [!INCLUDE[crm_md](includes/crm_md.md)] en jobbkötransaktion kan du ange den kontakten åt dig i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du vill veta mer om schemaläggning, gå till [Schemalägga en synkronisering mellan Business Central och Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### Schemalägg när du ska bokföra försäljnings- och inköpsorder

Med hjälp av jobbkötransaktioner kan du schemalägga affärsprocesser så att de körs i bakgrunden. Till exempel är bakgrundsuppgifter användbara när då flera användare bokför försäljningsorder samtidigt, men endast en order kan behandlas i taget. Om du vill veta mer om bakgrundsbokföring går du till [Så här ställer du in bakgrundsbokföring med jobbköer](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## Hantera problem med jobbkötransaktioner

Om en jobbkötransaktion visar ett fel, är ditt första alternativ att lösa problemet att starta om jobbkötransaktionen. Du kan ställa in statusen för jobbkötransaktionen till **Stoppad** och sedan **Klar** eller bara starta om den.

Om en omstart inte hjälper kan problemet bero på koden. Du kan hitta ägaren (kallas även för *utgivaren*) av koden i Al stackspåret i jobbkön. Om felet kommer från ett program/tillägg kontaktar du din Microsoft-partner. Om felet kommer från ett Microsoft-program öppnar du ett supportärende med Microsoft.

Om du kontaktar Microsoft-partnern eller Microsoft för support bör du ange följande information:

* ID för jobbkötransaktionen som kördes där felet inträffade
* Tidsstämpeln för när felet inträffade
* Din tidszon

> [!TIP]
> Beroende på om din [!INCLUDE [prod_short](includes/prod_short.md)] är tidigare eller senare än version 22.1, samla in informationen på följande sätt:
>
> * För tidigare versioner anger du en skärmbild av sidan **Loggtransaktioner för jobbkö**.
> * För senare versioner använder du åtgärden **Kopiera detaljer** på sidan Loggtransaktioner för jobbkö för att kopiera informationen (jobbkö-ID, tidsstämpel och tidszon).

## Övervaka jobbkön med telemetri

Administratörer kan använda [Azure Application Insights](/azure/azure-monitor/app/app-insights-overview) för att samla in och analysera telemetri för att identifiera problem. För att lära dig mer om telemetri, gå till [Övervaka och analysera telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) och [Analysera spårningstelemetri för livscykel för jobbkö](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

Med hjälp av telemetri kan administratörer ställa in aviseringar på de jobbköer som skickar ett textmeddelande, e-postmeddelande eller ett meddelande i Teams om något inte är rätt. Om du vill veta mer om dessa aviseringar går du till [Avisering om telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-alert).

## Se även

[Administration](admin-setup-and-administration.md)  
[Ställa in Business Central](setup.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Analysera spårningstelemetri för livscykel för jobbkö](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  
[Avisering om telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-alert)

[!INCLUDE[footer-include](includes/footer-banner.md)]
