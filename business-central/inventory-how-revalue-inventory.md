---
title: Skapa ny värdetransaktioner för artiklarna i lagret | Microsoft Docs
description: Beskriver hur du uppskattar eller skriver av värdetransaktionerna av en eller flera artiklar i lager genom att bokföra deras faktiska, beräknade värde.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b29e93d248e939eb9eb1cea97e53cd1718304e80
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923801"
---
# <a name="revalue-inventory"></a><span data-ttu-id="b3393-103">Omvärdera lager</span><span class="sxs-lookup"><span data-stu-id="b3393-103">Revalue Inventory</span></span>
<span data-ttu-id="b3393-104">Om du vill öka eller minska värdet för en artikel eller en viss artikeltransaktion, använder du omvärderingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="b3393-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="b3393-105">Omvärdera lager</span><span class="sxs-lookup"><span data-stu-id="b3393-105">To revalue inventory</span></span>
1. <span data-ttu-id="b3393-106">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Omvärderingsjournal** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="b3393-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="b3393-107">Välj åtgärden **Beräkna lagervärde**.</span><span class="sxs-lookup"><span data-stu-id="b3393-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="b3393-108">På sidan **Beräkna lagervärde** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="b3393-108">On the **Calculate Inventory Value** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="b3393-109">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3393-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="b3393-110">På varje rad på sidan **Omvärderingsjournal** i fältet **Styckkostnad (omvärderad)** anger du den nya styckkostnaden.</span><span class="sxs-lookup"><span data-stu-id="b3393-110">On each line on the **Revaluation Journal** page, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="b3393-111">Du kan alternativt ange det nya totalbeloppet i fältet **Lagervärde (omvärderad)**.</span><span class="sxs-lookup"><span data-stu-id="b3393-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="b3393-112">Relevanta fält uppdateras automatiskt.</span><span class="sxs-lookup"><span data-stu-id="b3393-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="b3393-113">Lägg märke till att den faktiska förändringen av lagervärdet för den aktuella artikeltransaktionen visas i fältet **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="b3393-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="b3393-114">Detta belopp utgör skillnaden mellan värdena i fälten **Lagervärde (beräknat)** och **Lagervärde (omvärderat)**.</span><span class="sxs-lookup"><span data-stu-id="b3393-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="b3393-115">När du har slutfört alla rader i omvärderingsjournalen väljer du åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="b3393-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="b3393-116">Nya värdetransaktioner skapas nu för att visa omvärderingarna som du har bokfört.</span><span class="sxs-lookup"><span data-stu-id="b3393-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="b3393-117">Du kan se de nya värdena på respektive artikelkort.</span><span class="sxs-lookup"><span data-stu-id="b3393-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3393-118">Se även</span><span class="sxs-lookup"><span data-stu-id="b3393-118">See Also</span></span>
[<span data-ttu-id="b3393-119">Designdetaljer: Omvärdering</span><span class="sxs-lookup"><span data-stu-id="b3393-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="b3393-120">Lager</span><span class="sxs-lookup"><span data-stu-id="b3393-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b3393-121">Försäljning</span><span class="sxs-lookup"><span data-stu-id="b3393-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="b3393-122">Inköp</span><span class="sxs-lookup"><span data-stu-id="b3393-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="b3393-123">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b3393-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
