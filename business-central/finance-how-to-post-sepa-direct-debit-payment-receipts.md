---
title: "Bokför betalningar för SEPA direktdebitering | Microsoft Docs"
description: "När en direkt autogiroinsamling framgångsrikt bearbetas av din bank, kan du fortsätta att bokföra mottagandet av betalningen för de berörda försäljningsfakturorna."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ee07ca7ba498858fac794f1ee1f27f281de8ae02
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="968c6-103">Så här bokför du betalningsinleveranser för SEPA Autogiro</span><span class="sxs-lookup"><span data-stu-id="968c6-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="968c6-104">När en direkt autogiroinsamling framgångsrikt bearbetas av din bank, kan du fortsätta att bokföra mottagandet av betalningen för de berörda försäljningsfakturorna.</span><span class="sxs-lookup"><span data-stu-id="968c6-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="968c6-105">För mer information, se [Så här skapar du insamlingsposter för SEPA Autogiro och exporterar till en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="968c6-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="968c6-106">Du kan bokföra Betalningsinleverans direkt från den **Samlingar med autogiro** eller **Transaktioner för samlingar med autogiro**.</span><span class="sxs-lookup"><span data-stu-id="968c6-106">You can post the payment receipt directly from the **Direct Debit Collections** window or the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="968c6-107">Alternativt kan du vidarebefordra arbetet till en annan användare genom att förbereda de relaterade journalraderna.</span><span class="sxs-lookup"><span data-stu-id="968c6-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a><span data-ttu-id="968c6-108">Så här bokför du ett betalningskvitto för autogiroinsamling</span><span class="sxs-lookup"><span data-stu-id="968c6-108">To post a direct-debit payment receipt from the Direct Debit Collections window</span></span>  
1. <span data-ttu-id="968c6-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Samlingar med autogiro** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="968c6-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="968c6-110">Välj en rad för en autogiroinsamling som har exporterats till en bankfil och framgångsrikt bearbetats av banken.</span><span class="sxs-lookup"><span data-stu-id="968c6-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="968c6-111">För mer information, se [Så här skapar du insamlingsposter för SEPA Autogiro och exporterar till en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="968c6-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="968c6-112">Välj åtgärden **Bokför betalningsinleveranser**.</span><span class="sxs-lookup"><span data-stu-id="968c6-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="968c6-113">I fönstret **Bokför samling med autogiro** fyller du i fälten enligt instruktionerna i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="968c6-113">In the **Post Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="968c6-114">Fält</span><span class="sxs-lookup"><span data-stu-id="968c6-114">Field</span></span>|<span data-ttu-id="968c6-115">Description</span><span class="sxs-lookup"><span data-stu-id="968c6-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="968c6-116">**Autogirosamlingsnr.**</span><span class="sxs-lookup"><span data-stu-id="968c6-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="968c6-117">Ange autogiroinsamlingen som du vill bokföra betalningskvittot för.</span><span class="sxs-lookup"><span data-stu-id="968c6-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="968c6-118">**Redovisningsjournalmall**</span><span class="sxs-lookup"><span data-stu-id="968c6-118">**General Journal Template**</span></span>|<span data-ttu-id="968c6-119">Ange vilken redovisningsjournalmallen som ska användas för att bokföra betalningskvitto, t.ex. mall för inbetalningar.</span><span class="sxs-lookup"><span data-stu-id="968c6-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="968c6-120">**Redovisningsjournalnamn**</span><span class="sxs-lookup"><span data-stu-id="968c6-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="968c6-121">Ange vilka redovisningsjournalbatch som ska användas för att bokföra ett betalningskvitto.</span><span class="sxs-lookup"><span data-stu-id="968c6-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="968c6-122">**Skapa enbart journal**</span><span class="sxs-lookup"><span data-stu-id="968c6-122">**Create Journal Only**</span></span>|<span data-ttu-id="968c6-123">Markera den här kryssrutan om du inte vill bokföra betalningskvittot när du väljer **OK** knappen.</span><span class="sxs-lookup"><span data-stu-id="968c6-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="968c6-124">Betalningskvittot skall förberedas i den angivna journalen och bokförs inte förrän någon bokför journalraderna i fråga.</span><span class="sxs-lookup"><span data-stu-id="968c6-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="968c6-125">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="968c6-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="968c6-126">Se även</span><span class="sxs-lookup"><span data-stu-id="968c6-126">See Also</span></span>  
 <span data-ttu-id="968c6-127">[Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="968c6-127">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="968c6-128">Försäljning</span><span class="sxs-lookup"><span data-stu-id="968c6-128">Sales</span></span>](sales-manage-sales.md)

