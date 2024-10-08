---
title: Konfigurera Copilot- och AI-funktioner
description: I den här artikeln beskrivs hur du aktiverar Copilot i en miljö.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/28/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
ms.search.form: '7771,7772_Primary,7775_Primary'
---

# <a name="configure-copilot-and-ai-capabilities"></a>Konfigurera Copilot- och AI-funktioner

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Den här artikeln förklarar hur du åtkomst till Microsoft Copilot och andra AI-funktioner i Dynamics 365 Business Central. En administratör måste slutföra dessa uppgifter.

Copilot är en systemfunktion och en integrerad del av Business Central. I likhet med de flesta systemfunktioner ger du inte åtkomst till enskilda användare och du kan inte heller slå på eller av Copilot. Copilot erbjuder dock datastyrningskontroller och möjligheten att inaktivera individuella Copilot- och AI-funktioner för varje miljö. Det finns olika nivåer av åtkomstkontroll till AI-funktioner, beroende på funktionen:

- Tillåt dataförflyttning mellan geografiska regioner.

    Den här uppgiften krävs bara om din Business Central-miljö finns i ett annat geografiskt område än den Azure OpenAI Service som används. [Läs mer om den här uppgiften](#allow-data-movement-across-geographies).

- Aktivera funktionen på sidan **Copilot och AI-funktioner**. [Läs mer om den här uppgiften](#activate-features).

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
- Enable the specific feature if it's governed by **Feature Management**.

  Check whether  of 2024 release wave 1, chat with Copilot, marketing text suggestions, and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)
<!-- 
- Enable the specific feature, if it's still governed by **Feature Management**.

  In 2023 release wave 2, both the marketing text suggestions and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)-->

Om något av dessa krav inte uppfylls kan funktionen inte användas.

## <a name="prerequisites"></a>Förutsättningar

- Du använder Business Central Online.
- Du är en [administratör](#requirements-for-being-an-administrator) i Business Central.

## <a name="allow-data-movement-across-geographies"></a>Tillåt dataförflyttning mellan geografiska områden

Den här uppgiften gäller endast om alternativet **Tillåt dataförflyttning** visas längst upp på sidan **Copilot och AI-funktioner**. Om länken **Hur styr jag mina copilot-data?** visas istället för alternativet **Tillåt dataförflyttning**, hoppa över detta steg.

![Skärmbild som visar alternativet Tillåt datarörelse på sidan Copilot & AI-funktioner.](media/allow-data-movement-v2.png)

Alternativet **Tillåt dataförflyttning** anger att din Business Central-miljö (det vill säga det geografiska område där data bearbetas och lagras) inte är detsamma som det Azure OpenAI Service-område som används av Copilot. Om du vill aktivera Copilot måste du tillåta dataförflyttning mellan geografiska områden. [Mer information om dataförflyttning](ai-copilot-data-movement.md).

Så här tillåter du dataförflyttning utanför ditt geografiska område:

1. I Business Central, sök efter och öppna sidan **Copilot- och AI-funktioner**.
1. Aktivera alternativet **Tillåt dataförflyttning**.

    > [!NOTE]
    > För miljöer i Azure-regionerna Europa, västra och Europa, norra är alternativet **Tillåt dataförflyttning** aktiverat som standard.

Du kan välja bort dataflytt genom att inaktivera alternativet **Tillåt dataförflyttning**.

När en Azure OpenAI Service blir tillgänglig i ditt Business Central-miljöområde ansluts din miljö automatiskt till den. Då visas inte längre alternativet **Tillåt dataförflyttning** på sidan **Copilot- och-funktioner**.

<!-- Don't review
| Australia, United Kingdom, United States | Within the respective geographical region |
| Europe, France, Germany, Norway, Switzerland  | Sweden or Switzerland |
| Asia Pacific, Brazil, Canada, India, Japan, Singapore, South Africa, South Korea, United Arab Emirates  | United States |-->



<!--Note

If your environment is hosted in North America, Copilot will use an Azure OpenAI endpoint in North America to process your data.
If your environment is hosted in Europe, Copilot will use an Azure OpenAI endpoint in Europe to process your data.
If your environment is hosted anywhere else, Copilot will use an Azure OpenAI endpoint outside of the region in which the environment is hosted.
To opt in 

Copilot and other AI capabilities use Azure OpenAI Service.  and are provided by default to only those customers with environments that have United States as their geography for data processing and storage. While the Azure OpenAI Service is available in multiple geographies including Australia, Canada, United States, France, Japan and UK, Copilot does not follow the same regional rollout schedule.

Meanwhile, customers with environments outside the United States can use Copilot AI features by opting in to share relevant data with the Azure OpenAI Service in United States or Switzerland.

The information in the following table outlines the Azure OpenAI service that's used by the Copilot services based on the geography of their Dynamics 365 environment when they opt-in to share data.-->

## <a name="activate-features"></a>Aktivera funktioner

Alla Copilot- och AI-funktioner är aktiva som standard när de görs tillgängliga i förhandsvisning eller blir allmänt tillgängliga. På sidan **Copilot och-funktioner** kan du aktivera eller inaktivera enskilda funktioner igen för alla användare.

1. I Business Central, sök efter och öppna sidan **Copilot- och AI-funktioner**.
1. På sidan visas alla tillgängliga Copilot- och AI-relaterade funktioner och deras aktuella status. (Status kan vara antingen *Aktiv* eller *Inaaktiv*.) Funktionerna är indelade i två avsnitt: ett avsnitt för funktioner i förhandsversionen och ett annat för funktioner som är allmänt tillgängliga.

    - Om du vill aktivera en funktion markerar du den i listan och väljer **Aktivera**.
    - Om du vill aktivera en funktion markerar du den och väljer sedan **Inaktivera**.

    [![Skärmbild som visar knapparna Aktivera och Inaktivera för funktionslistorna på sidan Copilot- och AI-funktioner.](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

<!-- don't review 

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
## <a name="enable-feature-in-feature-management"></a>Enable feature in Feature Management

When individual Copilot capabilities are released in Business Central minor updates, these capabilities are optional until the next major update. **Feature Management** is used to turn on or off features that are in preview, like bank reconciliation, and some features that are generally available, like marketing text suggestions. [Learn more about feature management](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. In Business Central, search for and open the **Feature Management** page.
2. To enable a feature, set the **Enabled for** column to **All users**. To disable a feature, set the **Enabled for** column to **None**. Use the following table to help you determine the switch that applies to the Copilot and AI capability you want to enable:

   - **Feature Preview: Bank account reconciliation with Copilot** enables the bank account reconciliation assist feature.
   - **Feature Preview: Chat with Copilot** enables the chat with Copilot feature.
   - **Feature preview: Create AI-powered product descriptions with Copilot** enables the marketing text suggestions feature.

   For more information about feature management in general, go to [Feature Management](/dynamics365/business-central/dev-itpro/administration/feature-management).-->

## <a name="granting-user-access"></a>Bevilja användaråtkomst

Copilot- och AI-funktioner kan erbjuda funktionalitet avsedd för alla användare i din organisation eller för specifika användarroller. De flesta Copilot- och AI-funktioner erbjuder åtkomstkontroll med hjälp av behörigheter och behörighetsuppsättningar i Business Central behörighetshanteringssystem. [Läs mer om behörigheter och behörighetsuppsättningar](ui-define-granular-permissions.md).

I följande tabell visas de behörigheter som krävs för att använda Copilot-funktioner som tillhandahålls av Business Central.

| Copilot-funktion | Behörigheter som krävs |
|---|---|
| Analyshjälp | **DATA ANALYSIS – EXEC** behörighetsuppsättning eller körningsbehörighet för systemobjekt 9640 **Tillåt dataanalysläge**. Dessa behörigheter är samma behörigheter som krävs för att komma åt analysläget. |
| Hjälp med bankkontoavstämning | Behörighet på sidan 7250 **AI-förslag för bankkontoavstämning** och sidan 7252 **AI-förslag för transaktion till redovisningskonto**. |
| Chatt | Det finns inga behörigheter eller behörighetsuppsättningar som kontrollerar åtkomst till chatt på en användarnivå. Om chatten är aktiverad är den tillgänglig för alla användare. |
| Mappa e-dokument | Behörighet på sidan 6166 **E-Doc. PO Copilot Prop**. |
| Förslag på marknadsföringstext | Behörighet på sidan 5836 **Marknadsföringstext för Copilot**. |
| Förslag på försäljningsrader | Tillstånd på sidan 7275 **AI-förslag på försäljningsrader** och sidan 7276 **AI-förslag på försäljningsrader** |

För att bevilja eller neka åtkomst till specifika Microsoft copilot- och AI-funktioner konsultera funktionens dokumentation eller utgivare för att identifiera de nödvändiga behörigheterna.

## <a name="requirements-for-being-an-administrator"></a>Krav för att vara administratör

Du måste ha antingen SUPER-behörighet i Business Central-användarkontot eller någon av följande Business Central-licenser:

- Delegerad administratörsagent – partner
- Delegerad helpdeskagent – partner
- Intern admin
- Intern BC-administratör
- Dynamics 365-administratör

Business Central erbjuder ännu inte detaljerade behörigheter på objektnivå så att endast specifika administratörer kan konfigurera Copilot.

## <a name="next-steps"></a>Nästa steg

När du har aktiverat och godkänt funktionerna är du redo att prova dem. Gå till följande artiklar:

- [Lägg till marknadsföringstext för artiklar med Copilot](item-marketing-text.md)
- [Analysera listdata med hjälp av Copilot](analysis-assist.md)
- [Chatt med Copilot](chat-with-copilot.md)
- [Mappa e-dokument mot inköpsorderrader med Copilot](map-edocuments-with-copilot.md)
- [Stämma av bankkonton med Copilot](bank-reconciliation-with-copilot.md)
- [Föreslå rader på försäljningsorder med Copilot](sales-suggest-sales-lines-with-copilot.md)

## <a name="see-also"></a>Se även

[Felsöka Copilot- och AI-funktioner](ai-copilot-troubleshooting.md)  
[Vanliga frågor och svar om analyshjälp](faqs-analysis-assist.md)  
[Vanliga frågor och svar om hjälp med bankkontoavstämning](faqs-bank-reconciliation.md)  
[Vanliga frågor och svar om chatt med Copilot](faqs-chat-with-copilot.md)  
[Vanliga frågor om mappning av e-dokument med inköpsorder](faqs-map-edocuments.md)  
[Vanliga frågor och svar om förslag på marknadsföringstext](faqs-marketing-text.md)  
[Vanliga frågor och svar för försäljningsrader](faq-sales-suggest-sales-lines-with-copilot.md)  
[Översikt över förslag på marknadsföringstext](ai-overview.md)
