---
title: Visa objekt som webbtjänster | Microsoft Docs
description: Publicera objekt som webbtjänster för att göra dem omedelbart tillgängliga för din Business Central-lösning.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/04/2020
ms.author: edupont
ms.openlocfilehash: 4e09df754895a8d0d3a1cc1ed84a7c8332e32880
ms.sourcegitcommit: 0cb8a646dcba8f6d6336ebd008587874d25f4629
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030250"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="b1281-103">Publicera en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="b1281-103">Publish a Web Service</span></span>

<span data-ttu-id="b1281-104">Webbtjänster är en enklare sätt att göra applikationfunktioner tillgängliga för en mängd olika externa system och användare.</span><span class="sxs-lookup"><span data-stu-id="b1281-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="b1281-105">innehåller ett antal objekt som visas som webbtjänster som standard på grund av integrationen med andra Microsoft-tjänster, men du kan också lägga till andra webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="b1281-105">includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="b1281-106">Du skapar en webbtjänst på [!INCLUDE[d365fin](includes/d365fin_md.md)]-klienten.</span><span class="sxs-lookup"><span data-stu-id="b1281-106">You set up a web service in the [!INCLUDE[d365fin](includes/d365fin_md.md)] client.</span></span> <span data-ttu-id="b1281-107">Sedan måste Du publicerar webbtjänsten för att göra den tillgänglig att serva förfrågningar över nätverket.</span><span class="sxs-lookup"><span data-stu-id="b1281-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="b1281-108">Användare kan upptäcka webbtjänster, genom att styra en webbläsare på serverplatsen och begär en lista över tillgängliga tjänster.</span><span class="sxs-lookup"><span data-stu-id="b1281-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="b1281-109">När du publicerar en webbtjänst, blir den direkt tillgänglig i nätverket för autentiserade användare.</span><span class="sxs-lookup"><span data-stu-id="b1281-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="b1281-110">Alla behöriga användare kan komma åt metadata för webbtjänster, men endast användare, som har tillräcklig behörighet kan komma åt faktiska data.</span><span class="sxs-lookup"><span data-stu-id="b1281-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="b1281-111">Skapa och publicera en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="b1281-111">Creating and Publishing a Web Service</span></span>  
<span data-ttu-id="b1281-112">Följande Moment beskriver hur du skapar och publicerar en webbtjänst.</span><span class="sxs-lookup"><span data-stu-id="b1281-112">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="b1281-113">Så här Skapa och publicera en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="b1281-113">To create and publish a web service</span></span>  

1. <span data-ttu-id="b1281-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Webbtjänster** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b1281-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b1281-115">Välj **Nytt** på sidan **Webbtjänster**.</span><span class="sxs-lookup"><span data-stu-id="b1281-115">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="b1281-116">**Codeunit** och **Sida** är giltiga typer för SOAP-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="b1281-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="b1281-117">**Sida** och **fråga** är giltiga typer för OData-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="b1281-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    > <span data-ttu-id="b1281-118">Om databasen innehåller flera företag, kan du välja ett objekt-ID som är unikt för ett av företagen.</span><span class="sxs-lookup"><span data-stu-id="b1281-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="b1281-119">Tjänstnamnet visas för konsumenter av din webbtjänsten och utgör basen för att identifiera och för att särskilja webbtjänster, så se till att välja ett meningsfullt namn.</span><span class="sxs-lookup"><span data-stu-id="b1281-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="b1281-120">Markera kryssrutan i kolumnen **Publicerat**.</span><span class="sxs-lookup"><span data-stu-id="b1281-120">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="b1281-121">När du publicerar webbtjänsten kan du, i fälten **OData-URL** och **SOAP-URL**, se URL som genereras för webbtjänsten.</span><span class="sxs-lookup"><span data-stu-id="b1281-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="b1281-122">Du kan testa webbtjänsten omedelbart, genom att välja länkarna i de fälten **OData-URL** och **SOAP-URL**.</span><span class="sxs-lookup"><span data-stu-id="b1281-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="b1281-123">Om du vill kan du kopiera värdet i fältet och spara det för senare användning.</span><span class="sxs-lookup"><span data-stu-id="b1281-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b1281-124">För kodenheter som har publicerats som en SOAP-webbtjänst, måste de metoder som visas i kodenheten vara markerade med `[External]` i koden.</span><span class="sxs-lookup"><span data-stu-id="b1281-124">For codeunits that are published as a SOAP web service, the methods exposed in the codeunit must be marked as `[External]` in the code.</span></span>

<span data-ttu-id="b1281-125">När du publicerar en webbtjänst, är den tillgänglig för externa parter.</span><span class="sxs-lookup"><span data-stu-id="b1281-125">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="b1281-126">Du kan kontrollera tillgängligheten för den webbtjänsten, genom att använda en webbläsare, eller så kan du välja länken i fälten **OData-URL** och **SOAP-URL** på sidan **Webbtjänster**.</span><span class="sxs-lookup"><span data-stu-id="b1281-126">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="b1281-127">Följande tillvägagångssätt visar hur du kan kontrollera tillgängligheten av webbtjänsten för senare användning.</span><span class="sxs-lookup"><span data-stu-id="b1281-127">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="b1281-128">Om du vill kontrollera tillgängligheten av en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="b1281-128">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="b1281-129">Ange den relevanta URL.en i din webbläsare.</span><span class="sxs-lookup"><span data-stu-id="b1281-129">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="b1281-130">Följande tabell visar vilka olika typer av URL som du kan ange för olika webbtjänsttyper.</span><span class="sxs-lookup"><span data-stu-id="b1281-130">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="b1281-131">Typ</span><span class="sxs-lookup"><span data-stu-id="b1281-131">Type</span></span>|<span data-ttu-id="b1281-132">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1281-132">Syntax</span></span>|<span data-ttu-id="b1281-133">Exempel</span><span class="sxs-lookup"><span data-stu-id="b1281-133">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="b1281-134">SOAP</span><span class="sxs-lookup"><span data-stu-id="b1281-134">SOAP</span></span>|<span data-ttu-id="b1281-135">https://api.businesscentral.dynamics.com/*version*/*klientorganisation*/Produktion/WS/*CompanyName*/*entitet*/</span><span class="sxs-lookup"><span data-stu-id="b1281-135">https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/</span></span> |https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument|
    > |<span data-ttu-id="b1281-136">OData V4</span><span class="sxs-lookup"><span data-stu-id="b1281-136">OData V4</span></span>|<span data-ttu-id="b1281-137">https://api.businesscentral.dynamics.com/*version*/*klientorganisation*/Produktion/ODataV4/företag('*CompanyName*')/*entitet*</span><span class="sxs-lookup"><span data-stu-id="b1281-137">https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*</span></span>|<span data-ttu-id="b1281-138">https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument</span><span class="sxs-lookup"><span data-stu-id="b1281-138">https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument</span></span><br/>    <span data-ttu-id="b1281-139">Företagsnamnsfältet är skiftlägeskänsligt.</span><span class="sxs-lookup"><span data-stu-id="b1281-139">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="b1281-140">Granska informationen som visas i webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="b1281-140">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="b1281-141">Kontrollera att du kan visa namnet på webbtjänsten som du har skapat.</span><span class="sxs-lookup"><span data-stu-id="b1281-141">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="b1281-142">När du öppnar en webbtjänst, och du vill skriva data tillbaka till [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du ange företagsnamn.</span><span class="sxs-lookup"><span data-stu-id="b1281-142">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="b1281-143">Du kan skriva in företaget som en del av URI som visas i exempel, eller så kan du skriva in företaget som en del av frågaparametrarna.</span><span class="sxs-lookup"><span data-stu-id="b1281-143">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="b1281-144">Till exempel pekar följande URI.er på samma OData-webbtjänst och båda är giltiga URI:er.</span><span class="sxs-lookup"><span data-stu-id="b1281-144">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="b1281-145">Se även</span><span class="sxs-lookup"><span data-stu-id="b1281-145">See Also</span></span>

[<span data-ttu-id="b1281-146">Administration</span><span class="sxs-lookup"><span data-stu-id="b1281-146">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="b1281-147">Business Central webbtjänster för utvecklare</span><span class="sxs-lookup"><span data-stu-id="b1281-147">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
