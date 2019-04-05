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
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 6f58e569bea6a42a9ee695095ce308e7a69e2a8d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807037"
---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="f676c-105">Automatisk överföring och kombinerade transaktioner</span><span class="sxs-lookup"><span data-stu-id="f676c-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="f676c-106">I kostnadsredovisningen kan du överföra redovisningstransaktioner till en kostnadstyp, genom att använda en kombinerad bokföring.</span><span class="sxs-lookup"><span data-stu-id="f676c-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="f676c-107">Du kan ange om en kostnadstyp tar emot kombinerade transaktioner i fältet **Kombinera transaktioner** i kostnadstypsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f676c-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="f676c-108">Alternativen beskrivs i tabellen nedan.</span><span class="sxs-lookup"><span data-stu-id="f676c-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="f676c-109">Kombinera transaktioner</span><span class="sxs-lookup"><span data-stu-id="f676c-109">Combine entries</span></span>|<span data-ttu-id="f676c-110">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="f676c-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="f676c-111">Ingen</span><span class="sxs-lookup"><span data-stu-id="f676c-111">None</span></span>|<span data-ttu-id="f676c-112">Varje redovisningstransaktion överförs individuellt till motsvarande kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="f676c-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="f676c-113">Dag</span><span class="sxs-lookup"><span data-stu-id="f676c-113">Day</span></span>|<span data-ttu-id="f676c-114">Redovisningstransaktioner med samma bokföringsdatum överförs som en post till motsvarande kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="f676c-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="f676c-115">Månad</span><span class="sxs-lookup"><span data-stu-id="f676c-115">Month</span></span>|<span data-ttu-id="f676c-116">Alla redovisningstransaktioner i samma kalendermånad överförs som en post till motsvarande kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="f676c-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="f676c-117">Om du har markerat kryssrutan **Automatisk överföring från redovisning** på sidan **Inställningar för kostnadsredovisning**, [!INCLUDE[d365fin](includes/d365fin_md.md)] uppdaterar kostnadsredovisningen efter varje bokföring i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="f676c-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="f676c-118">Kombinerade transaktioner är inte möjliga.</span><span class="sxs-lookup"><span data-stu-id="f676c-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f676c-119">Se även</span><span class="sxs-lookup"><span data-stu-id="f676c-119">See Also</span></span>  
 <span data-ttu-id="f676c-120">[Överföra och bokföra kostnadstransaktioner](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="f676c-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="f676c-121">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f676c-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
