---
title: Arbetsflöden i Dynamics 365 Business Central
description: Använd de inbyggda arbetsflödesfunktionerna för att skapa arbetsflöden för godkännande som ska komplettera automatiserade arbetsflöden som baseras på Power Automate. Du kan ange steg för att tilldela uppgifter till olika personer som en del i de olika verksamhetsuppgifterna.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: ecaaf9bbb56e1c1b47f9f617319b32f32a2920fd
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585628"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Arbetsflöden i Dynamics 365 Business Central

Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.

Standardversionen av [!INCLUDE [prod_short](includes/prod_short.md)] stöder tre typer av arbetsflöden:

* Arbetsflöden för godkännande baserade på inbygga mallar för arbetsflöden

  På sidan **Arbetsflödesmallar** kan du se alla tillgängliga arbetsflöden. Utvärderingsversionen av [!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett antal förkonfigurerade arbetsflöden som representeras av arbetsflödesmallar som du kan kopiera för att skapa nya. När du öppnar en mall från sidan **Arbetsflödesmallar** och arbetsflödets namn börjar med *MS-*, läggs mallen till av Microsoft.
  
* Power Automate flöden som du skapar själv

  Alla arbetsflödesmallar som du skapar med Microsoft Power Automate läggs till i listan över arbetsflödesmallar i [!INCLUDE[prod_short](includes/prod_short.md)]. Läs mer i [Använd [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate-flöden](across-how-use-financials-data-source-flow.md). 
  
* Omedelbara flöden som utlöses manuellt av åtgärden **Automatisera** ([!INCLUDE [prod_short](includes/prod_short.md)] endast online).

  Skapa och utlösa manuellt en Power Automate-flöde i en [!INCLUDE[prod_short](includes/prod_short.md)] såsom en kund, artikel eller försäljningsorder, med alternativ för att manipulera information både internt och externt (med hjälp av integrerade verktyg). Läs mer i avsnittet [Direktflöden](across-how-use-financials-data-source-flow.md#instant-flows).

## <a name="power-automate-flows"></a>Power Automate-flöden

Med [!INCLUDE [prod_short](includes/prod_short.md)] online kan du registrera dig Power Automate och bygga upp kraftfulla automatiserade arbetsflöden. Du kan köra dessa arbetsflöden inifrån [!INCLUDE [prod_short](includes/prod_short.md)], ansluta interna och externa källor med data och verktyg utan att behöva kodningskunskaper.

Power Automate-flöden kan utlösas av händelser (t.ex. post eller dokument som skapas, ändras eller tas bort) och köras på ett användardefinierat schema eller vid behov (kallas **direktflöde**).

## <a name="approval-workflows"></a>Arbetsflöden för godkännande

Du kan skapa ett arbetsflöde för godkännande genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.<!--What are the "values"? Can we give an example?-->

Exempel på olika typer av arbetsflödes händelser är bland annat generering av försäljningsorder, inköpsorder, offerter, fakturor, prisändringar och leverantörs- eller kundändringar.

[!INCLUDE[workflow](includes/workflow.md)]

| **Om du vill** | **Se** |
|--|--|
| Konfigurera arbetsflödesanvändare för godkännande, anger hur användarna får meddelanden och skapa nya arbetsflöden. (För att skapa nya arbetsflöden för scenarier som inte stöds, implementera de nödvändiga arbetsflödeselementen genom att anpassa programkoden.) | [Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md) |
| Aktivera arbetsflöden för godkännande, agera på arbetsflödemeddelanden inklusive begära och godkänna arbetsflödessteg. Arkivera och ta bort arbetsflöden. | [Använda arbetsflöden för godkännande](across-use-workflows.md) |
| Integrera företagsdata med Power Automate arbetsflöden med både interna och externa källor och händelser för att skapa och automatisera aktiviteter eller arbetsflöden. | [Använda Power Automate-flöden i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/create-workflows/)

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Hantera projekt](projects-manage-projects.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Felsöka automatiserade arbetsflöden i [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
