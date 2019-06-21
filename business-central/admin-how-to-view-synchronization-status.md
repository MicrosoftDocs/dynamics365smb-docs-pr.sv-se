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
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620890"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="14a80-103">Visa status för en synkronisering</span><span class="sxs-lookup"><span data-stu-id="14a80-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="14a80-104">Du kan visa statusen för de individuella synkroniseringsjobben som har körts för [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen.</span><span class="sxs-lookup"><span data-stu-id="14a80-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="14a80-105">Det innehåller synkroniseringjobb som har körts från jobbkön- och manuella synkroniseringsjobb som utfördes på poster från [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="14a80-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="14a80-106">Det är användbart när du felsöker synkroniseringsproblem eftersom det låter dig komma åt detaljer om specifika fel.</span><span class="sxs-lookup"><span data-stu-id="14a80-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-synchronization-issues-for-coupled-records"></a><span data-ttu-id="14a80-107">Så här visar du synkroniseringsproblem för sammanfogade poster</span><span class="sxs-lookup"><span data-stu-id="14a80-107">To view synchronization issues for coupled records</span></span>
1. <span data-ttu-id="14a80-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kopplade datasynkroniseringsfel** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="14a80-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="14a80-109">På sidan **sammankopplade datasynkroniseringar** visas problem som uppstod när du synkroniserade kopplade poster.</span><span class="sxs-lookup"><span data-stu-id="14a80-109">The **Coupled Data Synchronization Errors** page shows issues that occurred when you synchronized coupled records.</span></span> <span data-ttu-id="14a80-110">Du kan filtrera och sortera poster och utföra åtgärder såsom **Återställ** eller **Ta bort poster** för att lösa ärenden en och en.</span><span class="sxs-lookup"><span data-stu-id="14a80-110">You can filter and sort records and take actions such as **Restore** or **Delete Records** to resolve issues one by one.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="14a80-111">Så här visar du synkroniseringsloggen för specifika (manuellt synkroniserade) poster</span><span class="sxs-lookup"><span data-stu-id="14a80-111">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="14a80-112">Öppna till exempel kund, artikel eller någon annan post som synkroniserar data mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och försäljning</span><span class="sxs-lookup"><span data-stu-id="14a80-112">Open, for example, a customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales.</span></span>
2. <span data-ttu-id="14a80-113">Välj åtgärden **synkroniseringsloggen** om du vill visa synkroniseringsloggen för en vald post.</span><span class="sxs-lookup"><span data-stu-id="14a80-113">Choose the **Synchronization Log** action to view the synchronization log for a selected record.</span></span> <span data-ttu-id="14a80-114">Det kan till exempel vara en specifik kund som du har synkroniserat manuellt.</span><span class="sxs-lookup"><span data-stu-id="14a80-114">For example, a specific customer you synchronized manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="14a80-115">Se även</span><span class="sxs-lookup"><span data-stu-id="14a80-115">See Also</span></span>  
[<span data-ttu-id="14a80-116">Ställa in Dynamics 365 for Sales integrering i Business Central</span><span class="sxs-lookup"><span data-stu-id="14a80-116">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="14a80-117">Med hjälp av Dynamics 365 for Sales från Business Central</span><span class="sxs-lookup"><span data-stu-id="14a80-117">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
