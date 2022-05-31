---
title: Administrationsuppgifter i Business Central
description: Vissa uppgifter i Business Central kräver central administrering och konfigurering. Se vad de är och lär dig vad du ska göra.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/23/2021
ms.author: edupont
ms.openlocfilehash: 4995a1776beacd444912124da5e9e6315f6a22f8
ms.sourcegitcommit: 4853614c85beb347091c5c4c1ea8d974dec887fc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740211"
---
# <a name="administration-tasks"></a>Administrationsuppgifter

Central administration utförs vanligtvis av en roll i företaget. Omfattningen av dessa uppgifter kan vara beroende av företagets storlek och administratörens ansvarsområden. Dessa uppgifter kan omfatta att hantera databassynkronisering av projekt och e-postköer, konfigurera användare och anpassa användargränssnittet.  

Det är viktigt att ange rätt inställningsvärden från början för att en ny verksamhetsprogramvara ska fungera effektivt. [!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett antal assisterade installationer som hjälper dig att ställa in grundläggande information. Mer information finns i [Ställa in Business Central](setup.md).

> [!NOTE]
> Du kan använda migreringsverktyg för data för att migrera befintliga data till [!INCLUDE [prod_short](includes/prod_short.md)] online. Alternativt kan du skapa ett nytt företag i [!INCLUDE[prod_short](includes/prod_short.md)] med konfigurationspaket för att förkorta distributionstider, förbättra kvaliteten på implenteringen, införa en metod för implementeringar som går att upprepa samt förbättra produktiviteten genom att automatisera och förenkla återkommande uppgifter. Mer information finns i [Migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data).

Du kan ge stöd åt dina inställningsbeslut med några allmänna rekommendationer för valda inställningsfält som eventuellt orsakar att lösningen är ineffektiv, om fältet är felaktigt inställt.  

En superanvändare eller administratör kan konfigurera ramverket för datautbyte så att användare kan exportera och importera data i bank- och lönesystemfiler, till exempel för olika processer av likviditetsstyrning. Mer information finns i [Utbyta data elektroniskt](across-data-exchange.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de artiklar där de beskrivs.  

|**Om du vill**|**Se**|  
|------------|-------------|
|Ange vem som kan logga in på [!INCLUDE[prod_short](includes/prod_short.md)] genom att skapa användare i administrationscentret för Microsoft 365 enligt produktlicenserna.|[Skapa användare enligt licenser](ui-how-users-permissions.md)|
|Tilldela behörigheter till användare, ändra behörighetsuppsättningar och gruppera användare för enkel behörighetshantering.|[Tilldela behörigheter till användare och grupper](ui-how-users-permissions.md)|
|Lägg till användargrupper och hantera behörigheter, åtkomst till data, tilldela roller.|[Hantera profiler](admin-users-profiles-roles.md)|
|Hantera användarinställningar, till exempel företag, roll, språk, region och tidszon.|[Användarinställningar](admin-manage-user-settings-preferences.md)|
|Ställa in skrivare och ange vilka rapporter som ska skrivas ut på vilka skrivare.|[Ställa in skrivare](ui-specify-printer-selection-reports.md)|
|Klassificera datakänslighetsnivåer för fält så att du kan svara på begäranden från datasubjekt som rör deras personuppgifter.|[Klassificera datakänslighet](admin-classifying-data-sensitivity.md)|
|Svara på begäranden från datasubjekt som berör deras personuppgifter.|[Svara på begäranden om personuppgifter](admin-responding-to-requests-about-personal-data.md)|
|Skapa en ny affärsenhet med hjälp av mallar|[Skapa nytt företag](about-new-company.md)|
|Spåra alla direkta ändringar som användarna gör av data i databasen för att kunna identifiera var fel och dataändringar härrör från.|[Logga ändringar](across-log-changes.md)|  
|Ange enstaka eller återkommande begäranden om att köra rapporter eller kodenheter.|[Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)|  
|Hantera, ta bort eller komprimera dokument|[Ta bort dokument](admin-manage-documents.md)|  
|Visa sidor, kodenheter och frågor som webbtjänster.|[Publicera en webbtjänst](across-how-publish-web-service.md)|
|Som en del av att skapa Connect Apps mellan [!INCLUDE[prod_short](includes/prod_short.md)] och tredjepartslösningar via REST API:er, definiera mallar som används för att fylla i tomma egenskaper på en entitet när du skapar en POST-åtgärd genom API.|[Konfigurera API-mallar](admin-configuring-api-template.md)|
|Kryptera data i [!INCLUDE[prod_short](includes/prod_short.md)]-server genom att skapa nya eller importera befintliga krypteringsnycklar som du aktiverar på servern.|[Hantera datakryptering](admin-manage-data-encryption.md)|
|Ansluta Dynamics 365 Sales med [!INCLUDE[prod_short](includes/prod_short.md)] för att erhålla integreringen mellan kundrelationer och orderbehandling i processen från kundämne till betalning.|[Integrera med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Ändra vilka fält och åtgärder som visas i användargränssnittet så att de passar företagets affärsprocesser och utöka lösningen med appar.|[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|

## <a name="administration-in-the-admin-center"></a>Administration i administrationscentret

Interna och delegerade administratörer har tillgång till administrationscentret för [!INCLUDE [prod_short](includes/prod_short.md)] där de kan konfigurera, övervaka och felsöka [!INCLUDE [prod_short](includes/prod_short.md)]-miljöer. I följande register beskrivs vissa huvuduppgifter, med länkar till respektive beskrivande artikel.  

|**Om du vill**|**Se**|  
|------------|-------------|
|Lär dig mer om de verktyg som du kan använda för att felsöka.|[Teknisk support](/dynamics365/business-central/dev-itpro/technical-support)|
|Övervaka användning och felsök sessioner|[Miljötelemetri i Business Central administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Hantera användarsessioner, inklusive att avbryta en session om användaren är blockerad.|[Hantera sessioner](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions)|
|Konfigurera klientorganisationen så att den skickar telemetriska data till Azure Application Insights för bättre analys och fel sökning.|[Aktivera Skicka telemetri till Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights)|

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Affärsfunktion](across-business-functionality.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]