---
title: Definiera relationen mellan kostnadstyper och redovisningskonton | Microsoft Docs
description: "Lär dig hur du skapar relationen mellan kostnadstypen och redovisningskontot."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f30b8b56ae4afcff230a7934a6bcac4d205db
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a><span data-ttu-id="8d0d3-103">Definiera relationen mellan kostnadstyper och redovisningskonton</span><span class="sxs-lookup"><span data-stu-id="8d0d3-103">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>
<span data-ttu-id="8d0d3-104">Relationen mellan kostnadstypen och redovisningskontot skapas i kostnadstypen och i redovisningskontot.</span><span class="sxs-lookup"><span data-stu-id="8d0d3-104">The relationship between the cost type and the general ledger account is created in the cost type and in the general ledger account.</span></span>  

* <span data-ttu-id="8d0d3-105">Fältet **Redovisningskontointervall** i tabellen **Kostnadstyp** bestämmer vilka redovisningskonton som tillhör en kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="8d0d3-105">The **G/L Account Range** field in the **Cost Type** table establishes which general ledger accounts belong to a cost type.</span></span>  
* <span data-ttu-id="8d0d3-106">Fältet **Kostnadstypsnr.**</span><span class="sxs-lookup"><span data-stu-id="8d0d3-106">The **Cost Type No.**</span></span> <span data-ttu-id="8d0d3-107">i kontoplanen bestämmer vilken kostnadstyp ett redovisningskonto tillhör.</span><span class="sxs-lookup"><span data-stu-id="8d0d3-107">field in the chart of accounts establishes which cost type a general ledger account belongs to.</span></span>  

<span data-ttu-id="8d0d3-108">Dessa två fält fylls i automatiskt när du använder funktionen **Hämta kostnadstyper från kontoplan**.</span><span class="sxs-lookup"><span data-stu-id="8d0d3-108">These two fields are filled automatically when you use the **Get Cost Types from Chart of Accounts** function.</span></span>  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a><span data-ttu-id="8d0d3-109">Relationen mellan redovisningskonton och kostnadstyper</span><span class="sxs-lookup"><span data-stu-id="8d0d3-109">Relationship Between General Ledger Accounts and Cost Types</span></span>  
<span data-ttu-id="8d0d3-110">Det finns en många till en-relation mellan kostnadstyper och redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="8d0d3-110">There is an n:1 relationship between general ledger accounts and cost types.</span></span> <span data-ttu-id="8d0d3-111">Flera redovisningskonton kan tillhöra en kostnadstyp, men varje redovisningskonto tillhör endast en kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="8d0d3-111">Several general ledger accounts can belong to one cost type, but each general ledger account belongs to only one cost type.</span></span> <span data-ttu-id="8d0d3-112">Tabellen nedan beskriver informationen i sambandet.</span><span class="sxs-lookup"><span data-stu-id="8d0d3-112">The following table describes the details in the relationship.</span></span>  

|<span data-ttu-id="8d0d3-113">Samband</span><span class="sxs-lookup"><span data-stu-id="8d0d3-113">Relationship</span></span>|<span data-ttu-id="8d0d3-114">**Redovisningskontointervall**</span><span class="sxs-lookup"><span data-stu-id="8d0d3-114">**G/L Account Range**</span></span>|<span data-ttu-id="8d0d3-115">**Kostnadstypsnr**</span><span class="sxs-lookup"><span data-stu-id="8d0d3-115">**Cost Type No.**</span></span>|  
|------------------|------------------------------------------------|-------------------------------------------|  
|<span data-ttu-id="8d0d3-116">Ett redovisningskonto för varje kostnadstyp</span><span class="sxs-lookup"><span data-stu-id="8d0d3-116">One general ledger account for each cost type</span></span>|<span data-ttu-id="8d0d3-117">Ett redovisningskonton</span><span class="sxs-lookup"><span data-stu-id="8d0d3-117">One general ledger account</span></span>|<span data-ttu-id="8d0d3-118">En kostnadstyp</span><span class="sxs-lookup"><span data-stu-id="8d0d3-118">One cost type</span></span>|  
|<span data-ttu-id="8d0d3-119">Flera redovisningskonton för en kostnadstyp</span><span class="sxs-lookup"><span data-stu-id="8d0d3-119">Several general ledger accounts for one cost type</span></span>|<span data-ttu-id="8d0d3-120">Redovisningskontointervall, exempelvis 7110..7193 för varje redovisningskonto</span><span class="sxs-lookup"><span data-stu-id="8d0d3-120">General ledger account range, for example, 7110..7193 for each general ledger account</span></span>|<span data-ttu-id="8d0d3-121">För varje redovisningskonto i intervallet finns det bara en kostnadstyp</span><span class="sxs-lookup"><span data-stu-id="8d0d3-121">For each general ledger account in the range, there is only one cost type</span></span>|  
|<span data-ttu-id="8d0d3-122">Kostnadstyper utan motsvarande redovisningskonton</span><span class="sxs-lookup"><span data-stu-id="8d0d3-122">Cost types without corresponding general ledger accounts</span></span>|<Empty>||  
|<span data-ttu-id="8d0d3-123">Redovisningskonton vars transaktioner inte kommer att överföras</span><span class="sxs-lookup"><span data-stu-id="8d0d3-123">General ledger accounts whose entries will not be transferred</span></span>||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a><span data-ttu-id="8d0d3-124">Kostnadstyper utan en relation till redovisningen</span><span class="sxs-lookup"><span data-stu-id="8d0d3-124">Cost Types Without a Relationship to the General Ledger</span></span>  
<span data-ttu-id="8d0d3-125">En kostnadstyp kan inte ha en koppling till redovisningskonton, om ett av följande villkor gäller:</span><span class="sxs-lookup"><span data-stu-id="8d0d3-125">A cost type may not have a relationship to general ledger accounts if one of the following conditions is true:</span></span>  

* <span data-ttu-id="8d0d3-126">Konton för rörelseredovisning, till exempel Beräkna ränta och avskrivning, tar endast kostnader från rörelseredovisningen.</span><span class="sxs-lookup"><span data-stu-id="8d0d3-126">Accounts for operational accounting, such as Calc. Interest and Depreciation, only take costs from the operational accounting.</span></span>  
* <span data-ttu-id="8d0d3-127">Hjälpkostnadstyper, till exempel kostnadstyper 9901, 9902 och 9903 i databasen [!INCLUDE[d365fin](includes/d365fin_md.md)] används som kredit- och debetkonton för fördelningar.</span><span class="sxs-lookup"><span data-stu-id="8d0d3-127">Helping cost types, such as cost types 9901, 9902, and 9903 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, are used as credit and debit accounts for allocations.</span></span>  
* <span data-ttu-id="8d0d3-128">Hjälpkontot 9920 i databasen [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller faktiska periodiseringar som visar skillnaden mellan kostnader och utgifterna från redovisningen.</span><span class="sxs-lookup"><span data-stu-id="8d0d3-128">The helping account, 9920 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, contains actual accruals that show the difference between costs and the expense from the general ledger.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8d0d3-129">Se även</span><span class="sxs-lookup"><span data-stu-id="8d0d3-129">See Also</span></span>  
[<span data-ttu-id="8d0d3-130">Redovisa kostnader</span><span class="sxs-lookup"><span data-stu-id="8d0d3-130">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="8d0d3-131">[Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="8d0d3-131">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
[<span data-ttu-id="8d0d3-132">Om kostnadsredovisning</span><span class="sxs-lookup"><span data-stu-id="8d0d3-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="8d0d3-133">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8d0d3-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

