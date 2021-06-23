---
title: Optimera Outlook för din företagsinkorg
description: Lär dig mer om vad du kan göra för att förbättra upplevelsen av inkorgen för företag i Microsoft Outlook.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in
ms.date: 05/12/2021
ms.author: jswymer
ms.openlocfilehash: 2fee1782057d0f45319e4d12d715c2e1e0d3d4a6
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/19/2021
ms.locfileid: "6064862"
---
# <a name="optimizing-outlook-for-your-business-inbox"></a><span data-ttu-id="f573c-103">Optimera Outlook för din företagsinkorg</span><span class="sxs-lookup"><span data-stu-id="f573c-103">Optimizing Outlook for Your Business Inbox</span></span> 

<span data-ttu-id="f573c-104">I den här artikeln beskrivs saker du kan göra för att få bästa möjliga erfarenhet av inkorgen för företag i Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="f573c-104">This article discusses things you can do to get the best possible experience with the Business Inbox in Microsoft Outlook.</span></span> 

## <a name="update-outlook"></a><span data-ttu-id="f573c-105">Uppdatera Outlook</span><span class="sxs-lookup"><span data-stu-id="f573c-105">Update Outlook</span></span>

<span data-ttu-id="f573c-106">Uppdatera till Outlook-version 2012 eller nyare.</span><span class="sxs-lookup"><span data-stu-id="f573c-106">Update to Outlook version 2012 or newer.</span></span>

> [!NOTE]
> <span data-ttu-id="f573c-107">Om du inte kan uppdatera Outlook till version 2012 eller senare bör du kontrollera att du åtminstone uppdaterar till version 1905.</span><span class="sxs-lookup"><span data-stu-id="f573c-107">If you are unable to update Outlook to version 2012 or later, make sure that you at least update to version 1905.</span></span> <span data-ttu-id="f573c-108">Detta förhindrar att Outlook-tillägget körs med hjälp av äldre Internet Explorer-komponenter</span><span class="sxs-lookup"><span data-stu-id="f573c-108">This prevents the Outlook Add-in from running using legacy Internet Explorer components</span></span>

### <a name="how-to-check-your-version-of-outlook"></a><span data-ttu-id="f573c-109">Kontrollera din version av Outlook</span><span class="sxs-lookup"><span data-stu-id="f573c-109">How to check your version of Outlook</span></span>

<span data-ttu-id="f573c-110">Oavsett om du använder Office 2019 eller Microsoft 365 kan du kontrollera vilken version av Outlook du har genom att följa den här Microsoft Support-guiden:</span><span class="sxs-lookup"><span data-stu-id="f573c-110">Whether you use Office 2019 or Microsoft 365, follow this Microsoft Support guide to check which version of Outlook you have:</span></span>  

[<span data-ttu-id="f573c-111">Om Office: vilken version av Office använder jag?</span><span class="sxs-lookup"><span data-stu-id="f573c-111">About Office: What version of Office am I using?</span></span>](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### <a name="how-to-update-outlook"></a><span data-ttu-id="f573c-112">Uppdatera Outlook</span><span class="sxs-lookup"><span data-stu-id="f573c-112">How to update Outlook</span></span>

<span data-ttu-id="f573c-113">Om du vill uppdatera Outlook till den senaste versionen följer du den här Microsoft Support-guiden eller kontaktar administratören:</span><span class="sxs-lookup"><span data-stu-id="f573c-113">To update Outlook to the latest version, follow this Microsoft Support guide or contact your administrator:</span></span>

[<span data-ttu-id="f573c-114">Installera Office-uppdateringar</span><span class="sxs-lookup"><span data-stu-id="f573c-114">Install Office updates</span></span>](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## <a name="install-microsoft-edge-webview2"></a><span data-ttu-id="f573c-115">Installera Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="f573c-115">Install Microsoft Edge WebView2</span></span>

<span data-ttu-id="f573c-116">Kontrollera att Microsoft Edge WebView2 är installerat på enheten.</span><span class="sxs-lookup"><span data-stu-id="f573c-116">Ensure that Microsoft Edge WebView2 is installed on your device.</span></span>

### <a name="how-to-check-if-microsoft-edge-webview2-is-installed"></a><span data-ttu-id="f573c-117">Så här kontrollerar du om Microsoft Edge WebView2 har installerats</span><span class="sxs-lookup"><span data-stu-id="f573c-117">How to check if Microsoft Edge WebView2 is installed</span></span> 

<span data-ttu-id="f573c-118">Så här kontrollerar du om du har Microsoft Edge WebView2 installerat på en dator:</span><span class="sxs-lookup"><span data-stu-id="f573c-118">To check if you have Microsoft Edge WebView2 installed on a computer, do the following steps:</span></span>

<span data-ttu-id="f573c-119">Från Start-menyn:</span><span class="sxs-lookup"><span data-stu-id="f573c-119">From Start menu:</span></span>

1. <span data-ttu-id="f573c-120">Välj **Start** ![Windows Start](media/windows-start-icon.png "Startikon för Windows") > **Inställningar** ![Windows-inställningar](media/windows-settings-icon.png "Ikon för Windows-inställningar") > **Appar och funktioner**.</span><span class="sxs-lookup"><span data-stu-id="f573c-120">Choose **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon") > **Settings** ![Windows Settings](media/windows-settings-icon.png "Windows Settings icon") > **Apps & Features**.</span></span>
2. <span data-ttu-id="f573c-121">I sökrutan skriver du **WebView2**.</span><span class="sxs-lookup"><span data-stu-id="f573c-121">In the search box, type **WebView2**.</span></span> <span data-ttu-id="f573c-122">Om Microsoft Edge WebView2 är installerat visas en post med namnet **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="f573c-122">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

<span data-ttu-id="f573c-123">Från kontrollpanelen:</span><span class="sxs-lookup"><span data-stu-id="f573c-123">From Control Panel:</span></span>

1. <span data-ttu-id="f573c-124">I sökrutan bredvid **Start** ![Windows Start](media/windows-start-icon.png "Startikon för Windows") skriver du **Kontrollpanel** och väljer sedan resultatet.</span><span class="sxs-lookup"><span data-stu-id="f573c-124">In the search box next to **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon"), type **Control Panel**, and then select the result.</span></span>
2. <span data-ttu-id="f573c-125">Välj **Program** > **Program och funktioner**.</span><span class="sxs-lookup"><span data-stu-id="f573c-125">Choose **Programs** > **Programs and Features**.</span></span>
3. <span data-ttu-id="f573c-126">I sökrutan skriver du **WebView2**.</span><span class="sxs-lookup"><span data-stu-id="f573c-126">In the search box, type **WebView2**.</span></span> <span data-ttu-id="f573c-127">Om Microsoft Edge WebView2 är installerat visas en post med namnet **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="f573c-127">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

### <a name="how-to-install-microsoft-edge-webview2"></a><span data-ttu-id="f573c-128">Installera Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="f573c-128">How to install Microsoft Edge WebView2</span></span> 

1. <span data-ttu-id="f573c-129">Använd webbläsaren och gå till [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span><span class="sxs-lookup"><span data-stu-id="f573c-129">Using your browser, go to [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span></span>
2. <span data-ttu-id="f573c-130">Välj **Hämta**.</span><span class="sxs-lookup"><span data-stu-id="f573c-130">Choose **Download**.</span></span>
3. <span data-ttu-id="f573c-131">Ange **Välj arkitektur** som motsvarar ditt system.</span><span class="sxs-lookup"><span data-stu-id="f573c-131">Set **Select Architecture** to match your system.</span></span>
4. <span data-ttu-id="f573c-132">Välj **Hämta**.</span><span class="sxs-lookup"><span data-stu-id="f573c-132">Choose **Download**.</span></span>

> [!NOTE]
> <span data-ttu-id="f573c-133">Din organisation kan ha en begränsning på vilka komponenter som kan installeras på din enhet.</span><span class="sxs-lookup"><span data-stu-id="f573c-133">Your organization may have restriction on which components can be installed on your device.</span></span> <span data-ttu-id="f573c-134">Kontakta administratören om du behöver hjälp.</span><span class="sxs-lookup"><span data-stu-id="f573c-134">Contact your administrator for assistance.</span></span>

## <a name="use-a-supported-browser"></a><span data-ttu-id="f573c-135">Använd en webbläsare som stöds</span><span class="sxs-lookup"><span data-stu-id="f573c-135">Use a supported browser</span></span>

<span data-ttu-id="f573c-136">Du kan använda Outlook för webben i en av de webbläsare som stöds av Business Central.</span><span class="sxs-lookup"><span data-stu-id="f573c-136">Consider using Outlook for the Web in one of the browsers supported by Business Central.</span></span> <span data-ttu-id="f573c-137">En lista över vilka webbläsare som stöds finns i [Minimikrav för att använda Business Central](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="f573c-137">For a list of supported browsers, see [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>

## <a name="see-also"></a><span data-ttu-id="f573c-138">Se även</span><span class="sxs-lookup"><span data-stu-id="f573c-138">See Also</span></span>

[<span data-ttu-id="f573c-139">Gör dig redo att göra affärer</span><span class="sxs-lookup"><span data-stu-id="f573c-139">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
[<span data-ttu-id="f573c-140">Få Business Central på min mobila enhet</span><span class="sxs-lookup"><span data-stu-id="f573c-140">Getting Business Central on my Mobile Device</span></span>](install-mobile-app.md)  
[<span data-ttu-id="f573c-141">Skicka dokument via e-post</span><span class="sxs-lookup"><span data-stu-id="f573c-141">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="f573c-142">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="f573c-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="f573c-143">Försäljning</span><span class="sxs-lookup"><span data-stu-id="f573c-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="f573c-144">Inköp</span><span class="sxs-lookup"><span data-stu-id="f573c-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="f573c-145">Minsta krav för Outlook</span><span class="sxs-lookup"><span data-stu-id="f573c-145">Minimum Requirements for Outlook</span></span>](product-requirements.md#outlook)  
[<span data-ttu-id="f573c-146">Använda tillägg i Outlook på Internet</span><span class="sxs-lookup"><span data-stu-id="f573c-146">Using add-ins in Outlook on the web</span></span>](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]