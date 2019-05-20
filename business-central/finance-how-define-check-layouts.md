---
title: Ange layouten för en kontroll | Microsoft Docs
description: Du kan skapa och skriva ut dina checkar i flera olika format i överensstämmelse med standarder.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/24/2019
ms.author: edupont
ms.openlocfilehash: f2b7fa01cff36e3aab335f7d5921954343c69b74
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243601"
---
# <a name="define-check-layouts"></a><span data-ttu-id="b9133-103">Definiera checklayouter</span><span class="sxs-lookup"><span data-stu-id="b9133-103">Define Check Layouts</span></span>
<span data-ttu-id="b9133-104">Du kan designa dina checkar så att de uppfyller de normer som fastställts av de lokala myndigheterna.</span><span class="sxs-lookup"><span data-stu-id="b9133-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="b9133-105">Checkbilder kan vara skrivna ut på engelska, franska, eller spanska.</span><span class="sxs-lookup"><span data-stu-id="b9133-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="b9133-106">Checkar har utformats för att skrivas ut i både amerikanska och kanadensiska checkbildformat i antingen check-checktalong-check-format eller checktalong-checktalong-check-format.</span><span class="sxs-lookup"><span data-stu-id="b9133-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="b9133-107">Om du vill definiera checklayouter</span><span class="sxs-lookup"><span data-stu-id="b9133-107">To define check layouts</span></span>
1. <span data-ttu-id="b9133-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Rapportval - bankkonto** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b9133-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="b9133-109">På sidan **Rapportval - bankkonto** i fältet **Användning** väljer du **Check**.</span><span class="sxs-lookup"><span data-stu-id="b9133-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="b9133-110">Välj något av följande rapport-ID:</span><span class="sxs-lookup"><span data-stu-id="b9133-110">Select one of the following report IDs.</span></span>

  | <span data-ttu-id="b9133-111">Rapport-ID</span><span class="sxs-lookup"><span data-stu-id="b9133-111">Report ID</span></span> | <span data-ttu-id="b9133-112">Rapportnamn</span><span class="sxs-lookup"><span data-stu-id="b9133-112">Report Name</span></span> | <span data-ttu-id="b9133-113">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="b9133-113">Description</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="b9133-114">1401</span><span class="sxs-lookup"><span data-stu-id="b9133-114">1401</span></span> |<span data-ttu-id="b9133-115">Check</span><span class="sxs-lookup"><span data-stu-id="b9133-115">Check</span></span> |<span data-ttu-id="b9133-116">Detta är standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="b9133-116">This is the default report.</span></span> |
  | <span data-ttu-id="b9133-117">10411</span><span class="sxs-lookup"><span data-stu-id="b9133-117">10411</span></span> |<span data-ttu-id="b9133-118">Check (checktalong/checktalong/check)</span><span class="sxs-lookup"><span data-stu-id="b9133-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="b9133-119">Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/checktalong/check.</span><span class="sxs-lookup"><span data-stu-id="b9133-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
  | <span data-ttu-id="b9133-120">10412</span><span class="sxs-lookup"><span data-stu-id="b9133-120">10412</span></span> |<span data-ttu-id="b9133-121">Check (checktalong/check/checktalong)</span><span class="sxs-lookup"><span data-stu-id="b9133-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="b9133-122">Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/check/checktalong.</span><span class="sxs-lookup"><span data-stu-id="b9133-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
  | <span data-ttu-id="b9133-123">10413</span><span class="sxs-lookup"><span data-stu-id="b9133-123">10413</span></span> |<span data-ttu-id="b9133-124">Tre checkar per sida</span><span class="sxs-lookup"><span data-stu-id="b9133-124">Three Checks per Page</span></span> |<span data-ttu-id="b9133-125">Den här rapporten är utformad för att skriva ut tre checkar på varje sida.</span><span class="sxs-lookup"><span data-stu-id="b9133-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="b9133-126">När du har upprättat checklayouter, kan du skriva ut checkar från sidan **utbetalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="b9133-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="b9133-127">Mer information finns i [Arbeta med checkar](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="b9133-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b9133-128">Se även</span><span class="sxs-lookup"><span data-stu-id="b9133-128">See Also</span></span>
[<span data-ttu-id="b9133-129">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="b9133-129">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="b9133-130">[Hantera bankkonton](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="b9133-130">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="b9133-131">Slutföra periodslutsprocesser</span><span class="sxs-lookup"><span data-stu-id="b9133-131">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="b9133-132">[Arbeta med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b9133-132">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b9133-133">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="b9133-133">General Business Functionality</span></span>](ui-across-business-areas.md)
