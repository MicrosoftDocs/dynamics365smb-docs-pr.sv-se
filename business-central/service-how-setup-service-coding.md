---
title: "Definiera koder för standardtjänster | Microsoft Docs"
description: "Lär dig mer om att lägga upp koder för serviceaktiviteter som du utför ofta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f73f5b9d74e7b6a75be6320697aa1a4ad84fb4a1
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---

# <a name="set-up-standard-service-codes"></a><span data-ttu-id="350f6-103">Skapa standardtjänstekoder</span><span class="sxs-lookup"><span data-stu-id="350f6-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="350f6-104">När du utför en vanlig typ av service behöver du ofta skapa servicedokument som använder servicerader som innehåller liknande information.</span><span class="sxs-lookup"><span data-stu-id="350f6-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="350f6-105">Om du vill göra det enklare att skapa de här raderna, lägger du in standardtjänstkoder som har en fördefinierad grupp med servicerader.</span><span class="sxs-lookup"><span data-stu-id="350f6-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="350f6-106">Raderna infogas automatiskt när du väljer koden i ett servicedokument.</span><span class="sxs-lookup"><span data-stu-id="350f6-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="350f6-107">Du kan ställa in ett antal standardtjänstekoder, och varje kod kan ha ett obegränsat antal servicerader av olika typer, inklusive artikel, resurs, kostnad eller standardtext kopplade till sig.</span><span class="sxs-lookup"><span data-stu-id="350f6-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="350f6-108">Du skapar servicerader för varje standardtjänstkod på kortet **standardtjänstkod**.</span><span class="sxs-lookup"><span data-stu-id="350f6-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="350f6-109">Du kan sedan tilldela standardservicekoderna till serviceartikelgrupper i fönstret **Standardgruppkoder för serviceartiklar**.</span><span class="sxs-lookup"><span data-stu-id="350f6-109">You then assign standard service codes to service item groups in the **Standard Serv. Item Gr. Codes** window.</span></span> <span data-ttu-id="350f6-110">Senare när du skapar ett servicedokument kan du använda åtgärden **få standardtjänstkoder** för att lägga till serviceraderna.</span><span class="sxs-lookup"><span data-stu-id="350f6-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="350f6-111">Du kan använda samma begrepp för att skapa rader i försäljnings- och inköpsdokument.</span><span class="sxs-lookup"><span data-stu-id="350f6-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="350f6-112">Mer information finns i [Skapa återkommande försäljnings- och inköpsrader](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="350f6-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="350f6-113">Så här skapar du standardtjänstkoder</span><span class="sxs-lookup"><span data-stu-id="350f6-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="350f6-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Standardservicekoder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="350f6-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="350f6-115">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="350f6-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="350f6-116">Fyll i serviceraderna som är kopplade till den här servicekoden.</span><span class="sxs-lookup"><span data-stu-id="350f6-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="350f6-117">Så här tilldelar du en standardtjänstkod till en serviceartikelgrupp</span><span class="sxs-lookup"><span data-stu-id="350f6-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="350f6-118">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Serviceartikelgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="350f6-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="350f6-119">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="350f6-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="350f6-120">Fyll i serviceraderna som är kopplade till den här servicekoden.</span><span class="sxs-lookup"><span data-stu-id="350f6-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="350f6-121">Se även</span><span class="sxs-lookup"><span data-stu-id="350f6-121">See Also</span></span>
[<span data-ttu-id="350f6-122">Servicehantering</span><span class="sxs-lookup"><span data-stu-id="350f6-122">Service Management</span></span>](service-service.md)
