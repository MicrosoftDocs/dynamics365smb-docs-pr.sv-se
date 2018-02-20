---
title: "Sök efter dokument utan bilagor | Microsoft Docs"
Description: You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.
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
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c355657821f5f4d18c707d296d9607cf5ec60442
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="8a682-102">Söka efter bokförda dokument utan inkommande dokumentposter</span><span class="sxs-lookup"><span data-stu-id="8a682-102">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="8a682-103">Från fönstren **Kontoplan** och **Redovisningstransaktioner** kan du använda en sökfunktion för att hitta redovisningsposter för bokförda inköps- och försäljningsdokument som inte har inkommande dokumentposter, och sedan länka dem till centralt befintliga poster eller skapa nya med bifogade dokumentfiler.</span><span class="sxs-lookup"><span data-stu-id="8a682-103">From the **Chart of Accounts** and **General Ledger Entries** windows, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="8a682-104">Söka efter bokförda dokument utan inkommande dokumentposter</span><span class="sxs-lookup"><span data-stu-id="8a682-104">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="8a682-105">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kontoplan** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8a682-105">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="8a682-106">Välj en rad för ett redovisningskonto för vilka redovisningstransaktioner du vill se bokförda inköps- och försäljningsdokument utan inkommande dokumentpost och välj sedan **Bokförda dokument utan inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="8a682-106">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="8a682-107">Välj alternativt åtgärden **Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="8a682-107">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="8a682-108">I fönstret **Redovisningstransaktioner** väljer du åtgärden **Bokförda dokument utan inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="8a682-108">In the **General Ledger Entries** window, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="8a682-109">Fönstret **Dokförda dokument utan inkommande dokument** öppnas med visning av bokförda inköps- och försäljningsdokument utan inkommande dokumentposter som representeras av redovisningstransaktioner på det redovisningskonto som du öppnade fönstret för.</span><span class="sxs-lookup"><span data-stu-id="8a682-109">The **Posted Documents without Incoming Document** window opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the window for.</span></span> <span data-ttu-id="8a682-110">Fönstret kan innehålla högst 1000 rader.</span><span class="sxs-lookup"><span data-stu-id="8a682-110">The window can show a maximum of 1000 lines.</span></span> <span data-ttu-id="8a682-111">Som standard innehåller fältet **Datumfilter** därför ett filter som begränsar raderna till poster med bokföringsdatum från början av bokföringsperioden till arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="8a682-111">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="8a682-112">Koppla hittade dokument till befintliga inkommande dokumentposter</span><span class="sxs-lookup"><span data-stu-id="8a682-112">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="8a682-113">I fönstret **Bokförda dokument utan inkommande dokument** väljer du raden för ett bokfört dokument som du vill koppla till en befintlig inkommande dokumentpost och väljer sedan åtgärden **Välj inkommande dokument**.</span><span class="sxs-lookup"><span data-stu-id="8a682-113">In the **Posted Documents without Incoming Document** window, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="8a682-114">I fönstret **Inkommande dokument** väljer du den inkommande dokumentpost som du vill koppla till det hittade bokförda dokumentet och klickar sedan på knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a682-114">In the **Incoming Documents** window, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="8a682-115">Nu är den valda inkommande dokumentposten kopplad till det bokförda dokumentet i fönstret **Bokförda dokument utan inkommande dokument**, som du kan se i faktaboxen **Inkommande dokumentfiler**.</span><span class="sxs-lookup"><span data-stu-id="8a682-115">In the **Posted Documents without Incoming Document** window, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="8a682-116">Om en relevant inkommande dokumentpost inte finns i fönstret **Inkommande dokument** kan du skapa den.</span><span class="sxs-lookup"><span data-stu-id="8a682-116">If a relevant incoming document record does not exist in the **Incoming Documents** window, then you can create it.</span></span> <span data-ttu-id="8a682-117">Mer information finns i [Så här skapar du inkommande dokumentposter](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="8a682-117">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8a682-118">Se även</span><span class="sxs-lookup"><span data-stu-id="8a682-118">See Also</span></span>
[<span data-ttu-id="8a682-119">Bearbeta inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="8a682-119">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="8a682-120">Inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="8a682-120">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="8a682-121">Inköp</span><span class="sxs-lookup"><span data-stu-id="8a682-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8a682-122">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8a682-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

