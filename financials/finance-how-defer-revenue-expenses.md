---
title: "Så här periodiserar du intäkter och kostnader | Microsoft Docs"
description: "Beskriver hur du känner igen intäkter eller kostnader i perioder utanför den period som transaktionen bokfördes genom att automatiskt periodisera intäkter och kostnader över ett angivet schema."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 03/24/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 5d7dbdc6001f221df0659d5aca1e5939398e3a31
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-defer-revenues-and-expenses"></a>Så här periodiserar du intäkter och kostnader
För att känna igen en intäkt eller kostnad i en period utanför den period som transaktionen bokfördes i, kan du använda funktioner för att automatiskt periodisera intäkter och kostnader över ett angivet schema.

Om du vill fördela kostnader eller intäkter i berörda bokföringsperioder kan du skapa en periodiseringsmall för resursen, artikeln eller redovisningskontot som kostnaden eller intäkten kommer att bokföras för. När du bokför relaterade försäljnings- eller inköpsdokument, periodiseras kostnaden eller intäkten till de relevanta bokföringsperioderna, enligt en periodiseringsschema som styrs av inställningarna i periodiseringsmallen och bokföringsdatumet.

**Obs!** den här funktionen kräver att din upplevelse är inställd på **Paket **. Mer information finns i avsnittet [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="to-set-up-a-gl-account-for-deferral"></a>Så här anger du ett redovisningskonto för periodisering
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Kontoplan**, och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten som behövs för att skapa ett redovisningskonto för periodiserade intäkter. Mer information finns i [Redovisning och kontoplan](finance-general-ledger.md).
4. Upprepa steg 2 och 3 för att skapa ett nytt redovisningskonto för periodiserade kostnader.

För båda typerna av periodisering väljer du **balansräkningen** i fältet **Typ** och namnger kontona på lämpligt sätt, till exempel ”förutbetald inkomst” för periodiserade intäkter och "obetalda kostnader" för periodiserade kostnader.

## <a name="to-set-up-a-deferral-template"></a>Så här skapar du en periodiseringsmall
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Periodiseringsmallar**, och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs.
4. I fältet **Beräkningsmetod** anger du hur fältet **Belopp** för varje period i fönstret **Periodiseringsschema** beräknas. Du kan välja mellan följande typer:

   * **Rak**: De periodiska periodiseringsbeloppen beräknas enligt antalet perioder som fördelas enligt periodlängd.
   * **Linjär**: De periodiska periodiseringsbeloppen beräknas enligt antalet perioder som fördelas jämt över perioder.
   * **Dagar per period**: De periodiska periodiseringsbeloppen beräknas enligt antalet dagar i perioden.
   * **Användardefinierad**: De periodiska periodiseringsbeloppen beräknas inte. Du måste manuellt fylla i fältet **Belopp** för varje period i fönstret Periodiseringsschema. För mer information, se avsnittet “Så här ändrar du ett uppskjutandeschema från en försäljningsfaktura”.
5. I fältet **Periodbesk.** anger du en beskrivning som visas i transaktioner för periodiseringsbokföringen. Du kan ange följande platshållarkoder för vanliga värden, som ska infogas automatiskt, när periodbeskrivningen visas.

   * %1 = Dagnumret för periodens bokföringsdatum
   * %2 = Veckonumret för periodens bokföringsdatum
   * %3 = Månadsnumret för periodens bokföringsdatum
   * %4 = Månadsnamnet för periodens bokföringsdatum
   * %5 = Bokföringsperiodnamnet för periodens bokföringsdatum
   * %6 = Räkenskapsåret för periodens bokföringsdatum

Exempel: bokföringsdatumet är 2016-02-06. Om du anger ”kostnader periodiserade för %4 %6" kommer beskrivningen som visas vara ”kostnader som periodiseras för februari 2016”.

## <a name="to-assign-a-deferral-template-to-an-item"></a>Så här tilldelar du en periodiseringsmall till en artikel
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Periodiseringsmallar**, och välj sedan relaterad länk.
2. Öppna kortet för den artikel som intäkter och kostnader måste periodiseras för till de bokföringsperioder när artikeln såldes eller köptes.
3. I fältet **Standardmall för periodisering** väljer du relevant periodiseringsmall.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>Så här ändrar du en periodiseringsmall från en försäljningsfaktura
**Obs!**: Stegen i den här proceduren är samma som när du ändrar ett periodiseringsschema för kostnader från en inköpsfaktura.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Försäljningsfakturor**, och välj sedan relaterad länk.
2. Skapa en försäljningsfaktura för en artikel som har tilldelats en periodiseringsmall. Mer information finns i [Så här fakturerar du försäljning](sales-how-invoice-sales.md).

    Observera att så snart du anger artikeln (eller resursen eller redovisningskontot) för fakturaraden kommer fältet **Periodiseringskod** att fyllas i med koden för den tilldelade periodiseringsmallen.
3. Välj åtgärden **periodiseringsmall**.
4. I fönstret **Periodiseringsschema** ändrar du inställningar i rubriken eller värden på raderna, till exempel för att periodisera beloppet till en ytterligare bokföringsperiod.
5. Välj åtgärden **Beräkna schema**.
6. Välj **OK**. Periodiseringsschemat uppdateras för försäljningsfakturan. Den relaterade periodiseringsmallen är oförändrad.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Om du vill förhandsgranska hur periodiserade intäkter eller kostnader ska bokföras i redovisningen
**Obs!**: Stegen i den proceduren är samma som när du granskar hur kostnadsperiodiseringar bokförs.

1. I fönstret **Försäljningsfaktura** väljer du åtgärden **Förhandsgranska bokföring**.
2. I fönstret **Förhandsgranska bokföring** väljer du åtgärden **Redovisningstransaktion** och sedan **Visa relaterade transaktioner**.

Redovisningstransaktioner som kommer att bokföras på det angivna periodiseringskontot, till exempel förutbetald inkomst, anges med beskrivningen som du angav i fältet **Periodbesk.** i periodiseringsmallen till exempel "kostnader som periodiseras för februari 2016 ".

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>Om du vill förhandsgranska bokförda periodiseringar i rapporten Periodiseringssammanfattning för försäljning
**Obs!**: Stegen i den proceduren är samma som när du granskar Periodiseringssammanfattning för försäljning.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Periodiseringssammanfattning för försäljning**, och välj sedan relaterad länk.
2. I fönstret **Periodiseringssammanfattning för försäljning** i fältet **Saldo fr.o.m.:** anger du datum fram till vilket du vill se periodiserade intäkter.
3. Klicka på **Förhandsgranska**.

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Så här arbetar du med redovisningsjournaler](ui-work-general-journals.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

