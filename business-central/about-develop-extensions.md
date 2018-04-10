---
title: Anpassa Dynamics 365 Business Central | Microsoft Docs
description: "Skapa, presentera och marknadsför dina appar och tillägg för Business Central."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5f3557de5d69b8f64f85fabe4a60ecbddef276eb
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="extending-included365finlongincludesd365finlongmdmd"></a><span data-ttu-id="c0207-103">Utökning av [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0207-103">Extending [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="c0207-104">Det finns många fördelar med att använda [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] som en plattform för programverktyg:</span><span class="sxs-lookup"><span data-stu-id="c0207-104">There are plenty of benefits of using [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] as a platform for App builders:</span></span>

* <span data-ttu-id="c0207-105">Utöka [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], en beprövad Microsoft online-lösning med dina kunskaper</span><span class="sxs-lookup"><span data-stu-id="c0207-105">Enrich [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], a proven Microsoft online solution, with your expertise</span></span>  
* <span data-ttu-id="c0207-106">Utnyttja varumärket Business Central - ett varumärke som miljontals användare känner till och litar på</span><span class="sxs-lookup"><span data-stu-id="c0207-106">Leverage the Business Central brand – a brand that millions of users know and trust</span></span>  
* <span data-ttu-id="c0207-107">Nå fler kunder till dina affärsprogram med [Microsoft AppSource](https://appsource.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="c0207-107">Reach more customers for your business apps with [Microsoft AppSource](https://appsource.microsoft.com/)</span></span>  
* <span data-ttu-id="c0207-108">Uppnå mer med en plattform som ger en modern upplevelse och erbjuder skalning</span><span class="sxs-lookup"><span data-stu-id="c0207-108">Achieve more with a platform that delivers a modern experience and offers scale</span></span>  
* <span data-ttu-id="c0207-109">Samla intelligent business-program som t.ex. PowerApps, Flow, Power BI, Cortana Intelligence och mycket mer</span><span class="sxs-lookup"><span data-stu-id="c0207-109">Bundle with intelligent business apps such as PowerApps, Flow, Power BI, Cortana Intelligence, and many more</span></span>  

## <a name="to-bring-your-included365finincludesd365finmdmd-app-into-appsource"></a><span data-ttu-id="c0207-110">Hämta din [!INCLUDE[d365fin](includes/d365fin_md.md)]-app i AppSource:</span><span class="sxs-lookup"><span data-stu-id="c0207-110">To bring your [!INCLUDE[d365fin](includes/d365fin_md.md)] app into AppSource:</span></span>
+ <span data-ttu-id="c0207-111">Skapa konton</span><span class="sxs-lookup"><span data-stu-id="c0207-111">Create your accounts</span></span>  
<span data-ttu-id="c0207-112">Vi vill att du ska ha tillgång till alla nödvändiga verktyg.</span><span class="sxs-lookup"><span data-stu-id="c0207-112">We want you to have access to all the necessary tools!</span></span> <span data-ttu-id="c0207-113">Du måste ha en Microsoft Partner Network-ID, ett utvecklarkonto och ett PSBC-konto.</span><span class="sxs-lookup"><span data-stu-id="c0207-113">You must have a Microsoft Partner Network ID, a Developer account, and a PSBC account.</span></span>
<span data-ttu-id="c0207-114">Mer information om hur du får dina konton på plats finns i dokumentet [Skapa dina konton.pdf](https://go.microsoft.com/fwlink/?linkid=841514) från Download Center.</span><span class="sxs-lookup"><span data-stu-id="c0207-114">For more information about how you can get your accounts in place, get the [Create your accounts.pdf](https://go.microsoft.com/fwlink/?linkid=841514) document from the Download Center.</span></span>

+ <span data-ttu-id="c0207-115">Samarbeta med oss om din app-idé</span><span class="sxs-lookup"><span data-stu-id="c0207-115">Engage with us about your app idea</span></span>  
<span data-ttu-id="c0207-116">Dela din [!INCLUDE[d365fin](includes/d365fin_md.md)]-app med oss på Microsoft AppSource!</span><span class="sxs-lookup"><span data-stu-id="c0207-116">Share your [!INCLUDE[d365fin](includes/d365fin_md.md)] app idea with us on Microsoft AppSource!</span></span> <span data-ttu-id="c0207-117">När du skickar en idé, samarbetar vi med dig och ger dig allt du behöver för att börja arbeta med din app.</span><span class="sxs-lookup"><span data-stu-id="c0207-117">After submitting your idea, we will engage with you and provide you with everything you need to start working on your app.</span></span>
<span data-ttu-id="c0207-118">Mer information om alla åtgärder finns i dokumentet [Samarbeta med oss om din app-idé.pdf](https://go.microsoft.com/fwlink/?linkid=841515) från Download Center.</span><span class="sxs-lookup"><span data-stu-id="c0207-118">For more information about all the steps, get the [Engage with us about your app idea document.pdf](https://go.microsoft.com/fwlink/?linkid=841515) document from the Download Center.</span></span>

+ <span data-ttu-id="c0207-119">Utveckla tekniska aspekter av din app</span><span class="sxs-lookup"><span data-stu-id="c0207-119">Develop the technical aspects of your app</span></span>    
<span data-ttu-id="c0207-120">När du har skapat din egna apputvecklingsmiljö kan du utveckla din app.</span><span class="sxs-lookup"><span data-stu-id="c0207-120">After you have set up your own app development environment, you can develop your app.</span></span>
<span data-ttu-id="c0207-121">Mer information om allt du behöver veta om hur du utvecklar tekniska aspekter av din [!INCLUDE[d365fin](includes/d365fin_md.md)]-app finns i dokumentet [utveckla de tekniska aspekterna av din app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) från Download Center.</span><span class="sxs-lookup"><span data-stu-id="c0207-121">For more information about everything you need to know about how to develop the technical aspects of your [!INCLUDE[d365fin](includes/d365fin_md.md)] app, get the [Develop the technical aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) document from the Download Center.</span></span>

+ <span data-ttu-id="c0207-122">Utveckla marknadsföringsaspekter av din app</span><span class="sxs-lookup"><span data-stu-id="c0207-122">Develop the marketing aspects of your app</span></span>  
<span data-ttu-id="c0207-123">Att bara ange appens egenskaper och funktioner kommer inte att konvertera potentiella kunder till köpare.</span><span class="sxs-lookup"><span data-stu-id="c0207-123">Simply listing your app's features and functionality will not convert prospects to buyers.</span></span> <span data-ttu-id="c0207-124">Mer information om hur du bäst marknadsför din app i AppSource marketplace finns i dokumentet [utveckla marknadsföringsaspekter av din app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) från Download Center.</span><span class="sxs-lookup"><span data-stu-id="c0207-124">For more information about how to best market your app in the AppSource marketplace, get the [Develop the marketing aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) from the Download Center.</span></span>

+ <span data-ttu-id="c0207-125">Publicera din app</span><span class="sxs-lookup"><span data-stu-id="c0207-125">Publish your app</span></span>  
<span data-ttu-id="c0207-126">Innan vi publicerar samarbetar vi med dig och ser till att din app sticker ut på Microsoft AppSource och din egen landningssida.</span><span class="sxs-lookup"><span data-stu-id="c0207-126">Before we publish, we will collaborate with you to ensure that your app stands out on Microsoft AppSource and on your own landing page!</span></span> <span data-ttu-id="c0207-127">Vi måste validera din app för att se till att den marknadsförs är säker och uppdaterad.</span><span class="sxs-lookup"><span data-stu-id="c0207-127">We need to validate your app to ensure it is marketed well, trustworthy, and up to date.</span></span>
<span data-ttu-id="c0207-128">Mer information om valideringen och hur du publicerar din app finns i dokumentet [Publicera din app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) från Download Center.</span><span class="sxs-lookup"><span data-stu-id="c0207-128">For more information about the validation process and how to publish your app, get the [Publish your app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) document from the Download Center.</span></span>

## <a name="learn-more-about-extensions-v20"></a><span data-ttu-id="c0207-129">Få mer information om tillägg v2.0</span><span class="sxs-lookup"><span data-stu-id="c0207-129">Learn more about extensions v2.0</span></span>
<span data-ttu-id="c0207-130">De nya utvecklingsverktygen, som gör det möjligt för dig att skapa tillägg v2.0, granskas för närvarande och aktiveras snart i Business Central-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c0207-130">The new development tools, which enable to you to build extensions v2.0, are currently in preview and will be enabled in the Business Central  service soon.</span></span> <span data-ttu-id="c0207-131">Om du redan vill bekanta dig med de nya verktygen och lära dig mer om tillägg 2.0 kan du ta en titt på [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).</span><span class="sxs-lookup"><span data-stu-id="c0207-131">If you already want to familiarize yourself with the new tools or learn more about extensions 2.0, have a look at [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).</span></span>  

## <a name="need-help"></a><span data-ttu-id="c0207-132">Behöver du hjälp?</span><span class="sxs-lookup"><span data-stu-id="c0207-132">Need help?</span></span>
<span data-ttu-id="c0207-133">Om du vill ha hjälp kan du kontakta du en app-expert från följande lista:</span><span class="sxs-lookup"><span data-stu-id="c0207-133">If you would like some coaching, you can contact an app subject matter expert from the following list:</span></span>

* <span data-ttu-id="c0207-134">Cloud Ready-programvaran, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span><span class="sxs-lookup"><span data-stu-id="c0207-134">Cloud Ready Software, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span></span>  
* <span data-ttu-id="c0207-135">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span><span class="sxs-lookup"><span data-stu-id="c0207-135">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span></span>

<span data-ttu-id="c0207-136">Partner i den här listan:</span><span class="sxs-lookup"><span data-stu-id="c0207-136">Partners in this list:</span></span>

* <span data-ttu-id="c0207-137">Visas i alfabetisk ordning</span><span class="sxs-lookup"><span data-stu-id="c0207-137">Are listed alphabetically</span></span>  
* <span data-ttu-id="c0207-138">Hjälper eller har gett stöd till minst tre partner med att hämta appar till Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="c0207-138">Are assisting or have assisted a minimum of three partners with bringing apps into Microsoft AppSource</span></span>  
* <span data-ttu-id="c0207-139">Har förpackningstjänst (och finns i listan på webbplatsen) om appens riktlinjer</span><span class="sxs-lookup"><span data-stu-id="c0207-139">Have a packaged service available (and listed on their website) about the app guidance that they provide</span></span>  

<span data-ttu-id="c0207-140">Om du anser att du bör finnas med på listan som enn app-servicepartner kan du kontakta [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c0207-140">If you believe you should be listed as an app service partner, don't hesitate to reach out to [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="questions"></a><span data-ttu-id="c0207-141">Frågor?</span><span class="sxs-lookup"><span data-stu-id="c0207-141">Questions?</span></span>
<span data-ttu-id="c0207-142">Dessa [vanliga frågor](https://go.microsoft.com/fwlink/?linkid=841520) svarar på de vanligaste frågorna som du kanske har om appar för [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c0207-142">This [FAQ](https://go.microsoft.com/fwlink/?linkid=841520) responds to the most common questions you might have about apps for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="c0207-143">Om du har fler frågor får du gärna kontakta en lokal Microsoft-representant eller e-posta [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c0207-143">If you have further questions, don't hesitate to contact your local Microsoft representative or email [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="further-resources"></a><span data-ttu-id="c0207-144">Övriga resurser</span><span class="sxs-lookup"><span data-stu-id="c0207-144">Further Resources</span></span>
<span data-ttu-id="c0207-145">Du hittar ytterligare resurser för utveckling av appar i vår [DLP-ämnessida](https://mbspartner.microsoft.com/BFI/Topic/76) DLP-ämnessida.</span><span class="sxs-lookup"><span data-stu-id="c0207-145">Please find further resources for app development on our [DLP topic page](https://mbspartner.microsoft.com/BFI/Topic/76) DLP topic page.</span></span> <span data-ttu-id="c0207-146">Det finns några markerade kommentarer nedan:</span><span class="sxs-lookup"><span data-stu-id="c0207-146">Some selected ones are available below:</span></span>
-   [<span data-ttu-id="c0207-147">Användarregistrering och efterföljande fakturering </span><span class="sxs-lookup"><span data-stu-id="c0207-147">User Registration and Subsequent Billing </span></span>](http://download.microsoft.com/download/3/2/0/320D0286-8810-4A8F-B7DD-523ED87D441B/FAQ on apps for Dynamics 365 for Financials.pdf)



## <a name="see-also"></a><span data-ttu-id="c0207-148">Se även</span><span class="sxs-lookup"><span data-stu-id="c0207-148">See Also</span></span>
[<span data-ttu-id="c0207-149">Komma igång</span><span class="sxs-lookup"><span data-stu-id="c0207-149">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="c0207-150">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="c0207-150">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[https://appsource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365-for-financials&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
