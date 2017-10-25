---
title: "Skapa ett lagerställekort och definiera överföringsflöden | Microsoft Docs"
description: "Du kan skapa ett lagerställekort för varje plats som du vill lagra lagerartiklar, till exempel lager eller distributionscenter, och ange flöden för överföring av artiklar mellan olika lagerställen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7d82b1c63bb1da367736f8dd044640b583493af8
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-locations"></a>Så här skapar du lagerställen
Om du köper, lagrar eller säljer artiklar på mer än en plats eller ett lager, måste du ställa in varje plats med ett lagerställeskort och definiera överföringsflöden.

Du kan sedan skapa dokumentrader för ett visst lagerställe, visa disposition per lagerställe och överföra lager mellan olika lagerställen. Mer information finns i [Administrera projekt](inventory-manage-inventory.md).

> [!NOTE]  
>   Den här funktionen kräver att din upplevelse är inställd på **Paket**. Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="to-create-a-location-card"></a>Skapa ett nytt lagerställeskort
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. I fönstret **Lagerställeskort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Upprepa steg 2 och 3 för varje lagerställe där du vill bedriva lagerhållning.

> [!NOTE]  
> Många fält på lagerställekortet hänvisar till hanteringen av artiklar i ingående och utgående lagerprocesser. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md). 

## <a name="to-create-a-transfer-route"></a>Så här skapar du ett överföringsflöde
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Överföringsflöden** och välj sedan relaterad länk.
2. Alternativt kan du i fönstret **Lagerställekort** välja åtgärden **Överföringsflöden**.
3. Välj åtgärden **Ny**.
4. I fönstret **Lagerställeskort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Du kan nu överföra lagerartiklar mellan två lagerställen. Mer information finns i [Så här överför du lager mellan olika lagerställen](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Se även
[Hantera lager](inventory-manage-inventory.md)  
[Så här överför du lager mellan olika lagerställen](inventory-how-transfer-between-locations.md)    
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)]-upplevelse](ui-experiences.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

