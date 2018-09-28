---
title: Administrativa uppgifter i Business Central | Microsoft Docs
description: "Vissa uppgifter i Business Central kräver central administrering och konfigurering. Se vad de är och lär dig vad du ska göra."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: c1675921c82ddf00f6a00f94bb38bd594a9a0089
ms.contentlocale: sv-se
ms.lasthandoff: 06/28/2018

---
# <a name="administration"></a>Administration
Central administration utförs vanligtvis av en roll i företaget. Omfattningen av dessa uppgifter kan vara beroende av företagets storlek och administratörens ansvarsområden. Dessa uppgifter kan omfatta att hantera databassynkronisering av projekt och e-postköer, konfigurera användare och anpassa användargränssnittet.  

Det är viktigt att ange rätt inställningsvärden från början för att en ny verksamhetsprogramvara ska fungera effektivt. [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett antal assisterade installationer som hjälper dig att ställa in grundläggande information. Mer information finns i [Ställa in Business Central](setup.md).

Om du använder RapidStart Services för att implementera inställningsvärden, eller om du skriver in dem i det nya företaget manuellt, kan du stärka hantera dina inställningsalternativ med allmänna rekommendationer för valda inställningsfält som är kända för att eventuellt göra lösningen ineffektiv om den definierats felaktigt.  

En superanvändare eller administratör kan konfigurera ramverket för datautbyte så att användare kan exportera och importera data i bank- och lönesystemfiler, till exempel för olika processer av likviditetsstyrning.

> [!NOTE]
> Du kan skapa ett nytt företag i [!INCLUDE[d365fin](includes/d365fin_md.md)] med RapidStart Services, som är ett verktyg som har utformats för att förkorta distributionstider, förbättra kvaliteten på implementeringen, införa en upprepningsbar metod vid implementeringar, samt öka produktiviteten genom att automatisera och underlätta återkommande uppgifter. Mer information finns i # # [Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Lägg till användargrupper och hantera behörigheter, åtkomst till data, tilldela roller.|[Förstå profiler och rollcenter](admin-users-profiles-roles.md)|  
|Tilldela behörigheter till användare, ändra behörighetsgrupper och gruppera användare per behörigheter.|[Hantera användare och behörigheter](ui-how-users-permissions.md)|
|Klassificera datakänslighetsnivåer för fält så att du kan svara på begäranden från datasubjekt som rör deras personuppgifter.|[Klassificera datakänslighet](admin-classifying-data-sensitivity.md)|
|Svara på begäranden från datasubjekt som berör deras personuppgifter.|[Svara på begäranden om personuppgifter](admin-responding-to-requests-about-personal-data.md)|
|Skapa en ny affärsenhet med hjälp av mallar|[Skapa nya företag](about-new-company.md)|
|Ändra vilka fält och åtgärder som visas i användargränssnittet så att de passar företagets affärsprocesser. |[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md) |
|Spåra alla direkta ändringar som användarna gör av data i databasen för att kunna identifiera var fel och dataändringar härrör från.|[Logga ändringar](across-log-changes.md)|  
|Ange enstaka eller återkommande begäranden om att köra rapporter eller kodenheter.|[Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)|  
|Hantera, ta bort eller komprimera dokument|[Ta bort dokument](admin-manage-documents.md)|  
|Visa sidor, kodenheter och frågor som webbtjänster.|[Publicera en webbtjänst](across-how-publish-web-service.md)|
|Som en del av att skapa Connect-appar mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och 3:e partens tillverkarlösningar via REST API:er, definiera mallar som används för att fylla i tomma egenskaper på en enhet när du skapar en POST-åtgärd genom API.|[Konfigurera API-mallar](admin-configuring-api-template.md)|

## <a name="see-also"></a>Se även
[Affärsfunktion](across-business-functionality.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Komma igång](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

