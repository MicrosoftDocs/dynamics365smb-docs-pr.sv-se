---
title: "Använda en redovisningsjournal för att bokföra direkt i redovisningen | Microsoft Docs"
description: "Lär hur du använder Redovisningsjournaler för att bokföra ekonomiska transaktioner på redovisningskonton och andra konton, till exempel bank- och leverantörskonton."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b573bb55c29de329e5d9a804b49a91687dc369ff
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-general-journals"></a>Arbeta med redovisningsjournaler
De flesta finansiella transaktioner bokförs i redovisningen genom särskilda dokument, till exempel inköpsfakturor och försäljningsorder. För verksamhet som inte representeras av ett dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], till exempel mindre utgifter eller inbetalningar kan du skapa relaterade transaktioner genom att bokföra journalrader i fönstret **redovisningsjournal**. Mer information finns i [Så här bokför du transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md).

Du kan till exempel bokföra anställdas utgifter med egna pengar för affärsrelaterade utgifter för senare återbetalning. Mer information finns i [Så här registrerar du och återbetalar anställdas utgifter](finance-how-record-reimburse-employee-expenses.md).

Du använder Redovisningsjournaler för att bokföra ekonomiska transaktioner direkt på redovisningskonton och andra konton, till exempel bank-, leverantörs- och personalkonton. När du bokför med en redovisningsjournal skapas alltid transaktioner på redovisningskonton. Så sker till exempel även när en journalrad bokförs på ett kundkonto, eftersom en transaktion bokförs på ett kundfordringskonto i redovisningen via en bokföringsmall.

Den information som du anger i en journal är tillfällig och kan ändras så länge den finns i journalen. När du bokför journalen, överförs informationen till transaktioner på enskilda konton, där den inte kan ändras. Du kan emellertid ta bort kopplingar från bokförda transaktioner och bokföra återförande eller rättande transaktioner. Mer information finns i [Så hör: Återföra bokföringar](finance-how-reverse-journal-posting.md).

## <a name="using-journal-templates-and-batches"></a>Använda Journalmallar och journaler
Det finns flera redovisningsjournalmallar. Varje journalmall representeras av ett dedikerat fönster med särskilda funktioner och fälten som krävs för att stödja dessa funktioner, till exempel fönstret **Betalningsavstämningsjournal** för att bearbeta bankbetalningar och fönstret **Betalningsjournal** för att betala dina leverantörer eller återbetala dina anställda. Mer information finns i [göra betalningar](payables-make-payments.md) och [så här: stämma av kundens betalningar manuellt ](receivables-how-apply-sales-transactions-manually.md).

För varje journalmall kan du skapa din egen personliga journal som en journal. Du kan till exempel ange din egen journal för betalningsjournalen som har din personliga layout och inställningar. Följande tips är ett exempel på hur du anpassar en journal.

> [!TIP]  
> Om du väljer kryssrutan **Föreslå saldobelopp** på raden för din journal i fönstret **Redovisningsjournaler** kommer fältet **Belopp** till exempel, redovisningsjournalrader för samma verifikationsnummer automatiskt att fyllas i med värdet som krävs för att hantera dokumentet. Mer information finns i [Låta [!INCLUDE[d365fin](includes/d365fin_md.md)] föreslå värden](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Förstå Huvudkonton och motkonton
Om du har skapat standardmotkonton för journalerna på sidan **Redovisningsjournaler** fylls motkontot i automatiskt när du fyller i fältet **Kontonr**. Annars fyller du i både fältet **Kontonr** och fältet **Motkonto** manuellt. Ett positivt belopp i fältet **Belopp** debiteras på huvudkontot och krediteras på motkontot. Ett negativt belopp krediteras på huvudkontot och debiteras på motkontot.

> [!NOTE]  
>   Moms beräknas separat för huvudkontot och motkontot, så att olika momssatser kan användas för dem.

## <a name="working-with-recurring-journals"></a>Arbeta med Återkommande journaler
En återkommande journal är en redovisningsjournal med särskilda fält för hantering av transaktioner som du ofta bokför med få eller inga ändringar. Med fälten för återkommande transaktioner kan du bokföra både fasta och rörliga belopp. Du kan även ange automatiska återföringsposter dagen efter bokföringsdatumet och använda fördelningsnycklar med de återkommande transaktionerna.

## <a name="working-with-standard-journals"></a>Arbeta med Standardjournaler
När du har skapat journalrader som du vet att du förmodligen kommer att skapa igen, kan du spara dem som en standardjournal innan du bokför journalen. Den här funktionen gäller artikeljournaler och redovisningsjournaler.

> [!NOTE]  
>   Följande procedur gäller för artikeljournalen, men informationen kan också tillämpas på redovisningsjournalen.

### <a name="to-save-a-standard-journal"></a>Så här sparar du som en standardjournal
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artikeljournaler** och välj sedan relaterad länk.
2. Mata på en eller flera journalrader.
3. Markera de journalrader som du vill återanvända.
4. Välj åtgärden **Spara som standardjournal**.
5. I fönstret **Spara som standardartikeljournal** måste du definiera en ny eller befintlig standardartikeljournal som raderna ska sparas i:

    Om du redan har skapat en eller flera standardartikeljournaler och du vill ersätta någon av dessa med den nya uppsättningen artikeljournalrader, i fältet Kod och välja koden.
6. Välj knappen **OK** för att bekräfta att du vill skriva över den befintliga standardartikeljournalen och byta ut allt innehåll.
7. Välj fältet **Spara a-pris**, om du vill spara värdena i fältet **A-pris** i standardartikeljournalen.
8. Välj fältet **Spara antal**, om du vill att programmet ska spara värdena i fältet **Antal**.
9. Välj knappen **OK** för att spara standardartikeljournalen.

När du har sparat standardartikeljournalen visas fönstret Artikeljournal så att du kan fortsätta att bokföra den, samtidigt som du vet att den lätt kan återskapas nästa gång du bokför samma eller likartade rader.

### <a name="to-reuse-a-standard-journal"></a>Så här återanvänder du standardjournaler
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artikeljournaler** och välj sedan relaterad länk.
2. Välj åtgärden **Få standardjournal**.

    Fönstret Standardartikeljournaler visas med koder och beskrivningar för alla befintliga standardartikeljournaler.
3. Om du vill förhandsgranska en standardartikeljournal innan du väljer att återanvända den, klickar du på **Visa journal**.

    Alla ändringar som du gör i en standardartikeljournal införs omedelbart. De finns där nästa gång du öppnar eller återanvänder standardartikeljournalen i fråga. Du bör därför vara säker på att ändringen är tillräckligt viktig för att tillämpa allmänt. Annars skapar du den specifika ändringen i artikeljournalen efter att standardartikeljournalraderna har infogats. Se punkt 4 nedan.
4. När du kommer tillbaka till fönstret **Standardartikeljournaler** väljer du den standardartikeljournal som du vill återanvända och klickar på **OK**.

    Nu är artikeljournalen ifylld med raderna som du har sparat som standardartikeljournal. Om det redan finns journalrader i artikeljournalen, placeras de infogade raderna under de befintliga journalraderna.

    Om du inte markerar fältet **Spara a-pris** under när du använde funktionsjobbet **Spara som standardartikeljournal** innebär detta att fältet **A-pris** på raderna som infogas från standardjournalen  automatiskt kommer att fyllas med artikelns aktuella värde (kopieras från fältet **Styckkostnad** på artikelkortet).

    > [!NOTE]  
>   Om du har markerat fältet **Spara a-pris** eller **Spara antal** ska du nu kontrollera att de infogade värdena är korrekta för den här speciella lagerjusteringen innan du bokför artikeljournalen.

    Om de infogade artikeljournalraderna innehåller sparade a-priser som du inte vill bokföra, kan du snabbt justera dem till artikelns aktuella värde:

6. Välj de artikeljournalrader som du vill justera lagret för och välj sedan åtgärden **Omberäkna a-pris**. Då uppdateras fältet A-pris med artikelns aktuella styckkostnad.
7. Välj åtgärden **Bokföra**.

## <a name="to-renumber-document-numbers-in-journals"></a>Numrera om verifikationsnummer i journaler
Du kan använda funktionen **Numrera om nummer** innan du bokför en journal, för att kontrollera att du inte får bokföringsfel p.g.a. dokumentets nummerordning.

I alla journaler som är baserade på redovisningsjournalen är fältet **Dokumentnr** redigerbart så att du kan ange olika nummer för olika journalrader eller samma verifikationsnummer för relaterade journalrader.

Om fältet **Nr-serie** på journalen fylls, kräver bokföringsfunktionen i redovisningsjournaler att verifikationsnumret på enstaka eller grupperade journalrader är i ordningsföljd. Du kan använda funktionen **Numrera om nummer** innan du bokför journalen, för att kontrollera att du inte får bokföringsfel p.g.a. dokumentets nummerordning. Om relaterade rader grupperades efter verifikationsnummer innan du använde funktionen, förblir de grupperade men kan tilldelas ett annat verifikationsnummer.

Den här funktionen fungerar även på filtrerade vyer.

Alla omnumreringen av verifikationsnummer skall respektera relaterade tillämpningar, som en ansökan om betalningstillämpning som har gjorts från dokumentet på journalraden till ett leverantörskonto. I enlighet med detta kan fälten **Koppla till ID** och **Koppla till ver.nr.** i de berörda transaktionerna uppdateras.

Följande procedur är baserad på fönstret **Redovisningsjournal**, men gäller för alla andra journaler som baseras på den redovisningsjournalen, t.ex. fönstret **Utbetalningsjournal**.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler** och välj sedan relaterad länk.
2. När du är klar att bokföra journalraderna väljer du **Numrera om dokumentnummer**.

Värden i fältet **Dokumentnr** ändras, om så krävs, så att verifikationsnumret på enstaka eller grupperade journalrader är i ordningsföljd. När dokument numreras kan du fortsätta att bokföra journalen.

## <a name="see-also"></a>Se även
[Så här bokför du transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md)  
[Så här: Återföra en bokning](finance-how-reverse-journal-posting.md)  
[Så här: Fördela kostnader och intäkter.](year-allocate-costs-income.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

