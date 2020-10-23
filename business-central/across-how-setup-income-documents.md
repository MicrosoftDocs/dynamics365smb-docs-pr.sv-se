---
title: Konfigurera Inkommande dokument | Microsoft Docs
description: Du kan använda funktionen inkommande dokument för att skapa elektroniska dokument, hantera OCR-uppgifter, importera fakturor och konvertera bildfiler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0be6c730664d5162bd2359e029f9a387eae0d5d8
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915916"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="dc74c-103">Ställa in inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="dc74c-103">Set Up Incoming Documents</span></span>

<span data-ttu-id="dc74c-104">Om du skapar redovisningsjournalrader från inkommande dokumentposter måste du ange vilken journalmall och batch som ska användas på sidan **Inställning av inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="dc74c-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="dc74c-105">Om du inte vill att användare ska skapa fakturor eller redovisningsjournalrader från inkommande dokumentposter såvida inte dokumenten har godkänts först, måste du konfigurera godkännare för arbetsflöde.</span><span class="sxs-lookup"><span data-stu-id="dc74c-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="dc74c-106">För att omvandla PDF- och bildfiler till elektroniska dokument som du kan konverteras till, till exempel,inköpsfakturor inne i "[!INCLUDE[d365fin](includes/d365fin_md.md)]" måste du först konfigurera OCR-funktionen och aktivera tjänsten.</span><span class="sxs-lookup"><span data-stu-id="dc74c-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span> <span data-ttu-id="dc74c-107">Välj ett servicepaket som passar din organisation och/eller ditt land/din region.</span><span class="sxs-lookup"><span data-stu-id="dc74c-107">Choose a service package that is appropriate for your organization and/or country/region.</span></span> <span data-ttu-id="dc74c-108">Du kan också skapa transaktioner manuellt för att visa de externa dokumenten.</span><span class="sxs-lookup"><span data-stu-id="dc74c-108">Alternatively, you can create entries manually to represent the external documents.</span></span>  

<span data-ttu-id="dc74c-109">När funktionen för Inkommande dokument är inställd, kan du använda olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i .</span><span class="sxs-lookup"><span data-stu-id="dc74c-109">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="dc74c-110">De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="dc74c-110">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="dc74c-111">Mer information finns i [Bearbeta inkommande dokument](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="dc74c-111">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="dc74c-112">Så här konfigurerar du funktionen för inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="dc74c-112">To set up the Incoming Documents feature</span></span>

1. <span data-ttu-id="dc74c-113">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inkommande dokumentkonfiguration** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dc74c-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="dc74c-114">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="dc74c-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="dc74c-115">Som en del av inställningen måste du bestämma om du vill kräva godkännande av inkommande dokument.</span><span class="sxs-lookup"><span data-stu-id="dc74c-115">As part of the setup, you must decide if you want to require approval of incoming documents.</span></span> <span data-ttu-id="dc74c-116">Om du vill kräva godkännande måste du ställa in godkännare och arbetsflöde för godkännande.</span><span class="sxs-lookup"><span data-stu-id="dc74c-116">To require approval, you must set up approvers and approval workflows.</span></span> <span data-ttu-id="dc74c-117">Om organisationen inte avser att kräva godkännande kan du hoppa över nästa avsnitt.</span><span class="sxs-lookup"><span data-stu-id="dc74c-117">If your organization does not intend to require approval, you can skip the next section.</span></span>  

<span data-ttu-id="dc74c-118">Slutligen, om du använder en tjänst för att konvertera PDF- eller bildfiler som representerar inkommande dokument, måste du installera det.</span><span class="sxs-lookup"><span data-stu-id="dc74c-118">Finally, you if you use a service to convert PDF or image files representing incoming documents, you must it set up.</span></span> <span data-ttu-id="dc74c-119">Annars kan du hoppa över avsnittet.</span><span class="sxs-lookup"><span data-stu-id="dc74c-119">Otherwise, you can also skip that section.</span></span>  

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="dc74c-120">Så här konfigurerar du godkännare för inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="dc74c-120">To set up approvers of incoming document records</span></span>

<span data-ttu-id="dc74c-121">Om du vill kan du ställa in en godkännandeprocedur för inkommande dokument.</span><span class="sxs-lookup"><span data-stu-id="dc74c-121">Optionally, set up an approval process for the incoming documents.</span></span> <span data-ttu-id="dc74c-122">Godkännare för inkommande dokument måste skapas som användare av arbetsflöde för godkännande.</span><span class="sxs-lookup"><span data-stu-id="dc74c-122">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="dc74c-123">Innan du kan skapa arbetsflöden som innehåller godkännandesteg, måste du skapa arbetsflödeanvändare som är inblandade i godkännandeprocessen.</span><span class="sxs-lookup"><span data-stu-id="dc74c-123">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="dc74c-124">På sidan **Användarinställningar för godkännande** anger du även beloppsgränser för vissa typer av förfrågningar och definierar ersättande godkännare som godkännandebegäran kan delegeras till när den ursprungliga godkännaren är frånvarande.</span><span class="sxs-lookup"><span data-stu-id="dc74c-124">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="dc74c-125">Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="dc74c-125">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="dc74c-126">Så här konfigurerar du en OCR-tjänst</span><span class="sxs-lookup"><span data-stu-id="dc74c-126">To set up an OCR service</span></span>

1. <span data-ttu-id="dc74c-127">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för OCR-tjänst** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dc74c-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="dc74c-128">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="dc74c-128">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="dc74c-129">Dina inloggningsdata krypteras automatiskt.</span><span class="sxs-lookup"><span data-stu-id="dc74c-129">You login data is automatically encrypted.</span></span>

<span data-ttu-id="dc74c-130">Mer information finns i [Använda OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md).</span><span class="sxs-lookup"><span data-stu-id="dc74c-130">For more information, see [Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="dc74c-131">Se även</span><span class="sxs-lookup"><span data-stu-id="dc74c-131">See Also</span></span>

[<span data-ttu-id="dc74c-132">Bearbeta inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="dc74c-132">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="dc74c-133">Inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="dc74c-133">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="dc74c-134">Inköp</span><span class="sxs-lookup"><span data-stu-id="dc74c-134">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="dc74c-135">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dc74c-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
