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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

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
    *När en post skapas*,  
    *När en post tas bort*,  
    *När en post ändras*,  
    *När ett kundgodkännande begärs*,  
    *När ett godkännande för redovisningsjournal begärs*,  
    *När ett godkännande av en redovisningsjournalrad begärs*,  
    *När ett artikelgodkännande begärs*,  
    *När ett godkännande av ett inköpsdokument begärs*,  
    *När ett godkännande av ett säljdokument begärs*, eller  
    *När ett leverantörsgodkännande begärs*.
5. Flow komner att uppmana dig att ange den information som behövs för att ansluta till dina [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Om du har valt någon av följande utlösare: *När en post skapas*, *När en post ändras*, eller *När en post tas bort*, måste du välja ett företagsnamn och tabellnamn. Till varje utlösare krävs bara företagsnamnet för att ansluta.

   Flow visar en lista över företag och tabeller som finns på [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dessa listor eller slutpunkter motsvarar de webbtjänster som du har publicerat från ditt [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Du kan också skapa en ny webbtjänst-URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] med hjälp av åtgärden **skapa datauppsättning** på sidan **webbtjänster** med hjälp av den assisterade inställningsguiden **Ställa in rapportering**  eller genom att välja åtgärden **redigera i Excel** i någon lista.

Du har nu lyckats ansluta till dina Finance and Operations, Business edition-data och är redo att börja skapa ditt flöde. Mer information finns i [Flow-dokumentation](https://flow.microsoft.com/documentation/getting-started/).

För att felsöka ditt Microsoft Flow, se [Felsöka integrering med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Se även
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  
[Hantera användare och behörigheter](ui-how-users-permissions.md)    
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  

