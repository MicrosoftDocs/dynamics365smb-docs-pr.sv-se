---
title: "Använda tillägg för betalningar och avstämning (DK) | Microsoft Docs"
description: "Det här tillägget gör det enkelt att exportera filer som är förformaterade för att uppfylla bankkraven för elektroniska inlagor."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 09/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b345100f2ec89685855bfd8e630e3ef44506e86d
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---

# <a name="the-payments-and-reconciliations-dk-extension-for-microsoft-dynamics-for-business-central"></a><span data-ttu-id="bbd82-103">Tillägget Betalningar och avstämningar (DK) för Microsoft Dynamics for Business Central</span><span class="sxs-lookup"><span data-stu-id="bbd82-103">The Payments and Reconciliations (DK) Extension for Microsoft Dynamics for Business Central</span></span>
<span data-ttu-id="bbd82-104">Gör snabba, felfria betalninger genom att exportera filer som är specifikt formaterade för utbyte med din leverantör eller bank.</span><span class="sxs-lookup"><span data-stu-id="bbd82-104">Make fast, error-free payments by exporting files that are formatted specifically for exchanges with your vendor or bank.</span></span> <span data-ttu-id="bbd82-105">Filerna påskyndar processerna för betalning och avstämning och undviker fel som kan inträffa när du manuellt anger information på en bankwebbplats.</span><span class="sxs-lookup"><span data-stu-id="bbd82-105">These files speed up the payment and reconciliation processes, and eliminate errors that can happen when you manually enter the information on a bank website.</span></span>  
  
<span data-ttu-id="bbd82-106">Det här tillägget stöder filformat för flera danska banker.</span><span class="sxs-lookup"><span data-stu-id="bbd82-106">This extension supports file formats for several Danish banks.</span></span> <span data-ttu-id="bbd82-107">När du exporterar betalningsinformation till en fil, packar tillägget data i det format som krävs av din bank.</span><span class="sxs-lookup"><span data-stu-id="bbd82-107">When you export payment information to a file, the extension packages the data into the format that your bank requires.</span></span> <span data-ttu-id="bbd82-108">Formaten omfattar till exempel Bankdata-vl, V3, BEC, SDC och FIK som många olika banker använder och några som är mer specialiserade för vissa banker, till exempel Danske Bank och Nordea.</span><span class="sxs-lookup"><span data-stu-id="bbd82-108">For example, the formats include Bankdata-V3, BEC, SDC, and FIK, which many different banks use, and some that are more specialized for certain banks, for example, Danske Bank and Nordea.</span></span> <span data-ttu-id="bbd82-109">Tillägget innehåller dessutom vissa format för import och avstämning av bankutdrag.</span><span class="sxs-lookup"><span data-stu-id="bbd82-109">The extension also includes some formats for importing and reconciling bank statements.</span></span>  
  
> [!Note]
> <span data-ttu-id="bbd82-110">Om du vill använda tillägget måste du känna till det format som banken eller leverantör kräver.</span><span class="sxs-lookup"><span data-stu-id="bbd82-110">To use the extension, you must know the format that your bank or vendor requires.</span></span> <span data-ttu-id="bbd82-111">Vissa banker eller leverantörer tillhandahåller denna information på sina webbplatser; Du kan dock behöva kontakta deras kundservice för att hämta önskad information.</span><span class="sxs-lookup"><span data-stu-id="bbd82-111">Some banks or vendors provide this information on their websites; however, you might need to contact their customer service to get the information.</span></span>  
  
## <a name="supported-bank-formats"></a><span data-ttu-id="bbd82-112">Bankformat som stöds</span><span class="sxs-lookup"><span data-stu-id="bbd82-112">Supported Bank Formats</span></span>
<span data-ttu-id="bbd82-113">Det här tillägget använder följande format för betalningsfiler:</span><span class="sxs-lookup"><span data-stu-id="bbd82-113">This extension can apply the following file formats for payment files:</span></span>  
  
* <span data-ttu-id="bbd82-114">BANKDATA-V3</span><span class="sxs-lookup"><span data-stu-id="bbd82-114">BANKDATA-V3</span></span>  
* <span data-ttu-id="bbd82-115">BEC INDLAND</span><span class="sxs-lookup"><span data-stu-id="bbd82-115">BEC-INDLAND</span></span>  
* <span data-ttu-id="bbd82-116">BEC-CSV</span><span class="sxs-lookup"><span data-stu-id="bbd82-116">BEC-CSV</span></span>  
* <span data-ttu-id="bbd82-117">DANSKEBANK CMKV</span><span class="sxs-lookup"><span data-stu-id="bbd82-117">DANSKEBANK-CMKV</span></span>  
* <span data-ttu-id="bbd82-118">DANSKEBANK CMKXKSX</span><span class="sxs-lookup"><span data-stu-id="bbd82-118">DANSKEBANK-CMKXKSX</span></span>  
* <span data-ttu-id="bbd82-119">DANSKEBANK</span><span class="sxs-lookup"><span data-stu-id="bbd82-119">DANSKEBANK</span></span>  
* <span data-ttu-id="bbd82-120">FIK71</span><span class="sxs-lookup"><span data-stu-id="bbd82-120">FIK71</span></span>  
* <span data-ttu-id="bbd82-121">NORDEA-ERHVERV-CSV</span><span class="sxs-lookup"><span data-stu-id="bbd82-121">NORDEA-ERHVERV-CSV</span></span>  
* <span data-ttu-id="bbd82-122">NORDEA</span><span class="sxs-lookup"><span data-stu-id="bbd82-122">NORDEA</span></span>  
* <span data-ttu-id="bbd82-123">NORDEA-UNITEL-V3</span><span class="sxs-lookup"><span data-stu-id="bbd82-123">NORDEA-UNITEL-V3</span></span>  
* <span data-ttu-id="bbd82-124">SDC</span><span class="sxs-lookup"><span data-stu-id="bbd82-124">SDC</span></span>  
* <span data-ttu-id="bbd82-125">SDC CSV</span><span class="sxs-lookup"><span data-stu-id="bbd82-125">SDC-CSV</span></span>  

## <a name="to-set-up-the-extension"></a><span data-ttu-id="bbd82-126">Så här ställer du in tillägget</span><span class="sxs-lookup"><span data-stu-id="bbd82-126">To set up the extension</span></span>
<span data-ttu-id="bbd82-127">Det finns några steg för att komma igång.</span><span class="sxs-lookup"><span data-stu-id="bbd82-127">There are a few steps to get started.</span></span>  
  
* <span data-ttu-id="bbd82-128">Tillåt betalningsdataexport.</span><span class="sxs-lookup"><span data-stu-id="bbd82-128">Allow payment data exports.</span></span> <span data-ttu-id="bbd82-129">För att skydda dina data, är detta inte är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="bbd82-129">To help protect your data, this is not readily available.</span></span>  
* <span data-ttu-id="bbd82-130">Skapa inköpsorder och leverantörsreskontra så att du inte behöver externa verifikationsnummer på fakturor.</span><span class="sxs-lookup"><span data-stu-id="bbd82-130">Set up purchase and payables so that you do not require external document numbers on invoices.</span></span> <span data-ttu-id="bbd82-131">Om det behövs kan använda du referensnumret för att referera till en viss faktura.</span><span class="sxs-lookup"><span data-stu-id="bbd82-131">If needed, you can use the reference number to refer to a specific invoice.</span></span>  
* <span data-ttu-id="bbd82-132">Ange betalningssätt för varje leverantör.</span><span class="sxs-lookup"><span data-stu-id="bbd82-132">Specify the payment method for each vendor.</span></span> <span data-ttu-id="bbd82-133">Betalningssätt definierar hur du vill betala fakturor från leverantören.</span><span class="sxs-lookup"><span data-stu-id="bbd82-133">Payment methods define how you pay invoices from the vendor.</span></span> <span data-ttu-id="bbd82-134">Till exempel bank, kontanter, check eller konto.</span><span class="sxs-lookup"><span data-stu-id="bbd82-134">For example, Bank, Cash, Check, or Account.</span></span>  
* <span data-ttu-id="bbd82-135">Ange vilket format som ska användas för var och en av dina bankkonton.</span><span class="sxs-lookup"><span data-stu-id="bbd82-135">Specify the type of format to use for each of your bank accounts.</span></span> <span data-ttu-id="bbd82-136">Det kan t.ex. vara NORDEA, DANSKEBANK, SDC.</span><span class="sxs-lookup"><span data-stu-id="bbd82-136">For example, NORDEA, DANSKEBANK, SDC, and so on.</span></span>  
  
<span data-ttu-id="bbd82-137">Dessutom måste du tilldela leverantörer till en inhemsk **Gen. rörelsebokföringsmall** och en **Leverantörsbokföringsmall**.</span><span class="sxs-lookup"><span data-stu-id="bbd82-137">Additionally, you must assign vendors to a domestic **Gen. Bus. Posting Group** and a **Vendor Posting Group**.</span></span> <span data-ttu-id="bbd82-138">Inställningen av Land/Region måste för leverantören vara Danmark (DK).</span><span class="sxs-lookup"><span data-stu-id="bbd82-138">The Country/Region setting for the vendor must be Denmark (DK).</span></span> <span data-ttu-id="bbd82-139">Mer information finns i [Ställa in bokföringsmallar](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="bbd82-139">For more information, see [Setting Up Posting Groups](finance-posting-groups.md).</span></span>  
  
### <a name="to-allow-included365finincludesd365finmdmd-to-export-payment-data"></a><span data-ttu-id="bbd82-140">För att tillåta betalningsdataexport från [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="bbd82-140">To allow [!INCLUDE[d365fin](includes/d365fin_md.md)] to export payment data</span></span>
1. <span data-ttu-id="bbd82-141">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Utbetalningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bbd82-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bbd82-142">I fönstret **Redigera betalningsjournal**, välj journalen **Bank**.</span><span class="sxs-lookup"><span data-stu-id="bbd82-142">In the **Edit Payment Journal** window, choose the **Bank** batch.</span></span>  
3. <span data-ttu-id="bbd82-143">Markera kryssrutan **Tillåt betalningsexport**.</span><span class="sxs-lookup"><span data-stu-id="bbd82-143">Choose the **Allow Payment Export** check box.</span></span>  

### <a name="to-specify-a-payment-method-for-a-vendor"></a><span data-ttu-id="bbd82-144">Ange betalningssätt för en leverantör</span><span class="sxs-lookup"><span data-stu-id="bbd82-144">To specify a payment method for a vendor</span></span>
<span data-ttu-id="bbd82-145">I följande tabell visas kombinationerna av betalningssätten FIK och GIRO som [!INCLUDE[d365fin](includes/d365fin_md.md)] stödjer.</span><span class="sxs-lookup"><span data-stu-id="bbd82-145">The following table shows the combinations of FIK and GIRO payment methods that [!INCLUDE[d365fin](includes/d365fin_md.md)] supports.</span></span>

||<span data-ttu-id="bbd82-146">Typ 01</span><span class="sxs-lookup"><span data-stu-id="bbd82-146">Type 01</span></span> | <span data-ttu-id="bbd82-147">Typ 04</span><span class="sxs-lookup"><span data-stu-id="bbd82-147">Type 04</span></span> | <span data-ttu-id="bbd82-148">Typ 71</span><span class="sxs-lookup"><span data-stu-id="bbd82-148">Type 71</span></span> | <span data-ttu-id="bbd82-149">Typ 73</span><span class="sxs-lookup"><span data-stu-id="bbd82-149">Type 73</span></span> |
|----|---|---|---|---|
|<span data-ttu-id="bbd82-150">Postgiro eller FIK fordringsägarenr?</span><span class="sxs-lookup"><span data-stu-id="bbd82-150">Giro Account No. or FIK Creditor No.?</span></span> | <span data-ttu-id="bbd82-151">Postgiro</span><span class="sxs-lookup"><span data-stu-id="bbd82-151">Giro Account No.</span></span> | <span data-ttu-id="bbd82-152">Postgiro</span><span class="sxs-lookup"><span data-stu-id="bbd82-152">Giro Account No.</span></span> | <span data-ttu-id="bbd82-153">FIK Fordringsägarenr.</span><span class="sxs-lookup"><span data-stu-id="bbd82-153">FIK Creditor No.</span></span> | <span data-ttu-id="bbd82-154">FIK Fordringsägarenr.</span><span class="sxs-lookup"><span data-stu-id="bbd82-154">FIK Creditor No.</span></span>|
|<span data-ttu-id="bbd82-155">Tillåta meddelande till mottagare?</span><span class="sxs-lookup"><span data-stu-id="bbd82-155">Allows Message to Recipient?</span></span> | <span data-ttu-id="bbd82-156">Ja</span><span class="sxs-lookup"><span data-stu-id="bbd82-156">Yes</span></span> |<span data-ttu-id="bbd82-157">Nej</span><span class="sxs-lookup"><span data-stu-id="bbd82-157">No</span></span> |<span data-ttu-id="bbd82-158">Nej</span><span class="sxs-lookup"><span data-stu-id="bbd82-158">No</span></span> | <span data-ttu-id="bbd82-159">Ja</span><span class="sxs-lookup"><span data-stu-id="bbd82-159">Yes</span></span> |
|<span data-ttu-id="bbd82-160">Innehåller betalningsreferensnummer?</span><span class="sxs-lookup"><span data-stu-id="bbd82-160">Contains Payment Reference number?</span></span> | <span data-ttu-id="bbd82-161">Nej</span><span class="sxs-lookup"><span data-stu-id="bbd82-161">No</span></span> | <span data-ttu-id="bbd82-162">Ja, 16 siffror.</span><span class="sxs-lookup"><span data-stu-id="bbd82-162">Yes, 16 digits.</span></span> | <span data-ttu-id="bbd82-163">Ja, 15 siffror.</span><span class="sxs-lookup"><span data-stu-id="bbd82-163">Yes, 15 digits.</span></span> | <span data-ttu-id="bbd82-164">Nej</span><span class="sxs-lookup"><span data-stu-id="bbd82-164">No</span></span>|

1. <span data-ttu-id="bbd82-165">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Leverantör** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bbd82-165">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bbd82-166">Öppna kortet, expandera fliken **betalningar** i fältet **betalningssätt** och välj betalningssätt.</span><span class="sxs-lookup"><span data-stu-id="bbd82-166">Open the card, expand the **Payments** tab, in the **Payment Method** field choose the payment method.</span></span>  
3. <span data-ttu-id="bbd82-167">I vissa fall måste du fylla i andra fält.</span><span class="sxs-lookup"><span data-stu-id="bbd82-167">Depending on your selection, you must complete other fields.</span></span> <span data-ttu-id="bbd82-168">Se tabellen ovan för mer information om kombinationer.</span><span class="sxs-lookup"><span data-stu-id="bbd82-168">See the table above for a description of the combinations.</span></span>  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a><span data-ttu-id="bbd82-169">Ange formaten som ska användas för ett bankkonto</span><span class="sxs-lookup"><span data-stu-id="bbd82-169">To specify the format to use for a bank account</span></span>
1. <span data-ttu-id="bbd82-170">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bbd82-170">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bbd82-171">Öppna kortet för bankkontokort.</span><span class="sxs-lookup"><span data-stu-id="bbd82-171">Open the card for the bank account.</span></span>  
3. <span data-ttu-id="bbd82-172">I fältet **Format för betalningsexport**, välj format för exportfilen.</span><span class="sxs-lookup"><span data-stu-id="bbd82-172">In the **Payment Export Format** field, choose the format for your export file.</span></span>  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a><span data-ttu-id="bbd82-173">Välja FIK eller Giro betalningsinformation för leverantörsfakturor</span><span class="sxs-lookup"><span data-stu-id="bbd82-173">Choosing the FIK or Giro payment information for vendor invoices</span></span>
1. <span data-ttu-id="bbd82-174">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Inköpsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bbd82-174">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="bbd82-175">Välj Leverantören.</span><span class="sxs-lookup"><span data-stu-id="bbd82-175">Choose the vendor.</span></span> <span data-ttu-id="bbd82-176">Kom ihåg att detta måste en dansk leverantör med adress i Danmark.</span><span class="sxs-lookup"><span data-stu-id="bbd82-176">Remember, this must be a Danish vendor with an address in Denmark.</span></span>
3. <span data-ttu-id="bbd82-177">Skapa en faktura.</span><span class="sxs-lookup"><span data-stu-id="bbd82-177">Create an invoice.</span></span> <span data-ttu-id="bbd82-178">Fälten **betalningssätt** och **leverantörsnummer** fylls i baserat på inställningarna på leverantörskortet.</span><span class="sxs-lookup"><span data-stu-id="bbd82-178">The **Payment Method** and **Vendor Number** fields are filled in based on settings on the Vendor card.</span></span> <span data-ttu-id="bbd82-179">Du kan ändra dem om du vill.</span><span class="sxs-lookup"><span data-stu-id="bbd82-179">You can change them if you want.</span></span>
4. <span data-ttu-id="bbd82-180">I fältet **betalningsreferens** anger du det 15-siffriga numret på leverantörens faktura.</span><span class="sxs-lookup"><span data-stu-id="bbd82-180">In the **Payment Reference** field, enter the 15-digit number from the vendor invoice.</span></span>  
  
    > [!Tip]
    > <span data-ttu-id="bbd82-181">Du behöver bara lägga till de senaste 11 siffrorna.</span><span class="sxs-lookup"><span data-stu-id="bbd82-181">You only have to add the last 11 digits of the number.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="bbd82-182"> lägger till fyra nollor i början av numret.</span><span class="sxs-lookup"><span data-stu-id="bbd82-182"> will add four zeros to the beginning of the number.</span></span>  
  
5. <span data-ttu-id="bbd82-183">Bokföra fakturan</span><span class="sxs-lookup"><span data-stu-id="bbd82-183">Post the invoice.</span></span>

## <a name="to-use-the-extension-to-export-payment-data"></a><span data-ttu-id="bbd82-184">Du använder tillägget för att exportera betalningsdata</span><span class="sxs-lookup"><span data-stu-id="bbd82-184">To use the extension to export payment data</span></span>
1. <span data-ttu-id="bbd82-185">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Utbetalningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bbd82-185">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bbd82-186">Välj åtgärden **Föreslå betalningsjournaler för leverantör**.</span><span class="sxs-lookup"><span data-stu-id="bbd82-186">Choose the **Suggest Vendor Payment Journals** action.</span></span>  
  
    > [!Tip]
    > <span data-ttu-id="bbd82-187">Om du endast vill exportera specifika betalningar kan du använda alternativen för filtrering av data.</span><span class="sxs-lookup"><span data-stu-id="bbd82-187">If you want to export only specific payments, use the options for filtering the data.</span></span>  
  
3. <span data-ttu-id="bbd82-188">Om det behövs kan du lägga till filter om du endast vill exportera specifika betalningar.</span><span class="sxs-lookup"><span data-stu-id="bbd82-188">If needed, you can add filters to export only specific payments.</span></span>  
4. <span data-ttu-id="bbd82-189">I fältet **Bankbetalningstyp** väljer du **Elektronisk betalning.**</span><span class="sxs-lookup"><span data-stu-id="bbd82-189">In the **Bank Payment Type** field, choose **Electronic Payment**.</span></span>  
5. <span data-ttu-id="bbd82-190">Välj åtgärden **Exportera**.</span><span class="sxs-lookup"><span data-stu-id="bbd82-190">Choose the **Export** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bbd82-191">Se även</span><span class="sxs-lookup"><span data-stu-id="bbd82-191">See also</span></span>
<span data-ttu-id="bbd82-192">[Anpassning av Business Central för [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="bbd82-192">[Customizing Business Central for [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="bbd82-193">Skapa insamlingsposter för SEPA Autogiro och exportera till en bankfil</span><span class="sxs-lookup"><span data-stu-id="bbd82-193">Create SEPA Direct Debit Collection Entries and Export to a Bank File</span></span>](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
[<span data-ttu-id="bbd82-194">Konfigurera SEPA autogiro</span><span class="sxs-lookup"><span data-stu-id="bbd82-194">Set Up SEPA Direct Debit</span></span>](finance-how-to-set-up-sepa-direct-debit.md)  
[<span data-ttu-id="bbd82-195">Så här bokför du betalningsinleveranser för SEPA Autogiro</span><span class="sxs-lookup"><span data-stu-id="bbd82-195">Post SEPA Direct Debit Payment Receipts</span></span>](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[<span data-ttu-id="bbd82-196">Samla in betalningar med SEPA-autogiro</span><span class="sxs-lookup"><span data-stu-id="bbd82-196">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="bbd82-197">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="bbd82-197">Working with General Journals</span></span>](ui-work-general-journals.md)  





