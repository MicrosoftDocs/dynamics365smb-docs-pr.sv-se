---
title: Visa objekt som webbtjänster
description: Publicera objekt som webbtjänster för att göra dem omedelbart tillgängliga för din Business Central-lösning.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bca44382de10299ecbea73eda26ba858fbd2ef32
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437633"
---
# <a name="publish-a-web-service"></a>Publicera en webbtjänst

Webbtjänster är ett enklare sätt att göra applikationfunktioner tillgängliga för olika typer av externa system och användare. Som standard exponerar [!INCLUDE[prod_short](includes/prod_short.md)] flera objekt som webbtjänster för bättre integration med andra Microsoft-tjänster. Du kan lägga till andra webbtjänster när ditt företag behöver det.  

Skapa en webbtjänst i [!INCLUDE[prod_short](includes/prod_short.md)] och publicera sedan webbtjänsten så att den är tillgänglig för autentiserade användare. Alla behöriga användare kan komma åt metadata för webbtjänster, men endast användare, som har tillräcklig behörighet kan komma åt faktiska data.  

## <a name="creating-and-publishing-a-web-service"></a>Skapa och publicera en webbtjänst

Följande Moment beskriver hur du skapar och publicerar en webbtjänst.  

### <a name="to-create-and-publish-a-web-service"></a>Så här Skapa och publicera en webbtjänst  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Webbtjänster** och väljer sedan relaterad länk.  
2. Välj **Nytt** på sidan **Webbtjänster**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Codeunit** och **Sida** är giltiga typer för SOAP-webbtjänster. **Sida** och **fråga** är giltiga typer för OData-webbtjänster. Från och med version 16.3 är också **codeunit** en giltig typ för OData v4-webbtjänster, men då visas ingen URL i användargränssnittet. Om databasen innehåller flera företag, kan du välja ett objekt-ID som är unikt för ett av företagen.  
    > Tjänstnamnet visas för konsumenter av din webbtjänsten och utgör basen för att identifiera och för att särskilja webbtjänster, så se till att välja ett meningsfullt namn.

3. Markera kryssrutan i kolumnen **Publicerat**.  

När du publicerar webbtjänsten visar fälten **OData-URL** och **SOAP-URL** nya URL:er. För kodmoduler som är exponerade som icke-bundna åtgärder för OData v4 visas dock inte URL-fälten.  

Du kan testa webbtjänsten omedelbart, genom att välja länkarna i de fälten **OData-URL** och **SOAP-URL**. Om du vill kan du kopiera värdet i fältet och spara det för senare användning. Om du vill testa kodmoduler som visas som obundna åtgärder för OData v4 följer du instruktionerna i avsnittet [Verifiera webbtjänsttillgänglighet](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) i utvecklarinnehållet.

> [!NOTE]
> Om de objekt som du visar som webbtjänster inte får vara åtkomliga från [!INCLUDE[prod_short](includes/prod_short.md)] online, måste du markera de metoder som visas i koden som `[Scope('OnPrem')]`. Mer information finns i [attributet Omfattning](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).

När du publicerar en webbtjänst, är den tillgänglig för externa parter. Du kan kontrollera tillgängligheten för den webbtjänsten genom att använda en webbläsare, eller välja länken i fälten **OData-URL** och **SOAP-URL** på sidan **Webbtjänster**. Följande tillvägagångssätt visar hur du kan kontrollera tillgängligheten av webbtjänsten för senare användning.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Om du vill kontrollera tillgängligheten av en webbtjänst  

1. Ange den relevanta URL.en i din webbläsare. Följande tabell visar vilka olika typer av URL som du kan ange för olika webbtjänsttyper.  

    > [!div class="mx-tdBreakAll"]
    > |Typ|Syntax|Exempel|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Företagsnamnsfältet är skiftlägeskänsligt.|

2. Granska informationen som visas i webbläsaren. Kontrollera att du kan visa namnet på webbtjänsten som du har skapat.  

När du öppnar en webbtjänst, och du vill skriva data tillbaka till [!INCLUDE[prod_short](includes/prod_short.md)], måste du ange företagsnamn. Du kan skriva in företaget som en del av den URI som visas i exemplen, eller så kan du skriva in företaget som en del av frågeparametrarna. Till exempel pekar följande URI.er på samma OData-webbtjänst och båda är giltiga URI:er.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Se även

[Administration](admin-setup-and-administration.md)  
[Business Central webbtjänster för utvecklare](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[Begärandegräns för OData](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  


[!INCLUDE[footer-include](includes/footer-banner.md)]