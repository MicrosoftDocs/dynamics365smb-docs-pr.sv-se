---
title: Automatisk överföring och kombinerade transaktioner | Microsoft Docs
description: I kostnadsredovisningen kan du överföra redovisningstransaktioner till en kostnadstyp, genom att använda en kombinerad bokföring. Du kan ange om en kostnadstyp tar emot kombinerade transaktioner i fältet **Kombinera transaktioner** i kostnadstypsdefinitionen. Alternativen beskrivs i tabellen nedan.
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
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 8f6b5328b3a7b8cdcb4582deda363bdd0361ed9a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "941160"
---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="4e69e-105">Automatisk överföring och kombinerade transaktioner</span><span class="sxs-lookup"><span data-stu-id="4e69e-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="4e69e-106">I kostnadsredovisningen kan du överföra redovisningstransaktioner till en kostnadstyp, genom att använda en kombinerad bokföring.</span><span class="sxs-lookup"><span data-stu-id="4e69e-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="4e69e-107">Du kan ange om en kostnadstyp tar emot kombinerade transaktioner i fältet **Kombinera transaktioner** i kostnadstypsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4e69e-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="4e69e-108">Alternativen beskrivs i tabellen nedan.</span><span class="sxs-lookup"><span data-stu-id="4e69e-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="4e69e-109">Kombinera transaktioner</span><span class="sxs-lookup"><span data-stu-id="4e69e-109">Combine entries</span></span>|<span data-ttu-id="4e69e-110">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4e69e-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="4e69e-111">Ingen</span><span class="sxs-lookup"><span data-stu-id="4e69e-111">None</span></span>|<span data-ttu-id="4e69e-112">Varje redovisningstransaktion överförs individuellt till motsvarande kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="4e69e-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="4e69e-113">Dag</span><span class="sxs-lookup"><span data-stu-id="4e69e-113">Day</span></span>|<span data-ttu-id="4e69e-114">Redovisningstransaktioner med samma bokföringsdatum överförs som en post till motsvarande kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="4e69e-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="4e69e-115">Månad</span><span class="sxs-lookup"><span data-stu-id="4e69e-115">Month</span></span>|<span data-ttu-id="4e69e-116">Alla redovisningstransaktioner i samma kalendermånad överförs som en post till motsvarande kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="4e69e-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="4e69e-117">Om du har markerat kryssrutan **Automatisk överföring från redovisning** på sidan **Inställningar för kostnadsredovisning**, [!INCLUDE[d365fin](includes/d365fin_md.md)] uppdaterar kostnadsredovisningen efter varje bokföring i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="4e69e-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="4e69e-118">Kombinerade transaktioner är inte möjliga.</span><span class="sxs-lookup"><span data-stu-id="4e69e-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4e69e-119">Se även</span><span class="sxs-lookup"><span data-stu-id="4e69e-119">See Also</span></span>  
 <span data-ttu-id="4e69e-120">[Överföra och bokföra kostnadstransaktioner](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="4e69e-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="4e69e-121">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4e69e-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
