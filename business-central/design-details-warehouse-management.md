---
title: Designdetaljer – Lagerhantering | Microsoft Docs
description: Det här avsnittet innehåller en översikt över design, begrepp och metoder som ligger bakom distributionshanteringsfunktionerna i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 87b3717a8f45444bc43da445d359ed6d79b40372
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786443"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="5cbc7-103">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="5cbc7-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="5cbc7-104">Denna dokumentation visar en översikt över begrepp och principer som används i lagerstyrningsfunktioner i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="5cbc7-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="5cbc7-105">Den förklarar designen bakom centrala lagerfunktioner och hur lagerstyrning integreras med andra funktioner i försörjningskedjan.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="5cbc7-106">För att skilja mellan de olika komplexitetsnivåerna i lagerstyrningen är dokumentationen uppdelad i två allmänna grupper, grundläggande och avancerad lagerkonfigurationer, som anges med avsnittsrubriker.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="5cbc7-107">Den här enkla differentieringen täcker olika komplexitetsnivåer som definieras av produktpartiklar och lagerplatsinställningar.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="5cbc7-108">Mer information finns i [Designdetaljer: Lagerstyrningsinställningar](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="5cbc7-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="5cbc7-109">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="5cbc7-109">In This Section</span></span>  
[<span data-ttu-id="5cbc7-110">Designdetaljer: Översikt över distributionslager</span><span class="sxs-lookup"><span data-stu-id="5cbc7-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="5cbc7-111">Designdetaljer: Lagerstyrningsinställningar</span><span class="sxs-lookup"><span data-stu-id="5cbc7-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="5cbc7-112">Designdetaljer: inkommande distributionslagerflöde</span><span class="sxs-lookup"><span data-stu-id="5cbc7-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="5cbc7-113">Designdetaljer: Interna distributionslagerflöden</span><span class="sxs-lookup"><span data-stu-id="5cbc7-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="5cbc7-114">Designdetaljer: Disposition i distributionslagret</span><span class="sxs-lookup"><span data-stu-id="5cbc7-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="5cbc7-115">Designdetaljer: utgående distributionslagerflöde</span><span class="sxs-lookup"><span data-stu-id="5cbc7-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="5cbc7-116">Designdetaljer: Integrering med lager</span><span class="sxs-lookup"><span data-stu-id="5cbc7-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]