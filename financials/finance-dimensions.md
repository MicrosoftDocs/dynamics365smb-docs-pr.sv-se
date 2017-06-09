---
title: Dimensioner | Microsoft Docs
description: "Använda dimensioner för att analysera data."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7552ee2b3398c203a7f3295f3203c83914fbb15f
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="dimensions"></a>Dimensioner
Du kan använda dimensioner för att göra det enklare att analysera dokument såsom försäljningsorder. Dimensioner är attribut och värden som kategoriserar transaktioner så att du kan spåra och analysera dem. Dimensioner kan till exempel ange vilket projekt eller vilken avdelning en transaktion kom ifrån.  

T.ex. kan du använda dimensioner i stället för att skapa separata redovisningskonton för varje avdelning och projekt. Detta ger stora möjligheter för analys, utan att skapa en komplicerad kontoplan.  

Ett annat exempel är att ställa in en dimension kallad *Avdelning* och använda denna dimension när du bokför försäljningsdokument. Det gör att du kan använda business intelligence-verktyg för att visa vilken avdelning som sålt vilka artiklar.
Ju fler dimensioner du använder, desto mer detaljerade rapporter kan du baseras dina affärsbeslut på. En enda försäljningstransaktion kan till exempel innehålla olika dimensionsinformation som t.ex.:  

* Kontot som artikeln bokfördes till  
* Var artikeln såldes
* Vem som sålde den
* Vilken typ av kund som köpte den  

Du kan skapa så många dimensioner med så många värden du vill.  

**Obs!** den här funktionen kräver att din upplevelse är inställd på **Paket **. Mer information finns i avsnittet [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="using-dimensions"></a>Använda dimensioner
I ett dokument som t.ex. en försäljningsorder kan du lägga till dimensionsinformation för både en individuell dokumentrad och själva dokument. T.ex. i fönstret **Försäljningsorder** kan du ange dimensionsvärden för de två första genvägsdimensionerna på den individuella försäljningsraden och du kan lägga till ytterligare dimensionsinformation om du väljer knappen **Dimensioner**.  

Om du istället arbetar med en journal kan du lägga till dimensionsinformation i en transaktion om du har lagt upp genvägsdimensioner som fält direkt på journalraderna.  

Du kan ställa in standarddimensioner för konton eller kontotyper, så att dimensioner och dimensionsvärden fylls i automatiskt.  

## <a name="dimension-sets"></a>Dimensionsuppsättningar
En dimensionsuppsättning en är en unik kombination av dimensionsvärden. Den lagras som dimensionsuppsättningstransaktioner i databasen. Varje dimensionsuppsättningstransaktion representerar ett enstaka dimensionsvärde. Dimensionsuppsättningen identifieras av ett gemensamt dimensionsuppsättnings-ID som tilldelats varje dimensionsuppsättningstransaktion som tillhör dimensionsuppsättningen.  

När du skapar en journalrad, dokumenthuvud eller dokumentrad kan du ange en kombination av dimensionsvärden. I stället för att uttryckligen lagra varje dimensionsvärde i databasen tilldelas ett dimensionsuppsättnings-ID till journalraden, dokumenthuvudet eller dokumentraden för att specificera dimensionsuppsättningen.  

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Lägga upp dimensioner](finance-setup-dimensions.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

