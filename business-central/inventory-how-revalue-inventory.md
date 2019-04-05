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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 7dd38fc58ed7bd2aafafa09042a9e23c821c76e4
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807268"
---
# <a name="revalue-inventory"></a><span data-ttu-id="64c49-103">Omvärdera lager</span><span class="sxs-lookup"><span data-stu-id="64c49-103">Revalue Inventory</span></span>
<span data-ttu-id="64c49-104">Om du vill öka eller minska värdet för en artikel eller en viss artikeltransaktion, använder du omvärderingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="64c49-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="64c49-105">Omvärdera lager</span><span class="sxs-lookup"><span data-stu-id="64c49-105">To revalue inventory</span></span>
1. <span data-ttu-id="64c49-106">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Omvärderingsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="64c49-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="64c49-107">Välj åtgärden **Beräkna lagervärde**.</span><span class="sxs-lookup"><span data-stu-id="64c49-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="64c49-108">På sidan **Beräkna lagervärde** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="64c49-108">On the **Calculate Inventory Value** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="64c49-109">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="64c49-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="64c49-110">På varje rad på sidan **Omvärderingsjournal** i fältet **Styckkostnad (omvärderad)** anger du den nya styckkostnaden.</span><span class="sxs-lookup"><span data-stu-id="64c49-110">On each line on the **Revaluation Journal** page, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="64c49-111">Du kan alternativt ange det nya totalbeloppet i fältet **Lagervärde (omvärderad)**.</span><span class="sxs-lookup"><span data-stu-id="64c49-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="64c49-112">Relevanta fält uppdateras automatiskt.</span><span class="sxs-lookup"><span data-stu-id="64c49-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="64c49-113">Lägg märke till att den faktiska förändringen av lagervärdet för den aktuella artikeltransaktionen visas i fältet **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="64c49-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="64c49-114">Detta belopp utgör skillnaden mellan värdena i fälten **Lagervärde (beräknat)** och **Lagervärde (omvärderat)**.</span><span class="sxs-lookup"><span data-stu-id="64c49-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="64c49-115">När du har slutfört alla rader i omvärderingsjournalen väljer du åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="64c49-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="64c49-116">Nya värdetransaktioner skapas nu för att visa omvärderingarna som du har bokfört.</span><span class="sxs-lookup"><span data-stu-id="64c49-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="64c49-117">Du kan se de nya värdena på respektive artikelkort.</span><span class="sxs-lookup"><span data-stu-id="64c49-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="64c49-118">Se även</span><span class="sxs-lookup"><span data-stu-id="64c49-118">See Also</span></span>
[<span data-ttu-id="64c49-119">Designdetaljer: Omvärdering</span><span class="sxs-lookup"><span data-stu-id="64c49-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="64c49-120">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="64c49-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="64c49-121">Försäljning</span><span class="sxs-lookup"><span data-stu-id="64c49-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="64c49-122">Inköp</span><span class="sxs-lookup"><span data-stu-id="64c49-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="64c49-123">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="64c49-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
