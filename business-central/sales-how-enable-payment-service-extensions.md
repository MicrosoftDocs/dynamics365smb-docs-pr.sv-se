---
title: Aktivera kundbetalningar via betalningstjänster | Microsoft Docs
description: Gör det enklare för kunderna att betala sina fakturor genom att aktivera betalningstjänster.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3bcfac75d1d161a4163fda466e320b0efd408655
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758273"
---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="2bf71-103">Aktivera kundbetalningar via betalningstjänster</span><span class="sxs-lookup"><span data-stu-id="2bf71-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="2bf71-104">Som alternativ till att samla utbetalningar via banköverföring eller kreditkort, kan dina kunder betala via sina konton med betalningstjänster som t.ex. Microsoft Pay, PayPal eller WorldPay.</span><span class="sxs-lookup"><span data-stu-id="2bf71-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="2bf71-105">När du har aktiverat en betalningstjänst i [!INCLUDE[prod_short](includes/prod_short.md)], är en länk till den här tjänsten tillgänglig på försäljningsdokument som du skickar med e-post till kunder.</span><span class="sxs-lookup"><span data-stu-id="2bf71-105">After you enable a payment service in [!INCLUDE[prod_short](includes/prod_short.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="2bf71-106">Kunder kan använda länken för att gå till betalningstjänsten och betala fakturan direkt från försäljningsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="2bf71-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="2bf71-107">Om du inte vill inkludera länken, exempelvis om en kund vill betala kontant, kan du ta bort betalningstjänsten från fakturan innan du bokför.</span><span class="sxs-lookup"><span data-stu-id="2bf71-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="2bf71-108">Tilläggen Microsoft Pay, PayPal Payments Standard och WorldPay Payments Standard är installerade i [!INCLUDE[prod_short](includes/prod_short.md)] och klara att aktiveras.</span><span class="sxs-lookup"><span data-stu-id="2bf71-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[prod_short](includes/prod_short.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-prod_short"></a><span data-ttu-id="2bf71-109">Så här aktiverar du en betalningstjänst i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="2bf71-109">To enable a payment service in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>
1. <span data-ttu-id="2bf71-110">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Betalningstjänster** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="2bf71-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2bf71-111">På sidan **Betalningstjänst** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2bf71-111">On the **Payment Services** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="2bf71-112">Välj betalningstjänsten och stäng sedan sidan.</span><span class="sxs-lookup"><span data-stu-id="2bf71-112">Select the payment service, and then close the page.</span></span>  
4. <span data-ttu-id="2bf71-113">På sidan **Betalningstjänst** väljer du åtgärden **Installation**.</span><span class="sxs-lookup"><span data-stu-id="2bf71-113">On the **Payment Services** page, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="2bf71-114">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="2bf71-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="2bf71-115">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="2bf71-115">Close the page.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="2bf71-116">Välja en betalningstjänst för en försäljningsfaktura</span><span class="sxs-lookup"><span data-stu-id="2bf71-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="2bf71-117">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2bf71-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2bf71-118">Öppna den försäljningsfaktura som du vill betala med hjälp av betalningstjänsten.</span><span class="sxs-lookup"><span data-stu-id="2bf71-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="2bf71-119">I fältet **Betalningtjänst** väljer du betalningtjänsten.</span><span class="sxs-lookup"><span data-stu-id="2bf71-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="2bf71-120">Fältet **betalningstjänst** är bara tillgängligt om du har aktiverat betalningstjänsten.</span><span class="sxs-lookup"><span data-stu-id="2bf71-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2bf71-121">Se även</span><span class="sxs-lookup"><span data-stu-id="2bf71-121">See Also</span></span>  
[<span data-ttu-id="2bf71-122">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="2bf71-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="2bf71-123">Försäljning</span><span class="sxs-lookup"><span data-stu-id="2bf71-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="2bf71-124">[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2bf71-124">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="2bf71-125">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2bf71-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
