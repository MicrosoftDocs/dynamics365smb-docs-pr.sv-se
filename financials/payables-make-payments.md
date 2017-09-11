---
title: "Översikt över uppgifter för hantering av betalningar till leverantörer | Microsoft Docs"
description: "Innehåller information om hur du hanterar betalningar till leverantörer och fordringsägare, inklusive bokför betalningsraderna och få en översikt över saldot som förfaller."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a><span data-ttu-id="7dc5b-103">Gör utbetalningar</span><span class="sxs-lookup"><span data-stu-id="7dc5b-103">Make Payments</span></span>
<span data-ttu-id="7dc5b-104">När du gör betalningar till leverantörer, bokför du relaterade betalningsraderna i fönstret **Betalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-104">When you make payments to vendors, you post the related payment lines in the **Payment Journal** window.</span></span> <span data-ttu-id="7dc5b-105">Du kan använda funktionen **Betalningsförslag för lev.** för att söka efter betalningar som förfaller till betalning.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-105">You can use the **Suggest Vendor Payments** function to find payments that are due.</span></span> <span data-ttu-id="7dc5b-106">Du kan även använda rapporten **Lev.saldo - ålderssammandrag** för att få en översikt över betalningar som förfaller till betalning.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-106">You can also use the **Vendor - Summary Aging** report to get an overview of due payments.</span></span>

<span data-ttu-id="7dc5b-107">Från utbetalningsjournalen kan du skriva ut datorcheckar eller registrera när checkar skrivs.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-107">From the payment journal, you can print computer checks or record when checks are written.</span></span> <span data-ttu-id="7dc5b-108">När **Datorcheck** har valts i fältet **Bankbetalningstyp** i utbetalningsjournalen måste alla rader som representerar checkarna skrivas ut innan betalningsjournalen kan bokföras.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-108">If you select **Computer Check** in the **Bank Payment Type** field, then any lines representing checks must be printed before the payment journal can be posted.</span></span>

<span data-ttu-id="7dc5b-109">När du bokför betalningar, exporterar du dem till en bank-fil för överföring till din bank för bearbetning.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-109">When the payments are posted, you can export them to a bank file for upload to your bank for processing.</span></span>

<span data-ttu-id="7dc5b-110">När betalningarna har utförts på din bank, måste du koppla dem till deras tillhörande öppna leverantörsreskontratransaktioner.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-110">After the payments are made at your bank, you must apply them to their related open vendor ledger entries.</span></span> <span data-ttu-id="7dc5b-111">Du kan göra detta manuellt eller genom att importera en bankutdragsfil och att koppla betalningarna automatiskt.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-111">You can do this manually or by importing a bank statement file and applying the payments automatically.</span></span> <span data-ttu-id="7dc5b-112">Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="7dc5b-112">For more information, see [Apply Payments Automatically and Reconcile Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

<span data-ttu-id="7dc5b-113">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="7dc5b-114">Om du vill</span><span class="sxs-lookup"><span data-stu-id="7dc5b-114">To</span></span> | <span data-ttu-id="7dc5b-115">Gå till</span><span class="sxs-lookup"><span data-stu-id="7dc5b-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="7dc5b-116">Använd en funktion för att föreslå leverantörsbetalningar enligt valda kriterier, till exempel förfallodatum, rabattvalbarhet och din likviditeten.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-116">Use a function to suggest vendor payments according to selected criteria, such as due date, discount eligibility, and your liquidity.</span></span> |[<span data-ttu-id="7dc5b-117">Så här använder du betalningsförslag för leverantörer</span><span class="sxs-lookup"><span data-stu-id="7dc5b-117">How to: Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md) |
| <span data-ttu-id="7dc5b-118">Utfärda checkar för utbetalningar, antingen som utskrifter eller som datorcheckar.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-118">Issue checks for payments, either as print-outs or as computer checks.</span></span> <span data-ttu-id="7dc5b-119">Makulera checkar, före eller efter bokföring.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-119">Void checks before or after posting.</span></span> |[<span data-ttu-id="7dc5b-120">Så här arbetar du med checkar</span><span class="sxs-lookup"><span data-stu-id="7dc5b-120">How to: Work with Checks</span></span>](payables-how-work-checks.md) |
| <span data-ttu-id="7dc5b-121">Se till att banken bara godkänner validerade checkar och belopp genom att skicka en fil som innehåller information om leverantör, check ch betalning.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-121">Make sure that your bank only clears validated checks and amounts by sending them a file that contains vendor, check, and payment information.</span></span> |[<span data-ttu-id="7dc5b-122">Så här exporterar du en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="7dc5b-122">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md) |
|<span data-ttu-id="7dc5b-123">Exportera betalningar från fönstret **Betalningsjournal** till en bankfil som du skickar till din bank för bearbetning, inklusive EFT (elektronisk överföring) i Nordamerika.</span><span class="sxs-lookup"><span data-stu-id="7dc5b-123">Export payments from the **Payment Journal** window to a bank file that you upload to your bank for processing, including EFT (electronic funds transfer) in North America.</span></span> |[<span data-ttu-id="7dc5b-124">Så här exporterar du betalningar till en bankfil</span><span class="sxs-lookup"><span data-stu-id="7dc5b-124">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a><span data-ttu-id="7dc5b-125">Se även</span><span class="sxs-lookup"><span data-stu-id="7dc5b-125">See Also</span></span>
[<span data-ttu-id="7dc5b-126">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="7dc5b-126">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="7dc5b-127">Inköp</span><span class="sxs-lookup"><span data-stu-id="7dc5b-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="7dc5b-128">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="7dc5b-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="7dc5b-129">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7dc5b-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

