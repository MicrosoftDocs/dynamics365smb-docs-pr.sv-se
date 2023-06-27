---
title: Konsolidera data från flera företag
description: Detta ämne förklarar hur du kan konsolidera redovisningstransaktionerna för två eller flera separata företag (dotterbolag) till ett konsoliderat företag.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 09/29/2022
ms.author: bholtorf
---

# <a name="consolidating-financial-data-from-multiple-companies"></a>Konsolidera ekonomiska data från flera företag

Vissa organisationer använder [!INCLUDE [prod_short](includes/prod_short.md)] i flera affärsenheter eller juridiska enheter. Andra använder [!INCLUDE [prod_short](includes/prod_short.md)] i dotterbolag som ska rapportera till överordnade organisationer. I båda fallen använder revisorer inbyggda verktyg för att konsolidera ekonomiska data.  

Du kan konsolidera redovisningstransaktionerna för två eller flera separata företag (dotterbolag) till ett konsoliderat företag. Varje enskilt företag som är involverat i en konsolidering kallas för en affärsenhet. Det kombinerade företaget kallas för det konsoliderade företaget.  

Du kan importera data till det konsoliderade företaget från andra företag i samma [!INCLUDE [prod_short](includes/prod_short.md)]-klientorganisation från klientorganisationer eller från filer.  

Om en affärsenhets ekonomirapporter är i en annan valuta än det konsoliderade företagets måste du ange valutakurser för konsolideringen.  

Du kan konsolidera:  

* Genom företag med olika kontoplaner.  
* Företag som använder olika räkenskapsår och olika valutor.  
* Antingen hela beloppet eller en procentandel av ett företags finansiella information
* Med hjälp av olika valutakurser på enskilda redovisningskonton
* Företag i andra bokförings- och företagshanteringsprogram

Du kan lägga upp det konsoliderade företaget i en databas på samma sätt som du lägger upp andra företag. Kontoplanen är oberoende av kontoplanen i affärsenheterna. Kontoplanen i affärsenheterna kan skilja sig från varandra. Du kan lägga upp en lista över företag som ska konsolideras, verifiera redovisningsinformation innan du konsoliderar den, importera från filer eller databaser och generera konsolideringsrapporter. Mer information finns i [Konfigurera företagskonsolidering](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Att konsolidera ekonomiska data kan vara särskilt användbart i samband med koncerninterna processer. Mer information finns i [Hantera koncerninterna transaktioner](intercompany-manage.md).

## <a name="use-the-consolidated-trial-balance-report"></a>Använd rapporten Konsoliderad råbalans

Rapport **Konsoliderad råbalans** kan ge dig en överblick över din verksamhets övergripande ekonomiska hälsa. Rapporten kombinerar redovisningstransaktioner från var och ett av företagen i ett nytt företag som du skapar för att innehålla konsoliderade data. Detta företag kallas normalt för det *konsoliderade företaget*. Det konsoliderade företaget är bara en behållare för konsoliderade data och saknar levande affärsdata. Företagen som du inkluderar i det konsoliderade företaget blir **Affärsenheter** i rapporten. Mer information finns i [Konfigurera företagskonsolidering](finance-consolidated-company-reporting-setup.md). Om det är fyra affärsenheter eller färre kan rapporten **Konsoliderad råbalans (4)** användas.  

Rapporten visar en linje för varje konto och följer kontoplanens struktur. Ett konto visas inte om alla belopp på raden är 0. Rapporten visar visas följande information för varje konto:

* Kontonumret och namnet på kontot.
* Summorna för det konsoliderade företaget och för varje affärsenhet. Totalen kan visas som en nettoförändring eller som saldo t.o.m. datum.
* De gjorda elimineringarna i det konsoliderade företaget. Elimineringar kommer alltid att visas för en period motsvarande det konsoliderade företagets räkenskapsår.
* Totalen för det konsoliderade företaget efter elimineringar. Visas som en nettoförändring eller som saldo t.o.m. datum.

## <a name="consolidate-data"></a>Konsolidera data

Överföringen av siffrorna från affärsenheterna till det konsoliderade företaget är den faktiska *konsolideringen*. Innan du konsoliderar kan det vara bra att kontrollera om det finns några skillnader mellan den grundläggande informationen i affärsenheterna och i det konsoliderade företaget. Det finns två rapporter som du kan använda för att testa databasen och filen.

### <a name="to-test-the-data-before-you-consolidate"></a>Så här testar du data före konsolidering

Testa data innan du överför den till det konsoliderade företaget. [!INCLUDE[prod_short](includes/prod_short.md)] tittar efter skillnader i information som finns i affärsenheterna och det konsoliderade företaget. Till exempel om kontonummer eller dimensionskoder är olika. Du måste åtgärda felen innan du kan köra rapporten. Du kan testa en databas, eller om du importerar data från en XML-fil kan du testa filen.  

1. Öppna det konsoliderade företaget.  
2. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **affärsenhet** och väljer sedan relaterad länk.  
3. Testa filen och databasen enligt följande:  

    * Testa en fil genom att välja åtgärden **testa fil**, ange namnet på filen och välj sedan **Skriv ut**.  
    * Om du vill testa en databas väljer du **Testa databas**.  

### <a name="run-the-consolidation"></a>Kör konsolideringen

När du har testat data kan du starta konsolideringen överför den till det konsoliderade företaget.  

1. Logga in på det konsoliderade företaget.  
2. I rollcentret **Revisor** väljer du åtgärden **Kör konfiguration**.  
3. Fyll i relevanta fält.  
4. I avsnittet Filter anger du ett filter för den aktuella affärsenheten eller det aktuella företagsnamnet.  
5. Du kan också schemalägga en rapport att köras vid en tidpunkt som passar dig.  

## <a name="eliminate-repeated-transactions"></a>Eliminera upprepade transaktioner

När du har konsoliderat företagen måste du hitta och eliminera alla transaktioner som registreras mer än en gång mellan företag. Bearbeta konsolideringselimineringar är en manuell process.  

Så här eliminerar du upprepade transaktioner:

1. Hitta transaktioner som kan behöva justeras och ange redovisningsjournalrader om du vill ta bort dem.
2. Kör rapporten **Redov. konsolid.elimineringar** för att hjälpa dig att bedöma effekterna av redovisningsjournalraderna innan du bokför.
3. Bokför justeringstransaktionerna.

Rapporten **Redov. konsolid.elimineringar** visar en preliminär råbalans där du kan simulera konsekvenserna av att eliminera poster. I rapporten jämförs transaktionerna i det konsoliderade företaget med de elimineringar som registrerats i redovisningsjournalen.

Innan en affärsenhet kan ingå i rapporten måste du ställa in enheten på sidan **Affärsenheter**. Du måste välja fältet **konsolidera**.

En rad skapas för varje konto enligt kontoplanens uppställning. Ett konto visas inte om alla belopp på raden är 0. För varje konto visas följande information:

* Kontonummer.
* Kontonamn
* Om du har valt en eller flera koncernföretagskoder i fältet **Affärsenhetskod** på sidan för begäran visas en summa för det konsoliderade företaget exklusive de valda affärsenheterna och elimineringarna. Om du inte har fyllt i fältet **Affärsenhetskod** visas en summa för det konsoliderade företaget exklusive elimineringar.
* Om du har valt en affärsenhetskod i fältet **affärsenhetskod** på sidan för begäran visas en summa för de importerade transaktionerna från affärsenheten. Om du inte har fyllt i fältet **affärsenhetskod** visas en summa för de bokförda elimineringarna i det konsoliderade företaget.
* Totalen för det konsoliderade företaget med alla koncernföretag och alla bokförda elimineringar.
* De gjorda elimineringarna i det konsoliderade företaget. Transaktionerna i redovisningsjournalen som är vald på sidan för begäran.
* Beskrivningen kopierad från redovisningsjournalen.
* Det konsoliderade företagets total efter elimineringarna om de är bokförda.

## <a name="export-and-import-consolidated-data-between-databases"></a>Exportera och importera konsoliderade data mellan databaser

Om data för en affärsenheter är i en annan databas måste du exportera konsolideringsdata till en fil innan du kan inkludera den i konsolideringen. Varje företag måste exporteras var för sig. I detta avseende används batch-jobbet **Exportera konsolidering**.  

> [!TIP]
> Använd samma procedur för att exportera konsoliderade data som måste skickas till Dynamics 365 Finance, till exempel om den aktuella affärsenheten är ett dotterbolag och det överordnade företaget använder Dynamics 365 Finance.

När du kör batch-jobbet körs bearbetas alla poster i redovisningskonton. För varje kombination av valda dimensioner och datum summeras och exporteras innehållet i fälten **Belopp** för posterna. Nästa kombination av valda dimensioner och datum med samma kontonummer behandlas. Därefter behandlas kombinationerna i nästa kontonummer och så vidare.  

De exporterade posterna innehåller följande fält: **Kontonr**, **Bokföringsdatum** och **Belopp**. Om även dimensionsinformation har exporterats inkluderas dimensionskoder och dimensionsvärden.  

1. För varje exporterad rad, om summan av fälten **Belopp** är ett debetbelopp, kommer kontonumret som har angetts i affärsenhetens fält **Debetkonto konsolidering** att exporteras till raden. Om summan är ett kreditbelopp, kommer motsvarande nummer i fältet **Kreditkonto konsolid.** att exporteras till raden.  
2. Det datum som används för varje exporterad rad är antingen periodens slutdatum eller, om överföringen utförs varje dag, det exakta datumet för beräkningen.  
3. Det dimensionsvärde som exporteras för transaktionen är det konsoliderade företagets dimensionsvärde som har lagts upp i fältet **Konsolideringskod** för det dimensionsvärdet. Om inget dimensionsvärde har angetts för det konsoliderade företaget i fältet **Konsolideringskod** för det dimensionsvärdet, exporteras själva dimensionsvärdet till raden.  
4. XML-filerna innehåller dessutom valutakurserna i konsolideringsperioden. Dessa kurser placeras i ett separat avsnitt i början av filen.  

## <a name="see-also"></a>Se även

[Ställa in företagskonsolidering](finance-consolidated-company-reporting-setup.md)  
[Hantera koncerninterna transaktioner](intercompany-manage.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportera affärsdata till Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
