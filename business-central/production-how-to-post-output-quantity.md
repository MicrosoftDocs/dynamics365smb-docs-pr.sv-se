---
title: Batch-bokför produktionsutflöde och körtid
description: Utflödesantalet representerar arbetsförloppet i form av färdig kvantitet och utnyttjad kapacitet för produktions- eller maskingrupp.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787883"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="cf351-103">Batch-bokför utflöde och körtider</span><span class="sxs-lookup"><span data-stu-id="cf351-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="cf351-104">Utflödesantalet representerar arbetsförloppet i form av färdig kvantitet och utnyttjad kapacitet för produktions- eller maskingrupp.</span><span class="sxs-lookup"><span data-stu-id="cf351-104">The output quantity represents the work progress in the form of the finished quantity and used capacity of work or machine center.</span></span>

<span data-ttu-id="cf351-105">Du kan välja använda utflödesjournal för att:</span><span class="sxs-lookup"><span data-stu-id="cf351-105">You can use the output journal to:</span></span>
*  <span data-ttu-id="cf351-106">Justera lagret i samband med utflödet av slutartiklar från produktion.</span><span class="sxs-lookup"><span data-stu-id="cf351-106">Adjust inventory in connection with output of finished items from production.</span></span>
*  <span data-ttu-id="cf351-107">Registrera kvantiteter och skrot för varje operation i produktionsoperationsföljden.</span><span class="sxs-lookup"><span data-stu-id="cf351-107">Register quantities and scrap for each operation in production routing.</span></span>
*  <span data-ttu-id="cf351-108">Registrera inställning och körtid för produktions- och maskingrupper.</span><span class="sxs-lookup"><span data-stu-id="cf351-108">Register setup and run time for work and machine centers.</span></span>

> [!NOTE]
> <span data-ttu-id="cf351-109">Om produktionens operationsföljd används uppdateras inventeringen endast när du bokför utflöde antal vid den senaste operationen.</span><span class="sxs-lookup"><span data-stu-id="cf351-109">If production routing are used, the inventory is updated only when you post output quantity on the last operation.</span></span>

<span data-ttu-id="cf351-110">Med fönstret **Produktionsjournal** kan du utföra samma uppgifter som i fönstret **Utflödesjournal** och samtidigt utföra de relaterade bokföringsuppgifterna för förbrukningen.</span><span class="sxs-lookup"><span data-stu-id="cf351-110">With the **Production Journal** window, you can perform the same tasks as in the **Output Journal** window and at the same time perform the related consumption posting tasks.</span></span> <span data-ttu-id="cf351-111">För mer information, se [Så här registrerar du förbrukning och utflöde för en utsläppt produktionsorderrad](production-how-to-register-consumption-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="cf351-111">For more information, see [Register Consumption and Output for One Released Production order line](production-how-to-register-consumption-and-output.md).</span></span>

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="cf351-112">Om du vill bokföra utflödeskvantiteter och/eller registrera körtider för en eller flera produktionsorderrader</span><span class="sxs-lookup"><span data-stu-id="cf351-112">To post output quantities and/or register run times for one or more production order lines</span></span>
1. <span data-ttu-id="cf351-113">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **utflödesjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="cf351-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="cf351-114">Fyll i fälten med data om produktionsorden och utdata och/eller körtid.</span><span class="sxs-lookup"><span data-stu-id="cf351-114">Fill in the fields with the production order data and the output data and/or run time.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    <span data-ttu-id="cf351-115">Du kan använda funktionen expandera **Expandera oper.följd** när du vill generera journalrader från produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="cf351-115">You can use the **Explode Routing** function to generate journal lines from production orders.</span></span>
  
4. <span data-ttu-id="cf351-116">Om operationen har slutförts, välj fältet **FÄRDIG**.</span><span class="sxs-lookup"><span data-stu-id="cf351-116">If the operation has been completed, select the **Finished** field.</span></span>  
5. <span data-ttu-id="cf351-117">Välj åtgärden **Bokför** om du vill bokföra operationer.</span><span class="sxs-lookup"><span data-stu-id="cf351-117">Choose the **Post** action to post the operations.</span></span> 
 
<span data-ttu-id="cf351-118">Kapacitetstransaktioner uppdateras för de använda produktions- eller maskingrupperna med information om tid och kvantitet av produktion och kassation.</span><span class="sxs-lookup"><span data-stu-id="cf351-118">Capacity ledger entries are updated for the used work or machine centers with information about time and quantity of output and scrap.</span></span> <span data-ttu-id="cf351-119">Om du har bokfört den sista operationen kommer artikeln att läggas till i lagret.</span><span class="sxs-lookup"><span data-stu-id="cf351-119">If you posted the last operation, the item will be added to the inventory.</span></span> 

## <a name="see-also"></a><span data-ttu-id="cf351-120">Se även</span><span class="sxs-lookup"><span data-stu-id="cf351-120">See Also</span></span>  
<span data-ttu-id="cf351-121">[Bokföra kassation manuellt](production-how-to-post-scrap.md)
[Återför utflödesbokföring](production-how-to-reverse-output-posting.md)
[Tillverkning](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="cf351-121">[Post Scrap Manually](production-how-to-post-scrap.md)
[Reverse Output Posting](production-how-to-reverse-output-posting.md)
[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="cf351-122">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="cf351-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="cf351-123">[Planerad](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="cf351-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="cf351-124">Lager</span><span class="sxs-lookup"><span data-stu-id="cf351-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="cf351-125">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf351-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
