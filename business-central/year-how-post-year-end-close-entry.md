---
title: Bokför årsslutstransaktionen
description: Beskriver hur du öppnar den journal du har angett i batch-jobbet Avslut av resultatkonton och sedan granska och bokföra årsslutstransaktionen.
author: edupont04
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.search.form: 100
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: d426dc74506a244746d8696dc12f80a0ada3a58e
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8142704"
---
# <a name="posting-the-year-end-closing-entry"></a>Bokför du årsslutstransaktionen

När du har använt batch-jobbet **Avslut av resultatkonton** för att generera transaktioner eller bokslutsposter för årsslut, måste du öppna den journal du har angett i batch-jobbet och sedan granska och bokföra transaktionerna.  

> [!TIP]
> Beroende på organisationens arbetsprocesser kan du välja att avsluta eller inte avsluta bokföringsperioder och räkenskapsår i [!INCLUDE [prod_short](includes/prod_short.md)]. Följande procedur förutsätter att du har avslutat räkenskapsåret med hjälp av alternativet *Bokföringsperioder*, genererat en årsbokslutstransaktion med hjälp av batchjobbet **Avsluta resultaträkning** och är nu redo att bokföra årsbokslutstransaktionen tillsammans med kontoposter för motbokskapital. Organisationen kan välja att arbeta annorlunda, till exempel bokföra årsbokslutstransaktionen som en del av räkenskapsåret.

## <a name="to-post-the-year-end-closing-entry"></a>Så här bokför du årsslutstransaktionen

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **redovisningsjournal** och väljer sedan relaterad länk.
2. På sidan **Redovisningsjournal** i fältet **Batch-namn** väljer du den batch som innehåller årsavslutstransaktionerna.
3. Granska transaktionerna.
4. Om du vill bokföra journalen väljer du åtgärden **Bokför**.

> [!NOTE]  
> Om ett fel påträffas visas ett felmeddelande. Om bokföringen utförs tas de bokförda transaktionerna bort från journalen. Efter bokföringen bokförs en transaktion på varje resultatkonto så att saldot blir noll och årets resultat överförs till balansräkningen.

## <a name="see-also"></a>Se även

[Avsluta bokföringsperioder](year-close-account-periods.md)  
[Avsluta böcker](year-close-books.md)  
[Avslut av resultatkonton](year-close-income-statement.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]