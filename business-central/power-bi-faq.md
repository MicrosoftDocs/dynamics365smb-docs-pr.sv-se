---
title: Power BI Vanliga frågor och svar
description: Få svar på några vanliga frågor om att arbeta med Power BI och Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, reports, faq, errors
ms.date: 04/22/2021
ms.author: jswymer
ms.openlocfilehash: 939b280e631113d3196f6fbbc90d9bf19b9fc408
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025839"
---
# <a name="power-bi--faq"></a>Power BI Vanliga frågor och svar

I den här artikeln besvaras några frågor som du kanske har kring arbetet med Power BI och [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[Allmänt](#tab/general)
<!-- 26 -->
### <a name="ive-selected-a-report-for-my-role-center-in-business-central-if-i-later-make-changes-to-the-reports-visuals-online-will-the-role-center-automatically-update-to-my-changes"></a>Jag har valt en rapport för mitt rollcenter i Business Central. Kommer rollcentret automatiskt att uppdateras till mina ändringar om jag senare gör ändringar i rapportens visuella effekter?

Ja, eftersom rapporterna är inbäddade från Power BI.

<!-- 3 -->
### <a name="are-the-business-central-apps-for-power-bi-available-in-languages-other-than-english"></a>Finns det Business Central-appar för Power BI tillgängliga på andra språk än engelska?

Nr De här apparna finns för närvarande bara på engelska.

<!-- 24 -->
### <a name="once-a-report-is-published-on-mypowerbicomworkspace-can-i-download-its-pbix"></a>När en rapport har publicerats på min powerbi.com-arbetsyta kan jag hämta dess pbix? 

Ja. Mer information finns i [Hämta en rapport från Power BI-tjänsten till Power BI Desktop](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### <a name="can-i-download-the-apps-as-pbix-files"></a>Kan jag ladda ned apparna som pbix-filer? 

Nr För närvarande erbjuder vi inte hämtning av pbix-filer för de officiella Power BI-apparna, eftersom de publiceras på AppSource.

## <a name="license"></a>[Licens](#tab/license)

<!-- 14 -->
### <a name="do-i-need-a-power-bi-pro-license-to-publish-reports"></a>Behöver jag en Power BI Pro-licens för att publicera rapporter? 

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Nr En Pro-licens behövs inte för att publicera rapporter. Standardlicensen (gratis) för Power BI är tillräcklig. Mer information finns i [Power BI-licensiering](admin-powerbi-setup.md#license).

<!-- 15 -->
### <a name="is-there-anything-i-cant-do-with-the-free-license"></a>Finns det något jag inte kan göra med en gratis licens?

Du kan inte dela rapporter eller installera Business Central-apparna för Power BI. Med den kostnadsfria licensen kan du skapa nästan alla varianter av diagram och rapporter.

<!-- 16 -->
### <a name="if-someone-shares-a-report-with-another-person-then-that-person-needs-a-pro-license-to-see-the-report-are-there-plans-to-make-this-capability-possible-with-the-free-license"></a>Om någon delar en rapport med en annan person behöver personen en Pro-licens för att se rapporten. Finns det några planer på att göra detta möjligt med den kostnadsfria licensen?

Vi har inte kontroll över detta krav. Det här kravet anges av Power BI. Mer information finns i [Dela Power BI-instrumentpaneler och -rapporter med kollegor och andra](/power-bi/collaborate-share/service-share-dashboards).  

## <a name="designer"></a>[Designer](#tab/designer)

<!-- 7 -->
### <a name="does-the-connector-work-with-api-pages"></a>Fungerar anslutaren med API-sidor?

Inte ännu. Från och med juni 2021 kommer den nya Power BI-anslutningen att stödja både Business Centrals webbtjänster och API-sidor. Mer information finns i [Aktivera Power BI-anslutning för att arbeta med API:er för Business Central, i stället för med webbtjänster](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

<!-- 11 --> 
### <a name="is-it-possible-to-choose-which-business-central-environment-to-get-data-from-for-power-bi-for-example-like-a-sandbox-or-production-environment"></a>Är det möjligt att välja vilken Business Central-miljö som data ska hämtas från för Power BI, till exempel i en sandlåde- eller produktionsmiljö? 

Ja. Det kan vara lätt att välja. När du ansluter till Business Central via kopplingen måste du välja miljö och företagsnamn.

<!-- 6 --> 
### <a name="can-i-merge-data-from-several-production-environments-of-the-same-tenant"></a>Kan jag slå samman data från flera produktionsmiljöer med samma klientorganisation?

Ja. I Power BI kör du bara datadriften igen och väljer den miljö du vill använda.

<!-- 25 -->
### <a name="which-pages-in-business-central-have-the-power-bi-report-part"></a>Vilka sidor i Business Central har Power BI-rapportdelen?  

För närvarande finns det några sidor med en faktabox som innehåller en del med **Power BI-rapporter** om hur rapporten visas. 

På listsidor är delen **Power BI-rapporter** filtrerad så att den visar rapporter som hör till data i listan. Det här är listtypsidorna som innehåller delen **Power BI-rapporter**:

|Sid-ID|Name|
|-------|----|
|22|Kundlista|
|27|Leverantörslista|
|31|Artikellista|
|9305|Lista över försäljningsorder|
|9308|Inköpsfakturor|

Det här är andra sidor som innehåller den större, icke-filtrerade delen **Power BI-rapporter**:

|Sid-ID|Name|
|-------|----|
|1156|Företagsdetaljer|
|4013|Insikter för intelligent moln |
|9006|Rollcentret för orderhandläggare|
|9008|Dist.lager. Grundläggande rollcenter|
|9010|Rollcenter för produktionsplanerare|
|9015|Rollcenter för projektledare|
|9016|Rollcenter för serviceavsändare|
|9022|Rollcenter för chef|
|9024|Rollcenter för säkerhetsadministratör|
|9026|Hanterare av försäljning och relationer. ROLLCENTER|
|9027|Rollcentret Revisor|

> [!TIP]
> Det finns inga planer på att lägga till det på alla listsidor just nu. Du kan emellertid skapa ett enkelt sidtillägg som lägger till **Power BI-rapporter**-delen i en faktabox. Mer information finns i [Lägga till Power BI-rapportdelar på sidor](/dynamics365/business-central/dev-itpro/developer/devenv-power-bi-report-parts) i hjälpen för utvecklare och IT-proffs.

<!-- 5 -->
### <a name="is-there-any-way-to-filter-a-dataset-from-business-central-before-i-pull-it-into-power-bi-instead-of-applying-filters-afterwards"></a>Finns det något sätt att filtrera en datauppsättning från Business Central *innan* jag hämtar den till Power BI, i stället för att använda filtren efteråt?

Om du vill filtrera större datauppsättningar är det enklaste sättet att ange ett filter i Power BI-rapporten genom att direkt redigera Power Query-formeln. De flesta filter som du anger på det här sättet överförs till Business Central via frågevikning. Se [stegvis uppdatering för datauppsättningar](/power-bi/admin/service-premium-incremental-refresh).

Det finns för närvarande inget sätt att ställa in ett filter för webbtjänstdata från Business Central. Om programmet måste definiera ett filter inom Business Central måste du skapa en anpassad Business Central-app för det här ändamålet.

<!-- 8 and 9 -->

### <a name="for-embedding-reports-in-business-central-pages-right-now-its-only-possible-to-get-reports-from-my-workspace-in-power-bi-are-there-plans-to-make-it-possible-to-get-them-from-custom-workspaces"></a>När du bäddar in rapporter på Business Central-sidor går det bara att hämta rapporter från *Min arbetsyta* i Power BI. Finns det några planer på att göra det möjligt att få dem från anpassade arbetsytor?

Ja. Vi har planer på att lägga till stöd för delade arbetsytor, men det finns ännu ingen tidslinje tillgänglig.  

<!-- 10 -->
### <a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table"></a>Från Power BI, förutom att använda en fråga, finns det något annat sätt att hämta data från Business Central-tabeller som inte har en kopplad sida? Det kan till exempel vara tabellen *Mappning av värde på artikelattribut*.

Nr Inte just nu.

<!-- 12 --> 
### <a name="are-published-queries-faster-to-use-than-published-pages"></a>Går det snabbare att använda publicerade frågor än publicerade sidor?

När det kommer till webbtjänster är publicerade frågor oftast snabbare än motsvarande publicerade sidor. Orsaken är att frågorna har optimerats för att läsa data och inte innehåller dyra utlösare som OnAfterGetRecord.

När den nya kopplingen är tillgänglig i juni 2021 rekommenderas du att använda API-sidor över frågor som publicerats som webbtjänster.

<!-- 13 --> 
### <a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-developer-have-to-create-a-custom-query"></a>Finns det ett sätt för en slutanvändare att skapa en webbtjänst med en kolumn i en Business Central-tabell, men inte en sida? Eller måste utvecklare skapa en anpassad fråga? 

Inte ännu. När den nya kopplingen är tillgänglig i juni 2021 kan en utvecklare skapa en ny API-sida som uppfyller detta krav. 

<!-- 28 --> 
### <a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online"></a>Kan jag ansluta Power BI till en skrivskyddad databasserver på Business Central Online? 

Nr Men vi har denna funktion i vår långsiktiga plan. 

## <a name="performance"></a>[Prestanda](#tab/performance)

<!-- 17 -->

### <a name="is-it-faster-to-get-data-using-api-pages-than-using-web-services"></a>Går det snabbare att hämta data med hjälp av API-sidor än webbtjänster?

Ja. Våra tester tyder på att API-sidorna har upp till 25 % högre prestanda än webbtjänster.

<!-- 18 -->
### <a name="are-there-plans-to-have-a-mirror-on-the-azure-sql-database-instance-which-i-can-connect-to-directly"></a>Finns det planer på att ha en spegling på Azure SQL Database-instansen, som jag kan ansluta till direkt?

Nr Inte just nu. Du kan bara kommunicera med Business Central via API:er.

<!-- 19 -->
### <a name="loading-data-from-business-central-web-services-seems-slow-is-there-any-way-to-get-data-directly-from-the-sql-database-table"></a>Datainläsning från Business Centrals webbtjänster verkar vara långsamma. Finns det något sätt att hämta data direkt från SQL Database-tabellen?

Nr Det går inte att direkt komma åt databasen, men om du växlar till API-sidor (när den nya anslutningen är tillgänglig) blir det mycket enklare.

## <a name="advanced"></a>[Avancerat](#tab/advanced)
<!-- 1 -->

### <a name="are-there-plans-for-the-power-bi-connector-to-support-the-incremental-refresh-features-in-the-power-bi-service"></a>Finns det planer för Power BI-anslutningen för att stödja de inkrementella uppdateringsfunktionerna i Power BI-tjänsten?

Ja. Det finns i vår plan.

<!-- 2 -->
### <a name="if-a-business-central-on-premises-solution-doesnt-have-internet-access-can-i-still-use-power-bi"></a>Om en lokal Business Central-lösning inte har tillgång till Internet, kan jag fortfarande använda Power BI?
<!-- todo: please explain this one-->

Ja. I det här fallet använder du Power BI Desktop lokalt och ansluter till den lokala installationen av Business Central. När du är ansluten kan du skapa och visa rapporter, men du kan inte publicera dem till Power BI-tjänsten. 
<!-- 20 -->
### <a name="are-there-any-plans-to-make-it-possible-to-replicate-business-central-online-databases-so-theyre-accessible-for-read-only-sql-queries-this-capability-would-support-incremental-refresh-and-be-a-lot-faster-than-apis-or-web-services"></a>Finns det några planer på att göra det möjligt att replikera Business Central Online-databaser så att de är tillgängliga för skrivskyddade SQL-frågor? Denna möjlighet kan stödja inkrementell uppdatering och vara mycket snabbare än API:er eller webbtjänster.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Ja. Vi har denna funktion i vår långsiktiga plan. 

<!-- 21 -->
### <a name="if-i-use-azure-data-factory-to-get-data-from-business-central-and-consume-it-on-power-bi-will-that-help-in-increase-in-performance"></a>Om jag använder Azure Data Factory för att hämta data från Business Central och använder dem på Power BI, bidrar det till att höja prestandan? 

Ja. Det här avancerade scenariot gör att Business Central bibehåller prestandan eftersom dataåtkomsten görs via Azure Data Factory.

<!-- 22 -->
### <a name="are-there-any-plans-to-support-power-bi-deployment-pipelines-or-a-way-to-build-deployment-pipelines-for-pbi-reports-similar-to-extensions-or-maybe-even-a-simple-api-in-the-business-admin-center"></a>Finns det några planer på att stödja Power BI-distribution eller ett sätt att bygga distributionsledningar för PBI-rapporter, ungefär som tillägg? Eller kanske till och med ett enkelt API i Business Admin Center? 

Vi undersöker den här funktionen. Power BI innehåller många API:er som styr rapportdistributioner. Mer information finns i [Introduktion till distributionsledningar](/power-bi/create-reports/deployment-pipelines-overview).

### <a name="ive-tried-the-preview-of-the-new-connector-which-will-be-live-in-june-2021-i-see-some-values-like-_x0020_-when-connecting-to-api-v20-what-are-these-values"></a>Jag provade förhandsversionen av den nya kontakten, som lanseras i juni 2021. Jag ser vissa värden som "_x0020_" vid anslutning till API v2.0. Vilka är dessa värden?

Med den kommande versionen av Power BI-anslutningen kan du ansluta till Business Central API-sidorna, inklusive API v2.0. Dessa sidor innehåller några fält som baseras på [Al Enum-objekt](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Fält som baseras på AL Enum-objekt måste ha namn som är konsekventa och alltid samma, så att filter i rapporten alltid fungerar&mdash;oavsett vilket språk eller operativsystem du använder. Därför är inte fälten som baseras på AL Enum översatta och kodade för att undvika specialtecken, inklusive blanksteg. När det inte finns ett tomt alternativ i det AL-Enum-objektet kodas det till "_x0020_". Du kan alltid använda en omvandling till data på Power BI om du vill visa olika värden för dessa fält, t. ex. "Tomt".


---

## <a name="see-also"></a>Se även

[Power BI-licensiering](admin-powerbi-setup.md#license)
[Introduktion till Business Central och Power BI](admin-powerbi.md)  
[Översikt över Power BI-integrering](admin-powerbi-overview.md)  
[Aktivera Power BI i Business Central](admin-powerbi-setup.md)  
[Arbeta med Power BI-rapporter i Business Central](across-working-with-powerbi.md)  
[Arbeta med Business Central-data i Power BI](across-working-with-business-central-in-powerbi.md)  
[Skapa Power BI-rapporter för att visa Business Central-data](across-how-use-financials-data-source-powerbi.md)    
[Dokumentation om Power BI](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]