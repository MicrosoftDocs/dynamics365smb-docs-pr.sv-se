---
title: Konfigurera din webbläsare
description: Beskriver hur du konfigurerar webbläsare så att dessa fungerar med Business Central och produkter som är integrerade med det.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 90625ed6d5664efc9605aeacbc66d8174e55799d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776303"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><span data-ttu-id="1fcac-103">Ställa in och felsöka webbläsaren så att den fungerar med webb klienten för Business Central</span><span class="sxs-lookup"><span data-stu-id="1fcac-103">Setting Up and Troubleshooting Your Browser to Work With Business Central Web Client</span></span>

<span data-ttu-id="1fcac-104">I den här artikeln beskrivs hur du konfigurerar din webbläsare så att [!INCLUDE[web_client](includes/web_client.md)] och dess funktioner fungerar korrekt.</span><span class="sxs-lookup"><span data-stu-id="1fcac-104">This article explains how to set up your browser so that the [!INCLUDE[web_client](includes/web_client.md)] and all its features work properly.</span></span> <span data-ttu-id="1fcac-105">Läs den här artikeln om du har problem med att öppna [!INCLUDE[web_client](includes/web_client.md)], detta eftersom vissa problem kan orsakas av webbläsarens inställningar.</span><span class="sxs-lookup"><span data-stu-id="1fcac-105">Read this article if you're having problems opening the [!INCLUDE[web_client](includes/web_client.md)], because some problems may be caused by your browser's settings.</span></span>

<span data-ttu-id="1fcac-106">Artikeln innehåller information om hur du konfigurerar Microsoft Edge, men kraven för JavaScript, cookies och popup-fönster är desamma för alla webbläsare som stöds.</span><span class="sxs-lookup"><span data-stu-id="1fcac-106">The article provides details for setting up Microsoft Edge, but the requirements for JavaScript, cookies, and pop-ups are the same for all supported browsers.</span></span> <span data-ttu-id="1fcac-107">Mer information om andra webbläsare finns i tillverkarens instruktioner.</span><span class="sxs-lookup"><span data-stu-id="1fcac-107">For other browsers, refer to the instructions provided by the manufacturer.</span></span>  

## <a name="use-a-supported-browser"></a><span data-ttu-id="1fcac-108">Använd en webbläsare som stöds</span><span class="sxs-lookup"><span data-stu-id="1fcac-108">Use a supported browser</span></span>

<span data-ttu-id="1fcac-109">Se till att du använder en av de webbläsare som stöds.</span><span class="sxs-lookup"><span data-stu-id="1fcac-109">Make sure to use a one of the supported browsers.</span></span> <span data-ttu-id="1fcac-110">Se [Minimikrav för att använda Business Central](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="1fcac-110">See [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>  

## <a name="allow-javascript-from-business-central"></a><span data-ttu-id="1fcac-111">Tillåt JavaScript från Business Central</span><span class="sxs-lookup"><span data-stu-id="1fcac-111">Allow JavaScript from Business Central</span></span>

<span data-ttu-id="1fcac-112">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="1fcac-112">*Problem:*</span></span>

<span data-ttu-id="1fcac-113">Om webbläsaren inte tillåter JavaScript visas **NotSupported/DisabledJavaScript** i adressfältet och ett **HTTP-fel 404.0 – meddelandet hittades inte** när du försöker öppna [!INCLUDE[prod_short](includes/prod_short.md)], och</span><span class="sxs-lookup"><span data-stu-id="1fcac-113">If the browser doesn't allow JavaScript, you'll see **NotSupported/DisabledJavaScript** in the address bar and an **HTTP Error 404.0 - Not Found** message when you try to open [!INCLUDE[prod_short](includes/prod_short.md)], and the</span></span> 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

<span data-ttu-id="1fcac-114">*Lösningen*</span><span class="sxs-lookup"><span data-stu-id="1fcac-114">*Fix:*</span></span>

1. <span data-ttu-id="1fcac-115">I Microsoft Edge går du till **Inställningar** > **Cookies och webbplatsbehörigheter** > **JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="1fcac-115">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **JavaScript**.</span></span>
2. <span data-ttu-id="1fcac-116">Gör något av följande.</span><span class="sxs-lookup"><span data-stu-id="1fcac-116">Do one of the following steps.</span></span> <span data-ttu-id="1fcac-117">Välj det steg som rekommenderas av organisationen:</span><span class="sxs-lookup"><span data-stu-id="1fcac-117">Choose the step that is recommended by your organization:</span></span>

    - <span data-ttu-id="1fcac-118">Flytta reglaget **Tillåtet** åt vänster (Av).</span><span class="sxs-lookup"><span data-stu-id="1fcac-118">Move the **Allowed** toggle to the left (Off).</span></span> <span data-ttu-id="1fcac-119">Välj sedan **Lägg till** och skriv in webbadressen (URL) för [!INCLUDE[prod_short](includes/prod_short.md)] i rutan **Webbplats**.</span><span class="sxs-lookup"><span data-stu-id="1fcac-119">Then, select **Add** and type the address (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] in the **Site** box.</span></span> <span data-ttu-id="1fcac-120">Välj **Lägg till** när du är klar.</span><span class="sxs-lookup"><span data-stu-id="1fcac-120">Select **Add** when done.</span></span>
    - <span data-ttu-id="1fcac-121">Flytta reglaget **Tillåtet** åt höger (På).</span><span class="sxs-lookup"><span data-stu-id="1fcac-121">Move the **Allowed** toggle to the right (On).</span></span>

## <a name="allow-cookies-from-business-central"></a><span data-ttu-id="1fcac-122">Tillåt cookies från Business Central</span><span class="sxs-lookup"><span data-stu-id="1fcac-122">Allow cookies from Business Central</span></span>

<span data-ttu-id="1fcac-123">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="1fcac-123">*Problem:*</span></span>

<span data-ttu-id="1fcac-124">Om webbläsaren inte tillåter cookies visas följande felmeddelande:</span><span class="sxs-lookup"><span data-stu-id="1fcac-124">If the browser doesn't allow cookies, you'll get the following error:</span></span>

<span data-ttu-id="1fcac-125">**Det gick tyvärr inte att hitta sidan. Kontrollera adressen och försök igen.**</span><span class="sxs-lookup"><span data-stu-id="1fcac-125">**Sorry, the page could not be found. Please check the address and try again.**</span></span> 

<span data-ttu-id="1fcac-126">*Lösningen*</span><span class="sxs-lookup"><span data-stu-id="1fcac-126">*Fix:*</span></span>

1. <span data-ttu-id="1fcac-127">I Microsoft Edge går du till **Inställningar** > **Cookies och webbplatsbehörigheter** > **Cookies och webbplatsdata**.</span><span class="sxs-lookup"><span data-stu-id="1fcac-127">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.</span></span>
2. <span data-ttu-id="1fcac-128">Flytta reglaget för **Tillåt webbplatser att spara och läsa cookiedata** åt höger (På).</span><span class="sxs-lookup"><span data-stu-id="1fcac-128">Move the **Allow sites to save and read cookie data** toggle to the right (On).</span></span>  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a><span data-ttu-id="1fcac-129">Tillåt popup-fönster från Business Central</span><span class="sxs-lookup"><span data-stu-id="1fcac-129">Allow pop-ups from Business Central</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="1fcac-130">integreras med flera produkter.</span><span class="sxs-lookup"><span data-stu-id="1fcac-130">integrates with several products.</span></span> <span data-ttu-id="1fcac-131">I vissa fall, t. ex. när Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] eller "popup-fönster" öppnas i produkten.</span><span class="sxs-lookup"><span data-stu-id="1fcac-131">In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product.</span></span> <span data-ttu-id="1fcac-132">Denna funktion kräver att webbläsaren tillåter popup-fönster från [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1fcac-132">This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="1fcac-133">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="1fcac-133">*Problem:*</span></span>

<span data-ttu-id="1fcac-134">Om popup-fönster för [!INCLUDE[prod_short](includes/prod_short.md)] blockeras visas ett meddelande som påminner om följande:</span><span class="sxs-lookup"><span data-stu-id="1fcac-134">If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:</span></span>

<span data-ttu-id="1fcac-135">**Något gick fel. Din webbläsare kanske blockerar popup-fönster som krävs av Business Central.**</span><span class="sxs-lookup"><span data-stu-id="1fcac-135">**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**</span></span>

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
<span data-ttu-id="1fcac-136">*Lösningen*</span><span class="sxs-lookup"><span data-stu-id="1fcac-136">*Fix:*</span></span>

1. <span data-ttu-id="1fcac-137">I Microsoft Edge går du till **Inställningar** > **Cookies och webbplatsbehörigheter** > **Popup-fönster och omdirigeringar**.</span><span class="sxs-lookup"><span data-stu-id="1fcac-137">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.</span></span>
2. <span data-ttu-id="1fcac-138">Flytta reglaget **Blockerat** åt höger (På).</span><span class="sxs-lookup"><span data-stu-id="1fcac-138">Move the **Blocked** toggle to the right (On).</span></span>
3. <span data-ttu-id="1fcac-139">Välj **Lägg till**.</span><span class="sxs-lookup"><span data-stu-id="1fcac-139">Select **Add**.</span></span> <span data-ttu-id="1fcac-140">I rutan **Webbplats** anger du `https://businesscentral.dynamics.com` och väljer sedan **Lägg till**.</span><span class="sxs-lookup"><span data-stu-id="1fcac-140">In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fcac-141">Se även</span><span class="sxs-lookup"><span data-stu-id="1fcac-141">See Also</span></span>

[<span data-ttu-id="1fcac-142">Felsöka Teams</span><span class="sxs-lookup"><span data-stu-id="1fcac-142">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]