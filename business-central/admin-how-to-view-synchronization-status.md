---
title: Visa status för en synkroniseringsjobb | Microsoft Docs
description: Lär dig mer om hur du visar statusen efter att ha synkroniserat kopplade poster.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: a54ce7805deafa5d67c3e25b89606a1a40634ad6
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378154"
---
# <a name="view-the-status-of-synchronization-jobs"></a><span data-ttu-id="33f28-103">Visa status för en synkroniseringsjobb</span><span class="sxs-lookup"><span data-stu-id="33f28-103">View the Status of Synchronization Jobs</span></span>
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

<span data-ttu-id="33f28-104">Anvönd sidan **Kopplade datasynkroniseringsfel** för att visa statusen för synkroniseringsjobb som körts för kopplade transaktioner i Dataverse- eller [!INCLUDE[crm_md](includes/crm_md.md)]-integreringar.</span><span class="sxs-lookup"><span data-stu-id="33f28-104">Use the **Coupled Data Synchronization Errors** page to view the status of synchronization jobs that have been run for coupled records in a Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)] integrations.</span></span> <span data-ttu-id="33f28-105">Det innehåller synkroniseringjobb som har körts från jobbkön- och manuella synkroniseringsjobb som kördes på poster från [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="33f28-105">This includes jobs that were run from the job queue and manual synchronization jobs that ran on records from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="33f28-106">Det kan till exempel vara bra att visa deras status vid felsökning eftersom det ger dig tillgång till information om fel som rör sammankopplade poster.</span><span class="sxs-lookup"><span data-stu-id="33f28-106">For example, viewing their status is helpful when troubleshooting because it gives you access to details about errors related to coupled records.</span></span> <span data-ttu-id="33f28-107">Dessa typer av fel orsakas vanligen av användaråtgärder, till exempel när:</span><span class="sxs-lookup"><span data-stu-id="33f28-107">Typically, these types of errors are caused by user actions, for example, when:</span></span>  

* <span data-ttu-id="33f28-108">Två personer gjorde ändringar i samma data i båda affärsappar.</span><span class="sxs-lookup"><span data-stu-id="33f28-108">Two people made a change to the same data in both business apps.</span></span>
* <span data-ttu-id="33f28-109">Någon har tagit bort data i en av apparna, men inte båda.</span><span class="sxs-lookup"><span data-stu-id="33f28-109">Someone deleted data in one of the apps, but not both.</span></span>

> [!Note]
> <span data-ttu-id="33f28-110">På sidan **Kopplade synkroniseringsfel** visas information om projekt som hör samman med kopplade poster.</span><span class="sxs-lookup"><span data-stu-id="33f28-110">The **Coupled Data Synchronization Errors** page shows information about jobs related to coupled records.</span></span> <span data-ttu-id="33f28-111">Om du löser alla fel men posterna fortfarande inte synkroniseras, kan det vara något fel på inställning för integreringen.</span><span class="sxs-lookup"><span data-stu-id="33f28-111">If you resolve all of the errors but records are still not synchronizing, it might have something to do with a setting for the integration.</span></span> <span data-ttu-id="33f28-112">Normalt sett måste administratören lösa dessa typer av fel.</span><span class="sxs-lookup"><span data-stu-id="33f28-112">Typically, your administrator will need to resolve those types of errors.</span></span>   

<!--

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

-->

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a><span data-ttu-id="33f28-113">Så här visar och löser du synkroniseringsfel för kopplade poster</span><span class="sxs-lookup"><span data-stu-id="33f28-113">To view and resolve synchronization errors for coupled records</span></span>
1. <span data-ttu-id="33f28-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Synkroniseringsfel för kopplade data** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="33f28-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="33f28-115">På sidan **sammankopplade datasynkroniseringar** visas problem som uppstod när du synkroniserade kopplade poster.</span><span class="sxs-lookup"><span data-stu-id="33f28-115">The **Coupled Data Synchronization Errors** page shows issues that occurred when you synchronized coupled records.</span></span> <span data-ttu-id="33f28-116">Följande tabell innehåller åtgärder som du kan använda för att lösa ärenden en i taget:</span><span class="sxs-lookup"><span data-stu-id="33f28-116">The following table includes actions that you can use to resolve issues one by one:</span></span>

|<span data-ttu-id="33f28-117">Åtgärd</span><span class="sxs-lookup"><span data-stu-id="33f28-117">Action</span></span>|<span data-ttu-id="33f28-118">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="33f28-118">Description</span></span>|
|----|----|
|<span data-ttu-id="33f28-119">**Ta bort koppling**</span><span class="sxs-lookup"><span data-stu-id="33f28-119">**Remove Coupling**</span></span>|<span data-ttu-id="33f28-120">Tar bort kopplingen för posterna och synkroniserar dem inte längre.</span><span class="sxs-lookup"><span data-stu-id="33f28-120">Uncouples the records and they will no longer synchronize.</span></span> <span data-ttu-id="33f28-121">Om du vill starta om synkroniseringen måste du koppla dem igen.</span><span class="sxs-lookup"><span data-stu-id="33f28-121">To restart the synchronization you must couple them again.</span></span> |
|<span data-ttu-id="33f28-122">**Försök igen** och **Försök alla igen**</span><span class="sxs-lookup"><span data-stu-id="33f28-122">**Retry** and **Retry All**</span></span>|<span data-ttu-id="33f28-123">För varje post där ett fel påträffas hoppas synkroniseringen över om du inte korrigerar ärendet.</span><span class="sxs-lookup"><span data-stu-id="33f28-123">For each record where an error is found, synchronization is skipped unless you fix the issue.</span></span> <span data-ttu-id="33f28-124">Om du försöker igen kommer den valda posten att inkluderas i nästa synkronisering och **Försök alla igen** inkluderar alla posterna.</span><span class="sxs-lookup"><span data-stu-id="33f28-124">Retry will include the selected record in the next synchronization, and **Retry All** includes all of the records.</span></span>|
|<span data-ttu-id="33f28-125">**Synkronisera**</span><span class="sxs-lookup"><span data-stu-id="33f28-125">**Synchronize**</span></span>|<span data-ttu-id="33f28-126">Programmet kommer att försöka lösa en konflikt där data har ändrats i båda affärsapparna.</span><span class="sxs-lookup"><span data-stu-id="33f28-126">The app will try to resolve a conflict where data was changed in both business apps.</span></span> <span data-ttu-id="33f28-127">Du kan välja vila data som ska användas.</span><span class="sxs-lookup"><span data-stu-id="33f28-127">You can choose the data to use.</span></span>|
|<span data-ttu-id="33f28-128">**Återställa poster** och **ta bort poster**</span><span class="sxs-lookup"><span data-stu-id="33f28-128">**Restore Records** and **Delete Records**</span></span>|<span data-ttu-id="33f28-129">Dessa är användbara när en transaktion har tagits bort i en av företagsapparna.</span><span class="sxs-lookup"><span data-stu-id="33f28-129">These are useful when a record was deleted in one of the business apps.</span></span> <span data-ttu-id="33f28-130">"Ta bort poster" tar bort posten eller raden i appen där den fortfarande finns kvar.</span><span class="sxs-lookup"><span data-stu-id="33f28-130">Delete Records deletes the record or row in the app where it still exists.</span></span> <span data-ttu-id="33f28-131">"Återskapa poster" återskapar posten eller raden i den affärsapp där den togs bort.</span><span class="sxs-lookup"><span data-stu-id="33f28-131">Restore Records recreates the record or row in the business app where it was deleted.</span></span>|

> [!NOTE]
> <span data-ttu-id="33f28-132">Om du vill minska antalet konflikter som du behöver lösa kan du ställa in mappningarna för integreringstabellen så att de här åtgärderna tillämpas automatiskt.</span><span class="sxs-lookup"><span data-stu-id="33f28-132">To reduce the number of conflicts you need to resolve, you can set up your integration table mappings to apply these actions automatically.</span></span> <span data-ttu-id="33f28-133">Mer information finns i [Mappning för integreringstabeller](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).</span><span class="sxs-lookup"><span data-stu-id="33f28-133">For more information, [Mapping Integration Tables](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).</span></span>

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a><span data-ttu-id="33f28-134">Så här visar du synkroniseringsloggen för specifika (manuellt synkroniserade) poster</span><span class="sxs-lookup"><span data-stu-id="33f28-134">To view the synchronization log for a specific (manually synchronized) record</span></span>
1. <span data-ttu-id="33f28-135">Öppna till exempel kund, artikel eller någon annan transaktion som synkroniserar data mellan [!INCLUDE[prod_short](includes/prod_short.md)] och Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="33f28-135">Open, for example, a customer, item or any other record that is synchronizing data between [!INCLUDE[prod_short](includes/prod_short.md)] and Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="33f28-136">Välj åtgärden **synkroniseringsloggen** om du vill visa synkroniseringsloggen för en vald post.</span><span class="sxs-lookup"><span data-stu-id="33f28-136">Choose the **Synchronization Log** action to view the synchronization log for a selected record.</span></span> <span data-ttu-id="33f28-137">Det kan till exempel vara en specifik kund som du har synkroniserat manuellt.</span><span class="sxs-lookup"><span data-stu-id="33f28-137">For example, a specific customer you synchronized manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="33f28-138">Se även</span><span class="sxs-lookup"><span data-stu-id="33f28-138">See Also</span></span>  
[<span data-ttu-id="33f28-139">Ställa in konton för integrering med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="33f28-139">Setting Up User Accounts for Integrating with Dynamics 365 Sales</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="33f28-140">Använda Dynamics 365 Sales från Business Central</span><span class="sxs-lookup"><span data-stu-id="33f28-140">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]