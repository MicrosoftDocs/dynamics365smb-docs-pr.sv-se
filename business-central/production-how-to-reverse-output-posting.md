---
title: Så här återför du en utflödesbokföring | Microsoft Docs
description: Det finns tillfällen när bokföring av utflöde måste återföras. Ett exempel på detta är om det inträffar ett informationsregistreringsfel och ett felaktigt utflödesbelopp bokförs i en produktionsorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ed275469dd172af43ceb96b85d5ac0aa99e96a2f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759048"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="df2cd-104">Återföra bokföring av utflöde</span><span class="sxs-lookup"><span data-stu-id="df2cd-104">Reverse Output Posting</span></span>
<span data-ttu-id="df2cd-105">Det finns tillfällen när bokföring av utflöde måste återföras.</span><span class="sxs-lookup"><span data-stu-id="df2cd-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="df2cd-106">Ett exempel på detta är om det inträffar ett informationsregistreringsfel och ett felaktigt utflödesbelopp bokförs i en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="df2cd-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="df2cd-107">Så här återför du en utflödesbokföring</span><span class="sxs-lookup"><span data-stu-id="df2cd-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="df2cd-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **utflödesjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="df2cd-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="df2cd-109">Välj din batch.</span><span class="sxs-lookup"><span data-stu-id="df2cd-109">Select your batch.</span></span>  
2. <span data-ttu-id="df2cd-110">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="df2cd-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="df2cd-111">Mer information finns i [Batch-bokför utflöde och körtider](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="df2cd-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="df2cd-112">I fältet **Kopplas till löpnr** väljer du den tillhörande artikeltransaktionen.</span><span class="sxs-lookup"><span data-stu-id="df2cd-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="df2cd-113">Kapaciteten och artikeltransaktionerna återförs.</span><span class="sxs-lookup"><span data-stu-id="df2cd-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="df2cd-114">Bokför återföringen genom att bokföra journalen.</span><span class="sxs-lookup"><span data-stu-id="df2cd-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="df2cd-115">Transaktionerna i utflödesjournalen bokförs som en positiv justering i artikeltransaktionen.</span><span class="sxs-lookup"><span data-stu-id="df2cd-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="df2cd-116">Se även</span><span class="sxs-lookup"><span data-stu-id="df2cd-116">See Also</span></span>  
 <span data-ttu-id="df2cd-117">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="df2cd-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="df2cd-118">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="df2cd-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="df2cd-119">[Planerad](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="df2cd-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="df2cd-120">Lager</span><span class="sxs-lookup"><span data-stu-id="df2cd-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="df2cd-121">Inköp</span><span class="sxs-lookup"><span data-stu-id="df2cd-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="df2cd-122">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="df2cd-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
