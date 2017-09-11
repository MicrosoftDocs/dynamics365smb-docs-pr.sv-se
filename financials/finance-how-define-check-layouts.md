---
title: "Ange layouten för en kontroll | Microsoft Docs"
description: "Du kan skapa och skriva ut dina checkar i flera olika format i överensstämmelse med standarder."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a2db2860846cd9b8010222faf580f0c9889e39a4
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-define-check-layouts"></a><span data-ttu-id="99a1f-103">Så här definierar du checklayouter</span><span class="sxs-lookup"><span data-stu-id="99a1f-103">How to: Define Check Layouts</span></span>
<span data-ttu-id="99a1f-104">Du kan designa dina checkar så att de uppfyller de normer som fastställts av de lokala myndigheterna.</span><span class="sxs-lookup"><span data-stu-id="99a1f-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="99a1f-105">Checkbilder kan vara skrivna ut på engelska, franska, eller spanska.</span><span class="sxs-lookup"><span data-stu-id="99a1f-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="99a1f-106">Checkar har utformats för att skrivas ut i både amerikanska och kanadensiska checkbildformat i antingen check-checktalong-check-format eller checktalong-checktalong-check-format.</span><span class="sxs-lookup"><span data-stu-id="99a1f-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="99a1f-107">Om du vill definiera checklayouter</span><span class="sxs-lookup"><span data-stu-id="99a1f-107">To define check layouts</span></span>
1. <span data-ttu-id="99a1f-108">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Rapportval - bankkonto** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="99a1f-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="99a1f-109">I fönstret **Rapportval - bankkonto.**</span><span class="sxs-lookup"><span data-stu-id="99a1f-109">In the **Report Selection - Bank Acc.**</span></span> <span data-ttu-id="99a1f-110">i fältet **Användning** markerar du **Check**.</span><span class="sxs-lookup"><span data-stu-id="99a1f-110">window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="99a1f-111">Välj något av följande rapport-ID:</span><span class="sxs-lookup"><span data-stu-id="99a1f-111">Select one of the following report IDs.</span></span>

| <span data-ttu-id="99a1f-112">Rapport-ID</span><span class="sxs-lookup"><span data-stu-id="99a1f-112">Report ID</span></span> | <span data-ttu-id="99a1f-113">Rapportnamn</span><span class="sxs-lookup"><span data-stu-id="99a1f-113">Report Name</span></span> | <span data-ttu-id="99a1f-114">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="99a1f-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="99a1f-115">1401</span><span class="sxs-lookup"><span data-stu-id="99a1f-115">1401</span></span> |<span data-ttu-id="99a1f-116">Check</span><span class="sxs-lookup"><span data-stu-id="99a1f-116">Check</span></span> |<span data-ttu-id="99a1f-117">Detta är standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="99a1f-117">This is the default report.</span></span> |
| <span data-ttu-id="99a1f-118">10401</span><span class="sxs-lookup"><span data-stu-id="99a1f-118">10401</span></span> |<span data-ttu-id="99a1f-119">Check (checktalong/checktalong/check)</span><span class="sxs-lookup"><span data-stu-id="99a1f-119">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="99a1f-120">Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/checktalong/check.</span><span class="sxs-lookup"><span data-stu-id="99a1f-120">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="99a1f-121">10411</span><span class="sxs-lookup"><span data-stu-id="99a1f-121">10411</span></span> |<span data-ttu-id="99a1f-122">Check (checktalong/check/checktalong)</span><span class="sxs-lookup"><span data-stu-id="99a1f-122">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="99a1f-123">Den här rapporten är utformad för att skriva ut checkar i formatet check/checktalong/check.</span><span class="sxs-lookup"><span data-stu-id="99a1f-123">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="99a1f-124">När du har upprättat checklayouter, kan du skriva ut checkar från fönstret **utbetalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="99a1f-124">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="99a1f-125">Mer information finns i [Så här arbetar du med checkar](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="99a1f-125">For more information, see [How to: Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="99a1f-126">Se även</span><span class="sxs-lookup"><span data-stu-id="99a1f-126">See Also</span></span>
[<span data-ttu-id="99a1f-127">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="99a1f-127">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="99a1f-128">[Hantera bankkonton](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="99a1f-128">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="99a1f-129">Slutföra periodslutsprocesser</span><span class="sxs-lookup"><span data-stu-id="99a1f-129">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="99a1f-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="99a1f-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="99a1f-131">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="99a1f-131">General Business Functionality</span></span>](ui-across-business-areas.md)

