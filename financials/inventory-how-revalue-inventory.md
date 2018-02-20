---
title: "Skapa ny värdetransaktioner för artiklarna i lagret | Microsoft Docs"
description: "Beskriver hur du uppskattar eller skriver av värdetransaktionerna av en eller flera artiklar i lager genom att bokföra deras faktiska, beräknade värde."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8460dac8478fa101a255d93110578fa9ea20516f
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="revalue-inventory"></a><span data-ttu-id="83e78-103">Omvärdera lager</span><span class="sxs-lookup"><span data-stu-id="83e78-103">Revalue Inventory</span></span>
<span data-ttu-id="83e78-104">Om du vill öka eller minska värdet för en artikel eller en viss artikeltransaktion, använder du omvärderingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="83e78-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="83e78-105">Omvärdera lager</span><span class="sxs-lookup"><span data-stu-id="83e78-105">To revalue inventory</span></span>
1. <span data-ttu-id="83e78-106">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Omvärderingsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="83e78-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="83e78-107">Välj åtgärden **Beräkna lagervärde**.</span><span class="sxs-lookup"><span data-stu-id="83e78-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="83e78-108">I fönstret **Beräkna lagervärde** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="83e78-108">In the **Calculate Inventory Value** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="83e78-109">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="83e78-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="83e78-110">På varje rad i fönstret **Omvärderingsjournal** i fältet **Styckkostnad (omvärderad)** anger du den nya styckkostnaden.</span><span class="sxs-lookup"><span data-stu-id="83e78-110">On each line in the **Revaluation Journal** window, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="83e78-111">Du kan alternativt ange det nya totalbeloppet i fältet **Lagervärde (omvärderad)**.</span><span class="sxs-lookup"><span data-stu-id="83e78-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="83e78-112">Relevanta fält uppdateras automatiskt.</span><span class="sxs-lookup"><span data-stu-id="83e78-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="83e78-113">Lägg märke till att den faktiska förändringen av lagervärdet för den aktuella artikeltransaktionen visas i fältet **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="83e78-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="83e78-114">Detta belopp utgör skillnaden mellan värdena i fälten **Lagervärde (beräknat)** och **Lagervärde (omvärderat)**.</span><span class="sxs-lookup"><span data-stu-id="83e78-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="83e78-115">När du har slutfört alla rader i omvärderingsjournalen väljer du åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="83e78-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="83e78-116">Nya värdetransaktioner skapas nu för att visa omvärderingarna som du har bokfört.</span><span class="sxs-lookup"><span data-stu-id="83e78-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="83e78-117">Du kan se de nya värdena på respektive artikelkort.</span><span class="sxs-lookup"><span data-stu-id="83e78-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="83e78-118">Se även</span><span class="sxs-lookup"><span data-stu-id="83e78-118">See Also</span></span>
[<span data-ttu-id="83e78-119">Designdetaljer: Omvärdering</span><span class="sxs-lookup"><span data-stu-id="83e78-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="83e78-120">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="83e78-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="83e78-121">Försäljning</span><span class="sxs-lookup"><span data-stu-id="83e78-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="83e78-122">Inköp</span><span class="sxs-lookup"><span data-stu-id="83e78-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="83e78-123">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="83e78-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

