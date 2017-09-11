---
title: Konfigurera Inkommande dokument | Microsoft Docs
description: "Du kan använda funktionen inkommande dokument för att skapa elektroniska dokument, hantera OCR-uppgifter, importera fakturor och konvertera bildfiler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 69cb1037da2f3873ecb9a3f498ce5fadfeabac1d
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-incoming-documents"></a><span data-ttu-id="05540-103">Så här konfigurerar du Inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="05540-103">How to: Set Up Incoming Documents</span></span>
<span data-ttu-id="05540-104">Om du skapar redovisningsjournalrader från inkommande dokumentposter måste du ange vilken journalmall och batch som ska användas i fönstret **Inställning av inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="05540-104">If you create general journal lines from incoming document records, you must specify in the **Incoming Documents Setup** window which journal template and batch to use.</span></span>

<span data-ttu-id="05540-105">Om du inte vill att användare ska skapa fakturor eller redovisningsjournalrader från inkommande dokumentposter om inte dokumenten har godkänts först, måste du konfigurera godkännare i fönstret **Godkännare för inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="05540-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers in the **Incoming Document Approvers** window.</span></span>

<span data-ttu-id="05540-106">För att omvandla PDF- och bildfiler till elektroniska dokument som du kan konverteras till, till exempel,inköpsfakturor inne i "[!INCLUDE[d365fin](includes/d365fin_md.md)]" måste du först konfigurera OCR-funktionen och aktivera tjänsten.</span><span class="sxs-lookup"><span data-stu-id="05540-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="05540-107">När funktionen för Inkommande dokument är inställd, kan du använda olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i .</span><span class="sxs-lookup"><span data-stu-id="05540-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="05540-108">De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="05540-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="05540-109">Mer information finns i [Bearbeta inkommande dokument](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="05540-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="05540-110">Så här konfigurerar du funktionen för inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="05540-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="05540-111">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inställning av Inkommande dokument** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="05540-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="05540-112">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="05540-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="05540-113">Så här konfigurerar du godkännare för inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="05540-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="05540-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inställning av Inkommande dokument** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="05540-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="05540-115">I fönstret **Inställning av inkommande dokument** väljer du åtgärden **Godkännare**.</span><span class="sxs-lookup"><span data-stu-id="05540-115">In the **Incoming Documents Setup** window, choose the **Approvers** action.</span></span>

    <span data-ttu-id="05540-116">Fönstret **Godkännare för inkommande dokument** visar alla användare som är inställda i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="05540-116">The **Incoming Document Approvers** window shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="05540-117">Markera en eller flera användare som kan godkänna ett inkommande dokument, innan en relaterat dokumentet eller journalrad kan skapas.</span><span class="sxs-lookup"><span data-stu-id="05540-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="05540-118">När godkännare har konfigurerats i fönstret **Godkännare för inkommande dokument** kan endast dessa användare godkänna ett inkommande dokument om kryssrutan **Kräv godkännande för att skapa** i fönstret **Inställning av inkommande dokument** är markerad.</span><span class="sxs-lookup"><span data-stu-id="05540-118">When approvers have been set up in the **Incoming Document Approvers** window, only those users can approve an incoming document if the **Require Approval To Create** check box in the **Incoming Documents Setup** window is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="05540-119">Denna inställning av godkännande är inte relaterad till arbetsflöden för godkännande.</span><span class="sxs-lookup"><span data-stu-id="05540-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="05540-120">Mer information finns i [Så här använder du arbetsflöden för godkännande](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="05540-120">For more information, see [How to: Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="05540-121">Så här konfigurerar du en OCR-tjänst</span><span class="sxs-lookup"><span data-stu-id="05540-121">To set up an OCR service</span></span>
1. <span data-ttu-id="05540-122">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **OCR-serviceinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="05540-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="05540-123">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="05540-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a><span data-ttu-id="05540-124">Så här kan du kryptera dina inloggningsuppgifter</span><span class="sxs-lookup"><span data-stu-id="05540-124">To encrypt your login information</span></span>
<span data-ttu-id="05540-125">Du rekommenderas att skydda de inloggningsuppgifter som du anger i fönstret **OCR-serviceinställningar**.</span><span class="sxs-lookup"><span data-stu-id="05540-125">It is recommended that you protect the logon information that you enter in the **OCR Service Setup** window.</span></span> <span data-ttu-id="05540-126">Du kan kryptera data på servern genom att skapa nya eller importera befintliga krypteringsnycklar som aktiverar på serverinstansen med anslutningen till databasen.</span><span class="sxs-lookup"><span data-stu-id="05540-126">You can encrypt data on the server by generating new or importing existing encryption keys that you enable on the server instance that connects to the database.</span></span>

1. <span data-ttu-id="05540-127">I fönstret **OCR-serviceinställningar** väljer du åtgärden **Krypteringshantering**.</span><span class="sxs-lookup"><span data-stu-id="05540-127">In the **OCR Service Setup** window, choose the **Encryption Management** action.</span></span>
2. <span data-ttu-id="05540-128">Aktivera krypteringen av dina data i fönstret **Datakrypteringshantering**.</span><span class="sxs-lookup"><span data-stu-id="05540-128">In the **Data Encryption Management** window, enable encryption of your data.</span></span>

## <a name="see-also"></a><span data-ttu-id="05540-129">Se även</span><span class="sxs-lookup"><span data-stu-id="05540-129">See Also</span></span>
[<span data-ttu-id="05540-130">Bearbeta inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="05540-130">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="05540-131">Inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="05540-131">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="05540-132">Inköp</span><span class="sxs-lookup"><span data-stu-id="05540-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="05540-133">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="05540-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

