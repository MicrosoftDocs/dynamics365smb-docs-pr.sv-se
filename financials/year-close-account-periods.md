---
title: "Avsluta bokföringsperioder för räkenskapsåret | Microsoft Docs"
description: "Beskriver hur du avslutar bokföringsperioder som utgör räkenskapsåret."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 859801a5e9d9b900aed6af5fe672f650932b2e79
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-close-accounting-periods"></a>Så här avslutar du bokföringsperioder
När ett räkenskapsår är slut måste du avsluta perioderna som året omfattar.

## <a name="to-close-accounting-periods"></a>Så här avslutar du bokföringsperioder
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Bokföringsperioder** och välj sedan relaterad länk.
2. I fönstret **Bokföringsperioder** väljer du åtgärden **Avsluta år**.

    Om flera räkenskapsår är öppna kommer det tidigaste att stängas automatiskt. Visar ett meddelande för vilket år som ska stängas och konsekvenserna av att stänga året.
3. Välj **ja** för att stänga året.

Räkenskapsåret stängs och fälten **Avslutat** och **Låst datum** markeras för samtliga perioder i året. Räkenskapsåret kan inte öppnas igen och du kan inte heller ta bort markeringen i fälten **Avslutat** eller **Låst datum**.

> [!NOTE]  
>   Du kan inte avsluta ett räkenskapsår förrän du har upprättat ett nytt. Notera att du inte kan ändra startdatumet för det följande räkenskapsåret när räkenskapsåret är avslutat.

Även om ett räkenskapsår har avslutats kan du fortfarande bokföra redovisningstransaktioner på året. När du gör det markeras transaktionerna som bokförda på ett avslutat räkenskapsår och fältet **Föregående års transaktion** markeras.

När ett räkenskapsår har avslutats måste resultatkontona avslutas och årets resultat flyttas över till ett konto i balansräkningen. Du kan göra samma sak varje gång du bokför på det avslutade räkenskapsåret.

## <a name="see-also"></a>Se även
[Avsluta böcker](year-close-books.md)  
[Så här bokför du årsslutstransaktionen](year-how-post-year-end-close-entry.md)  
[Så här öppnar du ett nytt räkenskapsår](finance-how-open-new-fiscal-year.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

