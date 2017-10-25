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
# <a name="how-to-publish-a-web-service"></a>Så här: Publicerar du en webbtjänst
Webbtjänster är en enklare sätt att göra applikationfunktioner tillgängliga för en mängd olika externa system och användare. [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett antal objekt som visas som webbtjänster som standard på grund av integrationen med andra Microsoft-tjänster, men du kan också lägga till andra webbtjänster.  

Du kan ställa in en webbtjänst i Windows-klienten eller i webbklienten. Sedan måste Du publicerar webbtjänsten för att göra den tillgänglig att serva förfrågningar över nätverket. Användare kan upptäcka webbtjänster, genom att styra en webbläsare på serverplatsen och begär en lista över tillgängliga tjänster. När du publicerar en webbtjänst, blir den direkt tillgänglig i nätverket för autentiserade användare. Alla behöriga användare kan komma åt metadata för webbtjänster, men endast användare, som har tillräcklig behörighet kan komma åt faktiska data.

## <a name="creating-and-publishing-a-web-service"></a>Skapa och publicera en webbtjänst  
 Följande Moment beskriver hur du skapar och publicerar en webbtjänst.  

#### <a name="to-create-and-publish-a-web-service"></a>Så här Skapa och publicera en webbtjänst  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Webbtjänster** och välj sedan relaterad länk.  

2.  Välj **Nytt** på **Webbtjänster** sidan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  **Codeunit** och **Sida** är giltiga typer för SOAP-webbtjänster. **Sida** och **fråga** är giltiga typer för OData-webbtjänster.  
    Om databasen innehåller flera företag, kan du välja ett objekt-ID som är unikt för ett av företagen.  
    Tjänstnamnet visas för konsumenter av din webbtjänsten och utgör basen för att identifiera och för att särskilja webbtjänster, så se till att välja ett meningsfullt namn.

3.  Markera kryssrutan i kolumnen **Publicerat**.  

     När du publicerar webbtjänsten kan du, i fälten **OData-URL** och **SOAP-URL**, se URL som genereras för webbtjänsten. Du kan testa webbtjänsten omedelbart, genom att välja länkarna i de fälten **OData-URL** och **SOAP-URL**. Om du vill kan du kopiera värdet i fältet och spara det för senare användning.  

När du publicerar en webbtjänst, är den tillgänglig för externa parter. Du kan kontrollera tillgängligheten för den webbtjänsten, genom att använda en webbläsare, eller så kan du välja länken i fälten **OData-URL** och **SOAP-URL** i fönstret **Webbtjänster**. Följande tillvägagångssätt visar hur du kan kontrollera tillgängligheten av webbtjänsten för senare användning.  

#### <a name="to-verify-the-availability-of-a-web-service"></a>Om du vill kontrollera tillgängligheten av en webbtjänst  

1.  Ange den relevanta URL.en i din webbläsare. Följande tabell visar de olika typerna av URL:er som du kan ange. Använd följande format på din URI för SOAP-webbtjänster.  

    <table>
    <tr>
    <th>Webbtjänsttyp</th>
    <th>Syntax</th>
    <th>Exempel</th>
    </tr>
    <tr>
    <td>SOAP</td>
    <td>https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</td>
    <td>https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com</td>
    </tr>
    <tr>
    <td>OData</td>
    <td>https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</td>
    <td>https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com

         The company name is case-sensitive.</td>
    </tr>
    </table>

2.  Granska informationen som visas i webbläsaren. Kontrollera att du kan visa namnet på webbtjänsten som du har skapat.  

 När du öppnar en webbtjänst, och du vill skriva data tillbaka till [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du ange företagsnamn. Du kan skriva in företaget som en del av URI som visas i exempel, eller så kan du skriva in företaget som en del av frågaparametrarna. Till exempel pekar följande URI.er på samma OData-webbtjänst och båda är giltiga URI:er.  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a>Se även  
[Installation och administration i Dynamics 365 for Financials](admin-setup-and-administration.md)  

