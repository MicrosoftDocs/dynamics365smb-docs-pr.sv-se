---
title: "Så här skapar du ett produktionsorderhuvud | Microsoft Docs"
description: "Du kan skapa en produktionsorder manuellt och första steget är då att skapa ett produktionsorderhuvud."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 00ecc7031bc1c208444e89fbd13e2f2faf5fd413
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="create-production-order-headers"></a><span data-ttu-id="26740-103">Så här skapar du produktionsorderhuvud</span><span class="sxs-lookup"><span data-stu-id="26740-103">Create Production Order Headers</span></span>
<span data-ttu-id="26740-104">Du kan skapa en produktionsorder manuellt och första steget är då att skapa ett produktionsorderhuvud.</span><span class="sxs-lookup"><span data-stu-id="26740-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="26740-105">Produktionsorder skapas vanligtvis automatiskt av en planeringsfunktion för att uppfylla ett behov som är känt.</span><span class="sxs-lookup"><span data-stu-id="26740-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="26740-106">Mer information finns i [Planering](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="26740-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="26740-107">I det följande procedur skapas en fast planerad produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="26740-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="26740-108">Du kan också skapa produktionsorder med annan status.</span><span class="sxs-lookup"><span data-stu-id="26740-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="26740-109">Så här skapar du ett produktionsorderhuvud</span><span class="sxs-lookup"><span data-stu-id="26740-109">To create a production order header</span></span>  
1.  <span data-ttu-id="26740-110">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Fasta planerade prod.order** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26740-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="26740-111">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="26740-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="26740-112">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="26740-112">In the **No.**</span></span> <span data-ttu-id="26740-113">skriver du numret på den artikel som har beställts.</span><span class="sxs-lookup"><span data-stu-id="26740-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="26740-114">Välj produktionsorderns ursprung i fältet **Ursprungstyp**.</span><span class="sxs-lookup"><span data-stu-id="26740-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="26740-115">Här kan du välja att skapa en familj av artiklar.</span><span class="sxs-lookup"><span data-stu-id="26740-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="26740-116">Mer information finns i [Så här arbetar du med produktionsfamiljer](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="26740-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="26740-117">Välj artikelnummer, familj eller försäljningshuvud som produktionsordern ska skapas för i fältet **Ursprungsnr** .</span><span class="sxs-lookup"><span data-stu-id="26740-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="26740-118">Fyll i fälten **Antal** och **Förfallodatum** enligt aktuella specifikationer.</span><span class="sxs-lookup"><span data-stu-id="26740-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="26740-119">När produktionsbehov ändras, till exempel komponenter och operationer, kan du snabbt omplanera produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="26740-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="26740-120">Mer information finns i [Omplanera eller uppdatera produktionsorder direkt](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="26740-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="26740-121">Se även</span><span class="sxs-lookup"><span data-stu-id="26740-121">See Also</span></span>  
<span data-ttu-id="26740-122">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="26740-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="26740-123">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="26740-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="26740-124">[Planerad](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="26740-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="26740-125">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="26740-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="26740-126">Inköp</span><span class="sxs-lookup"><span data-stu-id="26740-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="26740-127">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26740-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
