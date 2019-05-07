---
title: Ställ in SEPA Kreditöverföringar | Microsoft Docs
description: Lär dig hur du ställer in SEPA-kreditöverföring i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sepa, credit, transfer, payment,
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.openlocfilehash: 56f200d00345bfe18d8fcccbee6493785fe6a034
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "929464"
---
# <a name="set-up-sepa-credit-transfer"></a><span data-ttu-id="6b354-103">Konfigurera SEPA-kreditöverföring</span><span class="sxs-lookup"><span data-stu-id="6b354-103">Set Up SEPA Credit Transfer</span></span>
<span data-ttu-id="6b354-104">Från sidan **Betalningsjournal** kan du exportera betalningar till en fil för överföring till din elektroniska bank för behandling av de relaterade pengaöverföringarna.</span><span class="sxs-lookup"><span data-stu-id="6b354-104">From the **Payment Journal** page, you can export payments to a file for upload to your electronic bank for processing of the related money transfers.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="6b354-105">stödjer SEPA kreditöverföringar-format, men andra format för elektroniska betalningar i ditt land/din region kan finnas.</span><span class="sxs-lookup"><span data-stu-id="6b354-105">supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>  

<span data-ttu-id="6b354-106">Om du vill aktivera export av bankfilformat som inte stöds från början i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du konfigurera en datautbytesdefinition med ramverket för datautbyte.</span><span class="sxs-lookup"><span data-stu-id="6b354-106">To enable export of a bank file formats that are not supported out of the box in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can set up a data exchange definition by using the data exchange framework.</span></span> <span data-ttu-id="6b354-107">Mer information finns i [Så här konfigurerar du dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="6b354-107">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

<span data-ttu-id="6b354-108">Innan du kan bearbeta betalning på elektronisk väg genom att exportera betalningsfiler i formatet SEPA Krediteringsöverföring, måste du utföra följande inställningssteg:</span><span class="sxs-lookup"><span data-stu-id="6b354-108">Before you can process payment electronically by exporting payment files in the SEPA Credit Transfer format, you must perform the following setup steps:</span></span>  

* <span data-ttu-id="6b354-109">Skapa bankkontot i fråga för att hantera format för SEPA-kreditöverföringen.</span><span class="sxs-lookup"><span data-stu-id="6b354-109">Set up the bank account in question to handle the SEPA Credit Transfer format</span></span>  
* <span data-ttu-id="6b354-110">Skapa leverantörskort för att behandla betalningar genom att exportera filer i formatet för SEPA-kreditöverföringen.</span><span class="sxs-lookup"><span data-stu-id="6b354-110">Set up vendor cards to process payments by exporting files in the SEPA Credit Transfer format</span></span>  
* <span data-ttu-id="6b354-111">Ställ in den relaterade redovisningsjournal-batchen för att aktivera betalningsexporten från sidan **Betalningsjournal**</span><span class="sxs-lookup"><span data-stu-id="6b354-111">Set up the related general journal batch to enable payment export from the **Payment Journal** page</span></span>  
* <span data-ttu-id="6b354-112">Så här kan du ansluta datautbytesdefinitionen för en eller flera betalningstyper till lämpliga betalningsmetoder</span><span class="sxs-lookup"><span data-stu-id="6b354-112">Connect the data exchange definition for one or more payment types with the relevant payment method or methods</span></span>  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a><span data-ttu-id="6b354-113">Så här lägger du upp ett bankkonto för SEPA-kreditöverföring</span><span class="sxs-lookup"><span data-stu-id="6b354-113">To set up a bank account for SEPA Credit Transfer</span></span>  
1. <span data-ttu-id="6b354-114">I rutan **Sök**, ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="6b354-114">In the **Search** box, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6b354-115">Öppna kortet för det bankkonto som du ska exportera betalningsfiler från i formatet SEPA Kreditöverföring.</span><span class="sxs-lookup"><span data-stu-id="6b354-115">Open the card of the bank account from which you will export payment files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="6b354-116">På snabbfliken **överför**i fältet **Format för betalningsexport**, välj **SEPADD**.</span><span class="sxs-lookup"><span data-stu-id="6b354-116">On the **Transfer** FastTab, in the **Payment Export Format** field, choose **SEPADD**.</span></span>  
4. <span data-ttu-id="6b354-117">I fältet **SEPA CT Medd ID-nr serie** väljer du en nummerserie från vilken nummer tilldelas till SEPA-kreditöverföringsartiklar.</span><span class="sxs-lookup"><span data-stu-id="6b354-117">In the **SEPA CT Msg. ID No. Series** field, choose a number series from which numbers are assigned to SEPA credit transfer entries.</span></span>  
5. <span data-ttu-id="6b354-118">Se till att fältet **IBAN** är ifyllt.</span><span class="sxs-lookup"><span data-stu-id="6b354-118">Make sure the **IBAN** field is filled.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6b354-119">Fältet **Valutakod** måste anges till **EUR**, eftersom SEPA-kreditöverföringar bara kan utföras i valutan EURO.</span><span class="sxs-lookup"><span data-stu-id="6b354-119">The **Currency Code** field must be set to **EUR**, because SEPA credit transfers can only be made in the EURO currency.</span></span>  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a><span data-ttu-id="6b354-120">Så här lägger du upp ett leverantörskort för SEPA-kreditöverföring</span><span class="sxs-lookup"><span data-stu-id="6b354-120">To set up a vendor card for SEPA Credit Transfer</span></span>  
1. <span data-ttu-id="6b354-121">I rutan **Sök**, ange **Leverantörer** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="6b354-121">In the **Search** box, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6b354-122">Öppna kortet för den leverantör som du ska betala elektronisk genom att exportera betalningsfiler i formatet SEPA Kreditöverföring.</span><span class="sxs-lookup"><span data-stu-id="6b354-122">Open the card of the vendor whom you will pay electronically by export payment files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="6b354-123">På snabbfliken **Betalning** i fältet **Betalningsmetodkod** väljer du **BANK**.</span><span class="sxs-lookup"><span data-stu-id="6b354-123">On the **Payment** FastTab, in the **Payment Method Code** field, choose **BANK**.</span></span>  
4. <span data-ttu-id="6b354-124">I fältet **Föredraget bankkonto** väljer du banken som pengarna ska överföras till när de har behandlat av din elektroniska bank.</span><span class="sxs-lookup"><span data-stu-id="6b354-124">In the **Preferred Bank Account** field, choose the bank to which the money will be transferred when it is processed by your electronic bank.</span></span>  

     <span data-ttu-id="6b354-125">Värdet i fältet **Föredraget bankkonto** kopieras till fältet **mottagarens bankkonto** på sidan **betalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="6b354-125">The value in the **Preferred Bank Account** field is copied to the **Recipient Bank Account** field on the **Payment Journal** page.</span></span>  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a><span data-ttu-id="6b354-126">Så här anger du utbetalningsjournalen för att exportera betalningsfiler</span><span class="sxs-lookup"><span data-stu-id="6b354-126">To set the payment journal up to export payment files</span></span>  
1. <span data-ttu-id="6b354-127">I rutan **Sök**, ange **Utbetalningsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="6b354-127">In the **Search** box, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6b354-128">Öppna utbetalningsjournalen som du använder för att behandla betalningar genom att exportera filer i formatet SEPA Kreditöverföring.</span><span class="sxs-lookup"><span data-stu-id="6b354-128">Open the payment journal that you use to process payments by exporting files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="6b354-129">I fältet **Journalnamn** väljer du listrute\-knappen.</span><span class="sxs-lookup"><span data-stu-id="6b354-129">In the **Batch Name** field, choose the drop\-down button.</span></span>  
4. <span data-ttu-id="6b354-130">På sidan **Redovisningsjournaler** på fliken **Start** i gruppen **Hantera** väljer du **Redigera lista**.</span><span class="sxs-lookup"><span data-stu-id="6b354-130">On the **General Journal Batches** page, on the **Home** tab, in the **Manage** group, choose **Edit List**.</span></span>  
5. <span data-ttu-id="6b354-131">Markera kryssrutan **Tillåt betalningsexport** på raden för utbetalningsjournalen som du kommer att använda när du vill exportera betalningar.</span><span class="sxs-lookup"><span data-stu-id="6b354-131">On the line for the payment journal that you will use to export payments, select the **Allow Payment Export** check box.</span></span>  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a><span data-ttu-id="6b354-132">Så här kan du ansluta datautbytesdefinitionen för en eller flera betalningstyper till lämpliga betalningsmetoder</span><span class="sxs-lookup"><span data-stu-id="6b354-132">To connect the data exchange definition for one or more payment types with the relevant payment method or methods</span></span>  
1. <span data-ttu-id="6b354-133">I rutan **Sök**, ange **Betalningssätt** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="6b354-133">In the **Search** box, enter **Payment Methods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6b354-134">På sidan **Betalningsmetoder** väljer du det betalningssätt som används att exportera betalningar från och väljer sedan fältet **Definition för bet.exportrad**.</span><span class="sxs-lookup"><span data-stu-id="6b354-134">On the **Payment Methods** page, select the payment method that is used to export payments from, and then choose the **Pmt. Export Line Definition** field.</span></span>  
3. <span data-ttu-id="6b354-135">På sidan **Definition för bet.exportrad** väljer du den kod som du har angett i fältet **Kod** på snabbfliken **Definitioner för rad** i steg 4 i avsnittet ”Beskriva layouten för rader och kolumner i filen” i förfarandet [Så här konfigurerar du dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="6b354-135">On the **Pmt. Export Line Definitions** page, select the code that you specified in the **Code** field on the **Line Definitions** FastTab in step 4 in the “To describe the formatting of lines and columns in the file” section in the [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) procedure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6b354-136">Se även</span><span class="sxs-lookup"><span data-stu-id="6b354-136">See Also</span></span>  
[<span data-ttu-id="6b354-137">Samla in betalningar med SEPA-autogiro</span><span class="sxs-lookup"><span data-stu-id="6b354-137">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="6b354-138">Skapa dataintegrationsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="6b354-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="6b354-139">Skapa återkommande försäljnings- och inköpsrader</span><span class="sxs-lookup"><span data-stu-id="6b354-139">Create Recurring Sales and Purchase Lines</span></span>](sales-how-work-standard-lines.md)  
<span data-ttu-id="6b354-140">[Utbyta data elektroniskt](across-data-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="6b354-140">[Exchanging Data Electronically](across-data-exchange.md)</span></span>  
