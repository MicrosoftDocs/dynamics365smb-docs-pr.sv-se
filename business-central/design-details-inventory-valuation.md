---
title: Designdetaljer - Lagervärdering | Microsoft Docs
description: Lagervärdering XE är fastställandet av kostnaden som tilldelats en lagerartikel, som uttryckt i följande ekvation.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1321c9cfdb3814802db295eb7f5dcc90b325c19e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "936722"
---
# <a name="design-details-inventory-valuation"></a><span data-ttu-id="e70c4-103">Designdetaljer: Lagervärdering</span><span class="sxs-lookup"><span data-stu-id="e70c4-103">Design Details: Inventory Valuation</span></span>
<span data-ttu-id="e70c4-104">Lagervärdering XE är fastställandet av kostnaden som tilldelats en lagerartikel, som uttryckt i följande ekvation.</span><span class="sxs-lookup"><span data-stu-id="e70c4-104">Inventory valuation XE "Inventory Valuation"  is the determination of the cost that is assigned to an inventory item, as expressed by the following equation.</span></span>  

<span data-ttu-id="e70c4-105">Slutlager = startlager + nettoinköp – kostnaden för sålda varor</span><span class="sxs-lookup"><span data-stu-id="e70c4-105">Ending inventory = beginning inventory + net purchases – cost of goods sold</span></span>  

<span data-ttu-id="e70c4-106">Beräkningen av lagervärderingen använder fältet **Kost.belopp (aktuellt)** i värdetransaktionerna för artikeln.</span><span class="sxs-lookup"><span data-stu-id="e70c4-106">The calculation of inventory valuation uses the **Cost Amount (Actual)** field of the value entries for the item.</span></span> <span data-ttu-id="e70c4-107">Transaktionerna klassificeras efter transaktionstypen XE "transaktionstyp" som motsvarar kostnadskomponenter, direkt kostnad, indirekt kostnad, avvikelse, omvärdering och avrundning.</span><span class="sxs-lookup"><span data-stu-id="e70c4-107">The entries are classified according to the entry type XE "Entry Type"  that corresponds to the cost components, direct cost, indirect cost, variance, revaluation, and rounding.</span></span> <span data-ttu-id="e70c4-108">Mer information finns i [Designdetaljer: kostnadskomponenter](design-details-cost-components.md).</span><span class="sxs-lookup"><span data-stu-id="e70c4-108">For more information, see [Design Details: Cost Components](design-details-cost-components.md).</span></span>  

<span data-ttu-id="e70c4-109">Transaktioner har kopplats mot varandra, antingen av fasta kopplingar XE "koppling; fast" eller enligt det allmänna antagandet om kostnadsflöde som definieras av värderingsprincipen XE "princip; kostnad" XE "kostnadsprincip"</span><span class="sxs-lookup"><span data-stu-id="e70c4-109">Entries are applied against each other, either by the fixed application XE "Application; Fixed" , or according to the general cost-flow assumption defined by the costing method XE "Method; Costing"  XE "Costing Method" .</span></span> <span data-ttu-id="e70c4-110">En transaktion med lagerminskning kan kopplas till flera ökningar med olika bokföringsdatum och eventuellt olika anskaffningskostnader XE "anskaffningskostnader".</span><span class="sxs-lookup"><span data-stu-id="e70c4-110">One entry of inventory decrease can be applied to more than one increase entry with different posting dates and possibly different acquisition cost XE "Acquisition Cost" s.</span></span> <span data-ttu-id="e70c4-111">Mer information finns i [Designdetaljer: Artikelkoppling](design-details-item-application.md).</span><span class="sxs-lookup"><span data-stu-id="e70c4-111">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span> <span data-ttu-id="e70c4-112">Därför baseras beräkningen av lagervärdet  XE "Lagervärde" för ett givet datum på summan av positiva och negativa värdetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="e70c4-112">Therefore, calculation of the inventory value XE "Inventory Value"  for a given date is based on summing up positive and negative value entries.</span></span>  

## <a name="inventory-valuation-report"></a><span data-ttu-id="e70c4-113">Lagervärdering - rapport</span><span class="sxs-lookup"><span data-stu-id="e70c4-113">Inventory Valuation report</span></span>  
<span data-ttu-id="e70c4-114">För att beräkna lagervärdet i rapporten **Lagervärdering** börjar rapporten med att beräkna värdet för artikelns lager på ett visst startdatum.</span><span class="sxs-lookup"><span data-stu-id="e70c4-114">To calculate the inventory value in the **Inventory Valuation** report, the report begins by calculating the value of the item’s inventory at a given starting date.</span></span> <span data-ttu-id="e70c4-115">Det lägger till värdet av lagerökningar och subtraherar sedan värdet av lagerminskningar upp till ett visst slutdatum.</span><span class="sxs-lookup"><span data-stu-id="e70c4-115">It then adds the value of inventory increases and subtracts the value of inventory decreases up to a given ending date.</span></span> <span data-ttu-id="e70c4-116">Slutresultatet är lagervärdet på slutdatumet.</span><span class="sxs-lookup"><span data-stu-id="e70c4-116">The end result is the inventory value on the ending date.</span></span> <span data-ttu-id="e70c4-117">Rapporten beräknar dessa värden genom att summera värdena i fältet **Kost.belopp (aktuellt)** i värdetransaktionerna, med hjälp av bokföringsdatum som filter.</span><span class="sxs-lookup"><span data-stu-id="e70c4-117">The report calculates these values by summing the values in the **Cost Amount (Actual)** field in the value entries, using the posting dates as filters.</span></span>  

<span data-ttu-id="e70c4-118">I den utskrivna rapporten visas alltid faktiska belopp, d.v.s. kostnaden för transaktioner som har bokförts som fakturerade.</span><span class="sxs-lookup"><span data-stu-id="e70c4-118">The printed report always shows actual amounts, that is, the cost of entries that have been posted as invoiced.</span></span> <span data-ttu-id="e70c4-119">Om du markerar fältet Ta med förväntad kostnad på snabbfliken Alternativ visas även den förväntade kostnaden för transaktioner som har bokförts som inlevererade eller utlevererade.</span><span class="sxs-lookup"><span data-stu-id="e70c4-119">The report will also print the expected cost of entries that have posted as received or shipped, if you select the Include Expected Cost field on the Options FastTab.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="e70c4-120">Värden i den rapporten **Lagervärdering** stäms av med lagerkontot i redovisningen vilket betyder att värdetransaktionerna i fråga har bokförts i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="e70c4-120">Values in the **Inventory Valuation** report is reconciled with the Inventory account in the general ledger, meaning the value entries in question have been posted to the general ledger.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="e70c4-121">Beloppen i kolumnerna **Värde** i rapporten baseras på bokföringsdatumet för transaktioner för en artikel.</span><span class="sxs-lookup"><span data-stu-id="e70c4-121">Amounts in the **Value** columns of the report are based on the posting date of transactions for an item.</span></span>  

## <a name="inventory-valuation---wip-report"></a><span data-ttu-id="e70c4-122">Lagervärdering - PIA-rapport</span><span class="sxs-lookup"><span data-stu-id="e70c4-122">Inventory Valuation - WIP report</span></span>  
<span data-ttu-id="e70c4-123">Ett produktionsföretag måste bestämma värdet av tre typer av lager:</span><span class="sxs-lookup"><span data-stu-id="e70c4-123">A manufacturing company needs to determine the value of three types of inventory:</span></span>  

* <span data-ttu-id="e70c4-124">Råmateriallager</span><span class="sxs-lookup"><span data-stu-id="e70c4-124">Raw Materials inventory</span></span>  
* <span data-ttu-id="e70c4-125">PIA-lager</span><span class="sxs-lookup"><span data-stu-id="e70c4-125">WIP inventory</span></span>  
* <span data-ttu-id="e70c4-126">Färdiga varor i lager</span><span class="sxs-lookup"><span data-stu-id="e70c4-126">Finished Goods inventory</span></span>  

<span data-ttu-id="e70c4-127">Värdet i PIA-lagret bestäms av efterföljande ekvation:</span><span class="sxs-lookup"><span data-stu-id="e70c4-127">The value of WIP inventory is determined by the following equation:</span></span>  

* <span data-ttu-id="e70c4-128">Avslutande PIA-lager = Start-PIA-lager + produktionskostnader – kostnaden för tillverkade varor</span><span class="sxs-lookup"><span data-stu-id="e70c4-128">Ending WIP inventory = Beginning WIP inventory + manufacturing costs – cost of goods manufactured</span></span>  

<span data-ttu-id="e70c4-129">När det gäller inköpt lager utgör värdetransaktioner grunden för lagervärderingen.</span><span class="sxs-lookup"><span data-stu-id="e70c4-129">As for purchased inventory, the value entries provide the basis of the inventory valuation.</span></span> <span data-ttu-id="e70c4-130">Beräkningen görs med hjälp av värdena i fältet **Kost.belopp (aktuellt)** för artikel- och kapacitetvärdetransaktionerna som är kopplade till en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="e70c4-130">The calculation is made using the values in the **Cost Amount (Actual)** field of the item and capacity value entries associated with a production order.</span></span>  

<span data-ttu-id="e70c4-131">Avsikten med PIA-lagervärderingen är att fastställa värdet för artiklarna vars tillverkning ännu inte har slutförts på ett givet datum.</span><span class="sxs-lookup"><span data-stu-id="e70c4-131">The purpose of WIP inventory valuation is to determine the value of the items whose manufacturing has not yet been completed on a given date.</span></span> <span data-ttu-id="e70c4-132">Därför baseras PIA-lagervärdet på de värdetransaktioner som är kopplade till förbrukningen och kapacitetstransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="e70c4-132">Therefore the WIP inventory value is based on the value entries related to the consumption and capacity ledger entries.</span></span> <span data-ttu-id="e70c4-133">Förbrukningstransaktioner måste vara helt fakturerade vid datumet för värderingen.</span><span class="sxs-lookup"><span data-stu-id="e70c4-133">Consumption ledger entries must be completely invoiced at the date of the valuation.</span></span> <span data-ttu-id="e70c4-134">Därför visar rapporten **Lagervärdering - PIA** kostnaderna som representerar PIA-lagervärdet i två kategorier: förbrukning och kapacitet.</span><span class="sxs-lookup"><span data-stu-id="e70c4-134">Therefore, the **Inventory Valuation – WIP** report shows the costs representing the WIP inventory value in two categories: consumption and capacity.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e70c4-135">Se även</span><span class="sxs-lookup"><span data-stu-id="e70c4-135">See Also</span></span>  
<span data-ttu-id="e70c4-136">[Designdetaljer: Avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="e70c4-136">[Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md) </span></span>  
<span data-ttu-id="e70c4-137">[Designdetaljer: Omvärdering](design-details-revaluation.md) </span><span class="sxs-lookup"><span data-stu-id="e70c4-137">[Design Details: Revaluation](design-details-revaluation.md) </span></span>  
<span data-ttu-id="e70c4-138">[Designdetaljer: Bokföring av produktionsorder](design-details-production-order-posting.md)
[Hantera lagerkostnader](finance-manage-inventory-costs.md)</span><span class="sxs-lookup"><span data-stu-id="e70c4-138">[Design Details: Production Order Posting](design-details-production-order-posting.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md)</span></span>  
[<span data-ttu-id="e70c4-139">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="e70c4-139">Finance</span></span>](finance.md)  
<span data-ttu-id="e70c4-140">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e70c4-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
