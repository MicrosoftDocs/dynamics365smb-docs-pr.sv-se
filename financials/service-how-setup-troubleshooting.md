---
title: "Ställa in Felsökningsprocesser | Microsoft Docs"
description: "Lär dig hur du ställer in processer som hjälper servicerepresentanten att identifiera och lösa problem med serviceartiklar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5876bf5d959d106eefb9b0f765e42e74dd13ab07
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---

# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="1f8fb-103">Ställa in felsökning av serviceartiklar.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="1f8fb-104">Du kan ställa in felsökningsriktlinjer som hjälper tekniker att lösa problem när de tillhandahåller tjänster.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="1f8fb-105">Riktlinjer kan till exempel vara en lista över de steg som måste utföras vid en reparation eller ett antal frågor att ställa om artiklarna.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="1f8fb-106">När du har angett riktlinjer för felsökning kan du tilldela dem till serviceartikelgrupper, serviceartiklar eller artiklar.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="1f8fb-107">Det finns en arvshierarki för riktlinjer.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="1f8fb-108">Om du tilldelar dem till en serviceartikelgrupp ärver artiklarna som ingår i gruppen riktlinjerna om du inte anger något annat för artiklarna.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="1f8fb-109">På ett liknande sätt ärver serviceartiklar riktlinjer från artiklar.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="1f8fb-110">Så här skapar du felsökningsriktlinjer</span><span class="sxs-lookup"><span data-stu-id="1f8fb-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="1f8fb-111">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Felsökning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1f8fb-112">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="1f8fb-113">För att koppla riktlinjer för felsökning till artiklar, serviceartiklar eller serviceartikelgrupper.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="1f8fb-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artiklar**, **Serviceartiklar**, eller **Serviceartikelgrupp** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1f8fb-115">Välj relevant enhet och välj sedan åtgärden **Felsökning**.</span><span class="sxs-lookup"><span data-stu-id="1f8fb-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1f8fb-116">Se även</span><span class="sxs-lookup"><span data-stu-id="1f8fb-116">See Also</span></span>
[<span data-ttu-id="1f8fb-117">Servicehantering</span><span class="sxs-lookup"><span data-stu-id="1f8fb-117">Service Management</span></span>](service-service.md)