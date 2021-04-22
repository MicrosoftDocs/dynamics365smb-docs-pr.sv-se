---
title: Stäng artikeltransaktioner som kommit från att använda fast koppling
description: Lär dig skapa en fast koppling mellan en inkommande transaktion och den ursprungliga utgående transaktionen i artikeljournalen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4fac4871fdf42210dfd48ca6dd7d9c2fede0c7ef
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788289"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="5c38e-103">Stäng öppna artikeltransaktioner som skapas från en fast koppling i artikeljournalen</span><span class="sxs-lookup"><span data-stu-id="5c38e-103">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>

<span data-ttu-id="5c38e-104">Du kan använda fältet **Kopplas från löpnr** på sidan **Artikeljournal** för att skapa en fast koppling mellan en inkommande transaktion och den ursprungliga utgående transaktionen.</span><span class="sxs-lookup"><span data-stu-id="5c38e-104">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="5c38e-105">Till exempel, för att korrigera utgående transaktion eller bearbeta dess retur.</span><span class="sxs-lookup"><span data-stu-id="5c38e-105">For example, to correct the outbound transaction or to process its return.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="5c38e-106">Fast koppling som gjorts på det här sättet gäller endast kostnaden, inte antal.</span><span class="sxs-lookup"><span data-stu-id="5c38e-106">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="5c38e-107">På så sätt kommer den bokförda positiv artikeltransaktion inte avsluta det kopplade utgående transaktion, och att stå öppen.</span><span class="sxs-lookup"><span data-stu-id="5c38e-107">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="5c38e-108">Detta gäller också när du bokför en fast koppling för en positiv transaktion på en negativ transaktion som inte har avslutats av en vanlig positiva transaktion, kommer både negativ och de positiva transaktionerna finns kvar öppna.</span><span class="sxs-lookup"><span data-stu-id="5c38e-108">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>
> <span data-ttu-id="5c38e-109">Det innebär att du inte kan avsluta en lagerperiod, om sådan transaktion finns.</span><span class="sxs-lookup"><span data-stu-id="5c38e-109">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="5c38e-110">Du kan ändra och återanvända kopplingstransaktioner under vissa omständigheter med hjälp av sidan **Kopplingsförslag**.</span><span class="sxs-lookup"><span data-stu-id="5c38e-110">You can change and reapply application entries under certain conditions by using the **Application Worksheet** page.</span></span>  

<span data-ttu-id="5c38e-111">I följande procedur beskrivs hur du avslutar sådana transaktioner genom att utföra två korrigerande bokföringar i artikeljournalen.</span><span class="sxs-lookup"><span data-stu-id="5c38e-111">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="5c38e-112">Om du vill avsluta öppna artikeltransaktioner som skapas från ett fast koppling i artikeljournalen</span><span class="sxs-lookup"><span data-stu-id="5c38e-112">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1. <span data-ttu-id="5c38e-113">Använd fältet **Kopplas från löpnr** om du vill bokföra en positiv justering med motsvarande antal.</span><span class="sxs-lookup"><span data-stu-id="5c38e-113">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="5c38e-114">Denna åtgärd stänger den ursprungliga negativ transaktion med en fast koppling.</span><span class="sxs-lookup"><span data-stu-id="5c38e-114">This closes the original negative entry with a fixed application.</span></span>  

    <span data-ttu-id="5c38e-115">Fältet **Transaktion gäller från** anger antalet utgående artikeltransaktioner vars kostnad vidarebefordrats till den inkommande artikeltransaktionen när du bokför en inkommande transaktion av typen **Positiv just.** eller **Inköp** med artikeljournalen.</span><span class="sxs-lookup"><span data-stu-id="5c38e-115">The **Applies-from Entry** field specifies the number of the outbound item ledger entry whose cost is forwarded to the inbound item ledger entry when you post an inbound transaction of type **Positive Adjmt.** or **Purchase** with the item journal.</span></span>  
2. <span data-ttu-id="5c38e-116">Använd fältet **Kopplas till löpnr** om du vill bokföra en negativ justering.</span><span class="sxs-lookup"><span data-stu-id="5c38e-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="5c38e-117">Denna åtgärd stänger den korrigerande positiva transaktionen med en fast koppling.</span><span class="sxs-lookup"><span data-stu-id="5c38e-117">This closes the original corrective positive entry with a fixed application.</span></span>  

    <span data-ttu-id="5c38e-118">Fältet **Transaktionen Gäller** anger om antalet på artikeljournalraden ska kopplas till ett redan bokfört dokument.</span><span class="sxs-lookup"><span data-stu-id="5c38e-118">The **Applies-to Entry** field specifies if the quantity in the item journal line should be applied to an already-posted document.</span></span> <span data-ttu-id="5c38e-119">I så fall anger du löpnumret på den artikeltransaktion som artikeljournalen ska kopplas till.</span><span class="sxs-lookup"><span data-stu-id="5c38e-119">If this is the case, enter the entry number of the item ledger entry to which the item journal line should be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c38e-120">Se även</span><span class="sxs-lookup"><span data-stu-id="5c38e-120">See Also</span></span>

[<span data-ttu-id="5c38e-121">Ta bort och koppla om artikeltransaktioner</span><span class="sxs-lookup"><span data-stu-id="5c38e-121">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
[<span data-ttu-id="5c38e-122">Behandla försäljningsreturer och annulleringar</span><span class="sxs-lookup"><span data-stu-id="5c38e-122">Process Sales Returns and Cancellations</span></span>](sales-how-process-sales-returns-cancellations.md)  
[<span data-ttu-id="5c38e-123">Ställa in lagervärdering och lagerkostnad</span><span class="sxs-lookup"><span data-stu-id="5c38e-123">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="5c38e-124">Hantera lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="5c38e-124">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="5c38e-125">Designdetaljer: Värderingsprinciper</span><span class="sxs-lookup"><span data-stu-id="5c38e-125">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]