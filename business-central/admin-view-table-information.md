---
title: Visa tabellinformation
description: Lär dig mer om hur du kan visa information om databaslås direkt från klientgränssnittet i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 72e220aa310515c665ce85bd43f4ebd3aac157d0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922273"
---
# <a name="viewing-table-information"></a><span data-ttu-id="cf07a-103">Visa tabellinformation</span><span class="sxs-lookup"><span data-stu-id="cf07a-103">Viewing Table Information</span></span>

<span data-ttu-id="cf07a-104">Sidan **8700 tabellInformation** innehåller information om alla system- och affärstabeller i en Business Central-lösning.</span><span class="sxs-lookup"><span data-stu-id="cf07a-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="cf07a-105">I synnerhet visar sidan information om mängden data som tabellerna innehåller.</span><span class="sxs-lookup"><span data-stu-id="cf07a-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="cf07a-106">Den här informationen är användbar för att felsöka prestandaproblem, eftersom du kan se fördelningen av datastorlek över tabeller.</span><span class="sxs-lookup"><span data-stu-id="cf07a-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="cf07a-107">Visa tabellinformation</span><span class="sxs-lookup"><span data-stu-id="cf07a-107">Viewing table information</span></span>

<span data-ttu-id="cf07a-108">Du öppnar den här sidan genom att välja ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **tabellinformation** och sedan välja relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="cf07a-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="cf07a-109">I följande tabell beskrivs de olika tabellerna som anges:</span><span class="sxs-lookup"><span data-stu-id="cf07a-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="cf07a-110">Kolumn</span><span class="sxs-lookup"><span data-stu-id="cf07a-110">Column</span></span>|<span data-ttu-id="cf07a-111">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="cf07a-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="cf07a-112">Företagsnamn</span><span class="sxs-lookup"><span data-stu-id="cf07a-112">Company Name</span></span>|<span data-ttu-id="cf07a-113">Namnet på företaget, om det finns något, som tabellen tillhör.</span><span class="sxs-lookup"><span data-stu-id="cf07a-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="cf07a-114">Tabellnamn</span><span class="sxs-lookup"><span data-stu-id="cf07a-114">Table Name</span></span>|<span data-ttu-id="cf07a-115">Tabellens namn.</span><span class="sxs-lookup"><span data-stu-id="cf07a-115">The name of the table.</span></span>|
|<span data-ttu-id="cf07a-116">Tabellnr</span><span class="sxs-lookup"><span data-stu-id="cf07a-116">Table No.</span></span>|<span data-ttu-id="cf07a-117">ID:t för tabellen.</span><span class="sxs-lookup"><span data-stu-id="cf07a-117">The ID of the table</span></span>|
|<span data-ttu-id="cf07a-118">Nr</span><span class="sxs-lookup"><span data-stu-id="cf07a-118">No.</span></span> <span data-ttu-id="cf07a-119">av poster</span><span class="sxs-lookup"><span data-stu-id="cf07a-119">of Records</span></span>|<span data-ttu-id="cf07a-120">Det totala antalet poster som lagras i tabellen.</span><span class="sxs-lookup"><span data-stu-id="cf07a-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="cf07a-121">Poststorlek</span><span class="sxs-lookup"><span data-stu-id="cf07a-121">Record Size</span></span>|<span data-ttu-id="cf07a-122">Den genomsnittliga poststorleken i KB/post.</span><span class="sxs-lookup"><span data-stu-id="cf07a-122">The average record size in KB/record.</span></span> <span data-ttu-id="cf07a-123">Värdet beräknas med hjälp av följande formel: 1024 (storlek)/(No.</span><span class="sxs-lookup"><span data-stu-id="cf07a-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="cf07a-124">av poster).</span><span class="sxs-lookup"><span data-stu-id="cf07a-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="cf07a-125">Se även</span><span class="sxs-lookup"><span data-stu-id="cf07a-125">See Also</span></span>

[<span data-ttu-id="cf07a-126">Kontrollera sidor</span><span class="sxs-lookup"><span data-stu-id="cf07a-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="cf07a-127">Prestandaartiklar för utvecklare</span><span class="sxs-lookup"><span data-stu-id="cf07a-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  
