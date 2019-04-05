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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 830c14eb96557f8852d0a4758922503fe0179b58
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807515"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="2ad20-103">Designdetaljer: Lagerkalkylering</span><span class="sxs-lookup"><span data-stu-id="2ad20-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="2ad20-104">Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna som används i lagringsvärderingsfunktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2ad20-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="2ad20-105">Lagervärdering, kallas även kostnadshantering, används vid registrering och rapportering av rörelsens driftskostnader.</span><span class="sxs-lookup"><span data-stu-id="2ad20-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="2ad20-106">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="2ad20-106">In This Section</span></span>  
[<span data-ttu-id="2ad20-107">Designdetaljer: Värderingsprinciper</span><span class="sxs-lookup"><span data-stu-id="2ad20-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="2ad20-108">Designdetaljer: Artikelkoppling</span><span class="sxs-lookup"><span data-stu-id="2ad20-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="2ad20-109">Designdetaljer: Kända problem med artikelkopplingar</span><span class="sxs-lookup"><span data-stu-id="2ad20-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="2ad20-110">Designdetaljer: Kostnadsjustering</span><span class="sxs-lookup"><span data-stu-id="2ad20-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="2ad20-111">Designinformation: Bokföringsdatumet för justeringsvärdetransaktionen</span><span class="sxs-lookup"><span data-stu-id="2ad20-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="2ad20-112">Designdetaljer: Bokföring av förväntad kostnad</span><span class="sxs-lookup"><span data-stu-id="2ad20-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="2ad20-113">Designdetaljer: Genomsnittskostnad</span><span class="sxs-lookup"><span data-stu-id="2ad20-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="2ad20-114">Designdetaljer: Varians</span><span class="sxs-lookup"><span data-stu-id="2ad20-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="2ad20-115">Designdetaljer: Avrundning</span><span class="sxs-lookup"><span data-stu-id="2ad20-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="2ad20-116">Designdetaljer: Kostnadskomponenter</span><span class="sxs-lookup"><span data-stu-id="2ad20-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="2ad20-117">Designdetaljer: Lagerperioder</span><span class="sxs-lookup"><span data-stu-id="2ad20-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="2ad20-118">Designdetaljer: Lagerbokföring</span><span class="sxs-lookup"><span data-stu-id="2ad20-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="2ad20-119">Designdetaljer: Bokföring av produktionsorder</span><span class="sxs-lookup"><span data-stu-id="2ad20-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="2ad20-120">Designdetaljer: Bokföring av monteringsorder</span><span class="sxs-lookup"><span data-stu-id="2ad20-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="2ad20-121">Designdetaljer: Avstämning med redovisningen</span><span class="sxs-lookup"><span data-stu-id="2ad20-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
<span data-ttu-id="2ad20-122">[Designdetaljer: Konton i redovisningen](design-details-accounts-in-the-general-ledger.md)
[Designdetaljer: Lagervärdering](design-details-inventory-valuation.md)</span><span class="sxs-lookup"><span data-stu-id="2ad20-122">[Design Details: Accounts in the General Ledger](design-details-accounts-in-the-general-ledger.md)
[Design Details: Inventory Valuation](design-details-inventory-valuation.md)</span></span>  
[<span data-ttu-id="2ad20-123">Designdetaljer: Omvärdering</span><span class="sxs-lookup"><span data-stu-id="2ad20-123">Design Details: Revaluation</span></span>](design-details-revaluation.md)
