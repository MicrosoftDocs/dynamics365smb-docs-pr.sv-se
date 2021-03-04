---
title: Så här Batch-bokför du produktionsutflöde och körtid | Microsoft Docs
description: Utflödesantalet representerar det pågående arbetet som det färdiga antalet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 82e28246f1a1c65c7bd702023d9c68c614383cc2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759148"
---
# <a name="batch-post-output-and-run-times"></a>Batch-bokför utflöde och körtider
Utflödesantalet representerar det pågående arbetet som det färdiga antalet.  

> [!NOTE]
> Endast när du bokför utflödesantalet för den sista operationen uppdateras lagret automatiskt.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Om du vill bokföra utflödeskvantiteter för produktion av en eller flera orderrader
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **utflödesjournal** och välj sedan relaterad länk.  
2. Fyll i fälten med data om produktionsorden och utdata. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om operationen har slutförts, välj fältet **FÄRDIG**.  

    Om lagerställen används på det lagerställe där artiklarna ska placeras, men bearbetning av artikelinförsel inte krävs,  ska journalraden tilldelas en lagerställeskod som anger var artiklarna ska placeras på distributionslagret. Mer information finns i [Föra in produktions- eller monteringsutflöde](warehouse-how-to-put-away-production-output.md).  

4. Om du vill bokföra operationerna väljer du åtgärden **Bokför**. Utflödesantalet bokförs. Artikeln är nu tillgänglig för leverans.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Om du vill bokföra körtider för produktion av en eller flera rader
Bearbetningstiden representerar det pågående arbetet som nödvändig arbetstid.    

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **utflödesjournal** och välj sedan relaterad länk.  
2. Fyll i fälten med data om produktionsorden och utdata.  
3.  Om operationen har slutförts, välj fältet **FÄRDIG**.  
4. Välj åtgärden **bokför** för att bokföra spenderad tid per operation. Kapacitetstransaktioner uppdateras för använt arbete eller maskingrupper.

## <a name="see-also"></a>Se även  
[Produktion](production-manage-manufacturing.md)    
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]