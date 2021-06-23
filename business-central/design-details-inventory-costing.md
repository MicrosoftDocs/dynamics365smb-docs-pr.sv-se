---
title: Designdetaljer – Lager och kostnadskalkylering | Microsoft Docs
description: Dokumentationen ger en detaljerad teknisk inblick i de begrepp och principer som används i lagervärderingsfunktionerna i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8bfcf2b10d9b302c9a65b7cf27c7fb336be68617
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215984"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="e7680-103">Designdetaljer: Lagerkalkylering</span><span class="sxs-lookup"><span data-stu-id="e7680-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="e7680-104">Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna som används i lagringsvärderingsfunktionerna i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="e7680-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="e7680-105">Lagervärdering, kallas även kostnadshantering, används vid registrering och rapportering av rörelsens driftskostnader.</span><span class="sxs-lookup"><span data-stu-id="e7680-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="e7680-106">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="e7680-106">In This Section</span></span>  
[<span data-ttu-id="e7680-107">Designdetaljer: Värderingsprinciper</span><span class="sxs-lookup"><span data-stu-id="e7680-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="e7680-108">Designdetaljer: Artikelkoppling</span><span class="sxs-lookup"><span data-stu-id="e7680-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="e7680-109">Designdetaljer: Kända problem med artikelkopplingar</span><span class="sxs-lookup"><span data-stu-id="e7680-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="e7680-110">Designdetaljer: Kostnadsjustering</span><span class="sxs-lookup"><span data-stu-id="e7680-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="e7680-111">Designinformation: Bokföringsdatumet för justeringsvärdetransaktionen</span><span class="sxs-lookup"><span data-stu-id="e7680-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="e7680-112">Designdetaljer: Bokföring av förväntad kostnad</span><span class="sxs-lookup"><span data-stu-id="e7680-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="e7680-113">Designdetaljer: Genomsnittskostnad</span><span class="sxs-lookup"><span data-stu-id="e7680-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="e7680-114">Designdetaljer: Varians</span><span class="sxs-lookup"><span data-stu-id="e7680-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="e7680-115">Designdetaljer: Avrundning</span><span class="sxs-lookup"><span data-stu-id="e7680-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="e7680-116">Designdetaljer: Kostnadskomponenter</span><span class="sxs-lookup"><span data-stu-id="e7680-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="e7680-117">Designdetaljer: Lagerperioder</span><span class="sxs-lookup"><span data-stu-id="e7680-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="e7680-118">Designdetaljer: Lagerbokföring</span><span class="sxs-lookup"><span data-stu-id="e7680-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="e7680-119">Designdetaljer: Bokföring av produktionsorder</span><span class="sxs-lookup"><span data-stu-id="e7680-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="e7680-120">Designdetaljer: Bokföring av monteringsorder</span><span class="sxs-lookup"><span data-stu-id="e7680-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="e7680-121">Designdetaljer: Avstämning med redovisningen</span><span class="sxs-lookup"><span data-stu-id="e7680-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="e7680-122">Designdetaljer: Konton i redovisningen</span><span class="sxs-lookup"><span data-stu-id="e7680-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="e7680-123">Designdetaljer: Lagervärdering</span><span class="sxs-lookup"><span data-stu-id="e7680-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="e7680-124">Designdetaljer: Omvärdering</span><span class="sxs-lookup"><span data-stu-id="e7680-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]