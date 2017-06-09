---
title: Arbeta med redovisningsjournaler | Microsoft Docs
description: "Så här fungerar du med redovisningsjournaler"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/03/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 13257a5d82d742d92fb22da9da7ff7f773d7d2f8
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="working-with-general-journals"></a>Arbeta med redovisningsjournaler
Du använder Redovisningsjournaler för att bokföra ekonomiska transaktioner på redovisningskonton och andra konton, till exempel bank-, kund-, leverantörskonton. När du bokför med en redovisningsjournal skapas alltid transaktioner på redovisningskonton. Så sker till exempel även när en journalrad bokförs på ett kundkonto, eftersom en transaktion bokförs på ett kundfordringskonto i redovisningen via en bokföringsmall.

[!INCLUDE[d365fin](includes/d365fin_md.md)] har även icke-finansiella journaler, till exempel artikeljournal och inventeringjournal, men dessa kan inte visas i användargränssnittet.

Den information som du anger i en journal är tillfällig och kan ändras så länge den finns i journalen. När du bokför journalen, överförs informationen till transaktioner på enskilda konton, där den inte kan ändras. Du kan emellertid ta bort kopplingar från bokförda transaktioner och bokföra återförande eller rättande transaktioner.

## <a name="journal-templates-and-batches"></a>Journalmallar och journaler
Det finns flera redovisningsjournalmallar. Varje journalmall representeras av ett dedikerat fönster med särskilda funktioner och fälten som krävs för att stödja dessa funktioner, till exempel fönstret **Betalningsavstämningsjournal** för att bearbeta bankbetalningar och fönstret **Betalningsjournal** för att betala dina leverantörer.

**Observera**: Om du exporterar betalningsfiler till din bank från utbetalningsjournalen kan du välja kryssrutan **Tillåt betalningsexport** för journalen i fråga i fönstret **redovisningsjournaler**. Mer information finns i [Så här exporterar du betalningar till en bankfil](payables-how-export-payments-bank-file.md).

För varje journalmall kan du skapa din egen personliga journal som en journal. Du kan till exempel ange din egen journal för betalningsjournalen som har din personliga layout och inställningar.

Ett exempel på en personlig inställning, som du kan definiera på din redovisningsjournal är att låta systemet hjälpa dig att fylla i beloppfält. Om du väljer kryssrutan **Föreslå saldobelopp** på raden för din journal i fönstret **Redovisningsjournaler** kommer fältet **Belopp** till exempel, redovisningsjournalrader för samma verifikationsnummer automatiskt att fyllas i med värdet som krävs för att hantera dokumentet. Mer information finns i avsnittet [Låta [!INCLUDE[d365fin](includes/d365fin_md.md)]föreslå värden](ui-let-system-suggest-values.md).

## <a name="main-accounts-and-balancing-accounts"></a>Huvudkonton och motkonton
Om du har skapat standardmotkonton för journalerna fylls motkontot i automatiskt när du fyller i fältet **Kontonr**. . Annars måste du fylla i både **Kontonr.** och **Motkonto** manuellt. Ett positivt belopp i fältet **Belopp** debiteras på huvudkontot och krediteras på motkontot. Ett negativt belopp krediteras på huvudkontot och debiteras på motkontot.

**Obs!** Moms beräknas separat för huvudkontot och motkontot, så att olika momssatser kan användas för dem.

## <a name="recurring-journals"></a>Återkommande journaler
En återkommande journal är en redovisningsjournal med särskilda fält för hantering av transaktioner som du ofta bokför med få eller inga ändringar. Med fälten för återkommande transaktioner kan du bokföra både fasta och rörliga belopp. Du kan även ange automatiska återföringsposter dagen efter bokföringsdatumet och använda fördelningsnycklar med de återkommande transaktionerna.

## <a name="see-also"></a>Se även
[Så här använder du fördelningsnycklar i redovisningsjournaler](ui-how-use-allocation-keys-general-journals.md)  
[Ekonomi](finance.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

