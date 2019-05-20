---
title: Visa status för en synkronisering | Microsoft Docs
description: Så här visar du status för ett enskilt synkroniseringsjobb.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245691"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="48632-103">Visa status för en synkronisering</span><span class="sxs-lookup"><span data-stu-id="48632-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="48632-104">Du kan visa statusen för de individuella synkroniseringsjobben som har körts för [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen.</span><span class="sxs-lookup"><span data-stu-id="48632-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="48632-105">Det innehåller synkroniseringjobb som har körts från jobbkön- och manuella synkroniseringsjobb som utfördes på poster från [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="48632-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="48632-106">Det är användbart när du felsöker synkroniseringsproblem eftersom det låter dig komma åt detaljer om specifika fel.</span><span class="sxs-lookup"><span data-stu-id="48632-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-all-synchronization-issues"></a><span data-ttu-id="48632-107">Så här visar du alla synkroniseringsproblem</span><span class="sxs-lookup"><span data-stu-id="48632-107">To view all synchronization issues</span></span>
1. <span data-ttu-id="48632-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kopplade datasynkroniseringsfel** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="48632-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="48632-109">På sidan **Kopplade datasynkroniseringsfel** kan du visa alla problem som inträffade i synkroniseringen mellan [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)], filtrera och sortera poster på sidan per tabell, felmeddelande och utföra åtgärder som **Försök igen** eller **Ta bort koppling** för att lösa ett problem i taget eller samtidigt.</span><span class="sxs-lookup"><span data-stu-id="48632-109">On the **Coupled Data Synchronization Errors** page you can view of all issues that occurred in synchronization of data between [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)], filter and sort records in the page by table, error message and take actions such as **Retry** or **Remove Coupling** to resolve issues one by one or in bulk.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="48632-110">Så här visar du synkroniseringsloggen för specifika (manuellt synkroniserade) poster</span><span class="sxs-lookup"><span data-stu-id="48632-110">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="48632-111">Öppna till exempel kund, artikel eller någon annan post som synkroniserar data mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och försäljning</span><span class="sxs-lookup"><span data-stu-id="48632-111">Open, for example, customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales</span></span>
2. <span data-ttu-id="48632-112">Välj åtgärder **synkroniseringsloggen** för att visa synkroniseringsloggen för den valda posten, till exempel specifik kund som synkroniserade manuellt</span><span class="sxs-lookup"><span data-stu-id="48632-112">Choose **Synchronization Log** action to view the synchronization log for selected record, for example, specific customer you synchronized manually</span></span>

## <a name="see-also"></a><span data-ttu-id="48632-113">Se även</span><span class="sxs-lookup"><span data-stu-id="48632-113">See Also</span></span>  
[<span data-ttu-id="48632-114">Ställa in Dynamics 365 for Sales integrering i Business Central</span><span class="sxs-lookup"><span data-stu-id="48632-114">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="48632-115">Med hjälp av Dynamics 365 for Sales från Business Central</span><span class="sxs-lookup"><span data-stu-id="48632-115">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
