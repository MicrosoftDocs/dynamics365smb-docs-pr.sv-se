---
title: "Exportera insamlingsposter för SEPA Autogiro | Microsoft Docs"
description: "Skapa en insamling för autogiro som innehåller information om kundens bankkonto och de berörda fakturorna och autogiromedgivandet."
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
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 34fb52bd39036477b479a4de626225876cfe5800
ms.contentlocale: sv-se
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-create-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a><span data-ttu-id="26624-103">Så här skapar du insamlingsposter för SEPA Autogiro och exporterar till en bankfil</span><span class="sxs-lookup"><span data-stu-id="26624-103">How to: Create SEPA Direct Debit Collection Entries and Export to a Bank File</span></span>
<span data-ttu-id="26624-104">För instruktioner till banken för att överföra betalningsbeloppet från kundens bankkonto till ditt företags konto, skapa en autogiroinsamling som innehåller information om kundens bankkonto, de berörda försäljningsfakturorna och medgivande för autogiro.</span><span class="sxs-lookup"><span data-stu-id="26624-104">To instruct the bank to transfer the payment amount from the customer’s bank account to your company’s account, you create a direct-debit collection, which holds information about the customer’s bank account, the affected sales invoices, and the direct-debit mandate.</span></span> <span data-ttu-id="26624-105">Från direktdebitering-insamlingsposten som skapas kan du sedan exportera en XML-fil som du skickar eller överför till din elektroniska bank för bearbetning.</span><span class="sxs-lookup"><span data-stu-id="26624-105">From the resulting direct-debit collection entry, you then export an XML file that you send or upload to your electronic bank for processing.</span></span> <span data-ttu-id="26624-106">Alla betalningar som inte kunde behandlas av banken meddelas till dig av din bank och du måste sedan manuellt avvisa de aktuella autogiroinsamlingsposterna.</span><span class="sxs-lookup"><span data-stu-id="26624-106">Any payments that could not be processed by the bank will be communicated to you by your bank, and you must then manually reject the direct debit-collection entries in question.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="26624-107">För att samla in betalningar med hjälp av SEPA Autogiro måste valutan på försäljningsfakturan vara EURO.</span><span class="sxs-lookup"><span data-stu-id="26624-107">To collect payments using SEPA Direct Debit, the currency on the sales invoice must be EURO.</span></span>  

### <a name="to-create-a-direct-debit-collection"></a><span data-ttu-id="26624-108">Skapa en direktdebitering-insamling</span><span class="sxs-lookup"><span data-stu-id="26624-108">To create a direct-debit collection</span></span>  

1. <span data-ttu-id="26624-109">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Autogiroinsamlingar**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26624-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="26624-110">I fönstret **Samlingar med autogiro** i fönstret **Start** i gruppen **Ny** väljer du **Skapa autogiroinsamling**.</span><span class="sxs-lookup"><span data-stu-id="26624-110">In the **Direct Debit Collections** window, on the **Home** tab, in the **New** group, choose **Create Direct Debit Collection**.</span></span>  
3. <span data-ttu-id="26624-111">I fönstret **Skapa samling med autogiro** fyller du i fälten enligt instruktionerna i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="26624-111">In the **Create Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="26624-112">Fält</span><span class="sxs-lookup"><span data-stu-id="26624-112">Field</span></span>|<span data-ttu-id="26624-113">Description</span><span class="sxs-lookup"><span data-stu-id="26624-113">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="26624-114">**Från förfallodatum**</span><span class="sxs-lookup"><span data-stu-id="26624-114">**From Due Date**</span></span>|<span data-ttu-id="26624-115">Ange tidigaste betalningsförfallodatumet på försäljningsfakturor som du vill skapa en direktdebitering-insamling för.</span><span class="sxs-lookup"><span data-stu-id="26624-115">Specify the earliest payment due date on sales invoices that you want to create a direct-debit collection for.</span></span>|  
    |<span data-ttu-id="26624-116">**Till förfallodatum**</span><span class="sxs-lookup"><span data-stu-id="26624-116">**To Due Date**</span></span>|<span data-ttu-id="26624-117">Ange senaste betalningsförfallodatumet på försäljningsfakturor som du vill skapa en direktdebitering-insamling för.</span><span class="sxs-lookup"><span data-stu-id="26624-117">Specify the latest payment due date on sales invoices that you want to create a direct-debit collection for.</span></span>|  
    |<span data-ttu-id="26624-118">**Partnertyp**</span><span class="sxs-lookup"><span data-stu-id="26624-118">**Partner Type**</span></span>|<span data-ttu-id="26624-119">Anger om direktdebitering-insamlingen görs för kunder som är av typen **företag** eller **person**.</span><span class="sxs-lookup"><span data-stu-id="26624-119">Specify if the direct-debit collection is made for customers of type **Company** or **Person**.</span></span>|  
    |<span data-ttu-id="26624-120">**Endast kunder med giltigt medgivande**</span><span class="sxs-lookup"><span data-stu-id="26624-120">**Only Customers With Valid Mandate**</span></span>|<span data-ttu-id="26624-121">Ange om en autogiroinsamling skapas för kunder som har ett giltigt medgivande för autogiro.</span><span class="sxs-lookup"><span data-stu-id="26624-121">Specify if a direct-debit collection is created for customers who have a valid direct-debit mandate.</span></span> <span data-ttu-id="26624-122">**Obs!**  En autogiroinsamling skapas även om fältet **Medgivande-ID för autogiro** inte fylls på försäljningsfakturan.</span><span class="sxs-lookup"><span data-stu-id="26624-122">**Note:**  A direct-debit collection is created even if the **Direct Debit Mandate ID** field is not filled on the sales invoice.</span></span>|  
    |<span data-ttu-id="26624-123">**Endast fakturor med giltigt medgivande**</span><span class="sxs-lookup"><span data-stu-id="26624-123">**Only Invoices With Valid Mandate**</span></span>|<span data-ttu-id="26624-124">Ange om en autogirering skapas för försäljningsfakturor endast om ett giltigt autogiromedgivande väljs i fältet **Medgivande-id för autogiro** på försäljningsfakturan.</span><span class="sxs-lookup"><span data-stu-id="26624-124">Specify if a direct-debit collection is only created for sales invoices if a valid direct-debit mandate is selected in the **Direct Debit Mandate ID** field on the sales invoice.</span></span>|  
    |<span data-ttu-id="26624-125">**Bankkontonr.**</span><span class="sxs-lookup"><span data-stu-id="26624-125">**Bank Account No.**</span></span>|<span data-ttu-id="26624-126">Ange vilka av företagets bankkonton som den insamlade betalningen ska överföras till från kundens bankkonto.</span><span class="sxs-lookup"><span data-stu-id="26624-126">Specify which of your company’s bank accounts the collected payment will be transferred to from the customer’s bank account.</span></span>|  
    |<span data-ttu-id="26624-127">**Bankkontonamn**</span><span class="sxs-lookup"><span data-stu-id="26624-127">**Bank Account Name**</span></span>|<span data-ttu-id="26624-128">Anger namnet på det bankkonto som du väljer i **Bankkontonr** fält.</span><span class="sxs-lookup"><span data-stu-id="26624-128">Specifies the name of the bank account that you select in the **Bank Account No.** field.</span></span> <span data-ttu-id="26624-129">Detta fält fylls i automatiskt.</span><span class="sxs-lookup"><span data-stu-id="26624-129">This field is filled automatically.</span></span>|  

4. <span data-ttu-id="26624-130">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="26624-130">Choose the **OK** button.</span></span>  

     <span data-ttu-id="26624-131">En autogiroinsamling läggs till i fönstret **Autogiroinsamlingar** och en eller flera autogiroinsamlingsposter skapas.</span><span class="sxs-lookup"><span data-stu-id="26624-131">A direct-debit collection is added to the **Direct Debit Collections** window, and one or more direct-debit collection entries are created.</span></span>  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a><span data-ttu-id="26624-132">Så här exporterar du direktdebeterings-insamlingposter till en bankfil</span><span class="sxs-lookup"><span data-stu-id="26624-132">To export a direct-debit collection entry to a bank file</span></span>  
1. <span data-ttu-id="26624-133">I fönstret **Samlingar med autogiro** i fönstret **Start** i gruppen **Process** väljer du **Transaktioner för samlingar med autogiro**.</span><span class="sxs-lookup"><span data-stu-id="26624-133">In the **Direct Debit Collections** window, on the **Home** tab, in the **Process** group, choose **Direct Debit Collect. Entries**.</span></span>  
2. <span data-ttu-id="26624-134">Fönstret **Transaktioner för samlingar med autogiro**-fönster, markera den post som du vill exportera och sedan på fliken **Start** i gruppen **Process** väljer du **Skapa autogirofil**.</span><span class="sxs-lookup"><span data-stu-id="26624-134">In the **Direct Debit Collect. Entries** window, select the entry that you want to export, and then, on the **Home** tab, in the **Process** group, choose **Create Direct Debit** File.</span></span>  
3. <span data-ttu-id="26624-135">Spara exportfilen på den plats från vilken du skickar eller överför den till din elektroniska bank.</span><span class="sxs-lookup"><span data-stu-id="26624-135">Save the export file to the location from where you send or upload it to your electronic bank.</span></span>  

     <span data-ttu-id="26624-136">I fönstret **Transaktioner för samlingar med autogiro** kan fältet **Status för autogirosamling** ändras till fil.</span><span class="sxs-lookup"><span data-stu-id="26624-136">In the **Direct Debit Collect. Entries** window, the **Direct Debit Collection Status** field is changed to File Created.</span></span> <span data-ttu-id="26624-137">I fönstret **SEPA Autogiromedgivanden** kan fältet **Debet antal** uppdateras fältet med ett antal.</span><span class="sxs-lookup"><span data-stu-id="26624-137">In the **SEPA Direct Debit Mandates** window, the **Debit Counter** field is updated with one count.</span></span>  

<span data-ttu-id="26624-138">Om den exporterade filen inte kan behandlas, till exempel eftersom kunden är insolvent, kan du avvisa direktdebitering-insamlingsposten.</span><span class="sxs-lookup"><span data-stu-id="26624-138">If the exported file cannot be processed, for example because the customer is insolvent, you can reject the direct-debit collection entry.</span></span> <span data-ttu-id="26624-139">Om den exporterade filen har bearbetats av banken, samlas automatiskt förfallna betalningar på de berörda försäljningsfakturorna från berörda kunder.</span><span class="sxs-lookup"><span data-stu-id="26624-139">If the exported file is successfully processed by the bank, the due payments of the involved sales invoices are automatically collected from the involved customers.</span></span> <span data-ttu-id="26624-140">I så fall kan du stänga samlingen.</span><span class="sxs-lookup"><span data-stu-id="26624-140">In that case you can close the collection.</span></span>  

### <a name="to-reject-a-direct-debit-collection-entry"></a><span data-ttu-id="26624-141">Avvisa en direktdebitering-insamlingspost</span><span class="sxs-lookup"><span data-stu-id="26624-141">To reject a direct-debit collection entry</span></span>  

* <span data-ttu-id="26624-142">I fönstret **Transaktioner för samlingar med autogiro**-fönster, markera den post som inte behandlades korrekt, och sedan på **Start** i gruppen **Process** och välj **Avvisa transaktionen**.</span><span class="sxs-lookup"><span data-stu-id="26624-142">In the **Direct Debit Collect. Entries** window, select the entry that was not successfully processed, and then, on the **Home** tab, in the **Process** group, choose **Reject Entry**.</span></span>  

     <span data-ttu-id="26624-143">Värdet **Status** i **Transaktioner för samlingar med autogiro** ändras till **Avvisad**.</span><span class="sxs-lookup"><span data-stu-id="26624-143">The value in the **Status** field in the **Direct Debit Collect. Entries** window is changed to **Rejected**.</span></span>  

### <a name="to-close-a-direct-debit-collection"></a><span data-ttu-id="26624-144">Stänga en direktdebitering-insamling</span><span class="sxs-lookup"><span data-stu-id="26624-144">To close a direct-debit collection</span></span>  
*  <span data-ttu-id="26624-145">I fönstret **Transaktioner för samlingar med autogiro**-fönster, markera den post som inte behandlades korrekt, och sedan på **Start** i gruppen **Process** och välj **Stäng samling**.</span><span class="sxs-lookup"><span data-stu-id="26624-145">In the **Direct Debit Collect. Entries** window, select the entry that was successfully processed, and then, on the **Home** tab, in the **Process** group, choose **Close Collection**.</span></span>  

     <span data-ttu-id="26624-146">Relaterade direktdebitering-insamlingen är stängd.</span><span class="sxs-lookup"><span data-stu-id="26624-146">The related direct-debit collection is closed.</span></span>  

<span data-ttu-id="26624-147">Du kan nu fortsätta med att bokföra inleveranser för de berörda försäljningsfakturorna.</span><span class="sxs-lookup"><span data-stu-id="26624-147">You can now proceed to post receipts of payment for the involved sales invoices.</span></span> <span data-ttu-id="26624-148">Du kan göra detta om du ofta bokför betalningsinleveranser, som i fönstret **Betalningsregistrering** eller du kan bokföra de relaterade betalningsinleveranser direkt från **Transaktioner för samlingar med autogiro**.</span><span class="sxs-lookup"><span data-stu-id="26624-148">You can do this as you typically post payment receipts, such as in the **Payment Registration** window, or you can post the related payment receipts directly from the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="26624-149">Mer information finns i [så här: Bokför betalningsinleveranser för SEPA Autogiro](finance-how-to-post-sepa-direct-debit-payment-receipts.md).</span><span class="sxs-lookup"><span data-stu-id="26624-149">For more information, see [How to: Post SEPA Direct Debit Payment Receipts](finance-how-to-post-sepa-direct-debit-payment-receipts.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="26624-150">Se även</span><span class="sxs-lookup"><span data-stu-id="26624-150">See Also</span></span>  
[<span data-ttu-id="26624-151">Så här: Konfigurera SEPA Autogiro</span><span class="sxs-lookup"><span data-stu-id="26624-151">How to: Set Up SEPA Direct Debit</span></span>](finance-how-to-set-up-sepa-direct-debit.md)  
[<span data-ttu-id="26624-152">Så här bokför du betalningsinleveranser för SEPA Autogiro</span><span class="sxs-lookup"><span data-stu-id="26624-152">How to: Post SEPA Direct Debit Payment Receipts</span></span>](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[<span data-ttu-id="26624-153">Samla in betalningar med SEPA-autogiro</span><span class="sxs-lookup"><span data-stu-id="26624-153">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
