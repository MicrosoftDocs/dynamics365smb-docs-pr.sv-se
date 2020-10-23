---
title: Organisera i kategorier | Microsoft Docs
description: För att söka efter och hitta objekt ska du tilldela artikelattribut och ordna objekt i kategorier.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a5698746fe52ff7ff6ca38e1207f09ded0742c96
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914115"
---
# <a name="categorize-items"></a><span data-ttu-id="23bbb-103">Kategorisera artiklar</span><span class="sxs-lookup"><span data-stu-id="23bbb-103">Categorize Items</span></span>

<span data-ttu-id="23bbb-104">För att underhålla en översikt över dina artiklar och för att sortera och söka artiklar är det praktiskt att ordna artiklarna i artikelkategorier.</span><span class="sxs-lookup"><span data-stu-id="23bbb-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="23bbb-105">Om du vill söka artiklar efter egenskaper kan du tilldela objektattribut till artiklar och även till artikelkategorier.</span><span class="sxs-lookup"><span data-stu-id="23bbb-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="23bbb-106">Mer information finns i [Så här arbetar du med attribut](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="23bbb-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a><span data-ttu-id="23bbb-107">Så här skapar du ett artikelkategori</span><span class="sxs-lookup"><span data-stu-id="23bbb-107">To create an item category</span></span>
1. <span data-ttu-id="23bbb-108">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artikelkategorier** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="23bbb-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="23bbb-109">På sidan **Artikelkategorier** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="23bbb-109">On the **Item Categories** page, choose the **New** action.</span></span>
3. <span data-ttu-id="23bbb-110">På sidan**Artikelkategori** på snabbfliken **Allmänt** fyller du sedan de fält som behövs.</span><span class="sxs-lookup"><span data-stu-id="23bbb-110">On the **Item Category Card** page, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="23bbb-111">På snabbfliken **Attribut** anger du ett artikelattribut för artikelkategorin.</span><span class="sxs-lookup"><span data-stu-id="23bbb-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="23bbb-112">Mer information finns i avsnittet [Att tilldela attribut till artikelattribut](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span><span class="sxs-lookup"><span data-stu-id="23bbb-112">For more information, see [To assign item attributes to item categories](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span></span>

> [!NOTE]  
> <span data-ttu-id="23bbb-113">Om artikelkategorin har en överordnad artikelkategori som indikeras i fältet **Överordnad kategori** kommer alla artikelattribut, som har tilldelats den överordnade artikelkategorin att förifyllas på snabbfliken **Attribut**.</span><span class="sxs-lookup"><span data-stu-id="23bbb-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
> <span data-ttu-id="23bbb-114">Artikelattribut som du tilldelar en artikelkategori, kommer automatiskt att gälla för den artikel som artikelkategorin tilldelats.</span><span class="sxs-lookup"><span data-stu-id="23bbb-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

<span data-ttu-id="23bbb-115">Om du ändrar dig om en artikelkategori kan du ta bort den.</span><span class="sxs-lookup"><span data-stu-id="23bbb-115">If you change your mind about an item category, you can delete it.</span></span> <span data-ttu-id="23bbb-116">Om en artikel redan har tilldelats måste du dock ta bort tilldelningen innan du kan ta bort artikelkategorin.</span><span class="sxs-lookup"><span data-stu-id="23bbb-116">However, if it has already been assigned to an item, you must remove that assignment before you can delete the item category.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="23bbb-117">Så här tilldelar du en artikelkategori till en artikel</span><span class="sxs-lookup"><span data-stu-id="23bbb-117">To assign an item category to an item</span></span>

1. <span data-ttu-id="23bbb-118">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="23bbb-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="23bbb-119">Öppna kortet för den artikel som du vill tilldela en en artikelkategori.</span><span class="sxs-lookup"><span data-stu-id="23bbb-119">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="23bbb-120">Välj sökknappen i fältet **Artikelkategorikod** och välj en befintlig artikelkategori.</span><span class="sxs-lookup"><span data-stu-id="23bbb-120">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="23bbb-121">Välj alternativt åtgärden **Ny** för att först skapa en ny artikelkategori som förklaras i [Att skapa en artikelkategori](inventory-how-categorize-items.md#to-create-an-item-category).</span><span class="sxs-lookup"><span data-stu-id="23bbb-121">Alternatively, choose the **New** action to first create a new item category as explained in [To create an item category](inventory-how-categorize-items.md#to-create-an-item-category).</span></span>

## <a name="categories-attributes-and-variants"></a><span data-ttu-id="23bbb-122">Kategorier, attribut och varianter</span><span class="sxs-lookup"><span data-stu-id="23bbb-122">Categories, attributes, and variants</span></span>

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a><span data-ttu-id="23bbb-123">Se även</span><span class="sxs-lookup"><span data-stu-id="23bbb-123">See Also</span></span>

[<span data-ttu-id="23bbb-124">Arbeta med artikelattribut</span><span class="sxs-lookup"><span data-stu-id="23bbb-124">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="23bbb-125">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="23bbb-125">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="23bbb-126">Lager</span><span class="sxs-lookup"><span data-stu-id="23bbb-126">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="23bbb-127">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="23bbb-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
