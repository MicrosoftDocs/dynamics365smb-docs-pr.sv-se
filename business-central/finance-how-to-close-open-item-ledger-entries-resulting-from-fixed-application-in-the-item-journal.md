---
title: Avsluta öppna artikeltransaktioner som skapas från en fast koppling i artikeljournalen | Microsoft Docs
description: Du kan använda fältet **Kopplas från löpnr** på sidan **Artikeljournal** för att skapa en fast koppling mellan en inkommande transaktion och den ursprungliga utgående transaktionen. Till exempel, för att korrigera utgående transaktion eller bearbeta dess retur.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: e3f210b86168d34ec775f85b416b6d0e365cce88
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807348"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="c2be1-104">Stäng öppna artikeltransaktioner som skapas från en fast koppling i artikeljournalen</span><span class="sxs-lookup"><span data-stu-id="c2be1-104">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="c2be1-105">Du kan använda fältet **Kopplas från löpnr** på sidan **Artikeljournal** för att skapa en fast koppling mellan en inkommande transaktion och den ursprungliga utgående transaktionen.</span><span class="sxs-lookup"><span data-stu-id="c2be1-105">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="c2be1-106">Till exempel, för att korrigera utgående transaktion eller bearbeta dess retur.</span><span class="sxs-lookup"><span data-stu-id="c2be1-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="c2be1-107">Mer information finns i Kopplas från löpnr.</span><span class="sxs-lookup"><span data-stu-id="c2be1-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="c2be1-108">Fast koppling som gjorts på det här sättet gäller endast kostnaden, inte antal.</span><span class="sxs-lookup"><span data-stu-id="c2be1-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="c2be1-109">På så sätt kommer den bokförda positiv artikeltransaktion inte avsluta det kopplade avgående transaktion, och att stå öppen.</span><span class="sxs-lookup"><span data-stu-id="c2be1-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="c2be1-110">Detta gäller också när du bokför en fast koppling för en positiv transaktion på en negativ transaktion som inte har avslutats av en vanlig positiva transaktion, kommer både negativ och de positiva transaktionerna finns kvar öppna.</span><span class="sxs-lookup"><span data-stu-id="c2be1-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="c2be1-111">Det innebär att du inte kan avsluta en lagerperiod, om sådan transaktion finns.</span><span class="sxs-lookup"><span data-stu-id="c2be1-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="c2be1-112">I följande procedur beskrivs hur du avslutar sådana transaktioner genom att utföra två korrigerande bokföringar i artikeljournalen.</span><span class="sxs-lookup"><span data-stu-id="c2be1-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="c2be1-113">Om du vill avsluta öppna artikeltransaktioner som skapas från ett fast koppling i artikeljournalen</span><span class="sxs-lookup"><span data-stu-id="c2be1-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="c2be1-114">Använd fältet **Kopplas från löpnr** om du vill bokföra en positiv justering med motsvarande antal.</span><span class="sxs-lookup"><span data-stu-id="c2be1-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="c2be1-115">Denna åtgärd stänger den ursprungliga negativ transaktion med en fast koppling.</span><span class="sxs-lookup"><span data-stu-id="c2be1-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="c2be1-116">Använd fältet **Kopplas till löpnr** om du vill bokföra en negativ justering.</span><span class="sxs-lookup"><span data-stu-id="c2be1-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="c2be1-117">Denna åtgärd stänger den korrigerande positiva transaktionen med en fast koppling.</span><span class="sxs-lookup"><span data-stu-id="c2be1-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c2be1-118">Se även</span><span class="sxs-lookup"><span data-stu-id="c2be1-118">See Also</span></span>  
[<span data-ttu-id="c2be1-119"> Ta bort och koppla om artikeltransaktioner</span><span class="sxs-lookup"><span data-stu-id="c2be1-119"> Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="c2be1-120">[Behandla försäljningsreturer och annulleringar](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="c2be1-120">[Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="c2be1-121">[Ställa in lagervärdering och lagerkostnad](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="c2be1-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="c2be1-122">[Hantera lagerkostnader](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="c2be1-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="c2be1-123">Designdetaljer: Värderingsprinciper</span><span class="sxs-lookup"><span data-stu-id="c2be1-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
