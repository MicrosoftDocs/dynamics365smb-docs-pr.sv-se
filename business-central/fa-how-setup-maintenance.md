---
title: "Skapa underhållnning för anläggningstillgångar | Microsoft Docs"
description: "Om du vill hantera anläggningstillgångars reparationer och service, kan du ange allmän underhållsinformation, koder för typen av arbete och ett bokföringskonto för kostnader."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: b730e880a3cf9f2ba3a2abaa25a1b80848f52e97
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-fixed-asset-maintenance"></a>Skapa underhåll för anläggningstillgångar
Om du vill hantera underhåll av anläggningstillgångar måste du först ange viss allmän underhållsinformation, ett bokföringskonto för underhållskostnader och underhållskoder för olika typer av arbete, till exempel rutintjänst eller reparation.

## <a name="to-set-up-general-maintenance-information"></a>Så här ställer du in allmän underhållsinformation
Om du skapar fält för underhåll kan du bokföra underhållskostnader från anläggningstillgångsjournalen.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Anläggningstillgångar** och välj sedan relaterad länk.
2. Markera den fasta anläggningstillgång som du definierar täckning av försäkring för välj sedan åtgärden **Redigera**.
3. Fyll i så många fält som behövs på snabbfliken **Underhåll**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Så här skapar du underhållskoder
När du bokför underhållskostnader (från en redovisningsjournal eller en inköpsfaktura) fyller du i fältet **Underhållskod** för att ange vilken typ av underhåll som har utförts, t.ex. rutinservice eller reparation.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Underhåll** och välj sedan relaterad länk.
2. Lägg upp koder för andra typer av underhållsarbete i fönstret **Underhåll**.

## <a name="to-set-up-maintenance-expense-accounts"></a>Så här skapar du underhållskostnader
Om du vill bokföra underhållskostnader måste du först ange ett kontonummer i fönstret **Anl. bokföringsmallar**.

1. Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Anl. bokföringsmallar** och välj sedan relaterad länk.
2. Fyll i fältet **Underhållskostnader** för varje bokföringsmall.

> [!NOTE]  
>   Om du vill att underhållskostnaderna ska fördelas på avdelningar och/eller projekt måste du skapa en fördelningsnyckel Mer information finns i [Konfigurera allmänna funktioner för anläggningstillgångar](fa-how-setup-general.md).

## <a name="see-also"></a>Se även
[Ställa in anläggningstillgångar](fa-setup.md)  
[Anläggningstillgångar](fa-manage.md)  
[Ekonomi](finance.md)  
[Komma igång](product-get-started.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

