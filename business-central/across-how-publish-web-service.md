---
title: "Visa objekt som webbtjänster | Microsoft Docs"
description: "Publicera objekt som webbtjänster i syfte att göra dem omedelbart tillgängliga i nätverket."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: d22de15b3e91897a209a31d03a63fb7d927d2f96
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="publish-a-web-service"></a>Publicera en webbtjänst
Webbtjänster är en enklare sätt att göra applikationfunktioner tillgängliga för en mängd olika externa system och användare. [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett antal objekt som visas som webbtjänster som standard på grund av integrationen med andra Microsoft-tjänster, men du kan också lägga till andra webbtjänster.  

Du kan ställa in en webbtjänst i Windows-klienten eller i webbklienten. Sedan måste Du publicerar webbtjänsten för att göra den tillgänglig att serva förfrågningar över nätverket. Användare kan upptäcka webbtjänster, genom att styra en webbläsare på serverplatsen och begär en lista över tillgängliga tjänster. När du publicerar en webbtjänst, blir den direkt tillgänglig i nätverket för autentiserade användare. Alla behöriga användare kan komma åt metadata för webbtjänster, men endast användare, som har tillräcklig behörighet kan komma åt faktiska data.

## <a name="creating-and-publishing-a-web-service"></a>Skapa och publicera en webbtjänst  
Följande Moment beskriver hur du skapar och publicerar en webbtjänst.  

### <a name="to-create-and-publish-a-web-service"></a>Så här Skapa och publicera en webbtjänst  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Webbtjänster** och välj sedan relaterad länk.  
2.  Välj **Nytt** på **Webbtjänster** sidan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  **Codeunit** och **Sida** är giltiga typer för SOAP-webbtjänster. **Sida** och **fråga** är giltiga typer för OData-webbtjänster.  
    Om databasen innehåller flera företag, kan du välja ett objekt-ID som är unikt för ett av företagen.  
    Tjänstnamnet visas för konsumenter av din webbtjänsten och utgör basen för att identifiera och för att särskilja webbtjänster, så se till att välja ett meningsfullt namn.

3.  Markera kryssrutan i kolumnen **Publicerat**.  

När du publicerar webbtjänsten kan du, i fälten **OData-URL** och **SOAP-URL**, se URL som genereras för webbtjänsten. Du kan testa webbtjänsten omedelbart, genom att välja länkarna i de fälten **OData-URL** och **SOAP-URL**. Om du vill kan du kopiera värdet i fältet och spara det för senare användning.  

När du publicerar en webbtjänst, är den tillgänglig för externa parter. Du kan kontrollera tillgängligheten för den webbtjänsten, genom att använda en webbläsare, eller så kan du välja länken i fälten **OData-URL** och **SOAP-URL** i fönstret **Webbtjänster**. Följande tillvägagångssätt visar hur du kan kontrollera tillgängligheten av webbtjänsten för senare användning.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Om du vill kontrollera tillgängligheten av en webbtjänst  

1.  Ange den relevanta URL.en i din webbläsare. Följande tabell visar vilka olika typer av URL som du kan ange för olika webbtjänsttyper.  
> [!div class="mx-tdBreakAll"]
> |Kontakttyp|Syntax|Exempel|
> |----------------|------|-------|
> |SOAP |https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/ |https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com |
> |OData |https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')|[https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MinFirma')/salesDocuments?tenant=MyCompany.financials.dynamics.com](https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com) <br />    Företagsnamnsfältet är skiftlägeskänsligt.|

2.  Granska informationen som visas i webbläsaren. Kontrollera att du kan visa namnet på webbtjänsten som du har skapat.  

När du öppnar en webbtjänst, och du vill skriva data tillbaka till [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du ange företagsnamn. Du kan skriva in företaget som en del av URI som visas i exempel, eller så kan du skriva in företaget som en del av frågaparametrarna. Till exempel pekar följande URI.er på samma OData-webbtjänst och båda är giltiga URI:er.  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a>Se även  
[Administration](admin-setup-and-administration.md)  

