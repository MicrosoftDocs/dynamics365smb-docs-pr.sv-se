---
title: Ange betalsätt
description: Du kan använda betalningsmetoder, till exempel, kontrollera, banköverföring, kontant eller PayPal, för att ange hur försäljnings- och inköpsfakturor ska betalas.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 1e836b43392cd915a77c5ee85d5a322753dcd5df
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773961"
---
# <a name="set-up-payment-methods"></a><span data-ttu-id="b89e8-103">Ange betalsätt</span><span class="sxs-lookup"><span data-stu-id="b89e8-103">Set Up Payment Methods</span></span>

<span data-ttu-id="b89e8-104">Betalningssätt definierar hur du föredrar att kunderna betalar dig och hur du vill betala dina leverantörer.</span><span class="sxs-lookup"><span data-stu-id="b89e8-104">Payment methods define the way you prefer for customers to pay you, and how you like to pay your vendors.</span></span> <span data-ttu-id="b89e8-105">Metoden kan variera för varje kund eller leverantör.</span><span class="sxs-lookup"><span data-stu-id="b89e8-105">The method can vary for each customer or vendor.</span></span> <span data-ttu-id="b89e8-106">Exempel på typiska betalningssätt är **bank**, **kontanter**, **check** eller **konto**.</span><span class="sxs-lookup"><span data-stu-id="b89e8-106">Examples of typical payment methods are **bank**, **cash**, **check**, or **account**.</span></span>

<span data-ttu-id="b89e8-107">Du kan tilldela ett betalningssätt till kunder och leverantörer så att samma metod alltid används på de försäljningsorderrader och inköpsdokument som du skapar dem för.</span><span class="sxs-lookup"><span data-stu-id="b89e8-107">You can assign a payment method to customers and vendors so that the same method is always used on the sales and purchase documents you create for them.</span></span> <span data-ttu-id="b89e8-108">Om det behövs kan du ändra metoden för försäljnings- eller inköpsdokument.</span><span class="sxs-lookup"><span data-stu-id="b89e8-108">If needed, you can change the method on the sales or purchase document.</span></span> <span data-ttu-id="b89e8-109">Till exempel om du vill betala en viss inköpsfaktura kontant och inte med checkar.</span><span class="sxs-lookup"><span data-stu-id="b89e8-109">For example, if you want to pay a particular purchase invoice in cash rather than by check.</span></span> <span data-ttu-id="b89e8-110">Standardbetalningsmetoden som tilldelats leverantören ändras inte.</span><span class="sxs-lookup"><span data-stu-id="b89e8-110">This does not change the default payment method assigned to the vendor.</span></span>

<span data-ttu-id="b89e8-111">Samma betalningssätt används för försäljnings- och inköpsdokument.</span><span class="sxs-lookup"><span data-stu-id="b89e8-111">The same payment methods are used for sales and purchase documents.</span></span> <span data-ttu-id="b89e8-112">Till exempel ett _kontant_ betalningssätt används både när du gör betalningar och när du tar emot dem.</span><span class="sxs-lookup"><span data-stu-id="b89e8-112">For example, a _cash_ payment method is used both when you make payments and when you receive them.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="b89e8-113">vet att när du skapar en försäljningsfaktura förväntar du dig att erhålla betalning och motsatsen för inköpsfakturor.</span><span class="sxs-lookup"><span data-stu-id="b89e8-113">knows that when you are creating a sales invoice you expect to receive payment, and the opposite for purchase invoices.</span></span>

<span data-ttu-id="b89e8-114">Kreditnotor för returer är emellertid undantag eftersom pengar flödar i motsatt riktning från dig till din kund och från din leverantör till dig.</span><span class="sxs-lookup"><span data-stu-id="b89e8-114">Credit memos for returns, however, are exceptions because money is flowing in the opposite directions, from you to your customer and from your vendor to you.</span></span> <span data-ttu-id="b89e8-115">Därför tilldelas inte ett standardbetalningssätt för kreditnotor.</span><span class="sxs-lookup"><span data-stu-id="b89e8-115">Therefore, a default payment method is not assigned to credit memos.</span></span> <span data-ttu-id="b89e8-116">Det finns emellertid en lösning om du har angett betalningsvillkoren för kunden eller leverantören.</span><span class="sxs-lookup"><span data-stu-id="b89e8-116">There is, however, a workaround if you have specified terms of payment for the customer or vendor.</span></span> <span data-ttu-id="b89e8-117">Även om fältet **Beräkna kassarabatt i kr.nota** inte är avsett för detta, om du väljer den här kryssrutan på sidan **betalningsvillkor** kommer ett standardbetalningssätt att läggas till när du skapar en kreditnota.</span><span class="sxs-lookup"><span data-stu-id="b89e8-117">Though the **Calc. Pmt. Disc. on Cr. Memos** field is not intended for this, if you choose the check box on the **Payment Terms** page a default payment method will be added when you create a credit memo.</span></span> <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a><span data-ttu-id="b89e8-118">Så här definierar du betalningssätt:</span><span class="sxs-lookup"><span data-stu-id="b89e8-118">To set up a payment method</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="b89e8-119">innehåller några betalningssätt som företag använder ofta.</span><span class="sxs-lookup"><span data-stu-id="b89e8-119">provides a few payment methods that businesses often use.</span></span> <span data-ttu-id="b89e8-120">Du kan emellertid lägga till hur många rader du vill.</span><span class="sxs-lookup"><span data-stu-id="b89e8-120">You can, however, add as many as you need.</span></span>

1. <span data-ttu-id="b89e8-121">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **betalningssätt** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b89e8-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="b89e8-122">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="b89e8-122">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="b89e8-123">Du kan också lägga till betalningsvillkor i betalsättet.</span><span class="sxs-lookup"><span data-stu-id="b89e8-123">Optionally, add payment terms to your payment method.</span></span> <span data-ttu-id="b89e8-124">Mer information finns i [Ange betalningsvillkor](finance-payment-terms.md).</span><span class="sxs-lookup"><span data-stu-id="b89e8-124">For more information, see [Set Up Payment Terms](finance-payment-terms.md).</span></span>  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a><span data-ttu-id="b89e8-125">Så här kopplar du betalningssätt till en kund eller leverantör</span><span class="sxs-lookup"><span data-stu-id="b89e8-125">To assign a payment method to a customer or vendor</span></span>

1. <span data-ttu-id="b89e8-126">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Kund** eller **Leverantör** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b89e8-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer** or **Vendor**, and then choose the related link.</span></span>
2. <span data-ttu-id="b89e8-127">I fältet **betalningssättkod**, välj metoden som ska användas som standard för kunden eller leverantören.</span><span class="sxs-lookup"><span data-stu-id="b89e8-127">In the **Payment Method Code** field, choose the method to use by default for the customer or vendor.</span></span>

## <a name="see-also"></a><span data-ttu-id="b89e8-128">Se även</span><span class="sxs-lookup"><span data-stu-id="b89e8-128">See Also</span></span>

[<span data-ttu-id="b89e8-129">Registrera nya kunder</span><span class="sxs-lookup"><span data-stu-id="b89e8-129">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="b89e8-130">Ställa in betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="b89e8-130">Set Up Payment Terms</span></span>](finance-payment-terms.md)  
[<span data-ttu-id="b89e8-131">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="b89e8-131">Finance</span></span>](finance.md)  
<span data-ttu-id="b89e8-132">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b89e8-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]