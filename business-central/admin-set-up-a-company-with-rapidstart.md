---
title: Konfigurera ett företag med RapidStart Services
description: Du kan skapa ett nytt företag i Business Central med RapidStart Services för att öka produktiviteten genom att automatisera och förenkla återkommande uppgifter.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 8610, 8614, 8615, 8620, 8632
ms.date: 03/28/2022
ms.author: edupont
ms.openlocfilehash: b2d3378e9c06221bc91977883a53bba8514c6afc
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518317"
---
# <a name="set-up-a-company-with-rapidstart-services"></a>Konfigurera ett företag med RapidStart Services

Du kan skapa ett nytt företag i [!INCLUDE[prod_short](includes/prod_short.md)] med RapidStart Services som är ett verktyg som har utformats för att förkorta distributiontider, förbättra kvalitet på implementeringen, införa en metod med upprepning vid implementeringar och öka produktiviteten genom att automatisera och underlätta återkommande uppgifter.  

Med dessa funktioner kan du skala företaget som en återförsäljare. De flesta relevanta sidorna gäller både [!INCLUDE [prod_short](includes/prod_short.md)] online och lokalt. Vissa processer är emellertid beroende av åtkomst till filer på disken och är för komplicerade för att användas för [!INCLUDE [prod_short](includes/prod_short.md)] online. För [!INCLUDE [prod_short](includes/prod_short.md)] lokalt vill du förmodligen använda Windows PowerShell för distributionen. Mer information finns i avsnitten [Administration av Business Central lokalt](/dynamics365/business-central/dev-itpro/administration/administration) respektive [Administration av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).  

Med hjälp av RapidStart Services får du en översikt över processen i ditt nya företag genom att tillhandahålla ett formulär där du kan lägga upp tabeller som ofta används i konfigurationer av nya företag. När du gör detta kan du skapa ett frågeformulär som hjälper dina kunder genom att samla in information om inställningar. Kunderna får valet att använda frågeformuläret för att skapa moduler eller öppna sidan med inställningar direkt och göra inställningarna där. Och viktigast av allt: RapidStart Services hjälper dig som kund att förbereda företag med standardinställningsdata som du kan finjustera och anpassa. Slutligen, när du använder RapidStart Services, kan du konfigurera och migrera befintliga kunddata som till exempel en lista över kunder och artiklar till det nya företaget.

Du kan använda följande komponenter för att snabba på inställningen av ditt företag:  

- Konfigurationsguide  
- Konfigurationskalkylark  
- Konfigurationspaket  
- Konfigurationsmallar  
- Konfigurationfrågeformulär  

> [!Note]  
> Det finns delar av [!INCLUDE[prod_short](includes/prod_short.md)] som måste ställas in manuellt. Dessa omfattar att lägga till användare, lägga upp bokföringsperioder och ställa in enhetskoder för affärsstöd. Mer information finns i [Skapa [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

|**Om du vill**|**Se**|  
|------------|-------------|  
|Skapa ett nytt företag och importera grundläggande inställningsdata och mallar.|[Ställa in företagskonfiguration](admin-set-up-company-configuration.md)|  
|Distribuera det konfigurerade paketet till kunden för implementering.|[Koppla konfigurationen till nya företag](admin-apply-configuration-to-new-companies.md)|
|Definiera och validera kundens konfigurationssvärden för alla viktiga områden, till exempel företagsinformation, redovisning, lager, försäljning och produktion.|[Samla in kundinställningsvärden](admin-gather-customer-setup-values.md)|  
|Konfigurera huvuddataposter med mallar för att förbereda migrering av befintliga kunddata.|[Förbereda migrering av kunddata](admin-use-templates-to-prepare-customer-data-for-migration.md)|  
|Definiera tabeller och fält, kontrollera befintliga kunddata och migrerar data i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen.|[Migrera kunddata](admin-migrate-customer-data.md)|
|Förbered återanvändning av företagskonfigurationer i andra företag (i utvecklings- och administrationsinnehåll).|[Skapa anpassade konfigurationspaket för företag](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)|
|Hitta lösningar till kända problem i RapidStart Services-verktyget.|[Tips och råd: RapidStart Services](admin-tips-and-tricks-rapidstart-services.md)|  

## <a name="see-also"></a>Se även

[Administration](admin-setup-and-administration.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Skapa komplexa moduler med hjälp av bästa praxis](set-up-complex-application-areas-using-best-practices.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]