---
title: Koppla Data med | Microsoft Docs
description: Du kan göra dina Business Central-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa ett automatiskt arbetsflöde.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 1652c4bc22425bd6df4ac303a96a2ab1b28bfaf9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241102"
---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett automatiskt arbetsflöde
Du kan använda din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av ett arbetsflöde i Microsoft Flow.

> [!NOTE]
> Förutom Microsoft Flow kan du nu använda funktionerna för arbetsflöde inom [!INCLUDE[d365fin](includes/d365fin_md.md)]. Observera att trots att det finns två separata arbetsflödessystem, kommer alla Flow-mallar du skapar med Microsoft Flow läggas till i listan över arbetsflödesmallar i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Arbetsflöden](across-workflow.md).  

> [!NOTE]  
>   Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Att lägga till [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakälla i Flow.
1. I webbläsaren, går du till [flow.microsoft.com](https://flow.microsoft.com/en-us/), och loggar in.
2. Välj **Mina flöden** från menyn längst upp på sidan.
3. Det finns 2 olika sätt att skapa ett flöde: **Skapa från mall** och **Skapa från tom**. En mall är ett fördefinierat flöde som har skapats åt dig.  Om du vill använda en mall markerar du den och skapar en anslutning för varje tjänst som ska användas. Med en tom mall kan du skapa ett nytt flöde helt och hållet från början.
4. På sidan **Mina flöden** väljer du alternativet **Skapa från tom** om du vill skapa från en tom mall.
5. Sök efter **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**-anslutaren.
6. I listan över tillgängliga utlösare, välj någon av de [!INCLUDE[d365fin](includes/d365fin_md.md)] utlösare som är tillgängliga:  
    *När ett kundgodkännande begärs*,  
    *När ett godkännande för redovisningsjournal begärs*,  
    *När ett godkännande av en redovisningsjournalrad begärs*,  
    *När ett artikelgodkännande begärs*,  
    *När ett godkännande av ett inköpsdokument begärs*,  
    *När ett godkännande av ett säljdokument begärs*, eller  
    *När ett leverantörsgodkännande begärs*.
7. Flödet omber dig att välja ett företag inom din [!INCLUDE[d365fin](includes/d365fin_md.md)]-klientorganisation samt de villkor som du vill hitta bland dina uppgifter.

Nu har du lyckats ansluta till dina Business Central-data och är redo att börja skapa ditt flöde.

8. Välj alternativet **Skapa från mall** för att skapa från en mall.
9. Sök efter **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**-mallar.
10. I listan över tillgängliga mallar väljer du någon av mallarna.  
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-försäljningsorder*,  
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-försäljningsoffert*,  
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-försäljningsfaktura*,  
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-försäljningskreditnota*,  
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-kund*,  
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-inköpsorder*,  
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-inköpsfaktura*,  
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-inköpskreditnota*,  
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-artikel*,  
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-leverantör*,  
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-redovisningsjournal-batch*,  
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-redovisningsjournalrader*.  
11. Flödet kommer att be dig att välja ett företag inom din [!INCLUDE[d365fin_md](includes/d365fin_md.md)] klientorganisation. Eftersom varje steg i flödet är oberoende av nästa kan du behöva definiera företaget flera gånger när du använder en [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-flödesmall.

Mer information finns i [Flödesdokumentationen](https://docs.microsoft.com/en-us/flow/getting-started).

För felsökning av din Microsoft Flow, se [felsökning integrering med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Se även
[Komma igång](product-get-started.md)  
[Arbetsflöde](across-workflow.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Hantera användare och behörigheter](ui-how-users-permissions.md)   
[Hantera [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-arbetsflöden](across-use-workflows.md)  
[Användarinställningar för godkännande](across-how-to-set-up-approval-users.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  
