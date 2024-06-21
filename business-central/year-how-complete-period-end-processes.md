---
title: Valfria aktiviteter för att avsluta perioder
description: I det här avsnittet beskrivs de valfria processer och aktiviteter för att avsluta bokföringsperioder i Business Central.
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments'
ms.date: 08/29/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Översikt över uppgifter för att avsluta bokföringsperioder

[!INCLUDE[prod_short](includes/prod_short.md)] tvingar dig inte att avsluta perioder, men det finns många periodslutsaktiviteter (månadsslut) som du kan göra. I det här avsnittet ges en översikt över valfria processer och aktiviteter för att avsluta perioder.  

## Redovisning

* Specificera intervall för bokföringsdatum som gäller hela systemet och är användarspecifik.  

    Detta anger datumen som bokföring kan göras i. Beroende på vilka behov som finns i ditt företag kanske du vill tillåta bokföring i början av perioden eller mot slutet. Läs mer på [Ange bokföringsperioder](finance-how-specify-posting-periods.md).  
* Gör alla nödvändiga redovisningsjusteringar.  
* Uppdatera och bokför återkommande journaler.  
  <!--* Process Consolidations-->
* Gör ekonomiska rapporter så här:  
  * Öppna sidan **Ekonomiska rapporter** och välj åtgärden **Skriv ut**.  

## Försäljning

* Bokför alla försäljningsorder, fakturor, kreditnotor och returorder.  
* Bokför alla inbetalningsjournaler.  
* Uppdatera och bokför återkommande journaler som hör till försäljning.  
* Stäm av kundreskontra i redovisningen.  
* Kör batch-jobbet **Ta bort fakturerade förs.order**  

## Inköp

* Bokför alla inköps order, fakturor, kreditnotor och returorder.  
* Bokför alla betalningsjournaler.  
* Uppdatera och bokför återkommande journaler som relaterar till inköp.  
* Kör rapporten **Lev.skulder – ålder** och stäm av leverantörsskulder i redovisningen.  
* Kör batch-jobbet **Ta bort fakturerade inköpsorder**  

## Anläggningstillgångar

* Bokför alla underhållskostnader som har bokförts via anl.journaler eller fakturor.
* Bokföra justeringar.
* Bokföra uppskrivning
* Bokföra avskrivning
* Uppdatera och bokföra återkommande journal för anläggningstillgångar.

## Koncernintern

* Behandla koncerninterna transaktioner.

## Beräkna och bearbeta omsättningsskatt

* Fyll i skattmeddelanden.  

## Se även

[Avsluta år och perioder](year-close-years-periods.md)  
[Avsluta böcker](year-close-books.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
