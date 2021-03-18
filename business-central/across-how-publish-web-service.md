---
title: Visa objekt som webbtjänster
description: Publicera objekt som webbtjänster för att göra dem omedelbart tillgängliga för din Business Central-lösning.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/08/2020
ms.author: edupont
ms.openlocfilehash: 94a4752abc133e59169209b94a145d2195ce783d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384630"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="c516a-103">Publicera en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="c516a-103">Publish a Web Service</span></span>

<span data-ttu-id="c516a-104">Webbtjänster är ett enklare sätt att göra applikationfunktioner tillgängliga för olika typer av externa system och användare.</span><span class="sxs-lookup"><span data-stu-id="c516a-104">Web services are a lightweight way to make application functionality available to different kinds of external systems and users.</span></span> <span data-ttu-id="c516a-105">Som standard exponerar [!INCLUDE[prod_short](includes/prod_short.md)] flera objekt som webbtjänster för bättre integration med andra Microsoft-tjänster.</span><span class="sxs-lookup"><span data-stu-id="c516a-105">By default, [!INCLUDE[prod_short](includes/prod_short.md)] exposes a number of objects as web services for better integration with other Microsoft services.</span></span> <span data-ttu-id="c516a-106">Du kan lägga till andra webbtjänster när ditt företag behöver det.</span><span class="sxs-lookup"><span data-stu-id="c516a-106">You can add other web services as your business requires.</span></span>  

<span data-ttu-id="c516a-107">Skapa en webbtjänst i [!INCLUDE[prod_short](includes/prod_short.md)] och publicera sedan webbtjänsten så att den är tillgänglig för autentiserade användare.</span><span class="sxs-lookup"><span data-stu-id="c516a-107">Set up a web service in [!INCLUDE[prod_short](includes/prod_short.md)], and then publish the web service so that it is available to authenticated users.</span></span> <span data-ttu-id="c516a-108">Alla behöriga användare kan komma åt metadata för webbtjänster, men endast användare, som har tillräcklig behörighet kan komma åt faktiska data.</span><span class="sxs-lookup"><span data-stu-id="c516a-108">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>  

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="c516a-109">Skapa och publicera en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="c516a-109">Creating and Publishing a Web Service</span></span>

<span data-ttu-id="c516a-110">Följande Moment beskriver hur du skapar och publicerar en webbtjänst.</span><span class="sxs-lookup"><span data-stu-id="c516a-110">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="c516a-111">Så här Skapa och publicera en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="c516a-111">To create and publish a web service</span></span>  

1. <span data-ttu-id="c516a-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Webbtjänster** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c516a-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c516a-113">Välj **Nytt** på sidan **Webbtjänster**.</span><span class="sxs-lookup"><span data-stu-id="c516a-113">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="c516a-114">**Codeunit** och **Sida** är giltiga typer för SOAP-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="c516a-114">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="c516a-115">**Sida** och **fråga** är giltiga typer för OData-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="c516a-115">**Page** and **Query** are valid types for OData web services.</span></span> <span data-ttu-id="c516a-116">Från och med version 16.3 är också **codeunit** en giltig typ för OData v4-webbtjänster, men då visas ingen URL i användargränssnittet.</span><span class="sxs-lookup"><span data-stu-id="c516a-116">Starting with version 16.3, **Codeunit** is also a valid type for OData v4 web services, but then no URL is shown in the user interface.</span></span> <span data-ttu-id="c516a-117">Om databasen innehåller flera företag, kan du välja ett objekt-ID som är unikt för ett av företagen.</span><span class="sxs-lookup"><span data-stu-id="c516a-117">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="c516a-118">Tjänstnamnet visas för konsumenter av din webbtjänsten och utgör basen för att identifiera och för att särskilja webbtjänster, så se till att välja ett meningsfullt namn.</span><span class="sxs-lookup"><span data-stu-id="c516a-118">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="c516a-119">Markera kryssrutan i kolumnen **Publicerat**.</span><span class="sxs-lookup"><span data-stu-id="c516a-119">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="c516a-120">När du publicerar webbtjänsten visar fälten **OData-URL** och **SOAP-URL** nya URL:er.</span><span class="sxs-lookup"><span data-stu-id="c516a-120">When you publish the web service, the **OData URL** and **SOAP URL** fields show the new URLs.</span></span> <span data-ttu-id="c516a-121">För kodmoduler som är exponerade som icke-bundna åtgärder för OData v4 visas dock inte URL-fälten.</span><span class="sxs-lookup"><span data-stu-id="c516a-121">However, for codeunits that are exposed as OData v4 unbound actions, the URL fields are not shown.</span></span>  

<span data-ttu-id="c516a-122">Du kan testa webbtjänsten omedelbart, genom att välja länkarna i de fälten **OData-URL** och **SOAP-URL**.</span><span class="sxs-lookup"><span data-stu-id="c516a-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="c516a-123">Om du vill kan du kopiera värdet i fältet och spara det för senare användning.</span><span class="sxs-lookup"><span data-stu-id="c516a-123">Optionally, copy the value of the field and save it for later use.</span></span> <span data-ttu-id="c516a-124">Om du vill testa kodmoduler som visas som obundna åtgärder för OData v4 följer du instruktionerna i avsnittet [Verifiera webbtjänsttillgänglighet](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) i utvecklarinnehållet.</span><span class="sxs-lookup"><span data-stu-id="c516a-124">To test codeunits that are exposed as OData v4 unbound actions, follow the instructions in the [Verifying web service availability](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) section in the developer content.</span></span>

> [!NOTE]
> <span data-ttu-id="c516a-125">Om de objekt som du visar som webbtjänster inte får vara åtkomliga från [!INCLUDE[prod_short](includes/prod_short.md)] online, måste du markera de metoder som visas i koden som `[Scope('OnPrem')]`.</span><span class="sxs-lookup"><span data-stu-id="c516a-125">If the objects that you expose as web services must not be accessible from [!INCLUDE[prod_short](includes/prod_short.md)] online, you must mark the methods exposed in the code as `[Scope('OnPrem')]`.</span></span> <span data-ttu-id="c516a-126">Mer information finns i [attributet Omfattning](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span><span class="sxs-lookup"><span data-stu-id="c516a-126">For more information, see [Scope Attribute](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span></span>

<span data-ttu-id="c516a-127">När du publicerar en webbtjänst, är den tillgänglig för externa parter.</span><span class="sxs-lookup"><span data-stu-id="c516a-127">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="c516a-128">Du kan kontrollera tillgängligheten för den webbtjänsten genom att använda en webbläsare, eller välja länken i fälten **OData-URL** och **SOAP-URL** på sidan **Webbtjänster**.</span><span class="sxs-lookup"><span data-stu-id="c516a-128">You can verify the availability of that web service by using a browser, or choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="c516a-129">Följande tillvägagångssätt visar hur du kan kontrollera tillgängligheten av webbtjänsten för senare användning.</span><span class="sxs-lookup"><span data-stu-id="c516a-129">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="c516a-130">Om du vill kontrollera tillgängligheten av en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="c516a-130">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="c516a-131">Ange den relevanta URL.en i din webbläsare.</span><span class="sxs-lookup"><span data-stu-id="c516a-131">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="c516a-132">Följande tabell visar vilka olika typer av URL som du kan ange för olika webbtjänsttyper.</span><span class="sxs-lookup"><span data-stu-id="c516a-132">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="c516a-133">Typ</span><span class="sxs-lookup"><span data-stu-id="c516a-133">Type</span></span>|<span data-ttu-id="c516a-134">Syntax</span><span class="sxs-lookup"><span data-stu-id="c516a-134">Syntax</span></span>|<span data-ttu-id="c516a-135">Exempel</span><span class="sxs-lookup"><span data-stu-id="c516a-135">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="c516a-136">SOAP</span><span class="sxs-lookup"><span data-stu-id="c516a-136">SOAP</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="c516a-137">OData V4</span><span class="sxs-lookup"><span data-stu-id="c516a-137">OData V4</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="c516a-138">Företagsnamnsfältet är skiftlägeskänsligt.</span><span class="sxs-lookup"><span data-stu-id="c516a-138">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="c516a-139">Granska informationen som visas i webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="c516a-139">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="c516a-140">Kontrollera att du kan visa namnet på webbtjänsten som du har skapat.</span><span class="sxs-lookup"><span data-stu-id="c516a-140">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="c516a-141">När du öppnar en webbtjänst, och du vill skriva data tillbaka till [!INCLUDE[prod_short](includes/prod_short.md)], måste du ange företagsnamn.</span><span class="sxs-lookup"><span data-stu-id="c516a-141">When you access a web service, and you want to write data back to [!INCLUDE[prod_short](includes/prod_short.md)], you must specify the company name.</span></span> <span data-ttu-id="c516a-142">Du kan skriva in företaget som en del av den URI som visas i exemplen, eller så kan du skriva in företaget som en del av frågeparametrarna.</span><span class="sxs-lookup"><span data-stu-id="c516a-142">You can specify the company as part of the URI as shown in the examples; alternatively, specify the company as part of the query parameters.</span></span> <span data-ttu-id="c516a-143">Till exempel pekar följande URI.er på samma OData-webbtjänst och båda är giltiga URI:er.</span><span class="sxs-lookup"><span data-stu-id="c516a-143">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="c516a-144">Se även</span><span class="sxs-lookup"><span data-stu-id="c516a-144">See Also</span></span>

[<span data-ttu-id="c516a-145">Administration</span><span class="sxs-lookup"><span data-stu-id="c516a-145">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="c516a-146">Business Central webbtjänster för utvecklare</span><span class="sxs-lookup"><span data-stu-id="c516a-146">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[<span data-ttu-id="c516a-147">Begärandegräns för OData</span><span class="sxs-lookup"><span data-stu-id="c516a-147">OData request limits</span></span>](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  


[!INCLUDE[footer-include](includes/footer-banner.md)]