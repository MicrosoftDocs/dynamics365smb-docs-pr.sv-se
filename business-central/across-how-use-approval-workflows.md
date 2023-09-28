---
title: Godkänna eller avvisa dokument i arbetsflöden
description: 'Begära, avvisa eller delegera godkännande av, till exempel ett inköps- eller försäljningsdokument, som en del av ett arbetsflöde.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '654, 662, 1500,'
ms.date: 09/12/2022
ms.author: bholtorf
---
# Så här använder du godkännande av arbetsflöden

När en post som till exempel ett inköpsdokument eller ett kundkort måste godkännas av någon i organisationen, skickar du en godkännandebegäran som en del av ett arbetsflöde. Beroende på hur arbetsflödet konfigureras meddelas sedan den lämpliga godkännaren om att posten kräver godkännande.

Du kan ställa in godkännandearbetsflöden på sidan **Arbetsflöde**. Du måste också ställa in godkännande användare, inklusive eventuella relevanta beloppsgränser, på sidan **användarinställningar för godkännande**. Läs mer i [Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md).  

Förutom arbetsflöden för godkännande som beskrivs i den här artikeln kan du utföra olika andra arbetsflödesuppgifter. Läs mer i [Använda arbetsflöden för godkännande](across-use-workflows.md).

Centrala arbetsflöden för godkännande för inköpsdokument, försäljningsdokument, utbetalningsjournaler, kundkort och artikelkort är klara att starta som guider. Lär dig mer på [Gör dig redo att göra affärer](ui-get-ready-business.md).

## Begära du godkännande av en post

Efterföljande aktivitet utförs av en godkännaranvändare.

1. På sidan som visar posten väljer du åtgärden **Skicka godkännandebegäran**.
2. För att alla godkännandebegäran, välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Transaktioner för godkännandebegärande** och välj sedan relaterad länk.  

Statusen på godkännandetransaktionen uppdateras från **Skapad** till **Öppen**. Statusen på posten, t. ex. en inköpsfaktura, uppdateras från **Öppen** till **Väntar på godkännande** och är låst för bearbetning tills alla godkännare har godkänt transaktionen.

När alla godkännare som krävs har godkänt transaktionen, ändras statusen till **Släppt**. Därefter kan du fortsätta arbeta med posten.

## Annullera godkännandebegäran

Efterföljande aktivitet utförs av en godkännaranvändare med behörigheten godkännare.

Det kan hända att en kund vill göra ändringar i en order efter att den har skickats till godkännande. I det här fallet kan du annullera godkännandeprocessen och göra nödvändiga ändringar i ordern innan du begär godkännande igen.

- På sidan som visar posten väljer du åtgärden **Avbryt godkännandebegäran**.

När godkännandebegäran har annullerats, ändras statusen på den relaterade godkännandeposten till **Annullerad**. Statusen på posten uppdateras från **Väntar på godkännande** till **Öppen**. Godkännandeprocessen kan sedan starta från början igen.

## Godkänna eller avvisa begäranden om godkännande

Efterföljande aktivitet utförs av en godkännaranvändare med behörigheten godkännare.

Du kan bearbeta godkännandebegäran på sidan **Begäranden att godkänna** inklusive godkänna flera begäran i taget. Du kan också godkänna enskilda poster genom att välja länken i det meddelande som du får.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **förfrågningar att godkänna** och välj sedan relaterad länk.
2. Markera en eller flera rader för posten som du vill godkänna eller avvisa.
3. Välj åtgärden **Godkänna**, **Avvisa**, eller **Delegera**.

När en post har godkänts eller har avvisats ändras godkännandestatus i fältet **Status** till **Godkänd** eller **Avvisad**.

Om en godkännarehierarki har ställts in är poststatusen **Väntar på godkännande** tills alla godkännare har godkänt transaktionen. Sedan ändras statusen till **Släppt**.

Samtidigt ändras godkännandestatus från **Skapad** till **Öppen** så snart som en godkännandebegäran skapas för posten. Om begäran avvisas, ändras godkännandestatus till **Avvisad**. Status står kvar som **Öppen** eller **Avvisad** tills alla godkännare har godkänt begäran.

## Delegera godkännandebegäranden

Efterföljande aktivitet utförs av en godkännaranvändare med behörigheten godkännare.

För att förhindra att poster staplas på hög eller blockerar arbetsflödet på något annat sätt kan godkännandeadministratören delegera en godkännandebegäran till en ersättare. Ersättaren kan vara antingen en utsedd ersättare, den direkta godkännaren eller godkännandeadministratören, i den prioritetsordningen. Du kan använda den här funktionen om en godkännare inte är tillgänglig för tillfället och inte kan godkänna begäranden före förfallodatumet.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **förfrågningar att godkänna** och välj sedan relaterad länk.
2. Markera en eller flera rader för godkännandebegäran som du vill delegera till en ersättande godkännare och välj sedan åtgärden **Delegera**.

Ett meddelande om att godkänna begäran skickas till den ersättande godkännaren.

## Hantera förfallna begäranden om godkännande

Efterföljande aktivitet utförs av en godkännaranvändare med behörigheten godkännare.

Med jämna mellanrum måste du påminna arbetsflödes användare om förfallna godkännande begäranden använder du funktionen **Skicka meddelanden om förfallna godkännanden**.

Med funktionen **Skicka meddelanden om förfallna godkännanden** görs en kontroll för att hitta alla förfallna öppna godkännandetransaktioner. Varje godkännare som har minst en förfallen godkännandetransaktion får meddelande med en lista över alla förfallna godkännandebegäranden. Meddelandet skickas också till deras godkännare och alla som begärt de förfallna godkännandena. Detta sista steg är praktiskt om den förfallna godkännandetransaktionen behöver delegeras till en ersättare.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Förfallna begäranden om godkännande** och välj sedan relaterad länk.
2. På sidan **Förfallna begäranden om godkännande** väljer du åtgärden **Skicka meddelanden om förfallna godkännanden**.

## Se relaterad [Microsoft utbildning](/training/modules/use-approval-workflows/)

## Se även

[Använda arbetsflöden för godkännande](across-use-workflows.md)  
[Arbetsflöde](across-workflow.md)  
[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)  
[Försäljning](sales-manage-sales.md)  
[Inkommande dokument](across-income-documents.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
