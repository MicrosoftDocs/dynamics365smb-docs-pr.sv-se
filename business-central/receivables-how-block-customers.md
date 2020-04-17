---
title: Spärra försäljning till kunders artiklar från försäljning eller inköp
description: I Business Central kan en artikel markeras som spärrad för försäljning, spärrad för inköp eller spärrad för alla syften.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 832963169f4c81d65b105ca71722435554d8e262
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193761"
---
# <a name="block-customers"></a><span data-ttu-id="af141-103">Spärra kunder</span><span class="sxs-lookup"><span data-stu-id="af141-103">Block Customers</span></span>
<span data-ttu-id="af141-104">Du kan spärra en kund, till exempel på grund av ett insolvensförfarande, så att kunden inte kan läggas till försäljningsdokument, eller så att inga transaktioner kan bokföras för kunden.</span><span class="sxs-lookup"><span data-stu-id="af141-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="af141-105">Förutom att spärra en kund, kan du ange ingående transaktioner för en kund som spärrade i samband med påminnelser.</span><span class="sxs-lookup"><span data-stu-id="af141-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="af141-106">Mer information finns i [Så här kräver du in utestående saldon](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="af141-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="af141-107">De olika spärrningsalternativen beskrivs i tabellen nedan.</span><span class="sxs-lookup"><span data-stu-id="af141-107">The following table describes the different blocking options.</span></span>  

|<span data-ttu-id="af141-108">Alternativ</span><span class="sxs-lookup"><span data-stu-id="af141-108">Option</span></span>|<span data-ttu-id="af141-109">Description</span><span class="sxs-lookup"><span data-stu-id="af141-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="af141-110">**Tomt**</span><span class="sxs-lookup"><span data-stu-id="af141-110">**Blank**</span></span>|<span data-ttu-id="af141-111">Transaktioner tillåts för den här kunden.</span><span class="sxs-lookup"><span data-stu-id="af141-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="af141-112">**Leverera**</span><span class="sxs-lookup"><span data-stu-id="af141-112">**Ship**</span></span>|<span data-ttu-id="af141-113">Det går inte att skapa nya order eller nya leveranser för den här kunden.</span><span class="sxs-lookup"><span data-stu-id="af141-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="af141-114">Befintliga leveranser som inte ännu har fakturerats kan faktureras.</span><span class="sxs-lookup"><span data-stu-id="af141-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="af141-115">**Fakturera**</span><span class="sxs-lookup"><span data-stu-id="af141-115">**Invoice**</span></span>|<span data-ttu-id="af141-116">Det går inte att skapa nya order, nya leveranser eller nya fakturor för den här kunden.</span><span class="sxs-lookup"><span data-stu-id="af141-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="af141-117">Befintliga leveranser som inte ännu har fakturerats kan inte faktureras.</span><span class="sxs-lookup"><span data-stu-id="af141-117">Existing shipments not yet invoiced cannot be invoiced.</span></span>|  
|<span data-ttu-id="af141-118">**Allt**</span><span class="sxs-lookup"><span data-stu-id="af141-118">**All**</span></span>|<span data-ttu-id="af141-119">Ingen transaktion tillåts för den här kunden, inklusive betalningar.</span><span class="sxs-lookup"><span data-stu-id="af141-119">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="af141-120">Om du vill spärra en kund</span><span class="sxs-lookup"><span data-stu-id="af141-120">To block a customer</span></span>  
1. <span data-ttu-id="af141-121">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="af141-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="af141-122">Välj en kund och välj sedan åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="af141-122">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="af141-123">Fyll i fältet **spärrad** med något av alternativen ovan.</span><span class="sxs-lookup"><span data-stu-id="af141-123">Fill in the **Blocked** field with one of the options described above.</span></span>

## <a name="see-also"></a><span data-ttu-id="af141-124">Se även</span><span class="sxs-lookup"><span data-stu-id="af141-124">See Also</span></span>  
[<span data-ttu-id="af141-125">Registrera nya kunder</span><span class="sxs-lookup"><span data-stu-id="af141-125">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="af141-126">Kräva in utestående saldon</span><span class="sxs-lookup"><span data-stu-id="af141-126">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="af141-127">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="af141-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
