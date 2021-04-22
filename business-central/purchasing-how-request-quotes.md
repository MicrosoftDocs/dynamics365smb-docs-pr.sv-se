---
title: Skapa en inköpsoffert för att begära en offert | Microsoft Docs
description: Beskriver hur du skapar ett försäljningserbjudande eller begäran om förslag (Offertförfrågan) för att registrera ditt erbjudande till kunden att sälja produkter under vissa villkor.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 416c5a4e4376932c16a1496f2db2b0c79307d22b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772625"
---
# <a name="request-quotes"></a><span data-ttu-id="fe46f-103">Begär offerter</span><span class="sxs-lookup"><span data-stu-id="fe46f-103">Request Quotes</span></span>
<span data-ttu-id="fe46f-104">En inköpsoffert kan användas som ett preliminärt utkast för en inköpsorder, som sedan kan göras om till en inköpsfaktura eller en order.</span><span class="sxs-lookup"><span data-stu-id="fe46f-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="fe46f-105">Så här skapar du en inköpsoffert:</span><span class="sxs-lookup"><span data-stu-id="fe46f-105">To create a purchase quote</span></span>
1. <span data-ttu-id="fe46f-106">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsofferter** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="fe46f-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="fe46f-107">Skapa ett nytt dokument på samma sätt som du gör en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="fe46f-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="fe46f-108">Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="fe46f-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="fe46f-109">Så här gör du om inköpsofferter till inköpsorder:</span><span class="sxs-lookup"><span data-stu-id="fe46f-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="fe46f-110">När du har accepterat leverantörens offert kan du omvandla den till en inköpsfaktura eller en order för att behandla inköpet.</span><span class="sxs-lookup"><span data-stu-id="fe46f-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="fe46f-111">Öppna en inköpsoffert som är redo att konvertera och välj sedan åtgärden **skapa order**.</span><span class="sxs-lookup"><span data-stu-id="fe46f-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="fe46f-112">Inköpsofferten tas bort från databasen.</span><span class="sxs-lookup"><span data-stu-id="fe46f-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="fe46f-113">En inköpsfaktura eller försäljningsorder skapas baserat på informationen i inköpsofferten där du kan bearbeta inköpet.</span><span class="sxs-lookup"><span data-stu-id="fe46f-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="fe46f-114">I fältet **Offertnr** på inköpsfakturan eller inköpsordern kan du ange numret på inköpsofferten som den har skapats från.</span><span class="sxs-lookup"><span data-stu-id="fe46f-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe46f-115">Se även</span><span class="sxs-lookup"><span data-stu-id="fe46f-115">See Also</span></span>
[<span data-ttu-id="fe46f-116">Inköp</span><span class="sxs-lookup"><span data-stu-id="fe46f-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="fe46f-117">Ställa in inköp</span><span class="sxs-lookup"><span data-stu-id="fe46f-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="fe46f-118">Skicka dokument som e-transaktion</span><span class="sxs-lookup"><span data-stu-id="fe46f-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="fe46f-119">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fe46f-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]