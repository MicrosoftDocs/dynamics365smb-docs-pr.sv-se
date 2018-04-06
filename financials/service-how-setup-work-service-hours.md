---
title: "Ställa in arbetstimmar och servicetider | Microsoft Docs"
description: "Du kan ange servicearbetstider i företaget. Programmet använder dessa servicetider för att beräkna ett svarsdatum med tid för serviceorder och offerter och då svarstidsvarningar skickas ut."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 630875f80f4107522962c79734284569cbc2b6f7
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-work-hours-and-service-hours"></a><span data-ttu-id="ce1cb-104">Ställa in arbetstimmar och tjänstetider</span><span class="sxs-lookup"><span data-stu-id="ce1cb-104">Set Up Work Hours and Service Hours</span></span>
<span data-ttu-id="ce1cb-105">Ett tjänstehanteringssystem spårar vanligtvis resurstid och serviceorderstatus för prognostisering av arbetsbelastning och servicebehov.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-105">Typically, a service management system tracks resource hours and service order status in order to forecast workloads and service needs.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="ce1cb-106"> har inbyggda verktyg som du kan anpassa om du vill registrera den här typen av information.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-106"> has built-in tools that you can customize to record this kind of information.</span></span>  
  
<span data-ttu-id="ce1cb-107">När du har ställt in standardtjänsttid för företaget kan du beräkna svarstid för serviceorder eller skicka varningar eller aviseringar när servicesamtal kommer in.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-107">After you set the default service hours of your company, you can calculate response times for service orders or send warnings or alerts when service calls come in.</span></span> <span data-ttu-id="ce1cb-108">Aviseringsfunktionen implementeras tillsammans med projektschemat.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-108">The alert feature is implemented together with the job scheduler.</span></span>   
  
<span data-ttu-id="ce1cb-109">När du arbetar på en serviceorder kan du uppdatera deras status, så att du kan övervaka framsteg.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-109">As you work on a service order, you will want to update it's status so that you can monitor progress.</span></span> <span data-ttu-id="ce1cb-110">Tjänsteorderstatus visar reparationsstatus för alla serviceartiklar i serviceordern.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-110">The service order status reflects the repair status of all the service items in the service order.</span></span> <span data-ttu-id="ce1cb-111">Mer information finns i [om serviceordern och reparationsstatus](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="ce1cb-111">For more information, see [Understanding Service Order and Repair Status](service-order-repair-status.md).</span></span> 

## <a name="to-set-up-default-service-hours"></a><span data-ttu-id="ce1cb-112">Så här skapar du standard servicetider</span><span class="sxs-lookup"><span data-stu-id="ce1cb-112">To set up default service hours</span></span>  
<span data-ttu-id="ce1cb-113">Du kan använda fönstret **Standard servicetider** för att definiera vilka servicearbetstider som gäller på företaget.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-113">You use the **Default Service Hours** window to set up the usual service working hours in your company.</span></span> <span data-ttu-id="ce1cb-114">Programmet använder dessa servicetider för att beräkna ett svarsdatum med tid för serviceorder och offerter och då svarstidsvarningar skickas ut.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-114">These service hours are used to calculate the response date and time for service orders and quotes and to send response time warnings.</span></span> <span data-ttu-id="ce1cb-115">Standardservicetiden för servicekontrakt används automatiskt om du inte angett särskilda servicetider för ett kontrakt.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-115">The default service hours are used for service contracts unless you specify special service hours for a contract.</span></span>  
  
1. <span data-ttu-id="ce1cb-116">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **standardtjänsttider** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Default Service Hours**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ce1cb-117">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  <span data-ttu-id="ce1cb-118">Om du inte fyller i raderna i fönstret **Standard servicetider** används 24 timmar som standardvärde, som gäller bara för kalenderns arbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-118">If you leave the lines in the **Default Service Hours** window empty, the default value is 24 hours, valid only for calendar working days.</span></span>  
  
## <a name="to-set-up-work-hour-templates"></a><span data-ttu-id="ce1cb-119">Så här skapar du arbetstidsmallar</span><span class="sxs-lookup"><span data-stu-id="ce1cb-119">To set up work-hour templates</span></span>
<span data-ttu-id="ce1cb-120">Du kan använda fönstret **Arbetstidsmallar** för att skapa mallar som innehåller företagets vanligaste arbetstider.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-120">You can use the **Work-Hour Template** window to set up templates that contain the typical working hours in your company.</span></span> <span data-ttu-id="ce1cb-121">Du kan t.ex. skapa mallar för heltidstekniker och deltidstekniker.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-121">For example, you can create templates for full time technicians and part time technicians.</span></span> <span data-ttu-id="ce1cb-122">Använd arbetstidsmallar när du lägger till kapacitet i resurser.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-122">You can use work-hour templates when you add capacity to resources.</span></span>  
  
1. <span data-ttu-id="ce1cb-123">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **arbetstidsmallar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Hour Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ce1cb-124">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> <span data-ttu-id="ce1cb-125">När du har angett arbetstimmar per dag beräknas värdet i fältet **Totalt per vecka** automatiskt.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-125">After you enter work hours for each day, the value in the **Total per Week** field is calculated automatically.</span></span>  

## <a name="to-set-up-contract-specific-service-hours"></a><span data-ttu-id="ce1cb-126">Så här skapar du en kontraktspecifik servicekalender</span><span class="sxs-lookup"><span data-stu-id="ce1cb-126">To set up contract specific service hours</span></span>  
<span data-ttu-id="ce1cb-127">Du använder fönstret **Servicekalender** när du lägger upp servicetid för kunden som äger servicekontraktet.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-127">You can use the **Service Hours** window to set up specific service hours for the customer that owns the service contract.</span></span> <span data-ttu-id="ce1cb-128">Servicekalendern används för att beräkna svarsdatum och svarstid för serviceorder och serviceofferter som tillhör servicekontraktet.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-128">Service hours are used to calculate the response date and time for service orders and quotes that belong to the service contract.</span></span>  
  
<span data-ttu-id="ce1cb-129">Om du inte skapar en specifik servicekalender för ett servicekontrakt, används standardtjänstkalendern i stället.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-129">If you do not set up specific service hours for the service contract, the default service hours for service contracts are used.</span></span>  
  
1. <span data-ttu-id="ce1cb-130">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Servicekontrakt** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contracts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ce1cb-131">Öppna servicekontraktet du vill ställa in särskilda servicetimmar för och välj **Servicetimmar**.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-131">Open the service contract you want to set up specific service hours for, and choose **Service Hours**.</span></span>  
4. <span data-ttu-id="ce1cb-132">Om du vill lägga upp en servicekalender baserat på en standardtjänstkalender, väljer du åtgärden **Kopiera standardtjänsttider**.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-132">To set up service hours based on default service hours, choose the **Copy Default Service Hours** action.</span></span>  
5. <span data-ttu-id="ce1cb-133">Redigera fälten i servicekalendertransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-133">Edit the fields in the service hours entries.</span></span> <span data-ttu-id="ce1cb-134">Infoga eller ta bort transaktioner för att konfigurera servicekalendern för kontraktet.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-134">Insert or delete entries to set up the service hours for the contract.</span></span> <span data-ttu-id="ce1cb-135">Observera att fälten **Dag**, **Starttid** och **Sluttid** måste anges för varje rad.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-135">Note that the fields **Day**, **Starting Time** and **Ending Time** are required for each line.</span></span>  
6. <span data-ttu-id="ce1cb-136">Om du vill att servicekalendern ska gälla från ett visst datum fyller du i fältet **Startdatum**.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-136">If you want the service hours to be valid from a specific date, fill in the **Starting Date** field.</span></span>  
7. <span data-ttu-id="ce1cb-137">Om du vill att servicekontraktet ska gälla under semestern markerar du kryssrutan i fältet **Giltigt på semestrar**.</span><span class="sxs-lookup"><span data-stu-id="ce1cb-137">If you want the service hours to be valid on holidays, select the check box in the **Valid on Holidays** field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce1cb-138">Se även</span><span class="sxs-lookup"><span data-stu-id="ce1cb-138">See Also</span></span>  
[<span data-ttu-id="ce1cb-139">Förstå fördelningsstatus och reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="ce1cb-139">Understanding Allocation Status and Repair Status</span></span>](service-allocation-status-and-repair-status.md)  
[<span data-ttu-id="ce1cb-140">Ställa in tjänstehantering</span><span class="sxs-lookup"><span data-stu-id="ce1cb-140">Setting Up Service Management</span></span>](service-setup-service.md)  
[<span data-ttu-id="ce1cb-141">Förstå serviceorderstatus och reparationsstatus</span><span class="sxs-lookup"><span data-stu-id="ce1cb-141">Understanding Service Order and Repair Status</span></span>](service-order-repair-status.md)  

