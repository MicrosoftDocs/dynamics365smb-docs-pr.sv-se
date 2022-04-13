---
title: Ansluta dina data med Power Automate| Microsoft Docs
description: Du kan göra dina Business Central-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa ett automatiskt arbetsflöde.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 07/27/2021
ms.author: edupont
author: jswymer
ms.openlocfilehash: 62718df1c80cb419501b72bcbdb6d7a6f9f18402
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518473"
---
# <a name="use-prod_short-in-an-automated-workflow"></a>Använda [!INCLUDE[prod_short](includes/prod_short.md)] i ett automatiskt arbetsflöde

Du kan använda din [!INCLUDE[prod_short](includes/prod_short.md)]-data som en del av ett arbetsflöde i Microsoft Power Automate.

> [!NOTE]
> Förutom Power Automate kan du nu använda funktionerna för arbetsflöde inom [!INCLUDE[prod_short](includes/prod_short.md)]. Observera att trots att det finns två separata arbetsflödessystem, kommer alla arbetsflödesmallar du skapar med Power Automate läggas till i listan över arbetsflöde i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Arbetsflöden](across-workflow.md).  

> [!NOTE]  
> Du måste ha ett giltigt konto med [!INCLUDE[prod_short](includes/prod_short.md)] och med Power Automate.  

## <a name="add-prod_short-as-a-data-source-in-power-automate"></a>Lägg till [!INCLUDE[prod_short](includes/prod_short.md)] som datakälla i Power Automate

1. I webbläsaren, går du till [flow.microsoft.com](https://flow.microsoft.com), och loggar in.
2. Välj **Mina flöden** från menyn längst upp på sidan.
3. Det finns tre sätt att skapa ett flöde; **Starta från mall**, **Starta från tom** och **Starta från en anslutare**. En mall är ett fördefinierat flöde som har skapats åt dig. Om du vill använda en mall markerar du den och skapar en anslutning för varje tjänst som ska användas. Med alternativen **Starta från tom** och **Starta från en anslutning** kan du skapa ett nytt flöde helt från början.
4. För att skapa från tom väljer du på sidan **Mina flöden**, välj **Starta från tom** och **automatiserade flöde**.
5. Sök efter **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**-anslutaren.
6. Definiera ett namn och välj den utlösare som du vill använda för flödet.
7. I listan över tillgängliga utlösare, välj någon av de [!INCLUDE[prod_short](includes/prod_short.md)] utlösare som är tillgängliga:  

    - *När ett leverantörsgodkännande begärs*.  
    - *När ett godkännande av en redovisningsjournalrad begärs* 
    - *När en post tas bort*
    - *När en post ändras*
    - *När en post skapas*
    - *När en post ändras*
    - *När ett godkännande för redovisningsjournal begärs* 
    - *När ett kundgodkännande begärs*
    - *När ett artikelgodkännande begärs*
    - *När ett godkännande av ett inköpsdokument begärs*
    - *När ett godkännande av ett säljdokument begärs*

8. Power Automate kommer att uppmana dig att välja en miljö eller ett företag inom din [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisation samt de villkor som du vill hitta bland dina uppgifter.

    > [!NOTE]
    > [!INCLUDE[prod_short](includes/prod_short.md)]-anslutaren för Power Automate stöder flera produktions- och miljöer med begränsat läge. Om du inte har skapat flera produktionsmiljöer med begränsat läge är **Produktion** det enda tillgängliga alternativ som du kan välja.  

    Du har nu lyckats ansluta till dina Business Central [!INCLUDE[prod_short](includes/prod_short.md)]-data och är redo att börja skapa ditt flöde.

9. För att skapa från en mall väljer du alternativet **Starta från en mall**.
10. Sök efter **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**-mallar.
11. I listan över tillgängliga mallar väljer du någon av mallarna och välj sedan **Skapa**.  

    - *Begär godkännande av Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-försäljningsorder*
    - *Begär godkännande av Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-försäljningsoffert*
    - *Begär godkännande av Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-försäljningsfaktura*
    - *Begär godkännande av Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-försäljningskreditnota*
    - *Begär godkännande av Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-kund*
    - *Begär godkännande av Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-inköpsorder*
    - *Begär godkännande av Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-inköpsfaktura*
    - *Begär godkännande av Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-inköpskreditnota*  
    - *Begär godkännande av Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-artikel*
    - *Begär godkännande av Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-leverantör*
    - *Begär godkännande av Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-redovisningsjournal-batch*  
    - *Begär godkännande av Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-redovisningsjournalrader*
12. Power Automate visar en lista över tjänster som används i flödesmallen och ett försök görs att automatiskt ansluta till dessa tjänster. Om du inte redan har anslutit till en tjänst uppmanas du att logga in på alla de tjänster som du behöver ansluta till. En grön bockmarkering visas bredvid varje tjänst när en anslutning har utförts. Välj **Fortsätt**.
13. Power Automate kommer att be dig att välja en miljö eller företag inom din [!INCLUDE[prod_short](includes/prod_short.md)] klientorganisation. Eftersom varje steg i flödet är oberoende av nästa kan du behöva definiera miljö och företaget flera gånger när du använder en [!INCLUDE[prod_short](includes/prod_short.md)] Power Automate-flödesmall.

Mer information finns i [Power Automate dokumentation](/power-automate/getting-started).

## <a name="troubleshooting"></a>Felsökning

### <a name="entity-set-not-found-error"></a>Felmeddelandet "Entitetsuppsättningen hittades inte"

#### <a name="problem"></a>Problem

När du skapar ett nytt Power Automate-flöde med hjälp av en utlösare för [!INCLUDE[prod_short](includes/prod_short.md)]-godkännande, t. ex. *När ett godkännande av inköpsdokument begärs*, visas ett felmeddelande liknande detta:

**Entitetsuppsättningen hittades inte: \<name\>**

där **\<name\>** är namnet på den saknade webbtjänsten, exempelvis **workflowWebhookSubscriptions** eller **workflowPurchaseDocumentLines**.

#### <a name="possible-cause"></a>Möjlig orsak

För att du ska kunna använda Power Automate för att integrera med dina [!INCLUDE[prod_short](includes/prod_short.md)]-godkännandena måste vissa sidor och codeunit-objekt publiceras som webbtjänster. Som standard publiceras de flesta nödvändiga objekt som webbtjänster åt dig. I vissa fall kan din miljö emellertid ha anpassats så att dessa objekt inte längre publiceras.

#### <a name="fix"></a>Korrigering

Gå till sidan **Webbtjänster** och kontrollera att följande objekt publiceras som webbtjänster. Det ska finnas en post i listan för respektive objekt, med kryssrutan **Publicerad** markerad. 

|Objekttyp|Objekt-ID|Objektnamn|Tjänstnamn|
|-----------|---------|-----------|------------|
|Kodmodul|  1544    |WorkflowWebhookSubscription|WorkflowActionResponse|
|Sida|  6408|   workflowCustomers|  workflowCustomers|
|Sida   |6406   |workflowGenJournalBatches| workflowGenJournalBatches|
|Sida   |6407   |workflowGenJournalLines|workflowGenJournalLines|
|Sida   |6409   |workflowItems| workflowItems|
|Sida   |6405   |Entitet för inköpsdokumentrad|workflowPurchaseDocumentLines|
|Sida|  6404    |workflowPurchaseDocuments| workflowPurchaseDocuments|
|Sida|  6403    |Entitet för försäljningsdokumentrad |workflowSalesDocumentLines|
|Sida|  6402|   workflowSalesDocuments| workflowSalesDocuments|
|Sida|  6410    |workflowVendors|   workflowVendors|
|Sida|  831 |workflowWebhookSubscriptions|  workflowWebhookSubscriptions|

> [!NOTE]
> Värdet **Tjänstnamn** värde måste anges exakt det som visas i registret. Ändra eller äversätt inte tjänstnamnet.

Mer information om publicering av webbtjänster finns i [Publicera en webbtjänst](across-how-publish-web-service.md).

## <a name="see-also"></a>Se även

[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbetsflöde](across-workflow.md)  
[Importera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  
[Hantera [!INCLUDE[prod_long](includes/prod_long.md)]-arbetsflöden](across-use-workflows.md)  
[Användarinställningar för godkännande](across-how-to-set-up-approval-users.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Ekonomi](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]