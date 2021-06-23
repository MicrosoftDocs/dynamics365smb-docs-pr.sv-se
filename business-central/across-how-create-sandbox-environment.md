---
title: Skapa miljö för begränsat läge
description: Skapa en miljö där du kan utforska, utbilda, demonstrera, utveckla och prova inifrån Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: a76ae33815b8e9368f45b72fd8703bfc47cbd079
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215634"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a><span data-ttu-id="8c83c-103">Skapa en miljö för begränsat läge i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="8c83c-103">Creating a Sandbox Environment in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

<span data-ttu-id="8c83c-104">Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du enkelt skapa en säker miljö där du kan testa, träna eller felsöka utan att störa företagets arbetsprocesser eller företagsdata.</span><span class="sxs-lookup"><span data-stu-id="8c83c-104">With [!INCLUDE[prod_short](includes/prod_short.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="8c83c-105">En sådan icke-produktionsmiljö kallas för *begränsat läge*.</span><span class="sxs-lookup"><span data-stu-id="8c83c-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="8c83c-106">Isolerad från produktionen är begränsat läge stället för att säkert utforska, lära sig, demonstrera, utveckla och testa tjänsten utan att risk för att data och inställningar påverkas i din produktionsmiljö.</span><span class="sxs-lookup"><span data-stu-id="8c83c-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="8c83c-107">Administratören hanterar miljö för begränsat läge i [administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), men om du snabbt vill testa något kan du skapa en miljö för begränsat läge från insidan [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8c83c-107">Your administrator manages sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="8c83c-108">När du är klar kan du ta bort det begränsade läget med hjälp av administrationscentret.</span><span class="sxs-lookup"><span data-stu-id="8c83c-108">Once you're done, you can remove the sandbox, using the administration center.</span></span>  

> [!NOTE]
> <span data-ttu-id="8c83c-109">Tekniskt sett skiljer sig miljöer i begränsat läge mycket från produktionsmiljöer, även om administratören skapar ett begränsat läge som omfattar produktionsdata.</span><span class="sxs-lookup"><span data-stu-id="8c83c-109">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="8c83c-110">Du kan inte använda begränsat läge för benchmarking och du kan exempelvis inte begära en databasexport.</span><span class="sxs-lookup"><span data-stu-id="8c83c-110">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="8c83c-111">Om du vill skapa ett begränsat läge för benchmark-hantering kan administratören skapa en dedikerad miljö i administrationscentret.</span><span class="sxs-lookup"><span data-stu-id="8c83c-111">If you want to create a sandbox for benchmarking, your administrator can create a dedicated environment in the administration center.</span></span> <span data-ttu-id="8c83c-112">Mer information finns i [Produktionsmiljöer and miljöer för begränsat läge](/dynamics365/business-central/dev-itpro/administration/environment-types).</span><span class="sxs-lookup"><span data-stu-id="8c83c-112">For more information, see [Production and Sandbox Environments](/dynamics365/business-central/dev-itpro/administration/environment-types).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a><span data-ttu-id="8c83c-113">Skapa miljö för begränsat läge i din [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="8c83c-113">To create a sandbox environment in your [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

1. <span data-ttu-id="8c83c-114">Logga in i din instans för produktionsmiljö i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8c83c-114">Sign in to your production instance of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

2. <span data-ttu-id="8c83c-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **miljö för begränsat läge** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8c83c-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="8c83c-116">Klicka på knappen **Skapa**.</span><span class="sxs-lookup"><span data-stu-id="8c83c-116">Choose the **Create** button.</span></span>  

    <span data-ttu-id="8c83c-117">En annan flik med [!INCLUDE[prod_short](includes/prod_short.md)] öppnas där du kan slutföra inställningarna i miljön för begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="8c83c-117">Another tab with [!INCLUDE[prod_short](includes/prod_short.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="8c83c-118">Om du har ett popup-fönster aktiverat i din webbläsare, kan du ändra koden så att URL-adresser tillåts från adressen \*.businesscentral.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="8c83c-118">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="8c83c-119">När begränsat läge är klart, omdirigeras till välkomstguiden för begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="8c83c-119">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="8c83c-120">Du kan välja **lär dig mer** om du vill läsa om utvecklarscenarier som du kan prova i en miljö för begränsat läge eller välja knappen **Stäng** för att fortsätta till rollcenter för din [!INCLUDE[prod_short](includes/prod_short.md)]-miljö för begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="8c83c-120">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[prod_short](includes/prod_short.md)] sandbox instance.</span></span>

<span data-ttu-id="8c83c-121">Högst upp i Rollcentret visas ett meddelande att informera dig om att det är begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="8c83c-121">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="8c83c-122">Du kan också se miljötypen i namnlisten på klienten.</span><span class="sxs-lookup"><span data-stu-id="8c83c-122">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="8c83c-123">En miljö för begränsat läge som skapas på det här sättet innehåller endast standarddemonstrationsdata för CRONUS-företaget.</span><span class="sxs-lookup"><span data-stu-id="8c83c-123">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="8c83c-124">Inga data kopieras till eller på annat sätt överförs från produktionsmiljön.</span><span class="sxs-lookup"><span data-stu-id="8c83c-124">No data is copied or otherwise transferred from the production environment.</span></span>
>
> <span data-ttu-id="8c83c-125">Du kan också skapa en begränsad miljö baserad på produktionsdata.</span><span class="sxs-lookup"><span data-stu-id="8c83c-125">Alternatively, create a sandbox environment based on production data.</span></span> <span data-ttu-id="8c83c-126">Du måste göra detta i administrationscentret.</span><span class="sxs-lookup"><span data-stu-id="8c83c-126">You must do this through the administration center.</span></span> <span data-ttu-id="8c83c-127">Mer information finns i [Hantera miljöer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) i utvecklar- och administrationsinnehållet.</span><span class="sxs-lookup"><span data-stu-id="8c83c-127">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the developer and administration content.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="8c83c-128">En administratör kan begränsa eller även spärra åtkomsten för vissa användare till begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="8c83c-128">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="8c83c-129">Detta kan göras med hjälp av produktens standardsäkerhetsfunktioner som användarkort, användargrupper och behörighetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="8c83c-129">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="8c83c-130">Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="8c83c-130">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="8c83c-131">Avancerade funktioner i begränsat läge</span><span class="sxs-lookup"><span data-stu-id="8c83c-131">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="8c83c-132">Miljön i begränsat läge är inte minst användbar eftersom den innehåller ett par praktiska funktioner:</span><span class="sxs-lookup"><span data-stu-id="8c83c-132">The sandbox environment is not least useful because it includes a couple of handy features:</span></span>

* [<span data-ttu-id="8c83c-133">Avancerad användarupplevelse</span><span class="sxs-lookup"><span data-stu-id="8c83c-133">Advanced user experience</span></span>](#advanced-user-experience)  
* [<span data-ttu-id="8c83c-134">Fullständiga exempeldata</span><span class="sxs-lookup"><span data-stu-id="8c83c-134">Complete sample data</span></span>](#complete-sample-data)  
* [<span data-ttu-id="8c83c-135">Designer</span><span class="sxs-lookup"><span data-stu-id="8c83c-135">Designer</span></span>](#designer)  

### <a name="advanced-user-experience"></a><span data-ttu-id="8c83c-136">Avancerad användarupplevelse</span><span class="sxs-lookup"><span data-stu-id="8c83c-136">Advanced user experience</span></span>

<span data-ttu-id="8c83c-137">Det går att aktivera och prova alla funktioner i standardversionen av [!INCLUDE[prod_short](includes/prod_short.md)]  i ett begränsat läge för klientorganisation genom att ställa in fältet **Erfarenhet** på sidan **Företagsinformation** till *Premium*.</span><span class="sxs-lookup"><span data-stu-id="8c83c-137">It is possible to enable and try the full functionality of the standard version of [!INCLUDE[prod_short](includes/prod_short.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page to *Premium*.</span></span> Leta upp sidan **företagsinformation** i menyn :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="ikonen Inställningar"::: menu.  

<span data-ttu-id="8c83c-139">När du har aktiverat användarupplevelsen *Premium* får du tillgång till alla standardprofiler (roller) och Rollcenter i standardversionen.</span><span class="sxs-lookup"><span data-stu-id="8c83c-139">After you have enabled the *Premium* user experience, you get access to all the standard profiles (roles) and Role Centers in the standard version.</span></span> <span data-ttu-id="8c83c-140">Du kan också skapa ett utvärderingsföretag som helt har ställts in, inklusive demonstrationsdata och tillgång till avancerade delar av produkten.</span><span class="sxs-lookup"><span data-stu-id="8c83c-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span> <span data-ttu-id="8c83c-141">Alternativt kan du kontakta en återförsäljare för en demonstration av funktionerna.</span><span class="sxs-lookup"><span data-stu-id="8c83c-141">Alternatively, contact a reselling partner for a demonstration of the capabilities.</span></span> <span data-ttu-id="8c83c-142">Mer information finns i [Hur hittar jag efter en återförsäljningspartner?](/dynamics365/business-central/across-faq.yml#findpartner).</span><span class="sxs-lookup"><span data-stu-id="8c83c-142">For more information, see [How do I find a reselling partner?](/dynamics365/business-central/across-faq.yml#findpartner).</span></span>  

### <a name="complete-sample-data"></a><span data-ttu-id="8c83c-143">Fullständiga exempeldata</span><span class="sxs-lookup"><span data-stu-id="8c83c-143">Complete sample data</span></span>

<span data-ttu-id="8c83c-144">Om du behöver ytterligare exempeldata kan du prata med återförsäljningspartnern.</span><span class="sxs-lookup"><span data-stu-id="8c83c-144">For situations where you need additional sample data, please talk to your reselling partner.</span></span>
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a><span data-ttu-id="8c83c-145">Så här skapar du ett företag med fullständiga exempeldata i ett begränsat läge</span><span class="sxs-lookup"><span data-stu-id="8c83c-145">To create a company with complete sample data in a sandbox</span></span>

1. <span data-ttu-id="8c83c-146">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Företag** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="8c83c-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8c83c-147">Välj åtgärden **Ny** och välj sedan **Skapa nytt företag**.</span><span class="sxs-lookup"><span data-stu-id="8c83c-147">Choose the **New** action, and then choose **Create New Company**.</span></span>  
3. <span data-ttu-id="8c83c-148">På sidan **Assisterad konfiguration för att skapa ett företag** välj **Nästa**.</span><span class="sxs-lookup"><span data-stu-id="8c83c-148">In the **Assisted Setup for Creating a Company** page, choose **Next**.</span></span>  
4. <span data-ttu-id="8c83c-149">Ange ett namn på det nya företaget och sedan i fältet **Välj data och konfiguration för att komma igång** välj **Avancerad utvärdering – fullständig exempeldata**.</span><span class="sxs-lookup"><span data-stu-id="8c83c-149">Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.</span></span>  
5. <span data-ttu-id="8c83c-150">Följ resten av instruktionerna i assisterad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8c83c-150">Complete the rest of the assisted setup guide.</span></span>  

<span data-ttu-id="8c83c-151">När assisterad konfiguration är klar kan du börja utforska det nya företaget med de fullständiga exempeldata.</span><span class="sxs-lookup"><span data-stu-id="8c83c-151">When the assisted setup guide completes, you can start exploring the new company with the complete sample data.</span></span> <span data-ttu-id="8c83c-152">Mer information finns i [Skapa nya företag i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="8c83c-152">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>  

### <a name="designer"></a><span data-ttu-id="8c83c-153">Designer</span><span class="sxs-lookup"><span data-stu-id="8c83c-153">Designer</span></span>

<span data-ttu-id="8c83c-154">I en miljö för begränsat läge kan du se att **designer** är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="8c83c-154">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="8c83c-155">Du kan aktivera designer genom att välja ikonen ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en sida eller genom att välja menyalternativet **design** på inställningsmenyn ![inställningar](media/ui-experience/settings_icon_small.png).</span><span class="sxs-lookup"><span data-stu-id="8c83c-155">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>  

<span data-ttu-id="8c83c-156">Mer information finns i [Använda designer](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) i utvecklar- och administrationsinnehållet (enbart på engelska).</span><span class="sxs-lookup"><span data-stu-id="8c83c-156">For more information, see [Using Designer](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) in the developer and admin content (in English only).</span></span>  

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a><span data-ttu-id="8c83c-157">Se även</span><span class="sxs-lookup"><span data-stu-id="8c83c-157">See Also</span></span>

<span data-ttu-id="8c83c-158">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8c83c-158">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="8c83c-159">[[!INCLUDE[prod_long](includes/prod_long.md)] Utvärderingsversioner och prenumerationer](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="8c83c-159">[[!INCLUDE[prod_long](includes/prod_long.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="8c83c-160">Hantera miljöer i Business Central administrationscenter</span><span class="sxs-lookup"><span data-stu-id="8c83c-160">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
