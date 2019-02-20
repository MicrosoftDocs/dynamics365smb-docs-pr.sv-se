---
title: "Skapa miljö för begränsat läge | Microsoft Docs"
description: "Skapa en miljö där du kan utforska, utbilda demo, utveckla och prova."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 81eb819295a8d2b03f9c53ecd98053d0b1041faa
ms.contentlocale: sv-se
ms.lasthandoff: 12/11/2018

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a><span data-ttu-id="89282-103">Skapa en miljö för begränsat läge</span><span class="sxs-lookup"><span data-stu-id="89282-103">Creating a Sandbox Environment</span></span>
<span data-ttu-id="89282-104">Begränsat läge (förhandsgranskning) är en instans av [!INCLUDE[d365fin](includes/d365fin_md.md)] utanför produktionsmiljön.</span><span class="sxs-lookup"><span data-stu-id="89282-104">A sandbox environment (Preview) is a non-production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="89282-105">Isolerad från produktionen är begränsat läge stället för att säkert utforska, lära sig, demonstrera, utveckla och testa tjänsten utan att risk för att data och inställningar påverkas i din produktionsmiljö.</span><span class="sxs-lookup"><span data-stu-id="89282-105">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>

## <a name="to-create-a-sandbox-environment"></a><span data-ttu-id="89282-106">Skapa miljö för begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="89282-106">To create a sandbox environment</span></span>
<span data-ttu-id="89282-107">Du måste ha en prenumeration på [!INCLUDE[d365fin](includes/d365fin_md.md)] för att skapa begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="89282-107">You must have a subscription to [!INCLUDE[d365fin](includes/d365fin_md.md)] to be able to create a sandbox environment.</span></span> <span data-ttu-id="89282-108">Det kan bara finnas ett begränsat läge per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="89282-108">There can only be one sandbox environment per subscription.</span></span>

1. <span data-ttu-id="89282-109">Logga in i din instans för produktionsmiljö i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="89282-109">Sign in to your production instance of the [!INCLUDE[d365fin](includes/d365fin_md.md)] service.</span></span>
2. <span data-ttu-id="89282-110">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Miljö för begränsat läge** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="89282-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
<span data-ttu-id="89282-111">![Konfigurera miljö för begränsat läge.](./media/across-sandbox/sandbox-environment-setup.png)</span><span class="sxs-lookup"><span data-stu-id="89282-111">![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png)</span></span>
3. <span data-ttu-id="89282-112">Välj **skapa**.</span><span class="sxs-lookup"><span data-stu-id="89282-112">Select **Create**.</span></span>  
  <span data-ttu-id="89282-113">En annan flik i webbläsaren öppnas för att slutföra inställningarna för begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="89282-113">Another tab in your browser will open for finishing the setup of your sandbox environment.</span></span>
> [!NOTE]  
>  <span data-ttu-id="89282-114">Om du har ett popup-fönster aktiverat i din webbläsare, kan du ändra koden så att URL-adresser tillåts från adressen \*.businesscentral.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="89282-114">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>   

4. <span data-ttu-id="89282-115">När begränsat läge är klart, omdirigeras till välkomstguiden för begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="89282-115">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<span data-ttu-id="89282-116">![välkomstguiden för begränsat läge](./media/across-sandbox/sandbox-wizard.png)</span><span class="sxs-lookup"><span data-stu-id="89282-116">![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png)</span></span>

5. <span data-ttu-id="89282-117">Välj **Mer information** om du vill veta om scenarier som du kan pröva i begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="89282-117">Choose **Learn more** to read about scenarios that you can try in a sandbox environment.</span></span> <span data-ttu-id="89282-118">Klicka på **Stäng** för att fortsätta till rollcenter din [!INCLUDE[d365fin](includes/d365fin_md.md)]-instans för begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="89282-118">Or, choose **Close** to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>
6. <span data-ttu-id="89282-119">Högst upp i Rollcentret visas ett meddelande att informera dig om att det är begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="89282-119">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="89282-120">Du kan också se miljötypen i namnlisten på klienten.</span><span class="sxs-lookup"><span data-stu-id="89282-120">You can also see the type of the environment in the title bar of the client.</span></span>
<span data-ttu-id="89282-121">![Rollcenteraviseringar för begränsat läge](./media/across-sandbox/sandbox-rolecenter-notification.png)</span><span class="sxs-lookup"><span data-stu-id="89282-121">![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png)</span></span>  
<span data-ttu-id="89282-122">I begränsat läge, har en helt ny innehavare skapats.</span><span class="sxs-lookup"><span data-stu-id="89282-122">In the sandbox environment, a brand-new tenant has been created.</span></span> <span data-ttu-id="89282-123">Den här innehavaren laddas med standarddemonstrationsdata för företaget CRONUS.</span><span class="sxs-lookup"><span data-stu-id="89282-123">This tenant is loaded with default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="89282-124">Inga data kopieras till eller på annat sätt överförs från produktionsmiljön när begränsat läge skapas.</span><span class="sxs-lookup"><span data-stu-id="89282-124">No data is copied or otherwise transferred from the production environment during the sandbox creation.</span></span>
7.  <span data-ttu-id="89282-125">När som helst kan du återgå till sidan **begränsat läge** och återställa begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="89282-125">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>
> [!NOTE]  
>  <span data-ttu-id="89282-126">Återställa begränsat läge tar bort den helt och skapar den sedan igen med standarddemonstrationsdata.</span><span class="sxs-lookup"><span data-stu-id="89282-126">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

8.  <span data-ttu-id="89282-127">Du kan använda Business Centrals programmarstartbild om du vill växla mellan miljö för produktion och begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="89282-127">To switch between your production and sandbox environments, you can use the Business Central app launcher.</span></span>
<span data-ttu-id="89282-128">![Begränsat läge Dynamics365 meny](./media/across-sandbox/sandbox-dynamics365-menu.png)</span><span class="sxs-lookup"><span data-stu-id="89282-128">![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png)</span></span>

9.  <span data-ttu-id="89282-129">Det är möjligt för en administratör eller en annan användare att begränsa eller även spärra åtkomsten för vissa användare till begränsat läge.</span><span class="sxs-lookup"><span data-stu-id="89282-129">It is possible for an administrator or another user to limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="89282-130">Detta kan göras med hjälp av produktens standardsäkerhetsfunktioner som användarkort, användargrupper och behörighetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="89282-130">This can be done by using the standard security features of the product, such as the User card, User Groups, and Permission Sets.</span></span>

![Behörighetsuppsättningar för begränsat läge](./media/across-sandbox/sandbox-permission-sets.png)

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="89282-132">Avancerade funktioner i begränsat läge</span><span class="sxs-lookup"><span data-stu-id="89282-132">Advanced functionality in the sandbox environment</span></span>
### <a name="the-in-client-designer"></a><span data-ttu-id="89282-133">Designern på klienten.</span><span class="sxs-lookup"><span data-stu-id="89282-133">The in-client designer</span></span>
<span data-ttu-id="89282-134">I begränsat läge finns i designern på klienten aktiverad, som du kan aktivera genom att markera ikonen design</span><span class="sxs-lookup"><span data-stu-id="89282-134">In a sandbox environment, you will find the in-client designer feature enabled, which you can activate by selecting the design icon</span></span> ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) <span data-ttu-id="89282-136">på en sida.</span><span class="sxs-lookup"><span data-stu-id="89282-136">on a page.</span></span>

![Designern på klienten.](./media/across-sandbox/sandbox-inclient-designer.png)

### <a name="enable-the-advanced-user-experience"></a><span data-ttu-id="89282-138">Aktivera avancerade användare</span><span class="sxs-lookup"><span data-stu-id="89282-138">Enable the advanced user experience</span></span>
<span data-ttu-id="89282-139">Det går att aktivera och prova avancerade (alla) funktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett begränsat läge för innehavare genom att ange fältet **upplevelse** på sidan **företagsinformation**.</span><span class="sxs-lookup"><span data-stu-id="89282-139">It is possible to enable and try the advanced (full) functionality of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

![Avancerad miljö för begränsat läge.](./media/across-sandbox/sandbox-advanced.png)

![Begränsat läge för produktion](./media/across-sandbox/sandbox-production.png)

<span data-ttu-id="89282-142">När du har aktiverat den avancerade funktionen i en begränsad innehavare kan få du tillgång till alla vanliga profiler och rollcenter.</span><span class="sxs-lookup"><span data-stu-id="89282-142">After you’ve enabled the advanced functionality in a sandbox tenant, you get access to all the standard Profiles and Role Centers.</span></span> <span data-ttu-id="89282-143">Du kan också skapa ett utvärderingsföretag som helt har ställts in, inklusive demonstrationsdata och tillgång till avancerade delar av produkten.</span><span class="sxs-lookup"><span data-stu-id="89282-143">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span>

![Begränsat nytt företag](./media/across-sandbox/sandbox-newcompany.png)


## <a name="see-also"></a><span data-ttu-id="89282-145">Se även</span><span class="sxs-lookup"><span data-stu-id="89282-145">See Also</span></span>
<span data-ttu-id="89282-146">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="89282-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

