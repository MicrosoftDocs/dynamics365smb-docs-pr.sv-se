---
title: Konsolidera data från flera företag
description: Detta ämne förklarar hur du kan konsolidera redovisningstransaktionerna för två eller flera separata företag (dotterbolag) till ett konsoliderat företag.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 06/27/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# <a name="consolidating-financial-data-from-multiple-companies"></a>Konsolidera ekonomiska data från flera företag

Vissa organisationer använder [!INCLUDE [prod_short](includes/prod_short.md)] i flera affärsenheter eller juridiska enheter. Andra använder [!INCLUDE [prod_short](includes/prod_short.md)] i dotterbolag som ska rapportera till överordnade organisationer. [!INCLUDE [prod_short](includes/prod_short.md)] ger revisorer verktyg som hjälper dem att överföra redovisningstransaktioner från två eller flera företag (dotterbolag) till ett konsoliderat företag.  

Varje enskilt företag som är involverat i en konsolidering kallas för en affärsenhet. Det företag där du kombinerar datan kallas för det konsoliderade företaget.  

Du kan överföra ekonomiska data från dotterbolag till det konsoliderade företaget, även om dotterbolagen använder [!INCLUDE [prod_short](includes/prod_short.md)] i olika miljöer. Mer information om hur du ansluter till andra miljöer finns i [Konfigurera företagskonsolidering](finance-consolidated-company-reporting-setup.md#busunit).

Om en affärsenhets ekonomirapporter använder i en annan valuta än det konsoliderade företagets måste du ange valutakurser för konsolideringen. Mer information om valutakurser för konsolideringar finns i [Konfigurera företagskonsolidering](finance-consolidated-company-reporting-setup.md#exchrates).  

Du kan konsolidera:  

* Genom företag med olika kontoplaner.  
* Företag som använder olika räkenskapsår och olika valutor.  
* Antingen hela beloppet eller en procentandel av ett företags finansiella information.
* Med hjälp av olika valutakurser på enskilda redovisningskonton.
* Företag i andra bokförings- och affärshanteringsprogram.
* Företag i olika [!INCLUDE [prod_short](includes/prod_short.md)]-miljöer.

Du kan lägga upp det konsoliderade företaget i en databas på samma sätt som du lägger upp andra företag. Kontoplanen är oberoende av kontoplanen i affärsenheterna. Kontoplanen i affärsenheterna kan skilja sig från varandra. Om du vill ha mer information om hur du konfigurerar en konsolidering går du till [Konfigurera företagskonsolidering](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Att konsolidera ekonomiska data kan vara särskilt användbart för företagsinterna processer. Mer information om företagsinterna funktioner finns i [Hantera företagsinterna transaktioner](intercompany-manage.md).

## <a name="consolidate-data"></a>Konsolidera data

Innan du konsoliderar är det en bra idé att testa dina data innan du överför dem till det konsoliderade företaget. [!INCLUDE[prod_short](includes/prod_short.md)] tittar efter skillnader i information som finns i affärsenheterna och det konsoliderade företaget. Till exempel om kontonummer eller dimensionskoder är olika. Korrigera eventuella fel som du hittar innan du kör rapporten. Du kan testa en databas eller - om du importerar data från en XML-fil - testa filen.

### <a name="test-the-data-before-you-consolidate"></a>Testa du datan före konsolidering

1. Öppna det konsoliderade företaget.  
2. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **affärsenhet** och väljer sedan relaterad länk.  
3. Testa filen och databasen enligt följande:  

    * Testa en fil genom att välja åtgärden **testa fil**, ange namnet på filen och välj sedan **Skriv ut**.  
    * Om du vill testa en databas väljer du **Testa databas**.  

### <a name="run-the-consolidation"></a>Kör konsolideringen

När du har testat data kan du starta konsolideringen överför den till det konsoliderade företaget. En assisterad konfigurationsguide hjälper dig genom processen.

> [!NOTE]
> När du kör konsolideringen kan du välja vilka företag som ska inkluderas. Om ditt konsoliderade företag inte har tillgång till ett eller flera dotterbolag kan du bevilja åtkomst till dem i guiden.

1. Logga in på det konsoliderade företaget.  
2. På sidan **Affärsenheter** väljer du åtgärden **Konsolidera**.  
3. Fyll i relevanta fält.  

## <a name="use-the-consolidated-trial-balance-report"></a>Använd rapporten Konsoliderad råbalans

Rapport **Konsoliderad råbalans** kan ge dig en överblick över din verksamhets övergripande ekonomiska hälsa. Rapporten kombinerar redovisningstransaktioner från var och ett av företagen i ett nytt företag som du skapar för att innehålla konsoliderade data. Det konsoliderade företaget är bara en behållare för konsoliderade data och saknar levande affärsdata. Företagen som du inkluderar i det konsoliderade företaget blir **Affärsenheter** i rapporten. Om det är fyra affärsenheter eller färre kan rapporten **Konsoliderad råbalans (4)** användas.  

Rapporten visar en linje för varje konto och följer kontoplanens struktur. Ett konto visas inte om alla belopp på raden är 0. Rapporten visar visas följande information för varje konto:

* Kontonumret och namnet på kontot.
* Summorna för det konsoliderade företaget och för varje affärsenhet. Totalen kan visas som en nettoförändring eller som saldo t.o.m. datum.
* De gjorda elimineringarna i det konsoliderade företaget. Elimineringar kommer alltid att visas för en period motsvarande det konsoliderade företagets räkenskapsår.
* Totalen för det konsoliderade företaget efter elimineringar. Visas som en nettoförändring eller som saldo t.o.m. datum.

## <a name="eliminate-repeated-transactions"></a>Eliminera upprepade transaktioner

När du har konsoliderat företagen måste du hitta och eliminera alla transaktioner som registreras mer än en gång mellan företag. Bearbeta konsolideringselimineringar är en manuell process.  

Så här eliminerar du upprepade transaktioner:

1. Hitta transaktioner som kan behöva justeras och ange redovisningsjournalrader om du vill ta bort dem.
2. Kör rapporten **Redov. konsolid.elimineringar** för att hjälpa dig att bedöma effekterna av redovisningsjournalraderna innan du bokför.
3. Bokför justeringstransaktionerna.

Rapporten **Redov. konsolid.elimineringar** visar en preliminär råbalans där du kan simulera konsekvenserna av att eliminera poster. I rapporten jämförs transaktionerna i det konsoliderade företaget med de elimineringar som registrerats i redovisningsjournalen.

Innan du kan inkludera en affärsenhet i rapporten måste du konfigurera enheten på sidan **Affärsenheter**. Se till att aktivera växlingsknappen **Konsolidera**.

En rad skapas för varje konto enligt kontoplanens uppställning. Ett konto visas inte om alla belopp på raden är 0. Rapporten visar visas följande information för varje konto:

* Kontonummer.
* Kontonamn
* Om du har valt en eller flera koncernföretagskoder i fältet **Affärsenhetskod** på sidan för begäran visas en summa för det konsoliderade företaget exklusive de valda affärsenheterna och elimineringarna. Om du inte har fyllt i fältet **Affärsenhetskod** visas en summa för det konsoliderade företaget exklusive elimineringar.
* Om du har valt en affärsenhetskod i fältet **affärsenhetskod** på sidan för begäran visas en summa för de importerade transaktionerna från affärsenheten. Om du inte har fyllt i fältet **affärsenhetskod** visas en summa för de bokförda elimineringarna i det konsoliderade företaget.
* Totalen för det konsoliderade företaget med alla koncernföretag och alla bokförda elimineringar.
* De gjorda elimineringarna i det konsoliderade företaget. Transaktionerna i redovisningsjournalen som är vald på sidan för begäran.
* Beskrivningen kopierad från redovisningsjournalen.
* Det konsoliderade företagets total efter elimineringarna om de är bokförda.

## <a name="export-and-import-consolidated-data-between-databases"></a>Exportera och importera konsoliderade data mellan databaser

Om data för en affärsenhet finns i en annan databas kan du göra en manuell filbaserad överföring eller automatisera processen med hjälp av ett API. Mer information om API:et finns i [Använda vårt API för att automatiskt dela data mellan miljöer](#use-our-api-to-automatically-share-data-across-environments).

I det här avsnittet beskrivs den manuella, filbaserade processen.

Du exporterar datan till en fil innan du tar med den i konsolideringen. Exportera varje företag separat med hjälp av batch-projektet **Exportera konsolidering**.  

> [!TIP]
> Använd samma process för att exportera konsoliderade data som du måste skicka till Dynamics 365 Finance. Till exempel om affärsenheten är ett dotterbolag och moderbolaget använder Dynamics 365 Finance.

När du kör batchprojektet körs bearbetas alla poster i redovisningskonton. För varje kombination av valda dimensioner och datum summeras och exporteras innehållet i fälten **Belopp** för posterna. Nästa kombination av valda dimensioner och datum med samma kontonummer behandlas. Därefter behandlas kombinationerna i nästa kontonummer och så vidare.  

De exporterade posterna innehåller följande fält: **Kontonr**, **Bokföringsdatum** och **Belopp**. Om även dimensionsinformation har exporterats inkluderas dimensionskoder och dimensionsvärden.  

1. För varje exporterad rad, om summan av fälten **Belopp** är ett debetbelopp, kommer kontonumret som har angetts i affärsenhetens fält **Debetkonto konsolidering** att exporteras till raden. Om summan är ett kreditbelopp, kommer motsvarande nummer i fältet **Kreditkonto konsolid.** att exporteras till raden.  
2. Det datum som används för varje exporterad rad är antingen periodens slutdatum eller, om överföringen utförs varje dag, det exakta datumet för beräkningen.  
3. Det dimensionsvärde som exporteras för transaktionen är det konsoliderade företagets dimensionsvärde som har lagts upp i fältet **Konsolideringskod** för det dimensionsvärdet. Om inget dimensionsvärde har angetts för det konsoliderade företaget i fältet **Konsolideringskod** för det dimensionsvärdet, exporteras själva dimensionsvärdet till raden.  
4. XML-filerna innehåller dessutom valutakurserna i konsolideringsperioden. Dessa kurser placeras i ett separat avsnitt i början av filen.  

## <a name="use-our-api-to-automatically-share-data-across-environments"></a>Använd vårt API för att automatiskt dela data mellan miljöer

[!INCLUDE [prod_short](includes/prod_short.md)] innehåller ett API som gör att du kan automatisera processen för att dela ekonomiska data från affärsenheter till det konsoliderade företaget. API:et är gratis att använda och enkelt att installera. Du kan till och med dela data mellan [!INCLUDE [prod_short](includes/prod_short.md)]-miljöer. Du kan till exempel behöva dela mellan miljöer när affärsenheter inte finns i samma geografiska Azure-områden. Mer information om hur du använder API:et för att automatisera konsolideringsprocessen finns i [Konfigurera företagskonsolidering](finance-consolidated-company-reporting-setup.md#busunit).

## <a name="see-also"></a>Se även

[Konfigurera företagskonsolidering](finance-consolidated-company-reporting-setup.md)  
[Hantera koncerninterna transaktioner](intercompany-manage.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportera affärsdata till Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
