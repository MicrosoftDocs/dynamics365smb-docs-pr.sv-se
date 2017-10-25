---
title: Hantera lagerkostnader | Microsoft Docs
description: "Kostnadshantering används vid registrering och rapportering av rörelsens driftskostnader. Den omfattar rapportering av tillverkningskostnader och lagerkostnader, det vill säga varornas värdet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8da779426dfd06519507796c995adcedcd40ac81
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="managing-inventory-costs"></a><span data-ttu-id="ea369-104">Hantera lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="ea369-104">Managing Inventory Costs</span></span>
<span data-ttu-id="ea369-105">Kostnadshantering används vid registrering och rapportering av rörelsens driftskostnader.</span><span class="sxs-lookup"><span data-stu-id="ea369-105">Cost management, also referred to as “costing”, is concerned with recording and reporting business operating costs.</span></span> <span data-ttu-id="ea369-106">Den omfattar rapportering av tillverkningskostnader och lagerkostnader, det vill säga varornas värdet.</span><span class="sxs-lookup"><span data-stu-id="ea369-106">It includes the reporting of manufacturing costs and inventory costs, that is, the value of items.</span></span>   

<span data-ttu-id="ea369-107">Inom kostnadskalkylering måste du vara medveten om att värderingsprinciper anger hur varor värderas när de lämnar lagret, att kostnadsjusteringen uppdaterar kostnaderna för sålda varor med relaterad inköpskostnad som bokförs efter försäljningen och att lagervärdena måste bokföras på särskilda redovisningskonton med jämna mellanrum.</span><span class="sxs-lookup"><span data-stu-id="ea369-107">Central principles to understand are that costing methods define how items are valued when they leave inventory, that cost adjustment updates the cost of goods sold with related purchase costs posted after the sale, and that inventory values must be posted to dedicated G/L accounts at regular intervals.</span></span>

<span data-ttu-id="ea369-108">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="ea369-108">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="ea369-109">**Om du vill**</span><span class="sxs-lookup"><span data-stu-id="ea369-109">**To**</span></span>|<span data-ttu-id="ea369-110">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="ea369-110">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="ea369-111">Läs information om olika begrepp för att förstå principerna och definitionerna som styr lagerkostnadsredovisningsfunktionen i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ea369-111">Read various conceptual information to understand the principles and definitions that govern the inventory costing accounting functionality in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span></span>|[<span data-ttu-id="ea369-112">Om Lagerkostnad</span><span class="sxs-lookup"><span data-stu-id="ea369-112">About Inventory Costing</span></span>](finance-learn-about-costing.md)|  
|<span data-ttu-id="ea369-113">Ställ in lagerperioder, värderingsprinciper och avrundningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="ea369-113">Set up inventory periods, costing methods, and rounding methods.</span></span>|[<span data-ttu-id="ea369-114">Ställa in lagervärdering och lagerkostnad</span><span class="sxs-lookup"><span data-stu-id="ea369-114">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)|
|<span data-ttu-id="ea369-115">Uppskatta eller skriv av värdet av en eller flera artiklar i lager genom att bokföra deras faktiska, beräknade värde.</span><span class="sxs-lookup"><span data-stu-id="ea369-115">Appreciate or depreciate the value of one or more items in inventory by posting their current, calculated value.</span></span>|[<span data-ttu-id="ea369-116">Så här omvärderar du lager</span><span class="sxs-lookup"><span data-stu-id="ea369-116">How to: Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="ea369-117">Justera artikelkostnader, antingen automatiskt eller manuellt, för att vidarebefordra kostnadsförändringar från ingående transaktioner till deras relaterade utgående transaktioner.</span><span class="sxs-lookup"><span data-stu-id="ea369-117">Adjust item costs, either automatically or manually, to forward cost changes from inbound entries to their related outbound entries.</span></span>|[<span data-ttu-id="ea369-118">Så här justerar du artikelkostnader</span><span class="sxs-lookup"><span data-stu-id="ea369-118">How to: Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|
|<span data-ttu-id="ea369-119">Använda särskild kostnadsberäkning för dagligen återkommande artikeltransaktioner i artikeloperationer.</span><span class="sxs-lookup"><span data-stu-id="ea369-119">Use special costing functions for every-day item transactions in the item operations.</span></span>|[<span data-ttu-id="ea369-120">Hantera lager- och produktionskostnader</span><span class="sxs-lookup"><span data-stu-id="ea369-120">Handling Inventory and Manufacturing Costs</span></span>](finance-handle-inventory-and-manufacturing-costs.md)|  
|<span data-ttu-id="ea369-121">Du måste regelbundet uppdatera standardkostnader för komponenter i monterings- eller produktionsstrukturer och överföra de nya kostnaderna till den överordnade artikeln.</span><span class="sxs-lookup"><span data-stu-id="ea369-121">Periodically update the standard costs of components, in assembly or production BOMs, and roll the new costs up to the parent item.</span></span>|[<span data-ttu-id="ea369-122">Så här kan du uppdatera standardkostnader</span><span class="sxs-lookup"><span data-stu-id="ea369-122">How to: Update Standard Costs</span></span>](finance-how-to-update-standard-costs.md)|
|<span data-ttu-id="ea369-123">utföra kontroll- och rapporteringsuppgifter vid periodslut, till exempel beräkna lagervärdet och bokföra kostnader i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="ea369-123">Perform period-end control and reporting tasks, such calculate the value of inventory and post costs to the general ledger.</span></span>|[<span data-ttu-id="ea369-124">Rapportera kostnader och stämma av med redovisningen</span><span class="sxs-lookup"><span data-stu-id="ea369-124">Reporting Costs and Reconciling with the General Ledger</span></span>](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|<span data-ttu-id="ea369-125">Lär dig om alla funktioner i kostnadssystemet.</span><span class="sxs-lookup"><span data-stu-id="ea369-125">Learn about all mechanisms in the costing system.</span></span>|[<span data-ttu-id="ea369-126">Designdetaljer: Lagerkalkylering</span><span class="sxs-lookup"><span data-stu-id="ea369-126">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  

## <a name="see-also"></a><span data-ttu-id="ea369-127">Se även</span><span class="sxs-lookup"><span data-stu-id="ea369-127">See Also</span></span>  
 [<span data-ttu-id="ea369-128">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="ea369-128">Finance</span></span>](finance.md)  
 <span data-ttu-id="ea369-129">[Lagersaldo](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="ea369-129">[Inventory](inventory-manage-inventory.md) </span></span>  
 <span data-ttu-id="ea369-130">[Försäljning](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="ea369-130">[Sales](sales-manage-sales.md) </span></span>  
 [<span data-ttu-id="ea369-131">Inköp</span><span class="sxs-lookup"><span data-stu-id="ea369-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="ea369-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ea369-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

