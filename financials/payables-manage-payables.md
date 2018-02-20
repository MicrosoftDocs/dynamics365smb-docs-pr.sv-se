---
title: "Översikt över uppgifter för hantering av leverantörsskulder | Microsoft Docs"
description: "Innehåller information om hur du hanterar leverantörsreskontra, till exempel betala fordringsägare eller koppla utgående betalningar till transaktioner för att stänga fakturor eller kreditnotor."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: d59c00f7a00854639250ae587805dece50fd1d78
ms.contentlocale: sv-se
ms.lasthandoff: 02/02/2018

---
# <a name="managing-payables"></a><span data-ttu-id="10451-103">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="10451-103">Managing Payables</span></span>
<span data-ttu-id="10451-104">En stor del av hanteringen av leverantörsskulder betalar dina leverantörer eller återbetalar dina anställda för utgifter.</span><span class="sxs-lookup"><span data-stu-id="10451-104">A big part of managing accounts payable is paying your vendors, or reimbursing your employees for expenses.</span></span> <span data-ttu-id="10451-105">Du kan använda funktioner för att lägga till betalningsrder för inköpsfakturor som förfaller till betalning i fönstret **Betalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="10451-105">You can use functions to add payments lines for purchase invoices that are due in the **Payment Journal** window.</span></span> <span data-ttu-id="10451-106">För att skicka transaktioner till din bank kan du exportera flera betalningsjournalrader till en fil och sedan överför du filen till din bank.</span><span class="sxs-lookup"><span data-stu-id="10451-106">To send transactions to your bank, you can export multiple payment journal lines to a file, and then upload the file to your bank.</span></span> <span data-ttu-id="10451-107">Du kan också göra betalningar med check som inkluderar att överföra checkar som elektronisk betalning.</span><span class="sxs-lookup"><span data-stu-id="10451-107">You can also make payments by check, including transmitting checks as electronic payments.</span></span>

<span data-ttu-id="10451-108">En annan typisk aktivitet är att koppla utgående betalningar till deras relaterade leverantörers eller anställdas transaktioner för att avsluta de inköpsfakturor, inköpskreditnotor eller anställdas konton som betalda.</span><span class="sxs-lookup"><span data-stu-id="10451-108">Another typical task is to apply outgoing payments to their related vendor or employee ledger entries in order to close purchase invoices, purchase credit memos, or employee accounts as paid.</span></span> <span data-ttu-id="10451-109">Du kan göra detta i fönstret **Betalningsavstämningsjournal** genom att importera ett kontoutdrag för att snabbt registrera utbetalningarna.</span><span class="sxs-lookup"><span data-stu-id="10451-109">You can do this in the **Payment Reconciliation Journal** window by importing a bank statement file to register the payments.</span></span> <span data-ttu-id="10451-110">Betalningarna används för att öppna leverantörs-, kund- eller anställdas transaktioner genom att matcha betalningstexten och transaktionsinformation.</span><span class="sxs-lookup"><span data-stu-id="10451-110">The payments are applied to open vendor, customer, or employee ledger entries by matching payment text and entry information.</span></span> <span data-ttu-id="10451-111">Det finns olika sätt att visa och ändra matchningarna innan du bokför journalen.</span><span class="sxs-lookup"><span data-stu-id="10451-111">There are various ways to review and change the matches before you post the journal.</span></span> <span data-ttu-id="10451-112">Du kan välja att avsluta alla öppna bankkontotransaktioner som relateras till kopplade transaktioner, när du bokför journalen.</span><span class="sxs-lookup"><span data-stu-id="10451-112">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="10451-113">Bankkontot avstäms automatiskt, när alla utbetalningar kopplas.</span><span class="sxs-lookup"><span data-stu-id="10451-113">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="10451-114">Du kan också koppla utgående betalningar manuellt i fönstret **Betalningsjournal** eller från relaterade leverantörers eller anställdas transaktioner.</span><span class="sxs-lookup"><span data-stu-id="10451-114">Alternatively, you can apply outgoing payments manually in the **Payment Journal** window or from the related vendor or employee ledger entries.</span></span>

<span data-ttu-id="10451-115">I följande tabell beskrivs en serie uppgifter inom Leverantörsskulder med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="10451-115">The following table describes a sequence of tasks within accounts payable, with links to the topics that describe them.</span></span>

| <span data-ttu-id="10451-116">Om du vill</span><span class="sxs-lookup"><span data-stu-id="10451-116">To</span></span> | <span data-ttu-id="10451-117">Gå till</span><span class="sxs-lookup"><span data-stu-id="10451-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="10451-118">Generera förfallna leverantörsbetalningar eller återbetalningar till anställda, förbereda checkbetalningar och exportera betalningar till en bankfil när du bokför.</span><span class="sxs-lookup"><span data-stu-id="10451-118">Generate due vendor payments or employee reimbursements, prepare check payments, and export payments to a bank file when posting.</span></span> |[<span data-ttu-id="10451-119">Göra betalningar</span><span class="sxs-lookup"><span data-stu-id="10451-119">Making Payments</span></span>](payables-make-payments.md) |
| <span data-ttu-id="10451-120">Koppla leverantörsbetalningar automatiskt till obetalda inköpsfakturor, genom att importera bankutdragsfil.</span><span class="sxs-lookup"><span data-stu-id="10451-120">Apply vendor payments automatically to unpaid purchase invoices by importing a bank statement file.</span></span> |[<span data-ttu-id="10451-121">Koppla utbetalningar automatiskt och stämma av bankkonton</span><span class="sxs-lookup"><span data-stu-id="10451-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="10451-122">Koppla leverantörsbetalningar till obetalda inköpsfakturor manuellt.</span><span class="sxs-lookup"><span data-stu-id="10451-122">Apply vendor payments to unpaid purchase invoices manually.</span></span> |[<span data-ttu-id="10451-123">Stämma av leverantörsbetalningar manuellt</span><span class="sxs-lookup"><span data-stu-id="10451-123">Reconcile Vendor Payments Manually</span></span>](payables-how-apply-purchase-transactions-manually.md) |
|<span data-ttu-id="10451-124">Säkerställa korrekt värdering av lager genom att tilldela extra artikelkostnader, som till exempel frakt, fysisk hantering, försäkring och transport som förekommer vid inköp.</span><span class="sxs-lookup"><span data-stu-id="10451-124">Ensure correct inventory valuation by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing.</span></span>|[<span data-ttu-id="10451-125">Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader</span><span class="sxs-lookup"><span data-stu-id="10451-125">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|

## <a name="see-also"></a><span data-ttu-id="10451-126">Se även</span><span class="sxs-lookup"><span data-stu-id="10451-126">See Also</span></span>
[<span data-ttu-id="10451-127">Inköp</span><span class="sxs-lookup"><span data-stu-id="10451-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="10451-128">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="10451-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="10451-129">Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader</span><span class="sxs-lookup"><span data-stu-id="10451-129">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)  
[<span data-ttu-id="10451-130">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="10451-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="10451-131">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="10451-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

