---
title: Hantera bankkonton | Microsoft Docs
description: Du måste regelbundet stämma av banktransaktioner med relaterade banktransaktioner i dina bankkonton.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 25e1242541e98cc47e2fcc4f016a860ad08c635d
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2019
ms.locfileid: "939135"
---
# <a name="managing-bank-accounts"></a><span data-ttu-id="f18af-103">Hantera bankkonton</span><span class="sxs-lookup"><span data-stu-id="f18af-103">Managing Bank Accounts</span></span>
<span data-ttu-id="f18af-104">Du måste regelbundet stämma av dina banktransaktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)] med de relaterade transaktionerna på dina bankkonton i din bank och sedan bokföra saldot till ditt bankkonto.</span><span class="sxs-lookup"><span data-stu-id="f18af-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="f18af-105">Du kan utföra denna aktivitet antingen som en del av bearbetning av betalningarna som representeras på kontoutdraget i **Betalningsavstämningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="f18af-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="f18af-106">Alternativt kan du utföra åtgärden separat från betalningsbehandlingen på sidan **bankkontoavstämning** där du matchar (synkronisera) bankutdragets rader i den vänstra rutan med dina interna bankkontotransaktioner i den till höger.</span><span class="sxs-lookup"><span data-stu-id="f18af-106">Alternatively, you can perform the task separately from payment processing, on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="f18af-107">På båda sidor kan du fylla i bankutdragsinformationen genom att importera en fil eller mata in och använda automatiskt matchande förslag.</span><span class="sxs-lookup"><span data-stu-id="f18af-107">In both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="f18af-108">I Nordamerika kan du också utföra bankavstämning på sidan **Bank poster kalkylblad** som passar bättre för kontroller och inlåning men inte erbjuder import av bankutdragsfiler.</span><span class="sxs-lookup"><span data-stu-id="f18af-108">In North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="f18af-109">Du använder den här sidan i stället för sidan **bankkontoavstämning**, avmarkera fälten **Bankavstämning med auto. match** på sidan **Redovisningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="f18af-109">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="f18af-110">Mer information finns i avsnittet ”stämma av bankkonton” under Förenta staterna: lokal funktion.</span><span class="sxs-lookup"><span data-stu-id="f18af-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="f18af-111">Ibland kan du överföra belopp mellan bankkontot i [!INCLUDE[d365fin](includes/d365fin_md.md)] för att visa överföringar på din bank.</span><span class="sxs-lookup"><span data-stu-id="f18af-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="f18af-112">Du utför denna aktivitet på sidan **redovisningsjournal** på olika sätt beroende på pengarnas valuta.</span><span class="sxs-lookup"><span data-stu-id="f18af-112">You perform this task on the **General Journal** page, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="f18af-113">Innan du kan hantera bankkonton, måste du registrera varje bankkonto som bankkontokort.</span><span class="sxs-lookup"><span data-stu-id="f18af-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="f18af-114">Dessutom måste du skapa elektroniska tjänster som du kan använda för kontoutdragsimport-och betalningsfilexport.</span><span class="sxs-lookup"><span data-stu-id="f18af-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="f18af-115">Mer information finns i [Skapa bankkonton](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="f18af-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="f18af-116">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="f18af-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="f18af-117">Om du vill</span><span class="sxs-lookup"><span data-stu-id="f18af-117">To</span></span> | <span data-ttu-id="f18af-118">Gå till</span><span class="sxs-lookup"><span data-stu-id="f18af-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="f18af-119">Stämma av bankkonton i samband med betalningsbehandling på sidan **Betalningsavstämningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="f18af-119">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="f18af-120">Koppla utbetalningar automatiskt och stämma av bankkonton</span><span class="sxs-lookup"><span data-stu-id="f18af-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="f18af-121">Du kan stämma av bankkonton inklusive checktransaktioner som en separat aktivitet på sidan **Bankkontoavstämning**.</span><span class="sxs-lookup"><span data-stu-id="f18af-121">Reconcile bank accounts, including check ledger entries, as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="f18af-122">Stämma av bankkonton separat</span><span class="sxs-lookup"><span data-stu-id="f18af-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="f18af-123">bokföra överföringar mellan bankkonton i samma valuta eller olika valutor.</span><span class="sxs-lookup"><span data-stu-id="f18af-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="f18af-124">Överföra banktillgångar</span><span class="sxs-lookup"><span data-stu-id="f18af-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="f18af-125">Se även</span><span class="sxs-lookup"><span data-stu-id="f18af-125">See Also</span></span>
[<span data-ttu-id="f18af-126">Ställa in bankverksamhet</span><span class="sxs-lookup"><span data-stu-id="f18af-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="f18af-127">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="f18af-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="f18af-128">[Hantera Leverantörsreskontra](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="f18af-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="f18af-129">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f18af-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="f18af-130">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="f18af-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
