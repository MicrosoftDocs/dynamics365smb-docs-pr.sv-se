---
title: Så här spärrar du försäljning till kunder
description: Om det behövs kan du spärra en kund från att ingå i försäljningsdokument och andra försäljningstransaktioner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 720eb2d5899ba067dbcee8dc97492ebcd01b1abd
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779183"
---
# <a name="block-customers"></a><span data-ttu-id="59eb8-103">Spärra kunder</span><span class="sxs-lookup"><span data-stu-id="59eb8-103">Block Customers</span></span>
<span data-ttu-id="59eb8-104">Du kan spärra en kund, till exempel på grund av ett insolvensförfarande, så att kunden inte kan läggas till försäljningsdokument, eller så att inga transaktioner kan bokföras för kunden.</span><span class="sxs-lookup"><span data-stu-id="59eb8-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="59eb8-105">Förutom att spärra en kund, kan du ange ingående transaktioner för en kund som spärrade i samband med påminnelser.</span><span class="sxs-lookup"><span data-stu-id="59eb8-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="59eb8-106">Mer information finns i [Så här kräver du in utestående saldon](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="59eb8-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="59eb8-107">Följande tabell anger alternativen för att spärra kunder.</span><span class="sxs-lookup"><span data-stu-id="59eb8-107">The following table describes the options for blocking customers.</span></span>  

|<span data-ttu-id="59eb8-108">Alternativ</span><span class="sxs-lookup"><span data-stu-id="59eb8-108">Option</span></span>|<span data-ttu-id="59eb8-109">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="59eb8-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="59eb8-110">**Tomt**</span><span class="sxs-lookup"><span data-stu-id="59eb8-110">**Blank**</span></span>|<span data-ttu-id="59eb8-111">Transaktioner tillåts för den här kunden.</span><span class="sxs-lookup"><span data-stu-id="59eb8-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="59eb8-112">**Leverera**</span><span class="sxs-lookup"><span data-stu-id="59eb8-112">**Ship**</span></span>|<span data-ttu-id="59eb8-113">Det går inte att skapa nya order eller nya leveranser för den här kunden.</span><span class="sxs-lookup"><span data-stu-id="59eb8-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="59eb8-114">Befintliga leveranser som inte ännu har fakturerats kan faktureras.</span><span class="sxs-lookup"><span data-stu-id="59eb8-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="59eb8-115">**Fakturera**</span><span class="sxs-lookup"><span data-stu-id="59eb8-115">**Invoice**</span></span>|<span data-ttu-id="59eb8-116">Det går inte att skapa nya order, nya leveranser eller nya fakturor för den här kunden.</span><span class="sxs-lookup"><span data-stu-id="59eb8-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="59eb8-117">Befintliga leveranser som inte ännu har fakturerats kan inte faktureras.</span><span class="sxs-lookup"><span data-stu-id="59eb8-117">Existing shipments not yet invoiced cannot be invoiced.</span></span> <span data-ttu-id="59eb8-118">Du kan fortfarande skicka påminnelser och räntefakturor till kunden.</span><span class="sxs-lookup"><span data-stu-id="59eb8-118">You can still send reminders and finance charge memos to the customer.</span></span>|  
|<span data-ttu-id="59eb8-119">**Alla**</span><span class="sxs-lookup"><span data-stu-id="59eb8-119">**All**</span></span>|<span data-ttu-id="59eb8-120">Ingen transaktion tillåts för den här kunden, inklusive betalningar.</span><span class="sxs-lookup"><span data-stu-id="59eb8-120">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="59eb8-121">Om du vill spärra en kund</span><span class="sxs-lookup"><span data-stu-id="59eb8-121">To block a customer</span></span>  
1. <span data-ttu-id="59eb8-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="59eb8-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="59eb8-123">Välj en kund och välj sedan åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="59eb8-123">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="59eb8-124">I fältet **Spärrad** anger du vad som ska blockeras i enlighet med beskrivningen i tabellen ovan.</span><span class="sxs-lookup"><span data-stu-id="59eb8-124">In the **Blocked** field, choose what to block, as described in the table above.</span></span>

## <a name="see-also"></a><span data-ttu-id="59eb8-125">Se även</span><span class="sxs-lookup"><span data-stu-id="59eb8-125">See Also</span></span>  
[<span data-ttu-id="59eb8-126">Registrera nya kunder</span><span class="sxs-lookup"><span data-stu-id="59eb8-126">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="59eb8-127">Kräva in utestående saldon</span><span class="sxs-lookup"><span data-stu-id="59eb8-127">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="59eb8-128">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="59eb8-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
