---
title: Konfigurera Copilot- och AI-funktioner
description: I den här artikeln beskrivs hur du aktiverar Copilot i en miljö.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/29/2023
ms.custom: bap-template
ms.search.form: 7775
---

# <a name="configure-copilot-and-ai-capabilities"></a>Konfigurera Copilot- och AI-funktioner

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Den här artikeln förklarar hur du åtkomst till Copilot och andra AI-funktioner i Business Central. Denna uppgift utförs av en administratör. Copilot är en systemfunktion och en integrerad del av Business Central. I likhet med de flesta systemfunktioner ger du inte åtkomst till enskilda användare och du kan inte heller slå på eller av Copilot. Copilot erbjuder dock datastyrningskontroller och möjligheten att inaktivera individuella Copilot- och AI-funktioner för varje miljö. Det finns olika nivåer av åtkomstkontroll till AI-funktioner, beroende på funktionen:

- Tillåt dataförflyttning mellan geografiska regioner

  Den här uppgiften krävs bara om din Business Central-miljö finns i ett annat geografiskt område än den Azure OpenAI Service som används. [Läs mer](#allow-data-movement-across-geographies)

- Aktivera funktionen på sidan **Copilot och AI-funktioner**. [Läs mer](#activate-features)

- Aktivera den specifika funktionen om den fortfarande styrs av **funktionshantering**.

  I utgivningscykel 2 för 2023 ingår både textförslagen för marknadsföring och hjälpfunktionerna för bankkontoavstämning under **Funktionshantering**. [Läs mer](#enable-feature-in-feature-management)

Om något av dessa krav inte uppfylls kan funktionen inte användas.

## <a name="prerequisites"></a>Förutsättningar

- Du använder Business Central Online, version 23.1 eller senare. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Du har administratörs- eller superbehörighet i Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## <a name="allow-data-movement-across-geographies"></a>Tillåt dataförflyttning mellan geografiska områden

Den här uppgiften gäller endast om växeln **Tillåt dataförflyttning** visas längst upp på sidan **Copilot och AI-funktioner**. Om länken **Hur styr jag mina copilot-data?** visas istället för knappen **Tillåt dataförflyttning**, hoppa över detta steg.

![Visar en skärmbild av knappen Tillåt dataförflyttning på sidan Copilot och AI-kapacitet.](media/allow-data-movement-v2.png)

Knappen **Tillåt dataförflyttning** anger att din Business Central-miljöplats&mdash;det vill säga det geografiska område där data bearbetas och lagras&mdash;inte är detsamma som det Azure OpenAI Service-område som används av Copilot. Om du vill aktivera Copilot måste du tillåta dataförflyttning mellan geografiska områden. Mer information om dataförflyttning finns i [Copilot-dataförflyttning mellan geografiska områden](ai-copilot-data-movement.md). 

Så här tillåter du dataförflyttning utanför ditt geografiska område:

1. I Business Central, sök efter och öppna sidan **Copilot- och AI-funktioner**.
1. Aktivera reglaget **Tillåt dataförflyttning**.

Du kan välja bort detta genom att inaktivera reglaget  **Tillåt dataförflyttning**. När en Azure OpenAI Service blir tillgänglig i ditt Business Central-miljöområde ansluts din miljö automatiskt till den och växeln är inte längre tillgänglig. 


<!--
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

Alla Copilot- och AI-funktioner är aktiva som standard när de görs tillgängliga i förhandsvisning eller blir allmänt tillgängliga. Med sidan **Copilot och-funktioner** kan du aktivera eller inaktivera enskilda funktioner igen för alla användare.

1. I Business Central, sök efter och öppna sidan **Copilot- och AI-funktioner**.

1. På sidan visas alla tillgängliga Copilot- och AI-relaterade funktioner och deras aktuella status, som kan vara antingen aktiva eller inaktiva. Funktionerna är indelade i två avsnitt&mdash;ett avsnitt för funktioner i förhandsversionen och ett annat för funktioner som är allmänt tillgängliga. 

   [![Visar rollcenter för Business Central och checklista för Copilot](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Om du vill aktivera en funktion markerar du den i listan och väljer åtgärd **Aktivera**.
   - Om du vill aktivera en funktion markerar du den och väljer sedan åtgärden **Inaktivera**. 


## <a name="enable-feature-in-feature-management"></a>Aktivera funktionen i funktionshantering

När individuella Copilot-funktioner släpps i Business Central mindre uppdateringar, är dessa funktioner valfria fram till nästa större uppdatering. **Funktionshantering** används för att aktivera eller inaktivera funktioner som är i förhandsversion, till exempel bankavstämning och vissa funktioner som är allmänt tillgängliga, till exempel textförslag. [Läs mer om funktionshantering](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. I Business Central söker du efter och öppnar sidan **Funktionshantering**.
2. Om du vill aktivera en funktion anger du kolumnen **Aktiverad för** till **Alla användare**. Om du vill inaktivera en funktion anger du kolumnen **Aktiverad för** till **Ingen**. Använd följande tabell för att avgöra vilken växel som gäller för den Copilot- och AO-funktion som du vill aktivera:

   - **Förhandsgranskning av funktion: Bankkontoavstämning med Copilot** avser funktionen för bankkontoavstämningshjälp.
   - **Förhandsgranskning av funktioner: Skapa AI-drivna produktbeskrivningar med Copilot** avser funktionen för textförslag för marknadsföring.

   Mer information om funktionshantering i allmänhet finns i [Funktionshantering](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="granting-user-access"></a>Bevilja användaråtkomst

Copilot- och AI-funktioner kan erbjuda funktionalitet avsedd för alla användare i din organisation eller för specifika användarroller. De flesta Copilot- och AI-funktioner erbjuder åtkomstkontroll med hjälp av behörigheter och behörighetsuppsättningar i Business Central behörighetshanteringssystem. [Läs mer om behörigheter och behörighetsuppsättningar](ui-define-granular-permissions.md).

För att bevilja eller neka åtkomst till specifika Copilot- och AI-funktioner, läs dokumentationen eller rådfråga utgivaren av den funktionen för att identifiera vilka behörigheter som krävs. 

## <a name="next-steps"></a>Nästa steg

När du har aktiverat och godkänt funktionerna är du redo att prova dem. Gå till:

- [Lägg till marknadsföringstext för artiklar](item-marketing-text.md) 
- [Stämma med bankkontoavstämningshjälp](bank-reconciliation-with-copilot.md) 

## <a name="see-also"></a>Se även

[Felsöka Copilot- och AI-funktioner](ai-copilot-troubleshooting.md)  
[Översikt över förslag på marknadsföringstext](ai-overview.md)   
[Vanliga frågor och svar om förslag på marknadsföringstext](faqs-marketing-text.md)  
