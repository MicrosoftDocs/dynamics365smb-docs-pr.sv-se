---
title: "Skapa en inköpsoffert för att begära en offert från leverantören | Microsoft Docs"
description: "Beskriver hur du skapar ett försäljningserbjudande eller begäran om förslag (Offertförfrågan) för att registrera ditt erbjudande till kunden att sälja produkter under vissa villkor."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: df1793d811dea11c01ff5e7d90a9f52b9e987c13
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-request-quotes"></a><span data-ttu-id="7cb01-103">Så här begär du offerter</span><span class="sxs-lookup"><span data-stu-id="7cb01-103">How to: Request Quotes</span></span>
<span data-ttu-id="7cb01-104">En inköpsoffert kan användas som ett preliminärt utkast för en inköpsorder, som sedan kan göras om till en inköpsfaktura eller en order.</span><span class="sxs-lookup"><span data-stu-id="7cb01-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="7cb01-105">Så här skapar du en inköpsoffert:</span><span class="sxs-lookup"><span data-stu-id="7cb01-105">To create a purchase quote</span></span>
1. <span data-ttu-id="7cb01-106">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsofferter** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7cb01-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="7cb01-107">Skapa ett nytt dokument på samma sätt som du gör en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="7cb01-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="7cb01-108">Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="7cb01-108">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="7cb01-109">Så här gör du om inköpsofferter till inköpsorder:</span><span class="sxs-lookup"><span data-stu-id="7cb01-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="7cb01-110">När du har accepterat leverantörens offert kan du omvandla den till en inköpsfaktura eller en order för att behandla inköpet.</span><span class="sxs-lookup"><span data-stu-id="7cb01-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="7cb01-111">Öppna en inköpsoffert som är redo att konvertera och välj sedan åtgärden **skapa order**.</span><span class="sxs-lookup"><span data-stu-id="7cb01-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="7cb01-112">Inköpsofferten tas bort från databasen.</span><span class="sxs-lookup"><span data-stu-id="7cb01-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="7cb01-113">En inköpsfaktura eller försäljningsorder skapas baserat på informationen i inköpsofferten där du kan bearbeta inköpet.</span><span class="sxs-lookup"><span data-stu-id="7cb01-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="7cb01-114">I fältet **Offertnr** på inköpsfakturan eller inköpsordern kan du ange numret på inköpsofferten som den har skapats från.</span><span class="sxs-lookup"><span data-stu-id="7cb01-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cb01-115">Se även</span><span class="sxs-lookup"><span data-stu-id="7cb01-115">See Also</span></span>
[<span data-ttu-id="7cb01-116">Inköp</span><span class="sxs-lookup"><span data-stu-id="7cb01-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="7cb01-117">Ställa in inköp</span><span class="sxs-lookup"><span data-stu-id="7cb01-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="7cb01-118">Så här skickar du dokument som e-post</span><span class="sxs-lookup"><span data-stu-id="7cb01-118">How to: Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="7cb01-119">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7cb01-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

