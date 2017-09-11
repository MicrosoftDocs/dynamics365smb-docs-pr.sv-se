---
title: "Använda och ändra inställningarna i rapporter | Microsoft Docs"
description: "Beskriver hur du använder fördefinierade alternativ och filter för att anpassa en rapport och för att generera korrekta data."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9e5f7417579a5ba0629032cf9fa664e0060b9cbf
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="saved-settings-on-reports"></a><span data-ttu-id="e1761-103">Sparade inställningar i rapporter</span><span class="sxs-lookup"><span data-stu-id="e1761-103">Saved Settings on Reports</span></span>
<span data-ttu-id="e1761-104">Beroende på rapporten som körs, kan du presenteras med en sida som gör att du kan ange vissa alternativ och filter för att ändra data som ingår i den skapade rapporten.</span><span class="sxs-lookup"><span data-stu-id="e1761-104">Depending on the report that is run, you might be presented with a page that lets you to set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="e1761-105">Den här sidan är känd som sidan för rapportbegäran.</span><span class="sxs-lookup"><span data-stu-id="e1761-105">This page is known as the report request page.</span></span> <span data-ttu-id="e1761-106">En rapport kan innehålla en eller flera *sparade inställningar* som du kan tillämpa till rapporten från sidan för begäran.</span><span class="sxs-lookup"><span data-stu-id="e1761-106">A report can include one or more *saved settings* that you can apply to the report from the request page.</span></span> <span data-ttu-id="e1761-107">*Sparade inställningar* är i grunden fördefinierade alternativ och filter.</span><span class="sxs-lookup"><span data-stu-id="e1761-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="e1761-108">Att använda sparade inställningar är ett snabbt och pålitligt sätt att konsekvent skapa rapporter som innehåller korrekta data.</span><span class="sxs-lookup"><span data-stu-id="e1761-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span>

<span data-ttu-id="e1761-109">Du kan se de sparade inställningar som är tillgängliga för dig för en rapport i avsnittet **Sparade inställningar** på sidan för rapportbegäran.</span><span class="sxs-lookup"><span data-stu-id="e1761-109">You can see the saved settings that are available to you for a report in **Saved Settings** section of the report request page.</span></span>  

## <a name="to-apply-saved-settings-to-a-report"></a><span data-ttu-id="e1761-110">Om du vill ange sparade inställningar till en rapport</span><span class="sxs-lookup"><span data-stu-id="e1761-110">To apply saved settings to a report</span></span>
1. <span data-ttu-id="e1761-111">Öppna rapporten.</span><span class="sxs-lookup"><span data-stu-id="e1761-111">Open the report.</span></span>

   <span data-ttu-id="e1761-112">Sidan för rapportbegäran visas.</span><span class="sxs-lookup"><span data-stu-id="e1761-112">The report request page appears.</span></span>    
2. <span data-ttu-id="e1761-113">I avsnittet **Sparade inställningar** på sidan anger du fältet **Namn** till de sparade inställningar som du vill använda.</span><span class="sxs-lookup"><span data-stu-id="e1761-113">In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.</span></span>

   <span data-ttu-id="e1761-114">Avsnittet **Sparade inställningar** visas bara om rapporten har körts tidigare eller om det finns befintliga poster med sparade inställningar.</span><span class="sxs-lookup"><span data-stu-id="e1761-114">The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries.</span></span> <span data-ttu-id="e1761-115">Posten vid namn **Senast använda alternativ och filter** med sparade inställningar är alltid tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="e1761-115">The saved settings entry called **Last used options and filters** is always available.</span></span> <span data-ttu-id="e1761-116">Dessa inställningar är de alternativ- och filtervärden som användes förra gången som du körde rapporten.</span><span class="sxs-lookup"><span data-stu-id="e1761-116">These settings are the option and filter values that were used the last time you ran the report.</span></span>

## <a name="administer-saved-report-settings-for-users"></a><span data-ttu-id="e1761-117">Administrera sparade rapportinställningar för användare</span><span class="sxs-lookup"><span data-stu-id="e1761-117">Administer saved report settings for users</span></span>
<span data-ttu-id="e1761-118">Om du har rätt behörigheter kan du visa, ändra och skapa sparade inställningarna för alla rapporter för alla användare i företaget.</span><span class="sxs-lookup"><span data-stu-id="e1761-118">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="e1761-119">Du kan tilldela sparade inställningar för en rapport till individuella användare eller alla användare i företaget.</span><span class="sxs-lookup"><span data-stu-id="e1761-119">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<span data-ttu-id="e1761-120">Du hanterar sparade inställningar från sidan 1506 **rapportinställningar**.</span><span class="sxs-lookup"><span data-stu-id="e1761-120">You manage saved settings from page 1506 **Reports Settings**.</span></span> <span data-ttu-id="e1761-121">För att öppna denna sida väljer du ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rappor"), ange **Rapporinställningar**, och väljer sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e1761-121">To open this page, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Settings**, and then choose the related link.</span></span>

<span data-ttu-id="e1761-122">Från sidan **Rapporinställningar** kan du skapa nya inställningar från noll, eller så kan du göra en kopia och ändra befintliga inställningar.</span><span class="sxs-lookup"><span data-stu-id="e1761-122">From the **Report Settings** page, you can create a new settings from scratch or you can make a copy and modify existing settings.</span></span> <span data-ttu-id="e1761-123">För att ändra alternativ och filter för inställningar väljer du åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="e1761-123">To modify the options and filters for a settings, choose the **Edit** action.</span></span>

<span data-ttu-id="e1761-124">**Anteckningar**:</span><span class="sxs-lookup"><span data-stu-id="e1761-124">**Notes:**</span></span>

* <span data-ttu-id="e1761-125">Funktionen för sparade inställningar i rapporter är bara relevant när egenskapen SaveValues på sidan för begäran är inställd på Ja.</span><span class="sxs-lookup"><span data-stu-id="e1761-125">The saved settings feature on reports is only relevant when the SaveValues property of the request page is set to Yes.</span></span> <span data-ttu-id="e1761-126">Egenskapen SaveValues anges i utvecklingsmiljön.</span><span class="sxs-lookup"><span data-stu-id="e1761-126">The SaveValues property property is set in the development environment.</span></span>
* <span data-ttu-id="e1761-127">Om du skapar en artikel med sparade inställningar för alla användare och denna artikel har samma namn som befintliga sparade inställningar för en viss användare, kan den användaren inte använda de sparade inställningar som har tilldelats alla.</span><span class="sxs-lookup"><span data-stu-id="e1761-127">If you create a saved settings item for all users, and it has the same name as an existing saved settings for a specific user, then that user will not be able to use the saved settings that is assigned to everyone.</span></span>  <span data-ttu-id="e1761-128">I fältet Sparade inställningar på sidan för rapportbegäran visas två alternativ för sparade inställningar med samma namn.</span><span class="sxs-lookup"><span data-stu-id="e1761-128">In the Saved Settings field on the report request page, the user will see two saved settings options with the same name.</span></span> <span data-ttu-id="e1761-129">Oavsett vilket alternativ användaren väljer kommer de användarspecifika sparade inställningarna att tillämpas.</span><span class="sxs-lookup"><span data-stu-id="e1761-129">However, no matter which option he chooses, the user-specific saved settings will be used.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1761-130">Se även</span><span class="sxs-lookup"><span data-stu-id="e1761-130">See Also</span></span>
[<span data-ttu-id="e1761-131">Så här schemalägger du en rapportkörning</span><span class="sxs-lookup"><span data-stu-id="e1761-131">Schedule a Rpeort to Run</span></span>](ui-schedule-report.md)  

