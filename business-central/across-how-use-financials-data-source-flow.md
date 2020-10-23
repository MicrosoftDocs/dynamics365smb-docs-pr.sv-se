---
title: Ansluta dina data med Power Automate| Microsoft Docs
description: Du kan göra dina Business Central-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa ett automatiskt arbetsflöde.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: bmeier
ms.openlocfilehash: 8f4da5b51b4e0df5cdf6f41f7a78c0a51cf0f083
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924859"
---
# <a name="using-prodshort-in-an-automated-workflow"></a>Använda [!INCLUDE[prodshort](includes/prodshort.md)] i ett automatiskt arbetsflöde

Du kan använda din [!INCLUDE[prodshort](includes/prodshort.md)]-data som en del av ett arbetsflöde i Microsoft Power Automate.

> [!NOTE]
> Förutom Power Automate kan du nu använda funktionerna för arbetsflöde inom [!INCLUDE[prodshort](includes/prodshort.md)]. Observera att trots att det finns två separata arbetsflödessystem, kommer alla arbetsflödesmallar du skapar med Power Automate läggas till i listan över arbetsflöde i [!INCLUDE[prodshort](includes/prodshort.md)]. Mer information finns i [Arbetsflöden](across-workflow.md).  

> [!NOTE]  
> Du måste ha ett giltigt konto med [!INCLUDE[prodshort](includes/prodshort.md)] och med Power Automate.  

## <a name="to-add-prodshort-as-a-data-source-in-power-automate"></a>Att lägga till [!INCLUDE[prodshort](includes/prodshort.md)] som datakälla i Power Automate.

1. I webbläsaren, går du till [flow.microsoft.com](https://flow.microsoft.com), och loggar in.
2. Välj **Mina flöden** från menyn längst upp på sidan.
3. Det finns tre sätt att skapa ett flöde; **Starta från mall**, **Starta från tom** och **Starta från en anslutare**. En mall är ett fördefinierat flöde som har skapats åt dig. Om du vill använda en mall markerar du den och skapar en anslutning för varje tjänst som ska användas. Med alternativen **Starta från tom** och **Starta från en anslutning** kan du skapa ett nytt flöde helt från början.
4. För att skapa från tom väljer du på sidan **Mina flöden**, välj **Starta från tom** och **automatiserade flöde**.
5. Sök efter **Microsoft [!INCLUDE[prodlong](includes/prodlong.md)]**-anslutaren.
6. Definiera ett namn och välj den utlösare som du vill använda för flödet.
7. I listan över tillgängliga utlösare, välj någon av de [!INCLUDE[prodshort](includes/prodshort.md)] utlösare som är tillgängliga:  

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

8. Power Automate omber dig att välja en miljö eller ett företag inom din [!INCLUDE[prodshort](includes/prodshort.md)]-klientorganisation samt de villkor som du vill hitta bland dina uppgifter.

    > [!NOTE]
    > [!INCLUDE[prodshort](includes/prodshort.md)]-anslutaren för Power Automate stöder flera produktions- och miljöer med begränsat läge. Om du inte har skapat flera produktionsmiljöer med begränsat läge **Produktion** är de enda tillgängliga alternativ som du kan välja.  

    Nu har du lyckats ansluta till dina Business Central [!INCLUDE[prodshort](includes/prodshort.md)]-data och är redo att börja skapa ditt flöde.

9. För att skapa från en mall väljer du alternativet **Starta från en mall**.
10. Sök efter **Microsoft [!INCLUDE[prodlong](includes/prodlong.md)]**-mallar.
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
12. Power Automate visar en lista över tjänster som används i flödesmallen och ett försök görs att automatiskt ansluta till dessa tjänster. Om du inte redan har anslutit till en tjänst uppmanas du att logga in på alla de tjänster som behövs för att ansluta. En grön bockmarkering visas bredvid varje tjänst när en anslutning har utförts. Välj **Fortsätt**.
13. Power Automate kommer att be dig att välja en miljö eller företag inom din [!INCLUDE[prodshort](includes/prodshort.md)] klientorganisation. Eftersom varje steg i flödet är oberoende av nästa kan du behöva definiera miljö och företaget flera gånger när du använder en [!INCLUDE[prodshort](includes/prodshort.md)] Power Automate-flödesmall.

Mer information finns i [Power Automate dokumentation](/power-automate/getting-started).

## <a name="see-also"></a>Se även

[Komma igång](product-get-started.md)  
[Arbetsflöde](across-workflow.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  
[Hantera [!INCLUDE[prodlong](includes/prodlong.md)]-arbetsflöden](across-use-workflows.md)  
[Användarinställningar för godkännande](across-how-to-set-up-approval-users.md)  
[Ställa in [!INCLUDE[prodshort](includes/prodshort.md)]](setup.md)  
[Ekonomi](finance.md)  
