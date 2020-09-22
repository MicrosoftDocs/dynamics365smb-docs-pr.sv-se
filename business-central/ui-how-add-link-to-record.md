---
title: Lägg till bifogade filer, länkar och anteckningar på poster | Microsoft Docs
description: Koppla en hyperlänk till ett dokument eller en webbplats till en viss post, till exempel en kund eller ett dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/27/2020
ms.author: edupont
ms.openlocfilehash: 39aae609e588635a07fdc406faa63dd4ced3606d
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3789381"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="17a0c-103">Hantera bifogade filer, länkar och anteckningar på kort och dokument</span><span class="sxs-lookup"><span data-stu-id="17a0c-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="17a0c-104">I faktaboxen för de flesta kort och dokument kan du bifoga filer, lägga till länkar och skriva anteckningar.</span><span class="sxs-lookup"><span data-stu-id="17a0c-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="17a0c-105">För länkar och noteringar kan du också göra det på listsidan genom att först välja den relaterade raden.</span><span class="sxs-lookup"><span data-stu-id="17a0c-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="17a0c-106">Om du vill visa eller ändra dessa kopplade informationstyper måste du först öppna fliken **bifogade filer** i faktaboxen.</span><span class="sxs-lookup"><span data-stu-id="17a0c-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="17a0c-107">Numret bakom flikens rubrik visar hur många bifogade filer, länkar eller anteckningar som finns för kortet eller dokumentet.</span><span class="sxs-lookup"><span data-stu-id="17a0c-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="17a0c-108">Bilagor, länkar och anteckningar förblir kopplade till ett kort eller dokument, till exempel från en pågående försäljningsorder till en bokförd försäljningsfaktura.</span><span class="sxs-lookup"><span data-stu-id="17a0c-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="17a0c-109">Ingen av de bifogade filtyperna skrivs emellertid ut från systemet, till exempel vid utskrift eller vid sparande i fil.</span><span class="sxs-lookup"><span data-stu-id="17a0c-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="17a0c-110">När du delvis levererar och fakturerar en försäljningsorder eller en inköpsorder, kopplas den bifogade filen endast till den slutgiltiga fakturan för ordern.</span><span class="sxs-lookup"><span data-stu-id="17a0c-110">When you partially ship and invoice a sales order or purchase order, the attachment will only be attached to the final invoice of that order.</span></span> <span data-ttu-id="17a0c-111">På samma sätt, när du fakturerar med hjälp av funktionen för uppskov, kopplas den bifogade filen endast till redovisningstransaktionerna för dokumentet, men inte till periodiseringsposter.</span><span class="sxs-lookup"><span data-stu-id="17a0c-111">Likewise, when you invoice using the Deferrals feature, the attachment is only attached to the G/L entries for the document but not for the deferral entries.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="17a0c-112">Så här bifogar du en fil till en inköpsfaktura</span><span class="sxs-lookup"><span data-stu-id="17a0c-112">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="17a0c-113">Du kan bifoga alla typer av filer, som innehåller text, bilder och video, till ett kort eller dokument.</span><span class="sxs-lookup"><span data-stu-id="17a0c-113">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="17a0c-114">Detta är användbart om du t.ex. vill lagra en leverantörs faktura som en PDF-fil på den relaterade inköpsfakturan i [!INCLUDE[d365fin](includes/d365fin_md.md)]i.</span><span class="sxs-lookup"><span data-stu-id="17a0c-114">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="17a0c-115">Filer som bifogas med funktionen inkommande dokument finns inte på fliken **bifogade filer**. Mer information finns i [inkommande dokument](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="17a0c-115">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="17a0c-116">Följande procedur är baserad på en inköpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="17a0c-116">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="17a0c-117">Stegen är liknande för alla andra dokument och kort som stöds.</span><span class="sxs-lookup"><span data-stu-id="17a0c-117">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="17a0c-118">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="17a0c-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="17a0c-119">Öppna försäljningsorder som du vill bifoga en fil till.</span><span class="sxs-lookup"><span data-stu-id="17a0c-119">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="17a0c-120">Öppna fliken **bifogade filer** i faktaboxen.</span><span class="sxs-lookup"><span data-stu-id="17a0c-120">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="17a0c-121">Välj värdet bakom fältet **dokument**, till exempel "0".</span><span class="sxs-lookup"><span data-stu-id="17a0c-121">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="17a0c-122">På sidan **Bifogade dokument** i fältet **bilaga**, välj åtgärden **Välj en fil**.</span><span class="sxs-lookup"><span data-stu-id="17a0c-122">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** action.</span></span>
5. <span data-ttu-id="17a0c-123">Markera en fil varifrån som helst och välj sedan knappen **öppna**.</span><span class="sxs-lookup"><span data-stu-id="17a0c-123">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="17a0c-124">Filen är nu bifogad inköpsfakturan.</span><span class="sxs-lookup"><span data-stu-id="17a0c-124">The file is now attached to the purchase invoice.</span></span>

## <a name="to-view-an-attached-file"></a><span data-ttu-id="17a0c-125">Visa den bifogade filen</span><span class="sxs-lookup"><span data-stu-id="17a0c-125">To view an attached file</span></span>
1. <span data-ttu-id="17a0c-126">Öppna fliken **bifogade filer** i faktaboxen.</span><span class="sxs-lookup"><span data-stu-id="17a0c-126">In the FactBox, open the **Attachments** tab.</span></span>
2. <span data-ttu-id="17a0c-127">Välj värdet bakom fältet **dokument**, till exempel "1".</span><span class="sxs-lookup"><span data-stu-id="17a0c-127">Choose the value behind the **Documents** field, such as "1".</span></span>
3. <span data-ttu-id="17a0c-128">På sidan **Bifogade dokument** väljer du åtgärden **Förhandsgranskning**.</span><span class="sxs-lookup"><span data-stu-id="17a0c-128">On the **Attached Documents** page, choose the **Preview** action.</span></span>
4. <span data-ttu-id="17a0c-129">Öppna den hämtade filen.</span><span class="sxs-lookup"><span data-stu-id="17a0c-129">Open the downloaded file.</span></span>

## <a name="to-save-a-document-as-a-pdf-attachment"></a><span data-ttu-id="17a0c-130">Så här sparar du ett dokument som en bifogad PDF-fil</span><span class="sxs-lookup"><span data-stu-id="17a0c-130">To save a document as a PDF attachment</span></span>
<span data-ttu-id="17a0c-131">När du behöver spara ett dokument som en fil kan du använda åtgärden **Bifoga som PDF** för att överföra det aktuella dokumentinnehållet som en PDF-fil som är kopplad till faktaboxen för dokumentet.</span><span class="sxs-lookup"><span data-stu-id="17a0c-131">Whenever you need to save a document as a file, you can use the **Attach as PDF** action to capture the current document content as a PDF file attached to the FactBox of the document.</span></span> <span data-ttu-id="17a0c-132">Detta är användbart exempelvis när dokument följer flera steg i en procedur, t.ex. ett arbetsflöde för försäljning eller godkännande, och du vill referera till en utskrift av föregående steg.</span><span class="sxs-lookup"><span data-stu-id="17a0c-132">This is useful, for example, when documents follow multiple steps in a process, such as a sales process or an approval workflow, and you want to refer to a printout of the previous step.</span></span>

<span data-ttu-id="17a0c-133">Följande procedur är baserad på en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="17a0c-133">The following procedure is based on a sales order.</span></span> <span data-ttu-id="17a0c-134">Stegen är liknande för samtliga dokument som stöds.</span><span class="sxs-lookup"><span data-stu-id="17a0c-134">The steps are similar for all supported documents.</span></span>

1. <span data-ttu-id="17a0c-135">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="17a0c-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="17a0c-136">Markera en försäljningsorder och välj åtgärden **Bifoga som PDF**.</span><span class="sxs-lookup"><span data-stu-id="17a0c-136">Select a sales order, and then choose the **Attach as PDF** action.</span></span>

<span data-ttu-id="17a0c-137">En PDF-fil med det aktuella innehållet på försäljningsordern läggs till på fliken **Bilagor** i faktaboxen.</span><span class="sxs-lookup"><span data-stu-id="17a0c-137">A PDF file with the current content of the sales order is added to the **Attachments** tab in the FactBox.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="17a0c-138">Att lägga till länk från ett artikelkort</span><span class="sxs-lookup"><span data-stu-id="17a0c-138">To add a link from an item card</span></span>
<span data-ttu-id="17a0c-139">Du kan lägga till en länk från ett kort eller dokument till en URL eller sökväg.</span><span class="sxs-lookup"><span data-stu-id="17a0c-139">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="17a0c-140">Detta är användbart om du t.ex. vill koppla ett artikelkort till leverantörens artikelkatalog.</span><span class="sxs-lookup"><span data-stu-id="17a0c-140">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="17a0c-141">Följande procedur baseras på ett artikelkort.</span><span class="sxs-lookup"><span data-stu-id="17a0c-141">The following procedure is based on an item card.</span></span> <span data-ttu-id="17a0c-142">Stegen är liknande för alla andra kort och dokument.</span><span class="sxs-lookup"><span data-stu-id="17a0c-142">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="17a0c-143">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="17a0c-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="17a0c-144">Välj den artikel som du vill lägga till en länk från och välj sedan fliken **bifogade filer** i faktaboxen.</span><span class="sxs-lookup"><span data-stu-id="17a0c-144">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="17a0c-145">Välj ikonen **länkar**, välj ikonen **+**.</span><span class="sxs-lookup"><span data-stu-id="17a0c-145">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="17a0c-146">I fältet **länkadresser** anger du länken.</span><span class="sxs-lookup"><span data-stu-id="17a0c-146">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="17a0c-147">Länken måste vara en giltig URL för Internet eller intranätet.</span><span class="sxs-lookup"><span data-stu-id="17a0c-147">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="17a0c-148">I fältet **Beskrivning**, ange information om länken.</span><span class="sxs-lookup"><span data-stu-id="17a0c-148">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="17a0c-149">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="17a0c-149">Choose the **OK** button.</span></span>

<span data-ttu-id="17a0c-150">Länken kopplas nu till artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="17a0c-150">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="17a0c-151">Skriva en notering på en försäljningsorder</span><span class="sxs-lookup"><span data-stu-id="17a0c-151">To write a note on a sales order</span></span>
<span data-ttu-id="17a0c-152">Du kan skriva en notering på ett dokument eller kort, t.ex. om du vill skicka särskilda instruktioner till andra användare av dokumentet eller kortet.</span><span class="sxs-lookup"><span data-stu-id="17a0c-152">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="17a0c-153">Du kan ta med fillänkar och URL:er i anteckningar.</span><span class="sxs-lookup"><span data-stu-id="17a0c-153">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="17a0c-154">Anteckningarna på fliken **bifogade filer** är inte relaterade till interna anteckningsfunktioner, som i huvudsak används för att kommunicera mellan arbetsflödesanvändare.</span><span class="sxs-lookup"><span data-stu-id="17a0c-154">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="17a0c-155">Mer information finns i [Ställa in meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="17a0c-155">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="17a0c-156">Följande procedur är baserad på en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="17a0c-156">The following procedure is based on a sales order.</span></span> <span data-ttu-id="17a0c-157">Stegen är liknande för alla andra dokument och kort som stöds.</span><span class="sxs-lookup"><span data-stu-id="17a0c-157">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="17a0c-158">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="17a0c-158">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="17a0c-159">Välj den försäljningsorder som du vill skriva en anteckning på och välj sedan fliken **bifogade filer** i faktaboxen.</span><span class="sxs-lookup"><span data-stu-id="17a0c-159">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="17a0c-160">Välj avsnittet **anteckningar**, välj ikonen **+**.</span><span class="sxs-lookup"><span data-stu-id="17a0c-160">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="17a0c-161">I fältet **Anteckning** skriv någon text, t.ex. "detta är en brådskande order.".</span><span class="sxs-lookup"><span data-stu-id="17a0c-161">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="17a0c-162">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="17a0c-162">Choose the **OK** button.</span></span>

<span data-ttu-id="17a0c-163">Noteringen är nu kopplad till försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="17a0c-163">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="17a0c-164">Se även</span><span class="sxs-lookup"><span data-stu-id="17a0c-164">See Also</span></span>  
<span data-ttu-id="17a0c-165">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="17a0c-165">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="17a0c-166">Inkommande dokument</span><span class="sxs-lookup"><span data-stu-id="17a0c-166">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="17a0c-167">Konfigurera meddelanden för arbetsflödet</span><span class="sxs-lookup"><span data-stu-id="17a0c-167">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
