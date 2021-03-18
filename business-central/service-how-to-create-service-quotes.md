---
title: Så här skapar du Serviceofferter | Microsoft Docs
description: Du kan använda sidan **Serviceoffert** för att skapa dokument där du anger information om service, som reparation och underhåll, på serviceartiklar efter kundkrav. Du kan använda en serviceoffert som preliminärt utkast för en serviceorder och sedan omvandla offerten till en serviceorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 92c93b2e0b876920f1c259d31b4d839a5b2ecbc0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388805"
---
# <a name="create-service-quotes"></a><span data-ttu-id="8c71d-104">Skapa tjänsteofferter</span><span class="sxs-lookup"><span data-stu-id="8c71d-104">Create Service Quotes</span></span>
<span data-ttu-id="8c71d-105">Du kan se serviceofferter som grund för serviceorder.</span><span class="sxs-lookup"><span data-stu-id="8c71d-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="8c71d-106">De är i själva verket nästan identiska.</span><span class="sxs-lookup"><span data-stu-id="8c71d-106">In fact, they are almost identical.</span></span> <span data-ttu-id="8c71d-107">De innehåller båda information som till exempel vem kunden är, typ av order, artikeln som behöver service, fakturering- och leveransinformation och information om det faktiska servicearbetet.</span><span class="sxs-lookup"><span data-stu-id="8c71d-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="8c71d-108">Du kan använda en serviceoffert som preliminärt utkast för en serviceorder och sedan omvandla offerten till en serviceorder.</span><span class="sxs-lookup"><span data-stu-id="8c71d-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="8c71d-109">Så här skapar du serviceofferter</span><span class="sxs-lookup"><span data-stu-id="8c71d-109">To create a service quote</span></span>  
1. <span data-ttu-id="8c71d-110">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **serviceofferter** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8c71d-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8c71d-111">Skapa en ny serviceoffert.</span><span class="sxs-lookup"><span data-stu-id="8c71d-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="8c71d-112">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="8c71d-112">In the **No.**</span></span> <span data-ttu-id="8c71d-113">anger du ett nummer för serviceofferten.</span><span class="sxs-lookup"><span data-stu-id="8c71d-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="8c71d-114">Om du har angett nummerserier för serviceofferter på sidan **Serviceinställningar** kan du trycka på Retur, så väljs nästa tillgängliga serviceoffertnummer.</span><span class="sxs-lookup"><span data-stu-id="8c71d-114">Alternatively, if you have set up a number series for service quotes on the **Service Mgt. Setup** page, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="8c71d-115">I fältet **Kundnr.**</span><span class="sxs-lookup"><span data-stu-id="8c71d-115">In the **Customer No.**</span></span>  <span data-ttu-id="8c71d-116">välj relevant kund i listan.</span><span class="sxs-lookup"><span data-stu-id="8c71d-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="8c71d-117">Kundfälten fylls i automatiskt med information från kortet **Kund**.</span><span class="sxs-lookup"><span data-stu-id="8c71d-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="8c71d-118">Om kortet **Kund** inte finns för kunden, och du har lagt upp en kundmall, kan du skapa kunden från serviceofferten.</span><span class="sxs-lookup"><span data-stu-id="8c71d-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="8c71d-119">Fyll i relevanta fält och välj sedan åtgärden **Skapa kund**.</span><span class="sxs-lookup"><span data-stu-id="8c71d-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="8c71d-120">Beroende på inställningarna på snabbfliken **Obligatoriska fält** om ska finnas på sidan **Serviceinställningar** kanske du måste fylla i fältet **Tjänsteordertyp** på fältet **Säljarkod**.</span><span class="sxs-lookup"><span data-stu-id="8c71d-120">Depending on the settings on the **Mandatory Fields** FastTab on the **Service Mgt. Setup** page, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="8c71d-121">Fyll i serviceartikelraderna.</span><span class="sxs-lookup"><span data-stu-id="8c71d-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="8c71d-122">Registrera uppskattade kostnader på serviceraderna.</span><span class="sxs-lookup"><span data-stu-id="8c71d-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8c71d-123">Se även</span><span class="sxs-lookup"><span data-stu-id="8c71d-123">See Also</span></span>  
[<span data-ttu-id="8c71d-124">Skapa tjänsteorder</span><span class="sxs-lookup"><span data-stu-id="8c71d-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="8c71d-125">Arbeta med tjänsteuppgifter</span><span class="sxs-lookup"><span data-stu-id="8c71d-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 

[!INCLUDE[footer-include](includes/footer-banner.md)]