---
title: "Så här: Dela Dist.lageraktivitetsrader | Microsoft Docs"
description: "I distributionslagerartikelinförslar, -transporter och -plockningar, samt i lagerartikelinförslar och lagerplockningar, föreslås lagerplatser för plockning och införsel av artiklar. det faktiska antalet på den lagerplats som föreslås kanske inte räcker, eller också finns det inte tillräckligt mycket plats på den föreslagna lagerplatsen för införsel av det aktuella antalet. I så fall måste du dela upp raden, så att artiklarna på en rad tas från, eller placeras på, fler än en lagerplats."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 821d3bed8e90d7221fe343156b46663cdf601dcf
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="split-warehouse-activity-lines"></a><span data-ttu-id="40b01-105">Dela rader för dist.lageraktivitet</span><span class="sxs-lookup"><span data-stu-id="40b01-105">Split Warehouse Activity Lines</span></span>
<span data-ttu-id="40b01-106">I distributionslagerartikelinförslar, -transporter och -plockningar, samt i lagerartikelinförslar och lagerplockningar, föreslås lagerplatser för plockning och införsel av artiklar.</span><span class="sxs-lookup"><span data-stu-id="40b01-106">In warehouse put-aways, movements, or picks, and in inventory put-aways and inventory picks, bins are suggested for the picking or putting away of items.</span></span> <span data-ttu-id="40b01-107">det faktiska antalet på den lagerplats som föreslås kanske inte räcker, eller också finns det inte tillräckligt mycket plats på den föreslagna lagerplatsen för införsel av det aktuella antalet.</span><span class="sxs-lookup"><span data-stu-id="40b01-107">The actual quantity in the bin suggested may not be sufficient, or there is not enough room in the suggested bin to put away the required quantity.</span></span> <span data-ttu-id="40b01-108">I så fall måste du dela upp raden, så att artiklarna på en rad tas från, eller placeras på, fler än en lagerplats.</span><span class="sxs-lookup"><span data-stu-id="40b01-108">In these cases, you need to split the line, so that the items for one line are either taken from or placed into more than one bin.</span></span>  

<span data-ttu-id="40b01-109">Följande procedur gäller alla distributionslagerdokument, till exempel Dist.lager artikelinförsel, transport och plockningsrader, eller lager, artikelinförsel, transport och plockningsrader.</span><span class="sxs-lookup"><span data-stu-id="40b01-109">The following procedure applies to warehouse documents, such as warehouse put-away, movement, and pick lines, or inventory put-away, movement, and pick lines.</span></span>  

## <a name="to-split-warehouse-activity-lines"></a><span data-ttu-id="40b01-110">Att dela Dist.lageraktivitet rader</span><span class="sxs-lookup"><span data-stu-id="40b01-110">To split warehouse activity lines</span></span>  
1.  <span data-ttu-id="40b01-111">Öppna en lageraktivitetsrad där du försöker manipulera ett otillräckligt antal.</span><span class="sxs-lookup"><span data-stu-id="40b01-111">Open a warehouse activity line where you are trying to handle an insufficient quantity.</span></span>  
2.  <span data-ttu-id="40b01-112">I **Ant. att hantera** fältet, ange det antal som kan hantera.</span><span class="sxs-lookup"><span data-stu-id="40b01-112">In the **Qty. to Handle** field, enter the reduced quantity that you are able to handle.</span></span>  
3.  <span data-ttu-id="40b01-113">På snabbfliken **Rader** väljer du åtgärden **Åtgärder** och väljer sedan åtgärden **Funktioner** och sedan åtgärden **Dela rad**.</span><span class="sxs-lookup"><span data-stu-id="40b01-113">On the **Lines** FastTab, choose the **Actions** action, choose the **Functions** action, and then choose the **Split Line** action.</span></span> <span data-ttu-id="40b01-114">Det visas en ny rad, som är en kopia av den ursprungliga raden, med den skillnaden att fältet **Ant. att hantera** innehåller det antal som du tog bort från den ursprungliga raden.</span><span class="sxs-lookup"><span data-stu-id="40b01-114">A new line appears, which is a copy of the original line, except that the **Qty. to Handle** field contains the quantity that you removed from the original line.</span></span>  
4.  <span data-ttu-id="40b01-115">Tilldela den nya raden en lämplig lagerplats och zon, om du använder dirigerad artikelinförsel och plockning, eller fortsätt att dela upp raden efter behov tills du har önskat antal lagerplatser för hela kvantiteten.</span><span class="sxs-lookup"><span data-stu-id="40b01-115">Assign an appropriate bin and, if you are using directed put-away and pick, a zone, to this new line, or continue splitting the line as necessary until you find appropriate bins for all of the quantity.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="40b01-116">Om lagerstället är inställt på dirigerad artikelinförsel och plockning, och du delar raderna, måste du vara förtrogen med distributionslagret och kunna välja en lagerplats som passar artikelns lagringskrav och uppfyller de allmänna kraven i distributionslagerdokumentet.</span><span class="sxs-lookup"><span data-stu-id="40b01-116">If the location uses directed put-away and pick and you split the lines, you must be familiar with the warehouse and be able to choose a bin that matches the storage requirements of the item and that fulfills the general requirements of the warehouse document.</span></span> <span data-ttu-id="40b01-117">Du skulle till exempel inte dela en rad i ett plockningsdokument och placera några artiklar i volymlagret.</span><span class="sxs-lookup"><span data-stu-id="40b01-117">For example, you would not split a line on a pick document and place some items in the bulk storage.</span></span>  

## <a name="see-also"></a><span data-ttu-id="40b01-118">Se även</span><span class="sxs-lookup"><span data-stu-id="40b01-118">See Also</span></span>  
[<span data-ttu-id="40b01-119">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="40b01-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="40b01-120">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="40b01-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="40b01-121">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="40b01-121">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="40b01-122">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="40b01-122">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="40b01-123">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="40b01-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="40b01-124">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="40b01-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

