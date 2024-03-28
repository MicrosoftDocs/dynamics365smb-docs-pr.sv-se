---
title: Periodisera intäkter och kostnader
description: 'För att känna igen en intäkt eller kostnad i en period som transaktionen inte bokfördes i, kan du använda funktioner för att automatiskt periodisera eller skjuta upp dem över en angiven uppställning.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: postpone
ms.search.form: '1700, 1701, 1702, 1703, 1704, 1705, 1706, 1707'
ms.date: 12/06/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="defer-revenues-and-expenses"></a>Periodisera intäkter och kostnader

För att känna igen en intäkt eller kostnad i en period utanför den period som transaktionen bokfördes i, kan du använda funktioner för att automatiskt periodisera intäkter och kostnader över en angiven uppställning.

Om du vill fördela kostnader eller intäkter i berörda bokföringsperioder kan du skapa en periodiseringsmall för resursen, artikeln eller redovisningskontot som kostnaden eller intäkten kommer att bokföras för. När du bokför relaterade försäljnings- eller inköpsdokument, periodiseras kostnaden eller intäkten till de relevanta bokföringsperioderna, enligt en periodiseringsschema som styrs av inställningarna i periodiseringsmallen och bokföringsdatumet.

## <a name="to-set-up-a-gl-account-for-deferral"></a>Så här anger du ett redovisningskonto för periodisering

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten som behövs för att skapa ett redovisningskonto för periodiserade intäkter. Mer information finns i [Redovisning och kontoplan](finance-general-ledger.md).
4. Upprepa steg 2 och 3 för att skapa ett nytt redovisningskonto för periodiserade kostnader.

För båda typerna av periodisering väljer du **balansräkningen** i fältet **Typ** och namnger kontona på lämpligt sätt, till exempel ”förutbetald inkomst” för periodiserade intäkter och "obetalda kostnader" för periodiserade kostnader.

## <a name="to-set-up-a-deferral-template"></a>Så här skapar du en periodiseringsmall

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **periodiseringsmallar** och väljer sedan relaterad länk.
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
> Stegen i den här proceduren är desamma som när du tilldelar en periodiseringsmall till ett redovisningskonto eller en resurs.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artikel** och väljer sedan relaterad länk.
2. Öppna kortet för den artikel som intäkter och kostnader måste periodiseras för till de bokföringsperioder när artikeln såldes eller köptes.
3. I fältet **Standardmall för periodisering** väljer du relevant periodiseringsmall.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>Så här ändrar du en periodiseringsmall från en försäljningsfaktura

> [!NOTE]  
> Stegen i den här proceduren är samma som när du ändrar ett periodiseringsschema för kostnader från en inköpsfaktura.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsfakturor** och väljer sedan relaterad länk.
2. Skapa en försäljningsfaktura för en artikel som har tilldelats en periodiseringsmall. Mer information finns i [Så här fakturerar du försäljningsaktiviteter](sales-how-invoice-sales.md).

    Observera att så snart du anger artikeln (eller resursen eller redovisningskontot) för fakturaraden kommer fältet **Periodiseringskod** att fyllas i med koden för den tilldelade periodiseringsmallen.
3. Välj åtgärden **periodiseringsmall**.
4. På sidan **Periodiseringsschema** ändrar du inställningar i rubriken eller värden på raderna, till exempel för att periodisera beloppet till en ytterligare bokföringsperiod.
5. Välj åtgärden **Beräkna schema**.
6. Välj **OK**. Periodiseringsuppställningen uppdateras för försäljningsfakturan. Den relaterade periodiseringsmallen är oförändrad.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Om du vill förhandsgranska hur periodiserade intäkter eller kostnader ska bokföras i redovisningen

> [!NOTE]  
> Stegen i den proceduren är samma som när du granskar hur kostnadsperiodiseringar bokförs.

1. På sidan **Försäljningsfaktura** väljer du åtgärden **Förhandsgranska bokföring**.
2. På sidan **Förhandsgranska bokföring** väljer du åtgärden **Redovisningstransaktion** och sedan **Visa relaterade transaktioner**.

Redovisningstransaktioner som kommer att bokföras på det angivna periodiseringskontot, till exempel förutbetald inkomst, anges med beskrivningen som du angav i fältet **Periodbesk.** i periodiseringsmallen till exempel "kostnader som periodiseras för februari 2016 ".

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>Om du vill förhandsgranska bokförda periodiseringar i rapporten Periodiseringssammanfattning för försäljning

> [!NOTE]  
> Stegen i den proceduren är samma som när du granskar Periodiseringssammanfattning för försäljning.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Periodiseringssammanfattning** och väljer sedan relaterad länk.
2. På sidan **Periodiseringssammanfattning för försäljning** i fältet **Saldo fr.o.m.:** anger du datum fram till vilket du vill se periodiserade intäkter.
3. Klicka på **Förhandsgranska**.

## <a name="to-specify-a-period-in-which-to-allow-deferral-posting"></a>Så här anger du en period för att tillåta periodiseringsbokföring

Du kan ange en period då personer kan bokföra transaktioner genom att ange datum i fälten **Tillåt bokföring från** och **Tillåt bokföring till** på följande sätt:

* För alla användare på sidan **Redovisningsinställningar**
* För särskilda användare, på sidan **Användarinställningar**

Om du har gjort det måste du göra ett undantag för att tillåta dem att bokföras utanför perioden. Om du vill definiera perioden, följ dessa steg.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Redovisningsinställningar** eller **Användarinställningar** och välj sedan relaterad länk.
2. I fälten **Tillåt periodiseringsbokföring från** och **Tillåt periodiseringsbokföring till** anger du ett start- och slutdatum för perioden.

### <a name="video-guidance"></a>Videovägledning

Följande video visar hur du definierar den period under vilken du tillåter personer att bokföra uppskjutna intäkter och utgifter, och hur du anger undantag.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fG6C]

## <a name="see-also"></a>Se även

[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
