---
title: Hantera bankkonton | Microsoft Docs
description: Du måste regelbundet stämma av banktransaktioner med relaterade banktransaktioner i dina bankkonton.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: db4afccdd67e400f2effd34b2db3c449db10432a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779713"
---
# <a name="reconciling-bank-accounts"></a><span data-ttu-id="ba964-103">Stämma av bankkonton</span><span class="sxs-lookup"><span data-stu-id="ba964-103">Reconciling Bank Accounts</span></span>

<span data-ttu-id="ba964-104">En bankavstämning bör slutföras med jämna mellanrum för alla dina bankkonton för att säkerställa att företagets kassaregister är korrekta.</span><span class="sxs-lookup"><span data-stu-id="ba964-104">A bank reconciliation should be completed at regular intervals for all your bank accounts to ensure that the company's cash records are correct.</span></span> <span data-ttu-id="ba964-105">Du gör detta genom att jämföra och matcha poster i dina interna bankkonton med banktransaktioner på din bank och sedan bokföra saldona på dina interna bankkonton för att göra summorna tillgängliga för ekonomichefer.</span><span class="sxs-lookup"><span data-stu-id="ba964-105">You do this by comparing and matching entries in your internal bank accounts with bank transactions at your bank, and then posting the balances to your internal bank accounts to make totals available to finance managers.</span></span> <span data-ttu-id="ba964-106">Bankavstämning är också ett praktiskt sätt att upptäcka och lösa problem med saknade betalningar och bokföringsfel.</span><span class="sxs-lookup"><span data-stu-id="ba964-106">Bank reconciliation is also a practical way to discover and resolve missing payments and bookkeeping errors.</span></span>

<span data-ttu-id="ba964-107">Alternativt kan du utföra åtgärden på sidan **Bankkontoavstämning** där du matchar (synkroniserar) bankutdragets rader i den vänstra rutan med dina interna bankkontotransaktioner i den till höger.</span><span class="sxs-lookup"><span data-stu-id="ba964-107">You can perform the task on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="ba964-108">Alternativt kan du på sidan **Betalningsavstämningsjournal** utföra denna aktivitet som en del av bearbetningen av de betalningar som anges på kontoutdraget.</span><span class="sxs-lookup"><span data-stu-id="ba964-108">Alternatively, you can perform this task on the **Payment Reconciliation Journal** page as part of processing the payments that are represented on a bank statement.</span></span> <span data-ttu-id="ba964-109">På båda sidor kan du fylla i bankutdragsinformationen genom att importera en fil eller mata in och använda automatiskt matchande förslag.</span><span class="sxs-lookup"><span data-stu-id="ba964-109">On both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="ba964-110">I Nordamerika kan du också utföra bankavstämning på sidan **Bank poster kalkylblad** som passar bättre för kontroller och inlåning men inte erbjuder import av bankutdragsfiler.</span><span class="sxs-lookup"><span data-stu-id="ba964-110">In the North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="ba964-111">Du använder den här sidan i stället för sidan **bankkontoavstämning**, avmarkera fälten **Bankavstämning med auto. match** på sidan **Redovisningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="ba964-111">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="ba964-112">Mer information finns i avsnittet [stämma av bankkonton](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under Förenta staterna: lokal funktion.</span><span class="sxs-lookup"><span data-stu-id="ba964-112">For more information, see [Reconcile Bank Accounts](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under United States Local Functionality.</span></span>

<span data-ttu-id="ba964-113">Innan du kan hantera dina bankkonton i [!INCLUDE[prod_short](includes/prod_short.md)] måste du registrera varje bankkonto som bankkontokort.</span><span class="sxs-lookup"><span data-stu-id="ba964-113">Before you can manage your bank accounts within [!INCLUDE[prod_short](includes/prod_short.md)], you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="ba964-114">Dessutom måste du skapa elektroniska tjänster som du kan använda för kontoutdragsimport-och betalningsfilexport.</span><span class="sxs-lookup"><span data-stu-id="ba964-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="ba964-115">Mer information finns i [Konfigurera bank](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="ba964-115">For more information, see [Setting Up Banking](bank-setup-banking.md).</span></span>

<span data-ttu-id="ba964-116">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="ba964-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="ba964-117">Till</span><span class="sxs-lookup"><span data-stu-id="ba964-117">To</span></span> | <span data-ttu-id="ba964-118">Gå till</span><span class="sxs-lookup"><span data-stu-id="ba964-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="ba964-119">Du kan stämma av bankkonton som en separat aktivitet på sidan **Bankkontoavstämning**.</span><span class="sxs-lookup"><span data-stu-id="ba964-119">Reconcile bank accounts as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="ba964-120">Stämma av bankkonton</span><span class="sxs-lookup"><span data-stu-id="ba964-120">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="ba964-121">Stämma av bankkonton i samband med betalningsbehandling på sidan **Betalningsavstämningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="ba964-121">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="ba964-122">Tillämpa betalningar automatiskt och jämka bankkonton</span><span class="sxs-lookup"><span data-stu-id="ba964-122">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> <span data-ttu-id="ba964-123">Med bankavstämningar kan du kontrollera att dina böcker är aktuella och inte bokföra avstämningen förrän du är nöjd med avstämningen.</span><span class="sxs-lookup"><span data-stu-id="ba964-123">Use bank reconciliation to help verify that your books are up-to-date, and do not post the reconciliation until you are satisfied with the reconciliation.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="ba964-124">Se Relaterad utbildning på [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="ba964-124">See Related Training at [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="ba964-125">Se även</span><span class="sxs-lookup"><span data-stu-id="ba964-125">See Also</span></span>

[<span data-ttu-id="ba964-126">Ställa in bankverksamhet</span><span class="sxs-lookup"><span data-stu-id="ba964-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="ba964-127">Stämma av bankkonton</span><span class="sxs-lookup"><span data-stu-id="ba964-127">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md)  
[<span data-ttu-id="ba964-128">Tillämpa betalningar automatiskt och jämka bankkonton</span><span class="sxs-lookup"><span data-stu-id="ba964-128">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[<span data-ttu-id="ba964-129">Överföra banktillgångar</span><span class="sxs-lookup"><span data-stu-id="ba964-129">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md)  
[<span data-ttu-id="ba964-130">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="ba964-130">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="ba964-131">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="ba964-131">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="ba964-132">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ba964-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ba964-133">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="ba964-133">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]