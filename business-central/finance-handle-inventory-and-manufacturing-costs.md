---
title: Hantera lager- och produktionskostnader | Microsoft Docs
description: "Många av funktionerna inom kostnadskalkylering utförs i underliggande processer som användaren inte behöver bry sig om, till exempel transaktionskoppling och automatisk kostnadsjustering, men ett antal fält, fönster och rapporter riktar sig mot användare som direkt eller indirekt hanterar kostnader för artiklar eller driften."
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
ms.openlocfilehash: 7ee3f25cb08a1224445f10b9dfee61267c24aad2
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="handling-inventory-and-manufacturing-costs"></a><span data-ttu-id="69517-103">Hantera lager- och produktionskostnader</span><span class="sxs-lookup"><span data-stu-id="69517-103">Handling Inventory and Manufacturing Costs</span></span>
<span data-ttu-id="69517-104">Många av funktionerna inom kostnadskalkylering utförs i underliggande processer som användaren inte behöver bry sig om, till exempel transaktionskoppling och automatisk kostnadsjustering, men ett antal fält, fönster och rapporter riktar sig mot användare som direkt eller indirekt hanterar kostnader för artiklar eller driften.</span><span class="sxs-lookup"><span data-stu-id="69517-104">Although much of the cost accounting functionality is expressed in underlying processes with no user interaction, such as entry application and automatic cost adjustment, a number of fields, windows, and reports are aimed at users who directly or indirectly manage the cost of items or operations.</span></span>  

 <span data-ttu-id="69517-105">Att tilldela artikelomkostnader till inköpsdokument är ett exempel på en indirekt uppgift inom kostnadskalkylering.</span><span class="sxs-lookup"><span data-stu-id="69517-105">Assigning item charges to purchase documents is an example of an indirect cost accounting task.</span></span> <span data-ttu-id="69517-106">Att uppdatera styckkostnad för en artikel i monterings- eller produktionsstrukturen är ett exempel på en mer direkt uppgift inom kostnadskalkylering.</span><span class="sxs-lookup"><span data-stu-id="69517-106">Updating the unit cost of assembly or production BOM item is an example of a more direct cost accounting task.</span></span>  

 <span data-ttu-id="69517-107">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="69517-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="69517-108">**Om du vill**</span><span class="sxs-lookup"><span data-stu-id="69517-108">**To**</span></span>|<span data-ttu-id="69517-109">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="69517-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="69517-110">regelbundet eller automatiskt uppdatera styckkostnaden för en eller flera artiklar så att alla kostnadsändringar från ankommande transaktioner, till exempel de för inköp eller produktionsutflöde, flyttas fram till relaterade avgående transaktioner, till exempel försäljningar eller överföringar.</span><span class="sxs-lookup"><span data-stu-id="69517-110">Periodically or automatically update the unit cost of one or multiple items to forward any cost changes from inbound entries, such as those for purchases or production output, to the related outbound entries, such as consumption or transfers.</span></span>|[<span data-ttu-id="69517-111">Justera artikelkostnader</span><span class="sxs-lookup"><span data-stu-id="69517-111">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="69517-112">få en inblick i genomsnittskostnadsdynamiken för att fatta beslut om prissättning eller spåra kostnadsfluktuationer orsakade av informationsregistreringsfel.</span><span class="sxs-lookup"><span data-stu-id="69517-112">Get insight into average cost dynamics to make pricing decisions or to track cost fluctuations caused by data entry errors.</span></span>|[<span data-ttu-id="69517-113">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="69517-113">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="69517-114">skapa en produktionsartikels standardkostnad genom att ange de tre kostnadsslagen: materialkostnad, kapacitetskostnad och underleverantörskostnad.</span><span class="sxs-lookup"><span data-stu-id="69517-114">Create a manufacturing item's standard cost by entering the three cost elements: material cost, capacity cost, and subcontractor cost.</span></span>|[<span data-ttu-id="69517-115">Om beräkning av standardkostnad</span><span class="sxs-lookup"><span data-stu-id="69517-115">About Calculating Standard Cost</span></span>](finance-about-calculating-standard-cost.md)|  
|<span data-ttu-id="69517-116">beräkna styckkostnaden för en strukturartikel baserat på styckkostnaderna för dess underliggande komponenter.</span><span class="sxs-lookup"><span data-stu-id="69517-116">Calculate the unit cost of a BOM item based on the unit costs of its underlying components.</span></span>|[<span data-ttu-id="69517-117">Arbeta med strukturer</span><span class="sxs-lookup"><span data-stu-id="69517-117">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)|  
|<span data-ttu-id="69517-118">slutföra kostnadskalkyleringslivscykeln för en producerad artikel genom att justera kostnaderna och stämma av värdetransaktionerna med redovisningen.</span><span class="sxs-lookup"><span data-stu-id="69517-118">Complete the costing life cycle of a produced item by adjusting the costs and reconciling the value entries with the general ledger.</span></span>|[<span data-ttu-id="69517-119">Om kostnader för färdiga produktionsorder</span><span class="sxs-lookup"><span data-stu-id="69517-119">About Finished Production Order Costs</span></span>](finance-about-finished-production-order-costs.md)|  
|<span data-ttu-id="69517-120">ändra värdet för en artikel i lager eller värdet för en artikeltransaktion, till exempel en inköpstransaktion.</span><span class="sxs-lookup"><span data-stu-id="69517-120">Change the value of an item in inventory or the value of one item ledger entry, such as a purchase transaction.</span></span>|[<span data-ttu-id="69517-121">Omvärdera lager</span><span class="sxs-lookup"><span data-stu-id="69517-121">Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="69517-122">manuellt ångra en artikelkoppling eller koppla om artikeltransaktioner som skapats i programmet.</span><span class="sxs-lookup"><span data-stu-id="69517-122">Manually undo an item application or reapply item ledger entries created by the program.</span></span>|[<span data-ttu-id="69517-123">Ta bort och koppla om artikeltransaktioner</span><span class="sxs-lookup"><span data-stu-id="69517-123">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)|  
|<span data-ttu-id="69517-124">Du kan använda fältet **Kopplas från löpnr** i artikeljournal för att skapa en fast koppling mellan en inkommande transaktion och den ursprungliga utgående transaktionen.</span><span class="sxs-lookup"><span data-stu-id="69517-124">Use the **Applies-from Entry** field in the item journal to manually create a fixed application between an inbound transaction and the original outbound transaction.</span></span>|[<span data-ttu-id="69517-125">Avsluta öppna artikeltransaktioner som skapas från en fast koppling i artikeljournalen</span><span class="sxs-lookup"><span data-stu-id="69517-125">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a><span data-ttu-id="69517-126">Se även</span><span class="sxs-lookup"><span data-stu-id="69517-126">See Also</span></span>  
<span data-ttu-id="69517-127">[Hantera lagerkostnader](finance-manage-inventory-costs.md)
[Designdetaljer: Lagerkostnad](design-details-inventory-costing.md)</span><span class="sxs-lookup"><span data-stu-id="69517-127">[Manage Inventory Costs](finance-manage-inventory-costs.md)
[Design Details: Inventory Costing](design-details-inventory-costing.md)</span></span>

