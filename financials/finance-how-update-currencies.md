---
title: "Så här uppdaterar du valutakurser från en tjänst | Microsoft Docs"
description: Arbeta med flera valutor
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b261da0f233ce78a9f14c2979c876be401ffedef
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-update-currency-exchange-rates"></a>Så här uppdaterar du valutakurser
Du måste ange en kod för varje valuta du använder om du köper eller säljer i andra valutor än din lokala valuta, har tillgångar eller skulder i andra valutor eller registrerar transaktioner i olika valutor.  

**Obs!** den här funktionen kräver att din upplevelse är inställd på **Paket **. Mer information finns i avsnittet [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

Du kan använda en extern tjänst för kontinuerlig uppdatering av aktuella valutakurser. Tjänsten Yahoo valutakurser är förinstallerade och redo att aktiveras.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Så här konfigurerar du en valutakurstjänst
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Valutakurstjänster**, och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. I fönstret **Valutakurstjänster** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj kryssrutan **aktiverad** om du vill aktivera tjänsten.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Så här uppdaterar du valutakurser från en tjänst
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Valutor**, och välj sedan relaterad länk.
2. Välj åtgärden **uppdatera valutakurser**.

Värdet i fältet **valutakurs** i fönstret **valutor** uppdateras med den senaste valutakursen.

## <a name="see-also"></a>Se även
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

