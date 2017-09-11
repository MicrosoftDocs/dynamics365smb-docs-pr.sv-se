---
title: "Så här arbetar du med strukturer för att hantera komponenter | Microsoft Docs"
description: "Du kan skapa en monteringsstruktur för att ange vilka komponenter eller resurser som krävs för att skapa artikeln som monteringsstrukturen representerar i listan och du kan visa komponenterna i en monteringsartikel."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-bills-of-material"></a><span data-ttu-id="30157-103">Så här arbetar du med strukturer</span><span class="sxs-lookup"><span data-stu-id="30157-103">How to: Work with Bills of Material</span></span>
> [!NOTE]  
>   <span data-ttu-id="30157-104">Den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller bara den första delen av funktionen monteringshantering.</span><span class="sxs-lookup"><span data-stu-id="30157-104">The current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the first part of the Assembly Management feature.</span></span> <span data-ttu-id="30157-105">Nu kan du bara skapa monteringsstrukturer och därefter hantera de relaterade överordnade artiklarna som normala lagerartiklar.</span><span class="sxs-lookup"><span data-stu-id="30157-105">For now, you can only create assembly BOMs and then handle the related parent items as normal inventory items.</span></span> <span data-ttu-id="30157-106">I en kommande uppdatering kan du hantera den faktiska monteringen av artiklar från komponenter, antingen i montering mot lager eller montering mot orderflöden, och du kan sälja komponenter som satser.</span><span class="sxs-lookup"><span data-stu-id="30157-106">In a future update, you can manage the actual assembly of items from components, either in assemble-to-stock or assemble-to-order flows, and you can sell components as kits.</span></span>

<span data-ttu-id="30157-107">Använd strukturer för att strukturera de överordnade artiklar som du säljer som satser som består av komponenter som du monterar till order eller lager.</span><span class="sxs-lookup"><span data-stu-id="30157-107">You use bills of materials (BOMs) to structure parent items that you sell as kits consisting of the parent's components or that you assemble to order or to stock.</span></span>

<span data-ttu-id="30157-108">I [!INCLUDE[d365fin](includes/d365fin_md.md)],  är en struktur en monteringsstruktur.</span><span class="sxs-lookup"><span data-stu-id="30157-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], a bill of materials is referred to as an "assembly BOM".</span></span> <span data-ttu-id="30157-109">Monteringsstrukturer anger vilka komponenter som finns i överordnade artiklar.</span><span class="sxs-lookup"><span data-stu-id="30157-109">Assembly BOMs specify which components are contained in parent items.</span></span> <span data-ttu-id="30157-110">I den här dokumentationen kallas en artikel en "monteringsartikel".</span><span class="sxs-lookup"><span data-stu-id="30157-110">In this documentation, a parent item is referred to as an "assembly item".</span></span>

<span data-ttu-id="30157-111">Monteringsstrukturer innehåller vanligtvis artiklar men kan också innehålla en eller flera resurser som krävs för att utföra monteringsarbetet.</span><span class="sxs-lookup"><span data-stu-id="30157-111">Assembly BOMs usually contain items but can also contain one or more resources that are required to put the assembly item together.</span></span>

<span data-ttu-id="30157-112">Monteringsstrukturer kan ha flera nivåer, vilket innebär att en komponent på monteringsstruktur kan vara en monteringsartikel själv.</span><span class="sxs-lookup"><span data-stu-id="30157-112">Assembly BOMs can have multiple levels, which means that a component on the assembly BOM can be an assembly item itself.</span></span> <span data-ttu-id="30157-113">I så fall innehåller fältet **Monteringsstruktur** på monteringsstrukturraden **Ja**.</span><span class="sxs-lookup"><span data-stu-id="30157-113">In that case, the **Assembly BOM** field on the assembly BOM line contains **Yes**.</span></span>

<span data-ttu-id="30157-114">Särskilda krav gäller artiklarna på moneringsstrukturer med avseende på tillgängligheten.</span><span class="sxs-lookup"><span data-stu-id="30157-114">Special requirements apply to items on assembly BOMs with regards to availability.</span></span> <span data-ttu-id="30157-115">Mer information finns i avsnittet "För att visa tillgängligheten för en artikel med dess användning i monteringsstrukturer" i [så här visar du artikeldisposition](inventory-how-availability-overview.md).</span><span class="sxs-lookup"><span data-stu-id="30157-115">For more information, see the "To see the availability of an item by its use in assembly BOMs" section in [How to: View the Availability of Items](inventory-how-availability-overview.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="30157-116">Den här funktionen kräver att din upplevelse är inställd på **Paket**.</span><span class="sxs-lookup"><span data-stu-id="30157-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="30157-117">Mer information finns i [anpassa din finansiella upplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="30157-117">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>

## <a name="to-create-an-assembly-bom"></a><span data-ttu-id="30157-118">Skapa en monteringsstruktur</span><span class="sxs-lookup"><span data-stu-id="30157-118">To create an assembly BOM</span></span>
<span data-ttu-id="30157-119">Om du vill definiera en överordnad artikel som består av andra artiklar eller resurser som krävs för att montera den överordnade, måste du skapa en monteringsstruktur.</span><span class="sxs-lookup"><span data-stu-id="30157-119">To define a parent item that consists of other items, and potentially of resources required to put the parent together, you must create an assembly BOM.</span></span>  

<span data-ttu-id="30157-120">Det finns två delar för att skapa en monteringsstruktur:</span><span class="sxs-lookup"><span data-stu-id="30157-120">There are two parts to creating an assembly BOM:</span></span>
- <span data-ttu-id="30157-121">Skapa en ny artikel</span><span class="sxs-lookup"><span data-stu-id="30157-121">Setting up a new item</span></span>
- <span data-ttu-id="30157-122">Ange strukturem för monteringsartikeln.</span><span class="sxs-lookup"><span data-stu-id="30157-122">Defining the BOM structure of the assembly item.</span></span>

1. <span data-ttu-id="30157-123">Skapa en ny artikel.</span><span class="sxs-lookup"><span data-stu-id="30157-123">Set up a new item.</span></span> <span data-ttu-id="30157-124">Mer information finns i [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="30157-124">For more information, see [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

    <span data-ttu-id="30157-125">Fortsätt med att ange komponenter eller resurser i monteringsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="30157-125">Proceed to enter components or resources on the assembly BOM.</span></span>  
2. <span data-ttu-id="30157-126">I fönstret **artikelkort** för en monteringsartikel väljer du åtgärden **montering** och väljer sedan åtgärden **Monteringsstruktur**.</span><span class="sxs-lookup"><span data-stu-id="30157-126">In the **Item Card** window for an assembly item, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
3. <span data-ttu-id="30157-127">I fönstret **Monteringsstruktur** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="30157-127">In the **Assembly BOM** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a><span data-ttu-id="30157-128">Att visa komponenter i en monteringsartikel som dras in enligt strukturen</span><span class="sxs-lookup"><span data-stu-id="30157-128">To view the components of an assembly item indented according to the BOM structure</span></span>
<span data-ttu-id="30157-129">Från fönstret **Monteringsstruktur** kan du öppna ett separat fönster som visar komponenterna och resurserna med indrag enligt deras strukturplats under monteringsartikeln.</span><span class="sxs-lookup"><span data-stu-id="30157-129">From the **Assembly BOM** window, you can open a separate window that shows the components and any resources indented according to their BOM position under the assembly item.</span></span>

1. <span data-ttu-id="30157-130">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="30157-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="30157-131">Öppna kortet för monteringsartikeln.</span><span class="sxs-lookup"><span data-stu-id="30157-131">Open the card for an assembly item.</span></span> <span data-ttu-id="30157-132">(Fältet **Monteringsstruktur** i fönstret **artiklar** innehåller **Ja**.)</span><span class="sxs-lookup"><span data-stu-id="30157-132">(The **Assembly BOM** field in the **Items** window contains **Yes**.)</span></span>
3. <span data-ttu-id="30157-133">I fönstret **artikelkort** väljer du åtgärden **montering** och väljer sedan åtgärden **Monteringsstruktur**.</span><span class="sxs-lookup"><span data-stu-id="30157-133">In the **Item Card** window, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
4. <span data-ttu-id="30157-134">I fönstret **Monteringsstruktur** väljer du åtgärden **visa struktur**.</span><span class="sxs-lookup"><span data-stu-id="30157-134">In the **Assembly BOM** window, choose the **Show BOM** action.</span></span>

## <a name="to-buy-sell-or-transfer-assembly-items"></a><span data-ttu-id="30157-135">Att köpa, sälja eller överföra monteringsartiklar</span><span class="sxs-lookup"><span data-stu-id="30157-135">To buy, sell, or transfer assembly items</span></span>
<span data-ttu-id="30157-136">Eftersom den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] endast innehåller förmågan att definiera och tilldela strukturer till artiklar kan du hantera monteringsartiklar på rader som endast vanliga artiklar.</span><span class="sxs-lookup"><span data-stu-id="30157-136">Because the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the ability to define and assign assembly BOMs to items, you can handle assembly items on document lines as normal items only.</span></span>

<span data-ttu-id="30157-137">**Varning**: lagerkvantiteten för strukturkomponenter justeras inte om du gör detta.</span><span class="sxs-lookup"><span data-stu-id="30157-137">**Caution**: The inventory quantity of BOM components will not be adjusted if you do so.</span></span>

## <a name="see-also"></a><span data-ttu-id="30157-138">Se även</span><span class="sxs-lookup"><span data-stu-id="30157-138">See Also</span></span>
[<span data-ttu-id="30157-139">Så här registrerar du nya objekt</span><span class="sxs-lookup"><span data-stu-id="30157-139">How to: Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="30157-140">[Så här visar du artikeldisposition](inventory-how-availability-overview.md)   </span><span class="sxs-lookup"><span data-stu-id="30157-140">[How to: View the Availability of Items](inventory-how-availability-overview.md)   </span></span>  
[<span data-ttu-id="30157-141">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="30157-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="30157-142">[Arbeta med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="30157-142">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>

