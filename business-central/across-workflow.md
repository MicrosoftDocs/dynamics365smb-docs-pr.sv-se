---
title: Arbetsflöden i Dynamics 365 Business Central
description: Använd de inbyggda arbetsflödesfunktionerna för att skapa arbetsflöden för godkännande som ska komplettera automatiserade arbetsflöden som baseras på Power Automate. Du kan ange steg för att tilldela uppgifter till olika personer som en del i de olika verksamhetsuppgifterna.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/10/2022
ms.custom: bap-template
---
# <a name="workflows-in-dynamics-365-business-central"></a><a name="workflows-in-dynamics-365-business-central"></a>Arbetsflöden i Dynamics 365 Business Central

Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemaktiviteter, till exempel automatisk bokföring, kan inkluderas som arbetsflöden. Systemaktiviteter kan föregås eller följas av användaraktiviteter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.

Standardversionen av [!INCLUDE [prod_short](includes/prod_short.md)] stöder tre typer av arbetsflöden:
  
* Power Automate-flöden

  * Automatiserade flöden som utlöses av händelser (såsom skapande, ändring eller radering av poster eller dokument) i [!INCLUDE[prod_short](includes/prod_short.md)]. Dessutom ingår godkännande flöden som skapas i Power Automate som utlösare när ett godkännande begärs i [!INCLUDE[prod_short](includes/prod_short.md)].
  * Direkt flöden som aktiveras manuellt av åtgärden **Automatiserad** från listor, kort och dokumentsidor.

    Skapa och utlösa manuellt en Power Automate-flöde i en [!INCLUDE[prod_short](includes/prod_short.md)] såsom en kund, artikel eller försäljningsorder, med alternativ för att manipulera information både internt och externt (med hjälp av integrerade verktyg).

* Arbetsflöden för godkännande baserade på inbygga mallar för arbetsflöden

  På sidan **Arbetsflödesmallar** kan du se alla tillgängliga arbetsflöden. Utvärderingsversionen av [!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett antal förkonfigurerade arbetsflöden som representeras av arbetsflödesmallar som du kan kopiera för att skapa nya. När du öppnar en mall från sidan **Arbetsflödesmallar** och arbetsflödets namn börjar med *MS-*, läggs mallen till av Microsoft.

## <a name="power-automate-flows"></a><a name="power-automate-flows"></a>Power Automate-flöden

Med [!INCLUDE [prod_short](includes/prod_short.md)] online kan du registrera dig Power Automate och bygga upp kraftfulla automatiserade arbetsflöden. Du kör dessa arbetsflöden inifrån [!INCLUDE [prod_short](includes/prod_short.md)]. Flödena kan koppla ihop interna och externa datakällor och verktyg, utan kodkunskap.

|**Om du vill** |**Se**|
|-------|-------|
|Komma igång med Power Automate och skapa flöden, köra snabbflöden|[Använda Power Automate-flöden i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)|
|Mer information om hur du skapar, redigerar och hanterar flöden|[Ställa in automatiserade flöden](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) och [Ställa in direktflöden](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)|
|Ställ in Power Automate integration med [!INCLUDE[prod_short](includes/prod_short.md)] för användare som administratör|[Konfigurera Power Automate integrering](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup)|

## <a name="approval-workflows"></a><a name="approval-workflows"></a>Arbetsflöden för godkännande

Skapa ett arbetsflöde för godkännande genom att ange vad som ska starta arbetsflödet och vad som händer härnäst enligt följande:

* En arbetsflödeshändelse, som kontrolleras av händelsevillkor.
* Ett arbetsflödessvar som kontrolleras av svars alternativen.

För att definiera arbetsflödessteg, fyll i fält på arbetsflödeslinjer med hjälp av händelse- och svarsvärdena som representerar scenarier som stöds.

Exempel på olika typer av arbetsflödeshändelser är bland annat generering av försäljningsorder, inköpsorder, offerter, fakturor, prisändringar och leverantörs- eller kundändringar.

[!INCLUDE[workflow](includes/workflow.md)]

| **Om du vill** | **Se** |
|--|--|
| Konfigurera arbetsflödesanvändare för godkännande, anger hur användarna får meddelanden och skapa nya arbetsflöden. (För att skapa nya arbetsflöden för scenarier som inte stöds, implementera de nödvändiga arbetsflödeselementen genom att anpassa programkoden.) | [Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md) |
| Aktivera arbetsflöden för godkännande, agera på arbetsflödemeddelanden inklusive begära och godkänna arbetsflödessteg. Arkivera och ta bort arbetsflöden. | [Använda arbetsflöden för godkännande](across-use-workflows.md) |

<!--
| Integrate company data with Power Automate workflows, using both internal and external sources and events to create and automate tasks or workflows. | [Use Power Automate Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |-->

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/create-workflows/)

## <a name="see-also"></a><a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Hantera projekt](projects-manage-projects.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Felsöka automatiserade arbetsflöden i [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
