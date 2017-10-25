---
title: "Visa objekt som webbtjänster | Microsoft Docs"
description: "Publicera [!INCLUDE[d365fin](includes/d365fin_md.md)]-objekt som webbtjänster, de är tillgängliga direkt i nätverket."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 278515fc479a72957fb52dad71ce2f98d354ee32
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-publish-a-web-service"></a><span data-ttu-id="e0f2d-103">Så här: Publicerar du en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="e0f2d-103">How to: Publish a Web Service</span></span>
<span data-ttu-id="e0f2d-104">Webbtjänster är en enklare sätt att göra applikationfunktioner tillgängliga för en mängd olika externa system och användare.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="e0f2d-105"> innehåller ett antal objekt som visas som webbtjänster som standard på grund av integrationen med andra Microsoft-tjänster, men du kan också lägga till andra webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-105"> includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="e0f2d-106">Du kan ställa in en webbtjänst i Windows-klienten eller i webbklienten.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-106">You can set up a web service in the Windows client or in the Web client.</span></span> <span data-ttu-id="e0f2d-107">Sedan måste Du publicerar webbtjänsten för att göra den tillgänglig att serva förfrågningar över nätverket.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="e0f2d-108">Användare kan upptäcka webbtjänster, genom att styra en webbläsare på serverplatsen och begär en lista över tillgängliga tjänster.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="e0f2d-109">När du publicerar en webbtjänst, blir den direkt tillgänglig i nätverket för autentiserade användare.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="e0f2d-110">Alla behöriga användare kan komma åt metadata för webbtjänster, men endast användare, som har tillräcklig behörighet kan komma åt faktiska data.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="e0f2d-111">Skapa och publicera en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="e0f2d-111">Creating and Publishing a Web Service</span></span>  
 <span data-ttu-id="e0f2d-112">Följande Moment beskriver hur du skapar och publicerar en webbtjänst.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-112">The following steps explain how to create and publish a web service.</span></span>  

#### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="e0f2d-113">Så här Skapa och publicera en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="e0f2d-113">To create and publish a web service</span></span>  

1.  <span data-ttu-id="e0f2d-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Webbtjänster** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Web Services**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="e0f2d-115">Välj **Nytt** på **Webbtjänster** sidan.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-115">In the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  <span data-ttu-id="e0f2d-116">**Codeunit** och **Sida** är giltiga typer för SOAP-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="e0f2d-117">**Sida** och **fråga** är giltiga typer för OData-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    <span data-ttu-id="e0f2d-118">Om databasen innehåller flera företag, kan du välja ett objekt-ID som är unikt för ett av företagen.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    <span data-ttu-id="e0f2d-119">Tjänstnamnet visas för konsumenter av din webbtjänsten och utgör basen för att identifiera och för att särskilja webbtjänster, så se till att välja ett meningsfullt namn.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3.  <span data-ttu-id="e0f2d-120">Markera kryssrutan i kolumnen **Publicerat**.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-120">Select the check box in the **Published** column.</span></span>  

     <span data-ttu-id="e0f2d-121">När du publicerar webbtjänsten kan du, i fälten **OData-URL** och **SOAP-URL**, se URL som genereras för webbtjänsten.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="e0f2d-122">Du kan testa webbtjänsten omedelbart, genom att välja länkarna i de fälten **OData-URL** och **SOAP-URL**.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="e0f2d-123">Om du vill kan du kopiera värdet i fältet och spara det för senare användning.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

<span data-ttu-id="e0f2d-124">När du publicerar en webbtjänst, är den tillgänglig för externa parter.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-124">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="e0f2d-125">Du kan kontrollera tillgängligheten för den webbtjänsten, genom att använda en webbläsare, eller så kan du välja länken i fälten **OData-URL** och **SOAP-URL** i fönstret **Webbtjänster**.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-125">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields in the **Web Services** window.</span></span> <span data-ttu-id="e0f2d-126">Följande tillvägagångssätt visar hur du kan kontrollera tillgängligheten av webbtjänsten för senare användning.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-126">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

#### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="e0f2d-127">Om du vill kontrollera tillgängligheten av en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="e0f2d-127">To verify the availability of a web service</span></span>  

1.  <span data-ttu-id="e0f2d-128">Ange den relevanta URL.en i din webbläsare.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-128">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="e0f2d-129">Följande tabell visar de olika typerna av URL:er som du kan ange.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-129">The following table illustrates the types of URLs that you can enter.</span></span> <span data-ttu-id="e0f2d-130">Använd följande format på din URI för SOAP-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-130">For SOAP web services, use the following format for your URI.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="e0f2d-131">Webbtjänsttyp</span><span class="sxs-lookup"><span data-stu-id="e0f2d-131">Web service type</span></span></th>
    <th><span data-ttu-id="e0f2d-132">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0f2d-132">Syntax</span></span></th>
    <th><span data-ttu-id="e0f2d-133">Exempel</span><span class="sxs-lookup"><span data-stu-id="e0f2d-133">Example</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="e0f2d-134">SOAP</span><span class="sxs-lookup"><span data-stu-id="e0f2d-134">SOAP</span></span></td>
    <td><span data-ttu-id="e0f2d-135">https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</span><span class="sxs-lookup"><span data-stu-id="e0f2d-135">https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</span></span></td>
    <td><span data-ttu-id="e0f2d-136">https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="e0f2d-136">https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="e0f2d-137">OData</span><span class="sxs-lookup"><span data-stu-id="e0f2d-137">OData</span></span></td>
    <td><span data-ttu-id="e0f2d-138">https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</span><span class="sxs-lookup"><span data-stu-id="e0f2d-138">https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</span></span></td>
    <td><span data-ttu-id="e0f2d-139">https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="e0f2d-139">https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com</span></span>

         The company name is case-sensitive.</td>
    </tr>
    </table>

2.  <span data-ttu-id="e0f2d-140">Granska informationen som visas i webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-140">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="e0f2d-141">Kontrollera att du kan visa namnet på webbtjänsten som du har skapat.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-141">Verify that you can see the name of the web service that you have created.</span></span>  

 <span data-ttu-id="e0f2d-142">När du öppnar en webbtjänst, och du vill skriva data tillbaka till [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du ange företagsnamn.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-142">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="e0f2d-143">Du kan skriva in företaget som en del av URI som visas i exempel, eller så kan du skriva in företaget som en del av frågaparametrarna.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-143">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="e0f2d-144">Till exempel pekar följande URI.er på samma OData-webbtjänst och båda är giltiga URI:er.</span><span class="sxs-lookup"><span data-stu-id="e0f2d-144">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a><span data-ttu-id="e0f2d-145">Se även</span><span class="sxs-lookup"><span data-stu-id="e0f2d-145">See Also</span></span>  
[<span data-ttu-id="e0f2d-146">Installation och administration i Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="e0f2d-146">Setup and Administration in Dynamics 365 for Financials</span></span>](admin-setup-and-administration.md)  

