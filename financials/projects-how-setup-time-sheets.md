---
title: "Ställa in tidrapporter och deras godkännande | Microsoft Docs"
description: "Du lägger upp tidrapporter för att spåra den tid som använts för projekt och använder resurser kan hjälpa dig med projekthantering, personal och kapacitet"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a5b2027649e2adddfd3e59b4376303059f575a99
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-time-sheets"></a><span data-ttu-id="d8cfa-103">Så här skapar du tidrapporter</span><span class="sxs-lookup"><span data-stu-id="d8cfa-103">Set Up Time Sheets</span></span>
<span data-ttu-id="d8cfa-104">Tidrapporter i [!INCLUDE[d365fin](includes/d365fin_md.md)] hanterar tidregistrering veckovis, med sju dagars steg i taget.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-104">Time sheets in [!INCLUDE[d365fin](includes/d365fin_md.md)] handle time registration in weekly increments of seven days.</span></span> <span data-ttu-id="d8cfa-105">Du kan använda dem för att spåra den tid som används för projektet och du kan använda dem för att registrera enkel resurstimregistrering.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-105">You use them to track the time used on jobs, and you can use them to record simple resource time registration.</span></span> <span data-ttu-id="d8cfa-106">Innan du kan använda tidrapporter måste du ange hur du vill att de ska registreras och konfigureras.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-106">Before you can use time sheets, you must specify how you want them to be set up and configured.</span></span>

<span data-ttu-id="d8cfa-107">När du har ställt in hur organisationen ska använda tidrapporter, kan du ange om och hur tidrapporter godkänns.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-107">After you have set up how your organization will use time sheets, you can specify if and how time sheets are approved.</span></span> <span data-ttu-id="d8cfa-108">Beroende på organisationens behov kan du ange:</span><span class="sxs-lookup"><span data-stu-id="d8cfa-108">Depending on the needs of your organization, you can designate:</span></span>

* <span data-ttu-id="d8cfa-109">En eller flera användare som tidrapportsadministratör och godkännare för alla tidrapporter.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-109">One or more users as the time sheet administrator and approver for all time sheets.</span></span>
* <span data-ttu-id="d8cfa-110">En tidrapportsgodkännare för varje resurs.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-110">A time sheet approver for each resource.</span></span>

<span data-ttu-id="d8cfa-111">När du har konfigurerat tidrapporter, kan du skapa tidrapporter för resurser, tilldela dem till projektplaneringsrader och bokföra tidrapportrader.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-111">When you have set up time sheets, you can create time sheets for resources, assign them to job planning lines, and post time sheet lines.</span></span> <span data-ttu-id="d8cfa-112">Mer information finns i [Så här använder du tidrapporter](projects-how-use-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="d8cfa-112">For more information, see [Use Time Sheets](projects-how-use-time-sheets.md).</span></span>

## <a name="to-set-up-general-information-for-time-sheets"></a><span data-ttu-id="d8cfa-113">Så här anger du allmän information för tidrapporter</span><span class="sxs-lookup"><span data-stu-id="d8cfa-113">To set up general information for time sheets</span></span>
1. <span data-ttu-id="d8cfa-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Resursinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resources Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d8cfa-115">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="d8cfa-116">För fältet **Tidrapport per projektgodkännande** väljer du ett av följande alternativ.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-116">For the **Time Sheet by Job Approval** field, select one of the following options.</span></span>

| <span data-ttu-id="d8cfa-117">Alternativ</span><span class="sxs-lookup"><span data-stu-id="d8cfa-117">Option</span></span> | <span data-ttu-id="d8cfa-118">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d8cfa-118">Description</span></span> |
| --- | --- |
| <span data-ttu-id="d8cfa-119">**Aldrig**</span><span class="sxs-lookup"><span data-stu-id="d8cfa-119">**Never**</span></span> |<span data-ttu-id="d8cfa-120">Användaren i fältet **Användar-ID för tidrapportens godkännare** på resurskortet godkänner tidrapporten.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-120">The user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |
| <span data-ttu-id="d8cfa-121">**Alltid**</span><span class="sxs-lookup"><span data-stu-id="d8cfa-121">**Always**</span></span> |<span data-ttu-id="d8cfa-122">Användaren i fältet **Ansvarig person** på projektkortet godkänner tidrapporten.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-122">The user in the **Person Responsible** field on the job card approves the time sheet.</span></span> |
| <span data-ttu-id="d8cfa-123">**Enbart maskin**</span><span class="sxs-lookup"><span data-stu-id="d8cfa-123">**Machine Only**</span></span> |<span data-ttu-id="d8cfa-124">Om maskinens tidrapport är länkad till ett projekt, godkänner användaren i fältet **Ansvarig person** på projektkortet tidrapporten.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-124">If the machine time sheet is linked with a job, then the user in the **Person Responsible** field on the job card approves the time sheet.</span></span> <span data-ttu-id="d8cfa-125">Om maskinens tidrapport är länkad till en resurs, godkänner användaren i fältet **Användar-ID för tidrapportens godkännare** på resurskortet tidrapporten.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-125">If the machine time sheet is linked with a resource, then the user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |

## <a name="to-assign-a-time-sheet-administrator"></a><span data-ttu-id="d8cfa-126">Så här tilldelar du en tidrapportsadministratör</span><span class="sxs-lookup"><span data-stu-id="d8cfa-126">To assign a time sheet administrator</span></span>
1. <span data-ttu-id="d8cfa-127">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Resursinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d8cfa-128">Lägg till en ny användare om användarlistan inte innehåller den person som du vill ska vara tidrapportsadministratören.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-128">Add a new user if the user list does not include the person who you want to be the time sheet administrator.</span></span> <span data-ttu-id="d8cfa-129">Mer information finns i [Hantera användare och behörigheter](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="d8cfa-129">For more information, see [Manage Users and Permissions](ui-how-users-permissions.md).</span></span>
3. <span data-ttu-id="d8cfa-130">Välj en användare som ska vara en tidrapportadministratör och välj sedan kryssrutan **Tidrapportadmin.**</span><span class="sxs-lookup"><span data-stu-id="d8cfa-130">Select a user to be a time sheet administrator, and then select the **Time Sheet Admin.** check box.</span></span>  

> [!TIP]  
>   <span data-ttu-id="d8cfa-131">Vi rekommenderar att du endast anger en användare som tidrapportsadministratör för ett företag.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-131">It is recommended that you designate only one user to be the time sheet administrator for a company.</span></span> <span data-ttu-id="d8cfa-132">I följande procedur skapar du en tidrapportägare och godkännare där tidrapportgodkännaren tilldelas för varje resurs.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-132">In the following procedure, you set up a time sheet owner and approver where the time sheet approver is assigned for each resource.</span></span>  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a><span data-ttu-id="d8cfa-133">Så här tilldelar du en tidrapportsägare och en godkännare</span><span class="sxs-lookup"><span data-stu-id="d8cfa-133">To assign a time sheets owner and approver</span></span>
1. <span data-ttu-id="d8cfa-134">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Resurser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-134">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resources**, and then choose the related link.</span></span>
2. <span data-ttu-id="d8cfa-135">Välj den resurs som du vill ställa in möjlighet att använda tidrapporter för och markera sedan kryssrutan **Använd tidrapport**.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-135">Select the resource for which you want to set up the ability to use time sheets, and then select the **Use Time Sheet** check box.</span></span>  
3. <span data-ttu-id="d8cfa-136">I fältet **Användar-ID för tidrapportens ägare** anger du ID för ägaren av tidrapporten.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-136">In the **Time Sheet Owner User ID** field, enter the ID of the owner of the time sheet.</span></span> <span data-ttu-id="d8cfa-137">Ägaren kan ange tidförbrukning på en tidrapport och skicka den för godkännande.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-137">The owner can enter time usage on a time sheet and submit it for approval.</span></span> <span data-ttu-id="d8cfa-138">Vanligtvis, när resursen är en person, är den person också ägare.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-138">In general, when the resource is a person, that person is also the owner.</span></span>  
4. <span data-ttu-id="d8cfa-139">I fältet **Användar-ID för tidrapportens godkännare** anger du ID för godkännaren av tidrapporten.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-139">In the **Time Sheet Approver User ID** field, enter the ID of the approver of the time sheet.</span></span> <span data-ttu-id="d8cfa-140">Godkännaren kan godkänna, avvisa eller öppna en tidrapport igen.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-140">The approver can approve, reject, or reopen a time sheet.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="d8cfa-141">Du kan inte ändra ID på tidrapportsgodkännaren om det finns tidrapporter som inte ännu har behandlats och har statusen **Skickad** eller **Öppen**.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-141">You cannot change the ID of the time sheet approver if there are time sheets that have not yet been processed and have the status of **Submitted** or **Open**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8cfa-142">Se även</span><span class="sxs-lookup"><span data-stu-id="d8cfa-142">See Also</span></span>
[<span data-ttu-id="d8cfa-143">Ställa in projekthantering</span><span class="sxs-lookup"><span data-stu-id="d8cfa-143">Setting Up Project Management</span></span>](projects-setup-projects.md)  
[<span data-ttu-id="d8cfa-144">Projekthantering</span><span class="sxs-lookup"><span data-stu-id="d8cfa-144">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="d8cfa-145">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="d8cfa-145">Finance</span></span>](finance.md)  
<span data-ttu-id="d8cfa-146">[Inköp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="d8cfa-146">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="d8cfa-147">[Försäljning](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="d8cfa-147">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="d8cfa-148">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d8cfa-148">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

