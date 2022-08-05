---
title: Arbetsflöden i Dynamic 365 Business Central
description: Använd de inbyggda arbetsflödesfunktionerna för att skapa arbetsflöden för godkännande som ska komplettera automatiserade arbetsflöden som baseras på Power Automate. Du kan ange steg för att tilldela uppgifter till olika personer som en del i de olika verksamhetsuppgifterna.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/12/2022
ms.author: edupont
ms.openlocfilehash: ab7d131e965b0698c6e33a0b1a43c8f408a7b1b2
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129909"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Arbetsflöden i Dynamics 365 Business Central

Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.  

Standardversionen av [!INCLUDE [prod_short](includes/prod_short.md)] stöder tre typer av arbetsflöden:

* Automatiserade arbetsflöden för godkännande baserade på inbygga mallar för arbetsflöden  

  På sidan **Arbetsflödesmallar** kan du se alla tillgängliga arbetsflöden. Utvärderingsversionen av [!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett antal förkonfigurerade arbetsflöden som representeras av arbetsflödesmallar som du kan kopiera för att skapa arbetsflöden. När du öppnar en arbetsflödesmall från sidan **Arbetsflödesmallar** och arbetsflödets namn börjar med *MS-*, läggs arbetsflödesmallen till av Microsoft.  
* Automatiserade flöden som du skapar själv  

  Alla arbetsflödesmallar som du skapar med Power Automate läggs till i listan över arbetsflödesmallar i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Använda Business Central i Power Automate-flöden](across-how-use-financials-data-source-flow.md).  
* Manuellt utlösta flöden från åtgärden **Automatisera** ([!INCLUDE [prod_short](includes/prod_short.md)] endast online). Mer information finns i [Manuella snabbflöden](across-how-use-financials-data-source-flow.md#manual-instant-flows).  

## <a name="power-automate-flows"></a>Power Automate-flöden

För [!INCLUDE [prod_short](includes/prod_short.md)] online kan du registrera dig för Power Automate och sedan skapa kraftfulla automatiserade flöden som du kan köra i [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Använda [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate-flöden](across-how-use-financials-data-source-flow.md).  

## <a name="automated-approval-workflows"></a>Automatiserade arbetsflöden för godkännande

Du kan skapa ett arbetsflöde för godkännande genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.  

[!INCLUDE[workflow](includes/workflow.md)]

Om du vill konfigurera och använda arbetsflöden som inte har definierats i Power Automate kontrollerar du följande artiklar:  

|**Om du vill**|**Se**|  
|------------|-------------|  
|Konfigurera arbetsflödesanvändare, anger hur användarna får meddeladen och skapa nya arbetsflöden. Implementera nödvändiga arbetsflödeselement genom att anpassa programkoden för nya arbetsflöden i scenarier som inte stöds.|[Konfigurera arbetsflöden](across-set-up-workflows.md)|  
|Aktivera arbetsflöden, agera på arbetsflödemeddelanden inklusive begärandegodkännanden och godkänn begäranden för att utföra ett arbetsflödessteg. Arkivera och ta bort arbetsflöden.|[Använd arbetsflöden](across-use-workflows.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Hantera projekt](projects-manage-projects.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate-flöden](across-how-use-financials-data-source-flow.md)  
[Felsöka automatiserade arbetsflöden i [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]