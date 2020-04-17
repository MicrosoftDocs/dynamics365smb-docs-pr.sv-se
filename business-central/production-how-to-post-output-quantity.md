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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: a37f79ca10c7c45212d2c0ccf858b3bc7e3bff66
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3190401"
---
# <a name="batch-post-output-and-run-times"></a>Batch-bokför utflöde och körtider
Utflödesantalet representerar det pågående arbetet som det färdiga antalet.  

> [!NOTE]
> Endast när du bokför utflödesantalet för den sista operationen uppdateras lagret automatiskt.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Om du vill bokföra utflödeskvantiteter för produktion av en eller flera orderrader
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **utflödesjournal** och välj sedan relaterad länk.  
2. Fyll i fälten med data om produktionsorden och utdata. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om operationen har slutförts, välj fältet **FÄRDIG**.  

    Om lagerplatser används på det lagerställe där artiklarna ska placeras, men bearbetning av artikelinförsel inte krävs,  ska journalraden tilldelas en lagerplatskod som anger var artiklarna ska placeras på distributionslagret. Mer information finns i [Föra in produktions- eller monteringsutflöde](warehouse-how-to-put-away-production-output.md).  

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
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
