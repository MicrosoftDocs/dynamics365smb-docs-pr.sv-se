---
title: Skicka elektroniska dokument | Microsoft Docs
description: "Så här skickar du fakturor elektroniskt."
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
ms.openlocfilehash: eb9a20547c7eef346fa199eaa136211dcdd09dab
ms.contentlocale: sv-se
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-send-electronic-documents"></a><span data-ttu-id="0481d-103">Så här skickar du elektroniska dokument</span><span class="sxs-lookup"><span data-stu-id="0481d-103">How to: Send Electronic Documents</span></span>
<span data-ttu-id="0481d-104">Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] stöder utskick av elektroniska fakturor och kreditnotor i PEPPOL-format, som stöds av de största leverantörerna av dokumentväxlingstjänster</span><span class="sxs-lookup"><span data-stu-id="0481d-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="0481d-105">En leverantör av dokumentväxlingstjänster skickar dokument elektroniskt mellan handelspartners.</span><span class="sxs-lookup"><span data-stu-id="0481d-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="0481d-106">För att få stöd för andra elektroniska dokumentformat använder du ramverket för datautbyte.</span><span class="sxs-lookup"><span data-stu-id="0481d-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="0481d-107">I den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] finns en förkonfigurerad dokumentväxlingstjänst som är inställningsklar för företaget.</span><span class="sxs-lookup"><span data-stu-id="0481d-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="0481d-108">Mer information finns i [Så här konfigurerar du en dokumentväxlingstjänst](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="0481d-108">For more information, see [How to: Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="0481d-109">Om du vill skicka en försäljningsfaktura som ett elektroniskt PEPPOL-dokument väljer du alternativet **Elektroniskt dokument** i dialogrutan **Bokför och skicka**, där du även kan ställa in kundens standardprofil för dokumentutskick.</span><span class="sxs-lookup"><span data-stu-id="0481d-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="0481d-110">Först måste du skapa olika huvuddata, som företagsinformation, kunder, artiklar och enheter.</span><span class="sxs-lookup"><span data-stu-id="0481d-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="0481d-111">Dessa används för att identifiera dina affärspartners och artiklar vid konvertering av data i fält i [Så här konfigurerar du utskick och mottagning av elektroniska dokument](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="0481d-111">These are used to identify the business partners and items when converting data in fields in [How to: Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="0481d-112">Så här kan du skicka en elektronisk försäljningsfaktura</span><span class="sxs-lookup"><span data-stu-id="0481d-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="0481d-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="0481d-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="0481d-114">Skapa en ny försäljningsfaktura.</span><span class="sxs-lookup"><span data-stu-id="0481d-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="0481d-115">Välj **Bokför och skicka** på fliken **Åtgärder** i gruppen **Bokföring** när försäljningsfakturan är klar att faktureras.</span><span class="sxs-lookup"><span data-stu-id="0481d-115">When the sales invoice is ready to be invoiced, on the **Actions** tab, in the **Posting** group, choose **Post and Send**.</span></span>  

     <span data-ttu-id="0481d-116">Om kundens standardutskicksprofil är **Elektroniskt dokument** visas det i dialogrutan **Bekräftelse för bokför och utskick** och du behöver bara välja **Ja** för att bokföra och skicka fakturan elektroniskt i det valda formatet.</span><span class="sxs-lookup"><span data-stu-id="0481d-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="0481d-117">Välj knappen AssistEdit till höger om fältet **Skicka dokument till** i dialogrutan **Bekräftelse för bokför och utskick**.</span><span class="sxs-lookup"><span data-stu-id="0481d-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="0481d-118">Välj **Genom dokumentväxlingstjänst** i dialogrutan **Skicka dokument till** dialogrutan i fältet **Genom dokumentväxlingstjänst**.</span><span class="sxs-lookup"><span data-stu-id="0481d-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="0481d-119">Välj **PEPPOL** i fältet **Format**.</span><span class="sxs-lookup"><span data-stu-id="0481d-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="0481d-120">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="0481d-120">Choose the **OK** button.</span></span> <span data-ttu-id="0481d-121">Dialogrutan **Bekräftelse för bokför och utskick** visas.</span><span class="sxs-lookup"><span data-stu-id="0481d-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="0481d-122">**Elektroniskt dokument (PEPPOL)** läggs till i fältet **Skicka dokument till**.</span><span class="sxs-lookup"><span data-stu-id="0481d-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="0481d-123">Välj **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0481d-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="0481d-124">Försäljningsfakturan bokförs och skickas till kunden som ett elektroniskt dokument i PEPPOL-format.</span><span class="sxs-lookup"><span data-stu-id="0481d-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="0481d-125">Du kan även skicka en bokförd försäljningsfaktura som ett elektroniskt dokument.</span><span class="sxs-lookup"><span data-stu-id="0481d-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="0481d-126">Proceduren är samma som har beskrivits i det här avsnittet för icke-bokförda försäljningsdokument.</span><span class="sxs-lookup"><span data-stu-id="0481d-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="0481d-127">Välj **Aktivitetslogg** för att visa status för elektroniskt dokument på fliken **Åtgärder**, i gruppen **Allmänt**, i fönstret **Bokförd försäljningsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="0481d-127">In the **Posted Sales Invoice** window, on the **Actions** tab, in the **General** group, choose **Activity Log** to view the status of the electronic document.</span></span> <span data-ttu-id="0481d-128">Mer information finns i **Aktivitetslogg**</span><span class="sxs-lookup"><span data-stu-id="0481d-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0481d-129">Se även</span><span class="sxs-lookup"><span data-stu-id="0481d-129">See Also</span></span>  
[<span data-ttu-id="0481d-130">Så här fakturerar du försäljning</span><span class="sxs-lookup"><span data-stu-id="0481d-130">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="0481d-131">Så här konfigurerar du dokumentutskicksprofiler</span><span class="sxs-lookup"><span data-stu-id="0481d-131">How to: Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="0481d-132">Så här konfigurerar du utskick och mottagning av elektroniska dokument</span><span class="sxs-lookup"><span data-stu-id="0481d-132">How to: Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="0481d-133">Så här konfigurerar du en dokumentväxlingstjänst</span><span class="sxs-lookup"><span data-stu-id="0481d-133">How to: Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="0481d-134">Så här konfigurerar du datautbytesdefinitioner</span><span class="sxs-lookup"><span data-stu-id="0481d-134">How to: Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
<span data-ttu-id="0481d-135">[Utbyta data elektroniskt](across-data-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="0481d-135">[Exchanging Data Electronically](across-data-exchange.md)</span></span>  
[<span data-ttu-id="0481d-136">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="0481d-136">General Business Functionality</span></span>](ui-across-business-areas.md)  

