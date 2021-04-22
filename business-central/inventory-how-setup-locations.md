---
title: Skapa ett lagerställekort och definiera överföringsflöden | Microsoft Docs
description: Du kan skapa ett lagerställekort för varje plats som du vill lagra lagerartiklar, till exempel lager eller distributionscenter, och ange flöden för överföring av artiklar mellan olika lagerställen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5017df2ba46ba81884b2e99e3ea4a1bb983ea681
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785808"
---
# <a name="set-up-locations"></a>Konfigurera platser
Om du köper, lagrar eller säljer artiklar på mer än en plats eller ett lager, måste du ställa in varje plats med ett lagerställeskort och definiera överföringsflöden.

Du kan sedan skapa dokumentrader för ett visst lagerställe, visa disposition per lagerställe och överföra lager mellan olika lagerställen. Mer information finns i [Administrera projekt](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="to-create-a-location-card"></a>Skapa ett nytt lagerställeskort
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Platser** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. På sidan **Lagerställekort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Upprepa steg 2 och 3 för varje lagerställe där du vill bedriva lagerhållning.

> [!NOTE]  
> Många fält på lagerställekortet hänvisar till hanteringen av artiklar i ingående och utgående lagerprocesser. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

## <a name="to-create-a-transfer-route"></a>Så här skapar du ett överföringsflöde
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Överföringsflöden** och välj sedan relaterad länk.
2. Alternativt kan du på sidan **Lagerställekort** välja åtgärden **Överföringsflöden**.
3. Välj åtgärden **Ny**.
4. På sidan **Lagerställekort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Du kan nu överföra lagerartiklar mellan två lagerställen. Mer information finns i [Så här överför du lager mellan olika lagerställen](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Se även
[Hantera lager](inventory-manage-inventory.md)  
[Överföra lager mellan olika lagerställen](inventory-how-transfer-between-locations.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]