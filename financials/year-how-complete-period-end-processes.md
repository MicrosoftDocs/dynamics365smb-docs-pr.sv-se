---
title: "Valfria aktiviteter för att avsluta perioder | Microsoft Docs"
description: "I det här avsnittet beskrivs de valfria processer och aktiviteter för att avsluta bokföringsperioder i Financials."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 678cebc065594ed0ed6fea897676f109ff2c1dce
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Översikt över uppgifter för att avsluta bokföringsperioder
[!INCLUDE[d365fin](includes/d365fin_md.md)] tvingar dig inte att avsluta perioder, men det finns många periodslutsaktiviteter (månadsslut) som du kan göra. I det här avsnittet ges en översikt över valfria processer och aktiviteter för att avsluta perioder.  

## <a name="general-ledger"></a>Redovisning
* Specificera intervall för bokföringsdatum som gäller hela systemet och är användarspecifik.  

    Detta anger datumen som bokföring kan göras i. Beroende på vilka behov som finns i ditt företag kanske du vill tillåta bokföring i början av perioden eller mot slutet. Mer information finns [Så här anger du bokföringsperioder](finance-how-specify-posting-periods.md).  
* Gör alla nödvändiga redovisningsjusteringar.  
* Uppdatera och bokför återkommande journaler.  
  <!--* Process Consolidations-->
* Kör kontouppställningar enligt följande:  
  * Öppna fönstret **Kontouppställning** och klicka på **Skriv ut**.  

## <a name="sales-and-receivables"></a>Försäljning
* Bokför alla försäljningsorder, fakturor, kreditnotor och returorder.  
* Bokför alla inbetalningsjournaler.  
* Uppdatera och bokför återkommande journaler som hör till försäljning- och kundreskontra.  
* Stäm av kundreskontra i redovisningen.  
* Kör batch-jobbet **Ta bort fakturerade förs.order**  

## <a name="purchases-and-payables"></a>Inköp
* Bokför alla inköps order, fakturor, kreditnotor och returorder.  
* Bokför alla betalningsjournaler.  
* Uppdatera och bokför återkommande journaler som relaterar till inköps- och leverantörsreskontra.  
* Kör rapporten **Lev.skulder - ålder** och stäm av leverantörsskulder i redovisningen.  
* Kör batch-jobbet **Ta bort fakturerade inköpsorder**  

<!-- ### Fixed Assets
* Post all maintenance costs have been posted through the fixed asset journals or invoices.
* Post adjustments.
* Post appreciation.
* Post depreciation.
* Update and post the recurring fixed asset journal.-->

<!--### Intercompany
* Process Intercompany Postings.-->

## <a name="calculate-and-process-sales-tax"></a>Beräkna och bearbeta Omsättningsskatt
* Fyll i skattmeddelanden.  

## <a name="see-also"></a>Se även
[Avsluta år och perioder](year-close-years-periods.md)  
[Avsluta böcker](year-close-books.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

