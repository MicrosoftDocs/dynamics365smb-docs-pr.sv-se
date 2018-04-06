---
title: "Ställa in orealiserad moms | Microsoft Docs"
description: "Om du använder kontantbaserad redovisning kan ange du hur du vill hantera orealiserad moms för försäljning och inköp."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 09/08/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b8bbfac583e1e7ec7eedae9e412b4fd3ac956d0f
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a><span data-ttu-id="cab8a-103">Ställa in orealiserad moms för kontantbaserad redovisning</span><span class="sxs-lookup"><span data-stu-id="cab8a-103">Set Up Unrealized VAT for Cash-Based Accounting</span></span>
<span data-ttu-id="cab8a-104">Om du använder kontantbaserade redovisningsmetoder kan du skapa [!INCLUDE[d365fin](includes/d365fin_md.md)] för att hantera orealiserad moms.</span><span class="sxs-lookup"><span data-stu-id="cab8a-104">If you're using cash-based accounting methods, you can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] to handle unrealized VAT.</span></span>

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a><span data-ttu-id="cab8a-105">Använda redovisningskonton för orealiserad moms</span><span class="sxs-lookup"><span data-stu-id="cab8a-105">To use general ledger accounts for unrealized VAT</span></span>
<span data-ttu-id="cab8a-106">Du kan ange att momsbelopp ska beräknas och bokföras på ett temporärt redovisningskonto när en faktura bokförs, för att sedan bokföras på rätt redovisningskonto och inkluderas i momsrapporter när den faktiska betalningen av fakturan bokförs.</span><span class="sxs-lookup"><span data-stu-id="cab8a-106">You can choose to have VAT amounts calculated and posted to a temporary general ledger account when an invoice is posted, and then posted to the correct general ledger account and included in VAT statements when the actual payment of the invoice is posted.</span></span> <span data-ttu-id="cab8a-107">Innan du kan göra detta måste du komplettera momsbokföringsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="cab8a-107">Before you can do this, you must complete the VAT posting setup.</span></span>

<span data-ttu-id="cab8a-108">Om du vill använda konton för orealiserad moms, gör du så här:</span><span class="sxs-lookup"><span data-stu-id="cab8a-108">To use accounts for unrealized VAT, follow these steps:</span></span>
1. <span data-ttu-id="cab8a-109">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten") och ange **Redovisningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="cab8a-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, and enter **General Ledger Setup**.</span></span>
2. <span data-ttu-id="cab8a-110">På sidan **Redovisningsinställningar** på snabbfliken **allmänt** väljer du **visa fler**, och väljer sedan kryssrutan **orealiserad moms**.</span><span class="sxs-lookup"><span data-stu-id="cab8a-110">On the **General Ledger Setup** page, on the **General** FastTab, choose **Show More**, and then choose the **Unrealized VAT** check box.</span></span>
3. <span data-ttu-id="cab8a-111">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="cab8a-111">Close the page.</span></span>
4. <span data-ttu-id="cab8a-112">I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Bokföringsinställningar för moms**.</span><span class="sxs-lookup"><span data-stu-id="cab8a-112">choose the **Search for Page or Report** icon ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon"), and enter **VAT Posting Setup**.</span></span>
5. <span data-ttu-id="cab8a-113">På sidan **Bokföringsinställningar för moms** väljer du moms och väljer sedan **redigera**.</span><span class="sxs-lookup"><span data-stu-id="cab8a-113">On the **VAT Posting Setup** page, choose the VAT posting group, and then choose **Edit**.</span></span>
6. <span data-ttu-id="cab8a-114">I fältet **Orealiserad momstyp** väljer du ett alternativ för att ange hur du ska fördela betalningar till fakturabeloppet (exklusive moms) och själva momsbeloppet, samt hur momsbeloppen överförs från kontot för orealiserad moms till konto för (realiserad) moms.</span><span class="sxs-lookup"><span data-stu-id="cab8a-114">In the **Unrealized VAT Type** field, choose an option to specify how to allocate payments to the invoice amount (excluding VAT) and the VAT amount itself, and how to transfer VAT amounts from the unrealized VAT account to the realized account.</span></span> <span data-ttu-id="cab8a-115">Alternativen beskrivs i tabellen nedan.</span><span class="sxs-lookup"><span data-stu-id="cab8a-115">The following table describes the options.</span></span>

| <span data-ttu-id="cab8a-116">Alternativ</span><span class="sxs-lookup"><span data-stu-id="cab8a-116">Option</span></span> | <span data-ttu-id="cab8a-117">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="cab8a-117">Description</span></span> |
| --- | --- |
| <span data-ttu-id="cab8a-118">Tomt</span><span class="sxs-lookup"><span data-stu-id="cab8a-118">Blank</span></span> | <span data-ttu-id="cab8a-119">Välj det här alternativet om du inte vill använda funktionen för orealiserad moms.</span><span class="sxs-lookup"><span data-stu-id="cab8a-119">Choose this option if you don't want to use the unrealized VAT feature.</span></span> |
| <span data-ttu-id="cab8a-120">Procent</span><span class="sxs-lookup"><span data-stu-id="cab8a-120">Percentage</span></span> | <span data-ttu-id="cab8a-121">Betalningar täcker både moms och fakturabelopp i proportion till betalningens procent av det återstående fakturabeloppet.</span><span class="sxs-lookup"><span data-stu-id="cab8a-121">Payments covers both VAT and the invoice amount in proportion to the payment's percentage of the remaining invoice amount.</span></span> <span data-ttu-id="cab8a-122">Det betalda momsbeloppet överförs från kontot för orealiserad moms till realiserade momskontot.</span><span class="sxs-lookup"><span data-stu-id="cab8a-122">The paid VAT amount is transferred from the unrealized VAT account to the realized VAT account.</span></span> |
| <span data-ttu-id="cab8a-123">Första</span><span class="sxs-lookup"><span data-stu-id="cab8a-123">First</span></span> | <span data-ttu-id="cab8a-124">Betalningar täcker först momsbeloppet och sedan fakturabeloppet.</span><span class="sxs-lookup"><span data-stu-id="cab8a-124">Payments cover VAT first and then invoice amounts.</span></span> <span data-ttu-id="cab8a-125">I det här fallet kommer det belopp som överförs från kontot för orealiserad moms att vara lika med betalningsbeloppet tills den totala momsen har betalts.</span><span class="sxs-lookup"><span data-stu-id="cab8a-125">In this case, the amount transferred from the unrealized VAT account to the VAT account will equal the amount of the payment until the total VAT has been paid.</span></span> |
| <span data-ttu-id="cab8a-126">Sista</span><span class="sxs-lookup"><span data-stu-id="cab8a-126">Last</span></span> | <span data-ttu-id="cab8a-127">Betalningar täcker först fakturabeloppet och sedan momsen.</span><span class="sxs-lookup"><span data-stu-id="cab8a-127">Payments cover the invoice amount first and then VAT.</span></span> <span data-ttu-id="cab8a-128">I det här fallet kommer inget belopp att överföras från kontot för orealiserad moms till momskontot förrän fakturans totala belopp, exklusive moms, har betalts.</span><span class="sxs-lookup"><span data-stu-id="cab8a-128">In this case, no amount will be transferred from the unrealized VAT account to the VAT account until the total amount of the invoice, excluding VAT, has been paid.</span></span> |
| <span data-ttu-id="cab8a-129">Först (hela beloppet)</span><span class="sxs-lookup"><span data-stu-id="cab8a-129">First (Fully Paid)</span></span> | <span data-ttu-id="cab8a-130">Betalningar täcker först momsen (som i alternativet _Först_), men inget belopp överförs till momskontot förrän hela momsbeloppet har betalats.</span><span class="sxs-lookup"><span data-stu-id="cab8a-130">Payments will cover VAT first (like the _First_ option), but no amount will be transferred to the VAT account until the full amount of VAT has been paid.</span></span> |
| <span data-ttu-id="cab8a-131">Sist (hela beloppet)</span><span class="sxs-lookup"><span data-stu-id="cab8a-131">Last (Fully Paid)</span></span> | <span data-ttu-id="cab8a-132">Betalningar täcker först fakturabeloppet (som i alternativet _Sist_), men inget belopp överförs till momskontot förrän hela momsbeloppet har betalats.</span><span class="sxs-lookup"><span data-stu-id="cab8a-132">Payments will cover invoice amount first (like the _Last_ option), but no amount will be transferred to the VAT account until the full amount of VAT has been paid.</span></span> |

6. <span data-ttu-id="cab8a-133">I fältet **Oreal. utgående moms** anger du kontot för orealiserad utgående moms.</span><span class="sxs-lookup"><span data-stu-id="cab8a-133">In the **Sales VAT Unreal. Account** field, choose the account for unrealized sales VAT.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="cab8a-134">Momsbeloppet kommer att bokföras till kontot för orealiserad moms där det kvarstår tills betalningen till leverantören bokförts.</span><span class="sxs-lookup"><span data-stu-id="cab8a-134">The VAT amount will be posted to this account, and stay there until the customer payment is posted.</span></span> <span data-ttu-id="cab8a-135">Beloppet överförs sedan till kontot för utgående moms.</span><span class="sxs-lookup"><span data-stu-id="cab8a-135">The amount is then transferred to the account for sales VAT.</span></span>
7. <span data-ttu-id="cab8a-136">Ange redovisningskontot för orealiserad ingående moms i fältet **Oreal. ingående moms**.</span><span class="sxs-lookup"><span data-stu-id="cab8a-136">In the **Purch. VAT Unreal. Account** field, enter the general ledger account for unrealized purchase VAT.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="cab8a-137">Momsbeloppet kommer att bokföras till kontot för orealiserad moms där det kvarstår tills betalningen till leverantören bokförts.</span><span class="sxs-lookup"><span data-stu-id="cab8a-137">The VAT amount will be posted to this account, and stay there until the customer payment is posted.</span></span> <span data-ttu-id="cab8a-138">Beloppet överförs sedan till kontot för ingående moms.</span><span class="sxs-lookup"><span data-stu-id="cab8a-138">The amount is then transferred to the account for purchase VAT.</span></span>

## <a name="see-also"></a><span data-ttu-id="cab8a-139">Se även</span><span class="sxs-lookup"><span data-stu-id="cab8a-139">See Also</span></span>
[<span data-ttu-id="cab8a-140">Ställa in orealiserad moms</span><span class="sxs-lookup"><span data-stu-id="cab8a-140">Setting Up Value Added Tax</span></span>](finance-setup-vat.md)

