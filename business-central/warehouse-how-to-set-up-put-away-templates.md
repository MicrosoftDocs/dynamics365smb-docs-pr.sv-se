---
title: Så här skapar du artikelinförselmallar | Microsoft Docs
description: Med dirigerad artikelinförsel och plockning går det alltid att hitta den lämpligaste lagerplatsen för artiklarna enligt den artikelinförselmall som du har skapat för distributionslagret, de lagerplatsordningar som du har angett för lagerplatserna samt de lägsta och högsta antal som du har definierat för de fasta lagerplatserna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2020
ms.author: sgroespe
ms.openlocfilehash: 46dc891937ec4046a0403ca418296d1d7ee24a99
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529319"
---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="5d576-103">Skapa artikelinförselmallar</span><span class="sxs-lookup"><span data-stu-id="5d576-103">Set Up Put-away Templates</span></span>

<span data-ttu-id="5d576-104">Med dirigerad artikelinförsel och plockning går det alltid att hitta den lämpligaste lagerplatsen för artiklarna enligt den artikelinförselmall som du har skapat för distributionslagret, de lagerplatsordningar som du har angett för lagerplatserna samt de lägsta och högsta antal som du har definierat för de fasta lagerplatserna.</span><span class="sxs-lookup"><span data-stu-id="5d576-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="5d576-105">Du kan skapa flera artikelinförselmallar och välja en av dem för att styra allmänna artikelinförslar i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="5d576-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="5d576-106">Du kan även välja en artikelinförselmall för valfri artikel eller lagerställeenhet som kan ha specialkrav beträffande artikelinförsel.</span><span class="sxs-lookup"><span data-stu-id="5d576-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="5d576-107">Så här skapar du artikelinförselmallar:</span><span class="sxs-lookup"><span data-stu-id="5d576-107">To set up put-away templates</span></span>

1. <span data-ttu-id="5d576-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **artikelinförselmallar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5d576-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5d576-109">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5d576-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="5d576-110">Ange en kod som är unik för den mall som du ska skapa.</span><span class="sxs-lookup"><span data-stu-id="5d576-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4. <span data-ttu-id="5d576-111">Ange vid behov en kort beskrivning.</span><span class="sxs-lookup"><span data-stu-id="5d576-111">Enter a short description, if you wish.</span></span>  
5. <span data-ttu-id="5d576-112">Fyll i den första raden med de lagerplatskrav som du vill ska uppfyllas först och främst när en artikelinförsel föreslås.</span><span class="sxs-lookup"><span data-stu-id="5d576-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>

    <span data-ttu-id="5d576-113">Om du till exempel vill att standard artikelinförselmetoden ska baseras på fasta lagerplatser väljer du fältet **Sök fast lagerplats**.</span><span class="sxs-lookup"><span data-stu-id="5d576-113">For example, if want the default put-away method to be based on fixed bins, then choose the **Find Fixed Bin** field.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="5d576-114">Fyll i den andra raden med de lagerplatskrav som ska gälla i andra hand vid artikelinförsel till en lagerplats.</span><span class="sxs-lookup"><span data-stu-id="5d576-114">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="5d576-115">Den andra raden används endast om det inte går att hitta en lagerplats som uppfyller kraven på den första raden.</span><span class="sxs-lookup"><span data-stu-id="5d576-115">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7. <span data-ttu-id="5d576-116">Fortsätt att fylla i raderna tills du har beskrivit alla godtagbara lagerplatsplaceringar som du vill använda vid artikelinförsel.</span><span class="sxs-lookup"><span data-stu-id="5d576-116">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8. <span data-ttu-id="5d576-117">På den sista raden i artikelinförselmallen markerar du kryssrutan **Sök flytande lagerplats**.</span><span class="sxs-lookup"><span data-stu-id="5d576-117">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="5d576-118">Du kan skapa olika artikelinförselmallar och sedan använda dem som du vill.</span><span class="sxs-lookup"><span data-stu-id="5d576-118">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="5d576-119">Den artikelinförselmall som du har valt för artikeln eller lagerställeenheten om det finns någon.</span><span class="sxs-lookup"><span data-stu-id="5d576-119">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="5d576-120">Om de här fälten inte fylls i används den artikelinförselmall som du har valt för distributionslagret på snabbfliken **Lagerplatsprinciper** på lagerställekortet.</span><span class="sxs-lookup"><span data-stu-id="5d576-120">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5d576-121">Se även</span><span class="sxs-lookup"><span data-stu-id="5d576-121">See Also</span></span>

[<span data-ttu-id="5d576-122">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="5d576-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="5d576-123">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="5d576-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="5d576-124">Ställa in lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="5d576-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="5d576-125">Monteringshantering</span><span class="sxs-lookup"><span data-stu-id="5d576-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="5d576-126">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="5d576-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="5d576-127">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5d576-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
