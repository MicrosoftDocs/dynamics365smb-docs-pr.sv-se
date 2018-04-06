---
title: Koppla transaktioner i olika valutor | Microsoft Docs
description: "Du kan koppla transaktioner i olika valutor om du t.ex.. säljer i en valuta och får betalningen i en annan valuta."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d98fdf358e387be1d53b188cc05c57108e8592b8
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="dfffe-103">Aktivera koppling av kundreskontratransaktioner till olika valutor</span><span class="sxs-lookup"><span data-stu-id="dfffe-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="dfffe-104">Om en valuta används vid inköp från en leverantör och en annan vid betalning kan du koppla betalningen till inköpet.</span><span class="sxs-lookup"><span data-stu-id="dfffe-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="dfffe-105">Om du säljer i en valuta och får betalt i en annan kan du koppla betalningen till försäljningsfakturan.</span><span class="sxs-lookup"><span data-stu-id="dfffe-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="dfffe-106">Efterföljande proceduren beskriver hur du ställer in detta för leverantörsreskontratransaktioner i fönstret **Inköpsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="dfffe-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="dfffe-107">Denna inställning liknar den för kundreskontratransaktioner i fönstret **Försäljningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="dfffe-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="dfffe-108">Så här aktiverar du koppling av leverantörsreskontratransaktioner i olika valutor</span><span class="sxs-lookup"><span data-stu-id="dfffe-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="dfffe-109">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Inköpsinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dfffe-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="dfffe-110">I fältet **Koppling mellan valutor** markerar du ett av följande alternativ.</span><span class="sxs-lookup"><span data-stu-id="dfffe-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="dfffe-111">Alternativ</span><span class="sxs-lookup"><span data-stu-id="dfffe-111">Option</span></span> | <span data-ttu-id="dfffe-112">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="dfffe-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="dfffe-113">Ingen</span><span class="sxs-lookup"><span data-stu-id="dfffe-113">None</span></span> |<span data-ttu-id="dfffe-114">Koppling mellan valutor är inte tillåten.</span><span class="sxs-lookup"><span data-stu-id="dfffe-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="dfffe-115">EMU</span><span class="sxs-lookup"><span data-stu-id="dfffe-115">EMU</span></span> |<span data-ttu-id="dfffe-116">Koppling mellan EMU-valutor är tillåten.</span><span class="sxs-lookup"><span data-stu-id="dfffe-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="dfffe-117">Alla</span><span class="sxs-lookup"><span data-stu-id="dfffe-117">All</span></span> |<span data-ttu-id="dfffe-118">Koppling mellan alla valutor är tillåten.</span><span class="sxs-lookup"><span data-stu-id="dfffe-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="dfffe-119">Så här skapar du redovisningskonton för avrundningsdifferenser vid valutakoppling</span><span class="sxs-lookup"><span data-stu-id="dfffe-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="dfffe-120">Om du kopplar transaktioner till olika valutor måste du ange de redovisningskonton som du vill bokföra avrundningsdifferenserna på.</span><span class="sxs-lookup"><span data-stu-id="dfffe-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="dfffe-121">Du måste skapa redovisningskonton innan du slutför uppgiften.</span><span class="sxs-lookup"><span data-stu-id="dfffe-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="dfffe-122">Mer information finns i [Förstå redovisning och kontoplan](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="dfffe-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="dfffe-123">Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kundbokningsgruppen** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dfffe-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dfffe-124">Ange aktuella redovisningskonton för bokföring av avrundningsskillnader i fälten **Debet valutakopp. avrundning** och **Kredit valutakopp. avrundning**.</span><span class="sxs-lookup"><span data-stu-id="dfffe-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="dfffe-125">Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Leverantörsbokföringsmallar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dfffe-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="dfffe-126">Ange aktuella redovisningskonton för bokföring av avrundningsskillnader i fälten **Debet valutakopp. avrundning** och **Kredit valutakopp. avrundning**.</span><span class="sxs-lookup"><span data-stu-id="dfffe-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dfffe-127">Se även</span><span class="sxs-lookup"><span data-stu-id="dfffe-127">See Also</span></span>
[<span data-ttu-id="dfffe-128">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="dfffe-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="dfffe-129">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="dfffe-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="dfffe-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dfffe-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

