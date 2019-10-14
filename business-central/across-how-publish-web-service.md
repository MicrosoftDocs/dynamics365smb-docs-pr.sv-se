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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 05a414d6f12243f55105863b66d9b6e759a29189
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305702"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="787bc-103">Publicera en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="787bc-103">Publish a Web Service</span></span>

<span data-ttu-id="787bc-104">Webbtjänster är en enklare sätt att göra applikationfunktioner tillgängliga för en mängd olika externa system och användare.</span><span class="sxs-lookup"><span data-stu-id="787bc-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="787bc-105">innehåller ett antal objekt som visas som webbtjänster som standard på grund av integrationen med andra Microsoft-tjänster, men du kan också lägga till andra webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="787bc-105">includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="787bc-106">Du skapar en webbtjänst på [!INCLUDE[d365fin](includes/d365fin_md.md)]-klienten.</span><span class="sxs-lookup"><span data-stu-id="787bc-106">You set up a web service in the [!INCLUDE[d365fin](includes/d365fin_md.md)] client.</span></span> <span data-ttu-id="787bc-107">Sedan måste Du publicerar webbtjänsten för att göra den tillgänglig att serva förfrågningar över nätverket.</span><span class="sxs-lookup"><span data-stu-id="787bc-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="787bc-108">Användare kan upptäcka webbtjänster, genom att styra en webbläsare på serverplatsen och begär en lista över tillgängliga tjänster.</span><span class="sxs-lookup"><span data-stu-id="787bc-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="787bc-109">När du publicerar en webbtjänst, blir den direkt tillgänglig i nätverket för autentiserade användare.</span><span class="sxs-lookup"><span data-stu-id="787bc-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="787bc-110">Alla behöriga användare kan komma åt metadata för webbtjänster, men endast användare, som har tillräcklig behörighet kan komma åt faktiska data.</span><span class="sxs-lookup"><span data-stu-id="787bc-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="787bc-111">Skapa och publicera en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="787bc-111">Creating and Publishing a Web Service</span></span>  
<span data-ttu-id="787bc-112">Följande Moment beskriver hur du skapar och publicerar en webbtjänst.</span><span class="sxs-lookup"><span data-stu-id="787bc-112">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="787bc-113">Så här Skapa och publicera en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="787bc-113">To create and publish a web service</span></span>  

1. <span data-ttu-id="787bc-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Webbtjänster** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="787bc-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="787bc-115">Välj **Nytt** på sidan **Webbtjänster**.</span><span class="sxs-lookup"><span data-stu-id="787bc-115">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="787bc-116">**Codeunit** och **Sida** är giltiga typer för SOAP-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="787bc-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="787bc-117">**Sida** och **fråga** är giltiga typer för OData-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="787bc-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    > <span data-ttu-id="787bc-118">Om databasen innehåller flera företag, kan du välja ett objekt-ID som är unikt för ett av företagen.</span><span class="sxs-lookup"><span data-stu-id="787bc-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="787bc-119">Tjänstnamnet visas för konsumenter av din webbtjänsten och utgör basen för att identifiera och för att särskilja webbtjänster, så se till att välja ett meningsfullt namn.</span><span class="sxs-lookup"><span data-stu-id="787bc-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="787bc-120">Markera kryssrutan i kolumnen **Publicerat**.</span><span class="sxs-lookup"><span data-stu-id="787bc-120">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="787bc-121">När du publicerar webbtjänsten kan du, i fälten **OData-URL** och **SOAP-URL**, se URL som genereras för webbtjänsten.</span><span class="sxs-lookup"><span data-stu-id="787bc-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="787bc-122">Du kan testa webbtjänsten omedelbart, genom att välja länkarna i de fälten **OData-URL** och **SOAP-URL**.</span><span class="sxs-lookup"><span data-stu-id="787bc-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="787bc-123">Om du vill kan du kopiera värdet i fältet och spara det för senare användning.</span><span class="sxs-lookup"><span data-stu-id="787bc-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="787bc-124">För kodenheter som har publicerats som en SOAP-webbtjänst, måste de metoder som visas i kodenheten vara markerade med `[External]` i koden.</span><span class="sxs-lookup"><span data-stu-id="787bc-124">For codeunits that are published as a SOAP web service, the methods exposed in the codeunit must be marked as `[External]` in the code.</span></span>

<span data-ttu-id="787bc-125">När du publicerar en webbtjänst, är den tillgänglig för externa parter.</span><span class="sxs-lookup"><span data-stu-id="787bc-125">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="787bc-126">Du kan kontrollera tillgängligheten för den webbtjänsten, genom att använda en webbläsare, eller så kan du välja länken i fälten **OData-URL** och **SOAP-URL** på sidan **Webbtjänster**.</span><span class="sxs-lookup"><span data-stu-id="787bc-126">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="787bc-127">Följande tillvägagångssätt visar hur du kan kontrollera tillgängligheten av webbtjänsten för senare användning.</span><span class="sxs-lookup"><span data-stu-id="787bc-127">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="787bc-128">Om du vill kontrollera tillgängligheten av en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="787bc-128">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="787bc-129">Ange den relevanta URL.en i din webbläsare.</span><span class="sxs-lookup"><span data-stu-id="787bc-129">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="787bc-130">Följande tabell visar vilka olika typer av URL som du kan ange för olika webbtjänsttyper.</span><span class="sxs-lookup"><span data-stu-id="787bc-130">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="787bc-131">Typ</span><span class="sxs-lookup"><span data-stu-id="787bc-131">Type</span></span>|<span data-ttu-id="787bc-132">Syntax</span><span class="sxs-lookup"><span data-stu-id="787bc-132">Syntax</span></span>|<span data-ttu-id="787bc-133">Exempel</span><span class="sxs-lookup"><span data-stu-id="787bc-133">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="787bc-134">SOAP</span><span class="sxs-lookup"><span data-stu-id="787bc-134">SOAP</span></span> |<span data-ttu-id="787bc-135">https://api.businesscentral.dynamics.com/*version*/*innehavare*/WS/*CompanyName*/*enhet*/</span><span class="sxs-lookup"><span data-stu-id="787bc-135">https://api.businesscentral.dynamics.com/*version*/*tenant*/WS/*CompanyName*/*entity*/</span></span> |`https://api.businesscentral.dynamics.com/v1.0/a10b3ee6-d9a2-42fe-926f-946e23bb8ddd/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="787bc-136">OData V4</span><span class="sxs-lookup"><span data-stu-id="787bc-136">OData V4</span></span>|<span data-ttu-id="787bc-137">https://api.businesscentral.dynamics.com/*version*/*innehavare*/ODataV4/Company('*CompanyName*')/*enhet*</span><span class="sxs-lookup"><span data-stu-id="787bc-137">https://api.businesscentral.dynamics.com/*version*/*tenant*/ODataV4/Company('*CompanyName*')/*entity*</span></span>|`https://api.businesscentral.dynamics.com/v1.0/a10b3ee6-d9a2-42fe-926f-946e23bb8ddd/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="787bc-138">Företagsnamnsfältet är skiftlägeskänsligt.</span><span class="sxs-lookup"><span data-stu-id="787bc-138">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="787bc-139">Granska informationen som visas i webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="787bc-139">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="787bc-140">Kontrollera att du kan visa namnet på webbtjänsten som du har skapat.</span><span class="sxs-lookup"><span data-stu-id="787bc-140">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="787bc-141">När du öppnar en webbtjänst, och du vill skriva data tillbaka till [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du ange företagsnamn.</span><span class="sxs-lookup"><span data-stu-id="787bc-141">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="787bc-142">Du kan skriva in företaget som en del av URI som visas i exempel, eller så kan du skriva in företaget som en del av frågaparametrarna.</span><span class="sxs-lookup"><span data-stu-id="787bc-142">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="787bc-143">Till exempel pekar följande URI.er på samma OData-webbtjänst och båda är giltiga URI:er.</span><span class="sxs-lookup"><span data-stu-id="787bc-143">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="787bc-144">Se även</span><span class="sxs-lookup"><span data-stu-id="787bc-144">See Also</span></span>

[<span data-ttu-id="787bc-145">Administration</span><span class="sxs-lookup"><span data-stu-id="787bc-145">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="787bc-146">Business Central webbtjänster för utvecklare</span><span class="sxs-lookup"><span data-stu-id="787bc-146">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
