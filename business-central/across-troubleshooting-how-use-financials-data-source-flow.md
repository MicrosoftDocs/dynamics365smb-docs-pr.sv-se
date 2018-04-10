---
title: "Felsöka integrering med Microsoft Flow | Microsoft Docs"
description: "Felsök hur du kan göra dina Financials-data tillgängliga som datakälla, och ange en OData-URL för dina webbtjänster för att skapa ett automatiskt arbetsflöde."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 68355bc0b4afe4fcdd92f9cdb190d4b5c0d845df
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="f55a4-103">Felsöka integrering med Microsoft Flow - URL för begäran är för lång</span><span class="sxs-lookup"><span data-stu-id="f55a4-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="f55a4-104">Du kan använda din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av ett arbetsflöde i Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="f55a4-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="f55a4-105">Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Flow.</span><span class="sxs-lookup"><span data-stu-id="f55a4-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="f55a4-106">Om du skapar ett Microsoft Flow med hjälp av anslutningen [!INCLUDE[d365fin](includes/d365fin_md.md)] visas ibland ett felmeddelande om att begärd URL är för lång efter det att flödet har skapats, till exempel: **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="f55a4-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="f55a4-107">Orsak</span><span class="sxs-lookup"><span data-stu-id="f55a4-107">Cause</span></span>
<span data-ttu-id="f55a4-108">För att ett flöde ska lösa ut letar det efter ändringar i dina data.</span><span class="sxs-lookup"><span data-stu-id="f55a4-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="f55a4-109">För att bestämma huruvida din information har ändrats, jämför kopplingarna cachelagrade data med de nya uppgifter som begärs från källan.</span><span class="sxs-lookup"><span data-stu-id="f55a4-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="f55a4-110">Om databegäran skapar en URL som är för lång, misslyckas den.</span><span class="sxs-lookup"><span data-stu-id="f55a4-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="f55a4-111">Vanliga orsaker är till exempel:</span><span class="sxs-lookup"><span data-stu-id="f55a4-111">Common causes may include:</span></span>
- <span data-ttu-id="f55a4-112">I allmänhet källtabeller med mer än 250 rader</span><span class="sxs-lookup"><span data-stu-id="f55a4-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="f55a4-113">Källtabeller som innehåller flera tusen transaktioner</span><span class="sxs-lookup"><span data-stu-id="f55a4-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="f55a4-114">Lösning</span><span class="sxs-lookup"><span data-stu-id="f55a4-114">Workaround</span></span>
<span data-ttu-id="f55a4-115">Följ nedanstående instruktioner om du vill lösa problemet.</span><span class="sxs-lookup"><span data-stu-id="f55a4-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="f55a4-116">Välj att redigera det flöde som inte fungerar.</span><span class="sxs-lookup"><span data-stu-id="f55a4-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="f55a4-117">Expandera **visa avancerade alternativ** i flödesutlösaren.</span><span class="sxs-lookup"><span data-stu-id="f55a4-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="f55a4-118">I fältet **Hoppa över räkning** anger du det antal transaktioner som ska hoppas över.</span><span class="sxs-lookup"><span data-stu-id="f55a4-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="f55a4-119">Till exempel: Om den tabell som du använder som datakälla har 4 000 transaktioner, ange då 4 000 som antalet transaktioner som ska hoppas över.</span><span class="sxs-lookup"><span data-stu-id="f55a4-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="f55a4-120">Uppdatera ditt flöde.</span><span class="sxs-lookup"><span data-stu-id="f55a4-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="f55a4-121">Kopplingen är fortfarande på betastadiet.</span><span class="sxs-lookup"><span data-stu-id="f55a4-121">The connector is currently in Beta.</span></span> <span data-ttu-id="f55a4-122">Uppdateringar av hur förändras kommer i en framtida version.</span><span class="sxs-lookup"><span data-stu-id="f55a4-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="f55a4-123">Se även</span><span class="sxs-lookup"><span data-stu-id="f55a4-123">See Also</span></span>
<span data-ttu-id="f55a4-124">[Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett automatiserat arbetsflöde](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="f55a4-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
[<span data-ttu-id="f55a4-125">Komma igång</span><span class="sxs-lookup"><span data-stu-id="f55a4-125">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="f55a4-126">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="f55a4-126">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="f55a4-127">[Hantera användare och behörigheter](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="f55a4-127">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="f55a4-128">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="f55a4-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="f55a4-129">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="f55a4-129">Finance</span></span>](finance.md)  
