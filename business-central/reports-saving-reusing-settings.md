---
title: "Använda och ändra inställningarna i rapporter | Microsoft Docs"
description: "Beskriver hur du använder fördefinierade alternativ och filter för att anpassa en rapport och för att generera korrekta data."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 9fd086831c0d145570d87c33c62a003c166aca87
ms.contentlocale: sv-se
ms.lasthandoff: 11/22/2018

---
# <a name="managing-saved-settings-on-reports"></a><span data-ttu-id="16d3a-103">Hantering av sparade inställningar i rapporter</span><span class="sxs-lookup"><span data-stu-id="16d3a-103">Managing Saved Settings on Reports</span></span>
<span data-ttu-id="16d3a-104">När användaren kör en rapport visas vanligtvis en sida där han eller hon kan ange vissa alternativ och filter för att ändra den data som inkluderas i den genererade rapporten.</span><span class="sxs-lookup"><span data-stu-id="16d3a-104">When running a reports, users are typically presented with a page that lets them set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="16d3a-105">Denna sida kallas sidan för rapportförfrågan.</span><span class="sxs-lookup"><span data-stu-id="16d3a-105">This page is called the report request page.</span></span> <span data-ttu-id="16d3a-106">En rapport kan omfatta en eller flera *sparade(e) inställning(ar)* som användarna kan tillämpa på rapporten från sidan för förfrågan.</span><span class="sxs-lookup"><span data-stu-id="16d3a-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="16d3a-107">*Sparade inställningar* är i grunden fördefinierade alternativ och filter.</span><span class="sxs-lookup"><span data-stu-id="16d3a-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="16d3a-108">Att använda sparade inställningar är ett snabbt och säkert sätt att på ett konsekvent sätt generera rapporter som innehåller korrekta data.</span><span class="sxs-lookup"><span data-stu-id="16d3a-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="16d3a-109">Mer information om hur sparade anställningar används finns i [Använda sparade inställningar](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="16d3a-109">For more information about how saved settings are used, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="16d3a-110">Om du har rätt behörigheter kan du visa, ändra och skapa sparade inställningarna för alla rapporter för alla användare i företaget.</span><span class="sxs-lookup"><span data-stu-id="16d3a-110">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="16d3a-111">Du kan tilldela sparade inställningar för en rapport till individuella användare eller alla användare i företaget.</span><span class="sxs-lookup"><span data-stu-id="16d3a-111">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="16d3a-112">Skapa och ändra inställningarna för alla användare</span><span class="sxs-lookup"><span data-stu-id="16d3a-112">Create and modify saved settings for all users</span></span>
<span data-ttu-id="16d3a-113">Du hanterar sparade inställningar från sidan **1560 Rapportinställningar**.</span><span class="sxs-lookup"><span data-stu-id="16d3a-113">You manage saved settings from page **1560 Reports Settings**.</span></span> <span data-ttu-id="16d3a-114">Det finns två sätt att öppna denna sida:</span><span class="sxs-lookup"><span data-stu-id="16d3a-114">There are two ways to open this page:</span></span>
-   <span data-ttu-id="16d3a-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Rapportinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="16d3a-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="16d3a-116">Öppna en rapport, välj söktexten bredvid rutan **Använda standardvärden från:** och sedan **Välj från komplett lista**.</span><span class="sxs-lookup"><span data-stu-id="16d3a-116">Open a report, choose the lookup next to the **Used default values from:** box, choose **Select from full list**.</span></span>

<span data-ttu-id="16d3a-117">Denna sida visar samtliga befintliga poster för sparade inställningar för samtliga användare.</span><span class="sxs-lookup"><span data-stu-id="16d3a-117">The page displays all the existing save settings entries for all users.</span></span> <span data-ttu-id="16d3a-118">Om det finns ett användarnamn i kolumnen **Tilldelad till** kan endast denna användare använda de sparade inställningarna för associerad rapport.</span><span class="sxs-lookup"><span data-stu-id="16d3a-118">If there is a user name in the **Assigned to** column, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="16d3a-119">Om det finns en bock i kolumnen **Dela med samtliga användare** kan samtliga användare använda de sparade inställningarna för rapporten.</span><span class="sxs-lookup"><span data-stu-id="16d3a-119">If there is a check mark in the **Share with all users** column, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="16d3a-120">Via sidan **Rapportinställningar** kan du:</span><span class="sxs-lookup"><span data-stu-id="16d3a-120">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="16d3a-121">Välja **Nytt** för att skapa en ny post för sparade inställningar från grunden.</span><span class="sxs-lookup"><span data-stu-id="16d3a-121">Choose **New** to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="16d3a-122">Välja en post för sparade inställningar i listan och sedan välja **Kopiera** för att skapa en kopia.</span><span class="sxs-lookup"><span data-stu-id="16d3a-122">Select a saved settings entry from the list, and choose **Copy** to create a copy.</span></span>
-   <span data-ttu-id="16d3a-123">Välja en post för sparade inställningar i listan och sedan välja **Redigera** för att ändra en post för sparade inställningar.</span><span class="sxs-lookup"><span data-stu-id="16d3a-123">Select a saved settings entry from the list, and choose **Edit** to modify a saved settings entry.</span></span>


> [!Important]
> <span data-ttu-id="16d3a-124">Var noggrann när du väljer namn för en post för sparade inställningar.</span><span class="sxs-lookup"><span data-stu-id="16d3a-124">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="16d3a-125">Om du skapar en post för sparade inställningar för samtliga användare, och du ger denna post samma namn som en befintlig post för sparade inställningar som endas tilldelats en specifik användare, så kommer denna användare inte att kunna använda posten för sparade inställningar som tilldelats alla.</span><span class="sxs-lookup"><span data-stu-id="16d3a-125">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="16d3a-126">Under **Sparade inställningar** på sidan för rapportförfrågan kommer användaren att se två sparade poster för sparade inställningar med samma namn.</span><span class="sxs-lookup"><span data-stu-id="16d3a-126">Under **Saved Settings** on the report request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="16d3a-127">Oavsett vilket alternativ han eller hon väljer kommer emellertid posten för användarspecifika sparade inställningar att användas.</span><span class="sxs-lookup"><span data-stu-id="16d3a-127">However, no matter which option he chooses, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="16d3a-128">Funktionen för sparade inställningar finns bara för rapporter där [värdet SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) på sidan för rapportförfrågan har angetts som `Yes`.</span><span class="sxs-lookup"><span data-stu-id="16d3a-128">The saved settings feature is available only on reports where the [SaveValues property](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) of the report's request page is set to `Yes`.</span></span> <span data-ttu-id="16d3a-129">Egenskapen **SaveValues** anges i utvecklingsmiljön.</span><span class="sxs-lookup"><span data-stu-id="16d3a-129">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="16d3a-130">Se även</span><span class="sxs-lookup"><span data-stu-id="16d3a-130">See Also</span></span>
[<span data-ttu-id="16d3a-131">Arbeta med rapporter</span><span class="sxs-lookup"><span data-stu-id="16d3a-131">Working with Reports</span></span>](ui-work-report.md)  

