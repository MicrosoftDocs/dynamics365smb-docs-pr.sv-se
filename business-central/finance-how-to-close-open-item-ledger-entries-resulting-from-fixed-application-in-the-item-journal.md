---
title: "Avsluta öppna artikeltransaktioner som skapas från en fast koppling i artikeljournalen | Microsoft Docs"
description: "Du kan använda fältet **Kopplas från löpnr** i fönstret **Artikeljournal** för att skapa en fast koppling mellan en inkommande transaktion och den ursprungliga utgående transaktionen. Till exempel, för att korrigera utgående transaktion eller bearbeta dess retur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f879688bd458714f354b2e98e58ce78686cf79d9
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="34ac8-104">Stäng öppna artikeltransaktioner som skapas från en fast koppling i artikeljournalen</span><span class="sxs-lookup"><span data-stu-id="34ac8-104">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="34ac8-105">Du kan använda fältet **Kopplas från löpnr** i fönstret **Artikeljournal** för att skapa en fast koppling mellan en inkommande transaktion och den ursprungliga utgående transaktionen.</span><span class="sxs-lookup"><span data-stu-id="34ac8-105">You can use the **Applies-from Entry** field in the **Item Journal** window to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="34ac8-106">Till exempel, för att korrigera utgående transaktion eller bearbeta dess retur.</span><span class="sxs-lookup"><span data-stu-id="34ac8-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="34ac8-107">Mer information finns i Kopplas från löpnr.</span><span class="sxs-lookup"><span data-stu-id="34ac8-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="34ac8-108">Fast koppling som gjorts på det här sättet gäller endast kostnaden, inte antal.</span><span class="sxs-lookup"><span data-stu-id="34ac8-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="34ac8-109">På så sätt kommer den bokförda positiv artikeltransaktion inte avsluta det kopplade avgående transaktion, och att stå öppen.</span><span class="sxs-lookup"><span data-stu-id="34ac8-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="34ac8-110">Detta gäller också när du bokför en fast koppling för en positiv transaktion på en negativ transaktion som inte har avslutats av en vanlig positiva transaktion, kommer både negativ och de positiva transaktionerna finns kvar öppna.</span><span class="sxs-lookup"><span data-stu-id="34ac8-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="34ac8-111">Det innebär att du inte kan avsluta en lagerperiod, om sådan transaktion finns.</span><span class="sxs-lookup"><span data-stu-id="34ac8-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="34ac8-112">I följande procedur beskrivs hur du avslutar sådana transaktioner genom att utföra två korrigerande bokföringar i artikeljournalen.</span><span class="sxs-lookup"><span data-stu-id="34ac8-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="34ac8-113">Om du vill avsluta öppna artikeltransaktioner som skapas från ett fast koppling i artikeljournalen</span><span class="sxs-lookup"><span data-stu-id="34ac8-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="34ac8-114">Använd fältet **Kopplas från löpnr** om du vill bokföra en positiv justering med motsvarande antal.</span><span class="sxs-lookup"><span data-stu-id="34ac8-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="34ac8-115">Denna åtgärd stänger den ursprungliga negativ transaktion med en fast koppling.</span><span class="sxs-lookup"><span data-stu-id="34ac8-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="34ac8-116">Använd fältet **Kopplas till löpnr** om du vill bokföra en negativ justering.</span><span class="sxs-lookup"><span data-stu-id="34ac8-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="34ac8-117">Denna åtgärd stänger den korrigerande positiva transaktionen med en fast koppling.</span><span class="sxs-lookup"><span data-stu-id="34ac8-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="34ac8-118">Se även</span><span class="sxs-lookup"><span data-stu-id="34ac8-118">See Also</span></span>  
[<span data-ttu-id="34ac8-119"> Ta bort och koppla om artikeltransaktioner</span><span class="sxs-lookup"><span data-stu-id="34ac8-119"> Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="34ac8-120">[Behandla försäljningsreturer och annulleringar](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="34ac8-120">[Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="34ac8-121">[Ställa in lagervärdering och lagerkostnad](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="34ac8-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="34ac8-122">[Hantera lagerkostnader](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="34ac8-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="34ac8-123">Designdetaljer: Värderingsprinciper</span><span class="sxs-lookup"><span data-stu-id="34ac8-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
