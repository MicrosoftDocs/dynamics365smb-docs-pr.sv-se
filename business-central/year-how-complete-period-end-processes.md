---
title: Valfria aktiviteter för att avsluta perioder | Microsoft Docs
description: I det här avsnittet beskrivs de valfria processer och aktiviteter för att avsluta bokföringsperioder i Business Central.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 6f1bbed79a2f5d817e3f486cfb4207e5b285aef2
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775256"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Översikt över uppgifter för att avsluta bokföringsperioder
[!INCLUDE[prod_short](includes/prod_short.md)] tvingar dig inte att avsluta perioder, men det finns många periodslutsaktiviteter (månadsslut) som du kan göra. I det här avsnittet ges en översikt över valfria processer och aktiviteter för att avsluta perioder.  

## <a name="general-ledger"></a>Redovisning
* Specificera intervall för bokföringsdatum som gäller hela systemet och är användarspecifik.  

    Detta anger datumen som bokföring kan göras i. Beroende på vilka behov som finns i ditt företag kanske du vill tillåta bokföring i början av perioden eller mot slutet. Mer information finns [Så här anger du bokföringsperioder](finance-how-specify-posting-periods.md).  
* Gör alla nödvändiga redovisningsjusteringar.  
* Uppdatera och bokför återkommande journaler.  
  <!--* Process Consolidations-->
* Kör kontouppställningar enligt följande:  
  * Öppna sidan **Kontouppställning** och klicka på **Skriv ut**.  

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
* Kör rapporten **Lev.skulder – ålder** och stäm av leverantörsskulder i redovisningen.  
* Kör batch-jobbet **Ta bort fakturerade inköpsorder**  

Anläggningstillgångar
* Alla underhållskostnader har bokförts via anl.journaler eller fakturor
* Bokföra justeringar.
* Bokföra uppskrivning
* Bokföra avskrivning
* Uppdatera och bokföra återkommande journal för anläggningstillgångar.

Koncernintern
* Behandla koncerninterna transaktioner

## <a name="calculate-and-process-sales-tax"></a>Beräkna och bearbeta Omsättningsskatt
* Fyll i skattmeddelanden.  

## <a name="see-also"></a>Se även
[Avsluta år och perioder](year-close-years-periods.md)  
[Avsluta böcker](year-close-books.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]