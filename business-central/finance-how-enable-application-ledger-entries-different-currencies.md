---
title: Koppla transaktioner i olika valutor | Microsoft Docs
description: "Du kan koppla transaktioner i olika valutor om du t.ex.. säljer i en valuta och får betalningen i en annan valuta."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 6d58c088c776a953cb76d102b7deeb3b8d69b42a
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="8e44a-103">Aktivera koppling av kundreskontratransaktioner till olika valutor</span><span class="sxs-lookup"><span data-stu-id="8e44a-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="8e44a-104">Om en valuta används vid inköp från en leverantör och en annan vid betalning kan du koppla betalningen till inköpet.</span><span class="sxs-lookup"><span data-stu-id="8e44a-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="8e44a-105">Om du säljer i en valuta och får betalt i en annan kan du koppla betalningen till försäljningsfakturan.</span><span class="sxs-lookup"><span data-stu-id="8e44a-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="8e44a-106">Efterföljande proceduren beskriver hur du ställer in detta för leverantörsreskontratransaktioner på sidan **Inköpsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="8e44a-106">The following procedure describes how to set this up for vendor ledger entries on the **Purchases & Payables Setup** page.</span></span> <span data-ttu-id="8e44a-107">Denna inställning liknar den för kundreskontratransaktioner på sidan **Försäljningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="8e44a-107">The setup is similar for customer ledger entries on the **Sales & Receivables Setup** page.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="8e44a-108">Så här aktiverar du koppling av leverantörsreskontratransaktioner i olika valutor</span><span class="sxs-lookup"><span data-stu-id="8e44a-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="8e44a-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8e44a-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="8e44a-110">I fältet **Koppling mellan valutor** markerar du ett av följande alternativ.</span><span class="sxs-lookup"><span data-stu-id="8e44a-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="8e44a-111">Alternativ</span><span class="sxs-lookup"><span data-stu-id="8e44a-111">Option</span></span> | <span data-ttu-id="8e44a-112">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="8e44a-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="8e44a-113">Ingen</span><span class="sxs-lookup"><span data-stu-id="8e44a-113">None</span></span> |<span data-ttu-id="8e44a-114">Koppling mellan valutor är inte tillåten.</span><span class="sxs-lookup"><span data-stu-id="8e44a-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="8e44a-115">EMU</span><span class="sxs-lookup"><span data-stu-id="8e44a-115">EMU</span></span> |<span data-ttu-id="8e44a-116">Koppling mellan EMU-valutor är tillåten.</span><span class="sxs-lookup"><span data-stu-id="8e44a-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="8e44a-117">Alla</span><span class="sxs-lookup"><span data-stu-id="8e44a-117">All</span></span> |<span data-ttu-id="8e44a-118">Koppling mellan alla valutor är tillåten.</span><span class="sxs-lookup"><span data-stu-id="8e44a-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="8e44a-119">Så här skapar du redovisningskonton för avrundningsdifferenser vid valutakoppling</span><span class="sxs-lookup"><span data-stu-id="8e44a-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="8e44a-120">Om du kopplar transaktioner till olika valutor måste du ange de redovisningskonton som du vill bokföra avrundningsdifferenserna på.</span><span class="sxs-lookup"><span data-stu-id="8e44a-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8e44a-121">Du måste skapa redovisningskonton innan du slutför uppgiften.</span><span class="sxs-lookup"><span data-stu-id="8e44a-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="8e44a-122">Mer information finns i [Förstå redovisning och kontoplan](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="8e44a-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="8e44a-123">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kundbokföringsmallar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8e44a-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8e44a-124">Ange aktuella redovisningskonton för bokföring av avrundningsskillnader i fälten **Debet valutakopp. avrundning** och **Kredit valutakopp. avrundning**.</span><span class="sxs-lookup"><span data-stu-id="8e44a-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="8e44a-125">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Leverantörsbokföringsmallar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8e44a-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="8e44a-126">Ange aktuella redovisningskonton för bokföring av avrundningsskillnader i fälten **Debet valutakopp. avrundning** och **Kredit valutakopp. avrundning**.</span><span class="sxs-lookup"><span data-stu-id="8e44a-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8e44a-127">Se även</span><span class="sxs-lookup"><span data-stu-id="8e44a-127">See Also</span></span>
[<span data-ttu-id="8e44a-128">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="8e44a-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="8e44a-129">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="8e44a-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="8e44a-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8e44a-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

