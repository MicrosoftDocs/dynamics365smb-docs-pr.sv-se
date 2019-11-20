---
title: Koppla Data med | Microsoft Docs
description: Du kan göra dina Business Central-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa ett automatiskt arbetsflöde.
documentationcenter: ''
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: a46692503b19ddad57c4a68d0f29b588d84f5c9e
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775457"
---
# <a name="using-included365finincludesd365fin_mdmd-in-an-automated-workflow"></a>Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett automatiskt arbetsflöde
Du kan använda din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av ett arbetsflöde i Microsoft Flow.

> [!NOTE]
> Förutom Microsoft Flow kan du nu använda funktionerna för arbetsflöde inom [!INCLUDE[d365fin](includes/d365fin_md.md)]. Observera att trots att det finns två separata arbetsflödessystem, kommer alla Flow-mallar du skapar med Microsoft Flow läggas till i listan över arbetsflöde i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Arbetsflöden](across-workflow.md).  

> [!NOTE]  
> Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Flow.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-flow"></a>Att lägga till [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakälla i Flow.
1. I webbläsaren, går du till [flow.microsoft.com](https://flow.microsoft.com/en-us/), och loggar in.
2. Välj **Mina flöden** från menyn längst upp på sidan.
3. Det finns tre sätt att skapa ett flöde; **Starta från mall**, **Starta från tom** och **Starta från en anslutare**. En mall är ett fördefinierat flöde som har skapats åt dig. Om du vill använda en mall markerar du den och skapar en anslutning för varje tjänst som ska användas. Med alternativen **Starta från tom** och **Starta från en anslutning** kan du skapa ett nytt flöde helt från början.
4. För att skapa från tom väljer du på sidan **Mina flöden**, välj **Starta från tom** och **automatiserade flöde**.
5. Sök efter **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**-anslutaren.
6. Definiera ett namn och välj den utlösare som du vill använda för flödet.
7. I listan över tillgängliga utlösare, välj någon av de [!INCLUDE[d365fin](includes/d365fin_md.md)] utlösare som är tillgängliga:  
    
    *När ett leverantörsgodkännande begärs*.    
    *När ett godkännande av en redovisningsjournalrad begärs*,    
    *När en post tas bort*,    
    *När en post ändras*,    
    *När en post skapas*,    
    *När en post ändras*,    
    *När ett godkännande för redovisningsjournal begärs*,   
    *När ett kundgodkännande begärs*,   
    *När ett artikelgodkännande begärs*,    
    *När ett godkännande av ett inköpsdokument begärs*, eller     
     *När ett godkännande av ett säljdokument begärs*.
     
8. Flödet omber dig att välja en miljö eller ett företag inom din [!INCLUDE[d365fin](includes/d365fin_md.md)]-klientorganisation samt de villkor som du vill hitta bland dina uppgifter.

> [!NOTE]  
>   [!INCLUDE[d365fin](includes/d365fin_md.md)]-anslutaren för Microsoft Flow stöder flera produktions- och miljöer med begränsat läge. Om du inte har skapat flera produktionsmiljöer med begränsat läge **Produktion** är de enda tillgängliga alternativ som du kan välja. 

Nu har du lyckats ansluta till dina Business Central-data och är redo att börja skapa ditt flöde.

9. För att skapa från en mall väljer du alternativet **Starta från en mall**.
10. Sök efter **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**-mallar.
11. I listan över tillgängliga mallar väljer du någon av mallarna och välj sedan **Skapa**.  

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
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-redovisningsjournal-batch*, eller    
    *Begär godkännande av Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-redovisningsjournalrader*.  
12. I flödet visas en lista över tjänster som används i flödesmallen och ett försök görs att automatiskt ansluta till dessa tjänster. Om du inte redan har anslutit till en tjänst uppmanas du att logga in på alla de tjänster som behövs för att ansluta. En grön bockmarkering visas bredvid varje tjänst när en anslutning har utförts. Välj **Fortsätt**.
13. Flödet kommer att be dig att välja en miljö eller företag inom din [!INCLUDE[d365fin_md](includes/d365fin_md.md)] klientorganisation. Eftersom varje steg i flödet är oberoende av nästa kan du behöva definiera miljö och företaget flera gånger när du använder en [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-flödesmall.

Mer information finns i [Flödesdokumentationen](/flow/getting-started).

## <a name="see-also"></a>Se även
[Komma igång](product-get-started.md)  
[Arbetsflöde](across-workflow.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)   
[Hantera [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-arbetsflöden](across-use-workflows.md)  
[Användarinställningar för godkännande](across-how-to-set-up-approval-users.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  
