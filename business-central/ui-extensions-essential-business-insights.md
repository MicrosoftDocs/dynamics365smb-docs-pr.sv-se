---
title: "Visa åtgärdsinriktade insikter i rollcenter | Microsoft Docs"
description: "Tillägget Vitala företagsinsikter roterar ett antal företagsinsikter om rollcenter."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: BI, add-in, insight, headline, data
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0879d8ff0fbca3b18c36412e0a5fbe2f39372f2a
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---

# <a name="the-essential-business-insights-extension"></a><span data-ttu-id="42a45-103">Tillägget Vitala företagsinsikter</span><span class="sxs-lookup"><span data-stu-id="42a45-103">The Essential Business Insights Extension</span></span>
<span data-ttu-id="42a45-104">Tillägget Vitala företagsinsikter hittar intressanta affärsfakta i dina företagsdata och visar dessa som tidningsaktiga rubriker i rollcenter.</span><span class="sxs-lookup"><span data-stu-id="42a45-104">The Essential Business Insights extension finds interesting business facts in your company data and displays them as newspaper-like headlines in Role Centers.</span></span> <span data-ttu-id="42a45-105">Beroende på vad tillägget hittar i datan kommer insikterna från förra veckan, förra månaden eller tre månader från dagens datum.</span><span class="sxs-lookup"><span data-stu-id="42a45-105">Depending on what the extension finds in the data, the insights are from the last week, month, or three months from the current date.</span></span> <span data-ttu-id="42a45-106">Denna kunskap uppdateras var 10:e minut.</span><span class="sxs-lookup"><span data-stu-id="42a45-106">The insights update every 10 minutes.</span></span>  

<span data-ttu-id="42a45-107">Om du vill titta närmare på en insikt kan du välja den för att komma till källan.</span><span class="sxs-lookup"><span data-stu-id="42a45-107">If you want to take a closer look at an insight, you can choose it to go to its source.</span></span> <span data-ttu-id="42a45-108">Om du exempelvis vill ha information om den största försäljningsfakturan som bokfördes förra veckan, kan du välja insikten för att visa fakturan.</span><span class="sxs-lookup"><span data-stu-id="42a45-108">For example, if you want details about the largest sales invoice that was posted last week, you can choose the insight to display the invoice.</span></span>

<span data-ttu-id="42a45-109">I följande tabell beskrivs den information som detta tillägg ger respektive rollcenter.</span><span class="sxs-lookup"><span data-stu-id="42a45-109">The following table describes the insights that this extension provides for each Role Center.</span></span>

|<span data-ttu-id="42a45-110">Rollcenter</span><span class="sxs-lookup"><span data-stu-id="42a45-110">Role Center</span></span>|<span data-ttu-id="42a45-111">Frågor som insikterna besvarar</span><span class="sxs-lookup"><span data-stu-id="42a45-111">Questions the Insights Answer</span></span>|
|----|-----|
|<span data-ttu-id="42a45-112">Standard</span><span class="sxs-lookup"><span data-stu-id="42a45-112">Default</span></span>|<span data-ttu-id="42a45-113">Visar en hälsningsfras och en länk till produktinformation.</span><span class="sxs-lookup"><span data-stu-id="42a45-113">Displays a greeting, and link to product information.</span></span>|
|<span data-ttu-id="42a45-114">Chef</span><span class="sxs-lookup"><span data-stu-id="42a45-114">Business Manager</span></span>|<li> <span data-ttu-id="42a45-115">Vilken artikel var mest populär föregående vecka, månad eller de senaste tre månaderna, och hur många sålde vi?</span><span class="sxs-lookup"><span data-stu-id="42a45-115">What was the most popular item last week, month, or last three months, and how many did we sell?</span></span><br><li> <span data-ttu-id="42a45-116">Vilken var den största försäljningsordern föregående vecka, månad eller de senaste tre månaderna?</span><span class="sxs-lookup"><span data-stu-id="42a45-116">What was the largest sale order last week, month, or last three months?</span></span><br><li> <span data-ttu-id="42a45-117">Vem eller vad var den mest använda resursen, och vilka var bokningarna?</span><span class="sxs-lookup"><span data-stu-id="42a45-117">Who, or what, was the busiest resource, and what were the bookings?</span></span><br><li> <span data-ttu-id="42a45-118">Har försäljningen ökat under den senaste veckan, månaden eller under de sista tre månaderna jämfört med samma period förra året?</span><span class="sxs-lookup"><span data-stu-id="42a45-118">Have sales gone up in the last week, month, or three months, compared to the same period last year?</span></span><br><li> <span data-ttu-id="42a45-119">Vilken var den största försäljningsfakturan som vi bokförda föregående vecka, månad eller de senaste tre månaderna, och till vilken kund skickades räkningen?</span><span class="sxs-lookup"><span data-stu-id="42a45-119">What was the biggest sales invoice we posted last week, month, or last three months, and to which customer did we send the bill?</span></span></li> |
|<span data-ttu-id="42a45-120">Revisor</span><span class="sxs-lookup"><span data-stu-id="42a45-120">Accountant</span></span>|<li> <span data-ttu-id="42a45-121">Vilken var den största försäljningsordern och bokförda fakturan föregående vecka, månad eller de senaste tre månaderna?</span><span class="sxs-lookup"><span data-stu-id="42a45-121">What was the largest sales order and posted invoice last week, month, or last three months?</span></span><br><li> <span data-ttu-id="42a45-122">Har försäljningen ökat under den senaste veckan, månaden eller under de sista tre månaderna jämfört med samma period förra året?</span><span class="sxs-lookup"><span data-stu-id="42a45-122">Have sales gone up in the last week, month, or three months, compared to the same period last year?</span></span> |
|<span data-ttu-id="42a45-123">Orderhandläggare</span><span class="sxs-lookup"><span data-stu-id="42a45-123">Order Processor</span></span>| <span data-ttu-id="42a45-124">Vilken var den största försäljningsordern och bokförda fakturan föregående vecka, månad eller de senaste tre månaderna?</span><span class="sxs-lookup"><span data-stu-id="42a45-124">What was the largest sale order and posted invoice last week, month, or last three months?</span></span>|
|<span data-ttu-id="42a45-125">Kundhanteringschef</span><span class="sxs-lookup"><span data-stu-id="42a45-125">Relationship Manager</span></span>| <span data-ttu-id="42a45-126">Vilket var det största fakturerade beloppet, och till vilken kund skickade vi räkningen?</span><span class="sxs-lookup"><span data-stu-id="42a45-126">What was the largest invoiced amount, and to which customer did we send the bill?</span></span>|
|<span data-ttu-id="42a45-127">Team Member</span><span class="sxs-lookup"><span data-stu-id="42a45-127">Team Member</span></span>| <span data-ttu-id="42a45-128">Visar en hälsningsfras och en länk till produktinformation.</span><span class="sxs-lookup"><span data-stu-id="42a45-128">Displays a greeting, and link to product information.</span></span>|
|<span data-ttu-id="42a45-129">Projektchef</span><span class="sxs-lookup"><span data-stu-id="42a45-129">Project Manager</span></span>| <span data-ttu-id="42a45-130">Visar en hälsningsfras och en länk till produktinformation.</span><span class="sxs-lookup"><span data-stu-id="42a45-130">Displays a greeting, and link to product information.</span></span>|
|<span data-ttu-id="42a45-131">Administratör</span><span class="sxs-lookup"><span data-stu-id="42a45-131">Administrator</span></span>| <span data-ttu-id="42a45-132">Visar en hälsningsfras och en länk till produktinformation.</span><span class="sxs-lookup"><span data-stu-id="42a45-132">Displays a greeting, and link to product information.</span></span>|

## <a name="see-also"></a><span data-ttu-id="42a45-133">Se även</span><span class="sxs-lookup"><span data-stu-id="42a45-133">See Also</span></span>
<span data-ttu-id="42a45-134">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="42a45-134">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>

