---
title: "Designdetaljer - Design av artikelspårning | Microsoft Docs"
description: "Detta avsnit beskriver designen bakom artikelspårningen i Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4d2b4d9e55851564b003ed9c85178237f8689122
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-item-tracking-design"></a><span data-ttu-id="445a9-103">Designdetaljer: Artikelkopplingsdesign</span><span class="sxs-lookup"><span data-stu-id="445a9-103">Design Details: Item Tracking Design</span></span>
<span data-ttu-id="445a9-104">I den första versionen av artikelspårning i [!INCLUDE[d365fin](includes/d365fin_md.md)] 2.60 registrerades serienummer eller partinummer direkt i artikeltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="445a9-104">In the first version of Item Tracking in [!INCLUDE[d365fin](includes/d365fin_md.md)] 2.60, serial numbers or lot numbers were recorded directly on item ledger entries.</span></span> <span data-ttu-id="445a9-105">Designen gav fullständig tillgänglighetsinformation och enkel spårning av historiska transaktioner, men den saknade flexibilitet och funktioner.</span><span class="sxs-lookup"><span data-stu-id="445a9-105">This design provided full availability information and simple tracking of historic entries, but it lacked flexibility and functionality.</span></span>  

<span data-ttu-id="445a9-106">Från [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.00 där artikelspårningsfunktion fanns i en separat objektstruktur med invecklade länkar till bokförda dokument och artikeltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="445a9-106">From [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.00, item tracking functionality was in a separate object structure with intricate links to posted documents and item ledger entries.</span></span> <span data-ttu-id="445a9-107">Design var flexibel och rik på funktioner, men artikelspårningstransaktioner var ingick inte helt i dispositionsberäkningarna.</span><span class="sxs-lookup"><span data-stu-id="445a9-107">This design was flexible and rich in functionality, but item tracking entries were not fully involved in availability calculations.</span></span>  

<span data-ttu-id="445a9-108">Sedan [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60 är artikelspårningsfunktionen integrerade med reservationssystemet, som hanterar reservation, orderspårning och åtgärdsmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="445a9-108">Since [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60, item tracking functionality is integrated with the reservation system, which handles reservation, order tracking, and action messaging.</span></span> <span data-ttu-id="445a9-109">Mer information finns i "Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden" i "Designdetaljer: Leveransplanering".</span><span class="sxs-lookup"><span data-stu-id="445a9-109">For more information, see “Design Details: Reservation, Order Tracking, and Action Messaging” in “Design Details: Supply Planning”.</span></span>  

<span data-ttu-id="445a9-110">Den senaste designen innehåller artikelspårningstransaktioner i beräkningar av den totala tillgängligheten i hela systemet, inklusive planering, produktion och lagerstyrning.</span><span class="sxs-lookup"><span data-stu-id="445a9-110">This latest design incorporates item tracking entries in total availability calculations throughout the system, including planning, manufacturing, and warehousing.</span></span> <span data-ttu-id="445a9-111">Det gamla konceptet att ha serie- och partinummer på artikeltransaktionerna återinförs för att säkerställa enkel tillgång till historiska data i artikelspårningssyfte.</span><span class="sxs-lookup"><span data-stu-id="445a9-111">The old concept of carrying serial and lot numbers on the item ledger entries is reintroduced to ensure simple access to historical data for item tracking purposes.</span></span> <span data-ttu-id="445a9-112">I samband med artikelspårningförbättringar i [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60 utvidgades reservationssystemet till nätverksenheter för icke-order, till exempel journaler, fakturor och kreditnotor.</span><span class="sxs-lookup"><span data-stu-id="445a9-112">In connection with item tracking improvements in [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60, the reservation system was expanded to non-order network entities, such as journals, invoices, and credit memos.</span></span>  

<span data-ttu-id="445a9-113">Med tillägg av serie- eller partinummer hanterar reservationssystemet permanenta artikelattribut, samtidigt som det även hanterar intermittenta länkar mellan tillgång och efterfrågan i form av orderspårningposter och reservationstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="445a9-113">With the addition of serial or lot numbers, the reservation system handles permanent item attributes while also handling intermittent links between supply and demand in the form of order tracking entries and reservation entries.</span></span> <span data-ttu-id="445a9-114">En annan egenskap som skiljer sig åt för serie- och partinummer jämfört med konventionella reservationdata är att de kan bokföras, antingen delvis eller helt.</span><span class="sxs-lookup"><span data-stu-id="445a9-114">Another different characteristic of serial or lot numbers compared to the conventional reservation data is the fact that they can be posted, either partially or fully.</span></span> <span data-ttu-id="445a9-115">Därför fungerar tabellen **Reservationstransaktion** (T337) nu med en relaterad tabell, tabellen **Spårningsspecifikation** (T336), som hanterar och visar summan av aktiva och bokförda artikelspårningsantal.</span><span class="sxs-lookup"><span data-stu-id="445a9-115">Therefore, the **Reservation Entry** table (T337) now works with a related table, the **Tracking Specification** table (T336), which manages and displays summing across active and posted item tracking quantities.</span></span> <span data-ttu-id="445a9-116">Mer information finns i [Designdetaljer: Aktiva kontra historiska artikelspårningstransaktioner](design-details-active-versus-historic-item-tracking-entries.md)</span><span class="sxs-lookup"><span data-stu-id="445a9-116">For more information, see [Design Details: Active versus Historic Item Tracking Entries](design-details-active-versus-historic-item-tracking-entries.md).</span></span>  

<span data-ttu-id="445a9-117">Följande diagram skisserar utformningen av artikelspårningsfunktionen i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="445a9-117">The following diagram outlines the design of item tracking functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="445a9-118">![Design för artikelspårning](media/design_details_item_tracking_design.png "design_details_item_tracking_design")</span><span class="sxs-lookup"><span data-stu-id="445a9-118">![Item tracking design](media/design_details_item_tracking_design.png "design_details_item_tracking_design")</span></span>  

<span data-ttu-id="445a9-119">Det centrala bokföringsobjektet omformas för att hantera den unika underklassificeringen av en dokumentrad i form av serie- eller partinummer, och särskilda relationstabeller läggs till för att skapa en-till-flera-relationer mellan bokförda dokument och deras delade artikeltransaktioner och värdetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="445a9-119">The central posting object is redesigned to handle the unique subclassification of a document line in the form of serial or lot numbers, and special relation tables are added to create the one-to-many relations between posted documents and their split item ledger entries and value ledger entries.</span></span>  

<span data-ttu-id="445a9-120">Kodenhet 22, **Artikeljournal – bokför rad**, delar nu bokföringen enligt de artikelspårningsnummer som anges på dokumentraden.</span><span class="sxs-lookup"><span data-stu-id="445a9-120">Codeunit 22, **Item Jnl. – Post Line**, now splits the posting according to the item tracking numbers that are specified on the document line.</span></span> <span data-ttu-id="445a9-121">Varje unikt artikelspårningsnummer på raden skapar en egen artikeltransaktion för artikeln.</span><span class="sxs-lookup"><span data-stu-id="445a9-121">Each unique item tracking number on the line creates its own item ledger entry for the item.</span></span> <span data-ttu-id="445a9-122">Det betyder att länken från den bokförda dokumentraden till de associerade artikeltransaktionerna nu är en-till-flera-relation.</span><span class="sxs-lookup"><span data-stu-id="445a9-122">This means that the link from the posted document line to the associated item ledger entries is now a one-to-many relation.</span></span> <span data-ttu-id="445a9-123">Relationen hanteras av följande relationstabeller för artikelspårning.</span><span class="sxs-lookup"><span data-stu-id="445a9-123">This relation is handled by the following item tracking relation tables.</span></span>  

|<span data-ttu-id="445a9-124">Fält</span><span class="sxs-lookup"><span data-stu-id="445a9-124">Field</span></span>|<span data-ttu-id="445a9-125">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="445a9-125">Description</span></span>|  
|---------------|---------------------------------------|  
|<span data-ttu-id="445a9-126">**Artikeltrans. relation** (T6507)</span><span class="sxs-lookup"><span data-stu-id="445a9-126">**Item Entry Relation** (T6507)</span></span>|<span data-ttu-id="445a9-127">Relaterar levererade eller inlevererade rader till artikeltransaktioner</span><span class="sxs-lookup"><span data-stu-id="445a9-127">Relates shipped or received lines to item ledger entries</span></span>|  
|<span data-ttu-id="445a9-128">**Värdetrans. relation** (T6508)</span><span class="sxs-lookup"><span data-stu-id="445a9-128">**Value Entry Relation** (T6508)</span></span>|<span data-ttu-id="445a9-129">Relaterar fakturerade rader till värdetransaktioner</span><span class="sxs-lookup"><span data-stu-id="445a9-129">Relates invoiced lines to value entries</span></span>|  

<span data-ttu-id="445a9-130">Mer information finns i [Designdetaljer: Bokföringsstruktur för artikelspårning](design-details-item-tracking-posting-structure.md).</span><span class="sxs-lookup"><span data-stu-id="445a9-130">For more information, see [Design Details: Item Tracking Posting Structure](design-details-item-tracking-posting-structure.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="445a9-131">Se även</span><span class="sxs-lookup"><span data-stu-id="445a9-131">See Also</span></span>  
[<span data-ttu-id="445a9-132">Designdetaljer: Artikelkoppling</span><span class="sxs-lookup"><span data-stu-id="445a9-132">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)
