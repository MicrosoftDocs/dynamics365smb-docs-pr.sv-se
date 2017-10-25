---
title: "Villkor för överföring av redovisningstransaktioner till kostnadstransaktioner | Microsoft Docs"
description: "Det är viktigt att förstå kriterier för överföring av redovisningstransaktioner mot kostnadstransaktioner. Under överföringen använder batchjobbet **Överför redovisningstransaktioner** till kostnadsredovisning följande kriterier för att bestämma om och hur redovisningstransaktionerna överförs."
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
ms.openlocfilehash: 59faad50504bff05e6cdb1c78d00553e85faf47e
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="d179d-104">Villkor för överföring av redovisningstransaktioner till kostnadstransaktioner</span><span class="sxs-lookup"><span data-stu-id="d179d-104">Criteria for Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="d179d-105">Det är viktigt att förstå kriterier för överföring av redovisningstransaktioner mot kostnadstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="d179d-105">It is important to understand the criteria for transferring general ledger entries to cost entries.</span></span> <span data-ttu-id="d179d-106">Under överföringen använder batchjobbet **Överför redovisningstransaktioner till kostnadsredovisning** följande kriterier för att bestämma om och hur redovisningstransaktionerna överförs.</span><span class="sxs-lookup"><span data-stu-id="d179d-106">During the transfer, the **Transfer GL Entries to CA** batch job uses the following criteria to determine if and how the general ledger entries are transferred.</span></span>  

<span data-ttu-id="d179d-107">Redovisningstransaktioner överförs om:</span><span class="sxs-lookup"><span data-stu-id="d179d-107">General ledger entries are transferred if:</span></span>  

-   <span data-ttu-id="d179d-108">Transaktionerna har dimensionsvärden som motsvarar antingen ett kostnadsställe eller en kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="d179d-108">The entries have dimension values corresponding to either a cost center or a cost object.</span></span>  
-   <span data-ttu-id="d179d-109">Transaktionerna har dimensionsvärden som motsvarar ett kostnadsställe och en kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="d179d-109">The entries have dimension values that correspond to a cost center and a cost object.</span></span> <span data-ttu-id="d179d-110">För dessa verifikationer har kostnadsstället prioritet.</span><span class="sxs-lookup"><span data-stu-id="d179d-110">For these entries, the cost center takes precedence.</span></span> <span data-ttu-id="d179d-111">Det gör att det går att undvika en situation där en kostnadstyp visas både i en kostnadsbärare och ett kostnadsställe och därigenom räknas två gånger i statistiken.</span><span class="sxs-lookup"><span data-stu-id="d179d-111">This helps avoid a situation where a cost type appears in both a cost object and a cost center and is therefore counted twice in the statistics.</span></span>  
-   <span data-ttu-id="d179d-112">Verifikationsnumret i transaktionerna är tomt, så att visas med verifikationsnumret 0000 i kostnadstransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="d179d-112">The document number in the entries is empty, so it will appear with a document number of 0000 in the cost entries.</span></span>  
-   <span data-ttu-id="d179d-113">Transaktionerna överförs till en kostnadstyp som används för kombinerade transaktioner, och dessa transaktioner överförs som en kombinerad transaktionen antingen månatligt eller dagligen.</span><span class="sxs-lookup"><span data-stu-id="d179d-113">The entries are transferred to a cost type that allows for combined entries and these entries are transferred as a combined entry either monthly or daily.</span></span>  

<span data-ttu-id="d179d-114">Redovisningstransaktioner överförs inte om:</span><span class="sxs-lookup"><span data-stu-id="d179d-114">General ledger entries are not transferred if:</span></span>  

-   <span data-ttu-id="d179d-115">Transaktionerna har dimensionsvärden som inte motsvarar ett kostnadsställe eller en kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="d179d-115">The entries have dimension values that do not correspond to a cost center or a cost object.</span></span>  
-   <span data-ttu-id="d179d-116">Transaktionerna har ett belopp på noll.</span><span class="sxs-lookup"><span data-stu-id="d179d-116">The entries have an amount of zero.</span></span>  
-   <span data-ttu-id="d179d-117">Transaktionerna har ett redovisningskonto som har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="d179d-117">The entries have a general ledger account that has been deleted.</span></span>  
-   <span data-ttu-id="d179d-118">Transaktionerna har ett redovisningskonto som inte är av typen **Resultaträkning**.</span><span class="sxs-lookup"><span data-stu-id="d179d-118">The entries have a general ledger account that is not of the type **Income Statement**.</span></span>  
-   <span data-ttu-id="d179d-119">Transaktionerna har ett redovisningskonto som inte har kopplats till en kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="d179d-119">The entries have a general ledger account that is not assigned a cost type.</span></span>  
-   <span data-ttu-id="d179d-120">Transaktionerna har ett bokföringsdatum före startdatum för **Startdatum för överföring till redovisning**.</span><span class="sxs-lookup"><span data-stu-id="d179d-120">The entries have a posting date before the **Starting Date for G/L Transfer**.</span></span>  
-   <span data-ttu-id="d179d-121">Transaktionerna har bokförts med ett stängningsdatum.</span><span class="sxs-lookup"><span data-stu-id="d179d-121">The entries have been posted with a closing date.</span></span> <span data-ttu-id="d179d-122">Dessa är vanliga transaktioner som nollställer saldot i resultaträkningen i slutet av året.</span><span class="sxs-lookup"><span data-stu-id="d179d-122">These are typically entries that set back the balance of the income statement at the end of the year.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d179d-123">Se även</span><span class="sxs-lookup"><span data-stu-id="d179d-123">See Also</span></span>  
[<span data-ttu-id="d179d-124">Redovisa kostnader</span><span class="sxs-lookup"><span data-stu-id="d179d-124">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
 <span data-ttu-id="d179d-125">[Så här: Överföra redovisningstransaktioner till kostnadstransaktioner](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="d179d-125">[How to: Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="d179d-126">[Överföra och bokföra kostnadstransaktioner](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="d179d-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="d179d-127">Om kostnadsredovisning</span><span class="sxs-lookup"><span data-stu-id="d179d-127">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
 <span data-ttu-id="d179d-128">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d179d-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
