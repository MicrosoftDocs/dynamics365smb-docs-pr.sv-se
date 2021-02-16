---
title: Definiera allmänna lagerinställningar
description: Beskriver hur du definierar den allmänna lagerinställningen så att du kan hantera distributionslagret och lagret.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e3ecf8d206e50244c19a820bdb67d2992cbefe36
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746372"
---
# <a name="set-up-general-inventory-information"></a><span data-ttu-id="02b14-103">Ställa in allmän lagerinformation</span><span class="sxs-lookup"><span data-stu-id="02b14-103">Set Up General Inventory Information</span></span>

<span data-ttu-id="02b14-104">Du ställer in dina allmänna lagerinställningar på sidan **Lagerinställningar**.</span><span class="sxs-lookup"><span data-stu-id="02b14-104">You specify your general inventory setup on the **Inventory Setup** page.</span></span>

## <a name="to-set-up-general-inventory-information"></a><span data-ttu-id="02b14-105">Så här ställer du in allmän lagerinformation</span><span class="sxs-lookup"><span data-stu-id="02b14-105">To set up general inventory information</span></span>

1. <span data-ttu-id="02b14-106">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Lagerinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="02b14-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="02b14-107">På sidan **Lagerinställningar** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="02b14-107">On the **Inventory Setup** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="02b14-108">Detaljerad information om kostnadsfälten, **Automatisk kostnadsbokföring**, **Förväntad kost.bokf. i redov.** och **Standarvärderingsprincip** finns i [Stämma av lagerkostnader med redovisningen](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Designdetaljer: Lagerkostnad](design-details-inventory-costing.md) och [Designdetaljer: Bokföring av förväntad kostnad](design-details-expected-cost-posting.md).</span><span class="sxs-lookup"><span data-stu-id="02b14-108">For detailed information about the costing fields, **Automatic Cost Posting**, **Expected Cost Posting to G/L**, and **Default Costing Method**, see [Reconcile Inventory Costs with the General Ledger](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Design Details: Inventory Costing](design-details-inventory-costing.md), and [Design Details: Expected Cost Posting](design-details-expected-cost-posting.md).</span></span> <span data-ttu-id="02b14-109">Mer information om kostnadsredovisning i allmänhet finns i [Hantera lagerkostnad](finance-manage-inventory-costs.md).</span><span class="sxs-lookup"><span data-stu-id="02b14-109">For more information about costing in general, see [Managing Inventory Costs](finance-manage-inventory-costs.md).</span></span>  

<span data-ttu-id="02b14-110">Om du vill ange en inkommande lagerhanteringstid som ska tas med i orderlöftesberäkningen på inköpsraden, kan du ange tiden som standard för lagret på sidan **Lagerinställning** och för lagerstället.</span><span class="sxs-lookup"><span data-stu-id="02b14-110">If you want to include warehouse handling time in the order promising calculation on the purchase line, you can set it up as a default for the inventory, on the **Inventory Setup** page, and for your location.</span></span> <span data-ttu-id="02b14-111">Mer information finns i [Så här beräknar du ett orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="02b14-111">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="02b14-112">Reglaget **Automatisk kostnadsjustering** är aktiverat som standard för att säkerställa att lagervärden alltid är korrekta i redovisningen, vilket i sin tur innebär att försäljnings- och vinststatistik är aktuell.</span><span class="sxs-lookup"><span data-stu-id="02b14-112">The **Automatic Cost Adjustment** toggle is turned on by default to ensure that inventory values are always correct in the general ledger, which in turn keeps your sales and profit statistics up to date.</span></span> <span data-ttu-id="02b14-113">Kostnadsändringar från inkommande transaktioner, t.ex. de för inköp eller produktionsutflöde tilldelas relaterade utgående transaktioner, t.ex. försäljningar eller överföringar.</span><span class="sxs-lookup"><span data-stu-id="02b14-113">Cost changes from inbound entries, such as those for purchases or production output, are assigned to the related outbound entries, such as sales or transfers.</span></span> <span data-ttu-id="02b14-114">Detta är användbart för nya [!INCLUDE[prod_short](includes/prod_short.md)]-kunder och mindre företag med relativt låga lagertransaktionsnivåer.</span><span class="sxs-lookup"><span data-stu-id="02b14-114">This is helpful for new [!INCLUDE[prod_short](includes/prod_short.md)] customers and small businesses with relatively low inventory transaction levels.</span></span> <span data-ttu-id="02b14-115">När företaget växer och lagernivåerna ökar kan detta emellertid sakta ner systemets prestanda.</span><span class="sxs-lookup"><span data-stu-id="02b14-115">However, as a business grows and inventory levels increase, this can slow down system performance.</span></span> <span data-ttu-id="02b14-116">Om du vill förhindra att prestandan vid bokföringen försämras väljer du ett tidsalternativ för att definiera hur långt tillbaka i tiden från arbetsdatumet som en inkommande transaktion kan inträffa för att eventuellt utlösa justeringar av relaterade utgående värdetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="02b14-116">To minimize reduced performance during posting, select a time option to define how far back in time from the work date an inbound transaction can occur to potentially trigger adjustment of related outbound value entries.</span></span> <span data-ttu-id="02b14-117">Du kan också justera kostnader manuellt med jämna mellanrum med batch-jobbet Justera kost.-artikeltrans.</span><span class="sxs-lookup"><span data-stu-id="02b14-117">Alternatively, you can manually adjust costs at regular intervals with the Adjust Cost - Item Entries batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="02b14-118">Se även</span><span class="sxs-lookup"><span data-stu-id="02b14-118">See Also</span></span>
[<span data-ttu-id="02b14-119">Lagerinställning</span><span class="sxs-lookup"><span data-stu-id="02b14-119">Set Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="02b14-120">[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)  </span><span class="sxs-lookup"><span data-stu-id="02b14-120">[Design Details: Costing Methods](design-details-costing-methods.md)  </span></span>  
[<span data-ttu-id="02b14-121">Hantera lager</span><span class="sxs-lookup"><span data-stu-id="02b14-121">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="02b14-122">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="02b14-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="02b14-123">Ändra vilka funktioner som visas</span><span class="sxs-lookup"><span data-stu-id="02b14-123">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="02b14-124">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="02b14-124">General Business Functionality</span></span>](ui-across-business-areas.md)
