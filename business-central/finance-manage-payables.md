---
title: "Hantera leverantörsskulder | Microsoft Docs"
description: "Översikt över hur Financials hjälper dig att hantera leverantörsreskontra (AP), inklusive leverantörsbetalningar fordringsägare, skulder, och förfallen betalning."
services: project-madeira
documentationcenter: 
author: bholtorf
manager: edupont
editor: 
ms.service: dynamics365-business-central
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b128e567a07f4b0a6abffe8f1c82c740317016ff
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="managing-payables"></a><span data-ttu-id="6dc26-103">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="6dc26-103">Managing Payables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6dc26-104"> har vad du behöver för att effektivt hantera leverantörsreskontra.</span><span class="sxs-lookup"><span data-stu-id="6dc26-104"> has what you need to effectively manage accounts payable.</span></span>  

## <a name="payments"></a><span data-ttu-id="6dc26-105">Betalningar</span><span class="sxs-lookup"><span data-stu-id="6dc26-105">Payments</span></span>
<span data-ttu-id="6dc26-106">Det är enkelt att prioritera betalningar, beräkna avgifter för förfallna betalningar och hantera rabatter för tidiga betalningar.</span><span class="sxs-lookup"><span data-stu-id="6dc26-106">It's easy to prioritize payments, account for penalties for overdue payments, and handle discounts for early payments.</span></span>

<span data-ttu-id="6dc26-107">Du kan registrera betalningar i en redovisningsjournal och sedan skriva ut checkar innan utbetalningsjournalen bokförs.</span><span class="sxs-lookup"><span data-stu-id="6dc26-107">You can record payments in a general journal, and then print checks before posting the payment journal.</span></span>

<span data-ttu-id="6dc26-108">Du kan koppla en betalning för att stänga fakturan när du bokför betalningen eller när du har bokfört den.</span><span class="sxs-lookup"><span data-stu-id="6dc26-108">You can apply payments to close invoices when you post the payment, or after you post the payment.</span></span> <span data-ttu-id="6dc26-109">Den **Avräkningsmetod** som anges för leverantören (på **leverantörskortet**) bestämmer om du måste göra en manuell betalning eller om det görs automatiskt.</span><span class="sxs-lookup"><span data-stu-id="6dc26-109">The **Application Method** specified for the vendor (on the **Vendor Card**) determines whether you apply the payment manually, or automatically.</span></span> <span data-ttu-id="6dc26-110">Du kan alltid koppla transaktioner manuellt.</span><span class="sxs-lookup"><span data-stu-id="6dc26-110">You can always apply transactions manually.</span></span> <span data-ttu-id="6dc26-111">Om avräkningsmetoden för leverantören är **Koppla till äldsta faktura** och du inte anger ett dokument som betalningen ska kopplas till, kopplas den emellertid till den äldsta öppna transaktionen för leverantören.</span><span class="sxs-lookup"><span data-stu-id="6dc26-111">However, if the application method for the vendor is **Apply to Oldest**, and you do not specify a document to apply the payment to, the payment is applied to the oldest open entry for the vendor.</span></span>

## <a name="suggest-vendor-payments"></a><span data-ttu-id="6dc26-112">Betalningsförslag för lev.</span><span class="sxs-lookup"><span data-stu-id="6dc26-112">Suggest Vendor Payments</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6dc26-113"> används för att ta fram olika betalningsförslag, t.ex. betalningar som snart förfaller eller betalningar för vilka en rabatt kan erhållas.</span><span class="sxs-lookup"><span data-stu-id="6dc26-113"> can suggest various payments to vendors, such as payments that will be due soon, or payments where a discount is available.</span></span> <span data-ttu-id="6dc26-114">Du kan ange att belopp som specificerats som tillgängliga betalningsmedel och berättigade kassarabatter ska beaktas i betalningsförslaget.</span><span class="sxs-lookup"><span data-stu-id="6dc26-114">The payment suggestion can consider an amount that you specify as available funds for payment, and eligibility for payment discounts.</span></span>

## <a name="issue-checks"></a><span data-ttu-id="6dc26-115">Utfärda checkar</span><span class="sxs-lookup"><span data-stu-id="6dc26-115">Issue Checks</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6dc26-116"> låter dig utfärda checkar till leverantörer elektroniskt och manuellt.</span><span class="sxs-lookup"><span data-stu-id="6dc26-116"> lets you issue checks to vendors manually and electronically.</span></span> <span data-ttu-id="6dc26-117">Du kan utföra båda i fönstret **betalningsjournaler**, där du kan även makulera checkar och granska checktransaktioner.</span><span class="sxs-lookup"><span data-stu-id="6dc26-117">You do both in the **Payment Journals** window, where you can also void checks and view check ledger entries.</span></span>

## <a name="export-payments-to-a-bank-file"></a><span data-ttu-id="6dc26-118">Exportera betalningar till en bankfil</span><span class="sxs-lookup"><span data-stu-id="6dc26-118">Export Payments to a Bank File</span></span>
<span data-ttu-id="6dc26-119">När du är redo att göra betalningar till leverantörer med hjälp av fönstret **Betalningsjournal**, kan du exportera en fil med betalningsinformation från journalraderna.</span><span class="sxs-lookup"><span data-stu-id="6dc26-119">When you are ready to pay a vendor, from the **Payment Journal** window you can export a file with the payment information from the journal lines.</span></span> <span data-ttu-id="6dc26-120">Du kan sedan överföra filen till den elektroniska banken att bearbeta pengaöverföringar.</span><span class="sxs-lookup"><span data-stu-id="6dc26-120">You can then upload the file to your electronic bank to process the money transfers.</span></span>

<span data-ttu-id="6dc26-121">Om du inte vill bokföra en utbetalningsjournalrad för en exporterad betalning, till exempel eftersom du väntar på att banken bekräftar transaktionen, kan du bara ta bort journalraden.</span><span class="sxs-lookup"><span data-stu-id="6dc26-121">If you do not want to post a payment journal line for an exported payment, for example because you are waiting for the bank to confirm the transaction, just delete the journal line.</span></span> <span data-ttu-id="6dc26-122">När du senare skapar en utbetalningsjournal för att betala återstående belopp på fakturan kan du i fältet **Totalt exporterat belopp** se hur mycket av beloppet som redan har exporterats.</span><span class="sxs-lookup"><span data-stu-id="6dc26-122">Later, when you create a payment journal line to pay the remaining amount on the invoice, the **Total Exported Amount** field shows how much of the payment amount has already been exported.</span></span> <span data-ttu-id="6dc26-123">Du kan också söka efter detaljerad information om det exporterade totalbeloppet genom att välja knappen **Transaktioner i kreditöverföringsregister**.</span><span class="sxs-lookup"><span data-stu-id="6dc26-123">Also, you can find detailed information about the exported total by choosing the **Credit Transfer Reg. Entries** button.</span></span>

<span data-ttu-id="6dc26-124">Om du väntar med att bokföra betalningar till när banken bekräftar att transaktionerna har behandlats, finns det två sätt att undvika återexporterande betalningar för öppna dokument av misstag:</span><span class="sxs-lookup"><span data-stu-id="6dc26-124">If you wait to post payments until after your bank confirms that it has processed transactions, there are two ways to avoid accidently re-exporting payments for open documents:</span></span>  

* <span data-ttu-id="6dc26-125">I en utbetalningsjournal med föreslagna betalningsrader kan du sortera på antingen kolumnen **Exporterat till betalningsfil** eller **Totalt exporterat belopp** och sedan ta bort betalningsförslag för öppna fakturor för vilka betalningar som redan har gjorts och du inte vill göra betalningar för.</span><span class="sxs-lookup"><span data-stu-id="6dc26-125">In a payment journal with suggested payment lines, sort on either the **Exported to Payment File** or **Total Exported Amount** columns, and then delete payment suggestions for open invoices for which payments have already been made and you do not want to make payments for.</span></span>

    <span data-ttu-id="6dc26-126">**Obs!** du kan behöva lägga till en kolumn i listan.</span><span class="sxs-lookup"><span data-stu-id="6dc26-126">**Note** You might have to add these columns to the list.</span></span> <span data-ttu-id="6dc26-127">Mer information finns i [Anpassa arbetsytan](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="6dc26-127">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  
* <span data-ttu-id="6dc26-128">Alternativt, på batchjobbet **Betalningsförslag för lev.**, där du anger vilka betalningar som ska inkluderas i utbetalningsjournalen, kan du ange att du inte infogar journalrader för betalningar som redan har exporterats genom att markera kryssrutan **Hoppa över exporterade betalningar**.</span><span class="sxs-lookup"><span data-stu-id="6dc26-128">Alternatively, on the **Suggest Vendor Payments** batch job, where you specify the payments to include in the payment journal, you can specify not to insert journal lines for payments that have already been exported by choosing the **Skip Exported Payments** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="6dc26-129">Se även</span><span class="sxs-lookup"><span data-stu-id="6dc26-129">See Also</span></span>
[<span data-ttu-id="6dc26-130">Betalningssätt</span><span class="sxs-lookup"><span data-stu-id="6dc26-130">Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="6dc26-131">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="6dc26-131">Finance</span></span>](finance.md)  
<span data-ttu-id="6dc26-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6dc26-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
