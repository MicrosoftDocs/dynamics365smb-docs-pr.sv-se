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
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 952f2b9dc301b6941d13b4c23ac55f83b781739f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245924"
---
# <a name="publish-a-web-service"></a>Publicera en webbtjänst

Webbtjänster är en enklare sätt att göra applikationfunktioner tillgängliga för en mängd olika externa system och användare. [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett antal objekt som visas som webbtjänster som standard på grund av integrationen med andra Microsoft-tjänster, men du kan också lägga till andra webbtjänster.  

Du kan ställa in en webbtjänst i Windows-klienten eller i webbklienten. Sedan måste Du publicerar webbtjänsten för att göra den tillgänglig att serva förfrågningar över nätverket. Användare kan upptäcka webbtjänster, genom att styra en webbläsare på serverplatsen och begär en lista över tillgängliga tjänster. När du publicerar en webbtjänst, blir den direkt tillgänglig i nätverket för autentiserade användare. Alla behöriga användare kan komma åt metadata för webbtjänster, men endast användare, som har tillräcklig behörighet kan komma åt faktiska data.

## <a name="creating-and-publishing-a-web-service"></a>Skapa och publicera en webbtjänst  
Följande Moment beskriver hur du skapar och publicerar en webbtjänst.  

### <a name="to-create-and-publish-a-web-service"></a>Så här Skapa och publicera en webbtjänst  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Webbtjänster** och välj sedan relaterad länk.  
2. Välj **Nytt** på sidan **Webbtjänster**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Codeunit** och **Sida** är giltiga typer för SOAP-webbtjänster. **Sida** och **fråga** är giltiga typer för OData-webbtjänster.  
    > Om databasen innehåller flera företag, kan du välja ett objekt-ID som är unikt för ett av företagen.  
    > Tjänstnamnet visas för konsumenter av din webbtjänsten och utgör basen för att identifiera och för att särskilja webbtjänster, så se till att välja ett meningsfullt namn.

3. Markera kryssrutan i kolumnen **Publicerat**.  

När du publicerar webbtjänsten kan du, i fälten **OData-URL** och **SOAP-URL**, se URL som genereras för webbtjänsten. Du kan testa webbtjänsten omedelbart, genom att välja länkarna i de fälten **OData-URL** och **SOAP-URL**. Om du vill kan du kopiera värdet i fältet och spara det för senare användning.  

> [!IMPORTANT]
> För kodenheter som har publicerats som en SOAP-webbtjänst, måste de metoder som visas i kodenheten vara markerade med `[External]` i koden.

När du publicerar en webbtjänst, är den tillgänglig för externa parter. Du kan kontrollera tillgängligheten för den webbtjänsten, genom att använda en webbläsare, eller så kan du välja länken i fälten **OData-URL** och **SOAP-URL** på sidan **Webbtjänster**. Följande tillvägagångssätt visar hur du kan kontrollera tillgängligheten av webbtjänsten för senare användning.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Om du vill kontrollera tillgängligheten av en webbtjänst  

1. Ange den relevanta URL.en i din webbläsare. Följande tabell visar vilka olika typer av URL som du kan ange för olika webbtjänsttyper.  

    > [!div class="mx-tdBreakAll"]
    > |Typ|Syntax|Exempel|
    > |----------------|------|-------|
    > |SOAP |https://api.businesscentral.dynamics.com/*version*/*innehavare*/WS/*CompanyName*/*enhet*/ |`https://api.businesscentral.dynamics.com/v1.0/a10b3ee6-d9a2-42fe-926f-946e23bb8ddd/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|https://api.businesscentral.dynamics.com/*version*/*innehavare*/ODataV4/Company('*CompanyName*')/*enhet*|`https://api.businesscentral.dynamics.com/v1.0/a10b3ee6-d9a2-42fe-926f-946e23bb8ddd/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Företagsnamnsfältet är skiftlägeskänsligt.|

2. Granska informationen som visas i webbläsaren. Kontrollera att du kan visa namnet på webbtjänsten som du har skapat.  

När du öppnar en webbtjänst, och du vill skriva data tillbaka till [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du ange företagsnamn. Du kan skriva in företaget som en del av URI som visas i exempel, eller så kan du skriva in företaget som en del av frågaparametrarna. Till exempel pekar följande URI.er på samma OData-webbtjänst och båda är giltiga URI:er.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Se även

[Administration](admin-setup-and-administration.md)  
[Business Central webbtjänster för utvecklare](/dynamics365/business-central/dev-itpro/webservices/web-services)  
