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
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c149949b939a551a14236c84f8ba7538fcb54bbe
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-customer-payments-through-payment-services"></a><span data-ttu-id="254a8-103">Så här aktiverar du kundbetalningar via betalningstjänster</span><span class="sxs-lookup"><span data-stu-id="254a8-103">How to: Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="254a8-104">Som alternativ till att samla utbetalningar via banköverföring eller kreditkort, kan dina kunder betala via sina konton med betalningstjänster som t.ex. Microsoft Pay, PayPal, or WorldPay.</span><span class="sxs-lookup"><span data-stu-id="254a8-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="254a8-105">När du har aktiverat en betalningstjänst i [!INCLUDE[d365fin](includes/d365fin_md.md)], är en länk till den här tjänsten tillgänglig på försäljningsdokument som du skickar med e-post till kunder.</span><span class="sxs-lookup"><span data-stu-id="254a8-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="254a8-106">Kunder kan använda länken för att gå till betalningstjänsten och betala fakturan direkt från försäljningsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="254a8-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="254a8-107">Om du inte vill inkludera länken, exempelvis om en kund vill betala kontant, kan du ta bort betalningstjänsten från fakturan innan du bokför.</span><span class="sxs-lookup"><span data-stu-id="254a8-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="254a8-108">Tilläggen Microsoft Pay, PayPal Payments Standard och WorldPay Payments Standard är installerade i [!INCLUDE[d365fin](includes/d365fin_md.md)], och klara att aktiveras.</span><span class="sxs-lookup"><span data-stu-id="254a8-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a><span data-ttu-id="254a8-109">Så här aktiverar du en betalningstjänst i [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="254a8-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="254a8-110">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Betalningstjänster** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="254a8-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="254a8-111">I fönstret **Betalningstjänst** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="254a8-111">In the **Payment Services** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="254a8-112">Välj betalningstjänsten och stäng sedan fönstret.</span><span class="sxs-lookup"><span data-stu-id="254a8-112">Select the payment service, and then close the window.</span></span>  
4. <span data-ttu-id="254a8-113">I fönstret **Betalningstjänst** väljer du åtgärden **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="254a8-113">In the **Payment Services** window, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="254a8-114">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="254a8-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="254a8-115">Stäng fönstret.</span><span class="sxs-lookup"><span data-stu-id="254a8-115">Close the window.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="254a8-116">Välj en betalningstjänst för en försäljningsfaktura</span><span class="sxs-lookup"><span data-stu-id="254a8-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="254a8-117">Välj åtgärden **Försäljningsfakturor** på startsidan.</span><span class="sxs-lookup"><span data-stu-id="254a8-117">On the Home page, choose **Sales Invoices**.</span></span>  
2. <span data-ttu-id="254a8-118">Öppna den försäljningsorder som du vill betala med hjälp av betalningstjänsten.</span><span class="sxs-lookup"><span data-stu-id="254a8-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="254a8-119">I fältet **Betalningtjänst** väljer du betalningtjänsten.</span><span class="sxs-lookup"><span data-stu-id="254a8-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="254a8-120">Fältet **betalningstjänst** är bara tillgängligt om du har aktiverat betalningstjänsten.</span><span class="sxs-lookup"><span data-stu-id="254a8-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="254a8-121">Se även</span><span class="sxs-lookup"><span data-stu-id="254a8-121">See Also</span></span>  
[<span data-ttu-id="254a8-122">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="254a8-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="254a8-123">Försäljning</span><span class="sxs-lookup"><span data-stu-id="254a8-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="254a8-124">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="254a8-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="254a8-125">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="254a8-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

