---
title: Betala inköpsfakturor snabbt
description: Om du vill betala leverantören kontant eller med check kan all nödvändig bokföring göras när du bokför fakturan.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: 60d3cf3c9e141c8df36eaca2c1975b696fdb105b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387255"
---
# <a name="settle-purchase-invoices-promptly"></a><span data-ttu-id="1ba23-103">Betala inköpsfakturor snabbt</span><span class="sxs-lookup"><span data-stu-id="1ba23-103">Settle Purchase Invoices Promptly</span></span>

<span data-ttu-id="1ba23-104">Om du vill betala leverantören kontant eller med check kan du bokföra betalningen när du bokför fakturan.</span><span class="sxs-lookup"><span data-stu-id="1ba23-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  

> [!NOTE]  
> <span data-ttu-id="1ba23-105">Om du ofta betalar inköpsfakturor kontant, via check eller banöverföring, kan det vara praktiskt att definiera ett särskilt betalningssätt för ett balanskonto och ange detta i fältet **Betalningssätt** på leverantörskortet.</span><span class="sxs-lookup"><span data-stu-id="1ba23-105">If you frequently pay purchase invoices in cash, check, or bank transfer, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="1ba23-106">Hädanefter infogas motkontonumret i fakturahuvudet automatiskt när du skapar en ny faktura.</span><span class="sxs-lookup"><span data-stu-id="1ba23-106">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span> <span data-ttu-id="1ba23-107">Mer information finns i [Definiera betalningssätt](finance-payment-methods.md).</span><span class="sxs-lookup"><span data-stu-id="1ba23-107">For more information, see [Defining Payment Methods](finance-payment-methods.md).</span></span>  

## <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="1ba23-108">Så här gör du för att snabbt betala inköpsfakturor:</span><span class="sxs-lookup"><span data-stu-id="1ba23-108">To settle purchase invoices promptly</span></span>

1. <span data-ttu-id="1ba23-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Inköpsfakturor** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="1ba23-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1ba23-110">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1ba23-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="1ba23-111">Ange numret på redovisningskassakontot eller bankkontot i fältet **Motkonto** om du vill betala kontant eller via banköverföring .</span><span class="sxs-lookup"><span data-stu-id="1ba23-111">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="1ba23-112">Fälten **Motkontotyp** och **Motkonto** ingår inte i standardlayouten för fakturahuvudet.</span><span class="sxs-lookup"><span data-stu-id="1ba23-112">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="1ba23-113">För att du ska kunna bokföra betalningen av en faktura måste du kontakta en Microsoft-partner som kan lägga till fälten via kod.</span><span class="sxs-lookup"><span data-stu-id="1ba23-113">In order to post the payment of an invoice, you must contact a Microsoft partner who can add the fields through code.</span></span>  
>
> <span data-ttu-id="1ba23-114">Denna anpassning krävs endast om du inte anger balanskonton för betalningssätten enligt beskrivningen ovan.</span><span class="sxs-lookup"><span data-stu-id="1ba23-114">This customization is only required if you do not specify balancing accounts on the payment methods as describe above.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ba23-115">Se även</span><span class="sxs-lookup"><span data-stu-id="1ba23-115">See Also</span></span>

[<span data-ttu-id="1ba23-116">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="1ba23-116">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="1ba23-117">Inköp</span><span class="sxs-lookup"><span data-stu-id="1ba23-117">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="1ba23-118">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1ba23-118">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]