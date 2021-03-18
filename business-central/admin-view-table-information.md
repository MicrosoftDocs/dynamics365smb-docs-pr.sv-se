---
title: Visa tabellinformation
description: Lär dig mer om hur du kan visa information om databaslås direkt från klientgränssnittet i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: a4695594573056ec492bc15c29d1b6fca3100e97
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388680"
---
# <a name="viewing-table-information"></a><span data-ttu-id="6fb81-103">Visa tabellinformation</span><span class="sxs-lookup"><span data-stu-id="6fb81-103">Viewing Table Information</span></span>

<span data-ttu-id="6fb81-104">Sidan **8700 tabellInformation** innehåller information om alla system- och affärstabeller i en Business Central-lösning.</span><span class="sxs-lookup"><span data-stu-id="6fb81-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="6fb81-105">I synnerhet visar sidan information om mängden data som tabellerna innehåller.</span><span class="sxs-lookup"><span data-stu-id="6fb81-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="6fb81-106">Den här informationen är användbar för att felsöka prestandaproblem, eftersom du kan se fördelningen av datastorlek över tabeller.</span><span class="sxs-lookup"><span data-stu-id="6fb81-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="6fb81-107">Visa tabellinformation</span><span class="sxs-lookup"><span data-stu-id="6fb81-107">Viewing table information</span></span>

<span data-ttu-id="6fb81-108">Du öppnar den här sidan genom att välja ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **tabellinformation** och sedan välja relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="6fb81-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="6fb81-109">I följande tabell beskrivs de olika tabellerna som anges:</span><span class="sxs-lookup"><span data-stu-id="6fb81-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="6fb81-110">Kolumn</span><span class="sxs-lookup"><span data-stu-id="6fb81-110">Column</span></span>|<span data-ttu-id="6fb81-111">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="6fb81-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="6fb81-112">Företagsnamn</span><span class="sxs-lookup"><span data-stu-id="6fb81-112">Company Name</span></span>|<span data-ttu-id="6fb81-113">Namnet på företaget, om det finns något, som tabellen tillhör.</span><span class="sxs-lookup"><span data-stu-id="6fb81-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="6fb81-114">Tabellnamn</span><span class="sxs-lookup"><span data-stu-id="6fb81-114">Table Name</span></span>|<span data-ttu-id="6fb81-115">Tabellens namn.</span><span class="sxs-lookup"><span data-stu-id="6fb81-115">The name of the table.</span></span>|
|<span data-ttu-id="6fb81-116">Tabellnr</span><span class="sxs-lookup"><span data-stu-id="6fb81-116">Table No.</span></span>|<span data-ttu-id="6fb81-117">ID:t för tabellen.</span><span class="sxs-lookup"><span data-stu-id="6fb81-117">The ID of the table</span></span>|
|<span data-ttu-id="6fb81-118">Nr</span><span class="sxs-lookup"><span data-stu-id="6fb81-118">No.</span></span> <span data-ttu-id="6fb81-119">av poster</span><span class="sxs-lookup"><span data-stu-id="6fb81-119">of Records</span></span>|<span data-ttu-id="6fb81-120">Det totala antalet poster som lagras i tabellen.</span><span class="sxs-lookup"><span data-stu-id="6fb81-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="6fb81-121">Poststorlek</span><span class="sxs-lookup"><span data-stu-id="6fb81-121">Record Size</span></span>|<span data-ttu-id="6fb81-122">Den genomsnittliga poststorleken i KB/post.</span><span class="sxs-lookup"><span data-stu-id="6fb81-122">The average record size in KB/record.</span></span> <span data-ttu-id="6fb81-123">Värdet beräknas med hjälp av följande formel: 1024 (storlek)/(No.</span><span class="sxs-lookup"><span data-stu-id="6fb81-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="6fb81-124">av poster).</span><span class="sxs-lookup"><span data-stu-id="6fb81-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="6fb81-125">Se även</span><span class="sxs-lookup"><span data-stu-id="6fb81-125">See Also</span></span>

[<span data-ttu-id="6fb81-126">Kontrollera sidor</span><span class="sxs-lookup"><span data-stu-id="6fb81-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="6fb81-127">Prestandaartiklar för utvecklare</span><span class="sxs-lookup"><span data-stu-id="6fb81-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]