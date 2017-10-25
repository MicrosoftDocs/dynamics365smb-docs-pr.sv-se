---
title: Flera kontrakt | Microsoft Docs
description: "Beroende på dina servicenivåavtal med en kund kan du bli tvungen att hantera en serviceartikel på fler än ett servicekontrakt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c4abfbcb3bc182fa14c44c427bc41ebd9d67f6cf
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="multiple-contracts"></a><span data-ttu-id="eb2be-103">Flera kontrakt</span><span class="sxs-lookup"><span data-stu-id="eb2be-103">Multiple Contracts</span></span>
<span data-ttu-id="eb2be-104">Beroende på dina servicenivåavtal med en kund kan du bli tvungen att hantera en serviceartikel på fler än ett servicekontrakt.</span><span class="sxs-lookup"><span data-stu-id="eb2be-104">Depending on your service level agreements with a customer, you may have to handle a service item under more than one service contract.</span></span>  
  
<span data-ttu-id="eb2be-105">Genom att hantera en serviceartikel i flera kontrakt, kan du göra följande:</span><span class="sxs-lookup"><span data-stu-id="eb2be-105">By handling a service item under multiple contracts, you can do the following:</span></span>  
  
* <span data-ttu-id="eb2be-106">Utfärda olika kontrakt för samma serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="eb2be-106">Issue different contracts for the same service item.</span></span>  
* <span data-ttu-id="eb2be-107">Utföra service på olika delar separat.</span><span class="sxs-lookup"><span data-stu-id="eb2be-107">Service parts separately.</span></span>  
* <span data-ttu-id="eb2be-108">Ta hänsyn till vilka behov som krävs för att utföra service på en serviceartikel, till exempel olika mekaniska komponenter och mjukvara.</span><span class="sxs-lookup"><span data-stu-id="eb2be-108">Consider different skills that are required to service different aspects of a service item, such as mechanical components and software.</span></span>  
* <span data-ttu-id="eb2be-109">Specificera olika svarstider och frekvenser för service på olika delar av en serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="eb2be-109">Specify different response times and frequencies in servicing different parts of a service item.</span></span>  
* <span data-ttu-id="eb2be-110">Hantera olika typer av aktiviteter som ska utföras på en serviceartikel när den kräver olika typer av service vid olika tidpunkter.</span><span class="sxs-lookup"><span data-stu-id="eb2be-110">Address different kinds of activities to be performed on a service item when the service item requires different types of service in different time periods.</span></span>  
* <span data-ttu-id="eb2be-111">Välja och tilldela en serviceartikelrad ett korrekt kontraktsnummer när du skapar en serviceorder.</span><span class="sxs-lookup"><span data-stu-id="eb2be-111">Select and assign an appropriate contract number to a service item line when you are creating a service order.</span></span>  
* <span data-ttu-id="eb2be-112">Hantera relevant ekonomisk information för serviceartiklar och servicenivåavtal.</span><span class="sxs-lookup"><span data-stu-id="eb2be-112">Handle relevant financial information about service items and service level agreements.</span></span>  
  
<span data-ttu-id="eb2be-113">Titta på följande exempel som visar hur du kan använda funktionen för flera kontrakt.</span><span class="sxs-lookup"><span data-stu-id="eb2be-113">You can consider the following examples of using the multiple contracts functionality.</span></span>  
  
## <a name="creating-multiple-contracts-per-service-item"></a><span data-ttu-id="eb2be-114">Skapa flera kontrakt per serviceartikel</span><span class="sxs-lookup"><span data-stu-id="eb2be-114">Creating Multiple Contracts per Service Item</span></span>  
<span data-ttu-id="eb2be-115">Du kan manuellt skapa ett servicekontrakt eller en kontraktsoffert för serviceartiklar som redan har registrerats i icke-annullerade kontrakt som ägs av samma kund.</span><span class="sxs-lookup"><span data-stu-id="eb2be-115">You can manually create a service contract or contract quote for service items already registered in non-canceled contracts owned by the same customer.</span></span> <span data-ttu-id="eb2be-116">Följ standardprocessen där du skapar servicekontrakt och servicekontraktsofferter om du vill göra detta.</span><span class="sxs-lookup"><span data-stu-id="eb2be-116">To do this, follow the standard procedure of creating service contracts and service contract quotes.</span></span> <span data-ttu-id="eb2be-117">Mer information finns i [så här: arbeta med servicekontrakt och servicekontraktsofferter](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span><span class="sxs-lookup"><span data-stu-id="eb2be-117">For more information, see [How to: Work with Service Contracts and Service Contract Quotes](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span></span>  
  
<span data-ttu-id="eb2be-118">När du lägger till en serviceartikel på en kontraktsrad som är registrerad i andra servicekontrakt eller kontraktsofferter, visas ett varningsmeddelande med texten att serviceartikeln redan tillhör ett eller flera servicekontrakt eller kontraktsofferter.</span><span class="sxs-lookup"><span data-stu-id="eb2be-118">When you add a service item on a contract line that is registered in other service contracts or contract quotes, a warning message is displayed stating that the service item already belongs to one or more service contracts or contract quotes.</span></span> <span data-ttu-id="eb2be-119">Om du bekräftar meddelandet kommer all relevant serviceartikelinformation att kopieras till en ny kontraktsrad.</span><span class="sxs-lookup"><span data-stu-id="eb2be-119">If you confirm this message, all relevant service item information is copied to a newly created contract line.</span></span>  
  
## <a name="copying-documents"></a><span data-ttu-id="eb2be-120">Kopiera dokument</span><span class="sxs-lookup"><span data-stu-id="eb2be-120">Copying Documents</span></span>  
<span data-ttu-id="eb2be-121">Du kan automatiskt skapa ett servicekontrakt eller en kontraktsoffert för serviceartiklar som redan har registrerats i andra servicekontrakt eller kontraktsofferter med hjälp av åtgärden **Kopiera dokument**.</span><span class="sxs-lookup"><span data-stu-id="eb2be-121">You can automatically create a service contract or contract quote for service items that are already registered in other service contracts or contract quotes by using the **Copy Document** action.</span></span>  
  
## <a name="creating-service-orders-for-multiple-contracts"></a><span data-ttu-id="eb2be-122">Skapa serviceorder för flera kontrakt</span><span class="sxs-lookup"><span data-stu-id="eb2be-122">Creating Service Orders for Multiple Contracts</span></span>  
<span data-ttu-id="eb2be-123">Du kan skapa en serviceorder manuellt för en serviceartikel som är registrerad i flera aktiva kontrakt.</span><span class="sxs-lookup"><span data-stu-id="eb2be-123">You can manually create a service order for a service item that is registered in multiple active contracts.</span></span> <span data-ttu-id="eb2be-124">Ett servicekontrakt är aktivt när det är signerat och inte utgånget.</span><span class="sxs-lookup"><span data-stu-id="eb2be-124">A service contract is active when it is signed and not expired.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb2be-125">Se även</span><span class="sxs-lookup"><span data-stu-id="eb2be-125">See Also</span></span>  
[<span data-ttu-id="eb2be-126">Uppfylla servicekontrakt</span><span class="sxs-lookup"><span data-stu-id="eb2be-126">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)  
[<span data-ttu-id="eb2be-127">Så här skapar du serviceorder</span><span class="sxs-lookup"><span data-stu-id="eb2be-127">How to: Create Service Orders</span></span>](service-how-to-create-service-orders.md)  

