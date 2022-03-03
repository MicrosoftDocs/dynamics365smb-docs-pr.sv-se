---
title: Arbetsflöden i Dynamic 365 Business Central
description: Använd arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemaktiviteter, till exempel automatisk bokföring, kan inkluderas som arbetsflödessteg.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 02f03c3b3423de2b78aea7f4e61c65c968290341
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8130885"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Arbetsflöden i Dynamics 365 Business Central

Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.  

 På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.  

 Den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett antal förkonfigurerade arbetsflöden som representeras av arbetsflödesmallar som du kan kopiera för att skapa arbetsflöden. Koden för arbetsflödesmallar som läggs till av Microsoft har prefixet ”MS-”. Mer information finns i listan över arbetsflödesmallar på sidan Arbetsflödesmallar.  

 Om ett företagsscenario kräver en arbetsflödehändelse eller ett svar som inte stöds kan du antingen använda Power Automate eller arbeta med en Microsoft-partner för att anpassa applikationskoden. Mer information finns i [Använda [!INCLUDE[prod_short](includes/prod_short.md)] i ett automatiskt arbetsflöde](across-how-use-financials-data-source-flow.md).

Alla arbetsflödesmallar som du skapar med Power Automate läggs till i listan över arbetsflödesmallar i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Använda Business Central i ett automatiskt arbetsflöde ](across-how-use-financials-data-source-flow.md).  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**För att**|**Gå till**|  
|------------|-------------|  
|Konfigurera arbetsflödesanvändare, anger hur användarna får meddeladen och skapa nya arbetsflöden. Implementera nödvändiga arbetsflödeselement genom att anpassa programkoden för nya arbetsflöden i scenarier som inte stöds.|[Konfigurera arbetsflöden](across-set-up-workflows.md)|  
|Aktivera arbetsflöden, agera på arbetsflödemeddelanden inklusive begärandegodkännanden och godkänn begäranden för att utföra ett arbetsflödessteg. Arkivera och ta bort arbetsflöden.|[Använda arbetsflöden](across-use-workflows.md)|  

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Hantera projekt](projects-manage-projects.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]