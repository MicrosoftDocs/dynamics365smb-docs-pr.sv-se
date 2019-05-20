---
title: 'Så här: Tilldela standardlagerplatser till artiklar | Microsoft Docs'
description: Om du använder lagerplatser för ett lagerställe blir det mycket enklare för dig att leverera, inleverera och flytta artiklar om du tilldelar dem standardlagerplatser. När en artikel tilldelas en standardlagerplats kommer denna lagerplats att föreslås varje gång du påbörjar en transaktion för artikeln.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0eb6dc74d9ac050c692c003799c3142bdbdaeeaa
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248761"
---
# <a name="assign-default-bins-to-items"></a><span data-ttu-id="09054-104">Tilldela standardlagerplatser till artiklar</span><span class="sxs-lookup"><span data-stu-id="09054-104">Assign Default Bins to Items</span></span>
<span data-ttu-id="09054-105">Om du använder lagerplatser för ett lagerställe blir det mycket enklare för dig att leverera, inleverera och flytta artiklar om du tilldelar dem standardlagerplatser.</span><span class="sxs-lookup"><span data-stu-id="09054-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="09054-106">När en artikel tilldelas en standardlagerplats kommer denna lagerplats att föreslås varje gång du påbörjar en transaktion för artikeln.</span><span class="sxs-lookup"><span data-stu-id="09054-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="09054-107">Standardlagerplatser definieras på sidan **Lagerplatsinnehåll**.</span><span class="sxs-lookup"><span data-stu-id="09054-107">Default bins are defined on the **Bin Content** page.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="09054-108">Så här tilldelar du en standardlagerplats till en artikel</span><span class="sxs-lookup"><span data-stu-id="09054-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="09054-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lagerplatsinnehålluppl förslag** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="09054-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="09054-110">Fyll i lagerplatskoden och information om artiklar för respektive lagerplats som du vill ange som standard för en artikel.</span><span class="sxs-lookup"><span data-stu-id="09054-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="09054-111">Se till att välja **Standard** här fältet.</span><span class="sxs-lookup"><span data-stu-id="09054-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="09054-112">Välj åtgärden **Skapa lagerplatsinnehåll**.</span><span class="sxs-lookup"><span data-stu-id="09054-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="09054-113">Din artikel tilldelas nu standardlagerplatser.</span><span class="sxs-lookup"><span data-stu-id="09054-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="09054-114">Vid införsel av artiklar som inte har tilldelats någon standardlagerplats, kommer den lagerplats där artikeln införs att anges som standardlagerplats.</span><span class="sxs-lookup"><span data-stu-id="09054-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="09054-115">Så här ändrar du standardlagerplatser en artikel</span><span class="sxs-lookup"><span data-stu-id="09054-115">To change the default bin for an item</span></span>  
<span data-ttu-id="09054-116">Ibland kan det bli nödvändigt att ändra fördelningen av standardlagerplats för en viss artikel, eller tilldela en ny artikel en standardlagerplats.</span><span class="sxs-lookup"><span data-stu-id="09054-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="09054-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lagerplatsinnehåll** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="09054-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="09054-118">Välj tillämplig lagerställekod i fältet **Lagerställefilter**.</span><span class="sxs-lookup"><span data-stu-id="09054-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="09054-119">Sök efter aktuell post för standardlagerplatsinnehåll för artikeln och avmarkera kryssrutan **Standardlagerplats**.</span><span class="sxs-lookup"><span data-stu-id="09054-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="09054-120">Sök efter raden för lagerplatsinnehåll för den lagerplats som du vill använda som ny standardlagerplats.</span><span class="sxs-lookup"><span data-stu-id="09054-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="09054-121">Markera kryssrutan **Standardlagerplats**.</span><span class="sxs-lookup"><span data-stu-id="09054-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="09054-122">När en artikel införs för första gången och den inte har tilldelats någon standardlagerplats, kommer den lagerplats där artikeln införs att anges som standardlagerplats.</span><span class="sxs-lookup"><span data-stu-id="09054-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="09054-123">Se även</span><span class="sxs-lookup"><span data-stu-id="09054-123">See Also</span></span>  
[<span data-ttu-id="09054-124">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="09054-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="09054-125">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="09054-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="09054-126">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="09054-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="09054-127">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="09054-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="09054-128">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="09054-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="09054-129">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="09054-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
