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
ms.date: 06/23/2020
ms.author: sgroespe
ms.openlocfilehash: 09047315c701bd2076f59b6c3f4840ba95eb06cc
ms.sourcegitcommit: 63102669366eb26f9c32729848170bc2e5c4d6ae
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503550"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="79720-103">Ställa in inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="79720-103">Set Up Incoming Documents</span></span>

<span data-ttu-id="79720-104">Om du skapar redovisningsjournalrader från inkommande dokumentposter måste du ange vilken journalmall och batch som ska användas på sidan **Inställning av inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="79720-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="79720-105">Om du inte vill att användare ska skapa fakturor eller redovisningsjournalrader från inkommande dokumentposter såvida inte dokumenten har godkänts först, måste du konfigurera godkännare för arbetsflöde.</span><span class="sxs-lookup"><span data-stu-id="79720-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="79720-106">För att omvandla PDF- och bildfiler till elektroniska dokument som du kan konverteras till, till exempel,inköpsfakturor inne i "[!INCLUDE[d365fin](includes/d365fin_md.md)]" måste du först konfigurera OCR-funktionen och aktivera tjänsten.</span><span class="sxs-lookup"><span data-stu-id="79720-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="79720-107">När funktionen för Inkommande dokument är inställd, kan du använda olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i .</span><span class="sxs-lookup"><span data-stu-id="79720-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="79720-108">De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="79720-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="79720-109">Mer information finns i [Bearbeta inkommande dokument](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="79720-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="79720-110">Så här konfigurerar du funktionen för inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="79720-110">To set up the Incoming Documents feature</span></span>

1. <span data-ttu-id="79720-111">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inkommande dokumentkonfiguration** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="79720-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="79720-112">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="79720-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="79720-113">Som en del av inställningen måste du bestämma om du vill kräva godkännande av inkommande dokument.</span><span class="sxs-lookup"><span data-stu-id="79720-113">As part of the setup, you must decide if you want to require approval of incoming documents.</span></span> <span data-ttu-id="79720-114">Om du vill kräva godkännande måste du ställa in godkännare och arbetsflöde för godkännande.</span><span class="sxs-lookup"><span data-stu-id="79720-114">To require approval, you must set up approvers and approval workflows.</span></span> <span data-ttu-id="79720-115">Om organisationen inte avser att kräva godkännande kan du hoppa över nästa avsnitt.</span><span class="sxs-lookup"><span data-stu-id="79720-115">If your organization does not intend to require approval, you can skip the next section.</span></span>  

<span data-ttu-id="79720-116">Slutligen, om du använder en tjänst för att konvertera PDF- eller bildfiler som representerar inkommande dokument, måste du installera det.</span><span class="sxs-lookup"><span data-stu-id="79720-116">Finally, you if you use a service to convert PDF or image files representing incoming documents, you must it set up.</span></span> <span data-ttu-id="79720-117">Annars kan du hoppa över avsnittet.</span><span class="sxs-lookup"><span data-stu-id="79720-117">Otherwise, you can also skip that section.</span></span>  

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="79720-118">Så här konfigurerar du godkännare för inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="79720-118">To set up approvers of incoming document records</span></span>

<span data-ttu-id="79720-119">Godkännare för inkommande dokument måste skapas som användare av arbetsflöde för godkännande.</span><span class="sxs-lookup"><span data-stu-id="79720-119">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="79720-120">Innan du kan skapa arbetsflöden som innehåller godkännandesteg, måste du skapa arbetsflödeanvändare som är inblandade i godkännandeprocessen.</span><span class="sxs-lookup"><span data-stu-id="79720-120">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="79720-121">På sidan **Användarinställningar för godkännande** anger du även beloppsgränser för vissa typer av förfrågningar och definierar ersättande godkännare som godkännandebegäran kan delegeras till när den ursprungliga godkännaren är frånvarande.</span><span class="sxs-lookup"><span data-stu-id="79720-121">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="79720-122">Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="79720-122">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="79720-123">Så här konfigurerar du en OCR-tjänst</span><span class="sxs-lookup"><span data-stu-id="79720-123">To set up an OCR service</span></span>

1. <span data-ttu-id="79720-124">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för OCR-tjänst** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="79720-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="79720-125">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="79720-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="79720-126">Dina inloggningsdata krypteras automatiskt.</span><span class="sxs-lookup"><span data-stu-id="79720-126">You login data is automatically encrypted.</span></span>

<span data-ttu-id="79720-127">Mer information finns i [Använda OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md).</span><span class="sxs-lookup"><span data-stu-id="79720-127">For more information, see [Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="79720-128">Se även</span><span class="sxs-lookup"><span data-stu-id="79720-128">See Also</span></span>

[<span data-ttu-id="79720-129">Bearbeta inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="79720-129">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="79720-130">Inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="79720-130">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="79720-131">Inköp</span><span class="sxs-lookup"><span data-stu-id="79720-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="79720-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="79720-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
