---
title: Ställa in mappning för text-till-konto för återkommande betalningar | Microsoft Docs
description: Länka text på betalningar med specifika konton så att betalningar bokförs på kontona när du bokför utbetalningsjournalen för avstämning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 225883d8b5d6c3d6fe327340d32ae4dbfd2a718b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392630"
---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Så här mappar du text på återkommande betalningar till konton för automatisk avstämning
På sidan **Mappa text till konto** som du öppnar från sidan **Betalningsavstämningsjournal** kan du skapa mappningar mellan text på betalningar och specifika debet-, kredit- och balanskonton så att sådana betalningar bokförs på de angivna kontona när du bokför betalningar i betalningsavstämningsjournalen.

Liknande funktioner finns för att stämma av överskottbelopp på Betalningsavstämningsjournaler på en ad hoc-basis. Mer information finns i [Så här stämmer du av betalningar som inte kan kopplas automatiskt](receivables-how-reconcile-payments-cannot-apply-auto.md).

Betalningar som bokförts baserat på text-till-konto-mappning kopplas inte till öppna transaktioner, utan bokförs bara på de angivna kontona utöver att skapa bankkontotransaktioner. Därför lämpar sig text-till-kontomappning för återkommande inbetalningar eller kostnader, till exempel frekventa inköp av bilbränsle eller bankavgifter och ränt, som visas regelbundet på bankutdraget och inte behöver ett relaterat affärsdokument. Mer information finns i avsnittet "Exempel – text-till-konto-mappning för bränsleutgifter" i det här ämnet.

> [!NOTE]  
>   Betalningar på avstämningsjournalrader anges endast för att bokföra enligt text-till-kontomappning om den automatiska kopplingsfunktionen bara kan ange matchningssäkerheten **Låg** eller **Medium**. Om funktionen för automatisk koppling ger matchningssäkerheten Hög kopplas betalningen automatiskt till en eller flera öppna transaktioner och betalningen bokförs inte på de konton som angetts på sidan **Mappa text till konto**. Med andra ord åsidosätter en matchningssäkerhet på **Hög** en text-till-konto-mappning.

På en rad i en utbetalningsavstämningsjournal där betalningen har angetts för bokföring enligt text-till-kontomappning innehåller fältet **Matchningssäkerhet** innehåller **Hög – mappa text till konto** och fälten **Kontotyp** och **Kontonr.** innehåller de mappade kontona.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Så här mappar du text på återkommande betalningar till konton för automatisk avstämning
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Betalningsavstämningsjournaler** och välj sedan tillhörande länk.
2. Öppna en betalningsavstämningsjournal. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).
3. Välj åtgärden **Mappa text till konto**. Sidan **Mappa text till konto** öppnas.
4. I fältet **Mappningstext** anger du text som finns på betalningar som du vill bokföra på angivna konton utan koppling till en öppen transaktion. Du kan ange upp till 50 tecken.

    > [!NOTE]  
    >   Om inga andra utbetalningar finns med mappningstexten i fråga kommer Mappa text till konto att uppstå, även om endast en del av texten på utbetalningen finns som en mappningtext.
5. På fältet **Leverantörsnr** anger du den leverantör som betalningar ska bokföras på.
6. Ange om betalningen ska bokföras på ett redovisningskonto eller till ett kund- eller leverantörskonto i fältet **Ursprungstyp för motkonto**.
7. På fältet **Ursprungsnr för motkonto** anger du det konto som betalningen ska bokföras på, beroende på ditt val i fältet **Ursprungstyp för motkonto**.

    > [!NOTE]
    > Använd inte fälten **Debetkontonr** och **Kreditkontonr** fält i samband med betalningsavstämning. De används endast för inkommande dokument. Mer information finns i [Använda OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md).

8. Upprepa moment 3 till och med 7 för all text på betalningar som du vill mappa till konton för direkt bokföring utan koppling.

Nästa gång importerar en bankutdragsfil eller väljer funktionen **Koppla automatiskt** på sidan **Betalningsavstämningsjournal** innehåller journalrader för betalningar som innehåller den angivna mappningstexten de mappade kontona i fälten **Kontotyp** och **Kontonr.**. Fältet **Matchningssäkerhet** ska innehålla **Hög – mappa text till konto**. Det sker på villkoret att den automatiska kopplingsfunktionen endast kan tillhandahålla matchningssäkerheten **Låg** eller **Medium**.

## <a name="example-text-to-account-mapping-for-bank-fees"></a>Exempel: Text-till-konto-mappning för bankavgifter

Fyll i en rad på sidan **Text-till-konto-mappning** enligt följande för att alltid bokföra utgifter som är kopplade till avgifter från en särskild bank, MyBank, i huvudbokskontot för bankavgifter (konto 60400).

| Mappningstext | Debetkontonr | Kreditkontonr | Ursprungstyp för motkonto | Ursprungsnr för motkonto |
| --- | --- | --- | --- | --- |
| MyBank |TOM |60400|Redovisningskonto |TOM |

## <a name="see-also"></a>Se även

[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Skapa tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]