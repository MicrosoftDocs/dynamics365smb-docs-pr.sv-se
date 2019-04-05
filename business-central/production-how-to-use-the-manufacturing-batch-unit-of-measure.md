---
title: Använda enheten för produktionsbatch | Microsoft Docs
description: Om en artikel lagerförs med en enhet men tillverkas med en annan, måste produktionsordern använda en enhet för produktionsbatch för att beräkna rätt antal komponenter. Ett exempel på beräkning med en enhet för produktionsbatch är när tillverkade artiklar lagerförs styckvis, men tillverkas tonvis.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: f5db99544cea6cb4f34789a4b2a5cae602cc1f75
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "806853"
---
# <a name="work-with-manufacturing-batch-units-of-measure"></a><span data-ttu-id="13194-104">Arbeta med måttenheter för produktionsbatch</span><span class="sxs-lookup"><span data-stu-id="13194-104">Work with Manufacturing Batch Units of Measure</span></span>
<span data-ttu-id="13194-105">Om en artikel lagerförs med en enhet men tillverkas med en annan, kan du skapa en produktionsorder som använder enheten för produktionsbatch för att beräkna rätt antal komponenter under batch-jobbet **Uppdatera produktionsorder**.</span><span class="sxs-lookup"><span data-stu-id="13194-105">If an item is stocked in one unit of measure but produced in another, a production order is created that uses a manufacturing batch unit of measure to calculate the correct quantity of the components during the **Refresh Production Order** batch job.</span></span> <span data-ttu-id="13194-106">Ett exempel på beräkning med en enhet för produktionsbatch är när tillverkade artiklar lagerförs styckvis, men tillverkas tonvis.</span><span class="sxs-lookup"><span data-stu-id="13194-106">An example of a manufacturing batch unit of measure calculation is when a manufactured item is stocked in pieces but produced in tons.</span></span>  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a><span data-ttu-id="13194-107">Så här skapar du en produktionsstruktur med hjälp av en batchenhet</span><span class="sxs-lookup"><span data-stu-id="13194-107">To create a production BOM using a batch unit of measure</span></span>  
1.  <span data-ttu-id="13194-108">Enheten för produktionsbatchen anges som en alternativ enhet på sidan **Artikelenheter** för den artikel som ska tillverkas.</span><span class="sxs-lookup"><span data-stu-id="13194-108">The manufacturing batch unit of measure is set up as an alternative unit of measure on the **Item Units of Measure** page on the item to be produced.</span></span> <span data-ttu-id="13194-109">Batchenheten kommer inte att ersätta basenheten för artikeln.</span><span class="sxs-lookup"><span data-stu-id="13194-109">The batch unit of measure will not replace the base unit of measure on the item.</span></span>  
2.  <span data-ttu-id="13194-110">Skapa en produktionsstruktur för den artikel som har angetts med enheten för produktionsbatch.</span><span class="sxs-lookup"><span data-stu-id="13194-110">Create a production BOM for the item set up with the manufacturing batch unit of measure.</span></span> <span data-ttu-id="13194-111">För mer information, se [Skapa produktionsstrukturer](production-how-to-create-production-boms.md).</span><span class="sxs-lookup"><span data-stu-id="13194-111">For more information, see [Create Production BOMs](production-how-to-create-production-boms.md).</span></span>  
3.  <span data-ttu-id="13194-112">Markera enhetskod för produktionsbatch i fältet **Enhetskod**.</span><span class="sxs-lookup"><span data-stu-id="13194-112">In the **Unit of Measure Code** field, select the manufacturing batch unit of measure.</span></span>  
4.  <span data-ttu-id="13194-113">I fältet **Antal per** anger du det antal av komponentartikeln som krävs för att skapa den här batchenheten för varje produktionsstrukturrad.</span><span class="sxs-lookup"><span data-stu-id="13194-113">For each production BOM line, in the **Quantity Per** field, enter the quantity of this component item that is required to create this batch unit of measure.</span></span>  
5.  <span data-ttu-id="13194-114">Öppna **Artikelkort** för den kopplade artikeln.</span><span class="sxs-lookup"><span data-stu-id="13194-114">Open the **Item Card** for the related item.</span></span>  

    <span data-ttu-id="13194-115">Klicka på snabbfliken **Återanskaffning**. I fältet **Prod.struktursnr** väljer du den produktionsstruktur som skapades ovan.</span><span class="sxs-lookup"><span data-stu-id="13194-115">On the **Replenishment** FastTab, in the **Production BOM No.** field, select the production BOM created above.</span></span>  
6.  <span data-ttu-id="13194-116">Skapa ett produktionsorderhuvud med hjälp av den artikel som har angetts med enheten för produktionsbatch.</span><span class="sxs-lookup"><span data-stu-id="13194-116">Create a production order header using the item set up with the manufacturing batch unit of measure.</span></span> <span data-ttu-id="13194-117">För mer information, se [Skapa produktionsorder](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="13194-117">For more information, see [Create Production Orders](production-how-to-create-production-orders.md).</span></span>  
7.  <span data-ttu-id="13194-118">Välj åtgärden **Uppdatera** och sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="13194-118">Choose the **Refresh** action, and then choose  the **OK** button.</span></span>  

<span data-ttu-id="13194-119">På snabbfliken **Rader** väljer du åtgärden **Rad** och väljer sedan åtgärden **Komponenter** för att visa resultatet.</span><span class="sxs-lookup"><span data-stu-id="13194-119">On the **Lines** FastTab, choose the **Line** action, and then choose the **Components** action to view the result.</span></span> <span data-ttu-id="13194-120">I programmet beräknas det rätta antalet komponenter som krävs för att uppfylla produktionsstrukturen baserat på enheten för produktionsbatch.</span><span class="sxs-lookup"><span data-stu-id="13194-120">The program calculates the correct quantity of the components needed to satisfy the production BOM based on the manufacturing batch unit of measure.</span></span>  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a><span data-ttu-id="13194-121">Så här beräknar du en enhet för produktionsbatch i en produktionsorder</span><span class="sxs-lookup"><span data-stu-id="13194-121">To calculate a manufacturing batch unit of measure on a production order</span></span>  
1.  <span data-ttu-id="13194-122">Skapa ett produktionsorderhuvud med hjälp av den artikel som har angetts med enheten för produktionsbatch.</span><span class="sxs-lookup"><span data-stu-id="13194-122">Create a production order header using the item set up with the manufacturing batch unit of measure.</span></span>  
2.  <span data-ttu-id="13194-123">I fältet **Artikelnr** på produktionsorderraden anger du samma artikelnummer som användes i huvudet.</span><span class="sxs-lookup"><span data-stu-id="13194-123">In the **Item No.** field in the Production Order line, type the same item number used in the header.</span></span>  
3.  <span data-ttu-id="13194-124">I fältet **Antal** anger du samma antal som användes i huvudet.</span><span class="sxs-lookup"><span data-stu-id="13194-124">In the **Quantity** field, enter the same quantity used in the header.</span></span>  
4.  <span data-ttu-id="13194-125">Markera enhetskod för produktionsbatch i fältet **Enhetskod**.</span><span class="sxs-lookup"><span data-stu-id="13194-125">In the **Unit of Measure Code** field, select the manufacturing batch unit of measure code.</span></span>  
5.  <span data-ttu-id="13194-126">Välj åtgärden **Uppdatera**.</span><span class="sxs-lookup"><span data-stu-id="13194-126">Choose the **Refresh** action.</span></span>
6.  <span data-ttu-id="13194-127">På snabbfliken **Beräkna** avmarkerar du kryssrutan **Rader**.</span><span class="sxs-lookup"><span data-stu-id="13194-127">On the **Calculate** FastTab, clear the **Lines** check box.</span></span>  
7.  <span data-ttu-id="13194-128">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="13194-128">Choose the **OK** button.</span></span>  
8.  <span data-ttu-id="13194-129">På snabbfliken **Rader** väljer du åtgärden **Rad** och väljer sedan åtgärden **Komponenter** för att visa resultatet.</span><span class="sxs-lookup"><span data-stu-id="13194-129">On the **Lines** FastTab, choose the **Line** action, and then choose the **Components** action to view the result.</span></span> <span data-ttu-id="13194-130">Det rätta antalet komponenter som krävs för att uppfylla produktionsstrukturen beräknas baserat på enheten för produktionsbatch.</span><span class="sxs-lookup"><span data-stu-id="13194-130">The correct quantity of the components needed to satisfy the production BOM is calculated based on the manufacturing batch unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="13194-131">Se även</span><span class="sxs-lookup"><span data-stu-id="13194-131">See Also</span></span>  
[<span data-ttu-id="13194-132">Skapa verksamhetsföljder</span><span class="sxs-lookup"><span data-stu-id="13194-132">Create Routings</span></span>](production-how-to-create-routings.md)  
<span data-ttu-id="13194-133">[Skapa produktionsstrukturer](production-how-to-create-production-boms.md)   </span><span class="sxs-lookup"><span data-stu-id="13194-133">[Create Production BOMs](production-how-to-create-production-boms.md)   </span></span>  
[<span data-ttu-id="13194-134">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="13194-134">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="13194-135">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="13194-135">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="13194-136">[Planerad](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="13194-136">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="13194-137">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="13194-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="13194-138">Inköp</span><span class="sxs-lookup"><span data-stu-id="13194-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="13194-139">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="13194-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
