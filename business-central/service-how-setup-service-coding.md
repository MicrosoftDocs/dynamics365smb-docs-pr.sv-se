---
title: Definiera koder för standardtjänster | Microsoft Docs
description: Lär dig mer om att lägga upp koder för serviceaktiviteter som du utför ofta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2db9480789e90b15e0a9d4e737817d3b8ff3b3c9
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925837"
---
# <a name="set-up-standard-service-codes"></a><span data-ttu-id="8a442-103">Skapa standardtjänstekoder</span><span class="sxs-lookup"><span data-stu-id="8a442-103">Set Up Standard Service Codes</span></span>

<span data-ttu-id="8a442-104">När du utför en vanlig typ av service behöver du ofta skapa servicedokument som använder servicerader som innehåller liknande information.</span><span class="sxs-lookup"><span data-stu-id="8a442-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="8a442-105">Om du vill göra det enklare att skapa de här raderna, lägger du in standardtjänstkoder som har en fördefinierad grupp med servicerader.</span><span class="sxs-lookup"><span data-stu-id="8a442-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="8a442-106">Raderna infogas automatiskt när du väljer koden i ett servicedokument.</span><span class="sxs-lookup"><span data-stu-id="8a442-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="8a442-107">Du kan ställa in ett antal standardtjänstekoder, och varje kod kan ha ett obegränsat antal servicerader av olika typer, inklusive artikel, resurs, kostnad eller standardtext kopplade till sig.</span><span class="sxs-lookup"><span data-stu-id="8a442-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standard text linked to it.</span></span> <span data-ttu-id="8a442-108">Du skapar servicerader för varje standardtjänstkod på kortet **standardtjänstkod**.</span><span class="sxs-lookup"><span data-stu-id="8a442-108">You create service lines of each standard service code on the **Standard Service Code** card.</span></span> <span data-ttu-id="8a442-109">Du kan sedan tilldela standardtjänstkoderna till serviceartikelgrupper på sidan **Standardgruppkoder för serviceartiklar**.</span><span class="sxs-lookup"><span data-stu-id="8a442-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="8a442-110">Senare när du skapar ett servicedokument kan du använda åtgärden **få standardtjänstkoder** för att lägga till serviceraderna.</span><span class="sxs-lookup"><span data-stu-id="8a442-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
> <span data-ttu-id="8a442-111">Du kan använda samma begrepp för att skapa rader i försäljnings- och inköpsdokument.</span><span class="sxs-lookup"><span data-stu-id="8a442-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="8a442-112">Mer information finns i [Skapa återkommande försäljnings- och inköpsrader](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="8a442-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>  
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="8a442-113">Så här skapar du standardtjänstkoder</span><span class="sxs-lookup"><span data-stu-id="8a442-113">To set up a standard service code</span></span>

1. <span data-ttu-id="8a442-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **standardservicekoder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8a442-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8a442-115">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="8a442-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="8a442-116">Fyll i serviceraderna som är kopplade till den här servicekoden.</span><span class="sxs-lookup"><span data-stu-id="8a442-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="8a442-117">Så här tilldelar du en standardtjänstkod till en serviceartikelgrupp</span><span class="sxs-lookup"><span data-stu-id="8a442-117">To assign a standard service code to a service item group</span></span>

1. <span data-ttu-id="8a442-118">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Serviceartikelgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8a442-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8a442-119">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="8a442-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="8a442-120">Fyll i serviceraderna som är kopplade till den här servicekoden.</span><span class="sxs-lookup"><span data-stu-id="8a442-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8a442-121">Se även</span><span class="sxs-lookup"><span data-stu-id="8a442-121">See Also</span></span>

[<span data-ttu-id="8a442-122">Servicehantering</span><span class="sxs-lookup"><span data-stu-id="8a442-122">Service Management</span></span>](service-service.md)