---
title: Så här skapar du poster för inkommande dokument | Microsoft Docs
description: Du kan skapa poster för inkommande dokument, till exempel e-fakturor och hantera OCR uppgifter, e-handel och dokumentutbyte.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 33ca7a06aa8c903bb6f65af298748417ac460f63
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807200"
---
# <a name="create-incoming-document-records"></a><span data-ttu-id="2da32-103">Skapa inkommande dokumentposter</span><span class="sxs-lookup"><span data-stu-id="2da32-103">Create Incoming Document Records</span></span>
<span data-ttu-id="2da32-104">På sidan **Inkommande dokument** använder du olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i .</span><span class="sxs-lookup"><span data-stu-id="2da32-104">On the **Incoming Documents** page, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="2da32-105">De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="2da32-105">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span>

<span data-ttu-id="2da32-106">Om du vill registrera ett externt dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du först skapa eller slutföra en inkommande dokumentpost.</span><span class="sxs-lookup"><span data-stu-id="2da32-106">To record an external document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first create or complete an incoming document record.</span></span> <span data-ttu-id="2da32-107">Du kan göra detta manuellt eller så kan du ta ett foto på det externa dokumentet och sedan skapa en inkommande dokumentpost med bildfilen bifogad.</span><span class="sxs-lookup"><span data-stu-id="2da32-107">You can do this manually, or you can take a photo of the external document and then create the incoming document record with the image file attached.</span></span>

<span data-ttu-id="2da32-108">Innan du kan använda funktionen för inkommande dokument måste du utföra de nödvändiga inställningarna.</span><span class="sxs-lookup"><span data-stu-id="2da32-108">Before you can use the Incoming Documents feature, you must perform the required setup.</span></span> <span data-ttu-id="2da32-109">Mer information finns i [Skapa inkommande dokument](across-how-setup-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="2da32-109">For more information, see [Set Up Incoming Documents](across-how-setup-income-documents.md).</span></span>

## <a name="to-approve-or-reject-an-incoming-document"></a><span data-ttu-id="2da32-110">Så här Godkänn eller avvisa ett inkommande dokument.</span><span class="sxs-lookup"><span data-stu-id="2da32-110">To approve or reject an incoming document</span></span>
<span data-ttu-id="2da32-111">Om du inte vill att användare ska skapa fakturor eller redovisningsjournalrader från inkommande dokumentposter om inte dokumenten har godkänts först kan du konfigurera godkännare som måste godkänna transaktionerna innan de kan behandlas.</span><span class="sxs-lookup"><span data-stu-id="2da32-111">If you do want to allow users to create invoices or general journal lines from incoming document records unless they are approved, you can set up approvers who must approve the records before they can be processed.</span></span>

1. <span data-ttu-id="2da32-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inkommande dokument** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2da32-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="2da32-113">Markera raden med dokumentet som du vill godkänna eller avvisa, och välj sedan åtgärden **godkänna** eller **avvisa**.</span><span class="sxs-lookup"><span data-stu-id="2da32-113">Select the line with the document that you want to approve or reject, and then choose the **Approve** or **Reject** actions.</span></span>

<span data-ttu-id="2da32-114">Om du godkänner den inkommande dokumentposten markeras kryssrutan **Släppt** på den inkommande dokumentraden.</span><span class="sxs-lookup"><span data-stu-id="2da32-114">If you approve the incoming document record, the **Released** check box on the incoming document line is selected.</span></span> <span data-ttu-id="2da32-115">Användaren som ansvarar för att skapa t.ex inköpsfakturor kan fortsätta med att bearbeta transaktionen.</span><span class="sxs-lookup"><span data-stu-id="2da32-115">The user in charge of creating, for example, purchase invoices can proceed to process the record.</span></span>

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="2da32-116">Så här skapar du en inkommande dokumentpost genom att ta ett foto</span><span class="sxs-lookup"><span data-stu-id="2da32-116">To create an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="2da32-117">Följande proceduren gäller endast [!INCLUDE[d365fin](includes/d365fin_md.md)] för surfplatte- och telefonklienter.</span><span class="sxs-lookup"><span data-stu-id="2da32-117">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="2da32-118">Välj panelen **Skapa inkommande dokument från kamera** i appfältet och gå sedan till steg 4.</span><span class="sxs-lookup"><span data-stu-id="2da32-118">On the app bar, choose the **Create Incoming Document from Camera** tile, and then go to step 4.</span></span>
2. <span data-ttu-id="2da32-119">Välj annars alternativknappen på appfältet, välj **Inkommande dokument** och välj sedan **Alla**.</span><span class="sxs-lookup"><span data-stu-id="2da32-119">Alternatively, on the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
3. <span data-ttu-id="2da32-120">På sidan **Inkommande dokument** väljer du ellipsknappen och sedan **Skapa från kamera**.</span><span class="sxs-lookup"><span data-stu-id="2da32-120">On the **Incoming Documents** page, choose the ellipsis button, and then choose **Create from Camera**.</span></span> <span data-ttu-id="2da32-121">Kameran på Tablet PC:n eller telefonen aktiveras.</span><span class="sxs-lookup"><span data-stu-id="2da32-121">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="2da32-122">Ta ett foto av ett dokument, t.ex. ett inköpskvitto, som du vill bearbeta som ett inkommande dokument, och välj sedan knappen **OK** .</span><span class="sxs-lookup"><span data-stu-id="2da32-122">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="2da32-123">En ny inkommande dokumentpost skapas med bilden bifogad.</span><span class="sxs-lookup"><span data-stu-id="2da32-123">A new incoming document record is created, with the image attached.</span></span>

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="2da32-124">Så här bifogar du en bild till en inkommande dokumentpost genom att ta ett foto</span><span class="sxs-lookup"><span data-stu-id="2da32-124">To attach an image to an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="2da32-125">Följande proceduren gäller endast [!INCLUDE[d365fin](includes/d365fin_md.md)] för surfplatte- och telefonklienter.</span><span class="sxs-lookup"><span data-stu-id="2da32-125">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="2da32-126">Välj alternativknappen på appfältet, välj **Inkommande dokument** och välj sedan **Alla**.</span><span class="sxs-lookup"><span data-stu-id="2da32-126">On the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
2. <span data-ttu-id="2da32-127">Öppna kortet för en befintlig inkommande dokumentpost.</span><span class="sxs-lookup"><span data-stu-id="2da32-127">Open the card for an existing incoming document record.</span></span>
3. <span data-ttu-id="2da32-128">På sidan **Inkommande dokument** väljer du ellipsknappen och sedan **Bifoga fil från kamera**.</span><span class="sxs-lookup"><span data-stu-id="2da32-128">On the **Incoming Document** page, choose the ellipsis button, and then choose **Attach Image from Camera**.</span></span> <span data-ttu-id="2da32-129">Kameran på Tablet PC:n eller telefonen aktiveras.</span><span class="sxs-lookup"><span data-stu-id="2da32-129">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="2da32-130">Ta ett foto av ett dokument, t.ex. ett inköpskvitto, som du vill bearbeta som ett inkommande dokument, och välj sedan knappen **OK** .</span><span class="sxs-lookup"><span data-stu-id="2da32-130">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="2da32-131">Bilden har bifogats till den inkommande dokumentposten.</span><span class="sxs-lookup"><span data-stu-id="2da32-131">The image is attached to the incoming document record.</span></span>

## <a name="to-create-an-incoming-document-record-manually"></a><span data-ttu-id="2da32-132">Så här skapar du en inkommande dokumentpost manuellt</span><span class="sxs-lookup"><span data-stu-id="2da32-132">To create an incoming document record manually</span></span>
1. <span data-ttu-id="2da32-133">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inkommande dokument** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2da32-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="2da32-134">Välj åtgärden **Skapa från fil**.</span><span class="sxs-lookup"><span data-stu-id="2da32-134">Choose the **Create from File** action.</span></span>  
3. <span data-ttu-id="2da32-135">Välj en fil och välj sedan **Öppna** på sidan **Infoga fil**.</span><span class="sxs-lookup"><span data-stu-id="2da32-135">On the **Insert File** page, select a file, and then choose **Open**.</span></span> <span data-ttu-id="2da32-136">Filen kopplas automatiskt.</span><span class="sxs-lookup"><span data-stu-id="2da32-136">The file is automatically attached.</span></span>
4. <span data-ttu-id="2da32-137">Välj alternativt åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2da32-137">Alternatively, choose the **New** action.</span></span>
5. <span data-ttu-id="2da32-138">För att bifoga en fil väljer du åtgärden **Bifoga fil**.</span><span class="sxs-lookup"><span data-stu-id="2da32-138">To attach a file, choose the **Attach File** action.</span></span>
6. <span data-ttu-id="2da32-139">Markera filen som representerar det inkommande dokumentet i fråga och välj sedan knappen **Öppna** på sidan **Infoga fil**.</span><span class="sxs-lookup"><span data-stu-id="2da32-139">On the **Insert File** page, select the file that represents the incoming document in question, and then choose the **Open** button.</span></span>
7. <span data-ttu-id="2da32-140">På sidan **Inkommande dokument** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="2da32-140">On the **Incoming Document** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="2da32-141">Se även</span><span class="sxs-lookup"><span data-stu-id="2da32-141">See Also</span></span>
[<span data-ttu-id="2da32-142">Bearbeta inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="2da32-142">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="2da32-143">Inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="2da32-143">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="2da32-144">Inköp</span><span class="sxs-lookup"><span data-stu-id="2da32-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="2da32-145">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2da32-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
