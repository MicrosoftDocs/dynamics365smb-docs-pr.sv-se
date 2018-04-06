---
title: "Bokför koncerninterna dokument och journaler | Microsoft Docs"
description: "använda koncerninterna dokument för att bokföra transaktioner med partnerföretag."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 98e0d9012dfdd998431aaed8dade02f592af47c8
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-intercompany-documents-and-journals"></a><span data-ttu-id="670d0-103">Arbeta med koncerninterna dokument och journaler</span><span class="sxs-lookup"><span data-stu-id="670d0-103">Work with Intercompany Documents and Journals</span></span>
<span data-ttu-id="670d0-104">Du använder koncerninterna dokument eller journaler för att bokföra transaktioner med koncerninterna partner.</span><span class="sxs-lookup"><span data-stu-id="670d0-104">You use intercompany documents or journals to post transactions with your intercompany partners.</span></span> <span data-ttu-id="670d0-105">När du bokför ett koncerninternt dokument eller journalrad i företaget skapas, skapas ett motsvarande dokument eller journalrad i din koncerninterna utkorg som du kan överföra till partnern.</span><span class="sxs-lookup"><span data-stu-id="670d0-105">When you post an intercompany document or journal line in your company, a corresponding document or journal line is created in your intercompany outbox that you can transfer to your partner.</span></span> <span data-ttu-id="670d0-106">Partnern kan sedan bokföra den koncerninterna transaktionen i sitt företag utan att behöva registrera samma data på nytt.</span><span class="sxs-lookup"><span data-stu-id="670d0-106">Your partner can then post the corresponding transaction in their company, without having to re-enter the data.</span></span>

<span data-ttu-id="670d0-107">För försäljnings- och inköpsdokument, säkerställer koden för koncernintern partner på den involverade kunden eller leverantören att alla order och fakturor som har genererats gäller transaktioner med dessa företag kommer att producera motsvarande dokument i partnerföretaget, vilket resulterar i att räkenskaperna balanseras korrekt.</span><span class="sxs-lookup"><span data-stu-id="670d0-107">For sales and purchase documents, the intercompany partner code on the involved customer or vendor ensures that all orders and invoices generated pertaining to transactions with these companies will produce corresponding documents in the partner company, resulting in correct balancing of the accounts.</span></span>

<span data-ttu-id="670d0-108">För koncerninterna redovisningsjournalrader behöver du inte ange konton för en enskild räkenskapsbok, utan helt enkelt ange moderbolaget.</span><span class="sxs-lookup"><span data-stu-id="670d0-108">For intercompany general journal lines, you do not need to specify the accounts for an individual set of books, but simply give the identification of the partner company.</span></span> <span data-ttu-id="670d0-109">Motsvarande koncerninterna redovisningsjournalrader skapas sedan i partnerföretaget som resulterar i att räkenskaperna balanseras för de båda företag som är involverade i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="670d0-109">Corresponding intercompany general journal lines are then created in the partner company that result in the balancing of the books of both companies involved in a transaction.</span></span>

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a><span data-ttu-id="670d0-110">Så här fyller du i och skickar en koncernintern försäljningsorder</span><span class="sxs-lookup"><span data-stu-id="670d0-110">To fill in and send an intercompany sales order</span></span>
<span data-ttu-id="670d0-111">Du kan skicka försäljnings- och inköpsorder samt returorder före bokföring.</span><span class="sxs-lookup"><span data-stu-id="670d0-111">You can send sales and purchase orders and return orders before posting.</span></span> <span data-ttu-id="670d0-112">Fakturor och kreditnotor kan inte skickas förrän de är bokförda.</span><span class="sxs-lookup"><span data-stu-id="670d0-112">Invoices and credit memos cannot be sent until they are posted.</span></span>

<span data-ttu-id="670d0-113">Följande procedur beskriver hur du fyller i och skickar en koncernintern försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="670d0-113">The following procedure describes how to fill in and send an intercompany sales order.</span></span> <span data-ttu-id="670d0-114">Samma steg gäller koncerninterna inköpsorder och returorder och till bokförda koncerninterna fakturor och kreditnotor.</span><span class="sxs-lookup"><span data-stu-id="670d0-114">The same steps apply to intercompany purchase orders and return orders, and to posted intercompany invoices and credit memos.</span></span>  

1. <span data-ttu-id="670d0-115">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="670d0-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="670d0-116">Välj **Ny** för att skapa en ny försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="670d0-116">Choose **New** to create a new sales order.</span></span> <span data-ttu-id="670d0-117">Mer information finns i [Sälja produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="670d0-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  
3. <span data-ttu-id="670d0-118">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="670d0-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="670d0-119">Se till att kunden är en koncernintern partner.</span><span class="sxs-lookup"><span data-stu-id="670d0-119">Make sure the customer is an intercompany partner.</span></span>
5. <span data-ttu-id="670d0-120">Om du vill skicka försäljningsordern innan du bokför den, väljer du åtgärden **skicka Koncerninterna försäljningsorder**.</span><span class="sxs-lookup"><span data-stu-id="670d0-120">To send the sales order before you post it, choose the **Send IC Sales Order** action.</span></span>

> [!NOTE]
> <span data-ttu-id="670d0-121">Om du utför steg 4, kommer försäljningsordern flyttas till koncerninterna utkorgen där du kan skicka den senare.</span><span class="sxs-lookup"><span data-stu-id="670d0-121">If you do perform step 4, then the sales order will be moved to your intercompany outbox where you can send it later.</span></span> <span data-ttu-id="670d0-122">Mer information finns i [Hantera den koncerninterna inkorgen och utkorgen](intercompany-how-manage-intercompany-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="670d0-122">For more information, see [Manage the Intercompany Inbox and Outbox](intercompany-how-manage-intercompany-inbox.md).</span></span>

## <a name="to-fill-in-and-post-an-intercompany-journal"></a><span data-ttu-id="670d0-123">Så här fyller du i och bokför koncerninterna journaler</span><span class="sxs-lookup"><span data-stu-id="670d0-123">To fill in and post an intercompany journal</span></span>
<span data-ttu-id="670d0-124">När du bokför ett koncernintern redovisningsjournalsrad i företaget skapas, skapas ett motsvarande journalrad i din koncerninterna utkorg som du kan överföra till partnern.</span><span class="sxs-lookup"><span data-stu-id="670d0-124">When you post an intercompany general journal line in your company, a corresponding journal line is created in your intercompany outbox that you can transfer to your partner.</span></span> <span data-ttu-id="670d0-125">Partnern kan sedan bokföra den koncerninterna transaktionen i sitt företag utan att behöva registrera samma data på nytt.</span><span class="sxs-lookup"><span data-stu-id="670d0-125">Your partner can then post the corresponding transaction in their company, without having to re-enter the data.</span></span>

1. <span data-ttu-id="670d0-126">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Konc.int. redovisningsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="670d0-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **IC General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="670d0-127">Öppna relevant journal.</span><span class="sxs-lookup"><span data-stu-id="670d0-127">Open the relevant journal batch.</span></span> <span data-ttu-id="670d0-128">Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="670d0-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="670d0-129">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="670d0-129">Fill in the fields as necessary.</span></span>
4. <span data-ttu-id="670d0-130">I fältet **Redov.ktonr konc.int. partner** anger du det koncerninterna redovisningskontot som beloppet ska bokföras på i partnerns företag.</span><span class="sxs-lookup"><span data-stu-id="670d0-130">In the **IC Partner G/L Acc. No.** field, enter the intercompany general ledger account that the amount will be posted to in your partner's company.</span></span>

    > [!NOTE]
    > <span data-ttu-id="670d0-131">Fältet måste vara ifyllt på en rad med ett bankkonto eller redovisningskonto i antingen fältet **Kontonr.** eller **Motkonto**.</span><span class="sxs-lookup"><span data-stu-id="670d0-131">This field must be filled in on a line with a bank account or general ledger account in either the **Account No.** field or the **Bal. Account No.** field.</span></span>  
5. <span data-ttu-id="670d0-132">Välj åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="670d0-132">Choose the **Post** action.</span></span>

<span data-ttu-id="670d0-133">Transaktionerna som bokförs i företaget och en journal med motsvarande transaktioner skapas i koncerninterna utkorgen som du kan skicka till partnerföretaget.</span><span class="sxs-lookup"><span data-stu-id="670d0-133">The involved entries are posted in your company and a journal with the corresponding entries are created in your intercompany outbox that you can send to your partner company.</span></span> <span data-ttu-id="670d0-134">Mer information finns i [Hantera den koncerninterna inkorgen och utkorgen](intercompany-how-manage-intercompany-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="670d0-134">For more information, see [Manage the Intercompany Inbox and Outbox](intercompany-how-manage-intercompany-inbox.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="670d0-135">Se även</span><span class="sxs-lookup"><span data-stu-id="670d0-135">See Also</span></span>
[<span data-ttu-id="670d0-136">Hantera koncerninterna transaktioner</span><span class="sxs-lookup"><span data-stu-id="670d0-136">Managing Intercompany Transactions</span></span>](intercompany-manage.md)  
[<span data-ttu-id="670d0-137">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="670d0-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="670d0-138">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="670d0-138">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="670d0-139">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="670d0-139">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="670d0-140">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="670d0-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

