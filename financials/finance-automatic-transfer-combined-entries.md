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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bd80d0a7a701256dfdae3346e899b84eeb990a40
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="373e7-105">Automatisk överföring och kombinerade transaktioner</span><span class="sxs-lookup"><span data-stu-id="373e7-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="373e7-106">I kostnadsredovisningen kan du överföra redovisningstransaktioner till en kostnadstyp, genom att använda en kombinerad bokföring.</span><span class="sxs-lookup"><span data-stu-id="373e7-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="373e7-107">Du kan ange om en kostnadstyp tar emot kombinerade transaktioner i fältet **Kombinera transaktioner** i kostnadstypsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="373e7-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="373e7-108">Alternativen beskrivs i tabellen nedan.</span><span class="sxs-lookup"><span data-stu-id="373e7-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="373e7-109">Kombinera transaktioner</span><span class="sxs-lookup"><span data-stu-id="373e7-109">Combine entries</span></span>|<span data-ttu-id="373e7-110">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="373e7-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="373e7-111">Ingen</span><span class="sxs-lookup"><span data-stu-id="373e7-111">None</span></span>|<span data-ttu-id="373e7-112">Varje redovisningstransaktion överförs individuellt till motsvarande kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="373e7-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="373e7-113">Dag</span><span class="sxs-lookup"><span data-stu-id="373e7-113">Day</span></span>|<span data-ttu-id="373e7-114">Redovisningstransaktioner med samma bokföringsdatum överförs som en post till motsvarande kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="373e7-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="373e7-115">Månad</span><span class="sxs-lookup"><span data-stu-id="373e7-115">Month</span></span>|<span data-ttu-id="373e7-116">Alla redovisningstransaktioner i samma kalendermånad överförs som en post till motsvarande kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="373e7-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="373e7-117">Om du har markerat kryssrutan **Automatisk överföring från redovisning** i fönstret **Inställningar för kostnadsredovisning**, [!INCLUDE[d365fin](includes/d365fin_md.md)] uppdaterar kostnadsredovisningen efter varje bokföring i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="373e7-117">If you have selected the **Auto Transfer from G/L** check box in the **Cost Accounting Setup** window, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="373e7-118">Kombinerade transaktioner är inte möjliga.</span><span class="sxs-lookup"><span data-stu-id="373e7-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="373e7-119">Se även</span><span class="sxs-lookup"><span data-stu-id="373e7-119">See Also</span></span>  
 <span data-ttu-id="373e7-120">[Så här: Överföra redovisningstransaktioner till kostnadstransaktioner](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="373e7-120">[How to: Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="373e7-121">[Villkor för överföring av redovisningstransaktioner till kostnadstransaktioner](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="373e7-121">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="373e7-122">[Resultat av överföringen](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="373e7-122">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 [<span data-ttu-id="373e7-123">Överföra och bokföra kostnadstransaktioner</span><span class="sxs-lookup"><span data-stu-id="373e7-123">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  
 <span data-ttu-id="373e7-124">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="373e7-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
