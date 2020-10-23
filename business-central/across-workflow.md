---
title: Arbetsflöden | Microsoft Docs
description: Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1685ca2ab698cad1b1c7a84f65b5633d1234624b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927253"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Arbetsflöden i Dynamics 365 Business Central

Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.  

 På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.  

 Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett antal förkonfigurerade arbetsflöden som representeras av arbetsflödesmallar som du kan kopiera för att skapa arbetsflöden. Koden för arbetsflödesmallar som läggs till av Microsoft har prefixet ”MS-”. Mer information finns i listan över arbetsflödesmallar på sidan Arbetsflödesmallar.  

 Om ett företagsscenario kräver en arbetsflödehändelse eller ett svar som inte stöds kan du antingen använda Power Automate eller arbeta med en Microsoft-partner för att anpassa applikationskoden. Mer information finns i [Använda [!INCLUDE[prodshort](includes/prodshort.md)] i ett automatiskt arbetsflöde](across-how-use-financials-data-source-flow.md).

Alla arbetsflödesmallar som du skapar med Power Automate läggs till i listan över arbetsflödesmallar i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Använda Business Central i ett automatiskt arbetsflöde ](across-how-use-financials-data-source-flow.md).  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**För att**|**Gå till**|  
|------------|-------------|  
|Konfigurera arbetsflödesanvändare, anger hur användarna får meddeladen och skapa nya arbetsflöden. Implementera nödvändiga arbetsflödeselement genom att anpassa programkoden för nya arbetsflöden i scenarier som inte stöds.|[Konfigurera arbetsflöden](across-set-up-workflows.md)|  
|Aktivera arbetsflöden, agera på arbetsflödemeddelanden inklusive begärandegodkännanden och godkänn begäranden för att utföra ett arbetsflödessteg. Arkivera och ta bort arbetsflöden.|[Använda arbetsflöden](across-use-workflows.md)|  

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Hantera projekt](projects-manage-projects.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
