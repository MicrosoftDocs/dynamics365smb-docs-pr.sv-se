---
title: Felsöka automatiserade arbetsflöden
description: Lär dig mer om felsökning av kopplingen mellan Business Central och Power Automate när du skapar ett automatiserat arbetsflöde.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: b8fff95ced93e7ee2a3112969f45525532b19445
ms.sourcegitcommit: e86f0bd15604c2fb327e3182929c44a4172790c7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786202"
---
# <a name="troubleshoot-your-prod_short-automated-workflows"></a>Felsöka [!INCLUDE[prod_short](includes/prod_short.md)] automatiserade arbetsflöden

När du ansluter [!INCLUDE [prod_short](includes/prod_short.md)] till Power Automate för att skapa automatiserade arbetsflöden kan det hända att du stöter på felmeddelanden. Den här artikeln innehåller förslag på lösningar av vanligt förekommande problem.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Flödet körs inte på alla poster som skapats eller ändrats

### <a name="problem"></a>Problem

Om en händelse skapar eller ändrar många poster, körs inte flödet på vissa eller inte på några poster.

### <a name="possible-cause"></a>Möjlig orsak

För närvarande finns det en gräns för hur många poster ett flöde kan hantera. Om fler än 100 poster skapas eller ändras inom 30 sekunder utlöses inte flödet.

> [!NOTE]
> För utvecklare utförs flödesaktiveringen via webhook-meddelanden, och denna begränsning beror på hur Business Central-anslutningen hanterar `collection`-meddelanden. Mer information finns i [Arbeta med webhooks i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) i Hjälp för utvecklare och administratörer.

## <a name="entity-set-not-found-error"></a>Felmeddelandet "Entitetsuppsättningen hittades inte"

### <a name="problem"></a>Problem

När du skapar ett nytt Power Automate-flöde med hjälp av en utlösare för [!INCLUDE[prod_short](includes/prod_short.md)]-godkännande, t. ex. *När ett godkännande av inköpsdokument begärs*, kan det hända att du får ett felmeddelande liknande detta:

`Entity set not found: \<name\>`

Platshållaren, `\<name\>`, är namnet på den webbtjänst som saknas, till exempel *workflowWebhookSubscriptions* eller *workflowPurchaseDocumentLines*.

### <a name="possible-cause"></a>Möjlig orsak

För att du ska kunna använda Power Automate för dina godkännanden måste vissa sidor och codeunit-objekt publiceras som webbtjänster. Som standard publiceras de flesta nödvändiga objekt som webbtjänster åt dig. I vissa fall kan din miljö emellertid ha anpassats så att dessa objekt inte längre publiceras.

### <a name="fix"></a>Korrigering

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

[Använda [!INCLUDE[prod_short](includes/prod_short.md)] i ett automatiserat arbetsflöde](across-how-use-financials-data-source-flow.md)  
[Arbetsflöde](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]