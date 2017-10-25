---
title: "Så här skapar du Serviceofferter | Microsoft Docs"
description: "Du kan använda fönstret **Serviceoffert** för att skapa dokument där du anger information om service, som reparation och underhåll, på serviceartiklar efter kundkrav. Du kan använda en serviceoffert som preliminärt utkast för en serviceorder och sedan omvandla offerten till en serviceorder."
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
ms.openlocfilehash: d5348e7b15eb0337f2a5f829c871dadcf3133b86
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-service-quotes"></a><span data-ttu-id="92052-104">Så här skapar du serviceofferter</span><span class="sxs-lookup"><span data-stu-id="92052-104">How to: Create Service Quotes</span></span>
<span data-ttu-id="92052-105">Du kan se serviceofferter som grund för serviceorder.</span><span class="sxs-lookup"><span data-stu-id="92052-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="92052-106">De är i själva verket nästan identiska.</span><span class="sxs-lookup"><span data-stu-id="92052-106">In fact, they are almost identical.</span></span> <span data-ttu-id="92052-107">De innehåller båda information som till exempel vem kunden är, typ av order, artikeln som behöver service, fakturering- och leveransinformation och information om det faktiska servicearbetet.</span><span class="sxs-lookup"><span data-stu-id="92052-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="92052-108">Du kan använda en serviceoffert som preliminärt utkast för en serviceorder och sedan omvandla offerten till en serviceorder.</span><span class="sxs-lookup"><span data-stu-id="92052-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="92052-109">Så här skapar du serviceofferter</span><span class="sxs-lookup"><span data-stu-id="92052-109">To create a service quote</span></span>  
1. <span data-ttu-id="92052-110">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Serviceoffert** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="92052-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="92052-111">Skapa en ny serviceoffert.</span><span class="sxs-lookup"><span data-stu-id="92052-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="92052-112">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="92052-112">In the **No.**</span></span> <span data-ttu-id="92052-113">anger du ett nummer för serviceofferten.</span><span class="sxs-lookup"><span data-stu-id="92052-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="92052-114">Om du har angett nummerserier för serviceofferter i fönstret **Serviceinställningar** kan du trycka på Retur, så väljs nästa tillgängliga serviceoffertnummer.</span><span class="sxs-lookup"><span data-stu-id="92052-114">Alternatively, if you have set up a number series for service quotes in the **Service Mgt. Setup** window, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="92052-115">I fältet **Kundnr.**</span><span class="sxs-lookup"><span data-stu-id="92052-115">In the **Customer No.**</span></span>  <span data-ttu-id="92052-116">välj relevant kund i listan.</span><span class="sxs-lookup"><span data-stu-id="92052-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="92052-117">Kundfälten fylls i automatiskt med information från kortet **Kund**.</span><span class="sxs-lookup"><span data-stu-id="92052-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="92052-118">Om kortet **Kund** inte finns för kunden, och du har lagt upp en kundmall, kan du skapa kunden från serviceofferten.</span><span class="sxs-lookup"><span data-stu-id="92052-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="92052-119">Fyll i relevanta fält och välj sedan åtgärden **Skapa kund**.</span><span class="sxs-lookup"><span data-stu-id="92052-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="92052-120">Beroende på inställningarna på snabbfliken **Obligatoriska fält** om ska finnas i fönstret **Serviceinställningar** kanske du måste fylla i fältet **Serviceordertyp** på fältet **Säljarkod**.</span><span class="sxs-lookup"><span data-stu-id="92052-120">Depending on the settings on the **Mandatory Fields** FastTab in the **Service Mgt. Setup** window, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="92052-121">Fyll i serviceartikelraderna.</span><span class="sxs-lookup"><span data-stu-id="92052-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="92052-122">Registrera uppskattade kostnader på serviceraderna.</span><span class="sxs-lookup"><span data-stu-id="92052-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="92052-123">Se även</span><span class="sxs-lookup"><span data-stu-id="92052-123">See Also</span></span>  
[<span data-ttu-id="92052-124">Så här skapar du serviceorder</span><span class="sxs-lookup"><span data-stu-id="92052-124">How to: Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="92052-125">Så här arbetar du med serviceuppgifter</span><span class="sxs-lookup"><span data-stu-id="92052-125">How to: Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 
