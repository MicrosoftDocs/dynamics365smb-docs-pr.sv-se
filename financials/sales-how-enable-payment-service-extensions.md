---
title: "Aktivera kundbetalningar via betalningstjänster | Microsoft Docs"
description: "Gör det enklare för kunderna att betala sina fakturor genom att aktivera betalningstjänster."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 49e75c5f43b495bfc053c58b27e06feace62971c
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-enable-customer-payments-through-payment-services"></a><span data-ttu-id="2580e-103">Så här aktiverar du kundbetalningar via betalningstjänster</span><span class="sxs-lookup"><span data-stu-id="2580e-103">How to: Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="2580e-104">Som alternativ till att samla utbetalningar via banköverföring eller kreditkort, kan dina kunder betala via sina konton med betalningstjänster som t.ex. PayPal eller WorldPay.</span><span class="sxs-lookup"><span data-stu-id="2580e-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as PayPal or WorldPay.</span></span>  

<span data-ttu-id="2580e-105">När du har aktiverat en betalningstjänst i [!INCLUDE[d365fin](includes/d365fin_md.md)], är en länk till den här tjänsten tillgänglig på försäljningsdokument som du skickar med e-post till kunder.</span><span class="sxs-lookup"><span data-stu-id="2580e-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="2580e-106">Kunder kan använda länken för att gå till betalningstjänsten och betala fakturan direkt från försäljningsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="2580e-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="2580e-107">Om du inte vill inkludera länken, exempelvis om en kund vill betala kontant, kan du ta bort betalningstjänsten från fakturan innan du bokför.</span><span class="sxs-lookup"><span data-stu-id="2580e-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="2580e-108">Tilläggen PayPal Payments Standard och WorldPay Payments Standard är installerade i [!INCLUDE[d365fin](includes/d365fin_md.md)], och klara att aktiveras.</span><span class="sxs-lookup"><span data-stu-id="2580e-108">The PayPal Payments Standard and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a><span data-ttu-id="2580e-109">Så här aktiverar du en betalningstjänst i [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="2580e-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="2580e-110">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Betalningstjänster** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2580e-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2580e-111">I fönstret **Betalningstjänst** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2580e-111">In the **Payment Services** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="2580e-112">Välj betalningstjänsten och stäng sedan fönstret.</span><span class="sxs-lookup"><span data-stu-id="2580e-112">Select the payment service, and then close the window.</span></span>  
4. <span data-ttu-id="2580e-113">I fönstret **Betalningstjänst** väljer du åtgärden **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="2580e-113">In the **Payment Services** window, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="2580e-114">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="2580e-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="2580e-115">Stäng fönstret.</span><span class="sxs-lookup"><span data-stu-id="2580e-115">Close the window.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="2580e-116">Välj en betalningstjänst för en försäljningsfaktura</span><span class="sxs-lookup"><span data-stu-id="2580e-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="2580e-117">Välj åtgärden **Försäljningsfakturor** på startsidan.</span><span class="sxs-lookup"><span data-stu-id="2580e-117">On the Home page, choose **Sales Invoices**.</span></span>  
2. <span data-ttu-id="2580e-118">Öppna den försäljningsorder som du vill betala med hjälp av betalningstjänsten.</span><span class="sxs-lookup"><span data-stu-id="2580e-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="2580e-119">I fältet **Betalningtjänst** väljer du betalningtjänsten.</span><span class="sxs-lookup"><span data-stu-id="2580e-119">In the **Payment Service** field, choose the payment service.</span></span>  
  
    > [!NOTE]  
>   <span data-ttu-id="2580e-120">Fältet **betalningstjänst** är bara tillgängligt om du har aktiverat betalningstjänsten.</span><span class="sxs-lookup"><span data-stu-id="2580e-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2580e-121">Se även</span><span class="sxs-lookup"><span data-stu-id="2580e-121">See Also</span></span>  
[<span data-ttu-id="2580e-122">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="2580e-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="2580e-123">Försäljning</span><span class="sxs-lookup"><span data-stu-id="2580e-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="2580e-124">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2580e-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="2580e-125">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2580e-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

