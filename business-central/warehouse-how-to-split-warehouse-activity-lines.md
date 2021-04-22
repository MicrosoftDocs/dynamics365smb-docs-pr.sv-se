---
title: 'Så här: Dela Dist.lageraktivitetsrader | Microsoft Docs'
description: I distributionslagerartikelinförslar, -transporter och -plockningar, samt i lagerartikelinförslar och lagerplockningar, föreslås lagerställen för plockning och införsel av artiklar. det faktiska antalet på den lagerplats som föreslås kanske inte räcker, eller också finns det inte tillräckligt mycket plats på den föreslagna lagerstället för införsel av det aktuella antalet. I så fall måste du dela upp raden, så att artiklarna på en rad tas från, eller placeras på, fler än en lagerplats.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 08cebf3fb140fd76396add89bf8d7418aa4f115a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784148"
---
# <a name="split-warehouse-activity-lines"></a><span data-ttu-id="a97e2-105">Dela rader för dist.lageraktivitet</span><span class="sxs-lookup"><span data-stu-id="a97e2-105">Split Warehouse Activity Lines</span></span>
<span data-ttu-id="a97e2-106">I distributionslagerartikelinförslar, -transporter och -plockningar, samt i lagerartikelinförslar och lagerplockningar, föreslås lagerställen för plockning och införsel av artiklar.</span><span class="sxs-lookup"><span data-stu-id="a97e2-106">In warehouse put-aways, movements, or picks, and in inventory put-aways and inventory picks, bins are suggested for the picking or putting away of items.</span></span> <span data-ttu-id="a97e2-107">det faktiska antalet på den lagerplats som föreslås kanske inte räcker, eller också finns det inte tillräckligt mycket plats på den föreslagna lagerstället för införsel av det aktuella antalet.</span><span class="sxs-lookup"><span data-stu-id="a97e2-107">The actual quantity in the bin suggested may not be sufficient, or there is not enough room in the suggested bin to put away the required quantity.</span></span> <span data-ttu-id="a97e2-108">I så fall måste du dela upp raden, så att artiklarna på en rad tas från, eller placeras på, fler än en lagerplats.</span><span class="sxs-lookup"><span data-stu-id="a97e2-108">In these cases, you need to split the line, so that the items for one line are either taken from or placed into more than one bin.</span></span>  

<span data-ttu-id="a97e2-109">Följande procedur gäller alla distributionslagerdokument, till exempel Dist.lager artikelinförsel, transport och plockningsrader, eller lager, artikelinförsel, transport och plockningsrader.</span><span class="sxs-lookup"><span data-stu-id="a97e2-109">The following procedure applies to warehouse documents, such as warehouse put-away, movement, and pick lines, or inventory put-away, movement, and pick lines.</span></span>  

## <a name="to-split-warehouse-activity-lines"></a><span data-ttu-id="a97e2-110">Att dela Dist.lageraktivitet rader</span><span class="sxs-lookup"><span data-stu-id="a97e2-110">To split warehouse activity lines</span></span>  
1.  <span data-ttu-id="a97e2-111">Öppna en lageraktivitetsrad där du försöker manipulera ett otillräckligt antal.</span><span class="sxs-lookup"><span data-stu-id="a97e2-111">Open a warehouse activity line where you are trying to handle an insufficient quantity.</span></span>  
2.  <span data-ttu-id="a97e2-112">I **Ant. att hantera** fältet, ange det antal som kan hantera.</span><span class="sxs-lookup"><span data-stu-id="a97e2-112">In the **Qty. to Handle** field, enter the reduced quantity that you are able to handle.</span></span>  
3.  <span data-ttu-id="a97e2-113">På snabbfliken **Rader** väljer du åtgärden **Åtgärder** och väljer sedan åtgärden **Funktioner** och sedan åtgärden **Dela rad**.</span><span class="sxs-lookup"><span data-stu-id="a97e2-113">On the **Lines** FastTab, choose the **Actions** action, choose the **Functions** action, and then choose the **Split Line** action.</span></span> <span data-ttu-id="a97e2-114">Det visas en ny rad, som är en kopia av den ursprungliga raden, med den skillnaden att fältet **Ant. att hantera** innehåller det antal som du tog bort från den ursprungliga raden.</span><span class="sxs-lookup"><span data-stu-id="a97e2-114">A new line appears, which is a copy of the original line, except that the **Qty. to Handle** field contains the quantity that you removed from the original line.</span></span>  
4.  <span data-ttu-id="a97e2-115">Tilldela den nya raden en lämplig lagerplats och zon, om du använder dirigerad artikelinförsel och plockning, eller fortsätt att dela upp raden efter behov tills du har önskat antal lagerställen för hela kvantiteten.</span><span class="sxs-lookup"><span data-stu-id="a97e2-115">Assign an appropriate bin and, if you are using directed put-away and pick, a zone, to this new line, or continue splitting the line as necessary until you find appropriate bins for all of the quantity.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a97e2-116">Om lagerstället är inställt på dirigerad artikelinförsel och plockning, och du delar raderna, måste du vara förtrogen med distributionslagret och kunna välja en lagerplats som passar artikelns lagringskrav och uppfyller de allmänna kraven i distributionslagerdokumentet.</span><span class="sxs-lookup"><span data-stu-id="a97e2-116">If the location uses directed put-away and pick and you split the lines, you must be familiar with the warehouse and be able to choose a bin that matches the storage requirements of the item and that fulfills the general requirements of the warehouse document.</span></span> <span data-ttu-id="a97e2-117">Du skulle till exempel inte dela en rad i ett plockningsdokument och placera några artiklar i volymlagret.</span><span class="sxs-lookup"><span data-stu-id="a97e2-117">For example, you would not split a line on a pick document and place some items in the bulk storage.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a97e2-118">Se även</span><span class="sxs-lookup"><span data-stu-id="a97e2-118">See Also</span></span>  
[<span data-ttu-id="a97e2-119">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="a97e2-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="a97e2-120">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="a97e2-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="a97e2-121">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="a97e2-121">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="a97e2-122">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="a97e2-122">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="a97e2-123">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="a97e2-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="a97e2-124">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a97e2-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]