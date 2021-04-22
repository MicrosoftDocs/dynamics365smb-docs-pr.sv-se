---
title: Konfiguration serviceartiklar och serviceartikelkomponenter | Microsoft Docs
description: Mer information om saker som du måste ställa in innan du kan använda serviceartiklar, inklusive standardvärden, till exempel svarstid, kontraktrabatt i procent och serviceprisgrupp.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ed02fb95e2f700f1cc5083472b668f49fab7d916
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775381"
---
# <a name="set-up-service-items-and-service-item-components"></a><span data-ttu-id="28d16-103">Ställa in tjänsteartiklar och tjänsteartikelkomponenter</span><span class="sxs-lookup"><span data-stu-id="28d16-103">Set Up Service Items and Service Item Components</span></span>
<span data-ttu-id="28d16-104">Om du vill arbeta med serviceartiklar måste du ställa in följande</span><span class="sxs-lookup"><span data-stu-id="28d16-104">To work with service items, you must set up the following</span></span>

* <span data-ttu-id="28d16-105">Serviceartikelgrupper</span><span class="sxs-lookup"><span data-stu-id="28d16-105">Service item groups.</span></span>
* <span data-ttu-id="28d16-106">Valfritt</span><span class="sxs-lookup"><span data-stu-id="28d16-106">Optional</span></span>

## <a name="to-set-up-service-item-groups"></a><span data-ttu-id="28d16-107">Så här skapar du serviceartikelgrupper:</span><span class="sxs-lookup"><span data-stu-id="28d16-107">To set up service item groups</span></span>
<span data-ttu-id="28d16-108">Du anger grupper med artiklar som hör ihop med avseende på reparation och underhåll.</span><span class="sxs-lookup"><span data-stu-id="28d16-108">You can set up groups of items that are related in terms of repair and maintenance.</span></span> <span data-ttu-id="28d16-109">Du kan ange standardvärden för serviceartiklar i serviceartikelgruppen, t. ex. svarstid, kontraktrabatt i procent och serviceprisgrupp.</span><span class="sxs-lookup"><span data-stu-id="28d16-109">You can define default values for service items in a service item group, such as response time, contract discount percent, and service price group.</span></span> <span data-ttu-id="28d16-110">För artiklar i en serviceartikelgrupp kan du välja om du vill att de ska registreras automatiskt som serviceartiklar då de säljs..</span><span class="sxs-lookup"><span data-stu-id="28d16-110">For items in a service item group, you can select whether you want them to be automatically registered as service items when they are sold.</span></span>  

<span data-ttu-id="28d16-111">Du tilldelar serviceartikelgrupper till artiklar på **Artikelkortet** och till serviceartiklar på **serviceartikelkortet**.</span><span class="sxs-lookup"><span data-stu-id="28d16-111">You assign service item groups to items on the **Item** card, and to service items on the **Service Item** card.</span></span>  

1. <span data-ttu-id="28d16-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Serviceartikelgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="28d16-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="28d16-113">Skapa en ny serviceartikelgrupp.</span><span class="sxs-lookup"><span data-stu-id="28d16-113">Create a new service item group.</span></span>  
3. <span data-ttu-id="28d16-114">Fyll i fälten **Kod** och **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="28d16-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="28d16-115">I fältet **Standard kontraktsrabatt %** anger du standardrabatten i procent för kontrakt som du vill att serviceartiklarna i gruppen ska ha.</span><span class="sxs-lookup"><span data-stu-id="28d16-115">In the **Default Contract Discount %** field, enter the default contract discount percentage that you want the service items in the group to have.</span></span>  
5. <span data-ttu-id="28d16-116">I fältet **Standard serviceprisgruppskod** anger du den förvalda serviceprisgruppskoden som du vill att serviceartiklarna i gruppen ska ha.</span><span class="sxs-lookup"><span data-stu-id="28d16-116">In the **Default Serv. Price Group Code** field, enter the default service price group code that you want the service items in the group to have.</span></span>  
6. <span data-ttu-id="28d16-117">I fältet **Standard svarstid (timmar)** anger du standardsvarstiden som du vill att serviceartiklarna i gruppen ska ha, i timmar.</span><span class="sxs-lookup"><span data-stu-id="28d16-117">In the **Default Response Time (Hours)** field, enter the default response time in hours that you want the service items in the group to have.</span></span>  
7. <span data-ttu-id="28d16-118">Om du vill att artiklarna i gruppen ska registreras som serviceartiklar då de säljs, väljer du fältet **Skapa serviceartikel**.</span><span class="sxs-lookup"><span data-stu-id="28d16-118">If you want to register the items in the group as service items when they are sold, select the **Create Service Item** field.</span></span>  

## <a name="to-set-up-service-item-components"></a><span data-ttu-id="28d16-119">Så här ställer du in serviceartikelkomponenter</span><span class="sxs-lookup"><span data-stu-id="28d16-119">To set up service item components</span></span>
<span data-ttu-id="28d16-120">En serviceartikel kan bestå av flera komponenter, som kan ersättas med reservdelar då artikeln är servad.</span><span class="sxs-lookup"><span data-stu-id="28d16-120">A service item can consist of several components, which can be replaced with spare parts when the item is serviced.</span></span> <span data-ttu-id="28d16-121">Komponenterna läggs upp på sidan **Serviceartikelkomponent lista**.</span><span class="sxs-lookup"><span data-stu-id="28d16-121">These components are set up on the **Service Item Component List** page.</span></span> <span data-ttu-id="28d16-122">Om du vill skapa komponenter för serviceartiklar som är strukturer kan du låta kopiera strukturartiklarna automatiskt och skapa dem som serviceartikelkomponenter.</span><span class="sxs-lookup"><span data-stu-id="28d16-122">Additionally, if you want to set up components for service items that are BOMs, you can copy the BOM items and create them as service item components.</span></span>

1. <span data-ttu-id="28d16-123">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **serviceartiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="28d16-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="28d16-124">Öppna serviceartikeln som du vill skapa komponenter för.</span><span class="sxs-lookup"><span data-stu-id="28d16-124">Open the service item for which you want to set up components.</span></span>  
3. <span data-ttu-id="28d16-125">Välj åtgärden **Komponenter**.</span><span class="sxs-lookup"><span data-stu-id="28d16-125">Choose the **Components** action.</span></span> <span data-ttu-id="28d16-126">Sidan **Serviceartikelkomponent lista** öppnas.</span><span class="sxs-lookup"><span data-stu-id="28d16-126">The **Service Item Component List** page opens.</span></span>  
4. <span data-ttu-id="28d16-127">Lägg till en ny komponent.</span><span class="sxs-lookup"><span data-stu-id="28d16-127">Add a new component.</span></span>  
5. <span data-ttu-id="28d16-128">I fältet **Typ** väljer du **Serviceartikel** om själva komponenten är en registrerad serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="28d16-128">In the **Type** field, choose **Service Item** if the component itself is a registered service item.</span></span> <span data-ttu-id="28d16-129">Välj annars **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="28d16-129">Otherwise, select **Item**.</span></span>  
6. <span data-ttu-id="28d16-130">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="28d16-130">In the **No.**</span></span> <span data-ttu-id="28d16-131">väljer du den artikel eller serviceartikel som utgör en serviceartikelkomponent.</span><span class="sxs-lookup"><span data-stu-id="28d16-131">field, choose the item or service item that is a component of the service item.</span></span>  

## <a name="to-set-up-service-item-components-from-a-bom"></a><span data-ttu-id="28d16-132">Så här ställer du in serviceartikelkomponenter från en struktur</span><span class="sxs-lookup"><span data-stu-id="28d16-132">To set up service item components from a BOM</span></span>
1.  <span data-ttu-id="28d16-133">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **serviceartiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="28d16-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="28d16-134">Öppna den serviceartikel som du vill skapa komponenter från en struktur för.</span><span class="sxs-lookup"><span data-stu-id="28d16-134">Open the service item for which you want to set up components from a BOM.</span></span>  
3. <span data-ttu-id="28d16-135">Välj åtgärden **Komponenter**.</span><span class="sxs-lookup"><span data-stu-id="28d16-135">Choose the **Components** action.</span></span> <span data-ttu-id="28d16-136">Sidan **Serviceartikelkomponent lista** öppnas.</span><span class="sxs-lookup"><span data-stu-id="28d16-136">The **Service Item Component List** page opens.</span></span>  
4. <span data-ttu-id="28d16-137">Välj fältet **Kopiera från struktur**</span><span class="sxs-lookup"><span data-stu-id="28d16-137">Choose the **Copy from BOM** action.</span></span>  

    <span data-ttu-id="28d16-138">Om artikeln som serviceartikeln är kopplad till är en struktur skapas automatiskt komponenter för alla artiklarna i strukturen.</span><span class="sxs-lookup"><span data-stu-id="28d16-138">If the item that the service item is linked to is a BOM, the components for all the items in the BOM are created automatically.</span></span>  

## <a name="to-set-up-a-service-shelf"></a><span data-ttu-id="28d16-139">Så här skapar du en servicehylla</span><span class="sxs-lookup"><span data-stu-id="28d16-139">To set up a service shelf</span></span>
<span data-ttu-id="28d16-140">Du kan lägga upp servicehyllor som hjälper till att identifiera där du lagrar dina serviceartiklar.</span><span class="sxs-lookup"><span data-stu-id="28d16-140">You can set up service shelves that identify where you store your service items.</span></span> <span data-ttu-id="28d16-141">Du tilldelar servicehyllor till serviceartiklar på sidan **Tjänsteorder** och i fönstret **Serviceartikel arbetsblad**.</span><span class="sxs-lookup"><span data-stu-id="28d16-141">You assign service shelves to service items on the **Service Order** and **Service Item Worksheet** pages.</span></span>  

1. <span data-ttu-id="28d16-142">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Servicehyllor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="28d16-142">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Shelves**, and then choose the related link.</span></span>
2. <span data-ttu-id="28d16-143">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="28d16-143">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="28d16-144">Se även</span><span class="sxs-lookup"><span data-stu-id="28d16-144">See Also</span></span>
<span data-ttu-id="28d16-145">[Skapa koder för standardtjänst](service-how-setup-service-coding.md) </span><span class="sxs-lookup"><span data-stu-id="28d16-145">[Set Up Codes for Standard Services](service-how-setup-service-coding.md) </span></span>  
[<span data-ttu-id="28d16-146">Ställa in felsökning</span><span class="sxs-lookup"><span data-stu-id="28d16-146">Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]