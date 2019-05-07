---
title: Ange layouten för en kontroll | Microsoft Docs
description: Du kan skapa och skriva ut dina checkar i flera olika format i överensstämmelse med standarder.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: eace865bc70f56206d478f8e8d38fd217133925e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "935264"
---
# <a name="define-check-layouts"></a><span data-ttu-id="2f6f7-103">Definiera checklayouter</span><span class="sxs-lookup"><span data-stu-id="2f6f7-103">Define Check Layouts</span></span>
<span data-ttu-id="2f6f7-104">Du kan designa dina checkar så att de uppfyller de normer som fastställts av de lokala myndigheterna.</span><span class="sxs-lookup"><span data-stu-id="2f6f7-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="2f6f7-105">Checkbilder kan vara skrivna ut på engelska, franska, eller spanska.</span><span class="sxs-lookup"><span data-stu-id="2f6f7-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="2f6f7-106">Checkar har utformats för att skrivas ut i både amerikanska och kanadensiska checkbildformat i antingen check-checktalong-check-format eller checktalong-checktalong-check-format.</span><span class="sxs-lookup"><span data-stu-id="2f6f7-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="2f6f7-107">Om du vill definiera checklayouter</span><span class="sxs-lookup"><span data-stu-id="2f6f7-107">To define check layouts</span></span>
1. <span data-ttu-id="2f6f7-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Rapportval - bankkonto** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2f6f7-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="2f6f7-109">På sidan **Rapportval - bankkonto** i fältet **Användning** väljer du **Check**.</span><span class="sxs-lookup"><span data-stu-id="2f6f7-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="2f6f7-110">Välj något av följande rapport-ID:</span><span class="sxs-lookup"><span data-stu-id="2f6f7-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="2f6f7-111">Rapport-ID</span><span class="sxs-lookup"><span data-stu-id="2f6f7-111">Report ID</span></span> | <span data-ttu-id="2f6f7-112">Rapportnamn</span><span class="sxs-lookup"><span data-stu-id="2f6f7-112">Report Name</span></span> | <span data-ttu-id="2f6f7-113">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="2f6f7-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2f6f7-114">1401</span><span class="sxs-lookup"><span data-stu-id="2f6f7-114">1401</span></span> |<span data-ttu-id="2f6f7-115">Check</span><span class="sxs-lookup"><span data-stu-id="2f6f7-115">Check</span></span> |<span data-ttu-id="2f6f7-116">Detta är standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="2f6f7-116">This is the default report.</span></span> |
| <span data-ttu-id="2f6f7-117">10401</span><span class="sxs-lookup"><span data-stu-id="2f6f7-117">10401</span></span> |<span data-ttu-id="2f6f7-118">Check (checktalong/checktalong/check)</span><span class="sxs-lookup"><span data-stu-id="2f6f7-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="2f6f7-119">Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/checktalong/check.</span><span class="sxs-lookup"><span data-stu-id="2f6f7-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="2f6f7-120">10411</span><span class="sxs-lookup"><span data-stu-id="2f6f7-120">10411</span></span> |<span data-ttu-id="2f6f7-121">Check (checktalong/check/checktalong)</span><span class="sxs-lookup"><span data-stu-id="2f6f7-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="2f6f7-122">Den här rapporten är utformad för att skriva ut checkar i formatet check/checktalong/check.</span><span class="sxs-lookup"><span data-stu-id="2f6f7-122">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="2f6f7-123">När du har upprättat checklayouter, kan du skriva ut checkar från sidan **utbetalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="2f6f7-123">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="2f6f7-124">Mer information finns i [Arbeta med checkar](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="2f6f7-124">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2f6f7-125">Se även</span><span class="sxs-lookup"><span data-stu-id="2f6f7-125">See Also</span></span>
[<span data-ttu-id="2f6f7-126">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="2f6f7-126">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="2f6f7-127">[Hantera bankkonton](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="2f6f7-127">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="2f6f7-128">Slutföra periodslutsprocesser</span><span class="sxs-lookup"><span data-stu-id="2f6f7-128">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="2f6f7-129">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2f6f7-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="2f6f7-130">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="2f6f7-130">General Business Functionality</span></span>](ui-across-business-areas.md)
