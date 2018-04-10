---
title: Hantera bankkonton | Microsoft Docs
description: "Du måste regelbundet stämma av banktransaktioner i Financials med relaterade banktransaktioner i dina bankkonton."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bfc83194a1010e3ac628484952bd0c6b1046481b
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="ed12f-103">Hantera bankkonton</span><span class="sxs-lookup"><span data-stu-id="ed12f-103">Managing Bank Accounts</span></span>
<span data-ttu-id="ed12f-104">Du måste regelbundet stämma av dina banktransaktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)] med de relaterade transaktionerna på dina bankkonton i din bank och sedan bokföra saldot till ditt bankkonto.</span><span class="sxs-lookup"><span data-stu-id="ed12f-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="ed12f-105">Du kan utföra denna aktivitet antingen som en del av bearbetning av betalningarna som representeras på kontoutdraget i **Betalningsavstämningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="ed12f-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="ed12f-106">Eller så kan du utföra aktiviteten separat från betalningsbehandling i fönstret **Bankkontoavstämning** som stöder checktransaktioner.</span><span class="sxs-lookup"><span data-stu-id="ed12f-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window, which supports check ledger entries.</span></span> <span data-ttu-id="ed12f-107">I båda fallen fyller du i fönstren genom att importera kontoutdraget till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ed12f-107">In both cases, you fill in the windows by importing the bank statement into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="ed12f-108">Ibland kan du överföra belopp mellan bankkontot i [!INCLUDE[d365fin](includes/d365fin_md.md)] för att visa överföringar på din bank.</span><span class="sxs-lookup"><span data-stu-id="ed12f-108">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="ed12f-109">Du utför denna aktivitet i fönstret **redovisningsjournal** på olika sätt beroende på pengarnas valuta.</span><span class="sxs-lookup"><span data-stu-id="ed12f-109">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="ed12f-110">Innan du kan hantera bankkonton, måste du registrera varje bankkonto som bankkontokort.</span><span class="sxs-lookup"><span data-stu-id="ed12f-110">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="ed12f-111">Dessutom måste du skapa elektroniska tjänster som du kan använda för kontoutdragsimport-och betalningsfilexport.</span><span class="sxs-lookup"><span data-stu-id="ed12f-111">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="ed12f-112">Mer information finns i [Skapa bankkonton](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="ed12f-112">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="ed12f-113">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="ed12f-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="ed12f-114">Om du vill</span><span class="sxs-lookup"><span data-stu-id="ed12f-114">To</span></span> | <span data-ttu-id="ed12f-115">Gå till</span><span class="sxs-lookup"><span data-stu-id="ed12f-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="ed12f-116">Stämma av bankkonton i samband med betalningsbehandling i fönstret **Betalningsavstämningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="ed12f-116">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="ed12f-117">Koppla utbetalningar automatiskt och stämma av bankkonton</span><span class="sxs-lookup"><span data-stu-id="ed12f-117">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="ed12f-118">Du kan stämma av bankkonton inklusive checktransaktioner som en separat aktivitet i fönstret **Bankkontoavstämning**.</span><span class="sxs-lookup"><span data-stu-id="ed12f-118">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="ed12f-119">Stämma av bankkonton separat</span><span class="sxs-lookup"><span data-stu-id="ed12f-119">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="ed12f-120">bokföra överföringar mellan bankkonton i samma valuta eller olika valutor.</span><span class="sxs-lookup"><span data-stu-id="ed12f-120">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="ed12f-121">Överföra banktillgångar</span><span class="sxs-lookup"><span data-stu-id="ed12f-121">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="ed12f-122">Se även</span><span class="sxs-lookup"><span data-stu-id="ed12f-122">See Also</span></span>
[<span data-ttu-id="ed12f-123">Ställa in bankverksamhet</span><span class="sxs-lookup"><span data-stu-id="ed12f-123">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="ed12f-124">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="ed12f-124">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="ed12f-125">[Hantera Leverantörsreskontra](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="ed12f-125">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="ed12f-126">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ed12f-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ed12f-127">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="ed12f-127">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
