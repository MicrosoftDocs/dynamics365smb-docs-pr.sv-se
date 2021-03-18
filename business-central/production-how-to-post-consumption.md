---
title: 'Så här: batch-bokföra förbrukning | Microsoft Docs'
description: Om bokföringsmetoden är **Manuell**, måste du bokföra komponenterna manuellt med hjälp av en förbrukningsjournaler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0bf0a92d05b6c9ecb3d5a5ba054b4675680ad43c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391805"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="af752-103">Batch-bokföra produktionsförbrukning</span><span class="sxs-lookup"><span data-stu-id="af752-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="af752-104">Om bokföringsmetoden är **Manuell** måste du bokföra komponenterna manuellt med hjälp av en förbrukningsjournaler.</span><span class="sxs-lookup"><span data-stu-id="af752-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="af752-105">Du kan också ställa in systemet att automatiskt bokföra (*bokföra*) komponenter när du startar eller färdigställer produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="af752-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="af752-106">Mer information finns i [Tillåta bokföring av komponenter enligt operationens utflöde](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="af752-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="af752-107">Om du vill bokföra förbrukning för produktion av en eller flera rader</span><span class="sxs-lookup"><span data-stu-id="af752-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="af752-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **förbrukningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="af752-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="af752-109">Fyll i fälten med data om produktionsorden och om förbrukningen.</span><span class="sxs-lookup"><span data-stu-id="af752-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="af752-110">Om distributionslagret där komponenterna lagras har konfigurerats till att använda lagerställen men inte kräva bearbetning av plockning, kopplar du en lagerställeskod till journalraden för att ange var artiklarna ska tas från i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="af752-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="af752-111">Mer information finns i [Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="af752-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="af752-112">Välj åtgärden **Bokför** om du vill bokföra förbrukningen.</span><span class="sxs-lookup"><span data-stu-id="af752-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="af752-113">De associerade artikeltransaktionerna misnkas.</span><span class="sxs-lookup"><span data-stu-id="af752-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="af752-114">Se även</span><span class="sxs-lookup"><span data-stu-id="af752-114">See Also</span></span>  
<span data-ttu-id="af752-115">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="af752-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="af752-116">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="af752-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="af752-117">[Planerad](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="af752-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="af752-118">Lager</span><span class="sxs-lookup"><span data-stu-id="af752-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="af752-119">Inköp</span><span class="sxs-lookup"><span data-stu-id="af752-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="af752-120">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af752-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]