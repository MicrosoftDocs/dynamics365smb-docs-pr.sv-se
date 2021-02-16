---
title: Periodisera intäkter och kostnader | Microsoft Docs
description: För att känna igen en intäkt eller kostnad i en period utanför den period som transaktionen bokfördes i, kan du använda funktioner för att automatiskt periodisera eller skjuta upp dem över ett angivet schema.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b9d936cffabaea38571fe755ca43ed0cd9a961b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750886"
---
# <a name="defer-revenues-and-expenses"></a>Periodisera intäkter och kostnader
För att känna igen en intäkt eller kostnad i en period utanför den period som transaktionen bokfördes i, kan du använda funktioner för att automatiskt periodisera intäkter och kostnader över ett angivet schema.

Om du vill fördela kostnader eller intäkter i berörda bokföringsperioder kan du skapa en periodiseringsmall för resursen, artikeln eller redovisningskontot som kostnaden eller intäkten kommer att bokföras för. När du bokför relaterade försäljnings- eller inköpsdokument, periodiseras kostnaden eller intäkten till de relevanta bokföringsperioderna, enligt en periodiseringsschema som styrs av inställningarna i periodiseringsmallen och bokföringsdatumet.

## <a name="to-set-up-a-gl-account-for-deferral"></a>Så här anger du ett redovisningskonto för periodisering
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kontoplan** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten som behövs för att skapa ett redovisningskonto för periodiserade intäkter. Mer information finns i [Redovisning och kontoplan](finance-general-ledger.md).
4. Upprepa steg 2 och 3 för att skapa ett nytt redovisningskonto för periodiserade kostnader.

För båda typerna av periodisering väljer du **balansräkningen** i fältet **Typ** och namnger kontona på lämpligt sätt, till exempel ”förutbetald inkomst” för periodiserade intäkter och "obetalda kostnader" för periodiserade kostnader.

## <a name="to-set-up-a-deferral-template"></a>Så här skapar du en periodiseringsmall
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Periodiseringsmallar** och välj sedan tillhörande länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs.
4. I fältet **Beräkningsmetod** anger du hur fältet **Belopp** för varje period på sidan **Periodiseringsschema** beräknas. Du kan välja mellan följande typer:

   * **Rak**: De periodiska periodiseringsbeloppen beräknas enligt antalet perioder som fördelas enligt periodlängd.
   * **Linjär**: De periodiska periodiseringsbeloppen beräknas enligt antalet perioder som fördelas jämt över perioder.
   * **Dagar per period**: De periodiska periodiseringsbeloppen beräknas enligt antalet dagar i perioden.
   * **Användardefinierad**: De periodiska periodiseringsbeloppen beräknas inte. Du måste manuellt fylla i fältet **Belopp** för varje period på sidan Periodiseringsschema. För mer information, se avsnittet “Så här ändrar du ett uppskjutandeschema från en försäljningsfaktura”.
5. I fältet **Periodbesk.** anger du en beskrivning som visas i transaktioner för periodiseringsbokföringen. Du kan ange följande platshållarkoder för vanliga värden, som ska infogas automatiskt, när periodbeskrivningen visas.

   * %1 = Dagnumret för periodens bokföringsdatum
   * %2 = Veckonumret för periodens bokföringsdatum
   * %3 = Månadsnumret för periodens bokföringsdatum
   * %4 = Månadsnamnet för periodens bokföringsdatum
   * %5 = Bokföringsperiodnamnet för periodens bokföringsdatum
   * %6 = Räkenskapsåret för periodens bokföringsdatum

Exempel: bokföringsdatumet är 2016-02-06. Om du anger ”kostnader periodiserade för %4%6" kommer beskrivningen som visas vara ”kostnader som periodiseras för februari 2016”.

## <a name="to-assign-a-deferral-template-to-an-item"></a>Så här tilldelar du en periodiseringsmall till en artikel
> [!NOTE]  
>   Stegen i den här proceduren är desamma som när du tilldelar en periodiseringsmall till ett redovisningskonto eller en resurs.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artikel** och välj sedan tillhörande länk.
2. Öppna kortet för den artikel som intäkter och kostnader måste periodiseras för till de bokföringsperioder när artikeln såldes eller köptes.
3. I fältet **Standardmall för periodisering** väljer du relevant periodiseringsmall.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>Så här ändrar du en periodiseringsmall från en försäljningsfaktura
> [!NOTE]  
>   Stegen i den här proceduren är samma som när du ändrar ett periodiseringsschema för kostnader från en inköpsfaktura.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsfakturor** och välj sedan relaterad länk.
2. Skapa en försäljningsfaktura för en artikel som har tilldelats en periodiseringsmall. Mer information finns i [Så här fakturerar du försäljningsaktiviteter](sales-how-invoice-sales.md).

    Observera att så snart du anger artikeln (eller resursen eller redovisningskontot) för fakturaraden kommer fältet **Periodiseringskod** att fyllas i med koden för den tilldelade periodiseringsmallen.
3. Välj åtgärden **periodiseringsmall**.
4. På sidan **Periodiseringsschema** ändrar du inställningar i rubriken eller värden på raderna, till exempel för att periodisera beloppet till en ytterligare bokföringsperiod.
5. Välj åtgärden **Beräkna schema**.
6. Välj **OK**. Periodiseringsschemat uppdateras för försäljningsfakturan. Den relaterade periodiseringsmallen är oförändrad.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Om du vill förhandsgranska hur periodiserade intäkter eller kostnader ska bokföras i redovisningen
> [!NOTE]  
>   Stegen i den proceduren är samma som när du granskar hur kostnadsperiodiseringar bokförs.

1. På sidan **Försäljningsfaktura** väljer du åtgärden **Förhandsgranska bokföring**.
2. På sidan **Förhandsgranska bokföring** väljer du åtgärden **Redovisningstransaktion** och sedan **Visa relaterade transaktioner**.

Redovisningstransaktioner som kommer att bokföras på det angivna periodiseringskontot, till exempel förutbetald inkomst, anges med beskrivningen som du angav i fältet **Periodbesk.** i periodiseringsmallen till exempel "kostnader som periodiseras för februari 2016 ".

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>Om du vill förhandsgranska bokförda periodiseringar i rapporten Periodiseringssammanfattning för försäljning
> [!NOTE]  
>   Stegen i den proceduren är samma som när du granskar Periodiseringssammanfattning för försäljning.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Periodiseringssammanfattning för försäljning** och välj sedan tillhörande länk.
2. På sidan **Periodiseringssammanfattning för försäljning** i fältet **Saldo fr.o.m.:** anger du datum fram till vilket du vill se periodiserade intäkter.
3. Klicka på **Förhandsgranska**.

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
