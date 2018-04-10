---
title: "Ställa in mappning för text-till-konto för återkommande betalningar | Microsoft Docs"
description: "Länka text på betalningar med specifika konton så att betalningar bokförs på kontona när du bokför utbetalningsjournalen för avstämning."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 3a7b7d9921c1cdc4a0024a3ee8208798d00e0701
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Så här mappar du text på återkommande betalningar till konton för automatisk avstämning
I fönstret **Mappa text till konto** som du öppnar från fönstret **Betalningsavstämningsjournal** kan du skapa mappningar mellan text på betalningar och specifika debet-, kredit- och balanskonton så att sådana betalningar bokförs på de angivna kontona när du bokför betalningar i betalningsavstämningsjournalen.

Liknande funktioner finns för att stämma av överskottbelopp på Betalningsavstämningsjournaler på en ad hoc-basis. Mer information finns i [Så här stämmer du av betalningar som inte kan kopplas automatiskt](receivables-how-reconcile-payments-cannot-apply-auto.md).

Betalningar som bokförts baserat på text-till-konto-mappning kopplas inte till öppna transaktioner, utan bokförs bara på de angivna kontona utöver att skapa bankkontotransaktioner. Därför lämpar sig text-till-kontomappning för återkommande inbetalningar eller kostnader, till exempel frekventa inköp av bilbränsle eller bankavgifter och ränt, som visas regelbundet på bankutdraget och inte behöver ett relaterat affärsdokument. Mer information finns i avsnittet “Exempel - Text-till-konto-mappning för bränslekostnad” i den här artikeln.

> [!NOTE]  
>   Betalningar på avstämningsjournalrader anges endast för att bokföra enligt text-till-kontomappning om den automatiska kopplingsfunktionen bara kan ange matchningssäkerheten **Låg** eller **Medium**. Om funktionen för automatisk koppling ger matchningssäkerheten Hög kopplas betalningen automatiskt till en eller flera öppna transaktioner och betalningen bokförs inte på de konton som angetts i fönstret **Mappa text till konto**. Med andra ord åsidosätter en matchningssäkerhet på **Hög** en text-till-konto-mappning.

På en rad i en utbetalningsavstämningsjournal där betalningen har angetts för bokföring enligt text-till-kontomappning innehåller fältet **Matchningssäkerhet** innehåller **Hög – mappa text till konto** och fälten **Kontotyp** och **Kontonr.** innehåller de mappade kontona.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Så här mappar du text på återkommande betalningar till konton för automatisk avstämning
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Betalningsavstämningsjournaler** och välj sedan relaterad länk.
2. Öppna en betalningsavstämningsjournal. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).
3. Välj åtgärden **Mappa text till konto**. Fönstret **Mappa text till konto** öppnas.
4. I fältet **Mappningstext** anger du text som finns på betalningar som du vill bokföra på angivna konton utan koppling till en öppen transaktion. Du kan ange upp till 50 tecken.

    > [!NOTE]  
    >   Om inga andra utbetalningar finns med mappningstexten i fråga kommer Mappa text till konto att uppstå, även om endast en del av texten på utbetalningen finns som en mappningtext.
5. På fältet **Leverantörsnr** anger du den leverantör som betalningar ska bokföras på.
6. Ange om betalningen ska bokföras på ett redovisningskonto eller till ett kund- eller leverantörskonto i fältet **Ursprungstyp för motkonto**.
7. På fältet **Ursprungsnr för motkonto** anger du det konto som betalningen ska bokföras på, beroende på ditt val i fältet **Ursprungstyp för motkonto**.

    > [!NOTE]
    > Använd inte fälten **Debetkontonr** och **Kreditkontonr** fält i samband med betalningsavstämning. De används endast för inkommande dokument. Mer information finns i [Använda OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md).

8. Upprepa moment 3 till och med 7 för all text på betalningar som du vill mappa till konton för direkt bokföring utan koppling.

Nästa gång importerar en bankutdragsfil eller väljer funktionen **Koppla automatiskt** i fönstret **Betalningsavstämningsjournal** innehåller journalrader för betalningar som innehåller den angivna mappningstexten de mappade kontona i fälten **Kontotyp** och **Kontonr.**. Fältet **Matchningssäkerhet** ska innehålla **Hög – mappa text till konto**. Det sker på villkoret att den automatiska kopplingsfunktionen endast kan tillhandahålla matchningssäkerheten **Låg** eller **Medium**.

## <a name="example-text-to-account-mapping-for-fuel-expense"></a>Exempel – Text-till-konto-mappning för bränslekostnad
Om du alltid vill bokföra bränslekostnader upplupna på Shell-bensinmackar i redovisningen för bensin (konto 8510) fyller du i en rad i fönstret **Mappa text till konto** så här.

| Mappningstext | Debetkontonr | Kreditkontonr | Ursprungstyp för motkonto | Ursprungsnr för motkonto |
| --- | --- | --- | --- | --- |
| Gränssnitt |TOM |8510 |Redovisningskonto |TOM |

> [!TIP]  
>   Mer information om hur du arbetar med fält och kolumner hittar du i [Arbeta med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md). För mer information om hur du hittar specifika sidor se [Sök](ui-search.md).

## <a name="see-also"></a>Se även
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Konfigurera bankfeedtjänsten Envestnet Yodlee](bank-how-setup-bank-statement-service.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

