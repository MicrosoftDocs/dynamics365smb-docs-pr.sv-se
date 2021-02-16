---
title: Designdetaljer – Lager och kostnadskalkylering | Microsoft Docs
description: Dokumentationen ger en detaljerad teknisk inblick i de begrepp och principer som används i lagervärderingsfunktionerna i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 97aa9dc23397403b74fc8f1c65d302733ab3301c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751486"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="75d7d-103">Designdetaljer: Lagerkalkylering</span><span class="sxs-lookup"><span data-stu-id="75d7d-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="75d7d-104">Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna som används i lagringsvärderingsfunktionerna i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="75d7d-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="75d7d-105">Lagervärdering, kallas även kostnadshantering, används vid registrering och rapportering av rörelsens driftskostnader.</span><span class="sxs-lookup"><span data-stu-id="75d7d-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="75d7d-106">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="75d7d-106">In This Section</span></span>  
[<span data-ttu-id="75d7d-107">Designdetaljer: Värderingsprinciper</span><span class="sxs-lookup"><span data-stu-id="75d7d-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="75d7d-108">Designdetaljer: Artikelkoppling</span><span class="sxs-lookup"><span data-stu-id="75d7d-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="75d7d-109">Designdetaljer: Kända problem med artikelkopplingar</span><span class="sxs-lookup"><span data-stu-id="75d7d-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="75d7d-110">Designdetaljer: Kostnadsjustering</span><span class="sxs-lookup"><span data-stu-id="75d7d-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="75d7d-111">Designinformation: Bokföringsdatumet för justeringsvärdetransaktionen</span><span class="sxs-lookup"><span data-stu-id="75d7d-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="75d7d-112">Designdetaljer: Bokföring av förväntad kostnad</span><span class="sxs-lookup"><span data-stu-id="75d7d-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="75d7d-113">Designdetaljer: Genomsnittskostnad</span><span class="sxs-lookup"><span data-stu-id="75d7d-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="75d7d-114">Designdetaljer: Varians</span><span class="sxs-lookup"><span data-stu-id="75d7d-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="75d7d-115">Designdetaljer: Avrundning</span><span class="sxs-lookup"><span data-stu-id="75d7d-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="75d7d-116">Designdetaljer: Kostnadskomponenter</span><span class="sxs-lookup"><span data-stu-id="75d7d-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="75d7d-117">Designdetaljer: Lagerperioder</span><span class="sxs-lookup"><span data-stu-id="75d7d-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="75d7d-118">Designdetaljer: Lagerbokföring</span><span class="sxs-lookup"><span data-stu-id="75d7d-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="75d7d-119">Designdetaljer: Bokföring av produktionsorder</span><span class="sxs-lookup"><span data-stu-id="75d7d-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="75d7d-120">Designdetaljer: Bokföring av monteringsorder</span><span class="sxs-lookup"><span data-stu-id="75d7d-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="75d7d-121">Designdetaljer: Avstämning med redovisningen</span><span class="sxs-lookup"><span data-stu-id="75d7d-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="75d7d-122">Designdetaljer: Konton i redovisningen</span><span class="sxs-lookup"><span data-stu-id="75d7d-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="75d7d-123">Designdetaljer: Lagervärdering</span><span class="sxs-lookup"><span data-stu-id="75d7d-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="75d7d-124">Designdetaljer: Omvärdering</span><span class="sxs-lookup"><span data-stu-id="75d7d-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)
