---
title: Skapa underhållnning för anläggningstillgångar | Microsoft Docs
description: Om du vill hantera anläggningstillgångars reparationer och service, kan du ange allmän underhållsinformation, koder för typen av arbete och ett bokföringskonto för kostnader.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b437f7508537ec438bf90c3a1239e2620e9db196
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775556"
---
# <a name="set-up-fixed-asset-maintenance"></a>Skapa underhåll för anläggningstillgångar
Om du vill hantera underhåll av anläggningstillgångar måste du först ange viss allmän underhållsinformation, ett bokföringskonto för underhållskostnader och underhållskoder för olika typer av arbete, till exempel rutintjänst eller reparation.

## <a name="to-set-up-general-maintenance-information"></a>Så här ställer du in allmän underhållsinformation
Om du skapar fält för underhåll kan du bokföra underhållskostnader från anläggningstillgångsjournalen.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Anläggningstillgångar** och välj sedan relaterad länk.
2. Markera den fasta anläggningstillgång som du definierar täckning av försäkring för välj sedan åtgärden **Redigera**.
3. Fyll i så många fält som behövs på snabbfliken **Underhåll**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Så här skapar du underhållskoder
När du bokför underhållskostnader (från en redovisningsjournal eller en inköpsfaktura) fyller du i fältet **Underhållskod** för att ange vilken typ av underhåll som har utförts, t. ex. rutinservice eller reparation.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Underhåll** och välj sedan tillhörande länk.
2. Lägg upp koder för andra typer av underhållsarbete på sidan **Underhåll**.

## <a name="to-set-up-maintenance-expense-accounts"></a>Så här skapar du underhållskostnader
Om du vill bokföra underhållskostnader måste du först ange ett kontonummer på sidan **Anl. bokföringsmallar**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Anl.bokföringsmallar** och välj sedan tillhörande länk.
2. Fyll i fältet **Underhållskostnader** för varje bokföringsmall.

> [!NOTE]  
>   Om du vill att underhållskostnaderna ska fördelas på avdelningar och/eller projekt måste du skapa en fördelningsnyckel Mer information finns i [Konfigurera allmänna funktioner för anläggningstillgångar](fa-how-setup-general.md).

## <a name="see-also"></a>Se även
[Ställa in anläggningstillgångar](fa-setup.md)  
[Anläggningstillgångar](fa-manage.md)  
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]