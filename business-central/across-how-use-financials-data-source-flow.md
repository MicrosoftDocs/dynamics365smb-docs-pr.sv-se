---
title: Använda Power Automate-flöden i Business Central
description: Konfigurera och använda Power Automate-flöden för att skapa eller ändra Business Central-data.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Power Automate,'
ms.search.form: '1500,'
ms.date: 08/31/2023
ms.custom: bap-template
---

<!-- Line 41 says there are three cloud flow types, but the table lists four. Should line 41 change? -->


# Använda Power Automate-flöden i [!INCLUDE[prod_short](includes/prod_short.md)]

Med [!INCLUDE[prod_short](includes/prod_short.md)] får du en licens Microsoft Power Automate. Med denna licens kan du använda din [!INCLUDE[prod_short](includes/prod_short.md)]-data som en del av ett arbetsflöde i Microsoft Power Automate. Du skapar dina egna flöden och anslut dina data från interna och externa källor med [!INCLUDE [prod_short](includes/prod_short.md)]-kopplingen.

Power Automate-flöden initieras av händelser, t.ex. när en post skapades, ändrades eller togs bort. Flödena kan också köras på ett användardefinierat schema eller vid behov.

> [!NOTE]
> Administratörer kan begränsa åtkomsten till Power Automate. Om du upptäcker att du inte har tillgång till några eller alla funktioner som beskrivs i den här artikeln, prata med din administratör. Om du vill lära dig hur du kan kontrollera Power Automate-åtkomst som en administratör, se [Konfigurera Power Automate-integrering](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

<!-- You must have a valid account with both [!INCLUDE[prod_short](includes/prod_short.md)] and Power Automate. --> 

> [!TIP]
> Förutom Power Automate kan du använda mallarna för arbetsflöden för godkännande i [!INCLUDE[prod_short](includes/prod_short.md)]. Trots att det finns två separata arbetsflödessystem, kommer alla mallar för arbetsflöden för godkännande som du skapar med Power Automate att läggas till i listan över arbetsflöden i [!INCLUDE[prod_short](includes/prod_short.md)]. Läs mer i [arbetsflöden](across-workflow.md).

## Om Power Automate-flöden

Power Automate är en tjänst som hjälper dig att skapa automatiserade arbetsflöden (eller flöden) mellan appar och tjänster, t.ex. [!INCLUDE[prod_short](includes/prod_short.md)]. Power Automate flöden kräver lite eller ingen kodkunskap. De kan kopplas till en mängd olika händelser och svar, till exempel:

- Poständringar
- Uppdateringar av externa filer
- Bokförda dokument
- Olika tjänster från Microsoft och andra leverantörer, som t.ex. Microsoft Outlook, Excel, Dataverse, Teams, SharePoint, Power Apps, mm.

Det finns tre olika typer av molnflöden som du kan arbeta med:

|Flödestyp|Beskrivning|
|---------|-----------|
|Automatiserat flöde|Den här flödestypen körs automatiskt av en händelse. I [!INCLUDE[prod_short](includes/prod_short.md)] kan en händelse vara när en post eller ett dokument skapas, ändras eller tas bort. En ny försäljningsfaktura kan t.ex. utlösa ett flöde för en begäran om godkännande, som kan ha olika händelser beroende på svar från godkännare. Ett negativt svar skickar ett meddelande och ett e-postmeddelande till godkännande beställaren. Ett positivt svar uppdaterar samtidigt ett Excel-kalkylblad som finns i en SharePoint-mapp och skickar en uppdatering till en chatt för Teams. Automatiserade flöden kan startas av både interna och externa händelser i [!INCLUDE[prod_short](includes/prod_short.md)].|
|Godkännandeflöde|Godkännandeflöden är också automatiserade flöden i Power Automate, men de är utformade specifikt för att begära godkännande när ändringar görs i poster och data. Du kan använda godkännandeflöden i Power Automate som ett alternativ till [funktionen för arbetsflöde för godkännande](across-use-workflows.md) som ingår i [!INCLUDE[prod_short](includes/prod_short.md)]. |
|Schemalagt flöde|Den här typen av flöde körs också automatiskt, men körs med jämna mellanrum vid schemalagda datum och tidpunkter. |
|Direktflöde|Den här flödestypen körs vid behov och kräver att användaren kör den manuellt från en knapp eller åtgärd i en annan app eller enhet, i det här fallet [!INCLUDE[prod_short](includes/prod_short.md)] klienten. Direktflöden fungerar på samma sätt som kommando genvägar, så att du kan utföra stegvisa steg med några knapptryckningar och startas från vissa sidor eller tabeller. Ett flöde kan t.ex. lägga till en knapp på åtgärds menyn på sidan **leverantörer** för att spärra betalningar till en leverantör och samtidigt skicka anpassningsbara e-postmeddelanden till leverantörens kontakt och företagets inköpare samt uppdatera kontakten i Outlook. |

## Power Automate-funktioner

Du kan utforska alla Power Automate flöden som är tillgängliga för dig genom att logga in på [Power Automate](https://powerautomate.com) och välja **Mina flöden** från navigeringsfältet till vänster. Här hittar du de flöden som du redan har skapat själv och flöden som har delats med dig av en administratör eller en medarbetare.

- Direkt flöden görs också tillgängliga för körning direkt från de flesta list-, kort- och dokumentsidor i [!INCLUDE[prod_short](includes/prod_short.md)]. Snabbflödena finns i åtgärdsgruppen **Automatisera** i åtgärdsfältet på sidorna. Om du vill köra ett flöde markerar du det och följer instruktionerna som visas för dig. Läs mer i avsnitten som följer.

- Med automatiska flöden i [!INCLUDE[prod_short](includes/prod_short.md)] finns det ingenting som du kan göra, om du inte vill ändra dem eller inaktivera dem. Annars fungerar de bara när de utlöses. 
<!--

## Automated flows

With Power Automate, you can create business flows directly in-house and rely on citizen developers. Automated workflows can be started by both internal and external events in [!INCLUDE[prod_short](includes/prod_short.md)], and also be set to run periodically. Learn more and get instructions on how to create flows in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

-->

## Kör direktflöden

Direktflöden öppnas i [!INCLUDE [prod_short](includes/prod_short.md)] online, så att du håller dig inom ramen för affärsprocessen du höll på med. Du kan köra ett direktflöde från de flesta listor, kort eller dokument.

1. Välj **automatisera** i åtgärdsfältet och välj sedan ett flöde från listan över tillgängliga flöden under **Power Automate** åtgärden.

    :::image type="content" source="media/power-automate-instant-menu.svg" alt-text="Visar åtgärden Automatisera med åtgärder för direktflöde.":::

    På vissa sidor kapslas funktionen **automatiskt** in under **fler alternativ (...)**. 
2. I fönstret **Kör flöde** i de obligatoriska fälten och välj **Fortsätt** för att köra flödet.

> [!NOTE]
> Första gången du använder **Automatiserat** objekt visas kanske bara åtgärden **Kom igång Power Automate**. Den här åtgärden visas eftersom det inte gick att acceptera sekretessmeddelandet för Microsoft Power Automate. Välj **Kom igång med Power Automate** och följ instruktionerna för att acceptera eller acceptera för att fortsätta.  
>
> :::image type="content" source="media/power-automate-action.png" alt-text="Visar det automatiserade objektet i åtgärdsfältet.":::

<!--

[!INCLUDE [prod_short](includes/prod_short.md)] can run a Power Automate flow from most list, card, and document pages. Once the admin has connected [!INCLUDE [prod_short](includes/prod_short.md)] with Power Automate, you'll see any flows your organization has added when you choose the **Automate** action on the relevant pages. Instant flows are run without leaving [!INCLUDE [prod_short](includes/prod_short.md)]. Learn more in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

These instant flows open on a page inside [!INCLUDE [prod_short](includes/prod_short.md)] online so you can remain within the context of the business process you were in the middle of. Choose the **Automate** action—on some pages nested under the **More Options** menu—choose the **Power Automate** menu item, then choose the relevant link to trigger the workflow. The connection to Power Automate is already set up for you.

Most flows require you to fill in a field or two before you choose the **Run flow** action.

> [!TIP]
> If you don't see an **Automate** action, then your [!INCLUDE [prod_short](includes/prod_short.md)] probably hasn't yet been set up to use Power Automate. Learn more from your admin.-->

## Skapa, redigera och hantera flöden

Att skapa nya flöden, ändra och hantera befintliga (som att aktivera eller inaktivera dem) kan göras direkt i Power Automate. Du kan emellertid starta några av dessa uppgifter via åtgärdsmenyn Automatisera i [!INCLUDE[prod_short](includes/prod_short.md)]:

:::image type="content" source="media/power-automate-menu.svg" alt-text="Visar instruktionen automatisera i åtgärdsfältet med utökade åtgärder.":::

- Om du vill skapa ett automatiserat flöde från en lista, ett kort eller en dokumentsida väljer du **Automatisera** > **Skapa automatiserat flöde**.
- Om du vill skapa ett arbetsflöde för godkännande från ett kort eller en dokumentsida väljer du **Automatisera** > **Skapa godkännandeflöde**.

  > [!TIP]
  > Den här åtgärden är endast tillgänglig på kort- och dokumenttypssidor, inte listor.
- Om du vill skapa ett direktflöde från en lista, ett kort eller en dokumentsida väljer du **Automatisera** > **Skapa åtgärd baserat på ett flöde**.
- Om du vill öppna Power Automate från en lista, ett kort eller en dokumentsida väljer du **Automatisera** > **Hantera flöden**.
<!--- To create new flows or manage existing flows from inside [!INCLUDE[prod_short](includes/prod_short.md)], got to the **Manage Power Automate Flows** page.-->

Dessa uppgifter utförs vanligtvis av en administratör eller superanvändare. Uppgifterna kräver en bredare kunskap om affärsprocesserna i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du vill veta mer går du till följande artiklar i Business Central-hjälpen för utvecklare och IT-proffs:

- [Power Automate integrering](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-overview)
- [Skapa automatiserade flöden](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows) (omfattar även godkännandeflöden)
- [Skaba snabbflöden](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)
- [Hantera Power Automate-flöden](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)
<!-- 

## Add more automated flows and instant flows

You can create flows through the [powerautomate.microsoft.com](https://powerautomate.microsoft.com) website. However, if your admin has switched on the capability to run Power Automate flows from inside [!INCLUDE [prod_short](includes/prod_short.md)] online, you can start the process of building a flow from the **Automate** action on the relevant pages, which can be found under the **More Options** menu depending on the page. Then choose the **Power Automate** menu item, and then choose the **Create a flow** action. Power Automate then opens in a new browser tab, and you're signed in automatically.

You can find sample templates to adapt to your company and all available trigger events, using both [!INCLUDE [prod_short](includes/prod_short.md)] and external tools, by choosing the **Connectors** menu on the Power Automate website. Learn more about available templates and triggers in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

## Create and manage Power Automate flows

You can create new flows or manage existing Power Automate flows in [!INCLUDE [prod_short](includes/prod_short.md)] on the **Manage Power Automate Flows** page. Learn more in the [Manage Power Automate Flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) article in the administration content.

<!--
You can also manage available Power Automate workflows on the **Workflows** page in [!INCLUDE[prod_short](includes/prod_short.md)]. The page lists both the built-in approval and Power Automate workflows, with options for the latter to enable/disable, delete, and view the workflow on the Power Automate website.-->

## Se även

[Felsöka automatiserade arbetsflöden i [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  
[Förbered dig för att göra affärer](ui-get-ready-business.md)  
[Arbetsflöden](across-workflow.md)  
[Importera affärsdata från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Tilldela användare och grupper behörigheter](ui-define-granular-permissions.md)  
[Konfigurera [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Ekonomihantering](finance.md)  
[Hantera Power Automate-flöden](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Konfigurera automatiserade arbetsflöden](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Växla till snabbflöden](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
