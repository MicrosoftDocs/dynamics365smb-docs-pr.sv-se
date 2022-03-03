---
title: Business Central för flera platser och internationella organisationer | Microsoft Docs
description: Business Central ger möjligheter som stöder en affärsmodell med nav och ekrar.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: hub-and-spoke, multi-site, headquarter, sites
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: a135499b12ed04ecf179f1cb5691c97ecc0f1aaf
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141105"
---
# <a name="business-central-for-multi-site-and-international-organizations"></a>Business Central för flera platser och internationella organisationer
Organisationer som har flera platser använder ofta en företagsmodell med nav och ekrar, där ett moderbolag, eller ett huvudkontor, hanterar verksamhetens övergripande verksamhet medan varje plats fungerar som en enda fristående enhet. Platser är ofta geografiskt spridda och har olika behov av att dela information med moderbolaget. Dessutom behöver inte platserna samma komplexitetsnivå, och de saknar ofta de resurser som behövs för att upprätthålla ett stort system.

[!INCLUDE[prod_short](includes/prod_short.md)] ger små och medelstora företag en affärshanteringslösning som är lätt att använda och som upprätthålls till en låg ägandekostnad.

I den här artikeln beskrivs några sätt som [!INCLUDE[prod_short](includes/prod_short.md)] stöder affärsmodeller med nav och ekrar.

## <a name="integrating-the-headquarter-company-and-the-sites"></a>Integrera moderbolaget och platserna

[!INCLUDE[prod_short](includes/prod_short.md)] kan integreras med moderbolagets redovisningssystem samtidigt samtidigt som det uppfyller olika behov för olika platser, oavsett storlek, läge eller typ av verksamhet.

Följande diagram är ett exempel på olika platser som är integrerade med ett moderbolag.

![Diagrambeskrivning som genereras automatiskt.](media/multisite-headquarter-sites.png)

## <a name="meet-the-needs-of-domestic-and-international-sites"></a>Uppfylla behoven hos inhemska och internationella platser

På platser varierar ofta olika företags behov, baserat på bransch, affärsmetoder eller deras relation till moderbolaget. [!INCLUDE[prod_short](includes/prod_short.md)] kan enkelt anpassas och utökas för olika typer av företag och språk. Microsoft AppSource erbjuder stora mängder program från Microsoft och våra partners, och partner kan snabbt driftsätta [!INCLUDE[prod_short](includes/prod_short.md)] med minimala störningar på den dagliga verksamheten.

För flera multinationella organisationer stöder [!INCLUDE[prod_short](includes/prod_short.md)] lokala rättsliga krav och affärspraxis.

* För online-versioner finns det fler än [40 lokaliserade landsversioner](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json) som du kan installera som tillägg från Microsoft AppSource.  
* I lokala versioner är [landsversioner](/azure/architecture/solution-ideas/articles/business-central) antingen tillgängliga som Microsoft-lokaliserade versioner eller partnerledda tilläggsprogram.

Ett nätverk av över 4 000 Microsoft-partner världen över ger lokal expertis.

| **Affärsbehov** | **Så här stöder Business Central det** | **Läs mer** |
|-------------------------|-------------------------|-------------------------|
| Skräddarsy systemet så att det passar företaget. | Njut av ett system som har utformats från starten för medelstora företag. | [Översikt](https://dynamics.microsoft.com/business-central/overview/) |
| Ta hand om regler och lokala metoder. | Uppfylla lokala lagstadgade krav och affärsmetoder. | [Lokal funktionalitet](about-localization.md) |
| Öppna flera företag från en enda sida. | Få snabb åtkomst till alla Business Central-företag i organisationen. | [Företagsnav](ui-extensions-company-hub.md) |
| Hantera flera språk och valutor. | Stöd för flera språk och valutor bidrar till att tillgodose lokala behov. | [Funktioner för flera språk](about-locale-language.md)<br></br>[Kapacitet för flera valutor](finance-how-setup-additional-currencies.md) |


## <a name="consolidate-financial-data"></a>Konsolidera ekonomiska data

En huvudaspekt av affärsmodellen med nav och ekrar är möjligheten för moderbolaget och platserna att utbyta ekonomiska data, även då moderbolaget och platserna använder olika system, redovisningsstrukturer, språk och valutor.

| **Affärsbehov** | **Så här stöder Business Central det** | **Läs mer** |
|-------------------------|-------------------------|-------------------------|
| Konsolidera ekonomiska data från platser. | Konsolidera ekonomiska rapporter för platser, oavsett om de kör Business Central eller andra program, till en enda affärsenhet (företag). | [Konsolidera ekonomiska data från flera företag](finance-consolidated-company-reporting.md) |
| Integrera redovisningsstrukturer. | Överför konsolideringsdata från olika redovisningsstrukturer till din egen. Inbyggt filformat för F & O (tillgängligt med utgivningscykel 2, 2020) | [Importera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)<br></br>[Förbereda redovisningskonton för konsolidering](finance-consolidated-company-reporting-setup.md#glacc) |
| Överför i flera valutor. | Hjälp till att säkerställa att finansiella rapporter i olika valutor är exakta och använd korrekta valutakurser. | [Uppdatera valutakurser](finance-how-update-currencies.md) |

## <a name="share-business-insight-with-integrated-analytics"></a>Dela affärsinsikt med integrerad analys

Anpassa organisationen med dina affärsmål genom att ge en gemensam förståelse för den aktuella verkligheten. Integrerad analys kan hjälpa andra att basera sina beslut på samma uppsättning fakta.

| **Affärsbehov** | **Så här stöder Business Central det** | **Läs mer** |
|-------------------------|-------------------------|-------------------------|
| Dela med dig insikter med platser utan omfattande IT-support. | Skapa KPI:er och affärsintelligens-instrumentpaneler i Power BI baserat på dina data. | [Arbeta med Business Central-data i Power BI](across-working-with-business-central-in-powerbi.md) |
| Utveckla anpassade ekonomiska rapporter. | Skapa parameterbaserade ekonomiska rapporter. | [Affärsstöd](bi.md) |
| Enas om fakta. | Generera, visa och dela rapporter med interna och externa intressenter. | [Ekonomisk rapportering](finance-reports.md) |
| Analysera data i Excel. | Sök fakta, felsök och gör ad hoc-analyser i Microsoft Excel. | [Analysera finansiella rapporter i Excel](finance-analyze-excel.md) |


## <a name="exchange-data-using-apis-and-xmlports"></a>Utbyta data med hjälp av API:er och XMLportar

API:er och XMLportar förenklar processen för att ansluta instanser av [!INCLUDE[prod_short](includes/prod_short.md)], inklusive sådana som har anpassats för varje plats.

| **Affärsbehov** | **Så här stöder Business Central det** | **Läs mer** |
|-------------------------|-------------------------|-------------------------|
| Anslut anpassade versioner mellan platser och moderbolaget. | API-sidor kan exponera alla representationer av en entitet, inklusive dess anpassningar. | [Aktivera API:er för Business Central](/dynamics-nav/enabling-apis-for-dynamics-nav) |
| Versionshantering och säkerhet. | API: er använder ODataV4, som tillhandahåller versionshantering, webhookar och ändringsspårning. | [Säkerhet och skydd](/dynamics365/business-central/dev-itpro/security/security-and-protection) |
| Bokför och importera XML-dokument. | Kodmoduler kan visas som obundna åtgärder för att stödja bokföring och insugning av XML-dokument. För bearbetning av XML-dokument kan XMLportar användas. Obundna åtgärder kan också användas för att generera ett XML- eller JSON-dokument. | [XMLport-objekt](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-object) |
| Gör underhållet enklare via elektronisk dataintegration. | En elektronisk dataintegrationslösning kan läggas till för att fungera som integrationsskikt mellan moderbolaget och platserna. | [Ramverk för dataintegration](across-about-the-data-exchange-framework.md) |
| Utbyta data mellan olika system. | Använd XMLportar för att skapa XML-dokument, som sedan kan utbytas mellan ett moderbolag som använder ett system och platser som använder Business Central. | [XMLport-översikt](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-overview) |
| Leda komplexa dataintegrationer. | Använd en kombination av XMLportar med Business Central och Microsoft BizTalk Server för att tillgodose unika behov på dina platser.</br>För komplicerade behov bör du använda en lösning för elektronisk dataintegration baserad på BizTalk Server och Commerce Gateway i Business Central i kombination med XMLportarna. | [Arbeta med rapporter och batch-jobb och XMLports](ui-work-report.md) |
| Anslut till <sup></sup>tredjepartslösningar och -tjänster. | Med API:er etableras en punkt-till-punkt-anslutning mellan Business Central och <sup></sup>tredjepartslösningar och -tjänster. | [API v2.0](/dynamics-nav/api-reference/v2.0/) |


## <a name="promote-an-efficient-intercompany-supply-chain"></a>Främja en effektiv koncernintern försörjningskedja

Platser behöver ofta ha till gång till försörjningskedjan och möjlighet att hantera vissa aspekter av den. Platser kan t.ex. använda samma leverantör, men hantera tillgångar och fysiska platser var för sig.

| **Affärsbehov** | **Så här stöder Business Central det** | **Läs mer** |
|-------------------------|-------------------------|-------------------------|
| Behandla koncerninterna transaktioner som normala försäljnings- och inköpstransaktioner. | Använd koncerninterna bokningar för att skapa försäljnings- och inköpsdokument och redovisningstransaktioner för hela arbetsflöden och för fler än ett företag i taget för att eliminera dubblerade dataposter. | [Hantera koncerninterna transaktioner](intercompany-manage.md) |
| Använd papperslösa processer. | Undvik kostnaden för att skicka, ta emot och skriva ut dokument. | [Inkommande dokument](across-income-documents.md)<br><br> [Hantera bifogade filer, länkar och anteckningar på kort och dokument](ui-how-add-link-to-record.md) |

## <a name="respond-quickly-to-new-business-conditions"></a>Svara snabbt på nya affärsvillkor

Moderbolaget måste kunna reagera snabbt på företagsförändringar vid varje plats. I kombination med Power Automate kan [!INCLUDE[prod_short](includes/prod_short.md)] fungera som en tidig varningsfunktion.

![En skärm bild av ett inlägg på sociala medier Beskrivning som genererats automatiskt.](media/multisite-apps.png)

| **Affärsbehov** | **Så här stöder Business Central det** | **Läs mer** |
|-------------------------|-------------------------|-------------------------|
| Generera e-postaviseringar automatiskt. | Konfigurera aviseringar i Power Automate som genererar e-postmeddelanden för att informera dig om kritiska affärsvillkor på platser eller hos partners i försörjningskedjan. | [Business Central och Power BI](admin-powerbi.md) |
| Använd vanliga eller anpassade aviseringar. | Använd 12 olika mallar som ingår i Business Central eller ange dina egna aviseringar så att de passar ditt företag. | [Använda Business Central i ett automatiskt arbetsflöde](across-how-use-financials-data-source-flow.md) |

## <a name="see-also"></a>Se även
[Administration av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
