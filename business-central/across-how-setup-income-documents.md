---
title: Konfigurera Inkommande dokument | Microsoft Docs
description: "Du kan använda funktionen inkommande dokument för att skapa elektroniska dokument, hantera OCR-uppgifter, importera fakturor och konvertera bildfiler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 35911fe862a016546954d6912b3cf12896d23fdd
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="b4b30-103">Ställa in inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="b4b30-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="b4b30-104">Om du skapar redovisningsjournalrader från inkommande dokumentposter måste du ange vilken journalmall och batch som ska användas i fönstret **Inställning av inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="b4b30-104">If you create general journal lines from incoming document records, you must specify in the **Incoming Documents Setup** window which journal template and batch to use.</span></span>

<span data-ttu-id="b4b30-105">Om du inte vill att användare ska skapa fakturor eller redovisningsjournalrader från inkommande dokumentposter om inte dokumenten har godkänts först, måste du konfigurera godkännare i fönstret **Godkännare för inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="b4b30-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers in the **Incoming Document Approvers** window.</span></span>

<span data-ttu-id="b4b30-106">För att omvandla PDF- och bildfiler till elektroniska dokument som du kan konverteras till, till exempel,inköpsfakturor inne i "[!INCLUDE[d365fin](includes/d365fin_md.md)]" måste du först konfigurera OCR-funktionen och aktivera tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b4b30-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="b4b30-107">När funktionen för Inkommande dokument är inställd, kan du använda olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i .</span><span class="sxs-lookup"><span data-stu-id="b4b30-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="b4b30-108">De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="b4b30-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="b4b30-109">Mer information finns i [Bearbeta inkommande dokument](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="b4b30-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="b4b30-110">Så här konfigurerar du funktionen för inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="b4b30-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="b4b30-111">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inställning av inkommande dokument** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b4b30-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="b4b30-112">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="b4b30-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="b4b30-113">Så här konfigurerar du godkännare för inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="b4b30-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="b4b30-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inställning av inkommande dokument** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b4b30-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b4b30-115">I fönstret **Inställning av inkommande dokument** väljer du åtgärden **Godkännare**.</span><span class="sxs-lookup"><span data-stu-id="b4b30-115">In the **Incoming Documents Setup** window, choose the **Approvers** action.</span></span>

    <span data-ttu-id="b4b30-116">Fönstret **Godkännare för inkommande dokument** visar alla användare som är inställda i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b4b30-116">The **Incoming Document Approvers** window shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="b4b30-117">Markera en eller flera användare som kan godkänna ett inkommande dokument, innan en relaterat dokumentet eller journalrad kan skapas.</span><span class="sxs-lookup"><span data-stu-id="b4b30-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="b4b30-118">När godkännare har konfigurerats i fönstret **Godkännare för inkommande dokument** kan endast dessa användare godkänna ett inkommande dokument om kryssrutan **Kräv godkännande för att skapa** i fönstret **Inställning av inkommande dokument** är markerad.</span><span class="sxs-lookup"><span data-stu-id="b4b30-118">When approvers have been set up in the **Incoming Document Approvers** window, only those users can approve an incoming document if the **Require Approval To Create** check box in the **Incoming Documents Setup** window is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b4b30-119">Denna inställning av godkännande är inte relaterad till arbetsflöden för godkännande.</span><span class="sxs-lookup"><span data-stu-id="b4b30-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="b4b30-120">Mer information finns i [Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="b4b30-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="b4b30-121">Så här konfigurerar du en OCR-tjänst</span><span class="sxs-lookup"><span data-stu-id="b4b30-121">To set up an OCR service</span></span>
1. <span data-ttu-id="b4b30-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **OCR-serviceinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b4b30-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="b4b30-123">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="b4b30-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="b4b30-124">Dina inloggningsdata krypteras automatiskt.</span><span class="sxs-lookup"><span data-stu-id="b4b30-124">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4b30-125">Se även</span><span class="sxs-lookup"><span data-stu-id="b4b30-125">See Also</span></span>
[<span data-ttu-id="b4b30-126">Bearbeta inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="b4b30-126">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="b4b30-127">Inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="b4b30-127">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="b4b30-128">Inköp</span><span class="sxs-lookup"><span data-stu-id="b4b30-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="b4b30-129">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b4b30-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

