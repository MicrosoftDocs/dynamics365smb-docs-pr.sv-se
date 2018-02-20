---
title: "Definiera koder för standardtjänster | Microsoft Docs"
description: "Lär dig mer om att lägga upp koder för serviceaktiviteter som du utför ofta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2d617fa06ea18d6e74f473600020f14d8f286d98
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---

# <a name="set-up-standard-service-codes"></a><span data-ttu-id="bb9ed-103">Skapa standardtjänstekoder</span><span class="sxs-lookup"><span data-stu-id="bb9ed-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="bb9ed-104">När du utför en vanlig typ av service behöver du ofta skapa servicedokument som använder servicerader som innehåller liknande information.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="bb9ed-105">Om du vill göra det enklare att skapa de här raderna, lägger du in standardtjänstkoder som har en fördefinierad grupp med servicerader.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="bb9ed-106">Raderna infogas automatiskt när du väljer koden i ett servicedokument.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="bb9ed-107">Du kan ställa in ett antal standardtjänstekoder, och varje kod kan ha ett obegränsat antal servicerader av olika typer, inklusive artikel, resurs, kostnad eller standardtext kopplade till sig.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="bb9ed-108">Du skapar servicerader för varje standardtjänstkod på kortet **standardtjänstkod**.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="bb9ed-109">Du kan sedan tilldela standardtjänstkoderna till serviceartikelgrupper på sidan **Standardgruppkoder för serviceartiklar**.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="bb9ed-110">Senare när du skapar ett servicedokument kan du använda åtgärden **få standardtjänstkoder** för att lägga till serviceraderna.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="bb9ed-111">Du kan använda samma begrepp för att skapa rader i försäljnings- och inköpsdokument.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="bb9ed-112">Mer information finns i [Skapa återkommande försäljnings- och inköpsrader](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="bb9ed-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="bb9ed-113">Så här skapar du standardtjänstkoder</span><span class="sxs-lookup"><span data-stu-id="bb9ed-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="bb9ed-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Standardservicekoder**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bb9ed-115">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="bb9ed-116">Fyll i serviceraderna som är kopplade till den här servicekoden.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="bb9ed-117">Så här tilldelar du en standardtjänstkod till en serviceartikelgrupp</span><span class="sxs-lookup"><span data-stu-id="bb9ed-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="bb9ed-118">Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Serviceartikelgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bb9ed-119">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="bb9ed-120">Fyll i serviceraderna som är kopplade till den här servicekoden.</span><span class="sxs-lookup"><span data-stu-id="bb9ed-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bb9ed-121">Se även</span><span class="sxs-lookup"><span data-stu-id="bb9ed-121">See Also</span></span>
[<span data-ttu-id="bb9ed-122">Servicehantering</span><span class="sxs-lookup"><span data-stu-id="bb9ed-122">Service Management</span></span>](service-service.md)
