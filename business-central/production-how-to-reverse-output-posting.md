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
ms.openlocfilehash: b33b0642d8cee6e26edeeece47c8fceb72c2bfa1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921573"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="99ff5-104">Återföra bokföring av utflöde</span><span class="sxs-lookup"><span data-stu-id="99ff5-104">Reverse Output Posting</span></span>
<span data-ttu-id="99ff5-105">Det finns tillfällen när bokföring av utflöde måste återföras.</span><span class="sxs-lookup"><span data-stu-id="99ff5-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="99ff5-106">Ett exempel på detta är om det inträffar ett informationsregistreringsfel och ett felaktigt utflödesbelopp bokförs i en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="99ff5-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="99ff5-107">Så här återför du en utflödesbokföring</span><span class="sxs-lookup"><span data-stu-id="99ff5-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="99ff5-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **utflödesjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="99ff5-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="99ff5-109">Välj din batch.</span><span class="sxs-lookup"><span data-stu-id="99ff5-109">Select your batch.</span></span>  
2. <span data-ttu-id="99ff5-110">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="99ff5-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="99ff5-111">Mer information finns i [Batch-bokför utflöde och körtider](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="99ff5-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="99ff5-112">I fältet **Kopplas till löpnr** väljer du den tillhörande artikeltransaktionen.</span><span class="sxs-lookup"><span data-stu-id="99ff5-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="99ff5-113">Kapaciteten och artikeltransaktionerna återförs.</span><span class="sxs-lookup"><span data-stu-id="99ff5-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="99ff5-114">Bokför återföringen genom att bokföra journalen.</span><span class="sxs-lookup"><span data-stu-id="99ff5-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="99ff5-115">Transaktionerna i utflödesjournalen bokförs som en positiv justering i artikeltransaktionen.</span><span class="sxs-lookup"><span data-stu-id="99ff5-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="99ff5-116">Se även</span><span class="sxs-lookup"><span data-stu-id="99ff5-116">See Also</span></span>  
 <span data-ttu-id="99ff5-117">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="99ff5-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="99ff5-118">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="99ff5-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="99ff5-119">[Planerad](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="99ff5-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="99ff5-120">Lager</span><span class="sxs-lookup"><span data-stu-id="99ff5-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="99ff5-121">Inköp</span><span class="sxs-lookup"><span data-stu-id="99ff5-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="99ff5-122">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="99ff5-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
