---
title: Så här konfigurerar du en dokumentväxlingstjänst | Microsoft Docs
description: Du kan använda en tjänstleverantör för att utbyta elektroniska dokument med dina handelspartner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0217f077c9c38603b9e3ff945fd47394c5b943bb
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384380"
---
# <a name="set-up-a-document-exchange-service"></a><span data-ttu-id="8f08b-103">Konfigurera en tjänst för dokumentutbyte</span><span class="sxs-lookup"><span data-stu-id="8f08b-103">Set Up a Document Exchange Service</span></span>
<span data-ttu-id="8f08b-104">Du kan använda en tjänstleverantör för att utbyta elektroniska dokument med dina handelspartner.</span><span class="sxs-lookup"><span data-stu-id="8f08b-104">You use an external service provider to exchange electronic documents with your trading partners.</span></span> <span data-ttu-id="8f08b-105">Mer information finns i [Utbyta data elektroniskt](across-data-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="8f08b-105">For more information, see [Exchanging Data Electronically](across-data-exchange.md).</span></span>  

## <a name="to-set-up-a-document-exchange-service"></a><span data-ttu-id="8f08b-106">Konfigurera en dokumentväxlingstjänst</span><span class="sxs-lookup"><span data-stu-id="8f08b-106">To set up a document exchange service</span></span>  
1. <span data-ttu-id="8f08b-107">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för dokumentöverföring** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="8f08b-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Doc. Exch. Service Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f08b-108">Fyll i fälten enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="8f08b-108">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="8f08b-109">Fält</span><span class="sxs-lookup"><span data-stu-id="8f08b-109">Field</span></span>|<span data-ttu-id="8f08b-110">Description</span><span class="sxs-lookup"><span data-stu-id="8f08b-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="8f08b-111">**Användare**</span><span class="sxs-lookup"><span data-stu-id="8f08b-111">**User Agent**</span></span>|<span data-ttu-id="8f08b-112">Ange valfri text som kan användas för att identifiera ditt företag i dokumentväxlingsprocesser.</span><span class="sxs-lookup"><span data-stu-id="8f08b-112">Enter any text that can be used to identify your company in document exchange processes.</span></span>|  
    |<span data-ttu-id="8f08b-113">**Klientorganisations-ID för dok.väx.**</span><span class="sxs-lookup"><span data-stu-id="8f08b-113">**Doc. Exch. Tenant ID**</span></span>|<span data-ttu-id="8f08b-114">Ange den klientorganisation i dokumentväxlingstjänsten som representerar ditt företag.</span><span class="sxs-lookup"><span data-stu-id="8f08b-114">Enter the tenant in the document exchange service that represents your company.</span></span> <span data-ttu-id="8f08b-115">Den tillhandahålls av leverantören av dokumentväxlingstjänsten.</span><span class="sxs-lookup"><span data-stu-id="8f08b-115">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="8f08b-116">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="8f08b-116">**Enabled**</span></span>|<span data-ttu-id="8f08b-117">Ange om tjänsten är aktiverad.</span><span class="sxs-lookup"><span data-stu-id="8f08b-117">Specify if the service is enabled.</span></span> <span data-ttu-id="8f08b-118">**Obs!** Så fort du aktiverar tjänsten skapas minst två jobbköposter för att bearbeta trafiken med elektroniska dokument in i och ut ur [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8f08b-118">**Note:**  As soon as you enable the service, at least two job queue entries are created to process the traffic of electronic documents in and out of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="8f08b-119">När du inaktiverar servicen tas jobbköposterna bort.</span><span class="sxs-lookup"><span data-stu-id="8f08b-119">When you disable the service, the job queue entries are deleted.</span></span>|  
    |<span data-ttu-id="8f08b-120">**Registrerings-URL**</span><span class="sxs-lookup"><span data-stu-id="8f08b-120">**Signup URL**</span></span>|<span data-ttu-id="8f08b-121">Ange webbsidan där du registrerade dig för dokumentväxlingstjänsten.</span><span class="sxs-lookup"><span data-stu-id="8f08b-121">Specify the web page where you sign up for the document exchange service.</span></span>|  
    |<span data-ttu-id="8f08b-122">**Servicesida**</span><span class="sxs-lookup"><span data-stu-id="8f08b-122">**Service URL**</span></span>|<span data-ttu-id="8f08b-123">Ange adressen till dokumentväxlingstjänsten som ska anropas när du skickar och tar emot elektroniska dokument.</span><span class="sxs-lookup"><span data-stu-id="8f08b-123">Specify the address of the document exchange service, which will be called when you send and receive electronic documents.</span></span>|  
    |<span data-ttu-id="8f08b-124">**InloggningsURL**</span><span class="sxs-lookup"><span data-stu-id="8f08b-124">**Login URL**</span></span>|<span data-ttu-id="8f08b-125">Ange inloggningssidan för dokumentväxlingstjänsten, det vill säga där du anger företagets användarnamn och lösenord för att logga in till tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8f08b-125">Specify the logon page for the document exchange service, which is where you enter your company’s user name and password to log on to the service.</span></span>|  
    |<span data-ttu-id="8f08b-126">**Användarnyckel**</span><span class="sxs-lookup"><span data-stu-id="8f08b-126">**Consumer Key**</span></span>|<span data-ttu-id="8f08b-127">Ange den 3-ledade OAuth-nyckeln för konsumentnyckeln.</span><span class="sxs-lookup"><span data-stu-id="8f08b-127">Enter the 3-legged OAuth key for the consumer key.</span></span> <span data-ttu-id="8f08b-128">Den tillhandahålls av leverantören av dokumentväxlingstjänsten.</span><span class="sxs-lookup"><span data-stu-id="8f08b-128">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="8f08b-129">**Konsumenthemlighet**</span><span class="sxs-lookup"><span data-stu-id="8f08b-129">**Consumer Secret**</span></span>|<span data-ttu-id="8f08b-130">Ange hemligheten som skyddar konsumentnyckeln.</span><span class="sxs-lookup"><span data-stu-id="8f08b-130">Enter the secret that protects the consumer key.</span></span> <span data-ttu-id="8f08b-131">Den tillhandahålls av leverantören av dokumentväxlingstjänsten.</span><span class="sxs-lookup"><span data-stu-id="8f08b-131">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="8f08b-132">**Token**</span><span class="sxs-lookup"><span data-stu-id="8f08b-132">**Token**</span></span>|<span data-ttu-id="8f08b-133">Ange den 3-ledade OAuth-nyckeln för token.</span><span class="sxs-lookup"><span data-stu-id="8f08b-133">Enter the 3-legged OAuth key for the token.</span></span> <span data-ttu-id="8f08b-134">Den tillhandahålls av leverantören av dokumentväxlingstjänsten.</span><span class="sxs-lookup"><span data-stu-id="8f08b-134">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="8f08b-135">**Tokenhemlighet**</span><span class="sxs-lookup"><span data-stu-id="8f08b-135">**Token Secret**</span></span>|<span data-ttu-id="8f08b-136">Ange hemligheten som skyddar token.</span><span class="sxs-lookup"><span data-stu-id="8f08b-136">Enter the secret that protects the token.</span></span> <span data-ttu-id="8f08b-137">Den tillhandahålls av leverantören av dokumentväxlingstjänsten.</span><span class="sxs-lookup"><span data-stu-id="8f08b-137">This is provided by the document exchange service provider.</span></span>|  

    > [!NOTE]  
    > <span data-ttu-id="8f08b-138">Dina inloggningsdata krypteras automatiskt.</span><span class="sxs-lookup"><span data-stu-id="8f08b-138">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f08b-139">Se även</span><span class="sxs-lookup"><span data-stu-id="8f08b-139">See Also</span></span>  
[<span data-ttu-id="8f08b-140">Konfigurera datautbyte</span><span class="sxs-lookup"><span data-stu-id="8f08b-140">Setting Up Data Exchange</span></span>](across-set-up-data-exchange.md)  
[<span data-ttu-id="8f08b-141">Utbyta data elektroniskt</span><span class="sxs-lookup"><span data-stu-id="8f08b-141">Exchanging Data Electronically</span></span>](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]