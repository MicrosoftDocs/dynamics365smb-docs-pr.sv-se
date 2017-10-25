---
title: "Så här kan du använda enheten för produktionsbatch | Microsoft Docs"
description: "Om en artikel lagerförs med en enhet men tillverkas med en annan, måste produktionsordern använda en enhet för produktionsbatch för att beräkna rätt antal komponenter. Ett exempel på beräkning med en enhet för produktionsbatch är när tillverkade artiklar lagerförs styckvis, men tillverkas tonvis."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 1b075d164e18a52fbda56cced8d88fabc77bec3f
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-manufacturing-batch-units-of-measure"></a><span data-ttu-id="c1972-104">Så här kan du arbeta med enheter för produktionsbatch</span><span class="sxs-lookup"><span data-stu-id="c1972-104">How to: Work with Manufacturing Batch Units of Measure</span></span>
<span data-ttu-id="c1972-105">Om en artikel lagerförs med en enhet men tillverkas med en annan, kan du skapa en produktionsorder som använder enheten för produktionsbatch för att beräkna rätt antal komponenter under batch-jobbet **Uppdatera produktionsorder**.</span><span class="sxs-lookup"><span data-stu-id="c1972-105">If an item is stocked in one unit of measure but produced in another, a production order is created that uses a manufacturing batch unit of measure to calculate the correct quantity of the components during the **Refresh Production Order** batch job.</span></span> <span data-ttu-id="c1972-106">Ett exempel på beräkning med en enhet för produktionsbatch är när tillverkade artiklar lagerförs styckvis, men tillverkas tonvis.</span><span class="sxs-lookup"><span data-stu-id="c1972-106">An example of a manufacturing batch unit of measure calculation is when a manufactured item is stocked in pieces but produced in tons.</span></span>  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a><span data-ttu-id="c1972-107">Så här skapar du en produktionsstruktur med hjälp av en batchenhet</span><span class="sxs-lookup"><span data-stu-id="c1972-107">To create a production BOM using a batch unit of measure</span></span>  
1.  <span data-ttu-id="c1972-108">Enheten för produktionsbatchen anges som en alternativ enhet i fönstret **Artikelenheter** för den artikel som ska tillverkas.</span><span class="sxs-lookup"><span data-stu-id="c1972-108">The manufacturing batch unit of measure is set up as an alternative unit of measure in the **Item Units of Measure** window on the item to be produced.</span></span> <span data-ttu-id="c1972-109">Batchenheten kommer inte att ersätta basenheten för artikeln.</span><span class="sxs-lookup"><span data-stu-id="c1972-109">The batch unit of measure will not replace the base unit of measure on the item.</span></span>  
2.  <span data-ttu-id="c1972-110">Skapa en produktionsstruktur för den artikel som har angetts med enheten för produktionsbatch.</span><span class="sxs-lookup"><span data-stu-id="c1972-110">Create a production BOM for the item set up with the manufacturing batch unit of measure.</span></span> <span data-ttu-id="c1972-111">För mer information, se [Så här skapar du produktionsstrukturer](production-how-to-create-production-boms.md).</span><span class="sxs-lookup"><span data-stu-id="c1972-111">For more information, see [How to: Create Production BOMs](production-how-to-create-production-boms.md).</span></span>  
3.  <span data-ttu-id="c1972-112">Markera enhetskod för produktionsbatch i fältet **Enhetskod**.</span><span class="sxs-lookup"><span data-stu-id="c1972-112">In the **Unit of Measure Code** field, select the manufacturing batch unit of measure.</span></span>  
4.  <span data-ttu-id="c1972-113">I fältet **Antal per** anger du det antal av komponentartikeln som krävs för att skapa den här batchenheten för varje produktionsstrukturrad.</span><span class="sxs-lookup"><span data-stu-id="c1972-113">For each production BOM line, in the **Quantity Per** field, enter the quantity of this component item that is required to create this batch unit of measure.</span></span>  
5.  <span data-ttu-id="c1972-114">Öppna **Artikelkort** för den kopplade artikeln.</span><span class="sxs-lookup"><span data-stu-id="c1972-114">Open the **Item Card** for the related item.</span></span>  

    <span data-ttu-id="c1972-115">Klicka på snabbfliken **Återanskaffning**. I fältet **Prod.struktursnr** väljer du den produktionsstruktur som skapades ovan.</span><span class="sxs-lookup"><span data-stu-id="c1972-115">On the **Replenishment** FastTab, in the **Production BOM No.** field, select the production BOM created above.</span></span>  
6.  <span data-ttu-id="c1972-116">Skapa ett produktionsorderhuvud med hjälp av den artikel som har angetts med enheten för produktionsbatch.</span><span class="sxs-lookup"><span data-stu-id="c1972-116">Create a production order header using the item set up with the manufacturing batch unit of measure.</span></span> <span data-ttu-id="c1972-117">Mer information finnsi [Så här skapar du ett produktionsorder](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="c1972-117">For more information, see [How to: Create Production Orders](production-how-to-create-production-orders.md).</span></span>  
7.  <span data-ttu-id="c1972-118">Välj åtgärden **Uppdatera** och sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1972-118">Choose the **Refresh** action, and then choose  the **OK** button.</span></span>  

<span data-ttu-id="c1972-119">På snabbfliken **Rader** väljer du åtgärden **Rad** och väljer sedan åtgärden **Komponenter** för att visa resultatet.</span><span class="sxs-lookup"><span data-stu-id="c1972-119">On the **Lines** FastTab, choose the **Line** action, and then choose the **Components** action to view the result.</span></span> <span data-ttu-id="c1972-120">I programmet beräknas det rätta antalet komponenter som krävs för att uppfylla produktionsstrukturen baserat på enheten för produktionsbatch.</span><span class="sxs-lookup"><span data-stu-id="c1972-120">The program calculates the correct quantity of the components needed to satisfy the production BOM based on the manufacturing batch unit of measure.</span></span>  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a><span data-ttu-id="c1972-121">Så här beräknar du en enhet för produktionsbatch i en produktionsorder</span><span class="sxs-lookup"><span data-stu-id="c1972-121">To calculate a manufacturing batch unit of measure on a production order</span></span>  
1.  <span data-ttu-id="c1972-122">Skapa ett produktionsorderhuvud med hjälp av den artikel som har angetts med enheten för produktionsbatch.</span><span class="sxs-lookup"><span data-stu-id="c1972-122">Create a production order header using the item set up with the manufacturing batch unit of measure.</span></span>  
2.  <span data-ttu-id="c1972-123">I fältet **Artikelnr** på produktionsorderraden anger du samma artikelnummer som användes i huvudet.</span><span class="sxs-lookup"><span data-stu-id="c1972-123">In the **Item No.** field in the Production Order line, type the same item number used in the header.</span></span>  
3.  <span data-ttu-id="c1972-124">I fältet **Antal** anger du samma antal som användes i huvudet.</span><span class="sxs-lookup"><span data-stu-id="c1972-124">In the **Quantity** field, enter the same quantity used in the header.</span></span>  
4.  <span data-ttu-id="c1972-125">Markera enhetskod för produktionsbatch i fältet **Enhetskod**.</span><span class="sxs-lookup"><span data-stu-id="c1972-125">In the **Unit of Measure Code** field, select the manufacturing batch unit of measure code.</span></span>  
5.  <span data-ttu-id="c1972-126">Välj åtgärden **Uppdatera**.</span><span class="sxs-lookup"><span data-stu-id="c1972-126">Choose the **Refresh** action.</span></span>
6.  <span data-ttu-id="c1972-127">På snabbfliken **Beräkna** avmarkerar du kryssrutan **Rader**.</span><span class="sxs-lookup"><span data-stu-id="c1972-127">On the **Calculate** FastTab, clear the **Lines** check box.</span></span>  
7.  <span data-ttu-id="c1972-128">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1972-128">Choose the **OK** button.</span></span>  
8.  <span data-ttu-id="c1972-129">På snabbfliken **Rader** väljer du åtgärden **Rad** och väljer sedan åtgärden **Komponenter** för att visa resultatet.</span><span class="sxs-lookup"><span data-stu-id="c1972-129">On the **Lines** FastTab, choose the **Line** action, and then choose the **Components** action to view the result.</span></span> <span data-ttu-id="c1972-130">Det rätta antalet komponenter som krävs för att uppfylla produktionsstrukturen beräknas baserat på enheten för produktionsbatch.</span><span class="sxs-lookup"><span data-stu-id="c1972-130">The correct quantity of the components needed to satisfy the production BOM is calculated based on the manufacturing batch unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c1972-131">Se även</span><span class="sxs-lookup"><span data-stu-id="c1972-131">See Also</span></span>  
[<span data-ttu-id="c1972-132">Så här skapar du operationsföljder</span><span class="sxs-lookup"><span data-stu-id="c1972-132">How to: Create Routings</span></span>](production-how-to-create-routings.md)  
<span data-ttu-id="c1972-133">[Så här skapar du nya produktionsstrukturer](production-how-to-create-production-boms.md)   </span><span class="sxs-lookup"><span data-stu-id="c1972-133">[How to: Create Production BOMs](production-how-to-create-production-boms.md)   </span></span>  
[<span data-ttu-id="c1972-134">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="c1972-134">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="c1972-135">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="c1972-135">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="c1972-136">[Planerad](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="c1972-136">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="c1972-137">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="c1972-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c1972-138">Inköp</span><span class="sxs-lookup"><span data-stu-id="c1972-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c1972-139">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c1972-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

