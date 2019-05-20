---
title: Felsöka integrering med Microsoft Flow| Microsoft Docs
description: Felsök hur du kan göra dina Business Central-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa ett automatiskt arbetsflöde.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 8a43df89261867f80ba16782cde92b040ce180c8
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240240"
---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="e78e9-103">Felsöka integrering med Microsoft Flow URL för begäran är för lång</span><span class="sxs-lookup"><span data-stu-id="e78e9-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="e78e9-104">Du kan använda din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av ett arbetsflöde i Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="e78e9-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="e78e9-105">Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Flow.</span><span class="sxs-lookup"><span data-stu-id="e78e9-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="e78e9-106">Om du skapar ett Microsoft Flow med hjälp av [!INCLUDE[d365fin](includes/d365fin_md.md)]-anslutningen visas ibland ett felmeddelande om att begärd URL är för lång efter det att flödet har skapats, till exempel: **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="e78e9-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="e78e9-107">Orsak</span><span class="sxs-lookup"><span data-stu-id="e78e9-107">Cause</span></span>
<span data-ttu-id="e78e9-108">För att ett flöde ska lösa ut letar det efter ändringar i dina data.</span><span class="sxs-lookup"><span data-stu-id="e78e9-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="e78e9-109">För att bestämma huruvida din information har ändrats, jämför kopplingarna cachelagrade data med de nya uppgifter som begärs från källan.</span><span class="sxs-lookup"><span data-stu-id="e78e9-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="e78e9-110">Om databegäran skapar en URL som är för lång, misslyckas den.</span><span class="sxs-lookup"><span data-stu-id="e78e9-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="e78e9-111">Vanliga orsaker är till exempel:</span><span class="sxs-lookup"><span data-stu-id="e78e9-111">Common causes may include:</span></span>
- <span data-ttu-id="e78e9-112">I allmänhet källtabeller med mer än 250 rader</span><span class="sxs-lookup"><span data-stu-id="e78e9-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="e78e9-113">Källtabeller som innehåller flera tusen transaktioner</span><span class="sxs-lookup"><span data-stu-id="e78e9-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="e78e9-114">Lösning</span><span class="sxs-lookup"><span data-stu-id="e78e9-114">Workaround</span></span>
<span data-ttu-id="e78e9-115">Följ nedanstående instruktioner om du vill lösa problemet.</span><span class="sxs-lookup"><span data-stu-id="e78e9-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="e78e9-116">Välj att redigera det flöde som inte fungerar.</span><span class="sxs-lookup"><span data-stu-id="e78e9-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="e78e9-117">Expandera **visa avancerade alternativ** i flödesutlösaren.</span><span class="sxs-lookup"><span data-stu-id="e78e9-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="e78e9-118">I fältet **Hoppa över räkning** anger du det antal transaktioner som ska hoppas över.</span><span class="sxs-lookup"><span data-stu-id="e78e9-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="e78e9-119">Till exempel: Om den tabell som du använder som datakälla har 4 000 transaktioner, ange då 4 000 som antalet transaktioner som ska hoppas över.</span><span class="sxs-lookup"><span data-stu-id="e78e9-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="e78e9-120">Uppdatera ditt flöde.</span><span class="sxs-lookup"><span data-stu-id="e78e9-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="e78e9-121">Kopplingen är fortfarande på betastadiet.</span><span class="sxs-lookup"><span data-stu-id="e78e9-121">The connector is currently in Beta.</span></span> <span data-ttu-id="e78e9-122">Uppdateringar av hur förändras kommer i en framtida version.</span><span class="sxs-lookup"><span data-stu-id="e78e9-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="e78e9-123">Se även</span><span class="sxs-lookup"><span data-stu-id="e78e9-123">See Also</span></span>
<span data-ttu-id="e78e9-124">[Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett automatiserat arbetsflöde](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="e78e9-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
[<span data-ttu-id="e78e9-125">Komma igång</span><span class="sxs-lookup"><span data-stu-id="e78e9-125">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="e78e9-126">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="e78e9-126">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="e78e9-127">[Hantera användare och behörigheter](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="e78e9-127">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="e78e9-128">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="e78e9-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="e78e9-129">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="e78e9-129">Finance</span></span>](finance.md)  
