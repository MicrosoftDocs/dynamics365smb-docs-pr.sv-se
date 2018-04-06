---
title: "Automatisk överföring och kombinerade transaktioner | Microsoft Docs"
description: "I kostnadsredovisningen kan du överföra redovisningstransaktioner till en kostnadstyp, genom att använda en kombinerad bokföring. Du kan ange om en kostnadstyp tar emot kombinerade transaktioner i fältet **Kombinera transaktioner** i kostnadstypsdefinitionen. Alternativen beskrivs i tabellen nedan."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f4796d9796788d2fbbf5706688aec75a4ed9a6d8
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="d465d-105">Automatisk överföring och kombinerade transaktioner</span><span class="sxs-lookup"><span data-stu-id="d465d-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="d465d-106">I kostnadsredovisningen kan du överföra redovisningstransaktioner till en kostnadstyp, genom att använda en kombinerad bokföring.</span><span class="sxs-lookup"><span data-stu-id="d465d-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="d465d-107">Du kan ange om en kostnadstyp tar emot kombinerade transaktioner i fältet **Kombinera transaktioner** i kostnadstypsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d465d-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="d465d-108">Alternativen beskrivs i tabellen nedan.</span><span class="sxs-lookup"><span data-stu-id="d465d-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="d465d-109">Kombinera transaktioner</span><span class="sxs-lookup"><span data-stu-id="d465d-109">Combine entries</span></span>|<span data-ttu-id="d465d-110">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d465d-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="d465d-111">Ingen</span><span class="sxs-lookup"><span data-stu-id="d465d-111">None</span></span>|<span data-ttu-id="d465d-112">Varje redovisningstransaktion överförs individuellt till motsvarande kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="d465d-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="d465d-113">Dag</span><span class="sxs-lookup"><span data-stu-id="d465d-113">Day</span></span>|<span data-ttu-id="d465d-114">Redovisningstransaktioner med samma bokföringsdatum överförs som en post till motsvarande kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="d465d-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="d465d-115">Månad</span><span class="sxs-lookup"><span data-stu-id="d465d-115">Month</span></span>|<span data-ttu-id="d465d-116">Alla redovisningstransaktioner i samma kalendermånad överförs som en post till motsvarande kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="d465d-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="d465d-117">Om du har markerat kryssrutan **Automatisk överföring från redovisning** i fönstret **Inställningar för kostnadsredovisning**, [!INCLUDE[d365fin](includes/d365fin_md.md)] uppdaterar kostnadsredovisningen efter varje bokföring i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="d465d-117">If you have selected the **Auto Transfer from G/L** check box in the **Cost Accounting Setup** window, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="d465d-118">Kombinerade transaktioner är inte möjliga.</span><span class="sxs-lookup"><span data-stu-id="d465d-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d465d-119">Se även</span><span class="sxs-lookup"><span data-stu-id="d465d-119">See Also</span></span>  
 <span data-ttu-id="d465d-120">[Överföra redovisningstransaktioner till kostnadstransaktioner](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="d465d-120">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="d465d-121">[Villkor för överföring av redovisningstransaktioner till kostnadstransaktioner](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="d465d-121">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="d465d-122">[Resultat av överföringen](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="d465d-122">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 [<span data-ttu-id="d465d-123">Överföra och bokföra kostnadstransaktioner</span><span class="sxs-lookup"><span data-stu-id="d465d-123">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  
 <span data-ttu-id="d465d-124">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d465d-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

