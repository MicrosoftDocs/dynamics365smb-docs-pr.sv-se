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
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 035f4c0e98e3b7ba308319c2017568de832e26c5
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="c5593-103">Så här aktiverar du koppling av kundreskontratransaktioner till olika valutor</span><span class="sxs-lookup"><span data-stu-id="c5593-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="c5593-104">Om en valuta används vid inköp från en leverantör och en annan vid betalning kan du koppla betalningen till inköpet.</span><span class="sxs-lookup"><span data-stu-id="c5593-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="c5593-105">Om du säljer i en valuta och får betalt i en annan kan du koppla betalningen till försäljningsfakturan.</span><span class="sxs-lookup"><span data-stu-id="c5593-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="c5593-106">Efterföljande proceduren beskriver hur du ställer in detta för leverantörsreskontratransaktioner i fönstret **Inköpsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="c5593-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="c5593-107">Denna inställning liknar den för kundreskontratransaktioner i fönstret **Försäljningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="c5593-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="c5593-108">Den här funktionen kräver att din upplevelse är inställd på **Paket**.</span><span class="sxs-lookup"><span data-stu-id="c5593-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="c5593-109">Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="c5593-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="c5593-110">Så här aktiverar du koppling av leverantörsreskontratransaktioner i olika valutor</span><span class="sxs-lookup"><span data-stu-id="c5593-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="c5593-111">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c5593-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="c5593-112">I fältet **Koppling mellan valutor** markerar du ett av följande alternativ.</span><span class="sxs-lookup"><span data-stu-id="c5593-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="c5593-113">Alternativ</span><span class="sxs-lookup"><span data-stu-id="c5593-113">Option</span></span> | <span data-ttu-id="c5593-114">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c5593-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="c5593-115">Ingen</span><span class="sxs-lookup"><span data-stu-id="c5593-115">None</span></span> |<span data-ttu-id="c5593-116">Koppling mellan valutor är inte tillåten.</span><span class="sxs-lookup"><span data-stu-id="c5593-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="c5593-117">EMU</span><span class="sxs-lookup"><span data-stu-id="c5593-117">EMU</span></span> |<span data-ttu-id="c5593-118">Koppling mellan EMU-valutor är tillåten.</span><span class="sxs-lookup"><span data-stu-id="c5593-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="c5593-119">Alla</span><span class="sxs-lookup"><span data-stu-id="c5593-119">All</span></span> |<span data-ttu-id="c5593-120">Koppling mellan alla valutor är tillåten.</span><span class="sxs-lookup"><span data-stu-id="c5593-120">Application between all currencies is allowed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c5593-121">Se även</span><span class="sxs-lookup"><span data-stu-id="c5593-121">See Also</span></span>
[<span data-ttu-id="c5593-122">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="c5593-122">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="c5593-123">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="c5593-123">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="c5593-124">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c5593-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

