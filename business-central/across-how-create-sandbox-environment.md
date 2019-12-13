---
title: Skapa miljö för begränsat läge | Microsoft Docs
description: Skapa en miljö där du kan utforska, utbilda demo, utveckla och prova.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 12/06/2019
ms.author: solsen
ms.openlocfilehash: 0f8f0f85df89c1d71fc3e114ebd902f2aa85f802
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896115"
---
# <a name="creating-a-sandbox-environment-in-include-prodshortincludesprodshortmd"></a><span data-ttu-id="3f700-103">Skapa en miljö för begränsat läge i [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="3f700-103">Creating a Sandbox Environment in [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="3f700-104">Med [!INCLUDE [prodshort](includes/prodshort.md)] kan du enkelt skapa en säker miljö där du kan testa, träna eller felsöka utan att störa företagets arbetsprocesser eller företagsdata.</span><span class="sxs-lookup"><span data-stu-id="3f700-104">With [!INCLUDE [prodshort](includes/prodshort.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="3f700-105">En sådan icke-produktionsmiljö kallas för *begränsat läge*.</span><span class="sxs-lookup"><span data-stu-id="3f700-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="3f700-106">Isolerad från produktionen är begränsat läge stället för att säkert utforska, lära sig, demonstrera, utveckla och testa tjänsten utan att risk för att data och inställningar påverkas i din produktionsmiljö.</span><span class="sxs-lookup"><span data-stu-id="3f700-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="3f700-107">Administratören kan skapa miljö för begränsat läge i [administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), men om du snabbt vill testa något kan du skapa en miljö för begränsat läge från insidan [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="3f700-107">Your administrator can create sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

> [!NOTE]
> <span data-ttu-id="3f700-108">Tekniskt sett skiljer sig miljöer i begränsat läge mycket från produktionsmiljöer, även om administratören skapar ett begränsat läge som omfattar produktionsdata.</span><span class="sxs-lookup"><span data-stu-id="3f700-108">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="3f700-109">Du kan inte använda begränsat läge för benchmarking och du kan exempelvis inte begära en databasexport.</span><span class="sxs-lookup"><span data-stu-id="3f700-109">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="3f700-110">Om du vill skapa ett begränsat läge för benchmark-hantering kan administratören skapa en dedikerad produktionsmiljö i administrationscentret.</span><span class="sxs-lookup"><span data-stu-id="3f700-110">If you want to create a sandbox for benchmarking, your administrator can create a dedicated production environment in the administration center.</span></span> <span data-ttu-id="3f700-111">Mer information finns i [Typer av miljöer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span><span class="sxs-lookup"><span data-stu-id="3f700-111">For more information, see [Types of environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-include-prodshortincludesprodshortmd"></a><span data-ttu-id="3f700-112">Skapa miljö för begränsat läge i din [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="3f700-112">To create a sandbox environment in your [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

1. <span data-ttu-id="3f700-113">Logga in i din instans för produktionsmiljö i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3f700-113">Sign in to your production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

2. <span data-ttu-id="3f700-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **miljö för begränsat läge** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3f700-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="3f700-115">Klicka på knappen **Skapa**.</span><span class="sxs-lookup"><span data-stu-id="3f700-115">Choose the **Create** button.</span></span>  

    <span data-ttu-id="3f700-116">En annan flik med [!INCLUDE[d365fin](includes/d365fin_md.md)] öppnas där du kan slutföra inställningarna i miljön för begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="3f700-116">Another tab with [!INCLUDE[d365fin](includes/d365fin_md.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="3f700-117">Om du har ett popup-fönster aktiverat i din webbläsare, kan du ändra koden så att URL-adresser tillåts från adressen \*.businesscentral.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="3f700-117">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="3f700-118">När begränsat läge är klart, omdirigeras till välkomstguiden för begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="3f700-118">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="3f700-119">Du kan välja **lär dig mer** om du vill läsa om utvecklarscenarier som du kan prova i en miljö för begränsat läge eller välja knappen **Stäng** för att fortsätta till rollcenter för din [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljö för begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="3f700-119">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>

<span data-ttu-id="3f700-120">Högst upp i Rollcentret visas ett meddelande att informera dig om att det är begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="3f700-120">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="3f700-121">Du kan också se miljötypen i namnlisten på klienten.</span><span class="sxs-lookup"><span data-stu-id="3f700-121">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="3f700-122">En miljö för begränsat läge som skapas på det här sättet innehåller endast standarddemonstrationsdata för CRONUS-företaget.</span><span class="sxs-lookup"><span data-stu-id="3f700-122">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="3f700-123">Inga data kopieras till eller på annat sätt överförs från produktionsmiljön.</span><span class="sxs-lookup"><span data-stu-id="3f700-123">No data is copied or otherwise transferred from the production environment.</span></span><br /><br />
> <span data-ttu-id="3f700-124">Du kan också skapa en miljö för begränsat läge som innehåller produktionsdata.</span><span class="sxs-lookup"><span data-stu-id="3f700-124">You can also create a sandbox environment containing the production data.</span></span> <span data-ttu-id="3f700-125">Du måste göra detta i administrationscentret.</span><span class="sxs-lookup"><span data-stu-id="3f700-125">You must do this through the administration center.</span></span> <span data-ttu-id="3f700-126">Mer information finns i [Hantera miljöer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) i hjälpen för utvecklare och IT-proffs.</span><span class="sxs-lookup"><span data-stu-id="3f700-126">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the Developer and IT-Pro help.</span></span>

<span data-ttu-id="3f700-127">När som helst kan du återgå till sidan **begränsat läge** och återställa begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="3f700-127">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>

> [!NOTE]  
> <span data-ttu-id="3f700-128">Återställa begränsat läge tar bort den helt och skapar den sedan igen med standarddemonstrationsdata.</span><span class="sxs-lookup"><span data-stu-id="3f700-128">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="3f700-129">En administratör kan begränsa eller även spärra åtkomsten för vissa användare till begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="3f700-129">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="3f700-130">Detta kan göras med hjälp av produktens standardsäkerhetsfunktioner som användarkort, användargrupper och behörighetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="3f700-130">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="3f700-131">Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="3f700-131">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="3f700-132">Avancerade funktioner i begränsat läge</span><span class="sxs-lookup"><span data-stu-id="3f700-132">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="3f700-133">Miljön i begränsat läge är inte minst användbar eftersom den innehåller ett par praktiska funktioner.</span><span class="sxs-lookup"><span data-stu-id="3f700-133">The sandbox environment is not least useful because it includes a couple of handy features.</span></span>

### <a name="designer"></a><span data-ttu-id="3f700-134">Designer</span><span class="sxs-lookup"><span data-stu-id="3f700-134">Designer</span></span>

<span data-ttu-id="3f700-135">I en miljö för begränsat läge kan du se att **designer** är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="3f700-135">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="3f700-136">Du kan aktivera designer genom att välja ikonen ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en sida eller genom att välja menyalternativet **design** på inställningsmenyn ![inställningar](media/ui-experience/settings_icon_small.png).</span><span class="sxs-lookup"><span data-stu-id="3f700-136">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a><span data-ttu-id="3f700-137">Aktivera avancerade användare</span><span class="sxs-lookup"><span data-stu-id="3f700-137">To enable the advanced user experience</span></span>
<span data-ttu-id="3f700-138">Det går att aktivera och prova avancerade (alla) funktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett begränsat läge för innehavare genom att ange fältet **upplevelse** på sidan **företagsinformation**.</span><span class="sxs-lookup"><span data-stu-id="3f700-138">It is possible to enable and try the advanced (full) functionality of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="3f700-139">När du har aktiverat den avancerade funktionen i en begränsad innehavare kan få du tillgång till alla vanliga profiler (roller) och rollcenter.</span><span class="sxs-lookup"><span data-stu-id="3f700-139">After you have enabled the advanced functionality in a sandbox tenant, you get access to all the standard profiles (roles) and Role Centers.</span></span> <span data-ttu-id="3f700-140">Du kan också skapa ett utvärderingsföretag som helt har ställts in, inklusive demonstrationsdata och tillgång till avancerade delar av produkten.</span><span class="sxs-lookup"><span data-stu-id="3f700-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span>

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a><span data-ttu-id="3f700-141">Se även</span><span class="sxs-lookup"><span data-stu-id="3f700-141">See Also</span></span>

<span data-ttu-id="3f700-142">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3f700-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="3f700-143">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Utvärderingsversioner och prenumerationer](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="3f700-143">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="3f700-144">Hantera miljöer i Business Central administrationscenter</span><span class="sxs-lookup"><span data-stu-id="3f700-144">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
