---
title: Uppdatera valutakurser | Microsoft Docs
description: "För att använda flera valutor i din verksamhet, kan du lägga upp en kod för varje valuta och använda en extern valutakurstjänst, som t.ex. Yahoo."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-update-currency-exchange-rates"></a>Så här uppdaterar du valutakurser
Du måste ange en kod för varje valuta du använder om du köper eller säljer i andra valutor än din lokala valuta, har tillgångar eller skulder i andra valutor eller registrerar transaktioner i olika valutor.  

> [!NOTE]  
>   Den här funktionen kräver att din upplevelse är inställd på **Paket**. Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

Du kan använda en extern tjänst för kontinuerlig uppdatering av aktuella valutakurser. Tjänsten Yahoo valutakurser är förinstallerade och redo att aktiveras.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Så här konfigurerar du en valutakurstjänst
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Valutakurstjänster** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. I fönstret **Valutakurstjänster** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj kryssrutan **aktiverad** om du vill aktivera tjänsten.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Så här uppdaterar du valutakurser från en tjänst
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Valutor** och välj sedan relaterad länk.
2. Välj åtgärden **uppdatera valutakurser**.

Värdet i fältet **valutakurs** i fönstret **valutor** uppdateras med den senaste valutakursen.

## <a name="see-also"></a>Se även
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

