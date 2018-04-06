---
title: Designdetaljer - Integrering med lager | Microsoft Docs
description: Lagerledningsmodulen och lagermodulen interagerar med varandra i inventeringsjournalen och i lager- eller distributionslagerjustering.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 00a12f3f2203ed3b22cfee1af6aa8f155ca5fe4b
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-integration-with-inventory"></a><span data-ttu-id="54931-103">Designdetaljer: Integrering med lager</span><span class="sxs-lookup"><span data-stu-id="54931-103">Design Details: Integration with Inventory</span></span>
<span data-ttu-id="54931-104">Lagerledningsmodulen och lagermodulen interagerar med varandra i inventeringsjournalen och i lager- eller distributionslagerjustering.</span><span class="sxs-lookup"><span data-stu-id="54931-104">The Warehouse Management application area and the Inventory application area interact with one another in physical inventory and in inventory or warehouse adjustment.</span></span>  
  
## <a name="physical-inventory"></a><span data-ttu-id="54931-105">Physical Inventory</span><span class="sxs-lookup"><span data-stu-id="54931-105">Physical Inventory</span></span>  
 <span data-ttu-id="54931-106">Fönstret **Dist.lager inventeringsjournal** används med fönstret **Inventeringsjournal** för alla avancerade distributionslagerplatser.</span><span class="sxs-lookup"><span data-stu-id="54931-106">The **Whse. Phys. Inventory Journal** window is used with the **Phys. Inventory Journal** window for all advanced warehouse locations.</span></span> <span data-ttu-id="54931-107">Lagret på lagerplatsnivå beräknas, och en utskriven lista levereras till lagerpersonalen.</span><span class="sxs-lookup"><span data-stu-id="54931-107">The inventory on bin level is calculated, and a printed list is provided for the warehouse employee.</span></span> <span data-ttu-id="54931-108">Listan visar vilka artiklar i vilka lagerplatser som ska inventeras.</span><span class="sxs-lookup"><span data-stu-id="54931-108">The list shows which items in which bins must be counted.</span></span>  
  
 <span data-ttu-id="54931-109">Lagerpersonalen anger det räknade antalet i fönstret **Dist.lager inventeringsjournal** och bokför sedan journalen.</span><span class="sxs-lookup"><span data-stu-id="54931-109">The warehouse employee enters the counted quantity in the **Whse. Phys. Inventory Journal** window and then posts the journal.</span></span>  
  
 <span data-ttu-id="54931-110">Om det inventerade antalet är större än antalet på journalraden bokförs en transport för skillnaden från standardjusteringslagerplatsen till den inventerade lagerplatsen.</span><span class="sxs-lookup"><span data-stu-id="54931-110">If the counted quantity is greater than the quantity on the journal line, a movement is posted for this difference from the default adjustment bin to the counted bin.</span></span> <span data-ttu-id="54931-111">Det ökar antalet på den inventerade lagerplatsen och minskar antalet i standardjusteringlagerplatsen.</span><span class="sxs-lookup"><span data-stu-id="54931-111">This increases the quantity in the counted bin and decreases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="54931-112">Om det inventerade antalet är mindre än antalet på journalraden bokförs en transport för skillnaden från den inventerade lagerplatsen till standardjusteringslagerplatsen.</span><span class="sxs-lookup"><span data-stu-id="54931-112">If the quantity counted is less than the quantity on the journal line, a movement for this difference is posted from the counted bin to the default adjustment bin.</span></span> <span data-ttu-id="54931-113">Det minskar antalet på den inventerade lagerplatsen och ökar antalet i standardjusteringlagerplatsen.</span><span class="sxs-lookup"><span data-stu-id="54931-113">This decreases the quantity in the counted bin and increases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="54931-114">I avancerad lagerkonfiguration hämtas värdet i fältet **Beräknat antal** från artikeltransaktioner, och värdet i fältet **Antal inventerat** hämtas från distributionslagertransaktioner exklusive justeringslagerplatsinnehåll.</span><span class="sxs-lookup"><span data-stu-id="54931-114">In advanced warehouse configurations, the value in the **Quantity (Calculated)** field is retrieved from item ledger entries and the value in the **Quantity (Phys. Inventory)** field is retrieved from warehouse entries, excluding the adjustment bin content.</span></span> <span data-ttu-id="54931-115">Fältet **Antal** anger skillnaden mellan de första två fälten, som ska vara lika med innehållet på justeringslagerplatsen.</span><span class="sxs-lookup"><span data-stu-id="54931-115">The **Quantity** field specifies the difference between the first two fields, which should be equal to the contents of the adjustment bin.</span></span>  
  
 <span data-ttu-id="54931-116">När du bokför inventeringjournalen uppdateras lagret och standardjusteringlagerplatsen.</span><span class="sxs-lookup"><span data-stu-id="54931-116">When you post the physical inventory journal, the inventory and the default adjustment bin are updated.</span></span>  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a><span data-ttu-id="54931-117">Distributionslagerjusteringar till artikeltransaktioner</span><span class="sxs-lookup"><span data-stu-id="54931-117">Warehouse Adjustments to the Item Ledger</span></span>  
 <span data-ttu-id="54931-118">Du kan använda fönstret **Artikeljournal** och funktionen **Beräkna dist.lager justering** för att justera lagret i artikeltransaktioner i enlighet med en justering som har gjorts av objektantalet på en lagerplats i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="54931-118">You use the **Item Journal** window and the **Calculate Whse. Adjustment** function to adjust inventory on the item ledger in accordance with an adjustment that has been made to the item quantity in a warehouse bin.</span></span> <span data-ttu-id="54931-119">För att skapa en koppling mellan lagret och distributionslagret måste du definiera en standardjusteringlagerplats per lagerställe.</span><span class="sxs-lookup"><span data-stu-id="54931-119">To create a link between the inventory and the warehouse, you must define a default adjustment bin per location.</span></span>  
  
 <span data-ttu-id="54931-120">Standardjusteringlagerplatsen registrerar artiklar i distributionslagret när du bokför en ökning för lagret.</span><span class="sxs-lookup"><span data-stu-id="54931-120">The default adjustment bin registers items in the warehouse when you post an increase for the inventory.</span></span> <span data-ttu-id="54931-121">Om du bokför en minskning, minskas antalet på lagerplatsen också.</span><span class="sxs-lookup"><span data-stu-id="54931-121">However, if you post a decrease, the quantity on the default bin is also decreased.</span></span> <span data-ttu-id="54931-122">I båda fallen skapas artikeltransaktioner och distributionslagerposter.</span><span class="sxs-lookup"><span data-stu-id="54931-122">In both cases, item ledger entries and warehouse entries are created.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="54931-123">Justeringslagerplatsen inkluderas inte i dispositionsberäkningarna.</span><span class="sxs-lookup"><span data-stu-id="54931-123">The adjustment bin is not included in the availability calculation.</span></span>  
  
 <span data-ttu-id="54931-124">Om du vill justera lagerplatsinnehåll kan du använda distributionslagerartikeljournalen, från vilken du kan ange artikelnummer, zonkoden, lagerplatskod och antal som du vill justera.</span><span class="sxs-lookup"><span data-stu-id="54931-124">If you want to adjust the bin content, you can use the warehouse item journal, from which you can enter the item number, zone code, bin code, and quantity that you want to adjust.</span></span>  
  
 <span data-ttu-id="54931-125">Om du anger ett positivt antal och bokför raden ökar lagret som lagras på lagerplatsen, och antalet på standardjusteringslagerplatsen minskar på motsvarande sätt.</span><span class="sxs-lookup"><span data-stu-id="54931-125">If you enter a positive quantity and post the line, then the inventory stored in the bin increases, and the quantity of the default adjustment bin decreases correspondingly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="54931-126">Se även</span><span class="sxs-lookup"><span data-stu-id="54931-126">See Also</span></span>  
 <span data-ttu-id="54931-127">[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md) </span><span class="sxs-lookup"><span data-stu-id="54931-127">[Design Details: Warehouse Management](design-details-warehouse-management.md) </span></span>  
 [<span data-ttu-id="54931-128">Designdetaljer: Disposition i distributionslagret</span><span class="sxs-lookup"><span data-stu-id="54931-128">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)
