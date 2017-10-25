---
title: "Rapportera kostnader och stämma av med redovisningen | Microsoft Docs"
description: "I slutet av bokföringsperioden varje månad, år eller annat – måste en serie uppgifter för kostnadskontroll och revision utföras så att ett korrekt och balanserat lagervärde rapporteras till ekonomiavdelningen. Förutom bokföringsrutinen som överför enskilda artikelvärdetransaktioner till särskilda redovisningskonton finns det flera rapporter, spårningsfunktioner och speciella avstämningsverktyg som revisorn eller controllern kan använda."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3c3a02aa2251b9b6b18576e9f274d018a617b179
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="reporting-costs-and-reconciling-with-the-general-ledger"></a><span data-ttu-id="590c6-104">Rapportera kostnader och stämma av med redovisningen</span><span class="sxs-lookup"><span data-stu-id="590c6-104">Reporting Costs and Reconciling with the General Ledger</span></span>
<span data-ttu-id="590c6-105">I slutet av bokföringsperioden varje månad, år eller annat – måste en serie uppgifter för kostnadskontroll och revision utföras så att ett korrekt och balanserat lagervärde rapporteras till ekonomiavdelningen.</span><span class="sxs-lookup"><span data-stu-id="590c6-105">At the end of accounting periods, monthly, yearly or other, a sequence of cost control and auditing tasks must be performed to report a correct and balanced inventory value to the finance department.</span></span> <span data-ttu-id="590c6-106">Förutom bokföringsrutinen som överför enskilda artikelvärdetransaktioner till särskilda redovisningskonton finns det flera rapporter, spårningsfunktioner och speciella avstämningsverktyg som revisorn eller controllern kan använda.</span><span class="sxs-lookup"><span data-stu-id="590c6-106">Apart from the posting routine that transfers the individual item value entries to dedicated general ledger accounts, several reports, tracing functions, and a special reconciliation tool are available to the auditor or controller responsible for this business-critical work.</span></span>  

 <span data-ttu-id="590c6-107">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="590c6-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="590c6-108">**Om du vill**</span><span class="sxs-lookup"><span data-stu-id="590c6-108">**To**</span></span>|<span data-ttu-id="590c6-109">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="590c6-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="590c6-110">visa lagervärdet för valda artiklar, inklusive information om kvantiteter och värden på ökningar och minskningar i lager över en vald period.</span><span class="sxs-lookup"><span data-stu-id="590c6-110">View the inventory value of selected items, including information about the quantities and values of increases and decreases in inventory over a selected period.</span></span>|<span data-ttu-id="590c6-111">**Lagervärdering**-rapport</span><span class="sxs-lookup"><span data-stu-id="590c6-111">**Inventory Valuation** report</span></span>|  
|<span data-ttu-id="590c6-112">visa lagervärdet för valda produktionsorder i ditt PIA-lager (produkter i arbete), till exempel kvantiteterna och värdena på förbrukning, kapacitetsförbrukning och utflöde i pågående produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="590c6-112">View the inventory value of selected production orders in your WIP (work in process) inventory, such as the quantities and values of consumption, capacity usage, and output in ongoing production orders.</span></span>|<span data-ttu-id="590c6-113">**Lagervärdering - WIP**-rapport</span><span class="sxs-lookup"><span data-stu-id="590c6-113">**Inventory Valuation - WIP** report</span></span>|  
|<span data-ttu-id="590c6-114">visa lagervärdet på valda artiklar, inklusive deras faktiska och förväntade kostnad på det angivna datumet.</span><span class="sxs-lookup"><span data-stu-id="590c6-114">View the inventory value of selected items, including their actual and expected cost on the date specified.</span></span>|<span data-ttu-id="590c6-115">**Lagervärdering - kost.spec.**-rapport</span><span class="sxs-lookup"><span data-stu-id="590c6-115">**Invt. Valuation - Cost Spec.** report</span></span>|  
|<span data-ttu-id="590c6-116">använda en rapport för att analysera orsakerna till kostnadsvariationer eller för att få information om kostnadsandelarna för sålda artiklar (KSV).</span><span class="sxs-lookup"><span data-stu-id="590c6-116">Use a report to analyze the reasons for cost variances or to gain insight into the cost shares of sold items (COGS).</span></span>|<span data-ttu-id="590c6-117">**Kostnadsandelar - analys**-rapport</span><span class="sxs-lookup"><span data-stu-id="590c6-117">**Cost Shares Breakdown** report</span></span>|  
|<span data-ttu-id="590c6-118">regelbundet bokföra värdetransaktionerna för artikeltransaktioner från inventeringen till relaterade redovisningskonton för att stämma av de båda bokföringsböckerna.</span><span class="sxs-lookup"><span data-stu-id="590c6-118">Periodically post the value entries of item transactions from the inventory ledger to the related G/L accounts to reconcile the two ledgers.</span></span>|[<span data-ttu-id="590c6-119">Så här kan du Stämma av lagerkostnader med redovisningen</span><span class="sxs-lookup"><span data-stu-id="590c6-119">How to: Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="590c6-120">använda ett fönster för att granska avstämningen mellan inventeringen och redovisningen.</span><span class="sxs-lookup"><span data-stu-id="590c6-120">Use one window to audit the reconciliation between the inventory ledger and the general ledger.</span></span>|[<span data-ttu-id="590c6-121">Så här kan du Stämma av lagerkostnader med redovisningen</span><span class="sxs-lookup"><span data-stu-id="590c6-121">How to: Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="590c6-122">fastställa PIA-beloppet som måste bokföras på balansräkningskonton för periodslutsrapportering.</span><span class="sxs-lookup"><span data-stu-id="590c6-122">Determine the WIP amount that needs to be posted to balance sheet accounts for period-end reporting.</span></span>|[<span data-ttu-id="590c6-123">Så här övervakar du projektets framsteg och resultat</span><span class="sxs-lookup"><span data-stu-id="590c6-123">How to: Monitor Job Progress and Performance</span></span>](projects-how-monitor-progress-performance.md)|

## <a name="see-also"></a><span data-ttu-id="590c6-124">Se även</span><span class="sxs-lookup"><span data-stu-id="590c6-124">See Also</span></span>  
[<span data-ttu-id="590c6-125">Ställa in lagervärdering och lagerkostnad</span><span class="sxs-lookup"><span data-stu-id="590c6-125">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="590c6-126">Hantera lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="590c6-126">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="590c6-127">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="590c6-127">Finance</span></span>](finance.md)  
<span data-ttu-id="590c6-128">[Lagersaldo](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="590c6-128">[Inventory](inventory-manage-inventory.md) </span></span>  
<span data-ttu-id="590c6-129">[Försäljning](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="590c6-129">[Sales](sales-manage-sales.md) </span></span>  
[<span data-ttu-id="590c6-130">Inköp</span><span class="sxs-lookup"><span data-stu-id="590c6-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="590c6-131">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="590c6-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
