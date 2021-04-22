---
title: Skicka elektroniska dokument
description: Så här skickar du fakturor elektroniskt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8056aa66531740634fb155e0b3b4419a7f014ffc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778378"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="9bea3-103">Skicka elektroniska dokument</span><span class="sxs-lookup"><span data-stu-id="9bea3-103">Send Electronic Documents</span></span>

<span data-ttu-id="9bea3-104">Den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] stöder utskick av elektroniska fakturor och kreditnotor i PEPPOL-format, ett format som stöds av de största leverantörerna av dokumentutbytestjänster.</span><span class="sxs-lookup"><span data-stu-id="9bea3-104">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports sending electronic invoices and credit memos in the PEPPOL format, a format that the largest document exchange service providers support.</span></span> <span data-ttu-id="9bea3-105">En leverantör av dokumentväxlingstjänster skickar dokument elektroniskt mellan handelspartners.</span><span class="sxs-lookup"><span data-stu-id="9bea3-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="9bea3-106">För att få stöd för andra elektroniska dokumentformat använder du ramverket för datautbyte.</span><span class="sxs-lookup"><span data-stu-id="9bea3-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="9bea3-107">I den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] finns en förkonfigurerad dokumentväxlingstjänst som är inställningsklar för företaget.</span><span class="sxs-lookup"><span data-stu-id="9bea3-107">In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="9bea3-108">Mer information finns i [Konfigurera en dokumentväxlingstjänst](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="9bea3-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span> <span data-ttu-id="9bea3-109">I vissa fall måste du dock installera en app.</span><span class="sxs-lookup"><span data-stu-id="9bea3-109">However, in some cases, you must install an app.</span></span> <span data-ttu-id="9bea3-110">Mer information finns i [Vanliga frågor om elektronisk fakturering](faq-electronic-invoicing.yml).</span><span class="sxs-lookup"><span data-stu-id="9bea3-110">For more information, see [Electronic Invoicing FAQ](faq-electronic-invoicing.yml).</span></span>  

 <span data-ttu-id="9bea3-111">Om du vill skicka en försäljningsfaktura som ett elektroniskt PEPPOL-dokument väljer du **Elektroniskt dokument** i dialogrutan **Bokför och skicka**.</span><span class="sxs-lookup"><span data-stu-id="9bea3-111">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box.</span></span> <span data-ttu-id="9bea3-112">Från denna dialogruta kan du även konfigurera kundens standardprofil för dokumentutskick.</span><span class="sxs-lookup"><span data-stu-id="9bea3-112">You can also set up the customer's default document sending profile from that dialog box.</span></span> <span data-ttu-id="9bea3-113">Först måste du skapa olika huvuddata, som företagsinformation, kunder, artiklar och enheter.</span><span class="sxs-lookup"><span data-stu-id="9bea3-113">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="9bea3-114">Dessa används för att identifiera dina affärspartners och artiklar vid konvertering av data i fält i [Så här konfigurerar du utskick och mottagning av elektroniska dokument](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="9bea3-114">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="9bea3-115">Så här kan du skicka en elektronisk försäljningsfaktura</span><span class="sxs-lookup"><span data-stu-id="9bea3-115">To send an electronic sales invoice</span></span>

1. <span data-ttu-id="9bea3-116">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Försäljningsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9bea3-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2. <span data-ttu-id="9bea3-117">Skapa en ny försäljningsfaktura.</span><span class="sxs-lookup"><span data-stu-id="9bea3-117">Create a new sales invoice.</span></span>  

3. <span data-ttu-id="9bea3-118">När försäljningsfakturaraderna är klara att faktureras väljer du åtgärden **Bokföra och skicka**.</span><span class="sxs-lookup"><span data-stu-id="9bea3-118">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="9bea3-119">Om kundens standardprofil för utskick är **Elektroniskt dokument** visas denna i dialogrutan **Bokför och skicka bekräftelse**.</span><span class="sxs-lookup"><span data-stu-id="9bea3-119">If the customer's default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box.</span></span> <span data-ttu-id="9bea3-120">På så sätt behöver du bara välja **Ja**-knappen för att bokföra och skicka fakturan elektroniskt i det valda formatet.</span><span class="sxs-lookup"><span data-stu-id="9bea3-120">This way, you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4. <span data-ttu-id="9bea3-121">Välj knappen AssistEdit till höger om fältet **Skicka dokument till** i dialogrutan **Bekräftelse för bokför och utskick**.</span><span class="sxs-lookup"><span data-stu-id="9bea3-121">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5. <span data-ttu-id="9bea3-122">Välj **Genom dokumentväxlingstjänst** i dialogrutan **Skicka dokument till** dialogrutan i fältet **Genom dokumentväxlingstjänst**.</span><span class="sxs-lookup"><span data-stu-id="9bea3-122">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6. <span data-ttu-id="9bea3-123">Välj **PEPPOL** i fältet **Format**.</span><span class="sxs-lookup"><span data-stu-id="9bea3-123">In the **Format** field, choose **PEPPOL**.</span></span>  

7. <span data-ttu-id="9bea3-124">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bea3-124">Choose the **OK** button.</span></span> <span data-ttu-id="9bea3-125">Dialogrutan **Bekräftelse för bokför och utskick** visas.</span><span class="sxs-lookup"><span data-stu-id="9bea3-125">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="9bea3-126">**Elektroniskt dokument (PEPPOL)** läggs till i fältet **Skicka dokument till**.</span><span class="sxs-lookup"><span data-stu-id="9bea3-126">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8. <span data-ttu-id="9bea3-127">Välj **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9bea3-127">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="9bea3-128">Försäljningsfakturan bokförs och skickas till kunden i PEPPOL-format.</span><span class="sxs-lookup"><span data-stu-id="9bea3-128">The sales invoice is posted and sent to the customer in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="9bea3-129">Du kan även skicka en bokförd försäljningsfaktura som ett elektroniskt dokument.</span><span class="sxs-lookup"><span data-stu-id="9bea3-129">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="9bea3-130">Proceduren är samma som har beskrivits i det här avsnittet för icke-bokförda försäljningsdokument.</span><span class="sxs-lookup"><span data-stu-id="9bea3-130">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="9bea3-131">På sidan **Bokförd försäljningsfaktura** väljer du åtgärden **Aktivitetslogg** för att visa status för det elektroniska dokumentet.</span><span class="sxs-lookup"><span data-stu-id="9bea3-131">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="9bea3-132">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="9bea3-132">See Related Training at [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="9bea3-133">Se även</span><span class="sxs-lookup"><span data-stu-id="9bea3-133">See Also</span></span>

[<span data-ttu-id="9bea3-134">Fakturaförsäljning</span><span class="sxs-lookup"><span data-stu-id="9bea3-134">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="9bea3-135">Skapa dokumentutskicksprofiler</span><span class="sxs-lookup"><span data-stu-id="9bea3-135">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="9bea3-136">Konfigurera utskick och mottagning av elektroniska dokument</span><span class="sxs-lookup"><span data-stu-id="9bea3-136">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="9bea3-137">Konfigurera en tjänst för dokumentutbyte</span><span class="sxs-lookup"><span data-stu-id="9bea3-137">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="9bea3-138">Skapa dataintegreringsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="9bea3-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="9bea3-139">Utbyta data elektroniskt</span><span class="sxs-lookup"><span data-stu-id="9bea3-139">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="9bea3-140">Vanliga frågor och svar om elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="9bea3-140">Electronic Invoicing FAQ</span></span>](faq-electronic-invoicing.yml)  
[<span data-ttu-id="9bea3-141">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="9bea3-141">General Business Functionality</span></span>](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]