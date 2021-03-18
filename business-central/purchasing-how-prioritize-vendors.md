---
title: Tilldela en leverantör till en prioritetsnivå | Microsoft Docs
description: Du kan tilldela nummer till dina leverantörer för att prioritera dessa och underlätta betalningsförslag i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c8cafd66724c8244abe311c8d7395a98ebe966ab
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386030"
---
# <a name="prioritize-vendors"></a><span data-ttu-id="e1535-103">Prioritera leverantörer</span><span class="sxs-lookup"><span data-stu-id="e1535-103">Prioritize Vendors</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="e1535-104">används för att ta fram olika betalningsförslag, t. ex. betalningar som snart förfaller eller betalningar för vilka en rabatt kan erhållas.</span><span class="sxs-lookup"><span data-stu-id="e1535-104">can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="e1535-105">Mer information finns i [Föreslå leverantörsbetalningar](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="e1535-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="e1535-106">Först måste du prioritera leverantörerna genom att tilldela nummer till dem.</span><span class="sxs-lookup"><span data-stu-id="e1535-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a><span data-ttu-id="e1535-107">Så här prioriterar du leverantörer:</span><span class="sxs-lookup"><span data-stu-id="e1535-107">To prioritize vendors</span></span>
1. <span data-ttu-id="e1535-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Leverantör** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e1535-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="e1535-109">Välj lämplig leverantör och sedan **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="e1535-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="e1535-110">Ange ett nummer i fältet **Prioritet**.</span><span class="sxs-lookup"><span data-stu-id="e1535-110">In the **Priority** field, enter a number.</span></span>

<span data-ttu-id="e1535-111">I [!INCLUDE[prod_short](includes/prod_short.md)] räknas lägst nummer (förutom 0) som högst prioritet.</span><span class="sxs-lookup"><span data-stu-id="e1535-111">[!INCLUDE[prod_short](includes/prod_short.md)] considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="e1535-112">Om du t. ex. använder 1, 2 och 3 har alltså 1 högst prioritet.</span><span class="sxs-lookup"><span data-stu-id="e1535-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="e1535-113">Om du inte vill prioritera en leverantör lämnar du fältet **Prioritet** tomt.</span><span class="sxs-lookup"><span data-stu-id="e1535-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="e1535-114">Om du sedan använder funktionen för betalningsförslag visas den här leverantören sist i listan, efter de leverantörer som har tilldelats ett prioritetsnummer.</span><span class="sxs-lookup"><span data-stu-id="e1535-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="e1535-115">Du kan ange valfritt antal prioritetsnivåer alltefter behov.</span><span class="sxs-lookup"><span data-stu-id="e1535-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1535-116">Se även</span><span class="sxs-lookup"><span data-stu-id="e1535-116">See Also</span></span>
[<span data-ttu-id="e1535-117">Ställa in inköp</span><span class="sxs-lookup"><span data-stu-id="e1535-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="e1535-118">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="e1535-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="e1535-119">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e1535-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]