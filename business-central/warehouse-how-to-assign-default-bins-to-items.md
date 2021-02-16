---
title: 'Så här: Tilldela standardlagerställen till artiklar | Microsoft Docs'
description: Om du använder lagerställen för ett lagerställe blir det mycket enklare för dig att leverera, inleverera och flytta artiklar om du tilldelar dem standardlagerställen. När en artikel tilldelas en standardlagerplats kommer denna lagerplats att föreslås varje gång du påbörjar en transaktion för artikeln.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f3374929434876cee088f046efc6d5f950671cc8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756323"
---
# <a name="assign-default-bins-to-items"></a><span data-ttu-id="0b418-104">Tilldela standardlagerställen till artiklar</span><span class="sxs-lookup"><span data-stu-id="0b418-104">Assign Default Bins to Items</span></span>
<span data-ttu-id="0b418-105">Om du använder lagerställen för ett lagerställe blir det mycket enklare för dig att leverera, inleverera och flytta artiklar om du tilldelar dem standardlagerställen.</span><span class="sxs-lookup"><span data-stu-id="0b418-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="0b418-106">När en artikel tilldelas en standardlagerplats kommer denna lagerplats att föreslås varje gång du påbörjar en transaktion för artikeln.</span><span class="sxs-lookup"><span data-stu-id="0b418-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="0b418-107">Standardlagerställen definieras på sidan **Lagerställesinnehåll**.</span><span class="sxs-lookup"><span data-stu-id="0b418-107">Default bins are defined on the **Bin Content** page.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="0b418-108">Så här tilldelar du en standardlagerplats till en artikel</span><span class="sxs-lookup"><span data-stu-id="0b418-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="0b418-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Lagerställesinnehålluppl förslag** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="0b418-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="0b418-110">Fyll i lagerställeskoden och information om artiklar för respektive lagerplats som du vill ange som standard för en artikel.</span><span class="sxs-lookup"><span data-stu-id="0b418-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="0b418-111">Se till att välja **Standard** här fältet.</span><span class="sxs-lookup"><span data-stu-id="0b418-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="0b418-112">Välj åtgärden **Skapa lagerställesinnehåll**.</span><span class="sxs-lookup"><span data-stu-id="0b418-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="0b418-113">Din artikel tilldelas nu standardlagerställen.</span><span class="sxs-lookup"><span data-stu-id="0b418-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0b418-114">Vid införsel av artiklar som inte har tilldelats någon standardlagerplats, kommer den lagerplats där artikeln införs att anges som standardlagerplats.</span><span class="sxs-lookup"><span data-stu-id="0b418-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="0b418-115">Så här ändrar du standardlagerställen en artikel</span><span class="sxs-lookup"><span data-stu-id="0b418-115">To change the default bin for an item</span></span>  
<span data-ttu-id="0b418-116">Ibland kan det bli nödvändigt att ändra fördelningen av standardlagerplats för en viss artikel, eller tilldela en ny artikel en standardlagerplats.</span><span class="sxs-lookup"><span data-stu-id="0b418-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="0b418-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **lagerställesinnehåll** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="0b418-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0b418-118">Välj tillämplig lagerställekod i fältet **Lagerställefilter**.</span><span class="sxs-lookup"><span data-stu-id="0b418-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="0b418-119">Sök efter aktuell post för standardlagerställesinnehåll för artikeln och avmarkera kryssrutan **Standardlagerplats**.</span><span class="sxs-lookup"><span data-stu-id="0b418-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="0b418-120">Sök efter raden för lagerställesinnehåll för den lagerplats som du vill använda som ny standardlagerplats.</span><span class="sxs-lookup"><span data-stu-id="0b418-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="0b418-121">Markera kryssrutan **Standardlagerplats**.</span><span class="sxs-lookup"><span data-stu-id="0b418-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0b418-122">När en artikel införs för första gången och den inte har tilldelats någon standardlagerplats, kommer den lagerplats där artikeln införs att anges som standardlagerplats.</span><span class="sxs-lookup"><span data-stu-id="0b418-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b418-123">Se även</span><span class="sxs-lookup"><span data-stu-id="0b418-123">See Also</span></span>  
[<span data-ttu-id="0b418-124">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="0b418-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="0b418-125">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="0b418-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0b418-126">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="0b418-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="0b418-127">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="0b418-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="0b418-128">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="0b418-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="0b418-129">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0b418-129">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
