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
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="4badf-103">Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett automatiskt arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="4badf-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="4badf-104">Du kan använda din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av ett arbetsflöde i Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="4badf-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="4badf-105">Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Flow.</span><span class="sxs-lookup"><span data-stu-id="4badf-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="4badf-106">Att lägga till [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakälla i Flow.</span><span class="sxs-lookup"><span data-stu-id="4badf-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="4badf-107">I webbläsaren, går du till [flow.microsoft.com](https://flow.microsoft.com/en-us/), och loggar in.</span><span class="sxs-lookup"><span data-stu-id="4badf-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="4badf-108">Välj **Mina flöden** från menyn längst upp på sidan.</span><span class="sxs-lookup"><span data-stu-id="4badf-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="4badf-109">I fönstret **Mina flöden** kan välja alternativet **Skapa från tom**.</span><span class="sxs-lookup"><span data-stu-id="4badf-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="4badf-110">I listan över tillgängliga utlösare, välj någon av de [!INCLUDE[d365fin](includes/d365fin_md.md)] utlösare som är tillgängliga:</span><span class="sxs-lookup"><span data-stu-id="4badf-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="4badf-111">*När en post skapas*,</span><span class="sxs-lookup"><span data-stu-id="4badf-111">*When a record is created*,</span></span>  
    <span data-ttu-id="4badf-112">*När en post tas bort*,</span><span class="sxs-lookup"><span data-stu-id="4badf-112">*When a record is deleted*,</span></span>  
    <span data-ttu-id="4badf-113">*När en post ändras*,</span><span class="sxs-lookup"><span data-stu-id="4badf-113">*When a record is modified*,</span></span>  
    <span data-ttu-id="4badf-114">*När ett kundgodkännande begärs*,</span><span class="sxs-lookup"><span data-stu-id="4badf-114">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="4badf-115">*När ett godkännande för redovisningsjournal begärs*,</span><span class="sxs-lookup"><span data-stu-id="4badf-115">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="4badf-116">*När ett godkännande av en redovisningsjournalrad begärs*,</span><span class="sxs-lookup"><span data-stu-id="4badf-116">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="4badf-117">*När ett artikelgodkännande begärs*,</span><span class="sxs-lookup"><span data-stu-id="4badf-117">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="4badf-118">*När ett godkännande av ett inköpsdokument begärs*,</span><span class="sxs-lookup"><span data-stu-id="4badf-118">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="4badf-119">*När ett godkännande av ett säljdokument begärs*, eller</span><span class="sxs-lookup"><span data-stu-id="4badf-119">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="4badf-120">*När ett leverantörsgodkännande begärs*.</span><span class="sxs-lookup"><span data-stu-id="4badf-120">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="4badf-121">Flow komner att uppmana dig att ange den information som behövs för att ansluta till dina [!INCLUDE[d365fin](includes/d365fin_md.md)]-data.</span><span class="sxs-lookup"><span data-stu-id="4badf-121">Flow will prompt you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="4badf-122">Om du har valt någon av följande utlösare: *När en post skapas*, *När en post ändras*, eller *När en post tas bort*, måste du välja ett företagsnamn och tabellnamn.</span><span class="sxs-lookup"><span data-stu-id="4badf-122">If you selected one of the following triggers: *When a record is created*, *When a record is modified*, or *When a record is deleted*, you must select a company name and table name.</span></span> <span data-ttu-id="4badf-123">Till varje utlösare krävs bara företagsnamnet för att ansluta.</span><span class="sxs-lookup"><span data-stu-id="4badf-123">With any other trigger, only the company name is required to connect.</span></span>

   <span data-ttu-id="4badf-124">Flow visar en lista över företag och tabeller som finns på [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4badf-124">Flow will show a list of companies and tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4badf-125">Dessa listor eller slutpunkter motsvarar de webbtjänster som du har publicerat från ditt [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4badf-125">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="4badf-126">Du kan också skapa en ny webbtjänst-URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] med hjälp av åtgärden **skapa datauppsättning** på sidan **webbtjänster** med hjälp av den assisterade inställningsguiden **Ställa in rapportering**  eller genom att välja åtgärden **redigera i Excel** i någon lista.</span><span class="sxs-lookup"><span data-stu-id="4badf-126">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>

<span data-ttu-id="4badf-127">Du har nu lyckats ansluta till dina Finance and Operations, Business edition-data och är redo att börja skapa ditt flöde.</span><span class="sxs-lookup"><span data-stu-id="4badf-127">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="4badf-128">Mer information finns i [Flow-dokumentation](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="4badf-128">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="4badf-129">För att felsöka ditt Microsoft Flow, se [Felsöka integrering med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="4badf-129">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4badf-130">Se även</span><span class="sxs-lookup"><span data-stu-id="4badf-130">See Also</span></span>
<span data-ttu-id="4badf-131">[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="4badf-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="4badf-132">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="4badf-132">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="4badf-133">[Hantera användare och behörigheter](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="4badf-133">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="4badf-134">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="4badf-134">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="4badf-135">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="4badf-135">Finance</span></span>](finance.md)  

