---
title: Analysera data efter dimensioner
description: I den här artikeln beskrivs hur du kan analysera affärsdata efter dimensioner för att få bättre insikt i verksamheten.
author: edupont
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: edupont
---
# <a name="analyze-data-by-dimensions" />Analysera data efter dimensioner

Inom ekonomisk analys är en dimension data som du lägger till en transaktion som en sorts markör. Dessa data används för att gruppera transaktioner med liknande egenskaper, till exempel kunder, regioner, produkter och säljare, och enkelt hämta dessa grupper för analys. Dimensioner kan användas på transaktioner i journaler, dokument och budgetar. 

Varje "dimension" används för att beskriva analysens fokus. Så till exempel en tvådimensionell analys är försäljning per område. Om du använder fler än två dimensioner när du skapar en transaktion kan du utföra mer komplexa analyser, exempelvis försäljning per försäljningskampanj per kundgrupp per område. Det ger dig bättre inblick i din verksamhet, till exempel hur väl verksamheten fungerar, inom vilka områden det går riktigt bra och inom vilka det går sämre samt var det krävs mer resurser, så att du kan fatta välgrundade beslut som tar verksamheten framåt. Mer information: [Arbeta med dimensioner](finance-dimensions.md).

> [!TIP]
> Som ett snabbt sätt att analysera transaktionsdata efter dimensioner kan du filtrera summorna i kontoplanen och posterna på alla sidor för **Transaktioner** per dimension. Sök efter åtgärden **Ange dimensionsfilter**.

> [!NOTE]
> Om du upptäcker att ett felaktigt dimensionsvärde har använts på bokförda redovisningstransaktioner kan du korrigera det och uppdatera analysvyerna. Läs mer i avsnittet [Felsöka och korrigera dimensioner](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="set-up-an-analysis-view" />Definiera en analysvy

En analys per dimension använder en vald kombination av dimensioner. Du kan lagra, hämta och uppdatera dimensionsuppsättningen genom att skapa ett **analysvykort**. 

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Analysvyer** och väljer sedan relaterad länk.  
2. På sidan **Analysvylista** väljer du åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Om du vill lägga till ytterligare dimensionskoder förutom de fyra koderna väljer du på snabbfliken **Dimensioner**, åtgärden **Filter**, fyller i fälten och klickar på **OK**.  
5. Om du vill uppdatera vyn, väljer du åtgärden **uppdatera**.

## <a name="analyze-by-dimensions" />Analysera efter dimensioner

Använd analysvyer som du redan har konfigurerat med matrisen **Analys per dimension** för att visa beloppen i redovisningen.   

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Analysvyer** och väljer sedan relaterad länk.  
2. Välj lämplig analysvy och välj åtgärden **Analys per dimension**.
3. Högst upp på sidan **Analys efter dimensioner** fyller du i fälten för att definiera vilka data som ska visas och hur.
4. Välj åtgärden **Visa matris** för att öppna respektive matrissida för den definierade analysvyn.
5. Om du vill visa en specifikation av ett belopp som visas på matrissidan väljer du beloppet för att granska dem i detalj.  

- Kolumnen till vänster innehåller information baserad på vad du valt i fältet **Visa som rader** i huvudet.  
- Kolumnen till höger innehåller information baserad på vad du valt i fältet **Visa som kolumner** i huvudet.

> [!IMPORTANT]  
> Du kan inte välja en period som är kortare än perioden som angetts för datumkomprimeringen på **Analysvy**-kortet. Kommandona **Nästa uppsättning** och **Föregående uppsättning** är inaktiva om du har valt **Period** i något av fälten **Visa som rader** eller **Visa som kolumner**.  

> [!NOTE]  
> Du kan använda rapporten **Dimensioner – detaljerad** om du vill visa en detaljerad klassificering av hur dimensionerna har använts på transaktioner under en vald period. Du använder rapporten **Dimensioner – total** om du bara vill visa totalbeloppen.  

> [!TIP]  
> Du kan också ändra vyn genom att ändra innehållet i fälten **Visa som rader** och **Visa som kolumner**. Om du vill ändra vyinställningen, väljer du åtgärden **Byt plats på rader och kolumner**.

## <a name="update-an-analysis-view" />Uppdatera en analysvy

Beloppen som visas på sidan **Analys per dimension** ger dig en bild av företagets status vid tidpunkten för den sista uppdateringen. Om du vill få en bild av den aktuella situationen måste du uppdatera analysvyn genom att köra funktionen Uppdatera.

Använd nedanstående procedur för att uppdatera en analysvy från sidan **Analys per dimension**. Stegen är liknande de för uppdatering av sidorna **Analysvykort** och **Analysvylista**.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Analysvyer** och väljer sedan relaterad länk.
2. Välj lämplig analysvy och välj åtgärden **Analys per dimension**.
3. På sidan **analys per dimension** väljer du fältet **Analysvykod** för att visa alternativen.  
4. Välj raden med önskad analysvy.  
5. På sidan **Analysvy** väljer du analysvyn och sedan åtgärden **Uppdatera**.  

> [!TIP]  
> Om du markerar kryssrutan **Uppdatera vid bokföring** på ett analysvykort, uppdateras vyn automatiskt när du bokför en transaktion som berörs.

> [!NOTE]  
> Om du vill uppdatera några eller alla analysvyer samtidigt måste du använda batchjobbet **Uppdatera analysvyer**.  

## <a name="see-related-training-at-microsoft-learn" />Se relaterad utbildning på [Microsoft Learn](/learn/modules/dimensions-financial-reports-dynamics-365-business-central/index).

## <a name="see-also" />Se även

[Financial Business Intelligence](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
