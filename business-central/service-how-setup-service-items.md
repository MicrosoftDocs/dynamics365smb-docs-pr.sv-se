---
title: Konfiguration serviceartiklar och serviceartikelkomponenter | Microsoft Docs
description: "Mer information om saker som du måste ställa in innan du kan använda serviceartiklar, inklusive standardvärden, till exempel svarstid, kontraktrabatt i procent och serviceprisgrupp."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e946bab348aeee1b65b85165b2d9d553736813ba
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-service-items-and-service-item-components"></a><span data-ttu-id="c1625-103">Ställa in tjänsteartiklar och tjänsteartikelkomponenter</span><span class="sxs-lookup"><span data-stu-id="c1625-103">Set Up Service Items and Service Item Components</span></span>
<span data-ttu-id="c1625-104">Om du vill arbeta med serviceartiklar måste du ställa in följande</span><span class="sxs-lookup"><span data-stu-id="c1625-104">To work with service items, you must set up the following</span></span>

* <span data-ttu-id="c1625-105">Serviceartikelgrupper</span><span class="sxs-lookup"><span data-stu-id="c1625-105">Service item groups.</span></span>
* <span data-ttu-id="c1625-106">Valfritt</span><span class="sxs-lookup"><span data-stu-id="c1625-106">Optional</span></span>

## <a name="to-set-up-service-item-groups"></a><span data-ttu-id="c1625-107">Så här skapar du serviceartikelgrupper:</span><span class="sxs-lookup"><span data-stu-id="c1625-107">To set up service item groups</span></span>
<span data-ttu-id="c1625-108">Du anger grupper med artiklar som hör ihop med avseende på reparation och underhåll.</span><span class="sxs-lookup"><span data-stu-id="c1625-108">You can set up groups of items that are related in terms of repair and maintenance.</span></span> <span data-ttu-id="c1625-109">Du kan ange standardvärden för serviceartiklar i serviceartikelgruppen, t.ex. svarstid, kontraktrabatt i procent och serviceprisgrupp.</span><span class="sxs-lookup"><span data-stu-id="c1625-109">You can define default values for service items in a service item group, such as response time, contract discount percent, and service price group.</span></span> <span data-ttu-id="c1625-110">För artiklar i en serviceartikelgrupp kan du välja om du vill att de ska registreras automatiskt som serviceartiklar då de säljs..</span><span class="sxs-lookup"><span data-stu-id="c1625-110">For items in a service item group, you can select whether you want them to be automatically registered as service items when they are sold.</span></span>  

<span data-ttu-id="c1625-111">Du tilldelar serviceartikelgrupper till artiklar på **Artikelkortet** och till serviceartiklar på **serviceartikelkortet**.</span><span class="sxs-lookup"><span data-stu-id="c1625-111">You assign service item groups to items on the **Item** card, and to service items on the **Service Item** card.</span></span>  

1. <span data-ttu-id="c1625-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Serviceartikelgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c1625-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c1625-113">Skapa en ny serviceartikelgrupp.</span><span class="sxs-lookup"><span data-stu-id="c1625-113">Create a new service item group.</span></span>  
3. <span data-ttu-id="c1625-114">Fyll i fälten **Kod** och **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="c1625-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="c1625-115">I fältet **Standard kontraktsrabatt %** anger du standardrabatten i procent för kontrakt som du vill att serviceartiklarna i gruppen ska ha.</span><span class="sxs-lookup"><span data-stu-id="c1625-115">In the **Default Contract Discount %** field, enter the default contract discount percentage that you want the service items in the group to have.</span></span>  
5. <span data-ttu-id="c1625-116">I fältet **Standard serviceprisgruppskod** anger du den förvalda serviceprisgruppskoden som du vill att serviceartiklarna i gruppen ska ha.</span><span class="sxs-lookup"><span data-stu-id="c1625-116">In the **Default Serv. Price Group Code** field, enter the default service price group code that you want the service items in the group to have.</span></span>  
6. <span data-ttu-id="c1625-117">I fältet **Standard svarstid (timmar)** anger du standardsvarstiden som du vill att serviceartiklarna i gruppen ska ha, i timmar.</span><span class="sxs-lookup"><span data-stu-id="c1625-117">In the **Default Response Time (Hours)** field, enter the default response time in hours that you want the service items in the group to have.</span></span>  
7. <span data-ttu-id="c1625-118">Om du vill att artiklarna i gruppen ska registreras som serviceartiklar då de säljs, väljer du fältet **Skapa serviceartikel**.</span><span class="sxs-lookup"><span data-stu-id="c1625-118">If you want to register the items in the group as service items when they are sold, select the **Create Service Item** field.</span></span>  

## <a name="to-set-up-service-item-components"></a><span data-ttu-id="c1625-119">Så här ställer du in serviceartikelkomponenter</span><span class="sxs-lookup"><span data-stu-id="c1625-119">To set up service item components</span></span>
<span data-ttu-id="c1625-120">En serviceartikel kan bestå av flera komponenter, som kan ersättas med reservdelar då artikeln är servad.</span><span class="sxs-lookup"><span data-stu-id="c1625-120">A service item can consist of several components, which can be replaced with spare parts when the item is serviced.</span></span> <span data-ttu-id="c1625-121">Komponenterna läggs upp i fönstret **Serviceartikelkomponent lista**.</span><span class="sxs-lookup"><span data-stu-id="c1625-121">These components are set up in the **Service Item Component List** window.</span></span> <span data-ttu-id="c1625-122">Om du vill skapa komponenter för serviceartiklar som är strukturer kan du låta kopiera strukturartiklarna automatiskt och skapa dem som serviceartikelkomponenter.</span><span class="sxs-lookup"><span data-stu-id="c1625-122">Additionally, if you want to set up components for service items that are BOMs, you can copy the BOM items and create them as service item components.</span></span>

1. <span data-ttu-id="c1625-123">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Serviceartiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c1625-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="c1625-124">Öppna serviceartikeln som du vill skapa komponenter för.</span><span class="sxs-lookup"><span data-stu-id="c1625-124">Open the service item for which you want to set up components.</span></span>  
3. <span data-ttu-id="c1625-125">Välj åtgärden **Komponenter**.</span><span class="sxs-lookup"><span data-stu-id="c1625-125">Choose the **Components** action.</span></span> <span data-ttu-id="c1625-126">Fönstret **Serviceartikelkomponent lista** öppnas.</span><span class="sxs-lookup"><span data-stu-id="c1625-126">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="c1625-127">Lägg till en ny komponent.</span><span class="sxs-lookup"><span data-stu-id="c1625-127">Add a new component.</span></span>  
5. <span data-ttu-id="c1625-128">I fältet **Typ** väljer du **Serviceartikel** om själva komponenten är en registrerad serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="c1625-128">In the **Type** field, choose **Service Item** if the component itself is a registered service item.</span></span> <span data-ttu-id="c1625-129">Välj annars **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="c1625-129">Otherwise, select **Item**.</span></span>  
6. <span data-ttu-id="c1625-130">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="c1625-130">In the **No.**</span></span> <span data-ttu-id="c1625-131">väljer du den artikel eller serviceartikel som utgör en serviceartikelkomponent.</span><span class="sxs-lookup"><span data-stu-id="c1625-131">field, choose the item or service item that is a component of the service item.</span></span>  

## <a name="to-set-up-service-item-components-from-a-bom"></a><span data-ttu-id="c1625-132">Så här ställer du in serviceartikelkomponenter från en struktur</span><span class="sxs-lookup"><span data-stu-id="c1625-132">To set up service item components from a BOM</span></span>
1.  <span data-ttu-id="c1625-133">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Serviceartiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c1625-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c1625-134">Öppna den serviceartikel som du vill skapa komponenter från en struktur för.</span><span class="sxs-lookup"><span data-stu-id="c1625-134">Open the service item for which you want to set up components from a BOM.</span></span>  
3. <span data-ttu-id="c1625-135">Välj åtgärden **Komponenter**.</span><span class="sxs-lookup"><span data-stu-id="c1625-135">Choose the **Components** action.</span></span> <span data-ttu-id="c1625-136">Fönstret **Serviceartikelkomponent lista** öppnas.</span><span class="sxs-lookup"><span data-stu-id="c1625-136">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="c1625-137">Välj fältet **Kopiera från struktur**</span><span class="sxs-lookup"><span data-stu-id="c1625-137">Choose the **Copy from BOM** action.</span></span>  

    <span data-ttu-id="c1625-138">Om artikeln som serviceartikeln är kopplad till är en struktur skapas automatiskt komponenter för alla artiklarna i strukturen.</span><span class="sxs-lookup"><span data-stu-id="c1625-138">If the item that the service item is linked to is a BOM, the components for all the items in the BOM are created automatically.</span></span>  

## <a name="to-set-up-a-service-shelf"></a><span data-ttu-id="c1625-139">Så här skapar du en servicehylla</span><span class="sxs-lookup"><span data-stu-id="c1625-139">To set up a service shelf</span></span>
<span data-ttu-id="c1625-140">Du kan lägga upp servicehyllor som hjälper till att identifiera där du lagrar dina serviceartiklar.</span><span class="sxs-lookup"><span data-stu-id="c1625-140">You can set up service shelves that identify where you store your service items.</span></span> <span data-ttu-id="c1625-141">Du tilldelar servicehyllor till serviceartiklar i fönstret **Tjänsteorder** och i fönstret **Serviceartikel arbetsblad**.</span><span class="sxs-lookup"><span data-stu-id="c1625-141">You assign service shelves to service items on the **Service Order** and **Service Item Worksheet** windows.</span></span>  

1. <span data-ttu-id="c1625-142">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Servicehyllor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c1625-142">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Shelves**, and then choose the related link.</span></span>
2. <span data-ttu-id="c1625-143">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="c1625-143">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1625-144">Se även</span><span class="sxs-lookup"><span data-stu-id="c1625-144">See Also</span></span>
<span data-ttu-id="c1625-145">[Skapa koder för standardtjänst](service-how-setup-service-coding.md) </span><span class="sxs-lookup"><span data-stu-id="c1625-145">[Set Up Codes for Standard Services](service-how-setup-service-coding.md) </span></span>  
[<span data-ttu-id="c1625-146">Ställa in felsökning</span><span class="sxs-lookup"><span data-stu-id="c1625-146">Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md)

