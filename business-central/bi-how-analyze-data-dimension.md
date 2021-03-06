---
title: Analysera data efter dimensioner | Microsoft Docs
description: Beskriver hur du kan analysera olika affärsdata per dimension.
services: project-madeira
documentationcenter: ''
author: edupont
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ea949363506e9bc0d9bb3a1a4d53937501e8a5bb
ms.sourcegitcommit: cbd00f24fb471381bbfd64670237eda176bd78e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947394"
---
#  <a name="analyze-data-by-dimensions"></a>Analysera data efter dimensioner
Inom ekonomisk analys är en dimension data som du kan lägga till en transaktion som en sorts markör. Dessa data används för att gruppera transaktioner med liknande egenskaper, till exempel kunder, regioner, produkter och säljare, och enkelt hämta dessa grupper för analys. Dimensioner kan användas på transaktioner i journaler, dokument och budgetar. Termen dimension används för att beskriva hur analyser utförs. Ett exempel på en tvådimensionell analys är försäljning per område. Om du använder fler än två dimensioner när du skapar en transaktion kan du utföra mer komplexa analyser, exempelvis försäljning per försäljningskampanj per kundgrupp per område. Mer information finns i [Arbeta med](finance-dimensions.md).

Att analyera data efter dimensioner ger dig bättre inblick i din verksamhet, så att du kan utvärdera information, till exempel hur väl verksamheten fungerar, inom vilka områden det går riktigt bra och inom vilka det går sämre samt var det krävs mer resurser.

> [!TIP]
> Som ett snabbt sätt att analysera transaktionsdata med dimensioner kan du filtrera summorna i kontoplanen och posterna på alla sidor för **Transaktioner** per dimension. Sök efter åtgärden **Ange dimensionsfilter**.

> [!NOTE]
> Om du upptäcker att en felaktig dimension har använts på bokförda redovisningstransaktioner kan du korrigera dimensionsvärdena och uppdatera analysvyerna. Mer information finns i [Felsöka och korrigera dimensioner](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting)

## <a name="to-set-up-an-analysis-view"></a>Så här definierar du en analysvy  
En analys per dimension visar en vald kombination av dimensioner. Du kan lagra och hämta alla analyser som har definierats. Informationen som används för att skapa en analys lagras på **analysvykortet** för att underlätta framtida analyser.  

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Analysvy** och välj sedan relaterad länk.  
2. På sidan **Analysvylista** väljer du åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Om du vill lägga till ytterligare dimensionskoder förutom de fyra koderna väljer du på snabbfliken **Dimensioner**, åtgärden **Filter**, fyller i fälten och klickar på **OK**.  
5. Om du vill uppdatera vyn, väljer du åtgärden **uppdatera**.

## <a name="to-analyze-by-dimensions"></a>Analysera efter dimensioner
Du kan använda matrisen **Analys per dimension** för att visa beloppen i redovisningen med hjälp av de analysvyer som du har definierat. Du fyller i sidan **Analys per dimension** för att definiera vad som ska visas i matrisen och klickar sedan på **Visa matris** för att visa matrisen.  

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Analysvy** och välj sedan relaterad länk.  
2. Välj lämplig analysvy och klicka på **Analys per dimension**.
3. Högst upp på sidan **Analys efter dimensioner** fyller du i fälten för att definiera vilka data som ska visas och hur.
4. Välj åtgärden **Visa matris** för att öppna respektive matrissida för den definierade analysvyn.
5. Om du vill visa en specifikation av ett belopp som visas på matrissidan väljer du beloppet för att granska dem i detalj.  

- Kolumnen till vänster innehåller information baserad på vad du valt i fältet **Visa som rader** i huvudet.  
- Kolumnen till höger innehåller information baserad på vad du valt i fältet **Visa som kolumner** i huvudet.

> [!IMPORTANT]  
>   Du kan inte välja en period som är kortare än perioden som angetts för datumkomprimeringen på **Analysvy**-kortet. Kommandona **Nästa period** och **Föregående period** är inaktiverade om du har valt **Period** i **Visa som rader** eller **Visa som kolumner**.  

> [!NOTE]  
>   Du kan använda rapporten **Dimensioner – detaljerad** om du vill visa en detaljerad klassificering av hur dimensionerna har använts på transaktioner under en vald period. Du använder rapporten **Dimensioner – total** om du bara vill visa totalbeloppen.  

> [!TIP]  
>   Du kan också ändra vyn genom att ändra innehållet i fältet **Visa som rader** och fältet **Visa om kolumner**. Om du vill ändra vyinställningen, väljer du åtgärden **Byt plats på rader och kolumner**.

## <a name="to-update-an-analysis-view"></a>Så här uppdaterar du en analysvy  
Beloppen som visas på sidan **Analys per dimension** ger dig en bild av företagets status vid tidpunkten för den sista uppdateringen. Om du vill få en bild av den aktuella situationen måste du uppdatera analysvyn genom att köra funktionen Uppdatera.

Nedanstående procedur beskriver hur du uppdaterar en analysvy från sidan **Analys per dimension**. Momentet är liknande från sidorna **Analysvykort** och **Analysvylista**.  

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Analysvy** och välj sedan relaterad länk.
2. Välj lämplig analysvy och klicka på **Analys per dimension**.
2. På sidan **analys per dimension** väljer du fältet **Analysvykod** för att visa alternativen.  
3. Välj raden med önskad analysvy.  
4. På sidan **Analysvy** väljer du åtgärden **Uppdatera**.  

> [!TIP]  
>   Om du väljer kryssrutan **Uppdatera vid bokföring** på ett analysvykort, uppdateras vyn automatiskt när du bokför en transaktion som berörs.

> [!NOTE]  
>   Om du vill uppdatera några eller alla analysvyer samtidigt måste du använda batchjobbet **Uppdatera analysvyer**.  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/dimensions-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även
[Affärsstöd](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]