---
title: Organisera i kategorier | Microsoft Docs
description: "För att söka efter och hitta objekt ska du tilldela artikelattribut och ordna objekt i kategorier."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5b684df40599a730054e333f1bdf2e526c840e0b
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="categorize-items"></a><span data-ttu-id="cf897-103">Kategorisera artiklar</span><span class="sxs-lookup"><span data-stu-id="cf897-103">Categorize Items</span></span>
<span data-ttu-id="cf897-104">För att underhålla en översikt över dina artiklar och för att sortera och söka artiklar är det praktiskt att ordna artiklarna i artikelkategorier.</span><span class="sxs-lookup"><span data-stu-id="cf897-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="cf897-105">Om du vill söka artiklar efter egenskaper kan du tilldela objektattribut till artiklar och även till artikelkategorier.</span><span class="sxs-lookup"><span data-stu-id="cf897-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="cf897-106">Mer information finns i [Så här arbetar du med attribut](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="cf897-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="cf897-107">Så här skapar du ett artikelkategori</span><span class="sxs-lookup"><span data-stu-id="cf897-107">To create an item category</span></span>
1. <span data-ttu-id="cf897-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artikelkategorier** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="cf897-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="cf897-109">På sidan **Artikelkategorier** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cf897-109">On the **Item Categories** page, choose the **New** action.</span></span>
3. <span data-ttu-id="cf897-110">På sidan**Artikelkategori** på snabbfliken **Allmänt** fyller du sedan de fält som behövs.</span><span class="sxs-lookup"><span data-stu-id="cf897-110">On the **Item Category Card** page, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="cf897-111">På snabbfliken **Attribut** anger du ett artikelattribut för artikelkategorin.</span><span class="sxs-lookup"><span data-stu-id="cf897-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="cf897-112">För mer information, se avsnittet "Tilldela artikelattribut till en artikelkategori" i [Så här arbetar du med artikelattribut](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="cf897-112">For more information, see the "To assign item attributes to an item category" section in [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="cf897-113">Om artikelkategorin har en överordnad artikelkategori som indikeras i fältet **Överordnad kategori** kommer alla artikelattribut, som har tilldelats den överordnade artikelkategorin att förifyllas på snabbfliken **Attribut**.</span><span class="sxs-lookup"><span data-stu-id="cf897-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="cf897-114">Artikelattribut som du tilldelar en artikelkategori, kommer automatiskt att gälla för den artikel som artikelkategorin tilldelats.</span><span class="sxs-lookup"><span data-stu-id="cf897-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="cf897-115">Så här tilldelar du en artikelkategori till en artikel</span><span class="sxs-lookup"><span data-stu-id="cf897-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="cf897-116">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="cf897-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="cf897-117">Öppna kortet för den artikel som du vill tilldela en en artikelkategori.</span><span class="sxs-lookup"><span data-stu-id="cf897-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="cf897-118">Välj sökknappen i fältet **Artikelkategorikod** och välj en befintlig artikelkategori.</span><span class="sxs-lookup"><span data-stu-id="cf897-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="cf897-119">Välj alternativt åtgärden **Ny** för att först skapa en ny artikelkategori som förklaras i avsnittet "Att skapa en artikelkategori".</span><span class="sxs-lookup"><span data-stu-id="cf897-119">Alternatively, choose the **New** action to first create a new item category as explained in the "To create an item category" section.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf897-120">Se även</span><span class="sxs-lookup"><span data-stu-id="cf897-120">See Also</span></span>
[<span data-ttu-id="cf897-121">Arbeta med artikelattribut</span><span class="sxs-lookup"><span data-stu-id="cf897-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="cf897-122">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="cf897-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="cf897-123">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="cf897-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="cf897-124">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf897-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

