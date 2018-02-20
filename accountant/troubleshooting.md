---
title: "Olika sätt att felsöka och lösa problem | Microsoft Docs"
description: "Lär dig hur du kan lösa eventuella problem i Accountant Hub för Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a9753b00b47fc4d74583482b2da92aae5e2f8a74
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="troubleshooting-included365acclongincludesd365acclongmdmd"></a><span data-ttu-id="60c6e-103">Felsökning [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="60c6e-103">Troubleshooting [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span></span>
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

<span data-ttu-id="60c6e-104">Det går enkelt och snabbt att registrera sig för [!INCLUDE[d365acc](includes/d365acc_md.md)].</span><span class="sxs-lookup"><span data-stu-id="60c6e-104">Signing up for [!INCLUDE[d365acc](includes/d365acc_md.md)] is easy and can be done very quickly.</span></span> <span data-ttu-id="60c6e-105">Lägga till klienter på instrumentpanelen är också lätt, men den här artikeln innehåller lösningar på problem som kan uppstå på vägen.</span><span class="sxs-lookup"><span data-stu-id="60c6e-105">Adding clients to the dashboard is also easy, but this article addresses issues that you may have on the way.</span></span>

## <a name="what-email-address-can-i-use-with-included365accincludesd365accmdmd"></a><span data-ttu-id="60c6e-106">Vilken e-postadress kan jag använda med [!INCLUDE[d365acc](includes/d365acc_md.md)]?</span><span class="sxs-lookup"><span data-stu-id="60c6e-106">What email address can I use with [!INCLUDE[d365acc](includes/d365acc_md.md)]?</span></span>
[!INCLUDE[d365acc](includes/d365acc_md.md)]<span data-ttu-id="60c6e-107"> kräver att du använder en e-postadress från ditt arbete eller skola för att registrera dig.</span><span class="sxs-lookup"><span data-stu-id="60c6e-107"> requires that you use a work or school email address to sign up.</span></span> [!INCLUDE[d365acc](includes/d365acc_md.md)]<span data-ttu-id="60c6e-108"> har inte stöd för e-postadresser som tillhandahålls av e-posttjänster för konsumenter eller telekommunikationsleverantörer.</span><span class="sxs-lookup"><span data-stu-id="60c6e-108"> does not support email addresses provided by consumer email services or telecommunication providers.</span></span> <span data-ttu-id="60c6e-109">Dessa omfattar outlook.com, hotmail.com, gmail.com, etc..</span><span class="sxs-lookup"><span data-stu-id="60c6e-109">This includes outlook.com, hotmail.com, gmail.com, and others.</span></span>  

<span data-ttu-id="60c6e-110">Om du försöker att registrera dig med en personlig e-postadress kommer du att få ett meddelande som indikerar att du använder en e-postadress från arbete eller skola.</span><span class="sxs-lookup"><span data-stu-id="60c6e-110">If you try to sign up with a personal email address, you will get a message indicating to use a work or school email address.</span></span>  

## <a name="why-cant-i-connect-to-my-clients-data"></a><span data-ttu-id="60c6e-111">Varför kan jag inte ansluta till min klients data?</span><span class="sxs-lookup"><span data-stu-id="60c6e-111">Why can't I connect to my client's data?</span></span>
<span data-ttu-id="60c6e-112">Det kan finnas ett par anledningar, bland annat följande:</span><span class="sxs-lookup"><span data-stu-id="60c6e-112">There can be a couple of reasons, including the following:</span></span>

- <span data-ttu-id="60c6e-113">URL i fältet **Klient-URL** är inte giltig:</span><span class="sxs-lookup"><span data-stu-id="60c6e-113">The URL in the **Client URL** field is not valid</span></span>  

  <span data-ttu-id="60c6e-114">Gå till **hantera klienter**, öppna klienten som du inte kan ansluta till och välj **Testa klient-URL**.</span><span class="sxs-lookup"><span data-stu-id="60c6e-114">Go to **Manage Clients**, open the client that you cannot connect to, and then choose **Test Client URL**.</span></span>  
- <span data-ttu-id="60c6e-115">Klientens företag är offline, till exempel om den uppgraderas</span><span class="sxs-lookup"><span data-stu-id="60c6e-115">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="60c6e-116">I instrumentpanelen, väljer du menyposten **verktyg** och väljer **kontrollera fel**.</span><span class="sxs-lookup"><span data-stu-id="60c6e-116">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="60c6e-117">Då öppnas en lista med teknisk information, så du kanske vill kontakta administratören om du ser fel.</span><span class="sxs-lookup"><span data-stu-id="60c6e-117">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="60c6e-118">Felmeddelandet ”servern godkände inte klientens referenser” innebär till exempel att du inte har tillgång.</span><span class="sxs-lookup"><span data-stu-id="60c6e-118">For example, the error message "The server has rejected the client credentials" suggests that you do not have access.</span></span>  
- <span data-ttu-id="60c6e-119">Du inte har fått ett e-postmeddelande från klienten som bjuder in dem till deras [!INCLUDE[d365fin](includes/d365fin_md.md)], eller om du inte öppnade länken i e-postmeddelandet eller om du inte accepterade inbjudan</span><span class="sxs-lookup"><span data-stu-id="60c6e-119">You have not received an email from your client that invites them to their [!INCLUDE[d365fin](includes/d365fin_md.md)], or you did not open the link in the email, or you did not accept the invitation</span></span>

  <span data-ttu-id="60c6e-120">Du måste öppna länken i inbjudan och acceptera de steg som lägger till dig i kundens [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="60c6e-120">You must open the link in the invitation and accept the steps that adds you to your client's [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="60c6e-121">Till dess kan har du inte tillgång till deras data.</span><span class="sxs-lookup"><span data-stu-id="60c6e-121">Until then, you do not have access to their data.</span></span>  
- <span data-ttu-id="60c6e-122">Du har inte tillgång till alla företag i din klients [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="60c6e-122">You do not have access to all companies in your client's [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>

  <span data-ttu-id="60c6e-123">Klienten kan ha flera affärsenheter eller företag i [!INCLUDE[d365fin](includes/d365fin_md.md)], och din inbjudan innehåller inte alltid alla företag.</span><span class="sxs-lookup"><span data-stu-id="60c6e-123">Your client can have multiple business units or companies in [!INCLUDE[d365fin](includes/d365fin_md.md)], and your invitation does not always include all companies.</span></span> <span data-ttu-id="60c6e-124">Arbeta med klienten för att se till att du har tillgång till företagen som klienten vill att du arbetar i.</span><span class="sxs-lookup"><span data-stu-id="60c6e-124">Work with your client to make sure that you have access to the companies that the client wants you to work in.</span></span>  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a><span data-ttu-id="60c6e-125">Varför uppdateras inte informationen på min instrumentpanel?</span><span class="sxs-lookup"><span data-stu-id="60c6e-125">Why doesn't the data refresh in my dashboard?</span></span>
<span data-ttu-id="60c6e-126">När du lägger till en klient eller begär en uppdatering av data hämtar [!INCLUDE[d365acc](includes/d365acc_md.md)] data.</span><span class="sxs-lookup"><span data-stu-id="60c6e-126">When you add a client or request a refresh of the data, [!INCLUDE[d365acc](includes/d365acc_md.md)] fetches the data.</span></span> <span data-ttu-id="60c6e-127">Men du måste uppdatera fönstret, till exempel om du väljer åtgärden ”Visa alla företag”, uppdatera webbläsarfönstret, navigera från instrumentpanelen och sedan tillbaka igen, eller liknande.</span><span class="sxs-lookup"><span data-stu-id="60c6e-127">But you must refresh the window yourself, such as choosing the "Redisplay all companies" action, refresh the browser window, navigate away from the dashboard and then back again, or similar.</span></span> <span data-ttu-id="60c6e-128">Detta är ett känt problem som vi arbetar på att förbättra i en senare uppdatering.</span><span class="sxs-lookup"><span data-stu-id="60c6e-128">This is a known issue that we are working on improving in a later update.</span></span>  

## <a name="see-also"></a><span data-ttu-id="60c6e-129">Se även</span><span class="sxs-lookup"><span data-stu-id="60c6e-129">See Also</span></span>
<span data-ttu-id="60c6e-130">[Komma igång med [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="60c6e-130">[Get Started with [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span></span>  
<span data-ttu-id="60c6e-131">[Lägga till klienter i instrumentpanelen i [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span><span class="sxs-lookup"><span data-stu-id="60c6e-131">[Add Clients to Your Dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span></span>  

