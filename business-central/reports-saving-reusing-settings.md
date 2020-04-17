---
title: Använda och ändra inställningarna i rapporter | Microsoft Docs
description: Beskriver hur du använder fördefinierade alternativ och filter för att anpassa en rapport och för att generera korrekta data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 4c43429e4436400dc9e3b991b9ccca59a439372a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191889"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><span data-ttu-id="9ca63-103">Hantera sparade inställningar för rapporter och batch-jobb</span><span class="sxs-lookup"><span data-stu-id="9ca63-103">Manage Saved Settings for Reports and Batch jobs</span></span>
<span data-ttu-id="9ca63-104">När användaren kör en rapport visas vanligtvis en sida där han eller hon kan välja alternativ och ange filter för att ändra den data som inkluderas i den genererade rapporten.</span><span class="sxs-lookup"><span data-stu-id="9ca63-104">When running reports, users are typically presented with a page that lets them select options and set filters to change the data that is included in the generated report.</span></span> <span data-ttu-id="9ca63-105">Denna sida kallas sidan för förfrågan.</span><span class="sxs-lookup"><span data-stu-id="9ca63-105">This page is called the request page.</span></span> <span data-ttu-id="9ca63-106">En rapport kan omfatta en eller flera *sparade(e) inställning(ar)* som användarna kan tillämpa på rapporten från sidan för förfrågan.</span><span class="sxs-lookup"><span data-stu-id="9ca63-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="9ca63-107">*Sparade inställningar* är i grunden fördefinierade alternativ och filter.</span><span class="sxs-lookup"><span data-stu-id="9ca63-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="9ca63-108">Att använda sparade inställningar är ett snabbt och säkert sätt att på ett konsekvent sätt generera rapporter som innehåller korrekta data.</span><span class="sxs-lookup"><span data-stu-id="9ca63-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="9ca63-109">Mer information finns i [Använda sparade inställningar](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="9ca63-109">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

> [!NOTE]
> <span data-ttu-id="9ca63-110">Det här avsnittet avser huvudsakligen ”rapport”, men liknande information gäller för batch-jobb.</span><span class="sxs-lookup"><span data-stu-id="9ca63-110">This topic refers mainly to "report", but similar information applies to batch jobs.</span></span>

<span data-ttu-id="9ca63-111">Om du har rätt behörigheter kan du visa, ändra och skapa sparade inställningarna för alla rapporter för alla användare i företaget.</span><span class="sxs-lookup"><span data-stu-id="9ca63-111">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in a company.</span></span> <span data-ttu-id="9ca63-112">Du kan tilldela sparade inställningar för en rapport till individuella användare eller alla användare i företaget.</span><span class="sxs-lookup"><span data-stu-id="9ca63-112">You can assign saved settings for a report to individual users or to all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="9ca63-113">För att skapa och ändra inställningarna för alla användare</span><span class="sxs-lookup"><span data-stu-id="9ca63-113">To create and modify saved settings for all users</span></span>
<span data-ttu-id="9ca63-114">Du hanterar sparade inställningar från sidan **Rapportinställningar**.</span><span class="sxs-lookup"><span data-stu-id="9ca63-114">You manage saved settings on the **Reports Settings** page.</span></span> <span data-ttu-id="9ca63-115">Det finns två sätt att öppna denna sida:</span><span class="sxs-lookup"><span data-stu-id="9ca63-115">There are two ways to open this page:</span></span>
-   <span data-ttu-id="9ca63-116">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Rapportinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9ca63-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="9ca63-117">Öppna en rapport, välj söktexten bredvid fältet **Använda standardvärden från** och sedan välja åtgärden **Välj från komplett lista**.</span><span class="sxs-lookup"><span data-stu-id="9ca63-117">Open a report, choose the lookup in the **Use default values from** field, and then choose the **Select from full list** action.</span></span>

<span data-ttu-id="9ca63-118">Denna sida visar samtliga befintliga poster för sparade inställningar för samtliga användare.</span><span class="sxs-lookup"><span data-stu-id="9ca63-118">The page displays all the existing saved settings entries for all users.</span></span> <span data-ttu-id="9ca63-119">Om det finns ett användarnamn i fältet **Tilldelad till** kan endast denna användare använda de sparade inställningarna för associerad rapport.</span><span class="sxs-lookup"><span data-stu-id="9ca63-119">If there is a user name in the **Assigned to** field, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="9ca63-120">Om det finns en bock i fältet **Dela med samtliga användare** kan samtliga användare använda de sparade inställningarna för rapporten.</span><span class="sxs-lookup"><span data-stu-id="9ca63-120">If there is a check mark in the **Share with all users** field, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="9ca63-121">Via sidan **Rapportinställningar** kan du:</span><span class="sxs-lookup"><span data-stu-id="9ca63-121">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="9ca63-122">Välj åtgärden **Nytt** för att skapa en ny post för sparade inställningar från grunden.</span><span class="sxs-lookup"><span data-stu-id="9ca63-122">Choose the **New** action to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="9ca63-123">Välja en post för sparade inställningar i listan och sedan välja åtgärden **Kopiera** för att skapa en kopia.</span><span class="sxs-lookup"><span data-stu-id="9ca63-123">Select a saved settings entry from the list, and choose the **Copy** action to create a copy.</span></span>
-   <span data-ttu-id="9ca63-124">Välja en post för sparade inställningar i listan och sedan välja åtgärden **Redigera** för att ändra en post för sparade inställningar.</span><span class="sxs-lookup"><span data-stu-id="9ca63-124">Select a saved settings entry from the list, and choose the **Edit** action to modify a saved settings entry.</span></span>

> [!Important]
> <span data-ttu-id="9ca63-125">Var noggrann när du väljer namn för en post för sparade inställningar.</span><span class="sxs-lookup"><span data-stu-id="9ca63-125">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="9ca63-126">Om du skapar en post för sparade inställningar för samtliga användare, och du ger denna post samma namn som en befintlig post för sparade inställningar som endas tilldelats en specifik användare, så kommer denna användare inte att kunna använda posten för sparade inställningar som tilldelats alla.</span><span class="sxs-lookup"><span data-stu-id="9ca63-126">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="9ca63-127">I avsnittet **Sparade inställningar** på sidan för rapportförfrågan kommer användaren att se två sparade poster för sparade inställningar med samma namn.</span><span class="sxs-lookup"><span data-stu-id="9ca63-127">In the **Saved Settings** section on the request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="9ca63-128">Oavsett vilket alternativ han eller hon väljer kommer emellertid posten för användarspecifika sparade inställningar att användas.</span><span class="sxs-lookup"><span data-stu-id="9ca63-128">However, no matter which option they choose, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="9ca63-129">Funktionen för sparade inställningar finns bara för rapporter där värdet [egenskapen SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property)  på sidan för rapportförfrågan har angetts som **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9ca63-129">The Saved Settings feature is available only on reports where the [SaveValues property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) of the report's request page is set to **Yes**.</span></span> <span data-ttu-id="9ca63-130">Egenskapen **SaveValues** anges i utvecklingsmiljön.</span><span class="sxs-lookup"><span data-stu-id="9ca63-130">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9ca63-131">Se även</span><span class="sxs-lookup"><span data-stu-id="9ca63-131">See Also</span></span>
[<span data-ttu-id="9ca63-132">Arbeta med rapporter och batch-jobb och XMLports</span><span class="sxs-lookup"><span data-stu-id="9ca63-132">Working with Reports, Batch Jobs, and XMLports</span></span>](ui-work-report.md)  
