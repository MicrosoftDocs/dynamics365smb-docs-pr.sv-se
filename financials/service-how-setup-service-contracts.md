---
title: Konfigurera servicekontrakt | Microsoft Docs
description: "Så här skapar du servicekontrakt"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 203f6ef7f156bdccaa491fdac761711fd32c317e
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---

# <a name="how-to-set-up-service-contracts"></a><span data-ttu-id="b92f3-103">Så här skapar du servicekontrakt</span><span class="sxs-lookup"><span data-stu-id="b92f3-103">How to: Set Up Service Contracts</span></span>
<span data-ttu-id="b92f3-104">Innan du kan arbeta med kontrakt, måste du ställa in följande:</span><span class="sxs-lookup"><span data-stu-id="b92f3-104">Before you can work with contracts, you must set up the following:</span></span> 

* <span data-ttu-id="b92f3-105">**Servicekontraktsgrupper**, som innehåller grupper med servicekontrakt som har vissa gemensamma egenskaper.</span><span class="sxs-lookup"><span data-stu-id="b92f3-105">**Service contract groups**, which gather service contracts that are related in some way.</span></span>
* <span data-ttu-id="b92f3-106">**Servicekontraktskontogrupper**, som används för att gruppera olika konton för servicekontrakt för servicefakturor som skapas för servicekontrakt.</span><span class="sxs-lookup"><span data-stu-id="b92f3-106">**Service contract account groups**, which are used to group the service contract accounts together for service invoices created for service contracts.</span></span> <span data-ttu-id="b92f3-107">Du kan tilldela dessa grupper servicekontrakt.</span><span class="sxs-lookup"><span data-stu-id="b92f3-107">You assign these groups to service contracts.</span></span>  
* <span data-ttu-id="b92f3-108">**Kontraktsmallar** som definierar kontrakslayouter av kontrakt som innehåller de vanligaste kontraktuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="b92f3-108">**Contract templates** that define contract layouts of contracts that include the most commonly used service contract details.</span></span> <span data-ttu-id="b92f3-109">Du kan skapa servicekontraktsofferter genom att använda mallar.</span><span class="sxs-lookup"><span data-stu-id="b92f3-109">When you create service contract quotes, you can create them by using templates.</span></span> <span data-ttu-id="b92f3-110">När du skapar en kontraktsoffert innehållet fälten mallfälten automatiskt.</span><span class="sxs-lookup"><span data-stu-id="b92f3-110">When you create a contract quote, the fields automatically contain the contents of the template fields.</span></span>
* <span data-ttu-id="b92f3-111">**Kundmallar** låter dig skapa serviceofferter för kontakter eller potentiella kunder som inte är registrerade som kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b92f3-111">**Customer templates** that let you create quotes for contacts or potential customers who are not registered as customers in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-set-up-a-service-contract-group"></a><span data-ttu-id="b92f3-112">Så här skapar du en servicekontraktsgrupp</span><span class="sxs-lookup"><span data-stu-id="b92f3-112">To set up a service contract group</span></span>  
1. <span data-ttu-id="b92f3-113">Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Servicekontraktgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b92f3-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contract Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b92f3-114">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="b92f3-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="b92f3-115">Markera kryssrutan **Endast rabatt på kont.order** om du vill att kontrakts- eller servicerabatter endast ska gälla för kontraktserviceorder, t.ex. underhåll.</span><span class="sxs-lookup"><span data-stu-id="b92f3-115">Choose the **Disc. on Contr. Orders Only** check box if you want contract or service discounts to be valid only for contract service orders, such as maintenance.</span></span>  

## <a name="to-set-up-a-service-contract-account-group"></a><span data-ttu-id="b92f3-116">Så här skapar du servicekontraktskontogrupper</span><span class="sxs-lookup"><span data-stu-id="b92f3-116">To set up a service contract account group</span></span>  
1. <span data-ttu-id="b92f3-117">Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Servicekontraktgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b92f3-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Serv. Contract Account Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b92f3-118">Skapa en ny servicekontraktskontomall.</span><span class="sxs-lookup"><span data-stu-id="b92f3-118">Create a new service contract account group.</span></span>   
3. <span data-ttu-id="b92f3-119">Fyll i fälten **Kod** och **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="b92f3-119">Fill in the **Code** and **Description** fields.</span></span> <span data-ttu-id="b92f3-120">Dessa fält beskriver servicekontogruppen.</span><span class="sxs-lookup"><span data-stu-id="b92f3-120">These fields describe the service account group.</span></span>  
4. <span data-ttu-id="b92f3-121">Fyll i fältet  **Ej förutbetalt kontrakt**. Det här fältet innehåller redovisningskontonumret för det konto som inte är förutbetalt.</span><span class="sxs-lookup"><span data-stu-id="b92f3-121">Fill in the **Non-Prepaid Contract Acc.** field, choose general ledger account number for the non-prepaid account.</span></span>  
5. <span data-ttu-id="b92f3-122">Fyll i fältet **Ej förutbetalt kontrakt**. Det här fältet innehåller redovisningskontonumret för det konto som inte är förutbetalt.</span><span class="sxs-lookup"><span data-stu-id="b92f3-122">In the **Prepaid Contract Acc.** field, choose the general ledger account number for the prepaid account.</span></span>  

## <a name="to-set-up-a-contract-template"></a><span data-ttu-id="b92f3-123">Så här skapar du en kontraktsmall</span><span class="sxs-lookup"><span data-stu-id="b92f3-123">To set up a contract template</span></span>  
1. <span data-ttu-id="b92f3-124">Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Servicekontraktgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b92f3-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contract Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b92f3-125">Skapa en ny servicekontraktsmall.</span><span class="sxs-lookup"><span data-stu-id="b92f3-125">Create a new service contract template.</span></span>  
3. <span data-ttu-id="b92f3-126">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="b92f3-126">In the **No.**</span></span> <span data-ttu-id="b92f3-127">Skriv numret på den artikel som har beställts i kontraktmallen.</span><span class="sxs-lookup"><span data-stu-id="b92f3-127">field, enter a number for the contract template.</span></span>  
  
     <span data-ttu-id="b92f3-128">Om du har skapat en nummerserie för kontraktsmallar i fönstret **Serviceinställningar** kan du trycka på Retur om du vill ange nästa lediga kontraktmallsnummer.</span><span class="sxs-lookup"><span data-stu-id="b92f3-128">Alternatively, if you have set up number series for contract templates in the **Service Mgt. Setup** window, you can press the Enter key to enter the next available contract template number.</span></span> <span data-ttu-id="b92f3-129">Fyll i resterande fält om det behövs.</span><span class="sxs-lookup"><span data-stu-id="b92f3-129">Fill in the other fields if appropriate.</span></span>  
  
4. <span data-ttu-id="b92f3-130">På snabbfliken **Faktura** fyller du i fältet **Serv.kontrakt kontomall kod** i **Fakturaperiod**, osv.</span><span class="sxs-lookup"><span data-stu-id="b92f3-130">On the **Invoice** FastTab, fill in the **Serv. Contract Acc. Group Code** field, the **Invoice Period**, and so on.</span></span> <span data-ttu-id="b92f3-131">Fyll i resterande fält om det behövs.</span><span class="sxs-lookup"><span data-stu-id="b92f3-131">Fill in the other fields if appropriate.</span></span>  
5. <span data-ttu-id="b92f3-132">Välj åtgärden **Servicerabatter** om du vill lägga till kontraktsrabatter.</span><span class="sxs-lookup"><span data-stu-id="b92f3-132">Choose the **Service Discounts** action to add contract discounts.</span></span>  

## <a name="to-set-up-a-customer-template"></a><span data-ttu-id="b92f3-133">Så här skapar du en kundmall</span><span class="sxs-lookup"><span data-stu-id="b92f3-133">To set up a customer template</span></span>  
1. <span data-ttu-id="b92f3-134">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kundmallar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b92f3-134">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b92f3-135">Skapa ett nytt kundmallskort.</span><span class="sxs-lookup"><span data-stu-id="b92f3-135">Create a new customer template card.</span></span>  
3. <span data-ttu-id="b92f3-136">Skriv en kod och en beskrivning av kundmallen på snabbfliken **Allmänt** i fälten **Kod** respektive **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="b92f3-136">On the **General** FastTab, enter a code and a description for the customer template in the **Code** and **Description** fields respectively.</span></span> 
4. <span data-ttu-id="b92f3-137">Om du vill definiera sökkriterier fyller du i de andra fälten, till exempel **Lands-/regionkod**, **Distriktskod** och **Språkkod**.</span><span class="sxs-lookup"><span data-stu-id="b92f3-137">To define search criteria, fill in the other fields, such as **Country/Region Code**, **Territory Code**, and **Language Code**.</span></span>  
5. <span data-ttu-id="b92f3-138">Fyll i fälten  **Rörelsebokföringsmall** och  **Kundbokföringsmall**.</span><span class="sxs-lookup"><span data-stu-id="b92f3-138">Fill in the **Gen. Bus. Posting Group** and **Customer Posting Group** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b92f3-139">Se även</span><span class="sxs-lookup"><span data-stu-id="b92f3-139">See Also</span></span>
[<span data-ttu-id="b92f3-140">Ställa in servicehantering</span><span class="sxs-lookup"><span data-stu-id="b92f3-140">Setting Up Service Management</span></span>](service-setup-service.md)
