---
title: Administrativa uppgifter i Business Central | Microsoft Docs
description: Vissa uppgifter i Business Central kräver central administrering och konfigurering. Se vad de är och lär dig vad du ska göra.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/22/2019
ms.author: edupont
ms.openlocfilehash: 41917ece38cf553582438d7c57ca3e09b82b21e9
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796717"
---
# <a name="administration"></a>Administration
Central administration utförs vanligtvis av en roll i företaget. Omfattningen av dessa uppgifter kan vara beroende av företagets storlek och administratörens ansvarsområden. Dessa uppgifter kan omfatta att hantera databassynkronisering av projekt och e-postköer, konfigurera användare och anpassa användargränssnittet.  

Det är viktigt att ange rätt inställningsvärden från början för att en ny verksamhetsprogramvara ska fungera effektivt. [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett antal assisterade installationer som hjälper dig att ställa in grundläggande information. Mer information finns i [Ställa in Business Central](setup.md).

Om du använder RapidStart Services för att implementera inställningsvärden, eller du skriver in dem i fältet nytt företag manuellt, kan du hantera dina inställningsalternativ med de allmänna rekommendationerna för valda inställningsfält som är kända att eventuellt göra lösningen ineffektiv om den definierats felaktigt.  

En superanvändare eller administratör kan konfigurera ramverket för datautbyte så att användare kan exportera och importera data i bank- och lönesystemfiler, till exempel för olika processer av likviditetsstyrning.

> [!NOTE]
> Du kan skapa ett nytt företag i [!INCLUDE[d365fin](includes/d365fin_md.md)] med RapidStart Services som är ett verktyg som har utformats för att förkorta distributiontider, förbättra kvalitet på implementeringen, införa en metod med upprepning vid implementeringar och öka produktiviteten genom att automatisera och underlätta återkommande uppgifter. Mer information finns i [Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Lägg till användargrupper och hantera behörigheter, åtkomst till data, tilldela roller.|[Förstå profiler (roller) och rollcenter](admin-users-profiles-roles.md)|  
|Tilldela behörigheter till användare, ändra behörighetsgrupper och gruppera användare per behörigheter.|[Hantera användare och behörigheter](ui-how-users-permissions.md)|
|Klassificera datakänslighetsnivåer för fält så att du kan svara på begäranden från datasubjekt som rör deras personuppgifter.|[Klassificera datakänslighet](admin-classifying-data-sensitivity.md)|
|Svara på begäranden från datasubjekt som berör deras personuppgifter.|[Svara på begäranden om personuppgifter](admin-responding-to-requests-about-personal-data.md)|
|Skapa en ny affärsenhet med hjälp av mallar|[Skapa nya företag](about-new-company.md)|
|Spåra alla direkta ändringar som användarna gör av data i databasen för att kunna identifiera var fel och dataändringar härrör från.|[Logga ändringar](across-log-changes.md)|  
|Ange enstaka eller återkommande begäranden om att köra rapporter eller kodenheter.|[Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)|  
|Hantera, ta bort eller komprimera dokument|[Ta bort dokument](admin-manage-documents.md)|  
|Visa sidor, kodenheter och frågor som webbtjänster.|[Publicera en webbtjänst](across-how-publish-web-service.md)|
|Som en del av att skapa Connect-appar mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och 3:e partens tillverkarlösningar via REST API, definiera mallar som används för att fylla i tomma egenskaper på en enhet när du skapar en POST-åtgärd genom API.|[Konfigurera API-mallar](admin-configuring-api-template.md)|
|Kryptera data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-server genom att skapa nya eller importera befintliga krypteringsnycklar som du aktiverar på servern.|[Hantera datakryptering](admin-manage-data-encryption.md)|
|Ansluta Dynamics 365 for Sales med [!INCLUDE[d365fin](includes/d365fin_md.md)] för att erhålla integreringen mellan kundrelationer och orderbehandling i processen från kundämne till betalning.|[Integrera med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Ändra vilka fält och åtgärder som visas i användargränssnittet så att de passar företagets affärsprocesser och utöka lösningen med appar.|[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)|

## <a name="see-also"></a>Se även
[Affärsfunktion](across-business-functionality.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Komma igång](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
