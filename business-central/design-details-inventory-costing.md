---
title: Designdetaljer - Lager och kostnadskalkylering | Microsoft Docs
description: Dokumentationen ger en detaljerad teknisk inblick i de begrepp och principer som används i lagervärderingsfunktionerna i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 65f298199d4451a64f75ddb6ad34fefc30af3d7a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787777"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="d16d7-103">Designdetaljer: Lagerkalkylering</span><span class="sxs-lookup"><span data-stu-id="d16d7-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="d16d7-104">Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna som används i lagringsvärderingsfunktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d16d7-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="d16d7-105">Lagervärdering, kallas även kostnadshantering, används vid registrering och rapportering av rörelsens driftskostnader.</span><span class="sxs-lookup"><span data-stu-id="d16d7-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="d16d7-106">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="d16d7-106">In This Section</span></span>  
[<span data-ttu-id="d16d7-107">Designdetaljer: Värderingsprinciper</span><span class="sxs-lookup"><span data-stu-id="d16d7-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="d16d7-108">Designdetaljer: Artikelkoppling</span><span class="sxs-lookup"><span data-stu-id="d16d7-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="d16d7-109">Designdetaljer: Kända problem med artikelkopplingar</span><span class="sxs-lookup"><span data-stu-id="d16d7-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="d16d7-110">Designdetaljer: Kostnadsjustering</span><span class="sxs-lookup"><span data-stu-id="d16d7-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="d16d7-111">Designinformation: Bokföringsdatumet för justeringsvärdetransaktionen</span><span class="sxs-lookup"><span data-stu-id="d16d7-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="d16d7-112">Designdetaljer: Bokföring av förväntad kostnad</span><span class="sxs-lookup"><span data-stu-id="d16d7-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="d16d7-113">Designdetaljer: Genomsnittskostnad</span><span class="sxs-lookup"><span data-stu-id="d16d7-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="d16d7-114">Designdetaljer: Varians</span><span class="sxs-lookup"><span data-stu-id="d16d7-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="d16d7-115">Designdetaljer: Avrundning</span><span class="sxs-lookup"><span data-stu-id="d16d7-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="d16d7-116">Designdetaljer: Kostnadskomponenter</span><span class="sxs-lookup"><span data-stu-id="d16d7-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="d16d7-117">Designdetaljer: Lagerperioder</span><span class="sxs-lookup"><span data-stu-id="d16d7-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="d16d7-118">Designdetaljer: Lagerbokföring</span><span class="sxs-lookup"><span data-stu-id="d16d7-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="d16d7-119">Designdetaljer: Bokföring av produktionsorder</span><span class="sxs-lookup"><span data-stu-id="d16d7-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="d16d7-120">Designdetaljer: Bokföring av monteringsorder</span><span class="sxs-lookup"><span data-stu-id="d16d7-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="d16d7-121">Designdetaljer: Avstämning med redovisningen</span><span class="sxs-lookup"><span data-stu-id="d16d7-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="d16d7-122">Designdetaljer: Konton i redovisningen</span><span class="sxs-lookup"><span data-stu-id="d16d7-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="d16d7-123">Designdetaljer: Lagervärdering</span><span class="sxs-lookup"><span data-stu-id="d16d7-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="d16d7-124">Designdetaljer: Omvärdering</span><span class="sxs-lookup"><span data-stu-id="d16d7-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)
