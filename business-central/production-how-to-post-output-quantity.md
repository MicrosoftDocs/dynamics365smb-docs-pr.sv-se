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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: cc4acf5fbaf10df3b833e310a83854e52b0d2b73
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313258"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="0c139-103">Batch-bokför utflöde och körtider</span><span class="sxs-lookup"><span data-stu-id="0c139-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="0c139-104">Utflödesantalet representerar det pågående arbetet som det färdiga antalet.</span><span class="sxs-lookup"><span data-stu-id="0c139-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="0c139-105">Endast när du bokför utflödesantalet för den sista operationen uppdateras lagret automatiskt.</span><span class="sxs-lookup"><span data-stu-id="0c139-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="0c139-106">Om du vill bokföra utflödeskvantiteter för produktion av en eller flera orderrader</span><span class="sxs-lookup"><span data-stu-id="0c139-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="0c139-107">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Utflödesjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="0c139-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0c139-108">Fyll i fälten med data om produktionsorden och utdata.</span><span class="sxs-lookup"><span data-stu-id="0c139-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="0c139-109">Om operationen har slutförts, välj fältet **FÄRDIG**.</span><span class="sxs-lookup"><span data-stu-id="0c139-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="0c139-110">Om lagerplatser används på det lagerställe där artiklarna ska placeras, men bearbetning av artikelinförsel inte krävs,  ska journalraden tilldelas en lagerplatskod som anger var artiklarna ska placeras på distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="0c139-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="0c139-111">Mer information finns i [Föra in produktions- eller monteringsutflöde](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="0c139-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="0c139-112">Om du vill bokföra operationerna väljer du åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="0c139-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="0c139-113">Utflödesantalet bokförs.</span><span class="sxs-lookup"><span data-stu-id="0c139-113">The output quantity will be posted.</span></span> <span data-ttu-id="0c139-114">Artikeln är nu tillgänglig för leverans.</span><span class="sxs-lookup"><span data-stu-id="0c139-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="0c139-115">Om du vill bokföra körtider för produktion av en eller flera rader</span><span class="sxs-lookup"><span data-stu-id="0c139-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="0c139-116">Bearbetningstiden representerar det pågående arbetet som nödvändig arbetstid.</span><span class="sxs-lookup"><span data-stu-id="0c139-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="0c139-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Utflödesjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="0c139-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0c139-118">Fyll i fälten med data om produktionsorden och utdata.</span><span class="sxs-lookup"><span data-stu-id="0c139-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="0c139-119">Om operationen har slutförts, välj fältet **FÄRDIG**.</span><span class="sxs-lookup"><span data-stu-id="0c139-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="0c139-120">Välj åtgärden **bokför** för att bokföra spenderad tid per operation.</span><span class="sxs-lookup"><span data-stu-id="0c139-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="0c139-121">Kapacitetstransaktioner uppdateras för använt arbete eller maskingrupper.</span><span class="sxs-lookup"><span data-stu-id="0c139-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c139-122">Se även</span><span class="sxs-lookup"><span data-stu-id="0c139-122">See Also</span></span>  
<span data-ttu-id="0c139-123">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="0c139-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="0c139-124">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="0c139-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="0c139-125">[Planerad](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="0c139-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="0c139-126">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="0c139-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="0c139-127">Inköp</span><span class="sxs-lookup"><span data-stu-id="0c139-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="0c139-128">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c139-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
