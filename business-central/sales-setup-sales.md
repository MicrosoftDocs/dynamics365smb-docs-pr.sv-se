---
title: Översikt över proceduren för att konfigurera försäljningsprocesser | Microsoft Docs
description: Innehåller information om hur du definierar regler och värden för att definiera dina försäljningspolicyer och -processer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 9bfdfa6d4abf49f163fd9478e4c0c59dda069abd
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194745"
---
# <a name="setting-up-sales"></a><span data-ttu-id="71144-103">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="71144-103">Setting Up Sales</span></span>
<span data-ttu-id="71144-104">Innan du kan hantera försäljningsprocesser måste du konfigurera reglerna och värdena som definierar företagets försäljningspolicies.</span><span class="sxs-lookup"><span data-stu-id="71144-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="71144-105">Först måste du definiera allmänna inställningar, till exempel vilka försäljningsdokument som krävs och hur deras värden bokförs.</span><span class="sxs-lookup"><span data-stu-id="71144-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="71144-106">Dessa allmänna inställningar görs vanligtvis bara en gång, under den initiala implementeringen.</span><span class="sxs-lookup"><span data-stu-id="71144-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="71144-107">En separat serie uppgifter relaterade till att registrera nya kunder är att registrera alla specialpriser eller rabattavtal som du har med varje kund.</span><span class="sxs-lookup"><span data-stu-id="71144-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="71144-108">Finansrelaterade försäljningar, till exempel betalningssätt och valutor, beskrivs i avsnittet Finans.</span><span class="sxs-lookup"><span data-stu-id="71144-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="71144-109">Mer information finns i [Konfigurera ekonomi](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="71144-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="71144-110">Om du vill</span><span class="sxs-lookup"><span data-stu-id="71144-110">To</span></span> | <span data-ttu-id="71144-111">Gå till</span><span class="sxs-lookup"><span data-stu-id="71144-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="71144-112">Skapa ett kundkort för varje kund som du säljer till.</span><span class="sxs-lookup"><span data-stu-id="71144-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="71144-113">Registrera nya kunder</span><span class="sxs-lookup"><span data-stu-id="71144-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="71144-114">Låt kunder betala via PayPal, genom att välja PayPal-logotypen på försäljningsdokument.</span><span class="sxs-lookup"><span data-stu-id="71144-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="71144-115">Så här aktiverar du kundutbetalning via PayPal</span><span class="sxs-lookup"><span data-stu-id="71144-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="71144-116">Ange olika rabatter och specialpriser som du beviljar kunden beroende på artikel, antal och/eller datum.</span><span class="sxs-lookup"><span data-stu-id="71144-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="71144-117">Registrera försäljningspris, rabatt och betalningsavtal</span><span class="sxs-lookup"><span data-stu-id="71144-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="71144-118">Skapa säljare så att du kan tilldela dem till kundkontakter eller mät säljares prestanda som grund för att beräkna deras försäljningprovision eller bonus.</span><span class="sxs-lookup"><span data-stu-id="71144-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="71144-119">Skapa säljare</span><span class="sxs-lookup"><span data-stu-id="71144-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="71144-120">Ange hur försäljningsdokument ska skickas som standard för enskilda kunder eller för alla kunder när du väljer åtgärden **Bokför och skicka**.</span><span class="sxs-lookup"><span data-stu-id="71144-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="71144-121">Skapa dokumentutskicksprofiler</span><span class="sxs-lookup"><span data-stu-id="71144-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="71144-122">Konfigurera din e-post så att den innehåller en sammanfattning av informationen på försäljningsdokumentet som har skickats.</span><span class="sxs-lookup"><span data-stu-id="71144-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="71144-123">[Skicka dokument som e-post](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="71144-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="71144-124">Du kan använda en EU-webbtjänst för att kontrollera kundens momsregistreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="71144-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="71144-125">Kontrollera momsregistreringsnummer</span><span class="sxs-lookup"><span data-stu-id="71144-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="71144-126">Definiera de olika Incoterms som du erbjuder till kunder eller som leverantören erbjuder dig.</span><span class="sxs-lookup"><span data-stu-id="71144-126">Define the different incoterms that you offer to customers or that your vendors offer you.</span></span>|[<span data-ttu-id="71144-127">Så här definierar du leveransmetoder</span><span class="sxs-lookup"><span data-stu-id="71144-127">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)|
|<span data-ttu-id="71144-128">Ange information om de olika transportleverantörerna som du använder, bland annat en länk till deras godsupplysningstjänst.</span><span class="sxs-lookup"><span data-stu-id="71144-128">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="71144-129">Så här konfigurerar du speditörer</span><span class="sxs-lookup"><span data-stu-id="71144-129">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="71144-130">Se Relaterad utbildning på [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="71144-130">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="71144-131">Se även</span><span class="sxs-lookup"><span data-stu-id="71144-131">See Also</span></span>
[<span data-ttu-id="71144-132">Försäljning</span><span class="sxs-lookup"><span data-stu-id="71144-132">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="71144-133">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="71144-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
