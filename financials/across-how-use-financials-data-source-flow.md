---
title: Koppla Data med | Microsoft Docs
description: "Du kan göra dina Financials-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa ett automatiskt arbetsflöde."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: dde99e50c6984a7ec162b4047e8640e6affb3f25
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett automatiskt arbetsflöde
Du kan använda din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av ett arbetsflöde i Microsoft Flow.  

> [!NOTE]  
>   Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Att lägga till [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakälla i Flow.
1. I webbläsaren, går du till [flow.microsoft.com](https://flow.microsoft.com/en-us/), och loggar in.
2. Välj **Mina flöden** från menyn längst upp på sidan.
3. I fönstret **Mina flöden** kan välja alternativet **Skapa från tom**.
4. I listan över tillgängliga utlösare, välj någon av de [!INCLUDE[d365fin](includes/d365fin_md.md)] utlösare som är tillgängliga:  
    *När ett kundgodkännande begärs*,  
    *När ett godkännande för redovisningsjournal begärs*,  
    *När ett godkännande av en redovisningsjournalrad begärs*,  
    *När ett artikelgodkännande begärs*,  
    *När ett godkännande av ett inköpsdokument begärs*,  
    *När ett godkännande av ett säljdokument begärs*, eller  
    *När ett leverantörsgodkännande begärs*.
5. Flödet kommer att be dig att välja ett företag inom din [!INCLUDE[d365fin](includes/d365fin_md.md)] klientorganisation. Eftersom varje steg i flödet är oberoende av nästa kan du behöva definiera företaget flera gånger när du använder en [!INCLUDE[d365fin](includes/d365fin_md.md)]-mall.

Du har nu lyckats ansluta till dina Finance and Operations, Business edition-data och är redo att börja skapa ditt flöde. Mer information finns i [Flow-dokumentation](https://flow.microsoft.com/documentation/getting-started/).

För att felsöka ditt Microsoft Flow, se [Felsöka integrering med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Se även
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  
[Hantera användare och behörigheter](ui-how-users-permissions.md)    
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  

