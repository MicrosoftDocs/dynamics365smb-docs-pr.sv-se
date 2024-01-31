---
title: Avsluta resultatkonton
description: Vid årsslut måste du köra batch-jobbet Avslut av resultatkonton för att avsluta bokföringsperioder som utgör räkenskapsåret.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.date: 06/25/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Avsluta resultatkonton
När ett räkenskapsår är slut måste du avsluta perioderna som året omfattar. Använd batch-jobbet **Avslut av resultatkonton** för detta ändamål. Detta jobb överför årets resultat till ett konto i balansräkningen och avslutar resultatkonton. Du gör detta genom att skapa rader i en journal, som du sedan kan bokföra.

## För att använda batch-jobbet Avslut av resultatkonton
1. Avsluta räkenskapsår. Räkenskapsåret måste vara avslutat innan batch-jobbet kan köras. Mer information finns i [Så här avslutar du bokföringsperioder](year-close-account-periods.md).
2. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Avsluta resultaträkning** och väljer sedan relaterad länk.
3. Klicka på **OK** för att köra batchjobbet.

## Om batch-jobbet Avslut av resultatkonton
Batchjobbet bearbetar alla redovisningskonton av typen resultaträkning och skapar transaktioner som upphäver respektive saldo. Varje transaktion är summan av alla redovisningstransaktioner på kontot i räkenskapsåret. Dessa nya transaktioner placeras i en journal där du måste specificera ett motkonto och ett konto för balanserad vinst eller förlust i balansräkningen innan du bokför. När du bokför journalen bokförs en transaktion på varje resultatkonto så att saldot blir noll och samtidigt överförs årets resultat till balansräkningen.

Du måste själv bokföra journalen. Transaktionerna bokförs inte automatiskt med batchjobbet utom när en alternativ rapporteringsvaluta används. När en alternativ rapporteringsvaluta används bokförs transaktionerna direkt i redovisningen.

Datumet på raderna, som batch-jobbet skriver in i journalen, kommer alltid att vara årets avslutsdatum. Avslutsdatumet är ett fiktivt datum mellan den sista dagen i räkenskapsåret och den första dagen i följande räkenskapsår. Fördelen med att bokföra på ett avslutsdatum är att du behåller rätta saldon på räkenskapsårets vanliga datum.

Batch-jobbet **Avslut av resultatkonton** kan användas upprepade gånger. Du kan bokföra på föregående räkenskapsår även efter det att resultatkontona har avslutats, om du kör batch-jobbet igen.

## Se även

[Avsluta böcker](year-close-books.md)  
[Bokför årsslutstransaktionen](year-how-post-year-end-close-entry.md)  
[Arbeta med bokföringsperioder och räkenskapsår](finance-accounting-periods-and-fiscal-years.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]