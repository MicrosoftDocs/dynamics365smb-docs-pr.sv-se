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
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 743cf7ecbed4157dc9283a97baa956e69ec0c6b5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807844"
---
# <a name="define-check-layouts"></a><span data-ttu-id="921be-103">Definiera checklayouter</span><span class="sxs-lookup"><span data-stu-id="921be-103">Define Check Layouts</span></span>
<span data-ttu-id="921be-104">Du kan designa dina checkar så att de uppfyller de normer som fastställts av de lokala myndigheterna.</span><span class="sxs-lookup"><span data-stu-id="921be-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="921be-105">Checkbilder kan vara skrivna ut på engelska, franska, eller spanska.</span><span class="sxs-lookup"><span data-stu-id="921be-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="921be-106">Checkar har utformats för att skrivas ut i både amerikanska och kanadensiska checkbildformat i antingen check-checktalong-check-format eller checktalong-checktalong-check-format.</span><span class="sxs-lookup"><span data-stu-id="921be-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="921be-107">Om du vill definiera checklayouter</span><span class="sxs-lookup"><span data-stu-id="921be-107">To define check layouts</span></span>
1. <span data-ttu-id="921be-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Rapportval - bankkonto** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="921be-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="921be-109">På sidan **Rapportval - bankkonto** i fältet **Användning** väljer du **Check**.</span><span class="sxs-lookup"><span data-stu-id="921be-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="921be-110">Välj något av följande rapport-ID:</span><span class="sxs-lookup"><span data-stu-id="921be-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="921be-111">Rapport-ID</span><span class="sxs-lookup"><span data-stu-id="921be-111">Report ID</span></span> | <span data-ttu-id="921be-112">Rapportnamn</span><span class="sxs-lookup"><span data-stu-id="921be-112">Report Name</span></span> | <span data-ttu-id="921be-113">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="921be-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="921be-114">1401</span><span class="sxs-lookup"><span data-stu-id="921be-114">1401</span></span> |<span data-ttu-id="921be-115">Check</span><span class="sxs-lookup"><span data-stu-id="921be-115">Check</span></span> |<span data-ttu-id="921be-116">Detta är standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="921be-116">This is the default report.</span></span> |
| <span data-ttu-id="921be-117">10401</span><span class="sxs-lookup"><span data-stu-id="921be-117">10401</span></span> |<span data-ttu-id="921be-118">Check (checktalong/checktalong/check)</span><span class="sxs-lookup"><span data-stu-id="921be-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="921be-119">Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/checktalong/check.</span><span class="sxs-lookup"><span data-stu-id="921be-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="921be-120">10411</span><span class="sxs-lookup"><span data-stu-id="921be-120">10411</span></span> |<span data-ttu-id="921be-121">Check (checktalong/check/checktalong)</span><span class="sxs-lookup"><span data-stu-id="921be-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="921be-122">Den här rapporten är utformad för att skriva ut checkar i formatet check/checktalong/check.</span><span class="sxs-lookup"><span data-stu-id="921be-122">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="921be-123">När du har upprättat checklayouter, kan du skriva ut checkar från sidan **utbetalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="921be-123">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="921be-124">Mer information finns i [Arbeta med checkar](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="921be-124">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="921be-125">Se även</span><span class="sxs-lookup"><span data-stu-id="921be-125">See Also</span></span>
[<span data-ttu-id="921be-126">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="921be-126">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="921be-127">[Hantera bankkonton](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="921be-127">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="921be-128">Slutföra periodslutsprocesser</span><span class="sxs-lookup"><span data-stu-id="921be-128">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="921be-129">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="921be-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="921be-130">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="921be-130">General Business Functionality</span></span>](ui-across-business-areas.md)
