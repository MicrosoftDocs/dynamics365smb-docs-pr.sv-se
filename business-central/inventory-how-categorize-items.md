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
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f7f40054c511b5f3bf1d61dc40d6107cc717dcd8
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="categorize-items"></a><span data-ttu-id="81a4c-103">Kategorisera artiklar</span><span class="sxs-lookup"><span data-stu-id="81a4c-103">Categorize Items</span></span>
<span data-ttu-id="81a4c-104">För att underhålla en översikt över dina artiklar och för att sortera och söka artiklar är det praktiskt att ordna artiklarna i artikelkategorier.</span><span class="sxs-lookup"><span data-stu-id="81a4c-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="81a4c-105">Om du vill söka artiklar efter egenskaper kan du tilldela objektattribut till artiklar och även till artikelkategorier.</span><span class="sxs-lookup"><span data-stu-id="81a4c-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="81a4c-106">Mer information finns i [Så här arbetar du med attribut](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="81a4c-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="81a4c-107">Så här skapar du ett artikelkategori</span><span class="sxs-lookup"><span data-stu-id="81a4c-107">To create an item category</span></span>
1. <span data-ttu-id="81a4c-108">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Artikelkategorier** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="81a4c-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="81a4c-109">I fönstret **Artikelkategorier** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="81a4c-109">In the **Item Categories** window, choose the **New** action.</span></span>
3. <span data-ttu-id="81a4c-110">I fönstret**Artikelkategori** på snabbfliken **Allmänt** fyller du sedan de fält som behövs.</span><span class="sxs-lookup"><span data-stu-id="81a4c-110">In the **Item Category Card** window, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="81a4c-111">På snabbfliken **Attribut** anger du ett artikelattribut för artikelkategorin.</span><span class="sxs-lookup"><span data-stu-id="81a4c-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="81a4c-112">För mer information, se avsnittet "Tilldela artikelattribut till en artikelkategori" i [Så här arbetar du med artikelattribut](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="81a4c-112">For more information, see the "To assign item attributes to an item category" section in [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="81a4c-113">Om artikelkategorin har en överordnad artikelkategori som indikeras i fältet **Överordnad kategori** kommer alla artikelattribut, som har tilldelats den överordnade artikelkategorin att förifyllas på snabbfliken **Attribut**.</span><span class="sxs-lookup"><span data-stu-id="81a4c-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="81a4c-114">Artikelattribut som du tilldelar en artikelkategori, kommer automatiskt att gälla för den artikel som artikelkategorin tilldelats.</span><span class="sxs-lookup"><span data-stu-id="81a4c-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="81a4c-115">Så här tilldelar du en artikelkategori till en artikel</span><span class="sxs-lookup"><span data-stu-id="81a4c-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="81a4c-116">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="81a4c-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="81a4c-117">Öppna kortet för den artikel som du vill tilldela en en artikelkategori.</span><span class="sxs-lookup"><span data-stu-id="81a4c-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="81a4c-118">Välj sökknappen i fältet **Artikelkategorikod** och välj en befintlig artikelkategori.</span><span class="sxs-lookup"><span data-stu-id="81a4c-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="81a4c-119">Välj alternativt åtgärden **Ny** för att först skapa en ny artikelkategori som förklaras i avsnittet "Att skapa en artikelkategori".</span><span class="sxs-lookup"><span data-stu-id="81a4c-119">Alternatively, choose the **New** action to first create a new item category as explained in the "To create an item category" section.</span></span>

## <a name="see-also"></a><span data-ttu-id="81a4c-120">Se även</span><span class="sxs-lookup"><span data-stu-id="81a4c-120">See Also</span></span>
[<span data-ttu-id="81a4c-121">Arbeta med artikelattribut</span><span class="sxs-lookup"><span data-stu-id="81a4c-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="81a4c-122">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="81a4c-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="81a4c-123">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="81a4c-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="81a4c-124">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="81a4c-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
