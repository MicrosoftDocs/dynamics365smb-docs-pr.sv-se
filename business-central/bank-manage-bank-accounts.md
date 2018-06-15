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
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: dd3068cc1af6a16a43f982d3b48cdec42a7d7eca
ms.contentlocale: sv-se
ms.lasthandoff: 05/17/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="96670-103">Hantera bankkonton</span><span class="sxs-lookup"><span data-stu-id="96670-103">Managing Bank Accounts</span></span>
<span data-ttu-id="96670-104">Du måste regelbundet stämma av dina banktransaktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)] med de relaterade transaktionerna på dina bankkonton i din bank och sedan bokföra saldot till ditt bankkonto.</span><span class="sxs-lookup"><span data-stu-id="96670-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="96670-105">Du kan utföra denna aktivitet antingen som en del av bearbetning av betalningarna som representeras på kontoutdraget i **Betalningsavstämningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="96670-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="96670-106">Alternativt kan du utföra åtgärden separat från betalningsbehandlingen i fönstret **bankkontoavstämning** där du matchar (synkronisera) bankutdragets rader i den vänstra rutan med dina interna bankkontotransaktioner i den till höger.</span><span class="sxs-lookup"><span data-stu-id="96670-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="96670-107">I båda fönstren kan du fylla i bankutdragsinformationen genom att importera en fil eller mata in och använda automatiskt matchande förslag.</span><span class="sxs-lookup"><span data-stu-id="96670-107">In both windows, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="96670-108">I Nordamerika kan du också utföra bankavstämning i fönstret **Bank poster kalkylblad** som passar bättre för kontroller och inlåning men inte erbjuder import av bankutdragsfiler.</span><span class="sxs-lookup"><span data-stu-id="96670-108">In North American versions, you can also perform bank reconciliation in the **Bank Rec. Worksheet** window, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="96670-109">Du använder det här fönstret i stället för fönstret **bankkontoavstämning**, avmarkera fälten **Bankavstämning med auto. match** i fönstret **Redovisningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="96670-109">To use this window instead of the **Bank Acc. Reconciliation** window, deselect the **Bank Recon. with Auto. Match** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="96670-110">Mer information finns i avsnittet ”stämma av bankkonton” under Förenta staterna: lokal funktion.</span><span class="sxs-lookup"><span data-stu-id="96670-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="96670-111">Ibland kan du överföra belopp mellan bankkontot i [!INCLUDE[d365fin](includes/d365fin_md.md)] för att visa överföringar på din bank.</span><span class="sxs-lookup"><span data-stu-id="96670-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="96670-112">Du utför denna aktivitet i fönstret **redovisningsjournal** på olika sätt beroende på pengarnas valuta.</span><span class="sxs-lookup"><span data-stu-id="96670-112">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="96670-113">Innan du kan hantera bankkonton, måste du registrera varje bankkonto som bankkontokort.</span><span class="sxs-lookup"><span data-stu-id="96670-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="96670-114">Dessutom måste du skapa elektroniska tjänster som du kan använda för kontoutdragsimport-och betalningsfilexport.</span><span class="sxs-lookup"><span data-stu-id="96670-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="96670-115">Mer information finns i [Skapa bankkonton](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="96670-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="96670-116">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="96670-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="96670-117">Om du vill</span><span class="sxs-lookup"><span data-stu-id="96670-117">To</span></span> | <span data-ttu-id="96670-118">Gå till</span><span class="sxs-lookup"><span data-stu-id="96670-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="96670-119">Stämma av bankkonton i samband med betalningsbehandling i fönstret **Betalningsavstämningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="96670-119">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="96670-120">Koppla utbetalningar automatiskt och stämma av bankkonton</span><span class="sxs-lookup"><span data-stu-id="96670-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="96670-121">Du kan stämma av bankkonton inklusive checktransaktioner som en separat aktivitet i fönstret **Bankkontoavstämning**.</span><span class="sxs-lookup"><span data-stu-id="96670-121">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="96670-122">Stämma av bankkonton separat</span><span class="sxs-lookup"><span data-stu-id="96670-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="96670-123">bokföra överföringar mellan bankkonton i samma valuta eller olika valutor.</span><span class="sxs-lookup"><span data-stu-id="96670-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="96670-124">Överföra banktillgångar</span><span class="sxs-lookup"><span data-stu-id="96670-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="96670-125">Se även</span><span class="sxs-lookup"><span data-stu-id="96670-125">See Also</span></span>
[<span data-ttu-id="96670-126">Ställa in bankverksamhet</span><span class="sxs-lookup"><span data-stu-id="96670-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="96670-127">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="96670-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="96670-128">[Hantera Leverantörsreskontra](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="96670-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="96670-129">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="96670-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="96670-130">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="96670-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

