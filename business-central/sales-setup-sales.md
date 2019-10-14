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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 701556c09944c5dcce74543b550c9036c5cc77dd
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311938"
---
# <a name="setting-up-sales"></a><span data-ttu-id="a5684-103">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="a5684-103">Setting Up Sales</span></span>
<span data-ttu-id="a5684-104">Innan du kan hantera försäljningsprocesser måste du konfigurera reglerna och värdena som definierar företagets försäljningspolicies.</span><span class="sxs-lookup"><span data-stu-id="a5684-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="a5684-105">Först måste du definiera allmänna inställningar, till exempel vilka försäljningsdokument som krävs och hur deras värden bokförs.</span><span class="sxs-lookup"><span data-stu-id="a5684-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="a5684-106">Dessa allmänna inställningar görs vanligtvis bara en gång, under den initiala implementeringen.</span><span class="sxs-lookup"><span data-stu-id="a5684-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="a5684-107">En separat serie uppgifter relaterade till att registrera nya kunder är att registrera alla specialpriser eller rabattavtal som du har med varje kund.</span><span class="sxs-lookup"><span data-stu-id="a5684-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="a5684-108">Finansrelaterade försäljningar, till exempel betalningssätt och valutor, beskrivs i avsnittet Finans.</span><span class="sxs-lookup"><span data-stu-id="a5684-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="a5684-109">Mer information finns i [Konfigurera ekonomi](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="a5684-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="a5684-110">Om du vill</span><span class="sxs-lookup"><span data-stu-id="a5684-110">To</span></span> | <span data-ttu-id="a5684-111">Gå till</span><span class="sxs-lookup"><span data-stu-id="a5684-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="a5684-112">Skapa ett kundkort för varje kund som du säljer till.</span><span class="sxs-lookup"><span data-stu-id="a5684-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="a5684-113">Registrera nya kunder</span><span class="sxs-lookup"><span data-stu-id="a5684-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="a5684-114">Låt kunder betala via PayPal, genom att välja PayPal-logotypen på försäljningsdokument.</span><span class="sxs-lookup"><span data-stu-id="a5684-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="a5684-115">Så här aktiverar du kundutbetalning via PayPal</span><span class="sxs-lookup"><span data-stu-id="a5684-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="a5684-116">Ange olika rabatter och specialpriser som du beviljar kunden beroende på artikel, antal och/eller datum.</span><span class="sxs-lookup"><span data-stu-id="a5684-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="a5684-117">Registrera försäljningspris, rabatt och betalningsavtal</span><span class="sxs-lookup"><span data-stu-id="a5684-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="a5684-118">Skapa säljare så att du kan tilldela dem till kundkontakter eller mät säljares prestanda som grund för att beräkna deras försäljningprovision eller bonus.</span><span class="sxs-lookup"><span data-stu-id="a5684-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="a5684-119">Skapa säljare</span><span class="sxs-lookup"><span data-stu-id="a5684-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="a5684-120">Ange hur försäljningsdokument ska skickas som standard för enskilda kunder eller för alla kunder när du väljer åtgärden **Bokför och skicka**.</span><span class="sxs-lookup"><span data-stu-id="a5684-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="a5684-121">Skapa dokumentutskicksprofiler</span><span class="sxs-lookup"><span data-stu-id="a5684-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="a5684-122">Konfigurera din e-post så att den innehåller en sammanfattning av informationen på försäljningsdokumentet som har skickats.</span><span class="sxs-lookup"><span data-stu-id="a5684-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="a5684-123">[Skicka dokument som e-post](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="a5684-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="a5684-124">Du kan använda en EU-webbtjänst för att kontrollera kundens momsregistreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="a5684-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="a5684-125">Kontrollera momsregistreringsnummer</span><span class="sxs-lookup"><span data-stu-id="a5684-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="a5684-126">Definiera de olika Incoterms som du erbjuder till kunder eller som leverantören erbjuder dig.</span><span class="sxs-lookup"><span data-stu-id="a5684-126">Define the different incoterms that you offer to customers or that your vendors offer you.</span></span>|[<span data-ttu-id="a5684-127">Så här definierar du leveransmetoder</span><span class="sxs-lookup"><span data-stu-id="a5684-127">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)|
|<span data-ttu-id="a5684-128">Ange information om de olika transportleverantörerna som du använder, bland annat en länk till deras godsupplysningstjänst.</span><span class="sxs-lookup"><span data-stu-id="a5684-128">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="a5684-129">Så här konfigurerar du speditörer</span><span class="sxs-lookup"><span data-stu-id="a5684-129">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a><span data-ttu-id="a5684-130">Se även</span><span class="sxs-lookup"><span data-stu-id="a5684-130">See Also</span></span>
[<span data-ttu-id="a5684-131">Försäljning</span><span class="sxs-lookup"><span data-stu-id="a5684-131">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="a5684-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a5684-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
