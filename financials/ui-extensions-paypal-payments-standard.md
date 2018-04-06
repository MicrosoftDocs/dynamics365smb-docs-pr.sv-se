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
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 64d1a76c4d35a87ab7af85e3325b786156f5a62f
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="the-paypal-payments-standard-extension-to-finance-and-operations-business-edition"></a><span data-ttu-id="f7378-103">Standardtillägget för PayPal-betalning i Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="f7378-103">The PayPal Payments Standard Extension to Finance and Operations, Business edition</span></span> 
<span data-ttu-id="f7378-104">Kunder kräver kontinuerligt högre kundservice både när det gäller produktkvalitet och även leveransdatum och betalningsalternativ.</span><span class="sxs-lookup"><span data-stu-id="f7378-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="f7378-105">Tjänsten för PayPal-standardbetalning hjälper dig att öka din kundservice.</span><span class="sxs-lookup"><span data-stu-id="f7378-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="f7378-106">Som alternativ till att samla utbetalningar via banköverföring eller kreditkort, kan du erbjuda dina kunder att betala via sina PayPal-konton.</span><span class="sxs-lookup"><span data-stu-id="f7378-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="f7378-107">När du skickar en försäljningsfaktura eller en försäljningsorder per e-post, finns en PayPal-länk i e-postbrödtexten och i det bifogade PDF-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="f7378-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="f7378-108">När kunden väljer länken, visar servicesidan för deras PayPal-konto försäljningens betalningsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="f7378-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="f7378-109">Då kan kunden betala fakturan som en PayPal-betalning.</span><span class="sxs-lookup"><span data-stu-id="f7378-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="f7378-110">Tjänsten för PayPal-standardbetalning ger följande förmåner:</span><span class="sxs-lookup"><span data-stu-id="f7378-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="f7378-111">Kundutbetalningar anländer snabbare till ditt bankkonto.</span><span class="sxs-lookup"><span data-stu-id="f7378-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="f7378-112">Kunder har flera sätt att betala fakturor.</span><span class="sxs-lookup"><span data-stu-id="f7378-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="f7378-113">PayPal har en trovärdig betalningtjänst, som kunder föredrar istället för att ange information om kreditkort på webbplatser.</span><span class="sxs-lookup"><span data-stu-id="f7378-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="f7378-114">PayPal erbjuder flera sätt för att hantera betalningar, inklusive bearbetning av kreditkort, PayPal-konton och andra källor.</span><span class="sxs-lookup"><span data-stu-id="f7378-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="f7378-115">PayPal-länken kan läggas till automatiskt till försäljningsdokument eller manuellt av användaren.</span><span class="sxs-lookup"><span data-stu-id="f7378-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="f7378-116">Tjänsten för PayPal-standardbetalning har inte månatliga avgifter eller installationsavgifter.</span><span class="sxs-lookup"><span data-stu-id="f7378-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="f7378-117">Eftersom det är ett tillägg, kan du enkelt aktivera tjänsten för PayPal-standardbetalning när din verksamhet kräver det.</span><span class="sxs-lookup"><span data-stu-id="f7378-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="f7378-118">Mer information finns i [Så här aktiverar du kundbetalningar via PayPal](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="f7378-118">For more information, see [Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f7378-119">Se även</span><span class="sxs-lookup"><span data-stu-id="f7378-119">See Also</span></span>
<span data-ttu-id="f7378-120">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="f7378-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="f7378-121">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="f7378-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="f7378-122">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7378-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

