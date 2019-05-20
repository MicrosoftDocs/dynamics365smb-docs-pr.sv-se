---
title: Tilldela en leverantör till en prioritetsnivå | Microsoft Docs
description: Du kan tilldela nummer till dina leverantörer för att prioritera dessa och underlätta betalningsförslag i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c709539b24aa1f94c86dee26dd63adead39c892b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252372"
---
# <a name="prioritize-vendors"></a><span data-ttu-id="2bd3e-103">Prioritera leverantörer</span><span class="sxs-lookup"><span data-stu-id="2bd3e-103">Prioritize Vendors</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2bd3e-104">används för att ta fram olika betalningsförslag, t.ex. betalningar som snart förfaller eller betalningar för vilka en rabatt kan erhållas.</span><span class="sxs-lookup"><span data-stu-id="2bd3e-104">can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="2bd3e-105">Mer information finns i [Föreslå leverantörsbetalningar](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="2bd3e-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="2bd3e-106">Först måste du prioritera leverantörerna genom att tilldela nummer till dem.</span><span class="sxs-lookup"><span data-stu-id="2bd3e-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>

## <a name="to-prioritize-vendors"></a><span data-ttu-id="2bd3e-107">Så här prioriterar du leverantörer:</span><span class="sxs-lookup"><span data-stu-id="2bd3e-107">To prioritize vendors</span></span>
1. <span data-ttu-id="2bd3e-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Leverantörer** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2bd3e-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="2bd3e-109">Välj lämplig leverantör och sedan **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="2bd3e-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="2bd3e-110">Ange ett nummer i fältet **Prioritet**.</span><span class="sxs-lookup"><span data-stu-id="2bd3e-110">In the **Priority** field, enter a number.</span></span>

<span data-ttu-id="2bd3e-111">I [!INCLUDE[d365fin](includes/d365fin_md.md)] räknas lägst nummer (förutom 0) som högst prioritet.</span><span class="sxs-lookup"><span data-stu-id="2bd3e-111">[!INCLUDE[d365fin](includes/d365fin_md.md)] considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="2bd3e-112">Om du t.ex. använder 1, 2 och 3 har alltså 1 högst prioritet.</span><span class="sxs-lookup"><span data-stu-id="2bd3e-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="2bd3e-113">Om du inte vill prioritera en leverantör lämnar du fältet **Prioritet** tomt.</span><span class="sxs-lookup"><span data-stu-id="2bd3e-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="2bd3e-114">Om du sedan använder funktionen för betalningsförslag visas den här leverantören sist i listan, efter de leverantörer som har tilldelats ett prioritetsnummer.</span><span class="sxs-lookup"><span data-stu-id="2bd3e-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="2bd3e-115">Du kan ange valfritt antal prioritetsnivåer alltefter behov.</span><span class="sxs-lookup"><span data-stu-id="2bd3e-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bd3e-116">Se även</span><span class="sxs-lookup"><span data-stu-id="2bd3e-116">See Also</span></span>
[<span data-ttu-id="2bd3e-117">Ställa in inköp</span><span class="sxs-lookup"><span data-stu-id="2bd3e-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="2bd3e-118">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="2bd3e-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="2bd3e-119">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2bd3e-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
