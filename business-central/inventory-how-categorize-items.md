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
ms.date: 06/22/2020
ms.author: sgroespe
ms.openlocfilehash: 206a7bcfe9152102dffbb9b2653c273dc8a27cdd
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528569"
---
# <a name="categorize-items"></a><span data-ttu-id="b959c-103">Kategorisera artiklar</span><span class="sxs-lookup"><span data-stu-id="b959c-103">Categorize Items</span></span>

<span data-ttu-id="b959c-104">För att underhålla en översikt över dina artiklar och för att sortera och söka artiklar är det praktiskt att ordna artiklarna i artikelkategorier.</span><span class="sxs-lookup"><span data-stu-id="b959c-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="b959c-105">Om du vill söka artiklar efter egenskaper kan du tilldela objektattribut till artiklar och även till artikelkategorier.</span><span class="sxs-lookup"><span data-stu-id="b959c-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="b959c-106">Mer information finns i [Så här arbetar du med attribut](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b959c-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a><span data-ttu-id="b959c-107">Så här skapar du ett artikelkategori</span><span class="sxs-lookup"><span data-stu-id="b959c-107">To create an item category</span></span>
1. <span data-ttu-id="b959c-108">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artikelkategorier** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b959c-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="b959c-109">På sidan **Artikelkategorier** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b959c-109">On the **Item Categories** page, choose the **New** action.</span></span>
3. <span data-ttu-id="b959c-110">På sidan**Artikelkategori** på snabbfliken **Allmänt** fyller du sedan de fält som behövs.</span><span class="sxs-lookup"><span data-stu-id="b959c-110">On the **Item Category Card** page, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="b959c-111">På snabbfliken **Attribut** anger du ett artikelattribut för artikelkategorin.</span><span class="sxs-lookup"><span data-stu-id="b959c-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="b959c-112">Mer information finns i avsnittet [Att tilldela attribut till artikelattribut](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span><span class="sxs-lookup"><span data-stu-id="b959c-112">For more information, see [To assign item attributes to item categories](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span></span>

> [!NOTE]  
> <span data-ttu-id="b959c-113">Om artikelkategorin har en överordnad artikelkategori som indikeras i fältet **Överordnad kategori** kommer alla artikelattribut, som har tilldelats den överordnade artikelkategorin att förifyllas på snabbfliken **Attribut**.</span><span class="sxs-lookup"><span data-stu-id="b959c-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
> <span data-ttu-id="b959c-114">Artikelattribut som du tilldelar en artikelkategori, kommer automatiskt att gälla för den artikel som artikelkategorin tilldelats.</span><span class="sxs-lookup"><span data-stu-id="b959c-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="b959c-115">Så här tilldelar du en artikelkategori till en artikel</span><span class="sxs-lookup"><span data-stu-id="b959c-115">To assign an item category to an item</span></span>

1. <span data-ttu-id="b959c-116">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b959c-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="b959c-117">Öppna kortet för den artikel som du vill tilldela en en artikelkategori.</span><span class="sxs-lookup"><span data-stu-id="b959c-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="b959c-118">Välj sökknappen i fältet **Artikelkategorikod** och välj en befintlig artikelkategori.</span><span class="sxs-lookup"><span data-stu-id="b959c-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="b959c-119">Välj alternativt åtgärden **Ny** för att först skapa en ny artikelkategori som förklaras i [Att skapa en artikelkategori](inventory-how-categorize-items.md#to-create-an-item-category).</span><span class="sxs-lookup"><span data-stu-id="b959c-119">Alternatively, choose the **New** action to first create a new item category as explained in [To create an item category](inventory-how-categorize-items.md#to-create-an-item-category).</span></span>

## <a name="categories-attributes-and-variants"></a><span data-ttu-id="b959c-120">Kategorier, attribut och varianter</span><span class="sxs-lookup"><span data-stu-id="b959c-120">Categories, attributes, and variants</span></span>

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a><span data-ttu-id="b959c-121">Se även</span><span class="sxs-lookup"><span data-stu-id="b959c-121">See Also</span></span>

[<span data-ttu-id="b959c-122">Arbeta med artikelattribut</span><span class="sxs-lookup"><span data-stu-id="b959c-122">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="b959c-123">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="b959c-123">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="b959c-124">Lager</span><span class="sxs-lookup"><span data-stu-id="b959c-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b959c-125">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b959c-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
