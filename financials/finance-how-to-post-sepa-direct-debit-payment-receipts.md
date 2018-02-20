---
title: "Bokför betalningar för SEPA direktdebitering | Microsoft Docs"
description: "När en direkt autogiroinsamling framgångsrikt bearbetas av din bank, kan du fortsätta att bokföra mottagandet av betalningen för de berörda försäljningsfakturorna."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0031017c96172dca76b50542e52c6a437c01427a
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="3de6f-103">Så här bokför du betalningsinleveranser för SEPA Autogiro</span><span class="sxs-lookup"><span data-stu-id="3de6f-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="3de6f-104">När en direkt autogiroinsamling framgångsrikt bearbetas av din bank, kan du fortsätta att bokföra mottagandet av betalningen för de berörda försäljningsfakturorna.</span><span class="sxs-lookup"><span data-stu-id="3de6f-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="3de6f-105">För mer information, se [Så här skapar du insamlingsposter för SEPA Autogiro och exporterar till en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="3de6f-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="3de6f-106">Du kan bokföra Betalningsinleverans direkt från den **Samlingar med autogiro** eller **Transaktioner för samlingar med autogiro**.</span><span class="sxs-lookup"><span data-stu-id="3de6f-106">You can post the payment receipt directly from the **Direct Debit Collections** window or the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="3de6f-107">Alternativt kan du vidarebefordra arbetet till en annan användare genom att förbereda de relaterade journalraderna.</span><span class="sxs-lookup"><span data-stu-id="3de6f-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a><span data-ttu-id="3de6f-108">Så här bokför du ett betalningskvitto för autogiroinsamling</span><span class="sxs-lookup"><span data-stu-id="3de6f-108">To post a direct-debit payment receipt from the Direct Debit Collections window</span></span>  
1. <span data-ttu-id="3de6f-109">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Autogiroinsamlingar**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3de6f-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3de6f-110">Välj en rad för en autogiroinsamling som har exporterats till en bankfil och framgångsrikt bearbetats av banken.</span><span class="sxs-lookup"><span data-stu-id="3de6f-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="3de6f-111">För mer information, se [Så här skapar du insamlingsposter för SEPA Autogiro och exporterar till en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="3de6f-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="3de6f-112">Välj åtgärden **Bokför betalningsinleveranser**.</span><span class="sxs-lookup"><span data-stu-id="3de6f-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="3de6f-113">I fönstret **Bokför samling med autogiro** fyller du i fälten enligt instruktionerna i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="3de6f-113">In the **Post Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="3de6f-114">Fält</span><span class="sxs-lookup"><span data-stu-id="3de6f-114">Field</span></span>|<span data-ttu-id="3de6f-115">Description</span><span class="sxs-lookup"><span data-stu-id="3de6f-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="3de6f-116">**Autogirosamlingsnr.**</span><span class="sxs-lookup"><span data-stu-id="3de6f-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="3de6f-117">Ange autogiroinsamlingen som du vill bokföra betalningskvittot för.</span><span class="sxs-lookup"><span data-stu-id="3de6f-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="3de6f-118">**Redovisningsjournalmall**</span><span class="sxs-lookup"><span data-stu-id="3de6f-118">**General Journal Template**</span></span>|<span data-ttu-id="3de6f-119">Ange vilken redovisningsjournalmallen som ska användas för att bokföra betalningskvitto, t.ex. mall för inbetalningar.</span><span class="sxs-lookup"><span data-stu-id="3de6f-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="3de6f-120">**Redovisningsjournalnamn**</span><span class="sxs-lookup"><span data-stu-id="3de6f-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="3de6f-121">Ange vilka redovisningsjournalbatch som ska användas för att bokföra ett betalningskvitto.</span><span class="sxs-lookup"><span data-stu-id="3de6f-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="3de6f-122">**Skapa enbart journal**</span><span class="sxs-lookup"><span data-stu-id="3de6f-122">**Create Journal Only**</span></span>|<span data-ttu-id="3de6f-123">Markera den här kryssrutan om du inte vill bokföra betalningskvittot när du väljer **OK** knappen.</span><span class="sxs-lookup"><span data-stu-id="3de6f-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="3de6f-124">Betalningskvittot skall förberedas i den angivna journalen och bokförs inte förrän någon bokför journalraderna i fråga.</span><span class="sxs-lookup"><span data-stu-id="3de6f-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="3de6f-125">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="3de6f-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3de6f-126">Se även</span><span class="sxs-lookup"><span data-stu-id="3de6f-126">See Also</span></span>  
 <span data-ttu-id="3de6f-127">[Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="3de6f-127">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="3de6f-128">Försäljning</span><span class="sxs-lookup"><span data-stu-id="3de6f-128">Sales</span></span>](sales-manage-sales.md)

