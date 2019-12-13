---
title: Ställa in Felsökningsprocesser | Microsoft Docs
description: Lär dig hur du ställer in processer som hjälper servicerepresentanten att identifiera och lösa problem med serviceartiklar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6a0a4b49b957d082ad66178aabd1ccc532011885
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877317"
---
# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="51ec7-103">Ställa in felsökning av serviceartiklar.</span><span class="sxs-lookup"><span data-stu-id="51ec7-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="51ec7-104">Du kan ställa in felsökningsriktlinjer som hjälper tekniker att lösa problem när de tillhandahåller tjänster.</span><span class="sxs-lookup"><span data-stu-id="51ec7-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="51ec7-105">Riktlinjer kan till exempel vara en lista över de steg som måste utföras vid en reparation eller ett antal frågor att ställa om artiklarna.</span><span class="sxs-lookup"><span data-stu-id="51ec7-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="51ec7-106">När du har angett riktlinjer för felsökning kan du tilldela dem till serviceartikelgrupper, serviceartiklar eller artiklar.</span><span class="sxs-lookup"><span data-stu-id="51ec7-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="51ec7-107">Det finns en arvshierarki för riktlinjer.</span><span class="sxs-lookup"><span data-stu-id="51ec7-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="51ec7-108">Om du tilldelar dem till en serviceartikelgrupp ärver artiklarna som ingår i gruppen riktlinjerna om du inte anger något annat för artiklarna.</span><span class="sxs-lookup"><span data-stu-id="51ec7-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="51ec7-109">På ett liknande sätt ärver serviceartiklar riktlinjer från artiklar.</span><span class="sxs-lookup"><span data-stu-id="51ec7-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="51ec7-110">Så här skapar du felsökningsriktlinjer</span><span class="sxs-lookup"><span data-stu-id="51ec7-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="51ec7-111">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Felsökning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="51ec7-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="51ec7-112">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="51ec7-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="51ec7-113">För att koppla riktlinjer för felsökning till artiklar, serviceartiklar eller serviceartikelgrupper.</span><span class="sxs-lookup"><span data-stu-id="51ec7-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="51ec7-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") gå till **Artiklar** eller **Tjänsteartiklar** eller **Tjänstartikelgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="51ec7-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="51ec7-115">Välj relevant enhet och välj sedan åtgärden **Felsökning**.</span><span class="sxs-lookup"><span data-stu-id="51ec7-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="51ec7-116">Se även</span><span class="sxs-lookup"><span data-stu-id="51ec7-116">See Also</span></span>
[<span data-ttu-id="51ec7-117">Servicehantering</span><span class="sxs-lookup"><span data-stu-id="51ec7-117">Service Management</span></span>](service-service.md)