---
title: "Fakturera förskottsbetalningar | Microsoft Docs"
description: "Förskottsbetalningar är betalningar som faktureras och bokförs för en försäljnings- eller inköpsorder före slutfaktureringen. Du kan till exempel kräva en deposition innan du tillverkar artiklar mot order eller också kan du kräva betalning innan du levererar artiklar till en kund. Med hjälp av funktionen för förskottsbetalning kan du fakturera och inkassera depositioner från kunder eller betala depositioner till leverantörer. På så sätt kan du se till att alla betalningar bokförs mot en faktura."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5cdc1ddde1762976a89d60f7906fb3e7363982f0
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="invoicing-prepayments"></a><span data-ttu-id="1d6a0-106">Fakturera förskottsbetalningar</span><span class="sxs-lookup"><span data-stu-id="1d6a0-106">Invoicing Prepayments</span></span>
<span data-ttu-id="1d6a0-107">Förskottsbetalningar är betalningar som faktureras och bokförs för en försäljnings- eller inköpsorder före slutfaktureringen.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-107">Prepayments are payments that are invoiced and posted to a sales or purchase prepayment order before final invoicing.</span></span> <span data-ttu-id="1d6a0-108">Du kan till exempel kräva en deposition innan du tillverkar artiklar mot order eller också kan du kräva betalning innan du levererar artiklar till en kund.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-108">You might require a deposit before you manufacture items to order, or you might require payment before you ship items to a customer.</span></span> <span data-ttu-id="1d6a0-109">Med hjälp av funktionen för förskottsbetalning kan du fakturera och inkassera depositioner från kunder eller betala depositioner till leverantörer.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-109">The prepayments functionality enables you to invoice and collect deposits required from customers or to remit deposits to vendors.</span></span> <span data-ttu-id="1d6a0-110">På så sätt kan du se till att alla betalningar bokförs mot en faktura.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-110">Thus, you can ensure that all payments are posted against an invoice.</span></span>  

 <span data-ttu-id="1d6a0-111">Förskottsbetalningskrav kan definieras för en kund eller leverantör för alla artiklar eller valda artiklar.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-111">Prepayment requirements can be defined for a customer or vendor for all items or selected items.</span></span> <span data-ttu-id="1d6a0-112">När du har gjort de nödvändiga inställningarna kan du generera förskottsfakturor från försäljnings- och inköpsorder för det beräknade förskottsbeloppet.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-112">After you complete the required setup, you can generate prepayment invoices from sales and purchase orders for the calculated prepayment amount.</span></span> <span data-ttu-id="1d6a0-113">Du ändra beloppet på fakturan om det behövs.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-113">You can change the amounts on the invoice as needed.</span></span> <span data-ttu-id="1d6a0-114">Du kan till exempel ange ett totalt belopp för hela ordern.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-114">For example, you can specify a total amount for the entire order.</span></span> <span data-ttu-id="1d6a0-115">Du kan även skicka ytterligare förskottsfakturor om, till exempel, ytterligare artiklar läggs till i ordern.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-115">You can also send additional prepayment invoices if, for example, additional items are added to the order.</span></span> <span data-ttu-id="1d6a0-116">Du kan öka antal eller lägga till nya rader på en order efter att du har skickat ut en förskottsbetalning, och du kan bokföra en ny förskottsfaktura.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-116">You can increase quantities or add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice.</span></span> <span data-ttu-id="1d6a0-117">Om du vill ta bort en rad som en förskottsbetalning redan har fakturerats för, måste du skicka ut en kreditnota för förskottsbetalningen innan du kan ta bort raden.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-117">If you want to delete a line for which a prepayment has already been invoiced, you must issue a prepayment credit memo before you can delete the line.</span></span>  

 <span data-ttu-id="1d6a0-118">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-118">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="1d6a0-119">**Om du vill**</span><span class="sxs-lookup"><span data-stu-id="1d6a0-119">**To**</span></span>|<span data-ttu-id="1d6a0-120">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="1d6a0-120">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="1d6a0-121">Ställa in förskottsbetalningsgrupper och nummerserie och ställa in standardvärden för procentuell förskottsbetalning för kunder, leverantörer och artiklar.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-121">Set up prepayment posting groups and number series, and set up default prepayment percentages for customers, vendors, and items.</span></span>|[<span data-ttu-id="1d6a0-122">Konfigurera förskottsbetalningar</span><span class="sxs-lookup"><span data-stu-id="1d6a0-122">Set Up Prepayments</span></span>](finance-set-up-prepayments.md)|
|<span data-ttu-id="1d6a0-123">skapa en order, justera förskottsbetalningsbeloppen och skicka ut en faktura för förskottsbetalningsbeloppen.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-123">Create an order, adjust the prepayment amounts, and issue an invoice for prepayment amounts.</span></span>|[<span data-ttu-id="1d6a0-124">Skapa förskottsfakturor</span><span class="sxs-lookup"><span data-stu-id="1d6a0-124">Create Prepayment Invoices</span></span>](finance-how-to-create-prepayment-invoices.md)|  
|<span data-ttu-id="1d6a0-125">skicka ut en ytterligare förskottsfaktura, antingen för ytterligare artiklar eller för en ytterligare deposition på den ursprungliga ordern, eller skicka ut en kreditnota för förskottsbetalning.</span><span class="sxs-lookup"><span data-stu-id="1d6a0-125">Issue an additional prepayment invoice, either for additional items or for an additional deposit on the original order, or issue a prepayment credit memo.</span></span>|[<span data-ttu-id="1d6a0-126">Korrigera förskottsbetalningar</span><span class="sxs-lookup"><span data-stu-id="1d6a0-126">Correct Prepayments</span></span>](finance-how-to-correct-prepayments.md)|  

## <a name="see-also"></a><span data-ttu-id="1d6a0-127">Se även</span><span class="sxs-lookup"><span data-stu-id="1d6a0-127">See Also</span></span>  
[<span data-ttu-id="1d6a0-128">Genomgång: Lägga upp och fakturera förskottsbetaln., försäljning</span><span class="sxs-lookup"><span data-stu-id="1d6a0-128">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="1d6a0-129">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="1d6a0-129">Finance</span></span>](finance.md)  
<span data-ttu-id="1d6a0-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1d6a0-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
