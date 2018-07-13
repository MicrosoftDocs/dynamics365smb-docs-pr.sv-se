---
title: "Felsöka integrering med Microsoft Flow | Microsoft Docs"
description: "Felsök hur du kan göra dina Business Central-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa ett automatiskt arbetsflöde."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 80bc35f6ea8c4264c2cd8960be3370e5966b88e3
ms.contentlocale: sv-se
ms.lasthandoff: 06/01/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a>Felsöka integrering med Microsoft Flow - URL för begäran är för lång
Du kan använda din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av ett arbetsflöde i Microsoft Flow.  

> [!NOTE]  
>   Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Flow.  

Om du skapar ett Microsoft Flow med hjälp av anslutningen [!INCLUDE[d365fin](includes/d365fin_md.md)] visas ibland ett felmeddelande om att begärd URL är för lång efter det att flödet har skapats, till exempel: **RequestUriTooLong**.

## <a name="cause"></a>Orsak
För att ett flöde ska lösa ut letar det efter ändringar i dina data. För att bestämma huruvida din information har ändrats, jämför kopplingarna cachelagrade data med de nya uppgifter som begärs från källan.  

Om databegäran skapar en URL som är för lång, misslyckas den. Vanliga orsaker är till exempel:
- I allmänhet källtabeller med mer än 250 rader
- Källtabeller som innehåller flera tusen transaktioner

## <a name="workaround"></a>Lösning
Följ nedanstående instruktioner om du vill lösa problemet.
1. Välj att redigera det flöde som inte fungerar.
2. Expandera **visa avancerade alternativ** i flödesutlösaren.
3. I fältet **Hoppa över räkning** anger du det antal transaktioner som ska hoppas över.  
Till exempel: Om den tabell som du använder som datakälla har 4 000 transaktioner, ange då 4 000 som antalet transaktioner som ska hoppas över.
4. Uppdatera ditt flöde.

> [!NOTE]  
> Kopplingen är fortfarande på betastadiet. Uppdateringar av hur förändras kommer i en framtida version.


## <a name="see-also"></a>Se även
[Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett automatiserat arbetsflöde](across-how-use-financials-data-source-flow.md)  
[Komma igång](product-get-started.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Hantera användare och behörigheter](ui-how-users-permissions.md)    
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  

