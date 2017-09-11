---
title: Koppla Data med | Microsoft Docs
description: "Du kan göra dina Financials-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa ett automatiskt arbetsflöde."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 277dda7c954380138af1ecabc02d77121f35aac7
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="784fc-103">Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett automatiskt arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="784fc-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="784fc-104">Du kan använda din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av ett arbetsflöde i Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="784fc-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="784fc-105">Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Flow.</span><span class="sxs-lookup"><span data-stu-id="784fc-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="784fc-106">Att lägga till [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakälla i Flow.</span><span class="sxs-lookup"><span data-stu-id="784fc-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="784fc-107">I webbläsaren, går du till [flow.microsoft.com](https://flow.microsoft.com/en-us/), och loggar in.</span><span class="sxs-lookup"><span data-stu-id="784fc-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="784fc-108">Välj **Mina flöden** från menyn längst upp på sidan.</span><span class="sxs-lookup"><span data-stu-id="784fc-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="784fc-109">I fönstret **Mina flöden** kan välja alternativet **Skapa från tom**.</span><span class="sxs-lookup"><span data-stu-id="784fc-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="784fc-110">I listan över tillgängliga utlösare markerar du ett av två [!INCLUDE[d365fin](includes/d365fin_md.md)]-utlösare som är tillgängliga: *När en post skapas*, eller *När en post ändras *.</span><span class="sxs-lookup"><span data-stu-id="784fc-110">From the list of available triggers, select one of the two [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available: *When a record is created*, or *When a record is modified*.</span></span>
5. <span data-ttu-id="784fc-111">Flow visar en anslutningssida som uppmanar dig till att ge den information som behövs för att ansluta till din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data.</span><span class="sxs-lookup"><span data-stu-id="784fc-111">Flow will display a connection page that prompts you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="784fc-112">Du måste ange ett namn för anslutningen, OData-URL, användarnamn, lösenord och företagsnamn för att ansluta.</span><span class="sxs-lookup"><span data-stu-id="784fc-112">To connect, you must specify a name for the connection, an OData URL, username, password, and company name.</span></span>

   <span data-ttu-id="784fc-113">För den *OData-URL*, kan du kopiera OData V4-URL för någon av webbtjänsterna som finns på sidan **webbtjänster** i [!INCLUDE[d365fin](includes/d365fin_md.md)], som t.ex. `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.</span><span class="sxs-lookup"><span data-stu-id="784fc-113">For the *OData URL*, you can copy the OData V4 URL of any of the web services that are listed in the **Web Services** page in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.</span></span>  

   <span data-ttu-id="784fc-114">För *företagsnamn*, använder du namnet som visas i fältet **namn** i fönstret **företagsinformation** i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="784fc-114">For the *Company Name*, use the name that is shown in the **Name** field in the **Company Information** window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="784fc-115">Om din [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller flera företag, väljer du relevant företagsnamn i listan i fönstret **företag**.</span><span class="sxs-lookup"><span data-stu-id="784fc-115">If your [!INCLUDE[d365fin](includes/d365fin_md.md)] contains multiple companies, choose the relevant company name from the list in the **Companies** window.</span></span> <span data-ttu-id="784fc-116">I båda fallen kontrollerar du att namnet som du anger i PowerApps-guiden motsvarar exakt den text som visas i [!INCLUDE[d365fin](includes/d365fin_md.md)], som t.ex. `My Company`.</span><span class="sxs-lookup"><span data-stu-id="784fc-116">In both cases, make sure that the name that you specify in the PowerApps wizard matches exactly the text shown in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as `My Company`.</span></span>

   <span data-ttu-id="784fc-117">För användarnamn och lösenord, använder du de namn- och webbtjänstnycklar som har angetts för kontot i fönstret **användare** i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="784fc-117">For the username and password, use the name and web service access key that are specified for your account in the **Users** window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="784fc-118">Ditt användarnamn är till exempel *ADMIN* och webbtjänståtkomstnyckeln som fungerar som ditt lösenord och *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.</span><span class="sxs-lookup"><span data-stu-id="784fc-118">For example, your username is *ADMIN*, and the web service access key that serves as your password is *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.</span></span> <span data-ttu-id="784fc-119">Mer information finns i [Så här hanterar du användare och behörigheter](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="784fc-119">For more information, see [How to: Manage Users and Permissions](ui-how-users-permissions.md).</span></span>
6. <span data-ttu-id="784fc-120">Välj knappen **skapa** längst ned på sidan om du vill fortsätta.</span><span class="sxs-lookup"><span data-stu-id="784fc-120">Choose the **Create** button at the bottom of the page to continue.</span></span>

   <span data-ttu-id="784fc-121">Flow visar en lista över tabeller som finns på [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="784fc-121">Flow will show a list of tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="784fc-122">Dessa listor eller slutpunkter motsvarar de webbtjänster som du har publicerat från ditt [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="784fc-122">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="784fc-123">Du kan också skapa en ny webbtjänst-URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] med hjälp av åtgärden **skapa datauppsättning** på sidan **webbtjänster** med hjälp av den assisterade inställningsguiden **Ställ in rapportering**  eller genom att välja åtgärden **redigera i Excel** i någon lista.</span><span class="sxs-lookup"><span data-stu-id="784fc-123">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>
7. <span data-ttu-id="784fc-124">Välj de data som du vill ska användas för i Flow.</span><span class="sxs-lookup"><span data-stu-id="784fc-124">Choose the data that you want to use for in Flow.</span></span>

<span data-ttu-id="784fc-125">Nu har du lyckats ansluta till dina Dynamics 365-data och är redo att börja skapa ditt flöde.</span><span class="sxs-lookup"><span data-stu-id="784fc-125">At this point, you have successfully connected to your Dynamics 365 data and are ready to begin building your flow.</span></span> <span data-ttu-id="784fc-126">Mer information finns i [Flow-dokumentation](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="784fc-126">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

## <a name="see-also"></a><span data-ttu-id="784fc-127">Se även</span><span class="sxs-lookup"><span data-stu-id="784fc-127">See Also</span></span>
<span data-ttu-id="784fc-128">[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="784fc-128">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="784fc-129">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="784fc-129">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="784fc-130">[Så här hanterar du användare och behörigheter](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="784fc-130">[How to: Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="784fc-131">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="784fc-131">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="784fc-132">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="784fc-132">Finance</span></span>](finance.md)  

