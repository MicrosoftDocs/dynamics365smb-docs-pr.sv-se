---
title: Spärra försäljning till kunders artiklar från försäljning eller inköp
description: I Business Central kan en artikel markeras som spärrad för försäljning, spärrad för inköp eller spärrad för alla syften.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c2b0d5b15571b7e8af1ed1dbee22859f4c131aa3
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316626"
---
# <a name="block-customers"></a><span data-ttu-id="7a82b-103">Spärra kunder</span><span class="sxs-lookup"><span data-stu-id="7a82b-103">Block Customers</span></span>
<span data-ttu-id="7a82b-104">Du kan spärra en kund, till exempel på grund av ett insolvensförfarande, så att kunden inte kan läggas till försäljningsdokument, eller så att inga transaktioner kan bokföras för kunden.</span><span class="sxs-lookup"><span data-stu-id="7a82b-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="7a82b-105">Förutom att spärra en kund, kan du ange ingående transaktioner för en kund som spärrade i samband med påminnelser.</span><span class="sxs-lookup"><span data-stu-id="7a82b-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="7a82b-106">Mer information finns i [Så här kräver du in utestående saldon](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="7a82b-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="7a82b-107">De olika spärrningsalternativen beskrivs i tabellen nedan.</span><span class="sxs-lookup"><span data-stu-id="7a82b-107">The following table describes the different blocking options.</span></span>  

|<span data-ttu-id="7a82b-108">Alternativ</span><span class="sxs-lookup"><span data-stu-id="7a82b-108">Option</span></span>|<span data-ttu-id="7a82b-109">Description</span><span class="sxs-lookup"><span data-stu-id="7a82b-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="7a82b-110">**Tomt**</span><span class="sxs-lookup"><span data-stu-id="7a82b-110">**Blank**</span></span>|<span data-ttu-id="7a82b-111">Transaktioner tillåts för den här kunden.</span><span class="sxs-lookup"><span data-stu-id="7a82b-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="7a82b-112">**Leverera**</span><span class="sxs-lookup"><span data-stu-id="7a82b-112">**Ship**</span></span>|<span data-ttu-id="7a82b-113">Det går inte att skapa nya order eller nya leveranser för den här kunden.</span><span class="sxs-lookup"><span data-stu-id="7a82b-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="7a82b-114">Befintliga leveranser som inte ännu har fakturerats kan faktureras.</span><span class="sxs-lookup"><span data-stu-id="7a82b-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="7a82b-115">**Fakturera**</span><span class="sxs-lookup"><span data-stu-id="7a82b-115">**Invoice**</span></span>|<span data-ttu-id="7a82b-116">Det går inte att skapa nya order, nya leveranser eller nya fakturor för den här kunden.</span><span class="sxs-lookup"><span data-stu-id="7a82b-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="7a82b-117">Befintliga leveranser som inte ännu har fakturerats kan inte faktureras.</span><span class="sxs-lookup"><span data-stu-id="7a82b-117">Existing shipments not yet invoiced cannot be invoiced.</span></span>|  
|<span data-ttu-id="7a82b-118">**Allt**</span><span class="sxs-lookup"><span data-stu-id="7a82b-118">**All**</span></span>|<span data-ttu-id="7a82b-119">Ingen transaktion tillåts för den här kunden, inklusive betalningar.</span><span class="sxs-lookup"><span data-stu-id="7a82b-119">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="7a82b-120">Om du vill spärra en kund</span><span class="sxs-lookup"><span data-stu-id="7a82b-120">To block a customer</span></span>  
1. <span data-ttu-id="7a82b-121">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kunder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7a82b-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="7a82b-122">Välj en kund och välj sedan åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="7a82b-122">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="7a82b-123">Fyll i fältet **spärrad** med något av alternativen ovan.</span><span class="sxs-lookup"><span data-stu-id="7a82b-123">Fill in the **Blocked** field with one of the options described above.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a82b-124">Se även</span><span class="sxs-lookup"><span data-stu-id="7a82b-124">See Also</span></span>  
[<span data-ttu-id="7a82b-125">Registrera nya kunder</span><span class="sxs-lookup"><span data-stu-id="7a82b-125">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="7a82b-126">Kräva in utestående saldon</span><span class="sxs-lookup"><span data-stu-id="7a82b-126">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="7a82b-127">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="7a82b-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
