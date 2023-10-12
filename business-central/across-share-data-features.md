---
title: Dela data
description: Lär dig mer om olika sätt att dela affärsdata från Business Central.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 09/21/2022
ms.author: jswymer
---
# Dela affärsdata från Business Central

Samarbete mellan personer inom och utanför en organisation är en vital del av de flesta företag. I [!INCLUDE[prod_short](includes/prod_short.md)] finns flera funktioner för att dela affärsdata, till exempel en lista över poster, specifika poster eller dokument. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Med alla dessa funktioner skyddas åtkomst till data av licensen och behörigheterna för Business Central.

## Kopiera en länk

![Stöds](media/check.png) Business Central Online ![Stöds](media/check.png) Business Central lokalt

På valfri sida kan du kopiera sidans URL och sedan klistra in och distribuera den i andra typer av media såsom e-post, Teams-chattar och textmeddelanden. Det enklaste sättet att kopiera en länk är att välja **Dela** > **Kopiera länk** längst upp på sidan. Ett annat sätt är att kopiera hela URL-adressen direkt från webbläsarens adressruta.

När du klistrar in URL:en i en RTF-redigerare, till exempel Word, Outlook eller Teams, istället för att visa den fullständiga URL:en får länken ett mer läsbart namn som tydligt anger målets kontext. Namnet och mönstret varierar beroende på vilken sida du länkar till. Föreställ dig följande exempel:

|Mönster|Sidexempel|Länknamn|
|-|-|-|
|Listsidor|Listsidan **Artiklar** | **Artiklar**|
|Listvy| **Öppna** filtrerad vy i listan **Försäljningsorder**|**Försäljningsorder – öppna**|
| Enstaka post|Artikelkort med en enskild post|"Artikelkort – 1896 ∙ ATEN-bord"|
|Postutkast| Nytt kundkort|**Nytt - Kundkort**|
|Företag som använder märket|Listsidan **Artiklar** för företag med märket **CRONUS**| **Artiklar (CRONUS)**|

> [!TIP]
> En liknande namngivningskonvention används på webbläsarflikar.

### Dela dataanalys
Om du visar en sida eller fråga i dataanalysläget kan du dela en specifik analysflik genom att välja nedpilspetsen på fliken och sedan välja **Kopiera länk**. [Läs mer om dataanalysläge](analysis-mode.md). 

### Ändra sidlänken

När du har kopierat en länk kan du, innan du skickar den, ändra URL-adressen för att ändra vad som ska visas när sidan öppnas. Du kan till exempel lägga till filter eller ange ett annat företag.

[Läs mer om webbklientens URL](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### Om filtrerade listor

Med filterrutan på list sidor kan du använda filter för att begränsa posterna som visas i listan. Om du använder åtgärden **Kopiera länk** eller kopierar URL-adressen från webbläsaren innehåller sidlänken inte filterändringarna. Användare som öppnar länken kommer att se hela samlingen. Sättet att behålla filtreringen på en länk till en samlingssida är att först spara den filtrerade sidan som en **Vy**. Öppna sedan vyn och kopiera länken därifrån.

[Läs mer om sortering, sökning och filtrering](ui-enter-criteria-filters.md).

## Dela med Teams

![Stöds](media/check.png) Business Central Online ![Stöds inte](media/x-icon.png) Business Central lokalt

Direkt från de flesta samlings- och informations sidor kan du skicka en länk till sidan till personer, grupper eller kanaler. Dela t.ex. en länk till en filtrerad vy över posterna. Om du har installerat [!INCLUDE[prod_short](includes/prod_short.md)]-appen för Teams kommer länken automatiskt att expanderas till ett kompakt kort som du kan ta med i meddelandet. Mottagarna kan sedan markera länken eller kortet så att sidan öppnas i Business Central.

[Läs mer om att dela poster och sidlänkar i Teams](across-working-with-teams.md).

## Dela via OneDrive

![Stöds](media/check.png) Business Central Online ![Stöds](media/check.png) Business Central lokalt

Med Business Central är det enkelt att lagra, hantera och dela filer med andra personer via OneDrive för företag. På de flesta sidor där det finns filer, t.ex. Rapportinkorgen eller filer som är bifogade till poster, finns åtgärderna **Öppna i OneDrive** och **Dela**. Bägge åtgärder sparar en kopia av en fil i OneDrive. I OneDrive kan du använda dess funktioner för delning och bidrag för filen. Skillnaden i åtgärder är att **Öppna i OneDrive** öppnar filen i OneDrive. **Dela** öppnar en sida och låter dig välja vem du vill dela filen med. Mottagare får ett e-postmeddelande om att de kan komma åt filen från din OneDrive.

[Läs mer om att dela filer i OneDrive](across-share-onedrive.md).

## Öppna i Excel

![Stöds](media/check.png) Business Central Online ![Stöds](media/check.png) Business Central lokalt

För listsidor och listor som är inbäddade på en sida kan du använda åtgärden **Öppna i Excel**. Med den här åtgärden exporteras listan över poster till en Excel-arbetsbok (.xlsx-fil) som du kan dela med andra. I arbetsboken kan du också använda funktionen Dela som ingår i Excel.

[Läs mer om hur du visar och redigerar i Excel](across-work-with-excel.md).

## Dela rader eller tabeller

![Stöds](media/check.png) Business Central Online ![Stöds](media/check.png) Business Central lokalt

Du kan dela en eller flera poster i en lista. Välj bara kortkommandot <kbd>Ctrl</kbd>+<kbd>C</kbd> för att kopiera till Urklipp. Klistra sedan in det du kopierade i ett annat program genom att trycka <kbd>Ctrl</kbd>+<kbd>V</kbd>. Om du till exempel kopierar tre försäljningsorder som klistras in i ett e-postmeddelande visas orderna i en snyggt formaterad tabell.

[Läs mer om kopiera och klistra in i Vanliga frågor](faq-copy-paste.yml).

## Se även

[Business Central- och OneDrive-integration](across-onedrive-overview.md)  
[Hantera OneDrive integrering med Business Central](admin-onedrive-integration.md)  
[OneDrive Vanliga frågor och svar](admin-onedrive-faq.md)