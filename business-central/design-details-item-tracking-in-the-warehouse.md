---
title: Designdetaljer - Artikelspårning i distributionslagret | Microsoft Docs
description: Hantering av serienummer- eller partinummerbruk är främst en distributionslageruppgift, och därför har alla ankommande och avgående distributionslagerdokument standardfunktioner för att tilldela och välja artikelspårningsnummer. Men eftersom reserveringssystemet baseras på artikeltransaktioner stöds inte lageraktivitetsdokument som bara registrerar distributionslagertransaktioner helt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b7fdb0d6495f1512e1ab3bf80eb76a5dad9d87e5
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880190"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a><span data-ttu-id="af966-104">Designdetaljer: Artikelspårning i distributionslagret</span><span class="sxs-lookup"><span data-stu-id="af966-104">Design Details: Item Tracking in the Warehouse</span></span>
<span data-ttu-id="af966-105">Hantering av serienummer- eller partinummerbruk är främst en distributionslageruppgift, och därför har alla ankommande och avgående distributionslagerdokument standardfunktioner för att tilldela och välja artikelspårningsnummer.</span><span class="sxs-lookup"><span data-stu-id="af966-105">Serial number and lot number handling is primarily a warehouse task and therefore all inbound and outbound warehouse documents have standard functionality for assigning and selecting item tracking numbers.</span></span>  

<span data-ttu-id="af966-106">Men eftersom reserveringssystemet baseras på artikeltransaktioner stöds inte lageraktivitetsdokument som bara registrerar distributionslagertransaktioner helt.</span><span class="sxs-lookup"><span data-stu-id="af966-106">However, because the reservation system is based on item ledger entries, warehouse activity documents that register only warehouse entries are not fully supported.</span></span> <span data-ttu-id="af966-107">Eftersom reservationer och artikelspårningsnummer endast kan hanteras på lagerställenivå, och inte på lagerplats- och zonnivå, kan sidan **Artikelspårningsrader** inte öppnas från distributionslageraktivitetsdokument.</span><span class="sxs-lookup"><span data-stu-id="af966-107">Because reservations and item tracking numbers can be handled only at the location level, not at the bin and zone level, the **Item Tracking Lines** page cannot be opened from warehouse activity documents.</span></span> <span data-ttu-id="af966-108">Samma gäller för sidan **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="af966-108">The same applies to the **Reservation** page.</span></span>  

<span data-ttu-id="af966-109">När ett serie- eller partinummer har lagts till i en artikel på en lagerplats kan det flyttas och grupperas fritt i distributionslagret med en oberoende artikelspårningstruktur som är orelaterad till reservationsystemet.</span><span class="sxs-lookup"><span data-stu-id="af966-109">After a serial or lot number has been added to an item at a warehouse location, it can be moved and reclassified freely within the warehouse by using an independent item tracking structure that is unrelated to the reservation system.</span></span> <span data-ttu-id="af966-110">Fälten **Serienr** och **Partinr** nås direkt på distributionslagerdokumentrader.</span><span class="sxs-lookup"><span data-stu-id="af966-110">**Serial No.** and **Lot No.** fields are accessed directly on warehouse document lines.</span></span> <span data-ttu-id="af966-111">När serie- eller partinumret senare ingår i avgående bokföring, synkroniseras det med reservationssystemet som en del av vanlig lagerplatsjustering.</span><span class="sxs-lookup"><span data-stu-id="af966-111">When the serial or lot number later partakes in outbound posting, it is synchronized with the reservation system as a part of ordinary bin adjustment.</span></span> <span data-ttu-id="af966-112">Mer information finns i [Designdetaljer: Integrering med lager](design-details-integration-with-inventory.md)</span><span class="sxs-lookup"><span data-stu-id="af966-112">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="af966-113">Däremot beaktar reservationssystemet distributionslageraktiviteter när det beräknar disposition.</span><span class="sxs-lookup"><span data-stu-id="af966-113">However, the reservation system does take warehouse activities into consideration when it calculates availability.</span></span> <span data-ttu-id="af966-114">Till exempel kan artiklar som tilldelats till plockningar, eller som registrerats som plockade,, inte reserveras.</span><span class="sxs-lookup"><span data-stu-id="af966-114">For example, items that are allocated to picks, or registered as picked, cannot be reserved.</span></span> <span data-ttu-id="af966-115">Mer information finns i [Designdetaljer: disposition i distributionslagret](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="af966-115">For more information, see [Design Details: Warehouse Availability](design-details-availability-in-the-warehouse.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="af966-116">Se även</span><span class="sxs-lookup"><span data-stu-id="af966-116">See Also</span></span>  
[<span data-ttu-id="af966-117">Designdetaljer: Artikelkoppling</span><span class="sxs-lookup"><span data-stu-id="af966-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="af966-118">Designdetaljer: Integrering med lager</span><span class="sxs-lookup"><span data-stu-id="af966-118">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)  
[<span data-ttu-id="af966-119">Designdetaljer - Disposition i distributionslagret</span><span class="sxs-lookup"><span data-stu-id="af966-119">Design Details: Warehouse Availability</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="af966-120">Designdetaljer: Artikelkopplingsdesign</span><span class="sxs-lookup"><span data-stu-id="af966-120">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)
