---
title: "Använd batch-jobbet Betalningsförslag för lev. | Microsoft Docs"
description: "Du kan ange leverantörsbetalningsinställningar för att få förslag till betalningar som förfaller snart eller där en rabatt kan erhållas."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7d2ebaf1efe49c8a66e6d562ab7655d45e181044
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="suggest-vendor-payments"></a><span data-ttu-id="e4617-103">Betalningsförslag för lev.</span><span class="sxs-lookup"><span data-stu-id="e4617-103">Suggest Vendor Payments</span></span>
<span data-ttu-id="e4617-104">I fönstret **Betalningsjournal** kan du använda batch-jobbet **Föreslå leverantörsbetalning** för att föreslå betalningsrader.</span><span class="sxs-lookup"><span data-stu-id="e4617-104">In the **Payment Journal** window, you can use the **Suggest Vendor Payments** batch job to suggest payment lines.</span></span> <span data-ttu-id="e4617-105">Rader för saker som t.ex. betalningar som förfaller snart eller betalningar där en kassarabatt finns tillgänglig föreslås utifrån dina inställningar.</span><span class="sxs-lookup"><span data-stu-id="e4617-105">Lines for payments that are due soon or payments where a payment discount is available are suggested based on your settings.</span></span>

<span data-ttu-id="e4617-106">För att dra full nytta av betalningsförslagen, måste du prioritera leverantörerna.</span><span class="sxs-lookup"><span data-stu-id="e4617-106">To benefit fully from payment suggestions, you must first prioritize your vendors.</span></span> <span data-ttu-id="e4617-107">Mer information finns i [Så här prioriterar du leverantörer](purchasing-how-prioritize-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="e4617-107">For more information, see [Prioritize Vendors](purchasing-how-prioritize-vendors.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="e4617-108">Leverantörsreskontratransaktioner som är **Stoppade** tas inte med i batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="e4617-108">Vendor ledger entries that are **On Hold** are not included in the batch job.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="e4617-109">Om du vill utnyttja kassarabatterna och har angett ett disponibelt belopp, används beloppet för:</span><span class="sxs-lookup"><span data-stu-id="e4617-109">If you want to take advantage of payment discounts, and have entered an available amount, the amount will be used for:</span></span>  
    * <span data-ttu-id="e4617-110">Prioritera förfallna leverantörstransaktioner först efter prioritet.</span><span class="sxs-lookup"><span data-stu-id="e4617-110">Prioritized overdue vendor entries first in order of priority.</span></span>   
    * <span data-ttu-id="e4617-111">Förfallna leverantörstransaktioner som inte prioriterats.</span><span class="sxs-lookup"><span data-stu-id="e4617-111">Overdue vendor entries that are not prioritized.</span></span>  
    * <span data-ttu-id="e4617-112">Öppna leverantörstransaktioner som är berättigade till kassarabatter, ordnade efter leverantörsnummer.</span><span class="sxs-lookup"><span data-stu-id="e4617-112">Open vendor entries that qualify for payment discounts, arranged by vendor number.</span></span>  

## <a name="to-use-the-suggest-vendor-payments-function"></a><span data-ttu-id="e4617-113">Om du vill använda funktionen Betalningsförslag för lev.</span><span class="sxs-lookup"><span data-stu-id="e4617-113">To use the Suggest Vendor Payments function</span></span>
1. <span data-ttu-id="e4617-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Betalningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e4617-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e4617-115">Öppna den relevanta journalen och välj sedan åtgärden **Betalningsförslag för lev.**.</span><span class="sxs-lookup"><span data-stu-id="e4617-115">Open the relevant journal, and then choose the **Suggest Vendor Payments** action.</span></span>  
3. <span data-ttu-id="e4617-116">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="e4617-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="e4617-117">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4617-117">Choose the **OK** button.</span></span>  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><span data-ttu-id="e4617-118">Så här infogar du förfallodatum som bokföringsdatum på betalningsjournalrader</span><span class="sxs-lookup"><span data-stu-id="e4617-118">To insert the due date as posting date on payment journal lines</span></span>
<span data-ttu-id="e4617-119">När du använder **Betalningsförslag för lev.**-batchjobbet för att skapa betalningsrader för leverantörer, kan du fylla två specialfält så att de genererade raderna använder förfallodatumet för att beräkna bokföringsdatumet.</span><span class="sxs-lookup"><span data-stu-id="e4617-119">When you use the **Suggest Vendor Payments** batch job to create payment lines for your vendors, you can fill two special fields to make sure that the generated lines use the due date to calculate the posting date.</span></span> <span data-ttu-id="e4617-120">Dessa fält är **Beräkna bokföringsdatum från dokumentets förfallodatum** och **Dokumentets förfallodatum är förskjutet**.</span><span class="sxs-lookup"><span data-stu-id="e4617-120">These fields are **Calculate Posting Date from Applies-to-Doc Due Date** and **Applies-to-Doc Due Date Offset**.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="e4617-121">Du kan inte använda fältet **Beräkna bokföringsdatum från dokumentets förfallodatum** tillsammans med fältet **Utnyttja kassarabatter** eller fältet **Summering per leverantör**.</span><span class="sxs-lookup"><span data-stu-id="e4617-121">You cannot use the **Calculate Posting Date from Applies-to-Doc Due Date** field together with the **Find Payment Discounts** field or the **Summarize per Vendor** field.</span></span> <span data-ttu-id="e4617-122">Om bokföringsdatumet baseras på förfallodatum, så kan vissa kassarabatter kanske inte beräknas korrekt eftersom bokföringsdatumet är efter kassarabattdatumet.</span><span class="sxs-lookup"><span data-stu-id="e4617-122">If the posting date is based on the due date, some payment discounts may not calculate correctly because the posting date is after the payment discount date.</span></span>  

<span data-ttu-id="e4617-123">Dessutom, om det beräknade bokföringsdatum inträffar tidigare flyttas bokföringsdatumet fram till arbetsdatumet, och en varning visas.</span><span class="sxs-lookup"><span data-stu-id="e4617-123">Also, if the calculated posting date is in the past, then the posting date is moved up to the work date, and a warning is displayed.</span></span>  

<span data-ttu-id="e4617-124">Du kan även skapa betalningsrader manuellt genom att använda förfallodatum för att beräkna bokföringsdatum.</span><span class="sxs-lookup"><span data-stu-id="e4617-124">Alternatively, you can manually create payment lines using the due date to calculate the posting date.</span></span> <span data-ttu-id="e4617-125">När du har installerat leverantörsreskontratransaktioner kan du använda åtgärden **beräkna bokföringsdatum** för att uppdatera bokföringsdatumet på journalraden med förfallodatumet för relaterad inköpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="e4617-125">After you apply vendor ledger entries, you can use the **Calculate Posting Date** action to update the posting date on the journal line with the due date of the related purchase invoice.</span></span> <span data-ttu-id="e4617-126">Mer information finns i [Så här kopplar du inköpstransaktioner manuellt](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="e4617-126">For more information, see [Apply Purchase Transactions Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="e4617-127">Om inköpsfakturan har förfallit kommer bokföringsdatum att anges till arbetsdatumet, och teckensnittet på raden ändras till röd färg.</span><span class="sxs-lookup"><span data-stu-id="e4617-127">If the purchase invoice is overdue, the posting date is set to the work date, and the font on the line becomes red.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e4617-128">Se även</span><span class="sxs-lookup"><span data-stu-id="e4617-128">See Also</span></span>
[<span data-ttu-id="e4617-129">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="e4617-129">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="e4617-130">Göra betalningar</span><span class="sxs-lookup"><span data-stu-id="e4617-130">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="e4617-131">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="e4617-131">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="e4617-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e4617-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

