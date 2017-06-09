---
title: "Så här mappar du text på återkommande betalningar till konton för automatisk avstämning | Microsoft Docs"
description: "Så här mappar du text på återkommande betalningar till konton för automatisk avstämning"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7c6f79959027625a33961d42abe26514bc94e81e
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Så här mappar du text på återkommande betalningar till konton för automatisk avstämning
I fönstret **Mappa text till konto** som du öppnar från fönstret **Betalningsavstämningsjournal** kan du skapa mappningar mellan text på betalningar och specifika debet-, kredit- och balanskonton så att sådana betalningar bokförs på de angivna kontona när du bokför betalningar i betalningsavstämningsjournalen.

**Obs!** Ämnet gäller även när du använder funktionen **Mappa text till konto** från en inkommande dokumentpost för att hjälpa till att konvertera elektroniska dokument som tas emot från externa tjänster till dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information [Så här använder du OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md).   

Liknande funktioner finns för att stämma av överskottbelopp på Betalningsavstämningsjournaler på en ad hoc-basis. Mer information finns i [Så här stämmer du av betalningar som inte kan kopplas automatiskt](receivables-how-reconcile-payments-cannot-apply-auto.md).

Betalningar som bokförts baserat på text-till-konto-mappning kopplas inte till öppna transaktioner, utan bokförs bara på de angivna kontona utöver att skapa bankkontotransaktioner. Därför lämpar sig text-till-kontomappning för återkommande inbetalningar eller kostnader, till exempel frekventa inköp av bilbränsle eller bankavgifter och ränt, som visas regelbundet på bankutdraget och inte behöver ett relaterat affärsdokument. Mer information finns i avsnittet “Exempel - Text-till-konto-mappning för bränslekostnad” i den här artikeln.

**Obs!** Betalningar på avstämningsjournalrader anges endast för att bokföra enligt text-till-kontomappning om den automatiska kopplingsfunktionen bara kan ange matchningssäkerheten **Låg** eller **Medium**. Om funktionen för automatisk koppling ger matchningssäkerheten Hög kopplas betalningen automatiskt till en eller flera öppna transaktioner och betalningen bokförs inte på de konton som angetts i fönstret **Mappa text till konto**. Med andra ord åsidosätter en matchningssäkerhet på **Hög** en text-till-konto-mappning.

På en rad i en utbetalningsavstämningsjournal där betalningen har angetts för bokföring enligt text-till-kontomappning innehåller fältet **Matchningssäkerhet** innehåller **Hög – mappa text till konto** och **Kontotyp** och **Kontonr.** innehåller de tilldelade kontona.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Så här mappar du text på återkommande betalningar till konton för automatisk avstämning
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger du **Betalningsavstämningsjournaler** och väljer sedan relaterad länk.
2. Öppna en betalningsavstämningsjournal. Mer information finns i [Så här stämmer du av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).
3. Välj åtgärden **Mappa text till konto**. Fönstret **Mappa text till konto** öppnas.
4. I fältet **Mappningstext** anger du text som finns på betalningar som du vill bokföra på angivna konton utan koppling till en öppen transaktion. Du kan ange upp till 50 tecken.

    **Obs**: Om inga andra utbetalningar eller inkommande dokument finns med mappningstexten i fråga kommer Mappa text till konto att uppstå, även om endast en del av texten på utbetalningen eller det inkommande dokumentet finns som en mappningtext.
5. I fältet **Leverantörsnr.** anges leverantören som inkommande dokument som innehåller mappningstexten ska skapas för, eller som betalningar ska bokföras på. Mer information [Så här använder du OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md).      
6. I fältet **Debetkontonr.** anger du det konto som betalningar som innehåller mappningstexten ska bokföras till om de är inkommande betalningar i fältet . För inkommande betalningar är tecken på värdet i fältet **Transaktionsbelopp** positivt.
7. I fältet **Kreditkontonr.** anger du det konto som betalningar som innehåller mappningstexten ska bokföras till om de är utgående betalningar i fältet . För utgående betalningar är tecken på värdet i fältet **Transaktionsbelopp** negativt.
8. Ange om betalningen ska bokföras på ett redovisningskonto eller till ett kund- eller leverantörskonto i fältet **Ursprungstyp för motkonto**.
9. I fältet **Ursprungsnr för motkonto** anger du det konto som betalningen ska bokföras på, beroende på ditt val i fältet **Ursprungstyp för motkonto**.
10. Upprepa moment 4 till och med 8 för all text på betalningar som du vill mappa till konton för direkt bokföring utan koppling.

Nästa gång importerar en bankutdragsfil eller väljer funktionen **Koppla automatiskt** i fönstret **Betalningsavstämningsjournal** innehåller journalrader för betalningar som innehåller den angivna mappningstexten de mappade kontona i fälten **Kontotyp** och **Kontonr.**. . Fältet **Matchningssäkerhet** ska innehålla **Hög – mappa text till konto**. Det sker på villkoret att den automatiska kopplingsfunktionen endast kan tillhandahålla matchningssäkerheten **Låg** eller **Medium**.

## <a name="example-text-to-account-mapping-for-fuel-expense"></a>Exempel – Text-till-konto-mappning för bränslekostnad
Om du alltid vill bokföra bränslekostnader upplupna på Shell-bensinmackar i redovisningen för bensin (konto 8510) fyller du i en rad i fönstret **Mappa text till konto** så här.

| Mappningstext | Debetkonto Nr | Kreditkont Nr | Saldo Ursprungstyp | Saldo Ursprungsnr |
| --- | --- | --- | --- | --- |
| Gränssnitt |TOM |8510 |Redovisningskonto |TOM |

**Tips**: Mer information om hur du arbetar med fält och kolumner hittar du i [Arbeta med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md). För mer information om hur du hittar specifika sidor se [Sök](ui-search.md).

## <a name="see-also"></a>Se även
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Så här konfigurerar du tjänsten Envestnet Yodlee bankfeeder](bank-how-setup-bank-statement-service.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)]med tillägg](ui-extensions.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

