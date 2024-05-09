---
title: Analysera data efter dimensioner
description: I den här artikeln beskrivs hur du kan analysera affärsdata efter dimensioner för att få bättre insikt i verksamheten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 04/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Analysera data efter dimensioner

Inom ekonomisk analys är en dimension data som du lägger till en transaktion som en sorts markör för att gruppera poster med liknande egenskaper. Dimensioner grupperar till exempel ofta transaktioner för kunder, regioner, produkter och säljare. Med grupperna kan du enkelt hämta data om dem för analys. Du kan använda dimensioner på transaktioner i journaler, dokument och budgetar.

Varje dimension används för att beskriva analysens fokus. Så till exempel en tvådimensionell analys är försäljning per område. Genom att använda fler än två dimensioner när du skapar en transaktion kan du utföra en mer komplex analys. Ett exempel på en komplex analys är att utforska försäljning per försäljningskampanj per kundgrupp per område. Det ger dig större insikt i ditt företag, till exempel hur väl ditt företag fungerar, var det är eller inte blomstrar och var du bör allokera mer resurser. Den insikten hjälper dig att fatta mer välgrundade affärsbeslut. Mer information: [Arbeta med dimensioner](finance-dimensions.md).

> [!TIP]
> Som ett snabbt sätt att analysera transaktionsdata efter dimensioner kan du filtrera summorna i kontoplanen och posterna på alla sidor för **Transaktioner** per dimension. Sök efter åtgärden **Ange dimensionsfilter**.

> [!NOTE]
> Om du upptäcker att ett felaktigt dimensionsvärde har använts på bokförda redovisningstransaktioner kan du korrigera det och uppdatera analysvyerna. Läs mer i [Felsökning och korrigering av dimensioner](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## Definiera en analysvy

En analys per dimension använder en vald kombination av dimensioner. Du kan lagra, hämta och uppdatera dimensionsuppsättningen genom att skapa ett **analysvykort**.

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Analysvyer** och väljer sedan relaterad länk.  
2. På sidan **Analysvylista** väljer du åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Om du vill lägga till ytterligare dimensionskoder förutom de fyra koderna väljer du på snabbfliken **Dimensioner**, åtgärden **Filter**, fyller i fälten och klickar på **OK**.  
5. Om du vill uppdatera vyn, väljer du åtgärden **uppdatera**.

## Analysera efter dimensioner

Använd analysvyer som du redan har konfigurerat med matrisen **Analys per dimension** för att visa beloppen i redovisningen.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Analysvyer** och väljer sedan relaterad länk.  
2. Välj lämplig analysvy och välj åtgärden **Analys per dimension**.
3. Högst upp på sidan **Analys efter dimensioner** fyller du i fälten för att definiera vilka data som ska visas och hur.
4. Välj åtgärden **Visa matris** för att öppna matrissidan för analysvyn.
5. Om du vill visa information om ett belopp på matrissidan väljer du beloppet.  

- Kolumnen till vänster innehåller information baserad på vad du valt i fältet **Visa som rader** i huvudet.  
- Kolumnen till höger innehåller information baserad på vad du valt i fältet **Visa som kolumner** i huvudet.

> [!IMPORTANT]  
> Du kan inte välja en period som är kortare än perioden som angetts för datumkomprimeringen på **Analysvy**-kortet. Åtgärderna **Nästa uppsättning** och **Föregående uppsättning** är inte tillgängliga om du har valt **Period** i något av fälten **Visa som rader** eller **Visa som kolumner**.  

> [!NOTE]  
> Du kan använda rapporten **Dimensioner - detaljerad** om du vill visa en detaljerad klassificering av hur dimensionerna har använts på transaktioner under en vald period. Du använder rapporten **Dimensioner – total** om du bara vill visa totalbeloppen.  

> [!TIP]  
> Du kan också ändra vyn genom att ändra innehållet i fälten **Visa som rader** och **Visa som kolumner**. Om du vill ändra vyinställningen, väljer du åtgärden **Byt plats på rader och kolumner**.

## Uppdatera en analysvy

Beloppen som visas på sidan **Analys per dimension** ger dig en bild av företagets status vid tidpunkten för den sista uppdateringen. Hämta det aktuella tillståndet genom att köra uppdateringsåtgärden för att uppdatera analysvyn.

Använd nedanstående procedur för att uppdatera en analysvy från sidan **Analys per dimension**. Stegen är liknande de för uppdatering av sidorna **Analysvykort** och **Analysvylista**.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Analysvyer** och väljer sedan relaterad länk.
2. Välj lämplig analysvy och välj åtgärden **Analys per dimension**.
3. På sidan **analys per dimension** väljer du fältet **Analysvykod** för att visa alternativen.  
4. Välj raden med önskad analysvy.  
5. På sidan **Analysvy** väljer du analysvyn och sedan åtgärden **Uppdatera**.  

> [!TIP]  
> Om du markerar kryssrutan **Uppdatera vid bokföring** på ett analysvykort, uppdateras vyn automatiskt när någon bokför en transaktion som berörs.

> [!NOTE]  
> Om du vill uppdatera några eller alla analysvyer samtidigt måste batchjobbet **Uppdatera analysvyer** användas.  

## Se även

[Ekonomisk business intelligence](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
