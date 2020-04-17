---
title: Designdetaljer - Lagerhantering | Microsoft Docs
description: Det här avsnittet innehåller en översikt över design, begrepp och metoder som ligger bakom distributionshanteringsfunktionerna i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 91e2f135f97e8d1e80edce3c6e45e08a080e826f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184730"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="979fd-103">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="979fd-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="979fd-104">Denna dokumentation visar en översikt över begrepp och principer som används i lagerstyrningsfunktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="979fd-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="979fd-105">Den förklarar designen bakom centrala lagerfunktioner och hur lagerstyrning integreras med andra funktioner i försörjningskedjan.</span><span class="sxs-lookup"><span data-stu-id="979fd-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="979fd-106">För att skilja mellan de olika komplexitetsnivåerna i lagerstyrningen är dokumentationen uppdelad i två allmänna grupper, grundläggande och avancerad lagerkonfigurationer, som anges med avsnittsrubriker.</span><span class="sxs-lookup"><span data-stu-id="979fd-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="979fd-107">Den här enkla differentieringen täcker olika komplexitetsnivåer som definieras av produktpartiklar och lagerplatsinställningar.</span><span class="sxs-lookup"><span data-stu-id="979fd-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="979fd-108">Mer information finns i [Designdetaljer: Lagerstyrningsinställningar](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="979fd-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="979fd-109">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="979fd-109">In This Section</span></span>  
[<span data-ttu-id="979fd-110">Designdetaljer: Översikt över distributionslager</span><span class="sxs-lookup"><span data-stu-id="979fd-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="979fd-111">Designdetaljer: Lagerstyrningsinställningar</span><span class="sxs-lookup"><span data-stu-id="979fd-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="979fd-112">Designdetaljer: Ankommande distributionslagerflöde</span><span class="sxs-lookup"><span data-stu-id="979fd-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="979fd-113">Designdetaljer: Interna distributionslagerflöden</span><span class="sxs-lookup"><span data-stu-id="979fd-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="979fd-114">Designdetaljer: Disposition i distributionslagret</span><span class="sxs-lookup"><span data-stu-id="979fd-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="979fd-115">Designdetaljer: Avgående distributionslagerflöde</span><span class="sxs-lookup"><span data-stu-id="979fd-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="979fd-116">Designdetaljer: Integrering med lager</span><span class="sxs-lookup"><span data-stu-id="979fd-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)
