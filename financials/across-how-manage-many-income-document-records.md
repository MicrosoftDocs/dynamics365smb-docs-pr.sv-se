---
title: Definiera vilka inkommande dokument Se | Microsoft Docs
description: "Ändra standardläge för inkommande dokument, till exempel e-fakturor, förbättra din översikt över bearbetade och obearbetade poster."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d840981dcceb54c74ac70ed0ddd05b3d3fa9bfc8
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-manage-many-incoming-document-records"></a><span data-ttu-id="a4117-103">Så här hanterar du många inkommande dokumentposter</span><span class="sxs-lookup"><span data-stu-id="a4117-103">How to: Manage Many Incoming Document Records</span></span>
<span data-ttu-id="a4117-104">När du skapar eller bearbetar inkommande dokumentposter, kan antalet rader i fönstret **Inkommande dokument** växa till en utsträckning att du förlorar översikt.</span><span class="sxs-lookup"><span data-stu-id="a4117-104">As you create or process incoming document records, the number of lines in the **Incoming Documents** window may grow to an extent where you lose overview.</span></span> <span data-ttu-id="a4117-105">Därför kan du ange inkommande dokumentposter som Bearbetade för att ta bort dem från standardvyn.</span><span class="sxs-lookup"><span data-stu-id="a4117-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="a4117-106">När du väljer åtgärden **Visa alla** kan du visa både behandlats och outredda transaktioner.</span><span class="sxs-lookup"><span data-stu-id="a4117-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="a4117-107">Du kan inte redigera information, koppla filer eller utföra andra processer på inkommande dokumentposter som har angetts till Bearbetad.</span><span class="sxs-lookup"><span data-stu-id="a4117-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="a4117-108">Du måste först ange den till Obearbetad.</span><span class="sxs-lookup"><span data-stu-id="a4117-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="a4117-109">Kryssrutan **Bearbetad** markeras automatiskt för inkommande dokumentposter som har bearbetats, men du kan även markera eller avmarkera kryssrutan manuellt.</span><span class="sxs-lookup"><span data-stu-id="a4117-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="a4117-110">Beroende på företagets rutiner kan en inkommande dokumentpost bearbetas när ett lagerrelaterat dokument har skapats för det, eller när en fil har bifogats.</span><span class="sxs-lookup"><span data-stu-id="a4117-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="a4117-111">När du öppnar fönstret **Inkommande dokument** med åtgärden **Mina inkommande dokument** i rollcentret, kommer endast obearbetade inkommande dokumentposter visas som standard.</span><span class="sxs-lookup"><span data-stu-id="a4117-111">When you open the **Incoming Documents** window with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="a4117-112">Detta kallas i detta ämne för"standardvyn".</span><span class="sxs-lookup"><span data-stu-id="a4117-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="a4117-113">Så här tar du bort inkommande dokumentposter från standardvyn</span><span class="sxs-lookup"><span data-stu-id="a4117-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="a4117-114">I fönstret **Inkommande dokument** markerar du en eller flera rader för inkommande dokumentposter som du vill ta bort från standardvyn.</span><span class="sxs-lookup"><span data-stu-id="a4117-114">In the **Incoming Documents** window, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="a4117-115">Välj åtgärden **Ange som bearbetad**.</span><span class="sxs-lookup"><span data-stu-id="a4117-115">Choose the **Set to Processed** action.</span></span>

<span data-ttu-id="a4117-116">De inkommande dokumentposterna tas bort från standardvyn och kryssrutan **Bearbetad** markeras på raderna.</span><span class="sxs-lookup"><span data-stu-id="a4117-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="a4117-117">Du kan också utföra den preliminära för den individuella transaktionen i fönstret **inkommande dokumentkort**.</span><span class="sxs-lookup"><span data-stu-id="a4117-117">You can also perform this action for the individual record in the **Incoming Document Card** window.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="a4117-118">Så här visar du inkommande dokumentposter</span><span class="sxs-lookup"><span data-stu-id="a4117-118">To view all incoming document records</span></span>
1. <span data-ttu-id="a4117-119">I fönstret **Inkommande dokument** väljer du åtgärden **Visa alla**.</span><span class="sxs-lookup"><span data-stu-id="a4117-119">In the **Incoming Documents** window, choose the **Show All** action.</span></span>

<span data-ttu-id="a4117-120">Alla inkommande dokumentposter visas inklusive de som inte har kryssrutan **Behandlad** markerad.</span><span class="sxs-lookup"><span data-stu-id="a4117-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="a4117-121">Så här lägger du till inkommande dokumentposter till standardvyn</span><span class="sxs-lookup"><span data-stu-id="a4117-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="a4117-122">I fönstret **Inkommande dokument** väljer du åtgärden **Visa alla**.</span><span class="sxs-lookup"><span data-stu-id="a4117-122">In the **Incoming Documents** window, choose the **Show All** action.</span></span>
2. <span data-ttu-id="a4117-123">Markera en eller flera rader för inkommande dokumentposter som du vill ska visas i standardvyn.</span><span class="sxs-lookup"><span data-stu-id="a4117-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="a4117-124">Välj åtgärden **Ange som obearbetad**.</span><span class="sxs-lookup"><span data-stu-id="a4117-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="a4117-125">Du kan också utföra den preliminära för den individuella transaktionen i fönstret **inkommande dokumentkort**.</span><span class="sxs-lookup"><span data-stu-id="a4117-125">You can also perform this action for the individual record in the **Incoming Document Card** window.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4117-126">Se även</span><span class="sxs-lookup"><span data-stu-id="a4117-126">See Also</span></span>
[<span data-ttu-id="a4117-127">Bearbeta inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="a4117-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="a4117-128">Inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="a4117-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="a4117-129">Inköp</span><span class="sxs-lookup"><span data-stu-id="a4117-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a4117-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a4117-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

