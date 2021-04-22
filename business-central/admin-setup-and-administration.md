---
title: Administrativa uppgifter i Business Central | Microsoft Docs
description: Vissa uppgifter i Business Central kräver central administrering och konfigurering. Se vad de är och lär dig vad du ska göra.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 13f713756fc1f771243686c549c22f3ce0974b6b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777222"
---
# <a name="administration"></a>Administration

Central administration utförs vanligtvis av en roll i företaget. Omfattningen av dessa uppgifter kan vara beroende av företagets storlek och administratörens ansvarsområden. Dessa uppgifter kan omfatta att hantera databassynkronisering av projekt och e-postköer, konfigurera användare och anpassa användargränssnittet.  

Det är viktigt att ange rätt inställningsvärden från början för att en ny verksamhetsprogramvara ska fungera effektivt. [!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett antal assisterade installationer som hjälper dig att ställa in grundläggande information. Mer information finns i [Ställa in Business Central](setup.md).

Om du använder RapidStart Services för att implementera inställningsvärden, eller du skriver in dem i fältet nytt företag manuellt, kan du hantera dina inställningsalternativ med de allmänna rekommendationerna för valda inställningsfält som är kända att eventuellt göra lösningen ineffektiv om den definierats felaktigt.  

En superanvändare eller administratör kan konfigurera ramverket för datautbyte så att användare kan exportera och importera data i bank- och lönesystemfiler, till exempel för olika processer av likviditetsstyrning. Mer information finns i [Utbyta data elektroniskt](across-data-exchange.md).

> [!NOTE]
> Du kan skapa ett nytt företag i [!INCLUDE[prod_short](includes/prod_short.md)] med RapidStart Services som är ett verktyg som har utformats för att förkorta distributiontider, förbättra kvalitet på implementeringen, införa en metod med upprepning vid implementeringar och öka produktiviteten genom att automatisera och underlätta återkommande uppgifter. Mer information finns i [Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**Om du vill**|**Se**|  
|------------|-------------|  
|Ange vem som kan logga in på [!INCLUDE[prod_short](includes/prod_short.md)] genom att skapa användare i Microsoft 365 administrationscenter enligt produktlicenserna.|[Skapa användare enligt licenser](ui-how-users-permissions.md)|
|Tilldela behörigheter till användare, ändra behörighetsuppsättningar och gruppera användare för enkel behörighetshantering.|[Tilldela behörigheter till användare och grupper](ui-how-users-permissions.md)|
|Lägg till användargrupper och hantera behörigheter, åtkomst till data, tilldela roller.|[Hantera profiler](admin-users-profiles-roles.md)|
|Hantera användarinställningar, till exempel företag, roll, språk, region och tidszon.|[Användarinställningar](admin-manage-user-settings-preferences.md)|
|Ställa in skrivare och ange vilka rapporter som ska skrivas ut på vilka skrivare.|[Ställa in skrivare](ui-specify-printer-selection-reports.md)|
|Klassificera datakänslighetsnivåer för fält så att du kan svara på begäranden från datasubjekt som rör deras personuppgifter.|[Klassificera datakänslighet](admin-classifying-data-sensitivity.md)|
|Svara på begäranden från datasubjekt som berör deras personuppgifter.|[Svara på begäranden om personuppgifter](admin-responding-to-requests-about-personal-data.md)|
|Skapa en ny affärsenhet med hjälp av mallar|[Skapa nya företag](about-new-company.md)|
|Spåra alla direkta ändringar som användarna gör av data i databasen för att kunna identifiera var fel och dataändringar härrör från.|[Logga ändringar](across-log-changes.md)|  
|Ange enstaka eller återkommande begäranden om att köra rapporter eller kodenheter.|[Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)|  
|Hantera, ta bort eller komprimera dokument|[Ta bort dokument](admin-manage-documents.md)|  
|Visa sidor, kodenheter och frågor som webbtjänster.|[Publicera en webbtjänst](across-how-publish-web-service.md)|
|Som en del av att skapa Connect Apps mellan [!INCLUDE[prod_short](includes/prod_short.md)] och tredjepartslösningar via REST API:er, definiera mallar som används för att fylla i tomma egenskaper på en entitet när du skapar en POST-åtgärd genom API.|[Konfigurera API-mallar](admin-configuring-api-template.md)|
|Kryptera data i [!INCLUDE[prod_short](includes/prod_short.md)]-server genom att skapa nya eller importera befintliga krypteringsnycklar som du aktiverar på servern.|[Hantera datakryptering](admin-manage-data-encryption.md)|
|Ansluta Dynamics 365 Sales med [!INCLUDE[prod_short](includes/prod_short.md)] för att erhålla integreringen mellan kundrelationer och orderbehandling i processen från kundämne till betalning.|[Integrering med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Ändra vilka fält och åtgärder som visas i användargränssnittet så att de passar företagets affärsprocesser och utöka lösningen med appar.|[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|
|Övervaka användning och felsök sessioner.|[Miljötelemetri i Business Central administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Hantera användarsessioner, inklusive att avbryta en session om användaren är blockerad.|[Hantera sessioner](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions)|  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Affärsfunktion](across-business-functionality.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]