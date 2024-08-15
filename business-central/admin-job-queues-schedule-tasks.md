---
title: Schemalägga projekt att köras automatiskt
description: Lär dig använda projektkötransaktioner för att köra rapporter och codeunit.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 07/16/2024
ms.custom: bap-template
ms.search.form: '672, 673, 674, 671'
ms.service: dynamics-365-business-central
---
# Använda projektköer för att schemalägga uppgifter

Använd sidan **Jobbkötransaktioner** för att schemalägga och köra specifika rapporter och kodenheter. Du kan ange att projekt ska köras en gång eller återkommande. Exempelvis vill du kanske köra rapporten **Salesperson * Sales Statistics** veckovis i syfte att spåra en säljares säljaktivitet varje vecka, eller också kanske du vill köra codeunit **Delegate Approval Requests** dagligen i syfte att förhindra att dokument ansamlas.

Sidan **Projektkötransaktioner** fönstret visas alla aktuella jobb. Om du lägger till en projektkötransaktion som körs på ett schema måste du ange en del information. Till exempel:

* Den objekttyp som ska köras, t.ex. en rapport eller codeunit. Du måste ha behörighet att köra rapporten eller codeunit.
* Objektets namn och objekt-ID.
* Parametrar för att ange beteendet för projektkötransaktionen. Du kan t.ex lägga till en planeringsparameter om att endast skicka bokförda försäljningsorder.
* Schemat för när och hur ofta projektkötransaktionen körs.

> [!IMPORTANT]  
> Om du tilldelas behörighetsuppsättningen SUPER som följer med [!INCLUDE[prod_short](includes/prod_short.md)] har du behörighet att köra alla artiklar som licensen medger. Om du har rollen Delegerad admin kan du skapa och schemalägga projektkötransaktioner, men endast administratörer och licensierade användare kan köra dem.

När ett projekt har slutförts korrekt, tar [!INCLUDE [prod_short](includes/prod_short.md)] bort det från listan över projektkötransaktioner, om det inte är ett återkommande projekt. Om det är ett återkommande projekt justeras fältet **tidigaste starttiden** till att visa nästa gång projektet ska köras.

## Viktigt för att schemalägga återkommande projekt

> [!IMPORTANT]  
> Återkommande projektköer kan påverka prestanda, så du bör inte köra dem för ofta. När du anger hur ofta ett återkommande projekt ska köras bör du försöka ange det största tidsintervall som du kan. Om du till exempel ska ange en upprepning på fem minuter kan du överväga om det kan vara 15 minuter eller till och med en gång i timmen istället. När du planerar för återkommande projektköer bör du tänka på vilka områden i programmet som projektet kommer att påverka. Är det ett område där många användare arbetar och kommer att påverkas av tung aktivitet? Tänk på längden på en enda projektkörning och affärsmotivationen för att köra projekt med en viss kadens.

## Tidigaste startdatum

Värdet i fältet **Tidigaste startdatum/starttid** på sidan **Transaktionskort för projektkö** visar nästa gång projektet ska köras. Det finns flera faktorer som kan påverka om en projektköpost verkligen körs vid den tidpunkten.

De vanligaste faktorerna är antalet projektkötransaktioner i en miljö och det totala antalet schemalagda aktiviteter. För att skydda prestandanivåer finns det driftsgränser. Om du har många transaktioner och till exempel om en av dem misslyckas eller tar längre tid än förväntat, kanske nästa projekt inte startar vid den förväntade tidpunkten. Om du har kodmoduler som genererar 100 000 eller fler schemalagda aktiviteter bör du undersöka om du verkligen behöver alla dessa aktiviteter. Du kan öppna listan över alla schemalagda aktiviteter på sidan **Schemalagda aktiviteter**.

Mer information om hur du övervakar status för projektkötransaktioner finns i [Så här visar du status för alla projekt](#to-view-status-for-any-job). Mer information om driftsbegränsningar finns i [Asynkrona aktivitetsgränser](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#Task).

## Övervaka status eller fel i projektkön

Data som projektkön genererar lagras så att du kan felsöka fel.  

För varje projektkötransaktion kan du visa och ändra statusen. När du skapar en projektkötransaktion anges dess status som **Stoppad**. Du kan exempelvis ange statusen som **Klar** och åter som **Stoppad**. I annat fall uppdateras information om status automatiskt.

I följande tabell beskrivs värdena i fältet **Status**.

| Status | Description |
|--|--|
| Klar | Jobbkötransaktionen är redo att köras. |
| Pågående | Jobbkötransaktionen pågår. Det här fältet uppdateras medan projektkön körs. |
| Stoppad | Standardstatusen för projektkötransaktionen när du skapade den. Välj åtgärden **Ställ in statusen som Klar** för att ändra statusen till **Klar**. Välj åtgärden **Stoppa** om du vill återställa till **Stoppad**. Om du vill veta mer går du till [Om Stoppad](#about-on-hold).|
| Stoppad på grund av inaktivitet | Används främst för projektkötransaktioner som schemalägger synkronisering mellan [!INCLUDE [prod_short](includes/prod_short.md)] och en annan app, t.ex. [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Mer information om den här statusen finns i [Om tidsgränser för inaktivitet](/dynamics365/business-central/admin-scheduled-synchronization-using-the-synchronization-job-queue-entries#about-inactivity-timeouts). |
|Väntar | Gäller endast för projektkötransaktioner som har tilldelats en kategorikod. Anger att projektet är schemalagt, men att den underliggande schemalagda uppgiften inte är aktiv. Efter att projektköposten som för närvarande körs och är i samma kategori avslutas, ändras statusen för nästa projekt i kategorin med status Väntar till Klar. |
| Fel | Något gick fel. Välj **Visa fel** för att visa felmeddelandet. |
| Slutförd | Jobbkötransaktionen har slutförts. |

 > [!TIP]  
> Jobbkötransaktioner stoppades när ett fel inträffar. Det kan till exempel vara problem när en post ansluter till en extern tjänst, till exempel en bankfeed. Om tjänsten inte är tillgänglig för tillfället och projektkötransaktionen inte kan ansluta visas ett felmeddelande i transaktionen och den stoppas. Du måste starta om projektkötransaktionen manuellt. Men fälten **Maximalt antal försök** och **Kör fördröjning igen (sek.)** kan du undvika problemet. Fältet **Maximalt antal försök** låter dig ange hur många gånger projektkötransaktionen kan misslyckas innan den slutar att försöka köras. Fältet **Kör fördröjning igen (sek.)** låter dig ange hur lång tid, i sekunder, mellan försöken. Kombinationen av dessa två fält kan behålla projektkötransaktionen tills den externa servicen blir tillgänglig.

### Om Stoppad

Att ange en projektköpost till **Stoppad** påverkar inte ett projekt som redan körs. När ett projekt startar fortsätter det att köras tills det är slutfört, oavsett eventuella efterföljande ändringar som görs i projektköposten, till exempel att stoppa det.<br><br>Statusen **Stoppad** används vanligtvis för att förhindra att ett projekt startar automatiskt när det når sin schemalagda starttid. Det gör att du tillfälligt kan pausa ett projekt innan det börjar bearbetas. <br><br>Om du behöver stoppa eller avbryta ett projekt som körs kan du ingripa manuellt i processen. Du kan till exempel stoppa motsvarande session eller process.

### Så här visar du status för ett projekt

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **projektkötransaktioner** och välj sedan relaterad länk.
2. På sidan **projektkötransaktioner** väljer du en projektkötransaktion, och väljer sedan åtgärden **loggposter**.  

> [!TIP]
> För mer djupgående analys baserad på telemetri kan du välja Application Insights i Microsoft Azure för att granska statusen för projektkötransaktioner. För att lära dig mer om telemetri, gå till [Övervaka och analysera telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) och [Analysera spårningstelemetri för livscykel för projektkö](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

## Visa schemalagda uppgifter

På sidan **schemalagda uppgifter** i [!INCLUDE [prod_short](includes/prod_short.md)] visas vilka uppgifter som är klara att köras i projektkön. På sidan visas också information om det företag som varje aktivitet har konfigurerats för att köras i. Endast aktiviteter som är markerade som tillhör den aktuella miljön kan dock köras.  

Om det aktuella företaget exempelvis finns i en miljö som är en kopia av en annan miljö stoppas alla schemalagda aktiviteter. Använd sidan **Schemalagda uppgifter** för att visa vilka uppgifter som är klara att köras i projektkön.  

> [!NOTE]
> Interna administratörer och licensierade användare kan schemalägga aktiviteter så att de körs. Delegerade administratörer kan konfigurera och schemalägga aktiviteter så att de körs, men endast licensierade användare kan köra dem.

## Min projektködel

I **Min projektködel** i ditt rollcenter visas de projektköer som du har inlett men som ännu inte slutfört. Som standard visas inte delen, så du behöver lägga till den i ditt rollcenter. Om du vill veta mer om anpassning, gå till [Anpassa arbetsyta](ui-personalization-user.md).  

Delen visar följande information:

* Vilka dokument med ditt ID i fältet **Tilldelat användar-ID** so behandlas eller står i kö, inklusive de dokument som bokförs i bakgrunden. 
* Om det uppstod ett fel vid bokföring av ett dokument eller i projektkötransaktionen. 

Delen Min projektkö ger dig också möjlighet att makulera en dokumentbokföring.

### Så här kan du visa ett fel från delen Min projektkö

1. På en transaktion med statusen **fel**, väljer du åtgärden **Visa felet**.
2. Granska felmeddelandet och lös problemet.

## Exempel på vad du kan schemalägga med projektkötransaktioner

### Schemalägg rapporter

Du kan schemalägga en rapport eller batchprojekt att köras vid ett visst datum och en viss tidpunkt. Planerade rapporter och batchprojekt anges i projektkön och behandlas vid den planerade tid, på liknande sätt som andra projekt. Du väljer alternativet **Schemalägg** när du har valt åtgärden **Skicka till**, och anger sedan information om t. ex. skrivare, tid och datum samt frekvens.  

Om du vill veta mer om schemaläggning går du till [Schemaläggning av en rapport som ska köras](ui-work-report.md#ScheduleReport)

### Schemalägg synkronisering mellan [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)]

Om du integrerar [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)] kan projektkön schemalägga när data ska synkroniseras. Beroende på vilken riktning och vilka regler du definierar kan projektkötransaktionen skapa poster i ett program för att matcha poster i den andra. Ett bra exempel är när du registrerar en kontakt i [!INCLUDE[crm_md](includes/crm_md.md)] en projektkötransaktion kan du ange den kontakten åt dig i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du vill veta mer om schemaläggning, gå till [Schemalägga en synkronisering mellan Business Central och Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### Schemalägg när du ska bokföra försäljnings- och inköpsorder

Med hjälp av projektkötransaktioner kan du schemalägga affärsprocesser så att de körs i bakgrunden. Till exempel är bakgrundsuppgifter användbara när då flera användare bokför försäljningsorder samtidigt, men endast en order kan behandlas i taget. Om du vill veta mer om bakgrundsbokföring går du till [Så här ställer du in bakgrundsbokföring med projektköer](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## Hantera problem med projektkötransaktioner

Om en projektkötransaktion visar ett fel, är ditt första alternativ att lösa problemet att starta om projektkötransaktionen. Du kan ställa in statusen för projektkötransaktionen till **Stoppad** och sedan **Klar** eller bara starta om den.

Om en omstart inte hjälper kan problemet bero på koden. Du kan hitta ägaren (kallas även för *utgivaren*) av koden i Al stackspåret i projektkön. Om felet kommer från ett program/tillägg kontaktar du din Microsoft-partner. Om felet kommer från ett Microsoft-program öppnar du ett supportärende med Microsoft.

Om du kontaktar Microsoft-partnern eller Microsoft för support bör du ange följande information:

* ID:t för jobbkötransaktionen körs där felet uppstod
* Tidsstämpeln för när felet inträffade
* Din tidszon

> [!TIP]
> Beroende på om din [!INCLUDE [prod_short](includes/prod_short.md)] är tidigare eller senare än version 22.1, samla in informationen på följande sätt:
>
> * För tidigare versioner anger du en skärmbild av sidan **Loggposter för projektkö**.
> * För senare versioner använder du åtgärden **Kopiera detaljer** på sidan Loggposter för projektkö för att kopiera informationen (projektkö-ID, tidsstämpel och tidszon).

## Övervaka projektkön med telemetri

Administratörer kan använda [Azure Application Insights](/azure/azure-monitor/app/app-insights-overview) för att samla in och analysera telemetri för att identifiera problem. För att lära dig mer om telemetri, gå till [Övervaka och analysera telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) och [Analysera spårningstelemetri för livscykel för projektkö](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

Med hjälp av telemetri kan administratörer ställa in aviseringar på de projektköer som skickar ett textmeddelande, e-postmeddelande eller ett meddelande i Teams om något inte är rätt. Om du vill veta mer om dessa aviseringar går du till [Avisering om telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-alert).

## Se även

[Administration](admin-setup-and-administration.md)  
[Ställa in Business Central](setup.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Analysera spårningstelemetri för livscykel för projektkö](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  
[Avisering om telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-alert)

[!INCLUDE[footer-include](includes/footer-banner.md)]
