---
title: "Med hjälp av tillägget PayPal-standardbetalning | Microsoft Docs"
description: "Beskriver hur du kan använda tillägget får att låta kunderna betala med PayPal."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fcbba8ecb2d63ab780a54aa4784a30b7fa5020fa
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="the-paypal-payments-standard-extension-to-dynamics-365-for-financials"></a><span data-ttu-id="c178c-103">Tillägget för PayPal-standardbetalning till Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="c178c-103">The PayPal Payments Standard Extension to Dynamics 365 for Financials</span></span>
<span data-ttu-id="c178c-104">Kunder kräver kontinuerligt högre kundservice både när det gäller produktkvalitet och även leveransdatum och betalningsalternativ.</span><span class="sxs-lookup"><span data-stu-id="c178c-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="c178c-105">Tjänsten för PayPal-standardbetalning hjälper dig att öka din kundservice.</span><span class="sxs-lookup"><span data-stu-id="c178c-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="c178c-106">Som alternativ till att samla utbetalningar via banköverföring eller kreditkort, kan du erbjuda dina kunder att betala via sina PayPal-konton.</span><span class="sxs-lookup"><span data-stu-id="c178c-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="c178c-107">När du skickar en försäljningsfaktura eller en försäljningsorder per e-post, finns en PayPal-länk i e-postbrödtexten och i det bifogade PDF-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="c178c-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="c178c-108">När kunden väljer länken, visar servicesidan för deras PayPal-konto försäljningens betalningsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="c178c-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="c178c-109">Då kan kunden betala fakturan som en PayPal-betalning.</span><span class="sxs-lookup"><span data-stu-id="c178c-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="c178c-110">Tjänsten för PayPal-standardbetalning ger följande förmåner:</span><span class="sxs-lookup"><span data-stu-id="c178c-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="c178c-111">Kundutbetalningar anländer snabbare till ditt bankkonto.</span><span class="sxs-lookup"><span data-stu-id="c178c-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="c178c-112">Kunder har flera sätt att betala fakturor.</span><span class="sxs-lookup"><span data-stu-id="c178c-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="c178c-113">PayPal har en trovärdig betalningtjänst, som kunder föredrar istället för att ange information om kreditkort på webbplatser.</span><span class="sxs-lookup"><span data-stu-id="c178c-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="c178c-114">PayPal erbjuder flera sätt för att hantera betalningar, inklusive bearbetning av kreditkort, PayPal-konton och andra källor.</span><span class="sxs-lookup"><span data-stu-id="c178c-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="c178c-115">PayPal-länken kan läggas till automatiskt till försäljningsdokument eller manuellt av användaren.</span><span class="sxs-lookup"><span data-stu-id="c178c-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="c178c-116">Tjänsten för PayPal-standardbetalning har inte månatliga avgifter eller installationsavgifter.</span><span class="sxs-lookup"><span data-stu-id="c178c-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="c178c-117">Eftersom det är ett tillägg, kan du enkelt aktivera tjänsten för PayPal-standardbetalning när din verksamhet kräver det.</span><span class="sxs-lookup"><span data-stu-id="c178c-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="c178c-118">Mer information finns i [Så här aktiverar du kundbetalning via PayPal](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="c178c-118">For more information, see [How to: Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c178c-119">Se även</span><span class="sxs-lookup"><span data-stu-id="c178c-119">See Also</span></span>
<span data-ttu-id="c178c-120">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="c178c-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="c178c-121">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="c178c-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="c178c-122">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c178c-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

