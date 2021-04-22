---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7ead218d289668d893a659f730a4c64e31195f10
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788595"
---
<span data-ttu-id="bdde1-101">När du anger datum och tid som datum och tid som kombineras till ett enda fält, måste du ange ett blanksteg mellan datumet och tiden.</span><span class="sxs-lookup"><span data-stu-id="bdde1-101">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="bdde1-102">Datumdelen kan bara innehålla blanksteg i form av officiella datumavgränsare för din regionsinställning.</span><span class="sxs-lookup"><span data-stu-id="bdde1-102">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="bdde1-103">Tiden kan innehålla blanksteg runt AM/PM-indikatorn i relevanta regionala inställningar.</span><span class="sxs-lookup"><span data-stu-id="bdde1-103">The time can contain spaces around the AM/PM indicator in relevant regional settings.</span></span>

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

<span data-ttu-id="bdde1-104">Listan nedan innehåller de olika sätt som du kan ange datum och tid på och en förklaring av hur de ska tolkas.</span><span class="sxs-lookup"><span data-stu-id="bdde1-104">The following table lists the various ways in which you can enter datetimes and how they're interpreted.</span></span>  

|<span data-ttu-id="bdde1-105">Transaktion</span><span class="sxs-lookup"><span data-stu-id="bdde1-105">Entry</span></span>|<span data-ttu-id="bdde1-106">Tolkning</span><span class="sxs-lookup"><span data-stu-id="bdde1-106">Interpretation</span></span>|
|---------------|------------------------|
|<span data-ttu-id="bdde1-107">08-01-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="bdde1-107">08-01-2022 05:48:12 PM</span></span>|<span data-ttu-id="bdde1-108">08\-01\-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="bdde1-108">08\-01\-2022 05:48:12 PM</span></span>|
|<span data-ttu-id="bdde1-109">131222 132455</span><span class="sxs-lookup"><span data-stu-id="bdde1-109">131222 132455</span></span>|<span data-ttu-id="bdde1-110">13-12-22 13:24:55</span><span class="sxs-lookup"><span data-stu-id="bdde1-110">13-12-22 13:24:55</span></span>|
|<span data-ttu-id="bdde1-111">1-12-22 10</span><span class="sxs-lookup"><span data-stu-id="bdde1-111">1-12-22 10</span></span>|<span data-ttu-id="bdde1-112">01-12-22 10:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-112">01-12-22 10:00:00</span></span>|
|<span data-ttu-id="bdde1-113">1.12.22 5</span><span class="sxs-lookup"><span data-stu-id="bdde1-113">1.12.22 5</span></span>|<span data-ttu-id="bdde1-114">01-12-22 05:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-114">01-12-22 05:00:00</span></span>|
|<span data-ttu-id="bdde1-115">1.12.22</span><span class="sxs-lookup"><span data-stu-id="bdde1-115">1.12.22</span></span>|<span data-ttu-id="bdde1-116">01-12-22 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-116">01-12-22 00:00:00</span></span>|
|<span data-ttu-id="bdde1-117">11 12</span><span class="sxs-lookup"><span data-stu-id="bdde1-117">11 12</span></span>|<span data-ttu-id="bdde1-118">innevarande år-innevarande månad-11 12:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-118">11-current month-current year 12:00:00</span></span>|
|<span data-ttu-id="bdde1-119">1112 12</span><span class="sxs-lookup"><span data-stu-id="bdde1-119">1112 12</span></span>|<span data-ttu-id="bdde1-120">innevarande år-12-11 12:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-120">11-12-current year 12:00:00</span></span>|
|<span data-ttu-id="bdde1-121">d eller dagens datum</span><span class="sxs-lookup"><span data-stu-id="bdde1-121">t or today</span></span>|<span data-ttu-id="bdde1-122">dagens datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-122">today's date 00:00:00</span></span>|
|<span data-ttu-id="bdde1-123">d tid</span><span class="sxs-lookup"><span data-stu-id="bdde1-123">t time</span></span>|<span data-ttu-id="bdde1-124">dagens datum aktuell tid</span><span class="sxs-lookup"><span data-stu-id="bdde1-124">today's date actual time</span></span>|
|<span data-ttu-id="bdde1-125">d 10:30</span><span class="sxs-lookup"><span data-stu-id="bdde1-125">t 10:30</span></span>|<span data-ttu-id="bdde1-126">dagens datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-126">today's date 10:30:00</span></span>|
|<span data-ttu-id="bdde1-127">d 03:03:03</span><span class="sxs-lookup"><span data-stu-id="bdde1-127">t 3:3:3</span></span>|<span data-ttu-id="bdde1-128">dagens datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="bdde1-128">today's date 03:03:03</span></span>|
|<span data-ttu-id="bdde1-129">a eller arbetsdagens datum</span><span class="sxs-lookup"><span data-stu-id="bdde1-129">w or workdate</span></span>|<span data-ttu-id="bdde1-130">arbetsdagens datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-130">the working date 00:00:00</span></span>|
|<span data-ttu-id="bdde1-131">m eller måndag</span><span class="sxs-lookup"><span data-stu-id="bdde1-131">m or Monday</span></span>|<span data-ttu-id="bdde1-132">måndag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-132">Monday of the current week 00:00:00</span></span>|
|<span data-ttu-id="bdde1-133">ti eller tisdag</span><span class="sxs-lookup"><span data-stu-id="bdde1-133">tu or Tuesday</span></span>|<span data-ttu-id="bdde1-134">tisdag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-134">Tuesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="bdde1-135">on eller onsdag</span><span class="sxs-lookup"><span data-stu-id="bdde1-135">we or Wednesday</span></span>|<span data-ttu-id="bdde1-136">onsdag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-136">Wednesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="bdde1-137">to eller torsdag</span><span class="sxs-lookup"><span data-stu-id="bdde1-137">th or Thursday</span></span>|<span data-ttu-id="bdde1-138">torsdag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-138">Thursday of the current week 00:00:00</span></span>|
|<span data-ttu-id="bdde1-139">fr eller fredag</span><span class="sxs-lookup"><span data-stu-id="bdde1-139">f or Friday</span></span>|<span data-ttu-id="bdde1-140">fredag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-140">Friday of the current week 00:00:00</span></span>|
|<span data-ttu-id="bdde1-141">lö eller lördag</span><span class="sxs-lookup"><span data-stu-id="bdde1-141">s or Saturday</span></span>|<span data-ttu-id="bdde1-142">lördag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-142">Saturday of the current week 00:00:00</span></span>|
|<span data-ttu-id="bdde1-143">sö eller söndag</span><span class="sxs-lookup"><span data-stu-id="bdde1-143">su or Sunday</span></span>|<span data-ttu-id="bdde1-144">söndag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-144">Sunday of the current week 00:00:00</span></span>|
|<span data-ttu-id="bdde1-145">ti 10:30</span><span class="sxs-lookup"><span data-stu-id="bdde1-145">tu 10:30</span></span>|<span data-ttu-id="bdde1-146">tisdag i innevarande vecka 10:30:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-146">Tuesday of the current week 10:30:00</span></span>|
|<span data-ttu-id="bdde1-147">ti 03:03:03</span><span class="sxs-lookup"><span data-stu-id="bdde1-147">tu 3:3:3</span></span>|<span data-ttu-id="bdde1-148">tisdag i innevarande vecka 03:03:03</span><span class="sxs-lookup"><span data-stu-id="bdde1-148">Tuesday of the current week 03:03:03</span></span>|
|<span data-ttu-id="bdde1-149">t23 t</span><span class="sxs-lookup"><span data-stu-id="bdde1-149">t23 t</span></span>|<span data-ttu-id="bdde1-150">Tisdag i en vecka 23 av arbetsdatumets år, aktuell tid på dagen</span><span class="sxs-lookup"><span data-stu-id="bdde1-150">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="bdde1-151">t23</span><span class="sxs-lookup"><span data-stu-id="bdde1-151">t23</span></span>|<span data-ttu-id="bdde1-152">Tisdag av vecka 23 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="bdde1-152">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="bdde1-153">t 23</span><span class="sxs-lookup"><span data-stu-id="bdde1-153">t 23</span></span>|<span data-ttu-id="bdde1-154">Idag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="bdde1-154">Today 23:00:00</span></span>|
|<span data-ttu-id="bdde1-155">t-1</span><span class="sxs-lookup"><span data-stu-id="bdde1-155">t-1</span></span>|<span data-ttu-id="bdde1-156">Tisdag av vecka 1 arbetsdatumets år</span><span class="sxs-lookup"><span data-stu-id="bdde1-156">Tuesday of week 1 of the work date year</span></span>|


