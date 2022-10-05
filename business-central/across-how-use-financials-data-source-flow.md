---
title: Använda Power Automate flöden i Business Central
description: Konfigurera och använda Power Automate-flöden för att skapa eller ändra Business Central-data.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Power Automate,
ms.search.form: 1500,
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: 369ee2b4aded272a8a3a21fe810b4b6c62dd1de0
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585466"
---
# <a name="use-power-automate-flows-in-prod_short"></a>Använda Power Automate-flöden i [!INCLUDE[prod_short](includes/prod_short.md)]

Du kan använda din [!INCLUDE[prod_short](includes/prod_short.md)]-data som en del av ett arbetsflöde i Microsoft Power Automate. Skapa dina egna flöden och anslut dina data från interna och externa källor med [!INCLUDE [prod_short](includes/prod_short.md)]-kopplingen.

> [!NOTE]
> Du måste ha ett giltigt konto med både [!INCLUDE[prod_short](includes/prod_short.md)] och Power Automate.  

> [!TIP]
> Förutom Power Automate kan du använda mallarna för arbetsflöden för godkännande i [!INCLUDE[prod_short](includes/prod_short.md)]. Trots att det finns två separata arbetsflödessystem, kommer alla mallar för arbetsflöden för godkännande som du skapar med Power Automate att läggas till i listan över arbetsflöden i [!INCLUDE[prod_short](includes/prod_short.md)]. Läs mer i [arbetsflöden](across-workflow.md).

Power Automate-flöden utlöses av händelser som t.ex. post och dokument skapande, ändring eller borttagning (automatiserade flöden). Flödena kan också köras på ett användardefinierat schema (schemalagda flöden) eller vid behov (direkt flöden).

## <a name="power-automate-features-in-prod_short"></a>Power Automate funktioner i [!INCLUDE[prod_short](includes/prod_short.md)]

Flödet utökar de inbyggda funktionerna för godkännande arbetsflöden som är tillgängliga i [!INCLUDE[prod_short](includes/prod_short.md)]utan att behöva använda sig av kunskap och kan associeras med ett brett utbud av händelser och svar, såsom registerändringar, externa filuppdateringar, upplagda dokument och olika Microsoft- och tredjepartstjänster som t.ex. Microsoft Outlook, Microsoft Excel, Microsoft Dataverse, Microsoft Teams, Microsoft SharePoint, Microsoft Power Apps med mera.

En ny försäljningsfaktura kan t.ex. utlösa ett arbetsflöde för en begäran om godkännande, som kan ha olika händelser beroende på svar från godkännare. Ett negativt svar skickar ett meddelande och ett e-postmeddelande till godkännande beställaren. Ett positivt svar uppdaterar samtidigt ett Excel-kalkylblad som finns i en SharePoint-mapp och skickar en uppdatering till en chatt för Teams.

Direktflöden fungerar på samma sätt som kommando genvägar, så att du kan utföra stegvisa steg med några knapptryckningar och startas från vissa sidor eller tabeller. Ett flöde kan t.ex. lägga till en knapp på åtgärds menyn på sidan **leverantörer** för att spärra betalningar till en leverantör och samtidigt skicka anpassningsbara e-postmeddelanden till leverantörens kontakt och företagets inköpare samt uppdatera kontakten i Outlook.

## <a name="automated-workflows"></a>Automatiserade arbetsflöden

Med Power Automate kan du skapa affärsflöden direkt internt och förlita dig på civila utvecklare. Automatiserade arbetsflöden kan startas av både interna och externa händelser i [!INCLUDE[prod_short](includes/prod_short.md)] och anges så att de körs med jämna mellanrum. Lär dig mer och få instruktioner om hur du skapar arbetsflöden i artikeln [ange automatiserade arbetsflöden](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrations innehållet.

## <a name="instant-flows"></a>Direktflöden

Från och med utgivningscykel 1 2022 (maj 2022) kan [!INCLUDE [prod_short](includes/prod_short.md)] online administratörer [aktivera en funktion](admin-feature-management.md) för att göra det möjligt att köra ett Power Automate-flöde från de flesta sidor. Mer information finns i [Konfigurera automatiserade arbetsflöden](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrationsinnehållet.

När administratören har anslutit [!INCLUDE [prod_short](includes/prod_short.md)] till Power Automate ser du alla flöden som organisationen har lagt till när du väljer åtgärden **Automatisera** på de relevanta sidorna. Direktflöden körs utan att lämna [!INCLUDE [prod_short](includes/prod_short.md)].

Dessa direktarbetsflöden öppnas på en sida i [!INCLUDE [prod_short](includes/prod_short.md)] online, så att du håller dig inom ramen för affärsprocessen du höll på med. Välj åtgärden **Automatisera** som på vissa sidor är kapslad under menyn **Fler alternativ**, men du hittar den genom att välja menyobjektet **Power Automate** och sedan relevant länk för att utlösa arbetsflödet. Anslutningen till Power Automate har redan ställts in åt dig.

De flesta flöden kräver att du fyller i ett fält eller två innan du väljer åtgärden **Kör flöde**.

> [!TIP]
> Om du inte ser åtgärden **Automatisera** har [!INCLUDE [prod_short](includes/prod_short.md)] troligtvis inte konfigurerats till att använda Power Automate. Mer information från din administratör.

## <a name="add-more-automated-flows-and-instant-flows"></a>Lägga till fler automatiserade flöden och snabbflöden

Du kan skapa flöden på webbplatsen [powerautomate.microsoft.com](https://powerautomate.microsoft.com). Om din administratör har ställt in möjligheten att köra Power Automate-flöden i [!INCLUDE [prod_short](includes/prod_short.md)] online, kan du emellertid börja bygga upp ett flöde från åtgärden **automatisera** på de relevanta sidorna, som du hittar på menyn **fler alternativ** beroende på vilken sida som används. Välj sedan menyartikeln **Power Automate** och åtgärden **Skapa ett flöde**. Power Automate öppnas sedan i en ny flik i webbläsaren och du loggas in automatiskt.

Du kan hitta exempelmallar för att anpassa till ditt företag och alla tillgängliga triggerhändelser med båda [!INCLUDE [prod_short](includes/prod_short.md)] och externa verktyg genom att välja menyn **kopplingar** på webbplatsen Power Automate. Mer information om tillgängliga mallar och utlösare finns i [Konfigurera automatiserade arbetsflöden](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrationsinnehållet.

## <a name="manage-automated-workflows"></a>Hantera automatiserade arbetsflöden

Du kan skapa nya flöden eller hantera befintliga Power Automate-flöden i [!INCLUDE [prod_short](includes/prod_short.md)] på sidan **Hantera Power Automate-flöden**. Mer information finns i artikeln [Hantera Power Automate-flöden](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows.md) i administrationsinnehållet.

Du kan också hantera tillgängliga Power Automate arbetsflöden på sidan **arbetsflöden** i [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan visas både inbyggda godkännanden och Power Automate arbetsflöden, med alternativ för de senare för att aktivera/inaktivera, ta bort och visa arbetsflödet på webbplatsen Power Automate.

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/use-power-automate/)

## <a name="see-also"></a>Se även

[Felsöka automatiserade arbetsflöden i [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  
[Gör dig redo för affärer](ui-get-ready-business.md)  
[Arbetsflöden](across-workflow.md)  
[Importera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  
[Konfigurera [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Ekonomi](finance.md)  
[Hantera Power Automate-flöden](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Konfigurera automatiserade arbetsflöden](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Växla till snabbflöden](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
