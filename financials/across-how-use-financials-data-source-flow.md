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
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: dde99e50c6984a7ec162b4047e8640e6affb3f25
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="8d73e-103">Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett automatiskt arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="8d73e-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="8d73e-104">Du kan använda din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av ett arbetsflöde i Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="8d73e-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="8d73e-105">Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Flow.</span><span class="sxs-lookup"><span data-stu-id="8d73e-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="8d73e-106">Att lägga till [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakälla i Flow.</span><span class="sxs-lookup"><span data-stu-id="8d73e-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="8d73e-107">I webbläsaren, går du till [flow.microsoft.com](https://flow.microsoft.com/en-us/), och loggar in.</span><span class="sxs-lookup"><span data-stu-id="8d73e-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="8d73e-108">Välj **Mina flöden** från menyn längst upp på sidan.</span><span class="sxs-lookup"><span data-stu-id="8d73e-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="8d73e-109">I fönstret **Mina flöden** kan välja alternativet **Skapa från tom**.</span><span class="sxs-lookup"><span data-stu-id="8d73e-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="8d73e-110">I listan över tillgängliga utlösare, välj någon av de [!INCLUDE[d365fin](includes/d365fin_md.md)] utlösare som är tillgängliga:</span><span class="sxs-lookup"><span data-stu-id="8d73e-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="8d73e-111">*När ett kundgodkännande begärs*,</span><span class="sxs-lookup"><span data-stu-id="8d73e-111">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="8d73e-112">*När ett godkännande för redovisningsjournal begärs*,</span><span class="sxs-lookup"><span data-stu-id="8d73e-112">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="8d73e-113">*När ett godkännande av en redovisningsjournalrad begärs*,</span><span class="sxs-lookup"><span data-stu-id="8d73e-113">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="8d73e-114">*När ett artikelgodkännande begärs*,</span><span class="sxs-lookup"><span data-stu-id="8d73e-114">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="8d73e-115">*När ett godkännande av ett inköpsdokument begärs*,</span><span class="sxs-lookup"><span data-stu-id="8d73e-115">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="8d73e-116">*När ett godkännande av ett säljdokument begärs*, eller</span><span class="sxs-lookup"><span data-stu-id="8d73e-116">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="8d73e-117">*När ett leverantörsgodkännande begärs*.</span><span class="sxs-lookup"><span data-stu-id="8d73e-117">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="8d73e-118">Flödet kommer att be dig att välja ett företag inom din [!INCLUDE[d365fin](includes/d365fin_md.md)] klientorganisation.</span><span class="sxs-lookup"><span data-stu-id="8d73e-118">Flow will prompt you to select a company within your [!INCLUDE[d365fin](includes/d365fin_md.md)] tenant.</span></span> <span data-ttu-id="8d73e-119">Eftersom varje steg i flödet är oberoende av nästa kan du behöva definiera företaget flera gånger när du använder en [!INCLUDE[d365fin](includes/d365fin_md.md)]-mall.</span><span class="sxs-lookup"><span data-stu-id="8d73e-119">Because each step in the Flow is independent of the next, you may be required to define the company multiple times when using a [!INCLUDE[d365fin](includes/d365fin_md.md)] template.</span></span>

<span data-ttu-id="8d73e-120">Du har nu lyckats ansluta till dina Finance and Operations, Business edition-data och är redo att börja skapa ditt flöde.</span><span class="sxs-lookup"><span data-stu-id="8d73e-120">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="8d73e-121">Mer information finns i [Flow-dokumentation](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="8d73e-121">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="8d73e-122">För att felsöka ditt Microsoft Flow, se [Felsöka integrering med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="8d73e-122">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8d73e-123">Se även</span><span class="sxs-lookup"><span data-stu-id="8d73e-123">See Also</span></span>
<span data-ttu-id="8d73e-124">[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="8d73e-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="8d73e-125">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="8d73e-125">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="8d73e-126">[Hantera användare och behörigheter](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="8d73e-126">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="8d73e-127">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="8d73e-127">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="8d73e-128">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="8d73e-128">Finance</span></span>](finance.md)  

