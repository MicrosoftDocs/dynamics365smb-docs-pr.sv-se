---
title: Konfigurera Inkommande dokument | Microsoft Docs
description: Du kan använda funktionen inkommande dokument för att skapa elektroniska dokument, hantera OCR-uppgifter, importera fakturor och konvertera bildfiler.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0a33652ac230e63607957916308ee960d14a2b47
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188474"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="f9f0e-103">Ställa in inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="f9f0e-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="f9f0e-104">Om du skapar redovisningsjournalrader från inkommande dokumentposter måste du ange vilken journalmall och batch som ska användas på sidan **Inställning av inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="f9f0e-105">Om du inte vill att användare ska skapa fakturor eller redovisningsjournalrader från inkommande dokumentposter såvida inte dokumenten har godkänts först, måste du konfigurera godkännare för arbetsflöde.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="f9f0e-106">För att omvandla PDF- och bildfiler till elektroniska dokument som du kan konverteras till, till exempel,inköpsfakturor inne i "[!INCLUDE[d365fin](includes/d365fin_md.md)]" måste du först konfigurera OCR-funktionen och aktivera tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="f9f0e-107">När funktionen för Inkommande dokument är inställd, kan du använda olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i .</span><span class="sxs-lookup"><span data-stu-id="f9f0e-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="f9f0e-108">De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="f9f0e-109">Mer information finns i [Bearbeta inkommande dokument](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="f9f0e-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="f9f0e-110">Så här konfigurerar du funktionen för inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="f9f0e-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="f9f0e-111">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inkommande dokumentkonfiguration** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f9f0e-112">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="f9f0e-113">Så här konfigurerar du godkännare för inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="f9f0e-113">To set up approvers of incoming document records</span></span>
<span data-ttu-id="f9f0e-114">Godkännare för inkommande dokument måste skapas som användare av arbetsflöde för godkännande.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-114">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="f9f0e-115">Innan du kan skapa arbetsflöden som innehåller godkännandesteg, måste du skapa arbetsflödeanvändare som är inblandade i godkännandeprocessen.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-115">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="f9f0e-116">På sidan **Användarinställningar för godkännande** anger du även beloppsgränser för vissa typer av förfrågningar och definierar ersättande godkännare som godkännandebegäran kan delegeras till när den ursprungliga godkännaren är frånvarande.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-116">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="f9f0e-117">Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="f9f0e-117">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="f9f0e-118">Så här konfigurerar du en OCR-tjänst</span><span class="sxs-lookup"><span data-stu-id="f9f0e-118">To set up an OCR service</span></span>
1. <span data-ttu-id="f9f0e-119">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för OCR-tjänst** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f9f0e-120">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="f9f0e-121">Dina inloggningsdata krypteras automatiskt.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-121">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9f0e-122">Se även</span><span class="sxs-lookup"><span data-stu-id="f9f0e-122">See Also</span></span>
[<span data-ttu-id="f9f0e-123">Bearbeta inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="f9f0e-123">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="f9f0e-124">Inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="f9f0e-124">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="f9f0e-125">Inköp</span><span class="sxs-lookup"><span data-stu-id="f9f0e-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f9f0e-126">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f9f0e-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
