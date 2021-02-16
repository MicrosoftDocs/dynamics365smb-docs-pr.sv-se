---
title: Microsoft Pay Standard | Microsoft Docs
description: Ger information om tillägget Microsoft Pay
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 748316c411c4b04947685c6053e9c53aa9102c35
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747574"
---
# <a name="the-microsoft-pay-extension"></a><span data-ttu-id="1af8a-103">Tillägget Microsoft Pay</span><span class="sxs-lookup"><span data-stu-id="1af8a-103">The Microsoft Pay Extension</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1af8a-104">Från och med den 8 februari 2020 kommer ändringar i Microsoft Pay-tjänsten att påverka Microsoft Pay-tillägget i Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span><span class="sxs-lookup"><span data-stu-id="1af8a-104">Effective February 8 2020, changes in the Microsoft Pay service will affect the Microsoft Pay extension in Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span></span> <span data-ttu-id="1af8a-105">På grund av ändringarna kommer **Betala nu**-betallänkarna som Microsoft Pay-tillägget genererar för fakturor i [!INCLUDE[prod_short](includes/prod_short.md)] inte att öppna Microsoft Pay efter den 8 februari.</span><span class="sxs-lookup"><span data-stu-id="1af8a-105">Due to the changes, after February 8, the **Pay now** payment links that the Microsoft Pay extension generates for invoices in [!INCLUDE[prod_short](includes/prod_short.md)] will not open Microsoft Pay.</span></span> <span data-ttu-id="1af8a-106">Kunder som använder tillägget bör ändra sina inställningar för betaltjänster och istället börja använda PayPal-tillägget.</span><span class="sxs-lookup"><span data-stu-id="1af8a-106">Customers who are using the extension should change their Payment Services setup to start using the PayPal extension instead.</span></span><br /></br>
>
> <span data-ttu-id="1af8a-107">Från och med den 8 januari kommer vi att visa en avisering i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1af8a-107">From January 8, we will display a notification in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="1af8a-108">Meddelandet kommer att innehålla en länk till de inställningar som du behöver ändra och till mer information.</span><span class="sxs-lookup"><span data-stu-id="1af8a-108">The notification will contain a link to the settings that you need to change and to more information.</span></span> <span data-ttu-id="1af8a-109">Efter den 8 februari kommer Microsoft Pay-tillägget inte längre att vara tillgängligt i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1af8a-109">After February 8, the Microsoft Pay extension will no longer be available in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span><br /></br>
>
> <span data-ttu-id="1af8a-110">Ändringarna påverkar följande versioner av Business Central:</span><span class="sxs-lookup"><span data-stu-id="1af8a-110">The changes impact the following versions of Business Central:</span></span>
> - <span data-ttu-id="1af8a-111">Microsoft Dynamics 365 Business Central oktober 2018</span><span class="sxs-lookup"><span data-stu-id="1af8a-111">Microsoft Dynamics 365 Business Central October 2018</span></span>
> - <span data-ttu-id="1af8a-112">Microsoft Dynamics 365 Business Central april 2019</span><span class="sxs-lookup"><span data-stu-id="1af8a-112">Microsoft Dynamics 365 Business Central April 2019</span></span>
> - <span data-ttu-id="1af8a-113">Microsoft Dynamics 365 Business Central 2019, utgivningsplan 2</span><span class="sxs-lookup"><span data-stu-id="1af8a-113">Microsoft Dynamics 365 Business Central 2019 Release Wave 2</span></span>

<span data-ttu-id="1af8a-114">Kunder kräver kontinuerligt högre kundservice både när det gäller produktkvalitet och även leverans- och betalningstjänster.</span><span class="sxs-lookup"><span data-stu-id="1af8a-114">Customers continuously require higher customer service, both in terms of the quality of product but also in terms of delivery and payment services.</span></span> <span data-ttu-id="1af8a-115">Tjänsten Microsoft Pay hjälper dig att öka din kundservice.</span><span class="sxs-lookup"><span data-stu-id="1af8a-115">The Microsoft Pay service helps you increase your customer service.</span></span>

<span data-ttu-id="1af8a-116">Tillägget Microsoft Pay lägger till en Microsoft Pay-länk till ditt försäljningsdokument så att kunder lätt kan betala med Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="1af8a-116">The Microsoft Pay extension adds a Microsoft Pay link to your sales documents so customers can easily pay using Microsoft Pay.</span></span> <span data-ttu-id="1af8a-117">Därefter kan du skicka dokument med e-post för att ge bättre kundservice och minska den tid det tar för kundens betalningar att komma till ditt bankkonto.</span><span class="sxs-lookup"><span data-stu-id="1af8a-117">Then you can send the documents by email to provide higher customer service and shorten the time it takes for customers’ payments to arrive on your bank account.</span></span>

<span data-ttu-id="1af8a-118">Tillägget Microsoft Pay ger följande fördelar:</span><span class="sxs-lookup"><span data-stu-id="1af8a-118">The Microsoft Pay extension provides the following benefits:</span></span>
- <span data-ttu-id="1af8a-119">Kundutbetalningar visas snabbare på ditt bankkonto.</span><span class="sxs-lookup"><span data-stu-id="1af8a-119">Customer payments appear faster on your bank account.</span></span>
- <span data-ttu-id="1af8a-120">Kunder har flera sätt att betala fakturor.</span><span class="sxs-lookup"><span data-stu-id="1af8a-120">Customers have more ways to pay invoices.</span></span>
- <span data-ttu-id="1af8a-121">Microsoft Pay har en trovärdig betalningtjänst, som kunder föredrar istället för att ange information om kreditkort på okända webbplatser.</span><span class="sxs-lookup"><span data-stu-id="1af8a-121">Microsoft Pay offers a trustworthy payment service, which customers prefer to entering credit card information on unknown web sites.</span></span>
- <span data-ttu-id="1af8a-122">Microsoft Pay erbjuder flera sätt för att hantera betalningar, inklusive bearbetning av kreditkort, PayPal och Stripe.</span><span class="sxs-lookup"><span data-stu-id="1af8a-122">Microsoft Pay offers multiple ways of handling payments, including credit card processing, such as PayPal and Stripe.</span></span>
- <span data-ttu-id="1af8a-123">Microsoft Pay-länken bäddas in automatiskt på alla fakturadokument eller av användaren.</span><span class="sxs-lookup"><span data-stu-id="1af8a-123">The Microsoft Pay link can be embedded automatically on every invoice document or by the user.</span></span>
- <span data-ttu-id="1af8a-124">Eftersom den här funktionen ingår som ett tillägg får du fullständig behörighet att aktivera den när och om dina affärsprocesser kräver det..</span><span class="sxs-lookup"><span data-stu-id="1af8a-124">Because this functionality is built as an extension, it gives you full control to enable it when and if your business processes require it.</span></span>

<span data-ttu-id="1af8a-125">Aktivera tillägg för betalningstjänster är gratis i [!INCLUDE[prod_short](includes/prod_short.md)], men du måste du kontakta betalningstjänsten för att få ett konto.</span><span class="sxs-lookup"><span data-stu-id="1af8a-125">Enabling payment service extensions is free in [!INCLUDE[prod_short](includes/prod_short.md)], however, you will need to contact the payment service to get an account.</span></span> <span data-ttu-id="1af8a-126">Mer information finns i [Aktivera kundbetalning via betalningstjänster](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="1af8a-126">For more information, see [Enable Customer Payment Through Payment Services](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1af8a-127">Se även</span><span class="sxs-lookup"><span data-stu-id="1af8a-127">See Also</span></span>
<span data-ttu-id="1af8a-128">[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="1af8a-128">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="1af8a-129">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="1af8a-129">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="1af8a-130">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1af8a-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
