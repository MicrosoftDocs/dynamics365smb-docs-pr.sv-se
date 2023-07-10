---
title: Felsöka automatiserade arbetsflöden
description: Lär dig mer om felsökning av kopplingen mellan Business Central och Power Automate när du skapar ett automatiserat arbetsflöde.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions, Power Automate,'
ms.date: 06/16/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: d365-business-central
---

# <a name="troubleshoot-your--automated-workflows"></a>Felsöka [!INCLUDE[prod_short](includes/prod_short.md)] automatiserade arbetsflöden

När du ansluter [!INCLUDE [prod_short](includes/prod_short.md)] till Power Automate för att skapa automatiserade arbetsflöden kan det hända att du stöter på felmeddelanden. Den här artikeln innehåller förslag på lösningar av vanligt förekommande problem.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Flödet körs inte på alla poster som skapats eller ändrats

### <a name="problem"></a>Problem

Om en händelse skapar eller ändrar många poster, körs inte flödet på vissa eller inte på några poster.

### <a name="possible-cause"></a>Möjlig orsak

För närvarande finns det en gräns för hur många poster ett flöde kan hantera. Om fler än 100 poster skapas eller ändras inom 30 sekunder utlöses inte flödet.

> [!NOTE]
> För utvecklare utförs flödesaktiveringen via webhook-meddelanden, och denna begränsning beror på hur Business Central-anslutningen hanterar `collection`-meddelanden. Mer information finns i [Arbeta med webhooks i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) i Hjälp för utvecklare och administratörer.

## <a name="the-response-from-the-business-central-service-is-too-large-error"></a>Felmeddelandet "svaret från den Business Central-tjänsten är för stort"

### <a name="problem-1"></a>Problem

När du använder en åtgärd som interagerar med poster (t.ex. *Skapa post (V3)* och *Skapa post (V3)*), Power Automate kan ett felmeddelande som liknar detta visas.

`The response from the Business Central service is too large`

### <a name="possible-cause-1"></a>Möjlig orsak

Även om Business Central inte har någon fastställd gräns för storleken på poster som returneras av API:er Dynamics 365 Business Central anslutningsprogram för Power Automate kan endast hantera poster upp till 8 MB.

Alla Business Central API:er som tillhandahålls av Microsoft returnerar poster under denna gräns, men API:er som tillhandahålls av partners kanske inte gör det. Om ett felmeddelande visas om att svaret från Business Central-tjänsten är för stort, kontaktar du den partner som skapade det API som du använder.

## <a name="entity-set-not-found-error"></a>Felmeddelandet "Entitetsuppsättningen hittades inte"

### <a name="problem-2"></a>Problem

När du skapar ett nytt Power Automate-flöde med hjälp av en utlösare för [!INCLUDE[prod_short](includes/prod_short.md)]-godkännande, t. ex. *När ett godkännande av inköpsdokument begärs*, kan det hända att du får ett felmeddelande liknande detta:

`Entity set not found: \<name\>`

Platshållaren, `\<name\>`, är namnet på den webbtjänst som saknas, till exempel *workflowWebhookSubscriptions* eller *workflowPurchaseDocumentLines*.

### <a name="possible-cause-2"></a>Möjlig orsak

För att du ska kunna använda Power Automate för dina godkännanden måste vissa sidor och codeunit-objekt publiceras som webbtjänster. Som standard publiceras de flesta nödvändiga objekt som webbtjänster. I vissa fall kan din miljö emellertid ha anpassats så att dessa objekt inte längre publiceras.

### <a name="fix"></a>Korrigera

Gå till sidan **Webbtjänster** och kontrollera att följande objekt publiceras som webbtjänster. Det ska finnas en post i listan för respektive objekt, med kryssrutan **Publicerad** markerad.  

| Objekttyp | Objekt-ID | Objektnamn | Tjänstnamn |
|--|--|--|--|
| Kodmodul | 1544 | WorkflowWebhookSubscription | WorkflowActionResponse |
| Sida | 6408 | workflowCustomers | workflowCustomers |
| Sida | 6406 | workflowGenJournalBatches | workflowGenJournalBatches |
| Sida | 6407 | workflowGenJournalLines | workflowGenJournalLines |
| Sida | 6409 | workflowItems | workflowItems |
| Sida | 6405 | Entitet för inköpsdokumentrad | workflowPurchaseDocumentLines |
| Sida | 6404 | workflowPurchaseDocuments | workflowPurchaseDocuments |
| Sida | 6403 | Entitet för försäljningsdokumentrad | workflowSalesDocumentLines |
| Sida | 6402 | workflowSalesDocuments | workflowSalesDocuments |
| Sida | 6410 | workflowVendors | workflowVendors |
| Sida | 831 | workflowWebhookSubscriptions | workflowWebhookSubscriptions |

> [!NOTE]
> Värdet **Tjänstnamn** värde måste anges exakt det som visas i registret. Ändra eller äversätt inte tjänstnamnet.

Mer information om publicering av webbtjänster finns i [Publicera en webbtjänst](across-how-publish-web-service.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/use-power-automate/).

## <a name="see-also"></a>Se även

[Använda Power Automate-flöden i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)  
[Arbetsflöde](across-workflow.md)  
[Konfigurera automatiserade arbetsflöden](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Växla till snabbflöden](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  
[Hantera Power Automate-flöden](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
