---
title: Designdetaljer - Lagerhantering | Microsoft Docs
description: "Detta avsnitt innehåller en översikt över design, begrepp och metoder bakom lagerhanteringsfunktionerna i Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3145c64e64274cefb19630b639879f09ead8a6f3
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="425b0-103">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="425b0-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="425b0-104">Denna dokumentation visar en översikt över begrepp och principer som används i lagerstyrningsfunktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="425b0-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="425b0-105">Den förklarar designen bakom centrala lagerfunktioner och hur lagerstyrning integreras med andra funktioner i försörjningskedjan.</span><span class="sxs-lookup"><span data-stu-id="425b0-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="425b0-106">För att skilja mellan de olika komplexitetsnivåerna i lagerstyrningen är dokumentationen uppdelad i två allmänna grupper, grundläggande och avancerad lagerkonfigurationer, som anges med avsnittsrubriker.</span><span class="sxs-lookup"><span data-stu-id="425b0-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="425b0-107">Den här enkla differentieringen täcker olika komplexitetsnivåer som definieras av produktpartiklar och lagerplatsinställningar.</span><span class="sxs-lookup"><span data-stu-id="425b0-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="425b0-108">Mer information finns i [Designdetaljer: Lagerstyrningsinställningar](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="425b0-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="425b0-109">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="425b0-109">In This Section</span></span>  
[<span data-ttu-id="425b0-110">Designdetaljer: Översikt över distributionslager</span><span class="sxs-lookup"><span data-stu-id="425b0-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="425b0-111">Designdetaljer: Lagerstyrningsinställningar</span><span class="sxs-lookup"><span data-stu-id="425b0-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="425b0-112">Designdetaljer: Ankommande distributionslagerflöde</span><span class="sxs-lookup"><span data-stu-id="425b0-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="425b0-113">Designdetaljer: Interna distributionslagerflöden</span><span class="sxs-lookup"><span data-stu-id="425b0-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="425b0-114">Designdetaljer: Disposition i distributionslagret</span><span class="sxs-lookup"><span data-stu-id="425b0-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="425b0-115">Designdetaljer: Avgående distributionslagerflöde</span><span class="sxs-lookup"><span data-stu-id="425b0-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="425b0-116">Designdetaljer: Integrering med lager</span><span class="sxs-lookup"><span data-stu-id="425b0-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)

