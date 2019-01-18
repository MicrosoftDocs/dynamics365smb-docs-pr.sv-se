---
title: "Avsluta bokföringsperioder för räkenskapsåret | Microsoft Docs"
description: "Beskriver hur du avslutar bokföringsperioder som utgör räkenskapsåret."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: c8f086e0dc7479ece62ab28b64f9553ba2d13b82
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="close-accounting-periods"></a>Avsluta bokföringsperioder
När ett räkenskapsår är slut måste du avsluta perioderna som året omfattar.

## <a name="to-close-accounting-periods"></a>Så här avslutar du bokföringsperioder
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokföringsperioder** och välj sedan relaterad länk.
2. På sidan **Bokföringsperioder** väljer du åtgärden **Avsluta år**.

    Om flera räkenskapsår är öppna kommer det tidigaste att stängas automatiskt. Visar ett meddelande för vilket år som ska stängas och konsekvenserna av att stänga året.
3. Välj **ja** för att stänga året.

Räkenskapsåret stängs och fälten **Avslutat** och **Låst datum** markeras för samtliga perioder i året. Räkenskapsåret kan inte öppnas igen och du kan inte heller ta bort markeringen i fälten **Avslutat** eller **Låst datum**.

> [!NOTE]  
>   Du kan inte avsluta ett räkenskapsår förrän du har upprättat ett nytt. Notera att du inte kan ändra startdatumet för det följande räkenskapsåret när räkenskapsåret är avslutat.

Även om ett räkenskapsår har avslutats kan du fortfarande bokföra redovisningstransaktioner på året. När du gör det markeras transaktionerna som bokförda på ett avslutat räkenskapsår och fältet **Föregående års transaktion** markeras.

När ett räkenskapsår har avslutats måste resultatkontona avslutas och årets resultat flyttas över till ett konto i balansräkningen. Du kan göra samma sak varje gång du bokför på det avslutade räkenskapsåret.

## <a name="see-also"></a>Se även
[Avsluta böcker](year-close-books.md)  
[Bokför årsslutstransaktionen](year-how-post-year-end-close-entry.md)  
[Så här öppnar du ett nytt räkenskapsår:](finance-how-open-new-fiscal-year.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

