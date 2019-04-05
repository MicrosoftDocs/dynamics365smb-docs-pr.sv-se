---
title: Så här Batch-bokför du produktionsutflöde och körtid | Microsoft Docs
description: Utflödesantalet representerar det pågående arbetet som det färdiga antalet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 7b895978bd55cd6ed7086326036016002519817e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "808227"
---
# <a name="batch-post-output-and-run-times"></a>Batch-bokför utflöde och körtider
Utflödesantalet representerar det pågående arbetet som det färdiga antalet.  

> [!NOTE]
> Endast när du bokför utflödesantalet för den sista operationen uppdateras lagret automatiskt.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Om du vill bokföra utflödeskvantiteter för produktion av en eller flera orderrader
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Utflödesjournal** och välj sedan relaterad länk.  
2. Fyll i fälten med data om produktionsorden och utdata. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om operationen har slutförts, välj fältet **FÄRDIG**.  

    Om lagerplatser används på det lagerställe där artiklarna ska placeras, men bearbetning av artikelinförsel inte krävs,  ska journalraden tilldelas en lagerplatskod som anger var artiklarna ska placeras på distributionslagret. Mer information finns i [Föra in produktions- eller monteringsutflöde](warehouse-how-to-put-away-production-output.md).  

4. Om du vill bokföra operationerna väljer du åtgärden **Bokför**. Utflödesantalet bokförs. Artikeln är nu tillgänglig för leverans.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Om du vill bokföra körtider för produktion av en eller flera rader
Bearbetningstiden representerar det pågående arbetet som nödvändig arbetstid.    

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Utflödesjournal** och välj sedan relaterad länk.  
2. Fyll i fälten med data om produktionsorden och utdata.  
3.  Om operationen har slutförts, välj fältet **FÄRDIG**.  
4. Välj åtgärden **bokför** för att bokföra spenderad tid per operation. Kapacitetstransaktioner uppdateras för använt arbete eller maskingrupper.

## <a name="see-also"></a>Se även  
[Produktion](production-manage-manufacturing.md)    
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)      
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
