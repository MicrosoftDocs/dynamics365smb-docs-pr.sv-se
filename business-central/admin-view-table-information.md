---
title: Visa tabellinformation
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/20/2020
ms.author: jswymer
ms.openlocfilehash: de93063a60e6b64405b1491a67489c8bfa4657ad
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275324"
---
# <a name="viewing-table-information"></a><span data-ttu-id="465dd-102">Visa tabellinformation</span><span class="sxs-lookup"><span data-stu-id="465dd-102">Viewing Table Information</span></span>

<span data-ttu-id="465dd-103">Sidan **8700 tabellInformation** innehåller information om alla system- och affärstabeller i en Business Central-lösning.</span><span class="sxs-lookup"><span data-stu-id="465dd-103">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="465dd-104">I synnerhet visar sidan information om mängden data som tabellerna innehåller.</span><span class="sxs-lookup"><span data-stu-id="465dd-104">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="465dd-105">Den här informationen är användbar för att felsöka prestandaproblem, eftersom du kan se fördelningen av datastorlek över tabeller.</span><span class="sxs-lookup"><span data-stu-id="465dd-105">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="465dd-106">Visa tabellinformation</span><span class="sxs-lookup"><span data-stu-id="465dd-106">Viewing table information</span></span>

<span data-ttu-id="465dd-107">Du öppnar den här sidan genom att välja ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **tabellinformation** och sedan välja relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="465dd-107">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="465dd-108">I följande tabell beskrivs de olika tabellerna som anges:</span><span class="sxs-lookup"><span data-stu-id="465dd-108">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="465dd-109">Kolumn</span><span class="sxs-lookup"><span data-stu-id="465dd-109">Column</span></span>|<span data-ttu-id="465dd-110">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="465dd-110">Description</span></span>|
|------|-----------|
|<span data-ttu-id="465dd-111">Företagsnamn</span><span class="sxs-lookup"><span data-stu-id="465dd-111">Company Name</span></span>|<span data-ttu-id="465dd-112">Namnet på företaget, om det finns något, som tabellen tillhör.</span><span class="sxs-lookup"><span data-stu-id="465dd-112">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="465dd-113">Tabellnamn</span><span class="sxs-lookup"><span data-stu-id="465dd-113">Table Name</span></span>|<span data-ttu-id="465dd-114">Tabellens namn.</span><span class="sxs-lookup"><span data-stu-id="465dd-114">The name of the table.</span></span>|
|<span data-ttu-id="465dd-115">Tabellnr</span><span class="sxs-lookup"><span data-stu-id="465dd-115">Table No.</span></span>|<span data-ttu-id="465dd-116">ID:t för tabellen.</span><span class="sxs-lookup"><span data-stu-id="465dd-116">The ID of the table</span></span>|
|<span data-ttu-id="465dd-117">Nr</span><span class="sxs-lookup"><span data-stu-id="465dd-117">No.</span></span> <span data-ttu-id="465dd-118">av poster</span><span class="sxs-lookup"><span data-stu-id="465dd-118">of Records</span></span>|<span data-ttu-id="465dd-119">Det totala antalet poster som lagras i tabellen.</span><span class="sxs-lookup"><span data-stu-id="465dd-119">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="465dd-120">Poststorlek</span><span class="sxs-lookup"><span data-stu-id="465dd-120">Record Size</span></span>|<span data-ttu-id="465dd-121">Den genomsnittliga poststorleken i KB/post.</span><span class="sxs-lookup"><span data-stu-id="465dd-121">The average record size in KB/record.</span></span> <span data-ttu-id="465dd-122">Värdet beräknas med hjälp av följande formel: 1024 (storlek)/(antal</span><span class="sxs-lookup"><span data-stu-id="465dd-122">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="465dd-123">poster).</span><span class="sxs-lookup"><span data-stu-id="465dd-123">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="465dd-124">Se även</span><span class="sxs-lookup"><span data-stu-id="465dd-124">See Also</span></span>

[<span data-ttu-id="465dd-125">Kontrollera sidor</span><span class="sxs-lookup"><span data-stu-id="465dd-125">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="465dd-126">Prestandaartiklar för utvecklare</span><span class="sxs-lookup"><span data-stu-id="465dd-126">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  
