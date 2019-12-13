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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: d4818c9dfe96f7e890d84a16c717d4451f56497a
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808583"
---
# <a name="select-a-check-layout"></a><span data-ttu-id="01e33-103">Välj en checklayout</span><span class="sxs-lookup"><span data-stu-id="01e33-103">Select a Check Layout</span></span>
<span data-ttu-id="01e33-104">Du kan designa dina checkar så att de uppfyller de normer som fastställts av de lokala myndigheterna.</span><span class="sxs-lookup"><span data-stu-id="01e33-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="01e33-105">Checkbilder kan vara skrivna ut på engelska, franska, eller spanska.</span><span class="sxs-lookup"><span data-stu-id="01e33-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="01e33-106">Checkar har utformats för att skrivas ut i både amerikanska och kanadensiska checkbildformat i antingen check-checktalong-check-format eller checktalong-checktalong-check-format.</span><span class="sxs-lookup"><span data-stu-id="01e33-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-select-a-check-layout"></a><span data-ttu-id="01e33-107">Välj en checklayout genom att</span><span class="sxs-lookup"><span data-stu-id="01e33-107">To select a check layout</span></span>
1. <span data-ttu-id="01e33-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Rapportval - bankkonto** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="01e33-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="01e33-109">På sidan **Rapportval - bankkonto** i fältet **Användning** väljer du **Check**.</span><span class="sxs-lookup"><span data-stu-id="01e33-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="01e33-110">Välj något av följande rapport-ID:</span><span class="sxs-lookup"><span data-stu-id="01e33-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="01e33-111">Rapport-ID</span><span class="sxs-lookup"><span data-stu-id="01e33-111">Report ID</span></span> | <span data-ttu-id="01e33-112">Rapportnamn</span><span class="sxs-lookup"><span data-stu-id="01e33-112">Report Name</span></span> | <span data-ttu-id="01e33-113">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="01e33-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="01e33-114">1401</span><span class="sxs-lookup"><span data-stu-id="01e33-114">1401</span></span> |<span data-ttu-id="01e33-115">Check</span><span class="sxs-lookup"><span data-stu-id="01e33-115">Check</span></span> |<span data-ttu-id="01e33-116">Detta är standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="01e33-116">This is the default report.</span></span> |
| <span data-ttu-id="01e33-117">10411</span><span class="sxs-lookup"><span data-stu-id="01e33-117">10411</span></span> |<span data-ttu-id="01e33-118">Check (checktalong/checktalong/check)</span><span class="sxs-lookup"><span data-stu-id="01e33-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="01e33-119">Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/checktalong/check.</span><span class="sxs-lookup"><span data-stu-id="01e33-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="01e33-120">10412</span><span class="sxs-lookup"><span data-stu-id="01e33-120">10412</span></span> |<span data-ttu-id="01e33-121">Check (checktalong/check/checktalong)</span><span class="sxs-lookup"><span data-stu-id="01e33-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="01e33-122">Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/check/checktalong.</span><span class="sxs-lookup"><span data-stu-id="01e33-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
| <span data-ttu-id="01e33-123">10413</span><span class="sxs-lookup"><span data-stu-id="01e33-123">10413</span></span> |<span data-ttu-id="01e33-124">Tre checkar per sida</span><span class="sxs-lookup"><span data-stu-id="01e33-124">Three Checks per Page</span></span> |<span data-ttu-id="01e33-125">Den här rapporten är utformad för att skriva ut tre checkar på varje sida.</span><span class="sxs-lookup"><span data-stu-id="01e33-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="01e33-126">När du har upprättat checklayouter, kan du skriva ut checkar från sidan **utbetalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="01e33-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="01e33-127">Mer information finns i [Arbeta med checkar](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="01e33-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

<span data-ttu-id="01e33-128">Om du vill ändra en av dessa standardlayouter använder du antingen Word- eller RDLC-integration.</span><span class="sxs-lookup"><span data-stu-id="01e33-128">To change one of these default check layouts, use either the Word or the RDLC integration to do so.</span></span> <span data-ttu-id="01e33-129">Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="01e33-129">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="01e33-130">Se även</span><span class="sxs-lookup"><span data-stu-id="01e33-130">See Also</span></span>
[<span data-ttu-id="01e33-131">Skapa och ändra anpassade rapportlayouter</span><span class="sxs-lookup"><span data-stu-id="01e33-131">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="01e33-132">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="01e33-132">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="01e33-133">[Hantera bankkonton](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="01e33-133">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="01e33-134">Slutföra periodslutsprocesser</span><span class="sxs-lookup"><span data-stu-id="01e33-134">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="01e33-135">[Arbeta med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="01e33-135">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="01e33-136">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="01e33-136">General Business Functionality</span></span>](ui-across-business-areas.md)
