---
title: "Skapa en inköpsoffert för att begära en offert | Microsoft Docs"
description: "Beskriver hur du skapar ett försäljningserbjudande eller begäran om förslag (Offertförfrågan) för att registrera ditt erbjudande till kunden att sälja produkter under vissa villkor."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 19e7b8e55d3276730c16401b1d5d0d8203b7e7c9
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="request-quotes"></a><span data-ttu-id="6d72b-103">Begär offerter</span><span class="sxs-lookup"><span data-stu-id="6d72b-103">Request Quotes</span></span>
<span data-ttu-id="6d72b-104">En inköpsoffert kan användas som ett preliminärt utkast för en inköpsorder, som sedan kan göras om till en inköpsfaktura eller en order.</span><span class="sxs-lookup"><span data-stu-id="6d72b-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="6d72b-105">Så här skapar du en inköpsoffert:</span><span class="sxs-lookup"><span data-stu-id="6d72b-105">To create a purchase quote</span></span>
1. <span data-ttu-id="6d72b-106">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Inköpsofferter** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="6d72b-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="6d72b-107">Skapa ett nytt dokument på samma sätt som du gör en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="6d72b-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="6d72b-108">Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="6d72b-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="6d72b-109">Så här gör du om inköpsofferter till inköpsorder:</span><span class="sxs-lookup"><span data-stu-id="6d72b-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="6d72b-110">När du har accepterat leverantörens offert kan du omvandla den till en inköpsfaktura eller en order för att behandla inköpet.</span><span class="sxs-lookup"><span data-stu-id="6d72b-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="6d72b-111">Öppna en inköpsoffert som är redo att konvertera och välj sedan åtgärden **skapa order**.</span><span class="sxs-lookup"><span data-stu-id="6d72b-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="6d72b-112">Inköpsofferten tas bort från databasen.</span><span class="sxs-lookup"><span data-stu-id="6d72b-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="6d72b-113">En inköpsfaktura eller försäljningsorder skapas baserat på informationen i inköpsofferten där du kan bearbeta inköpet.</span><span class="sxs-lookup"><span data-stu-id="6d72b-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="6d72b-114">I fältet **Offertnr** på inköpsfakturan eller inköpsordern kan du ange numret på inköpsofferten som den har skapats från.</span><span class="sxs-lookup"><span data-stu-id="6d72b-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d72b-115">Se även</span><span class="sxs-lookup"><span data-stu-id="6d72b-115">See Also</span></span>
[<span data-ttu-id="6d72b-116">Inköp</span><span class="sxs-lookup"><span data-stu-id="6d72b-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="6d72b-117">Ställa in inköp</span><span class="sxs-lookup"><span data-stu-id="6d72b-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="6d72b-118">Skicka dokument som e-post</span><span class="sxs-lookup"><span data-stu-id="6d72b-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="6d72b-119">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6d72b-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
