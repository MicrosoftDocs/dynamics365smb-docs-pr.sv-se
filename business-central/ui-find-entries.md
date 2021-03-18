---
title: Hitta transaktioner | Microsoft Docs
description: I den här artikeln beskrivs dokument och transaktioner relaterar till varandra
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 437e0c076b664ad35d5819783e98d9e91abee982
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393980"
---
# <a name="finding-related-entries-for-posted-documents"></a><span data-ttu-id="6ab5b-103">Hitta relaterade transaktioner för bokförda dokument</span><span class="sxs-lookup"><span data-stu-id="6ab5b-103">Finding Related Entries for Posted Documents</span></span> 

<span data-ttu-id="6ab5b-104">I den här artikeln får du lära dig att söka efter dokument och transaktioner som är relaterade till varandra baserat på en gemensam information, t. ex.:</span><span class="sxs-lookup"><span data-stu-id="6ab5b-104">In this article, you learn how to find documents and entries that are related to each other based on a common information, like:</span></span>

- <span data-ttu-id="6ab5b-105">Verifikationsnummer eller bokföringsdatum</span><span class="sxs-lookup"><span data-stu-id="6ab5b-105">Document number or posting date</span></span>
- <span data-ttu-id="6ab5b-106">Typ av företagskontakt, nummer eller externt dokumentnummer</span><span class="sxs-lookup"><span data-stu-id="6ab5b-106">Business contact type, number, or external document number</span></span>
- <span data-ttu-id="6ab5b-107">Artikelns serienummer eller partinummer</span><span class="sxs-lookup"><span data-stu-id="6ab5b-107">Item serial number or lot number</span></span>

<span data-ttu-id="6ab5b-108">Funktionen är användbar för att hitta redovisningstransaktionerna som har skapats som ett resultat av vissa transaktioner.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-108">This feature is useful for finding the ledger entries that resulted from certain transactions.</span></span> <span data-ttu-id="6ab5b-109">När du söker efter verifikationsnummer kan du skriva ut sammanfattningen i rapporten Dokumentposter.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-109">When you search by document number, you can print the summary from the Document Entries report.</span></span>

## <a name="get-started"></a><span data-ttu-id="6ab5b-110">Kom igång</span><span class="sxs-lookup"><span data-stu-id="6ab5b-110">Get started</span></span>

<span data-ttu-id="6ab5b-111">Funktionen Hitta transaktioner är tillgänglig på de flesta sidor som innehåller bokförda dokument eller bokförda dokumenttransaktioner – för både listor och kort.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-111">The find entries feature is readily available on most pages that display posted documents or posted documents entries - for both lists and cards.</span></span> <span data-ttu-id="6ab5b-112">Det första steget är att öppna en av de här sidorna.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-112">So the first step is open one of these pages.</span></span> <span data-ttu-id="6ab5b-113">Välj sedan antingen åtgärden **Hitta transaktioner** eller tryck på Alt + G.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-113">Then, either choose the **Find Entries** action or press the Alt+G keys.</span></span>

<span data-ttu-id="6ab5b-114">På sidan **Hitta transaktioner** finns alla relaterade dokument och transaktioner baserade på dokumentnr och bokföringsdatum.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-114">The **Find Entries** page  includes all related documents and entries based on the document no. and posting date.</span></span> <span data-ttu-id="6ab5b-115">Sidan är uppdelad i tre delar:</span><span class="sxs-lookup"><span data-stu-id="6ab5b-115">The page is divided into three sections:</span></span>

- <span data-ttu-id="6ab5b-116">I det övre avsnittet visas fält och åtgärder som du använder för att filtrera sökningen.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-116">The top section displays fields and actions that you use for filtering your search.</span></span>
- <span data-ttu-id="6ab5b-117">I mitten-avsnittet visas relaterade dokument baserat på sökningen.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-117">The middle section displays related documents based on the search.</span></span>
- <span data-ttu-id="6ab5b-118">I den nedre delen visas information om källdokumentet som hittades vid sökning.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-118">The bottom section displays information about the source document that was found by searching.</span></span>


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a><span data-ttu-id="6ab5b-119">Söka efter transaktioner</span><span class="sxs-lookup"><span data-stu-id="6ab5b-119">Search for entries</span></span>

<span data-ttu-id="6ab5b-120">Du kan söka efter transaktioner som bygger på information om antingen dokument, affärskontakt eller artikel.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-120">You can search for entries based on information about either the document, business contact, or item reference.</span></span> <span data-ttu-id="6ab5b-121">Om du vill ändra sökningen väljer du **Åtgärder**, **Sök efter** och sedan en av följande åtgärder:</span><span class="sxs-lookup"><span data-stu-id="6ab5b-121">To change the search, select **Actions**, **Find By**, then one of the following actions:</span></span>

|<span data-ttu-id="6ab5b-122">Åtgärd</span><span class="sxs-lookup"><span data-stu-id="6ab5b-122">Action</span></span>|<span data-ttu-id="6ab5b-123">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="6ab5b-123">Description</span></span>|
|------|-----------|
|<span data-ttu-id="6ab5b-124">Sök efter dokument</span><span class="sxs-lookup"><span data-stu-id="6ab5b-124">Find by Document</span></span>|<span data-ttu-id="6ab5b-125">Visa transaktioner baserat på ett visst verifikationsnummer eller bokföringsdatum.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-125">View entries based on a specific document number or posting date.</span></span>|
|<span data-ttu-id="6ab5b-126">Affärskontakt</span><span class="sxs-lookup"><span data-stu-id="6ab5b-126">Business Contact</span></span> |<span data-ttu-id="6ab5b-127">Visa transaktioner baserat på en viss kontakttyp, ett visst kontaktnummer och/eller externt dokumentnummer.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-127">View entries based on a specific contact type, contact number, anr/or external document number.</span></span> <span data-ttu-id="6ab5b-128">Du kan ange dokumentinformation som tilldelats av en leverantör eller en kund.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-128">You can enter document information that was assigned by a vendor or a customer.</span></span> <span data-ttu-id="6ab5b-129">Använd de tillgängliga fälten för att söka efter leverantörsdokument genom att använda numren som leverantören tilldelade dokumenten.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-129">Use the available fields to search for vendor documents by using the numbers that the vendor has assigned the documents.</span></span>|
|<span data-ttu-id="6ab5b-130">Artikelreferens</span><span class="sxs-lookup"><span data-stu-id="6ab5b-130">Item reference</span></span>|<span data-ttu-id="6ab5b-131">Visa transaktioner baserat på ett serienummer eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-131">View entires based on a serial number or lot number.</span></span> <span data-ttu-id="6ab5b-132">Du kan ange partinumret eller serienumret, eller ett filter för det parti- eller serienummer som du vill söka efter.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-132">You can enter the lot number or serial number, or filter on the lot number or serial number that you want to search for.</span></span> <span data-ttu-id="6ab5b-133">Denna åtgärd är användbar när du vill veta var ett specifikt artikelspårningsnummer har använts, vilken leverantör det kom ifrån eller till vilken kund det såldes.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-133">This action is useful to see where a specific item tracking number was used, what vendor it came from, or what customer it was sold to.</span></span>|

<span data-ttu-id="6ab5b-134">När du har gjort ett val anger du relevant sökningsinformation i fälten längst upp.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-134">After you make a selection, enter the relevant search information in the fields at the top.</span></span> <span data-ttu-id="6ab5b-135">Använd knappbeskrivningarna i fälten för att få hjälp.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-135">Use the tooltips on the fields to help.</span></span> <span data-ttu-id="6ab5b-136">När du är klar väljer du **Sök** för att starta sökningen.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-136">When you're finished, choose **Find** to start the search.</span></span> <span data-ttu-id="6ab5b-137">Om du ändrar något av filtren, måste du välja **Sök** igen.</span><span class="sxs-lookup"><span data-stu-id="6ab5b-137">If you change any of the filters, you have to choose **Find** again.</span></span>

> [!TIP]
> <span data-ttu-id="6ab5b-138">Ett par exempel på hur du använder **Hitta transaktioner** finns i [Spåra artikel-spårade artiklar](inventory-how-to-trace-item-tracked-items.md) och [Genomgång: spåra serie-/partinummer](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="6ab5b-138">For a couple examples about using **Find Entries**, see [Trace Item-Tracked Items](inventory-how-to-trace-item-tracked-items.md) and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="6ab5b-139">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="6ab5b-139">See Related Training at [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="6ab5b-140">Se även</span><span class="sxs-lookup"><span data-stu-id="6ab5b-140">See Also</span></span>

[<span data-ttu-id="6ab5b-141">Arbeta med Business Central</span><span class="sxs-lookup"><span data-stu-id="6ab5b-141">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="6ab5b-142">Lägga till en sidåtgärd i ditt rollcenter</span><span class="sxs-lookup"><span data-stu-id="6ab5b-142">Add a Page Action to Your Role Center</span></span>](ui-bookmarks.md)  
[<span data-ttu-id="6ab5b-143">Spåra artiklar med artikelspårning</span><span class="sxs-lookup"><span data-stu-id="6ab5b-143">Trace Item-Tracked Items</span></span>](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]