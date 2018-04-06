---
title: Designdetaljer - Lager och kostnadskalkylering | Microsoft Docs
description: "Dokumentationen ger en detaljerad teknisk inblick i de begrepp och principer som används i funktionerna för lagerkostnader i Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 11/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 2ee8988a89e4bd01683a6945e66e08ab9608af2e
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="0feab-103">Designdetaljer: Lagerkalkylering</span><span class="sxs-lookup"><span data-stu-id="0feab-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="0feab-104">Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna som används i lagringsvärderingsfunktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0feab-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="0feab-105">Lagervärdering, kallas även kostnadshantering, används vid registrering och rapportering av rörelsens driftskostnader.</span><span class="sxs-lookup"><span data-stu-id="0feab-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="0feab-106">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="0feab-106">In This Section</span></span>  
[<span data-ttu-id="0feab-107">Designdetaljer: Värderingsprinciper</span><span class="sxs-lookup"><span data-stu-id="0feab-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="0feab-108">Designdetaljer: Artikelkoppling</span><span class="sxs-lookup"><span data-stu-id="0feab-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="0feab-109">Designdetaljer: Kända problem med artikelkopplingar</span><span class="sxs-lookup"><span data-stu-id="0feab-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="0feab-110">Designdetaljer: Kostnadsjustering</span><span class="sxs-lookup"><span data-stu-id="0feab-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="0feab-111">Designinformation: Bokföringsdatumet för justeringsvärdetransaktionen</span><span class="sxs-lookup"><span data-stu-id="0feab-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="0feab-112">Designdetaljer: Bokföring av förväntad kostnad</span><span class="sxs-lookup"><span data-stu-id="0feab-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="0feab-113">Designdetaljer: Genomsnittskostnad</span><span class="sxs-lookup"><span data-stu-id="0feab-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="0feab-114">Designdetaljer: Varians</span><span class="sxs-lookup"><span data-stu-id="0feab-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="0feab-115">Designdetaljer: Avrundning</span><span class="sxs-lookup"><span data-stu-id="0feab-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="0feab-116">Designdetaljer: Kostnadskomponenter</span><span class="sxs-lookup"><span data-stu-id="0feab-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="0feab-117">Designdetaljer: Lagerperioder</span><span class="sxs-lookup"><span data-stu-id="0feab-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="0feab-118">Designdetaljer: Lagerbokföring</span><span class="sxs-lookup"><span data-stu-id="0feab-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="0feab-119">Designdetaljer: Bokföring av produktionsorder</span><span class="sxs-lookup"><span data-stu-id="0feab-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="0feab-120">Designdetaljer: Bokföring av monteringsorder</span><span class="sxs-lookup"><span data-stu-id="0feab-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="0feab-121">Designdetaljer: Avstämning med redovisningen</span><span class="sxs-lookup"><span data-stu-id="0feab-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="0feab-122">Designdetaljer: Konton i redovisningen</span><span class="sxs-lookup"><span data-stu-id="0feab-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="0feab-123">Designdetaljer: Omvärdering</span><span class="sxs-lookup"><span data-stu-id="0feab-123">Design Details: Revaluation</span></span>](design-details-revaluation.md)

