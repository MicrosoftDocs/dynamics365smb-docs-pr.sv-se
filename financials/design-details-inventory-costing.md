---
title: Designdetaljer - Lager och kostnadskalkylering | Microsoft Docs
description: "Dokumentationen ger en detaljerad teknisk inblick i de koncept och principer som används i lagringsvärderingsfunktionerna i Dynamics 365."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: ef098c17ab54d45eec380548f70042a436c95128
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="07ac6-103">Designdetaljer: Lagerkalkylering</span><span class="sxs-lookup"><span data-stu-id="07ac6-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="07ac6-104">Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna som används i lagringsvärderingsfunktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="07ac6-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="07ac6-105">Lagervärdering, kallas även kostnadshantering, används vid registrering och rapportering av rörelsens driftskostnader.</span><span class="sxs-lookup"><span data-stu-id="07ac6-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="07ac6-106">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="07ac6-106">In This Section</span></span>  
[<span data-ttu-id="07ac6-107">Designdetaljer: Värderingsprinciper</span><span class="sxs-lookup"><span data-stu-id="07ac6-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="07ac6-108">Designdetaljer: Objektkoppling</span><span class="sxs-lookup"><span data-stu-id="07ac6-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="07ac6-109">Designdetaljer: Kostnadsjustering</span><span class="sxs-lookup"><span data-stu-id="07ac6-109">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="07ac6-110">Designdetaljer: Bokföring av förväntad kostnad</span><span class="sxs-lookup"><span data-stu-id="07ac6-110">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="07ac6-111">Designdetaljer: Genomsnittskostnad</span><span class="sxs-lookup"><span data-stu-id="07ac6-111">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="07ac6-112">Designdetaljer: Varians</span><span class="sxs-lookup"><span data-stu-id="07ac6-112">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="07ac6-113">Designdetaljer: Avrundning</span><span class="sxs-lookup"><span data-stu-id="07ac6-113">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="07ac6-114">Designdetaljer: Kostnadskomponenter</span><span class="sxs-lookup"><span data-stu-id="07ac6-114">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="07ac6-115">Designdetaljer: Lagerperioder</span><span class="sxs-lookup"><span data-stu-id="07ac6-115">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="07ac6-116">Designdetaljer: Lagerbokföring</span><span class="sxs-lookup"><span data-stu-id="07ac6-116">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="07ac6-117">Designdetaljer: Bokföring av produktionsorder</span><span class="sxs-lookup"><span data-stu-id="07ac6-117">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="07ac6-118">Designdetaljer: Bokföring av monteringsorder</span><span class="sxs-lookup"><span data-stu-id="07ac6-118">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="07ac6-119">Designdetaljer: Avstämning med redovisningen</span><span class="sxs-lookup"><span data-stu-id="07ac6-119">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="07ac6-120">Designdetaljer: Konton i redovisningen</span><span class="sxs-lookup"><span data-stu-id="07ac6-120">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="07ac6-121">Designdetaljer: Omvärdering</span><span class="sxs-lookup"><span data-stu-id="07ac6-121">Design Details: Revaluation</span></span>](design-details-revaluation.md)

