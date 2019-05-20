---
title: Översikt över proceduren för att konfigurera försäljningsprocesser | Microsoft Docs
description: Innehåller information om hur du definierar regler och värden för att definiera dina försäljningspolicyer och -processer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6903744c1be0492267c8dee307e4b012aed4ffa4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251038"
---
# <a name="setting-up-sales"></a><span data-ttu-id="1c2e4-103">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="1c2e4-103">Setting Up Sales</span></span>
<span data-ttu-id="1c2e4-104">Innan du kan hantera försäljningsprocesser måste du konfigurera reglerna och värdena som definierar företagets försäljningspolicies.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="1c2e4-105">Först måste du definiera allmänna inställningar, till exempel vilka försäljningsdokument som krävs och hur deras värden bokförs.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="1c2e4-106">Dessa allmänna inställningar görs vanligtvis bara en gång, under den initiala implementeringen.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="1c2e4-107">En separat serie uppgifter relaterade till att registrera nya kunder är att registrera alla specialpriser eller rabattavtal som du har med varje kund.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="1c2e4-108">Finansrelaterade försäljningar, till exempel betalningssätt och valutor, beskrivs i avsnittet Finans.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="1c2e4-109">Mer information finns i [Konfigurera ekonomi](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="1c2e4-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="1c2e4-110">Om du vill</span><span class="sxs-lookup"><span data-stu-id="1c2e4-110">To</span></span> | <span data-ttu-id="1c2e4-111">Gå till</span><span class="sxs-lookup"><span data-stu-id="1c2e4-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="1c2e4-112">Skapa ett kundkort för varje kund som du säljer till.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="1c2e4-113">Registrera nya kunder</span><span class="sxs-lookup"><span data-stu-id="1c2e4-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="1c2e4-114">Låt kunder betala via PayPal, genom att välja PayPal-logotypen på försäljningsdokument.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="1c2e4-115">Så här aktiverar du kundutbetalning via PayPal</span><span class="sxs-lookup"><span data-stu-id="1c2e4-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="1c2e4-116">Ange olika rabatter och specialpriser som du beviljar kunden beroende på artikel, antal och/eller datum.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="1c2e4-117">Registrera försäljningspris, rabatt och betalningsavtal</span><span class="sxs-lookup"><span data-stu-id="1c2e4-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="1c2e4-118">Skapa säljare så att du kan tilldela dem till kundkontakter eller mät säljares prestanda som grund för att beräkna deras försäljningprovision eller bonus.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="1c2e4-119">Skapa säljare</span><span class="sxs-lookup"><span data-stu-id="1c2e4-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="1c2e4-120">Ange hur försäljningsdokument ska skickas som standard för enskilda kunder eller för alla kunder när du väljer åtgärden **Bokför och skicka**.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="1c2e4-121">Skapa dokumentutskicksprofiler</span><span class="sxs-lookup"><span data-stu-id="1c2e4-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="1c2e4-122">Konfigurera din e-post så att den innehåller en sammanfattning av informationen på försäljningsdokumentet som har skickats.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="1c2e4-123">[Skicka dokument som e-post](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="1c2e4-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="1c2e4-124">Du kan använda en EU-webbtjänst för att kontrollera kundens momsregistreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="1c2e4-125">Kontrollera momsregistreringsnummer</span><span class="sxs-lookup"><span data-stu-id="1c2e4-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="1c2e4-126">Ange information om de olika transportleverantörerna som du använder, bland annat en länk till deras godsupplysningstjänst.</span><span class="sxs-lookup"><span data-stu-id="1c2e4-126">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="1c2e4-127">Så här konfigurerar du speditörer</span><span class="sxs-lookup"><span data-stu-id="1c2e4-127">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a><span data-ttu-id="1c2e4-128">Se även</span><span class="sxs-lookup"><span data-stu-id="1c2e4-128">See Also</span></span>
[<span data-ttu-id="1c2e4-129">Försäljning</span><span class="sxs-lookup"><span data-stu-id="1c2e4-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="1c2e4-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1c2e4-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
