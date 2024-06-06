---
title: 'Översikt över analyser, business intelligence och rapportering'
description: 'Innehåller en översikt över alla analys-, Business Intelligence- och rapporteringsfunktioner som stöds i Business Central.'
author: KennieNP
ms.topic: get-started
ms.devlang: al
ms.search.keywords: feature overview
ms.reviewer: bholtorf
ms.date: 09/22/2022
ms.author: kepontop
ms.service: dynamics-365-business-central
---

# <a name="analytics-business-intelligence-and-reporting-overview"></a>Översikt över analyser, business intelligence och rapportering

Små och medelstora företag förlitar sig på inbyggd analys och rapportering som de kan använda direkt för att hålla reda på sin verksamhet. [!INCLUDE[prod_short](includes/prod_short.md)] tillhandahåller rapporter och analysverktyg som täcker grundläggande och komplexa affärsprocesser för sådana organisationer. Du kan också göra ad hoc-analyser direkt från din hemsida.  

## <a name="analytics-needs-in-organizations"></a>Analysbehov inom organisationer

När man tänker på analysbehov inom organisationer kan det hjälpa att använda en mental modell baserad på profiler beskrivna på en övergripande nivå och deras olika analytiska behov.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustration av olika profiler för analys" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Modellen bygger på att olika roller i en organisation har olika behov när det gäller data. Ju högre en roll placeras i organisationsschemat, desto mer aggregerade data behöver någon i rollen för att utföra sitt arbete.

Roller har ofta föredragna sätt att använda och analysera data, sätt som återspeglar den nivå av dataaggregering som de behöver.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustration av hur olika profiler har olika analysbehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

Använd följande avsnitt om du vill veta mer om olika sätt att använda data från [!INCLUDE[prod_short](includes/prod_short.md)]:

- Ekonomiska rapporter
- KPI:er och instrumentpaneler
- Ad hoc-analys
- Rapporter

## <a name="using-financial-reports-to-produce-financial-statements-and-kpis"></a>Använda ekonomiska rapporter för att göra finansiella rapporter och KPI:er

Funktionen ekonomiska rapporter ger dig insikt i ekonomiska data som lagras i din kontoplan. Du kan ställa in ekonomiska rapporter till att analysera siffror för redovisningskonton och jämför redovisningstransaktioner med budgettransaktioner.

:::image type="content" source="media/acc_schedule_13_columns.jpg" alt-text="Skärmbild av en finansiell rapport." lightbox="media/acc_schedule_13_columns.jpg":::

Dimensioner spelar en viktig roll i Business Intelligence. En dimension är data som du kan lägga till en transaktion som en parameter. Med hjälp av dimensioner kan du gruppera poster med liknande egenskaper. Till exempel grupper med kunder, regioner, produkter och säljare. Grupper gör det enklare att hämta data för analys. Bland annat kan du använda dimensioner när du definierar analysvyer och när du skapar ekonomiska rapporter. Mer information: [Arbeta med dimensioner](finance-dimensions.md).

Mer information om bokslut och KPI:er finns i [Använda ekonomiska rapporter för att skapa finansiella rapporter och KPI:er](bi.md).

## <a name="using-key-performance-indicators-to-meet-your-business-goals"></a>Använda KPI:er för att uppfylla dina verksamhetsmål

En KPI (Key Performance Indicator) är ett mätbart värde som visar hur effektivt du uppfyller dina mål. Tänk på KPI:er som ditt företags styrkort, ett sätt att mäta om du levererar dina mål eller inte.

Genom att identifiera och spåra KPI:er kan du veta om ditt företag är på rätt väg – eller om du bör ändra kurs. När KPI:er används på rätt sätt är de kraftfulla verktyg som hjälper dig att:

- Övervaka företagets ekonomiska hälsa.
- Mäta framsteg mot strategiska mål.
- Upptäcka problem tidigt.
- Göra snabba justeringar av taktiken.
- Motivera teammedlemmar.
- Fatta bättre beslut, snabbare.

För att lära dig mer om KPI:er, gå till [Använda KPI:er för att uppfylla dina verksamhetsmål](./analytics-about-kpis.md)

## <a name="ad-hoc-data-analysis"></a>Ad hoc-dataanalys

Du kanske bara vill kontrollera om siffrorna stämmer korrekt, snabbt bekräfta eller avslöja en hypotes om verksamheten eller kanske leta efter avvikelser i dina finansiella data. För ad hoc-analyser kanske du inte har en inbyggd rapport som hjälper dig att besvara dina frågor. Använd följande två funktioner för ad hoc-analyser:

- Dataanalys för huvudbokens listsidor
- Öppna i Excel

Med funktionen Dataanalys kan du öppna nästan alla listsidor, till exempel sidor för Redovisningstransaktioner eller Kundreskontratransaktioner, ange analysläge och sedan Gruppera, Filtrera och Pivotera data efter önskemål. 

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Exempel på hur du gör dataanalyser på sidan Redovisningstransaktioner." lightbox="media/data-analysis-gl-entries.png":::

På samma sätt kan du använda åtgärden **Öppna i Excel** för att öppna en listsida, eventuellt filtrera listan till en delmängd av data och sedan använda Excel för att arbeta med data. Du kan till exempel använda funktioner som Analysera data, What-If-analys eller Prognosblad.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Exempel på hur du gör dataanalyser på Redovisningstransaktioner med hjälp av Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Om du konfigurerar OneDrive för systemfunktioner öppnas Excel-arbetsboken i webbläsaren med hjälp av Excel för webben.

Mer information om ad hoc-analyser finns i [Ad hoc-dataanalys](reports-adhoc-analysis.md).

## <a name="reports"></a>Rapporter

En rapport i [!INCLUDE[prod_short](includes/prod_short.md)] samlar in information baserat på en angiven uppsättning kriterier. Rapporter organiserar och presenterar informationen i ett lättläst format som du kan använda i Excel, skriva ut eller spara som en fil.  

Rapporten ***Kundreskontra** är ett exempel på en interaktiv rapport i Excel och låter dig analysera vad dina kunder är skyldiga dig och när betalningar förfaller till betalning.

:::image type="content" source="media/aged-accounts-receivables-excel.png" alt-text="Exempel på den interaktiva rapporten Kundfordringar - ålder i Excel." lightbox="media/aged-accounts-receivables-excel.png":::

För Kundfordringar - ålder finns även [!INCLUDE[prod_short](includes/prod_short.md)] en rapport avsedd för utskrift. Möjligheten att skriva ut är praktisk om du föredrar att ha data i en .pdf-fil.

:::image type="content" source="media/aged-accounts-receivables-pdf.png" alt-text="Exempel på rapporten Kundfordringar - ålder i pdf." lightbox="media/aged-accounts-receivables-pdf.png":::

[!INCLUDE[prod_short](includes/prod_short.md)] levereras med mer än 300 inbyggda rapporter som du kan använda för att stödja dina affärsprocesser med datadrivna insikter. Om du vill få en snabb överblick över alla rapporter som är tillgängliga för din roll kan du öppna rapportutforskaren från rollcentret och alla listsidor samt från **Berätta**.

:::image type="content" source="media/report-explorer-finance.png" alt-text="Exempel på hur rapportutforskaren visar alla rapporter för en roll." lightbox="media/report-explorer-finance.png":::

Mer information om hur du använder rapportutforskaren för att se alla inbyggda rapporter finns i [Utforska rapporter per roll](ui-role-explorer.md).

I följande tabell visas artiklar om hur du använder inbyggda rapporter i [!INCLUDE[prod_short](includes/prod_short.md)].

| Till  | Gå till |
| --- | --- |
| Lär dig använda rapporter (bokmärk, kör, skriv ut, schemalägg och ändra layouten). | [Använda rapporter i det dagliga arbetet](reports-use-reports.md) |
| Mer information om de inbyggda rapporterna finns i [!INCLUDE[prod_short](includes/prod_short.md)]. |[Rapportöversikt](reports-available-reports.md)| 
| Använd Rapportutforskaren för att se alla inbyggda rapporter. | [Utforska rapporter per roll](ui-role-explorer.md) |

## <a name="external-business-intelligence-and-reporting-tools"></a>Externa Business Intelligence- och rapporteringsverktyg

Om du vill kan du använda business intelligence-verktyg som inte är inbäddade i [!INCLUDE[prod_short](includes/prod_short.md)]. Följande tabell innehåller länkar till vägledning och olika sätt att använda externa verktyg.

| Till  | Gå till |
| --- | --- |
| Använda Power BI med Business Central-data | [Använda Power BI med Business Central](admin-powerbi.md) |
| Integrera externa Business Intelligence-verktyg med [!INCLUDE[prod_short](includes/prod_short.md)].| [Externa Business Intelligence-verktyg](reports-external-analysis.md) |
| Hämta data till ett datadistributionslager eller datasjöar| [Hämta data till ett datadistributionslager eller en datasjö](/dynamics365/business-central/dev-itpro/performance/performance-developer#efficient-extracts-to-data-lakes-or-data-warehouses) |
| Analysera Business Central-data med Microsoft Fabric| [Introduktion till Microsoft Fabric och Business Central](admin-fabric.md) |
| Läs data från Business Central med API:er | [Business Central API v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) |

## <a name="analytics-by-functional-area"></a>Analys efter funktionsområde

Innehållet i denna allmänna artikel finns också i specialversioner för många funktionella områden i [!INCLUDE[prod_short](includes/prod_short.md)].

| Om du arbetar med... | Gå till |
| --- | --- |
| Ekonomi | [Ekonomisk analys](bi.md) |
| FÖRS | [Försäljningsanalys](sales-analytics-overview.md) |
| Inköp | [Inköpsanalys](purchasing-analytics-overview.md) |
| Hantering av anläggningstillgångar | [Analys av anläggningstillgångar](fa-analytics-overview.md) |


## <a name="see-also"></a>Se även

[Använda ekonomisk rapportering för att göra finansiella rapporter och KPI:er](bi.md)  
[Använda nyckeltal (KPI:er) för att uppfylla dina verksamhetsmål](analytics-about-kpis.md)  
[Gör ad hoc-dataanalyser](reports-adhoc-analysis.md)  
[Använd rapporter i det dagliga arbetet](reports-use-reports.md)  
[Översikt över inbyggda rapporter](reports-available-reports.md)  
[Utforska rapporter per roll](ui-role-explorer.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
