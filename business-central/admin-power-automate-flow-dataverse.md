---
title: Använda ett Power Automate flöde för aviseringar till enhetsändringar
description: Lär dig hur du skapar ett flöde i Power Automate som meddelar dig när en enhet ändras i Dataverse-miljön.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power Automate, Flow, Dataverse'
ms.search.form: null
ms.date: 09/05/2022
ms.author: bholtorf
---
# <a name="use-a-power-automate-flow-for-alerts-to-dataverse-entity-changes"></a>Använda ett Power Automate flöde för aviseringar till Dataverse enhetsändringar

Administratörer kan skapa ett automatiserat flöde i Power Automate som meddelar [!INCLUDE[prod_short](includes/prod_short.md)] om ändringar av poster i din [!INCLUDE [cds_long_md](includes/cds_long_md.md)] organisation.

> [!NOTE]
> I den här artikeln förutsätts att du har anslutit din online-version av [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE [cds_long_md](includes/cds_long_md.md)] och schemalagt synkronisering mellan de två programmen.

## <a name="import-the-flow-template"></a>Importera flödesmallen

> [!TIP]
> För att göra det enklare att konfigurera flödet har vi skapat en mall som definierar utlösaren och flödesvillkoret åt dig. Om du vill använda mallen följer du instruktionerna i det här avsnittet. Om du vill skapa flödet själv hoppar du över det här avsnittet och börjar med stegen i [definiera flödesutlösaren](#define-the-flow-trigger).

1. Logga in på [Power Automate](https://powerautomate.microsoft.com).
2. Välj **Mallar** och sök sedan efter **Meddela Business Central**.

:::image type="content" source="media/power-automate-import-template.png" alt-text="Nyckelord för att hitta flödesmallen.":::
3. Välj alternativet **Meddela Business Central när ett konto ändras**.
4. Fortsätt med stegen i avsnittet [Meddela Business Central om en ändring](#notify-business-central-about-a-change).

## <a name="define-the-flow-trigger"></a>Definiera flödesutlösaren

1. Logga in på [Power Automate](https://flow.microsoft.com).
2. Skapa ett automatiserat molnflöde som startar när en rad för en [!INCLUDE [cds_long_md](includes/cds_long_md.md)] entitet läggs till, ändras eller tas bort. Mer information finns i [Utlös flöden när en rad läggs till, ändras eller tas bort](/power-automate/dataverse/create-update-delete-trigger). I det här exemplet används enheten **konton** . I följande bild visas inställningarna för det första steget när en flödes utlösare definieras.

:::image type="content" source="media/power-automate-flow-dataverse-trigger.png" alt-text="Inställningar för utlösare för flödet":::
3. Använd knappen **AssistEdit (...)** i det övre högra hörnet för att lägga till anslutningen till din [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljö.
4. Välj **Visa avancerade alternativ** och på fältet **Filterrader** ange **customertypecode eq 3** eller **customertypecode eq 11** och **statecode eq 0**. Dessa värden innebär att utlösaren endast reagerar när aktiva konton av typen **kund**eller **leverantör** ändras.

## <a name="define-the-flow-condition"></a>Definiera flödesvillkor

Data synkroniseras mellan [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE [cds_long_md](includes/cds_long_md.md)] via ett integrationsanvändarkonto. Om du vill ignorera de ändringar som gjorts i synkroniseringen skapar du ett villkorssteg i flödet som inte täcker de ändringar som görs av integrationsanvändarkontot.  

1. Lägg till steget **Hämta en rad med ID från Dataverse** efter flödesutlösaren med följande inställningar. Mer information finns i [Hämta en rad efter ID Dataverse](/power-automate/dataverse/get-row-id).

    1. I fältet **Tabellnamn**, välj **Användare**
    2. I fältet **rad-ID** väljer du alternativet **ändrad av (värde)** från flödesutlösaren.  

2. Lägg till ett villkorssteg med följande **eller**-inställningar för att identifiera integrationsanvändarkontot.
    1. Användarens **primära e-postadress** innehåller **contoso.com**
    2. Användarens **fullständiga namn** innehåller **[!INCLUDE[prod_short](includes/prod_short.md)]**.

3. Lägg till en avsluta kontroll för att stoppa flödet om enheten ändrades av kontot integrationsanvändare.

Följande bild visar hur du definierar flödesutlösaren och flödesvillkoret.

:::image type="content" source="media/power-automate-flow-dataverse.png" alt-text="Översikt över flödesutlösare och villkorsinställningar":::

## <a name="notify-business-central-about-a-change"></a>Meddela Business Central om en ändring

Om flödet inte har stoppats av villkoret måste du meddela [!INCLUDE[prod_short](includes/prod_short.md)] att det inträffar en ändring. Använd [!INCLUDE[prod_short](includes/prod_short.md)]-anslutningsprogrammet för att göra detta.

1. I **inga**delen av villkorssteget lägger du till en åtgärd och söker efter **Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]**. Välj anslutningsikonen i listan.
2. Välj åtgärden **Skapa post (V3)**.

:::image type="content" source="media/power-automate-flow-dataverse-connector.png" alt-text="Inställningar för [!INCLUDE[prod_short](includes/prod_short.md)] anslutningsprogram":::

3. Använd knappen **Assist redigera (...)** i det övre högra hörnet för att lägga till anslutningen till din [!INCLUDE[prod_short](includes/prod_short.md)]-miljö.
4. När du är ansluten fyller du i fälten **miljönamn** och **företagsnamn**.
5. I fältet **API-kategori** ange **microsoft/dataverse/v1.0**.
6. I **Tabellnamn** ange **dataverseEntityChanges**.
7. I fältet **entityName** ange **konto**.
8. Spara flödet.

Följande bild visar hur ditt flöde ska se ut.

:::image type="content" source="media/power-automate-flow-dataverse-summary.png" alt-text="Översikt över alla inställningar för flödet":::

När du lägger till, tar bort eller ändrar ett konto i din [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljö utförs följande åtgärder av det här flödet:

1. Anropa den [!INCLUDE[prod_short](includes/prod_short.md)]-miljö som du har angett i [!INCLUDE[prod_short](includes/prod_short.md)]anslutningen.
2. Använd [!INCLUDE[prod_short](includes/prod_short.md)] API för att infoga en post med **entityName** inställt på **konto** i tabellen **Dataverse ingångsändring**. Den här parametern är det exakta namnet på den Dataverse entitet som du skapar flödet för.
3. [!INCLUDE[prod_short](includes/prod_short.md)] kommer att starta jobbkötransaktionen som synkroniserar kunder med konton.

## <a name="see-also"></a>Se även

[Använda Business Central i Power Automate-flöden](across-how-use-financials-data-source-flow.md)  
[Konfigurera automatiserade arbetsflöden](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Integrera med Microsoft Dataverse](admin-common-data-service.md)  
[Synkroniserar data i Business Central med Microsoft Dataverse](admin-synchronizing-business-central-and-sales.md)  
