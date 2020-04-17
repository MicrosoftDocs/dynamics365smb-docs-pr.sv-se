---
title: Sök efter dokument utan bilagor | Microsoft Docs
Description: Du kan söka efter redovisningstransaktioner för bokförda inköps- och försäljningsdokument som inte har inkommande elektroniska dokument, till exempel importerade fakturor.
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
ms.openlocfilehash: 0b31d225083d566967b3c9cb7facee564c3d3466
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188546"
---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="d6cf5-103">Söka efter bokförda dokument utan inkommande dokumentposter</span><span class="sxs-lookup"><span data-stu-id="d6cf5-103">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="d6cf5-104">Från sidorna **Kontoplan** och **Redovisningstransaktioner** kan du använda en sökfunktion för att hitta redovisningsposter för bokförda inköps- och försäljningsdokument som inte har inkommande dokumentposter, och sedan länka dem till centralt befintliga poster eller skapa nya med bifogade dokumentfiler.</span><span class="sxs-lookup"><span data-stu-id="d6cf5-104">From the **Chart of Accounts** and **General Ledger Entries** pages, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="d6cf5-105">Söka efter bokförda dokument utan inkommande dokumentposter</span><span class="sxs-lookup"><span data-stu-id="d6cf5-105">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="d6cf5-106">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kontoplan** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="d6cf5-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="d6cf5-107">Välj en rad för ett redovisningskonto för vilka redovisningstransaktioner du vill se bokförda inköps- och försäljningsdokument utan inkommande dokumentpost och välj sedan **Bokförda dokument utan inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="d6cf5-107">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="d6cf5-108">Välj alternativt åtgärden **Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="d6cf5-108">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="d6cf5-109">På sidan **Redovisningstransaktioner** väljer du åtgärden **Bokförda dokument utan inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="d6cf5-109">On the **General Ledger Entries** page, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="d6cf5-110">Sidan **Dokförda dokument utan inkommande dokument** öppnas med visning av bokförda inköps- och försäljningsdokument utan inkommande dokumentposter som representeras av redovisningstransaktioner på det redovisningskonto som du öppnade sidan för.</span><span class="sxs-lookup"><span data-stu-id="d6cf5-110">The **Posted Documents without Incoming Document** page opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the page for.</span></span> <span data-ttu-id="d6cf5-111">Sidan kan innehålla högst 1000 rader.</span><span class="sxs-lookup"><span data-stu-id="d6cf5-111">The page can show a maximum of 1000 lines.</span></span> <span data-ttu-id="d6cf5-112">Som standard innehåller fältet **Datumfilter** därför ett filter som begränsar raderna till poster med bokföringsdatum från början av bokföringsperioden till arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="d6cf5-112">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="d6cf5-113">Koppla hittade dokument till befintliga inkommande dokumentposter</span><span class="sxs-lookup"><span data-stu-id="d6cf5-113">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="d6cf5-114">På sidan **Bokförda dokument utan inkommande dokument** väljer du raden för ett bokfört dokument som du vill koppla till en befintlig inkommande dokumentpost och väljer sedan åtgärden **Välj inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="d6cf5-114">On the **Posted Documents without Incoming Document** page, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="d6cf5-115">På sidan **Inkommande dokument** väljer du den inkommande dokumentpost som du vill koppla till det hittade bokförda dokumentet och klickar sedan på knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6cf5-115">On the **Incoming Documents** page, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="d6cf5-116">Nu är den valda inkommande dokumentposten kopplad till det bokförda dokumentet på sidan **Bokförda dokument utan inkommande dokument**, som du kan se i faktaboxen **Inkommande dokumentfiler**.</span><span class="sxs-lookup"><span data-stu-id="d6cf5-116">On the **Posted Documents without Incoming Document** page, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="d6cf5-117">Om en relevant inkommande dokumentpost inte finns på sidan **Inkommande dokument** kan du skapa den.</span><span class="sxs-lookup"><span data-stu-id="d6cf5-117">If a relevant incoming document record does not exist on the **Incoming Documents** page, then you can create it.</span></span> <span data-ttu-id="d6cf5-118">Mer information finns i [Så här skapar du inkommande dokumentposter](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="d6cf5-118">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d6cf5-119">Se även</span><span class="sxs-lookup"><span data-stu-id="d6cf5-119">See Also</span></span>
[<span data-ttu-id="d6cf5-120">Bearbeta inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="d6cf5-120">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="d6cf5-121">Inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="d6cf5-121">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="d6cf5-122">Inköp</span><span class="sxs-lookup"><span data-stu-id="d6cf5-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="d6cf5-123">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d6cf5-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
