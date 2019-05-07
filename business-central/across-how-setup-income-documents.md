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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7e99f4b33767a1bdea7b942d1b183edbacc829ac
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "932747"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="1c079-103">Ställa in inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="1c079-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="1c079-104">Om du skapar redovisningsjournalrader från inkommande dokumentposter måste du ange vilken journalmall och batch som ska användas på sidan **Inställning av inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="1c079-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="1c079-105">Om du inte vill att användare ska skapa fakturor eller redovisningsjournalrader från inkommande dokumentposter om inte dokumenten har godkänts först, måste du konfigurera godkännare på sidan **Godkännare för inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="1c079-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers on the **Incoming Document Approvers** page.</span></span>

<span data-ttu-id="1c079-106">För att omvandla PDF- och bildfiler till elektroniska dokument som du kan konverteras till, till exempel,inköpsfakturor inne i "[!INCLUDE[d365fin](includes/d365fin_md.md)]" måste du först konfigurera OCR-funktionen och aktivera tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1c079-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="1c079-107">När funktionen för Inkommande dokument är inställd, kan du använda olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i .</span><span class="sxs-lookup"><span data-stu-id="1c079-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="1c079-108">De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="1c079-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="1c079-109">Mer information finns i [Bearbeta inkommande dokument](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="1c079-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="1c079-110">Så här konfigurerar du funktionen för inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="1c079-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="1c079-111">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inställning av inkommande dokument** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1c079-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="1c079-112">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="1c079-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="1c079-113">Så här konfigurerar du godkännare för inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="1c079-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="1c079-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inställning av inkommande dokument** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1c079-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1c079-115">På sidan **Inställning av inkommande dokument** väljer du åtgärden **Godkännare**.</span><span class="sxs-lookup"><span data-stu-id="1c079-115">On the **Incoming Documents Setup** page, choose the **Approvers** action.</span></span>

    <span data-ttu-id="1c079-116">Sidan **Godkännare för inkommande dokument** visar alla användare som är inställda i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1c079-116">The **Incoming Document Approvers** page shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="1c079-117">Markera en eller flera användare som kan godkänna ett inkommande dokument, innan en relaterat dokumentet eller journalrad kan skapas.</span><span class="sxs-lookup"><span data-stu-id="1c079-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="1c079-118">När godkännare har konfigurerats på sidan **Godkännare för inkommande dokument** kan endast dessa användare godkänna ett inkommande dokument om kryssrutan **Kräv godkännande för att skapa** på sidan **Inställning av inkommande dokument** är markerad.</span><span class="sxs-lookup"><span data-stu-id="1c079-118">When approvers have been set up on the **Incoming Document Approvers** page, only those users can approve an incoming document if the **Require Approval To Create** check box on the **Incoming Documents Setup** page is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="1c079-119">Denna inställning av godkännande är inte relaterad till arbetsflöden för godkännande.</span><span class="sxs-lookup"><span data-stu-id="1c079-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="1c079-120">Mer information finns i [Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="1c079-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="1c079-121">Så här konfigurerar du en OCR-tjänst</span><span class="sxs-lookup"><span data-stu-id="1c079-121">To set up an OCR service</span></span>
1. <span data-ttu-id="1c079-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **OCR-serviceinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1c079-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="1c079-123">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="1c079-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="1c079-124">Dina inloggningsdata krypteras automatiskt.</span><span class="sxs-lookup"><span data-stu-id="1c079-124">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c079-125">Se även</span><span class="sxs-lookup"><span data-stu-id="1c079-125">See Also</span></span>
[<span data-ttu-id="1c079-126">Bearbeta inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="1c079-126">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="1c079-127">Inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="1c079-127">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="1c079-128">Inköp</span><span class="sxs-lookup"><span data-stu-id="1c079-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="1c079-129">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1c079-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
