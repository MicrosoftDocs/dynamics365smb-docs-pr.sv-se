---
title: "Så här: Skapa underhåll för anläggningstillgångar | Microsoft Docs"
description: "Beskriver hur du ställer in systemet för underhåll av anläggningstillgångar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e97f3cec67fa8b0ef270d406a0efe804da82d99f
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-fixed-asset-maintenance"></a>Så här skapar du underhåll av anläggningstillgångar
Om du vill hantera underhåll av anläggningstillgångar måste du först ange viss allmän underhållsinformation, ett bokföringskonto för underhållskostnader och underhållskoder för olika typer av arbete, till exempel rutintjänst eller reparation.

## <a name="to-set-up-general-maintenance-information"></a>Så här ställer du in allmän underhållsinformation
Om du skapar fält för underhåll kan du bokföra underhållskostnader från anläggningstillgångsjournalen.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Anläggningstillgångar**, och välj sedan relaterad länk.
2. Markera den fasta anläggningstillgång som du definierar täckning av försäkring för välj sedan åtgärden **Redigera**.
3. Fyll i så många fält som behövs på snabbfliken **Underhåll**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Så här skapar du underhållskoder
När du bokför underhållskostnader (från en redovisningsjournal eller en inköpsfaktura) fyller du i fältet **Underhållskod** för att ange vilken typ av underhåll som har utförts, t.ex. rutinservice eller reparation.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **underhåll**, och välj sedan relaterad länk.
2. Lägg upp koder för andra typer av underhållsarbete i fönstret **Underhåll**.

## <a name="to-set-up-maintenance-expense-accounts"></a>Så här skapar du underhållskostnader
Om du vill bokföra underhållskostnader måste du först ange ett kontonummer i fönstret **Anl. bokföringsmallar**.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger **Anl. bokföringsmall** och väljer sedan relaterad länk.
2. Fyll i fältet **Underhållskostnader** för varje bokföringsmall.

**Obs**: om du vill att underhållskostnaderna ska fördelas på avdelningar och/eller projekt måste du skapa en fördelningsnyckel Mer information finns i [Så här ställer du in allmänna funktioner för anläggningstillgångar](fa-how-setup-general.md).

## <a name="see-also"></a>Se även
[Ställa in anläggningstillgångar](fa-setup.md)  
[Anläggningstillgångar](fa-manage.md)  
[Ekonomi](finance.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]] (index.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

