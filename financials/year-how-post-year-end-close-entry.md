---
title: "Granska och bokför du årsslutstransaktionen | Microsoft Docs"
description: "Beskriver hur du öppnar den journal du har angett i batch-jobbet Avslut av resultatkonton och sedan granska och bokföra årsslutstransaktionen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 68017b8b031ee4bd368936b6fb4de157328d7030
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-post-the-year-end-closing-entry"></a>Så här bokför du årsslutstransaktionen
När du har använt batch-jobbet **Avslut av resultatkonton** för att generera transaktioner eller bokslutsposter för årsslut, måste du öppna den journal du har angett i batch-jobbet och sedan granska och bokföra transaktionerna.

## <a name="to-post-the-year-end-closing-entry"></a>Så här bokför du årsslutstransaktionen
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningsjournal** och välj sedan relaterad länk.
2. I fönstret **Redovisningsjournal** i fältet **Batch-namn** väljer du den batch som innehåller årsavslutstransaktionerna.
3. Granska transaktionerna.
4. Om du vill bokföra journalen väljer du åtgärden **Bokför**.

> [!NOTE]  
>   Om ett fel påträffas visas ett felmeddelande. Om bokföringen utförs tas de bokförda transaktionerna bort från journalen. Efter bokföringen bokförs en transaktion på varje resultatkonto så att saldot blir noll och årets resultat överförs till balansräkningen.

## <a name="see-also"></a>Se även
[Så här avslutar du bokföringsperioder](year-close-account-periods.md)  
[Avsluta böcker](year-close-books.md)  
[Avslut av resultatkonton](year-close-income-statement.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

