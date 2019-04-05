---
title: Designdetaljer - Artikelspårning | Microsoft Docs
description: Det här avsnittet innehåller en översikt av designinformation för artikelspårning.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/12/2018
ms.author: sgroespe
ms.openlocfilehash: 1dce0ea658a2083c3d896fe6324751f63aabce06
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807045"
---
# <a name="design-details-item-tracking"></a><span data-ttu-id="3ebea-103">Designdetaljer: Objektspårning</span><span class="sxs-lookup"><span data-stu-id="3ebea-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="3ebea-104">Eftersom varuflödet i dagens försörjningskedja blir mer och mer komplicerat, är möjligheten att hålla reda på artiklar och allt viktigare för de inblandade företagen.</span><span class="sxs-lookup"><span data-stu-id="3ebea-104">As the flow of goods in today’s supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="3ebea-105">Övervaka en artikels transaktionsflöde är en lagkrav i företag för medicinsk och kemisk leverans, men andra företag kan vilja övervaka produkter med garantier eller utgångsdatum av kundserviceanledningar.</span><span class="sxs-lookup"><span data-stu-id="3ebea-105">Monitoring an item’s transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="3ebea-106">Ett artikelspårningsystem bör ge ett företag en enkel hantering av serie- och partinummer med hänsyn till varje unik vara: när och var den inlevererades, var den lagras, när och var den såldes.</span><span class="sxs-lookup"><span data-stu-id="3ebea-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="3ebea-107">har gradvis utvidgat sin täckning av det här affärskravet och har idag funktioner för hela programmet och utgör en robust kärna att utveckla tillägg på.</span><span class="sxs-lookup"><span data-stu-id="3ebea-107">has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="3ebea-108">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="3ebea-108">In This Section</span></span>  
[<span data-ttu-id="3ebea-109">Designdetaljer: Artikelkopplingsdesign</span><span class="sxs-lookup"><span data-stu-id="3ebea-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
[<span data-ttu-id="3ebea-110">Designdetaljer: Bokföringsstruktur för artikelspårning</span><span class="sxs-lookup"><span data-stu-id="3ebea-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
[<span data-ttu-id="3ebea-111">Designdetaljer: Aktiva kontra historiska artikelspårningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="3ebea-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
[<span data-ttu-id="3ebea-112">Designdetaljer - Sida för artikelspårningsrader</span><span class="sxs-lookup"><span data-stu-id="3ebea-112">Design Details: Item Tracking Lines Page</span></span>](design-details-item-tracking-lines-window.md)  
[<span data-ttu-id="3ebea-113">Designdetaljer: Disposition av artikelspårning</span><span class="sxs-lookup"><span data-stu-id="3ebea-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
[<span data-ttu-id="3ebea-114">Designdetaljer: Artikelkoppling och planering</span><span class="sxs-lookup"><span data-stu-id="3ebea-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
[<span data-ttu-id="3ebea-115">Designdetaljer: Artikelkoppling och reservationer</span><span class="sxs-lookup"><span data-stu-id="3ebea-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="3ebea-116">Designdetaljer: Artikelkoppling i distributionslagret</span><span class="sxs-lookup"><span data-stu-id="3ebea-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)
