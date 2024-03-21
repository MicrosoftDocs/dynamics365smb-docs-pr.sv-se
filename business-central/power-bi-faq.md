---
title: Power BI Vanliga frågor och svar
description: Få svar på några vanliga frågor om att arbeta med Power BI och Business Central.
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Power BI, reports, faq, errors'
ms.date: 04/22/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Power BI Vanliga frågor och svar

I den här artikeln besvaras några frågor som du kanske har kring arbetet med Power BI och [!INCLUDE [prod_short](includes/prod_short.md)].

## [Allmänt](#tab/general)
<!-- 26 -->
### Jag har valt en rapport för mitt rollcenter i Business Central. Kommer rollcentret automatiskt att uppdateras till mina ändringar om jag senare gör ändringar i rapportens visuella effekter?

Ja, eftersom rapporterna är inbäddade från Power BI.

<!-- 3 -->
### Finns det Business Central-appar för Power BI tillgängliga på andra språk än engelska?

Nej. De här apparna finns för närvarande bara på engelska.

<!-- 24 -->
### När en rapport har publicerats på min powerbi.com-arbetsyta kan jag hämta dess pbix? 

Ja. Mer information finns i [Hämta en rapport från Power BI-tjänsten till Power BI Desktop](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### Kan jag ladda ned apparna som pbix-filer? 

Nej. För närvarande erbjuder vi inte hämtning av pbix-filer för de officiella Power BI-apparna, eftersom de publiceras på AppSource.

## [Licens](#tab/license)

<!-- 14 -->
### Behöver jag en Power BI Pro-licens för att publicera rapporter? 

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Nej. En Pro-licens behövs inte för att publicera rapporter. Standardlicensen (gratis) för Power BI är tillräcklig. Mer information finns i [Power BI-licensiering](admin-powerbi-setup.md#license).

<!-- 15 -->
### Finns det något jag inte kan göra med en gratis licens?

Du kan inte dela rapporter eller installera Business Central-apparna för Power BI. Med den kostnadsfria licensen kan du skapa nästan alla varianter av diagram och rapporter.

<!-- 16 -->
### Om någon delar en rapport med en annan person behöver personen en Pro-licens för att se rapporten. Finns det några planer på att göra detta möjligt med den kostnadsfria licensen?

Vi har inte kontroll över detta krav. Det här kravet anges av Power BI. Mer information finns i [Dela Power BI-instrumentpaneler och -rapporter med kollegor och andra](/power-bi/collaborate-share/service-share-dashboards).  

## [Designer](#tab/designer)

<!-- 7 -->
### Fungerar anslutaren med API-sidor?

Ja. Från och med juni 2021 kommer den nya Power BI-anslutningen att stödja både Business Central webbtjänster och API-sidor. Mer information finns i [Aktivera Power BI-anslutning för att arbeta med API:er för Business Central, i stället för med webbtjänster](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

### Kan jag skapa en Power BI-rapport med hjälp av API-rader för försäljningsfaktura eller journalrader?

De vanligaste radposterna är tillgängliga i [Business Central-API:er v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/). Du kan använda dem för att skapa rapporter Power BI genom att markera dem i **Dynamics 365 Business Central**-kopplingen. Däremot är **rader** API:er avsedda att användas endast med vissa mycket specifika filter, och kanske inte fungerar i ditt scenario. Det kan visas ett fel som liknar "du måste ange ett ID eller ett dokument-ID för att hämta raderna". Lös problemet genom att göra följande när du hämtar data från Business Central för rapporten i Power BI Desktop:

1. I stället för att inkludera datakällan för entiteten rader lägger du till den överordnade datakällan. Lägg till **försäljningsfaktura** i stället för **försäljningsfakturarader**.
2. Välj **omvandla data** i åtgärdsfältet Power BI Desktop.
3. Välj den fråga som du just har lagt till, till exempel **Försäljningsfakturor**.
4. Använd eventuell filtrering på posterna för att minska antalet poster som läses in i rapporten.
5. Bläddra till höger tills du hittar en kolumn som heter som rader, t.ex. **SalesInvoiceLines**.
6. Välj knappen expandera i kolumnens rubrik, bredvid kolumnnamnet.

   :::image type="content" source="media/saleinvoicelines.png" alt-text="Visar kolumnen SalesInvoiceLines i Power BI Desktop.":::
<!-- 11 --> 
### Är det möjligt att välja vilken Business Central-miljö som data ska hämtas från för Power BI, till exempel i en sandlåde- eller produktionsmiljö? 

Ja. Det kan vara lätt att välja. När du ansluter till Business Central via kopplingen måste du välja miljö och företagsnamn.

<!-- 6 --> 
### Kan jag slå samman data från flera produktionsmiljöer med samma klientorganisation?

Ja. I Power BI kör du bara datadriften igen och väljer den miljö du vill använda.

<!-- 25 -->
### Vilka sidor i Business Central har Power BI-rapportdelen?  

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
### Finns det något sätt att filtrera en datauppsättning från Business Central *innan* jag hämtar den till Power BI, i stället för att använda filtren efteråt?

Om du vill filtrera större datauppsättningar är det enklaste sättet att ange ett filter i Power BI-rapporten genom att direkt redigera Power Query-formeln. De flesta filter som du anger på det här sättet överförs till Business Central via frågevikning. Se [stegvis uppdatering för datauppsättningar](/power-bi/admin/service-premium-incremental-refresh).

Det finns för närvarande inget sätt att ställa in ett filter för webbtjänstdata från Business Central. Om programmet måste definiera ett filter inom Business Central måste du skapa en anpassad Business Central-app för det här ändamålet.

<!-- 10 -->
### Från Power BI, förutom att använda en fråga, finns det något annat sätt att hämta data från Business Central-tabeller som inte har en kopplad sida? Det kan till exempel vara tabellen *Mappning av värde på artikelattribut*.

Nej. Inte just nu.

<!-- 12 --> 
### Går det snabbare att använda publicerade frågor än publicerade sidor?

När det kommer till webbtjänster är publicerade frågor oftast snabbare än motsvarande publicerade sidor. Orsaken är att frågorna har optimerats för att läsa data och inte innehåller dyra utlösare som OnAfterGetRecord.

Webbtjänster baseras på sidor eller frågor som har skapats för åtkomst från webben och som vanligtvis inte optimerats för åtkomst från externa tjänster. Även om Business Central-anslutningen fortfarande stöder datahämtning från webbtjänster, rekommenderar vi att du använder API-sidor i stället för webbtjänster när det är möjligt.

<!-- 13 --> 
### Finns det ett sätt för en slutanvändare att skapa en webbtjänst med en kolumn i en Business Central-tabell, men inte en sida? Eller måste utvecklare skapa en anpassad fråga? 

Det finns för närvarande inget sätt att lägga till ett nytt fält i en webbtjänst. API-sidor ger full flexibilitet i sidstrukturen, så en utvecklare kan skapa en ny API-sida som uppfyller detta krav. 

<!-- 28 --> 
### Kan jag ansluta Power BI till en skrivskyddad databasserver på Business Central Online? 

Den här funktionen kommer snart att vara tillgänglig. Från och med februari 2022 kommer nya rapporter som du skapar baserade på Business Central Online-data automatiskt att försöka ansluta till en skrivskyddad databaskopia. Detta medför att dina rapporter uppdateras snabbare och att prestanda påverkas mindre om du använder Business Central medan en rapport uppdateras. Vi rekommenderar att du, när det är möjligt, schemalägger rapporterna så att de uppdateras utanför normal arbetstid.

Om du har gamla rapporter baserade på Business Central-data, går de inte att ansluta till den skrivskyddade databaskopian.

### <a name="databasemods"></a>Jag har provat förhandsversionen av det nya anslutningsprogrammet för uppdateringen från februari 2022. När jag ansluter till min anpassade Business Central API-sida får jag felmeddelandet "Det går inte att infoga en post. Den aktuella anslutningens syfte är Skrivskyddad.". Hur kan jag åtgärda det?

Med det nya anslutningsprogrammet kommer nya rapporter som använder Business Central-data att anslutas till en skrivskyddad kopia av Business Central-databasen som standard. Den här ändringen ger bättre prestanda. I sällsynta fall kan det emellertid orsaka fel. Det här felet inträffar vanligen eftersom ditt anpassade API gör ändringar av Business Central-poster samtidigt som Power BI försöker hämta data. Det händer i synnerhet som en del av AL-utlösare: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord och OnAfterGetCurrRecord.

För att lösa problemet genom att tvinga Business Central-anslutningen att använda det här beteendet, se [Skapa Power BI-rapporter för att visa Business Central-data – åtgärda problem](across-how-use-financials-data-source-powerbi.md#fixing-problems).

<!--
In general, we recommend avoiding any database modifications in API pages when they're opening or loading records, because they cause performance issues and might cause your report refresh to fail. In some cases, you might still need to make a database modification when your custom API page opens or loads records. You can force the Business Central connector to allow this behavior. Do the following steps when getting data from Business Central for the report in Power BI Desktop:

1. Start Power BI Desktop.
2. In the ribbon, select **Get Data** > **Online Services**.
3. In the **Online Services** pane, select **Dynamics 365 Business Central**, then **Connect**.
4. In the **Navigator** window, select the API endpoint that you want to load data from.
5. In the preview pane on the right, you'll see the following error:

   *Dynamics365BusinessCentral: Request failed: The remote server returned an error: (400) Bad Request. (Cannot insert a record. Current connection intent is Read-Only. CorrelationId: [...])".*

6.  Select **Transform Data** instead of **Load** as you might normally do.
7. In **Power Query Editor**, select **Advanced Editor** from the ribbon.
8.  Replace the following line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null),
   ```

   with the line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false]),
   ```

9.  Select **Done**.
10. Select **Close & Apply** from the ribbon to save the changes and close Power Query Editor.

-->
### <a name="perms"></a>Hur ändrar jag eller avmarkerar jag det konto som jag använder för att ansluta till Business Central från Power BI Desktop?

I Power BI Desktop, gör något av följande:

1. I filmenyn, välj **Alternativ och inställningar** > **Inställningar av datakälla**.
2. Välj **Dynamics Business Central** i listan och välj sedan **Rensa behörigheter** > **Ta bort**.

Därefter ombeds du att logga in nästa gång du ansluter till Business Central för att hämta data.

## [Prestanda](#tab/performance)

<!-- 17 -->

### Går det snabbare att hämta data med hjälp av API-sidor än webbtjänster?

Ja. Våra tester tyder på att API-sidorna har upp till 25 % högre prestanda än webbtjänster.

<!-- 18 -->
### Finns det planer på att ha en spegling på Azure SQL Database-instansen, som jag kan ansluta till direkt?

Nej. Inte just nu. Du kan bara kommunicera med Business Central via API:er.

<!-- 19 -->
### Datainläsning från Business Centrals webbtjänster verkar vara långsamma. Finns det något sätt att hämta data direkt från SQL Database-tabellen?

Nej. Det går inte att direkt komma åt databasen, men om du växlar till API-sidor (när den nya anslutningen är tillgänglig) blir det mycket enklare.

## [Avancerat](#tab/advanced)
<!-- 1 -->

### Finns det planer för Power BI-anslutningen för att stödja de inkrementella uppdateringsfunktionerna i Power BI-tjänsten?

Ja. Det finns i vår plan.

<!-- 2 -->
### Om en lokal Business Central-lösning inte har tillgång till Internet, kan jag fortfarande använda Power BI?
<!-- todo: please explain this one-->

Ja. I det här fallet använder du Power BI Desktop lokalt och ansluter till den lokala installationen av Business Central. När du är ansluten kan du skapa och visa rapporter, men du kan inte publicera dem till Power BI-tjänsten. 
<!-- 20 -->
### Finns det några planer på att göra det möjligt att replikera Business Central Online-databaser så att de är tillgängliga för skrivskyddade SQL-frågor? Denna möjlighet kan stödja inkrementell uppdatering och vara mycket snabbare än API:er eller webbtjänster.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Ja. Vi har denna funktion i vår långsiktiga plan. 

<!-- 21 -->
### Om jag använder Azure Data Factory för att hämta data från Business Central och använder dem på Power BI, bidrar det till att höja prestandan? 

Ja. Det här avancerade scenariot gör att Business Central bibehåller prestandan eftersom dataåtkomsten görs via Azure Data Factory.

<!-- 22 -->
### Finns det några planer på att stödja Power BI-distribution eller ett sätt att bygga distributionsledningar för PBI-rapporter, ungefär som tillägg? Eller kanske till och med ett enkelt API i Business Admin Center? 

Vi undersöker den här funktionen. Power BI innehåller många API:er som styr rapportdistributioner. Mer information finns i [Introduktion till distributionsledningar](/power-bi/create-reports/deployment-pipelines-overview).

### När jag hämtar data från Business Central för att använda i mina Power BI-rapporter visas vissa värden som "_x0020_". Vilka är dessa värden?

Vissa API-sidor, inklusive de flesta API v 2.0-sidor, har fält baserade på [Al Enum-objekt](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Fält som baseras på AL Enum-objekt måste ha namn som är konsekventa och alltid samma, så att filter i rapporten alltid fungerar&mdash;oavsett vilket språk eller operativsystem du använder. Därför är inte fälten som baseras på AL Enum översatta och kodade för att undvika specialtecken, inklusive blanksteg. När det inte finns ett tomt alternativ i det AL-Enum-objektet kodas det till "_x0020_". Du kan alltid använda en omvandling till data på Power BI om du vill visa olika värden för dessa fält, t. ex. "Tomt".

## Se även

[Power BI licenser](admin-powerbi-setup.md#license)  
[Business Central och Power BI introduktion](admin-powerbi.md)  
[Översikt över Power BI-integrering](admin-powerbi-overview.md)  
[Aktivera Power BI i Business Central](admin-powerbi-setup.md)  
[Arbeta med Power BI-rapporter i Business Central](across-working-with-powerbi.md)  
[Arbeta med Business Central-data i Power BI](across-working-with-business-central-in-powerbi.md)  
[Skapa Power BI-rapporter för att visa Business Central-data](across-how-use-financials-data-source-powerbi.md)  
[Dokumentation om Power BI](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
