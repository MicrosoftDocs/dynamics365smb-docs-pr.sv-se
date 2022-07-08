---
title: Använda Business Central i Power Automate-flöden
description: Konfigurera och använda Power Automate-flöden som skapar eller ändrar Business Central-data.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: f1128a9fb4e9643286e4305695e1d40719d86301
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079330"
---
# <a name="use-prod_short-in-power-automate-flows"></a>Använda [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate-flöden

Du kan använda din [!INCLUDE[prod_short](includes/prod_short.md)]-data som en del av ett arbetsflöde i Microsoft Power Automate. Skapa dina egna flöden och anslut dina data med [!INCLUDE [prod_short](includes/prod_short.md)]-kopplingen.  

> [!NOTE]  
> Du måste ha ett giltigt konto med [!INCLUDE[prod_short](includes/prod_short.md)] och med Power Automate.  

> [!TIP]
> Förutom Power Automate kan du använda mallarna för arbetsflöden för godkännande i [!INCLUDE[prod_short](includes/prod_short.md)]. Trots att det finns två separata arbetsflödessystem, kommer alla mallar för arbetsflöden för godkännande som du skapar med Power Automate att läggas till i listan över arbetsflöden i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Arbetsflöden](across-workflow.md).  

## <a name="automated-workflows"></a>Automatiserade arbetsflöden

Med Power Automate kan du skapa affärsflöden direkt internt och förlita dig på civila utvecklare. Mer information finns i [Konfigurera automatiserade arbetsflöden](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrationsinnehållet.  

## <a name="manual-instant-flows"></a>Manuella snabbflöden

Från och med maj 2022 kan en administratör av [!INCLUDE [prod_short](includes/prod_short.md)] online [aktivera en funktion](admin-feature-management.md) för att göra det möjligt att köra ett Power Automate-flöde från de flesta sidor. Mer information finns i [Konfigurera automatiserade arbetsflöden](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrationsinnehållet.  

När administratören har anslutit [!INCLUDE [prod_short](includes/prod_short.md)] till Power Automate ser du alla flöden som organisationen har lagt till när du väljer åtgärden **Automatisera** på de relevanta sidorna. Du kör flödena utan att lämna [!INCLUDE [prod_short](includes/prod_short.md)].  

Dessa automatiserade arbetsflöden öppnas i ett fönster i [!INCLUDE [prod_short](includes/prod_short.md)] online, så att du håller dig inom ramen för affärsprocessen du höll på med. På vissa sidor är åtgärden **Automatisera** dold under menyn **Fler alternativ**, men du hittar den genom att välja menyobjektet **Power Automate** och sedan relevant länk för att utlösa arbetsflödet. Anslutningen till Power Automate har redan ställts in åt dig.  

De flesta flöden kräver att du fyller i ett fält eller två innan du väljer åtgärden **Kör flöde**.  

> [!TIP]
> Om du inte ser åtgärden **Automatisera** har [!INCLUDE [prod_short](includes/prod_short.md)] troligtvis inte konfigurerats till att använda Power Automate. Kontakta administratören om du vill ha mer information.

## <a name="add-more-automated-flows-and-manual-instant-flows"></a>Lägga till fler automatiserade flöden och manuella snabbflöden

Du kan skapa flöden på webbplatsen [powerautomate.microsoft.com](https://powerautomate.microsoft.com). Om administratören har aktiverat funktionen för att köra Power Automate-flöden direkt från [!INCLUDE [prod_short](includes/prod_short.md)] online, kan du emellertid börja bygga ett flöde från åtgärden **Automatisera** på de relevanta sidorna. På vissa sidor är åtgärden **Automatisera** dold under menyn **Fler alternativ**, men du hittar den genom att välja menyobjektet **Power Automate** och sedan åtgärden **Skapa ett flöde**. Power Automate öppnas sedan i en ny flik i webbläsaren och du loggas in automatiskt.

## <a name="manage-workflows"></a>Hantera arbetsflöden

Du kan få en översikt över alla arbetsflöden som du har åtkomst till genom att välja åtgärden **Hantera arbetsflöden** på menyn **Power Automate**. Listan öppnas i en ny flik i webbläsaren och du loggas in på Power Automate automatiskt. Där kan du se när varje flöde kördes senast.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/use-power-automate/)

## <a name="see-also"></a>Se även

[Felsöka automatiserade arbetsflöden i [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  
[Gör dig redo för affärer](ui-get-ready-business.md)  
[Arbetsflöden](across-workflow.md)  
[Importera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  
[Konfigurera [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Ekonomi](finance.md)  
[Konfigurera automatiserade arbetsflöden](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]