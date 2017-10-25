---
title: "Så här: batch-bokföra förbrukning | Microsoft Docs"
description: "Om bokföringsmetoden är **manuell** måste du bokföra komponenterna manuellt med hjälp av förbrukningsjournalerna."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 29e85f5264f007db3712d4f6227d689b2a3de926
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-batch-post-production-consumption"></a><span data-ttu-id="6d032-103">Så här: batch-bokföra förbrukning</span><span class="sxs-lookup"><span data-stu-id="6d032-103">How to: Batch Post Production Consumption</span></span>
<span data-ttu-id="6d032-104">Om bokföringsmetoden är **Manuell**, måste du bokföra komponenterna manuellt med hjälp av en förbrukningsjournaler.</span><span class="sxs-lookup"><span data-stu-id="6d032-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="6d032-105">Du kan också ställa in systemet att automatiskt bokföra (*bokföra*) komponenter när du startar eller färdigställer produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="6d032-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="6d032-106">Mer information finns i [Tillåta bokföring av komponenter enligt operationens utflöde](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="6d032-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="6d032-107">Om du vill bokföra förbrukning för produktion av en eller flera rader</span><span class="sxs-lookup"><span data-stu-id="6d032-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="6d032-108">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Förbrukningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="6d032-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6d032-109">Fyll i fälten med data om produktionsorden och om förbrukningen.</span><span class="sxs-lookup"><span data-stu-id="6d032-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="6d032-110">Om distributionslagret där komponenterna lagras har konfigurerats till att använda lagerplatser men inte kräva bearbetning av plockning, kopplar du en lagerplatskod till journalraden för att ange var artiklarna ska tas från i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="6d032-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="6d032-111">Mer information finnsi [Så här: Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="6d032-111">For more information, see [How to: Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="6d032-112">Välj åtgärden **Bokför** om du vill bokföra förbrukningen.</span><span class="sxs-lookup"><span data-stu-id="6d032-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="6d032-113">De associerade artikeltransaktionerna misnkas.</span><span class="sxs-lookup"><span data-stu-id="6d032-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d032-114">Se även</span><span class="sxs-lookup"><span data-stu-id="6d032-114">See Also</span></span>  
<span data-ttu-id="6d032-115">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="6d032-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="6d032-116">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="6d032-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="6d032-117">[Planerad](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="6d032-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="6d032-118">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="6d032-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="6d032-119">Inköp</span><span class="sxs-lookup"><span data-stu-id="6d032-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="6d032-120">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6d032-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
