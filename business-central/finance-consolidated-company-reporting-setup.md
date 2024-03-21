---
title: Konfigurera företagskonsolidering
description: Lär dig hur du kan konfigurera hur data från olika företag i Business Central rapporteras till ett konsolideringsföretag.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 09/25/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# <a name="set-up-company-consolidation"></a>Ställa in företagskonsolidering

Innan du kan konsolidera redovisningstransaktionerna för två eller flera separata företag (dotterbolag) till ett konsoliderat företag måste du förbereda kontoplaner och konsolideringsföretag.  

Det finns två sätt att ställa in konsolideringen beroende på hur komplicerat ditt företag är:

* Om du inte behöver avancerade inställningar, exempelvis genom att inkludera ett företag som du bara äger en del av, kan du använda den assisterade konfigurationsguiden **Företagskonsolidering** för att snabbt skapa en konsolidering. Guiden hjälper dig att följa de grundläggande stegen.
* Om du behöver mer avancerade inställningar kan du själv ställa in det konsoliderade företaget och affärsenheterna.
  * I varje affärsenhet anger du vilka redovisningskonton som ska inkluderas i konsolideringen, samt anger omräkningsmetoden för respetive konto.
  * I det konsoliderade företaget skapar du ett affärsenhetskort för varje företag som ska inkluderas i konsolideringen. Affärsenhetskortet innehåller information, till exempel datumen för affärsenhetens räkenskapsår och procentandelen av varje konto som ska inkluderas i konsolideringen.

## <a name="simple-consolidation-setup"></a>Enkel konsolidering

Om din konsolidering är enkel, till exempel eftersom du helt äger de affärsenheter som ska konsolideras, kommer guiden **Företagskonsolidering** att hjälpa dig med följande steg:

* Skapa ett nytt konsoliderat företag, eller konsolidera ett företag som du redan har skapat. Företaget bör inte innehålla transaktioner.
* Förhandsgranska resultatet. [!INCLUDE[prod_short](includes/prod_short.md)] verifierar att du kan överföra huvuddata och transaktioner till det konsoliderade företaget.

Så här använder du den assisterade konfigurationsguiden:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Assisterad konfiguration** och väljer sedan relaterad länk.
2. Välj **Behandla konsolideringar** och slutför sedan varje steg i den assisterade konfigurationsguiden för företagskonsolidering.

## <a name="advanced-consolidation-setup"></a>Avancerad konsolidering

Om du behöver mer avancerade inställningar för en konsolidering kan du konfigurera konsolideringen manuellt. Om du till exempel har kunder som du delvis äger, eller om du har företag som du inte vill inkludera.  

### <a name="set-up-the-consolidated-company"></a>Ange det konsoliderade företaget

Först måste du konfigurera det konsoliderade företaget. Du kan lägga upp det konsoliderade företaget i en databas på samma sätt som du lägger upp andra företag. Mer information om hur du konfigurerar ett företag finns i [Göra sig redo att göra affärer](ui-get-ready-business.md).  

I följande lista visas de viktigaste aspekterna av det konsoliderade företaget.

1. Konfigurera kontoplan.

    Om du vill veta mer om hur du ställer in en kontoplan går du till [Konfigurera eller ändra kontoplaner](finance-setup-chart-accounts.md).  

    Kontoplanen kan vara identisk över en affärsenhet och det konsoliderade företaget, eller så kan det konsoliderade företaget ha olika kontoplaner. Om en affärsenhets kontoplan skiljer sig från det konsoliderade företagets måste du mappa kontona till kontona i affärsenheten. Mer information finns i avsnittet [Förbereda redovisningskonton för konsolidering](#glacc).

2. Lägg till affärsenheter.

    Om du vill konsolidera data från flera företag måste du lägga upp dotterbolagen som affärsenheter och ange hur mycket av deras saldon som ska inkluderas. Om du vill veta mer om affärsenheter går du till avsnittet [Lägg till affärsenheter](#busunit).

3. Ange valutakurser om det behövs.

    Ange valutakurser om du ska konsolidera data för affärsenheter som använder olika valutor. De tre valutakurser som du kan använda är **Genomsnittskurs (manuell)**, **Slutkurs** och **Senaste slutkurs**. Mer information om valutakurser finns i avsnittet [Ange valutakurser för konsolideringar](#exchrates).

4. Konsolidera dimensionsinformation såväl som redovisningskonton.

    Mer information finns i avsnittet [Inkludera eller exkludera dimensioner](#dim).

### <a name="add-business-units"></a><a name="busunit"></a>Lägg till affärsenheter

I det konsoliderade företaget konfigurerar du varje företag som du vill konsolidera data från som en affärsenhet. Innan du kör en konsolidering och genererar konsolideringsrapporten är det en bra idé att verifiera de ekonomiska uppgifterna i respektive affärsenhet.

En stor del av att skapa affärsenheten är att ange hur enheten ska dela sina ekonomiska data med det konsoliderade företaget. Det finns manuella och automatiska alternativ:

* Om du vill använda en manuell process såväl för [!INCLUDE [prod_short](includes/prod_short.md)] online som lokalt, kan du exportera en XML-fil som innehåller enhetens redovisningstransaktioner. Importera sedan filen i det konsoliderade företaget.
* För att automatisera dataintegrationen kan du för [!INCLUDE [prod_short](includes/prod_short.md)] online använda ett API som [!INCLUDE [prod_short](includes/prod_short.md)] tillhandahåller för att dela data mellan miljöer. Om dina företag finns i samma miljö kan du använda alternativet **Databas**.

> [!NOTE]
> Med API-alternativet kan du också dela redovisningstransaktioner från andra [!INCLUDE [prod_short](includes/prod_short.md)]-miljöer. Om du vill använda API-alternativet måste användaren som konfigurerar konsolideringen ha behörighet att komma åt redovisningstransaktioner. Behörighetsuppsättningarna D365 Basic och D365 Read ger till exempel åtkomst.

1. Logga in på det konsoliderade företaget.
2. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **affärsenhet** och väljer sedan relaterad länk.  
3. Välj **Ny** och fyll sedan i erforderliga fält på snabbflikarna **Allmänt** och **Redovisningskonton**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > När du fyller i fältet **startdatum** och **slutdatum**, se till att du följer GAAP-reglerna för räkenskapsperioder för affärsenheten jämfört med moderbolag.
4. På snabbfliken **Dataimport**, i fältet **Standarddataimport** anger du hur redovisningstransaktioner sak delas med det konsoliderade företaget:

   * Om du vill dela data mellan företag i samma miljö väljer du **Databas**.
   * Om du vill dela data mellan företag i olika miljöer väljer du **API** och fyller sedan i fältet **Slutpunkt för API**.
        
        Om du vill hämta slutpunkts-URL:en öppnar du sidan **Affärsenhetskort** i företagets [!INCLUDE [prod_short](includes/prod_short.md)] och väljer åtgärden **Inställningar**. 
   * Om du vill exportera en XML-fil och dela den manuellt väljer du **Filformat**.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Förbereda redovisningskonton för konsolidering

Kontoplanen för ett företag som ska konsolideras måste innehålla konton för konsolidering. För respektive redovisningskonto i respektive företag måste du ange vilket redovisningskonto i det konsoliderade företaget som saldot ska överföras till. Med den här mappningen kan du konsolidera företag som har olika kontoplaner.

Om kontoplanen i affärsenheten skiljer sig från det konsoliderade företaget måste du förbereda redovisningskonton för konsolidering. Du kan ange vilka konton som ska bokföra debet- och kreditbelopp och metoden du använder för att översätta valutor i det konsoliderade företaget.

1. I varje affärsenhet [!INCLUDE [prod_short](includes/prod_short.md)], välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.  
2. Öppna kortet för kontot och fyll sedan i fälten på snabbfliken **konsolidering**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a>Ange valutakurs för konsolidering

Om en affärsenhet har en annan valuta än det konsoliderade företaget, måste du ange valutakurser för metoder för varje konto innan du konsoliderar. För varje konto bestämmer innehållet i **Konsoliderad omräkningsmetod** valutakursen. I det konsoliderade företaget, på varje affärsenhetskort, i fältet **Valutakurstabell**, anger du om konsolideringen ska använda valutakurser från affärsenheten eller det konsoliderade företaget. Om du använder valutakurser från det konsoliderade företaget kan du ändra valutakurserna för en affärsenhet. För affärsenheter, om fältet **Valutakurstabell** innehåller **Lokal** kan du ändra valutakursen från affärsenhetskortet. Valutakurserna kopieras från tabellen **Valutakurs**, men du kan ändra dem före konsolideringen.

Följande tabell beskriver valutakursmetoderna som du kan använda för konton.

|Växlingskurs | Normal användning |
|---|---|
|Genomsnittskurs (manuell) | Du kan beräkna genomsnittskurs manuellt för den period som ska konsolideras. Beräkna genomsnittet antingen som ett aritmetiskt genomsnitt eller som en bästa uppskattning och ange resultatet för varje affärsenhet. Används för resultaträkningskonton.|
|Slutkurs | Används för balansräkningskonton.|
|Senaste slutkurs | Kursen som var giltig på den utländska valutamarknaden vid den tidpunkt då balansräkningen eller resultaträkningen förbereds för. Du registrerar denna kurs för varje affärsenhet. Används för balansräkningskonton.|
|Historisk kurs | Valutakursen som användes när transaktionen genomfördes.|
|Sammansatt kurs | Den aktuella perioden omräknas med den genomsnittliga kursen och läggs till det tidigare registrerade saldot i det konsoliderade företaget. Du använder vanligtvis den här metoden för konton för balanserade vinster. Dessa konton innehåller belopp från olika perioder, vilket innebär att de innehåller belopp som omräknats med olika växelkurser.|
|Aktiekurs | Detta alternativ liknar **Sammansatt**. Skillnades bokförs på olika redovisningskonton.|

Om du vill ange valutakurs för affärsenheter gör du följande:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **affärsenhet** och väljer sedan relaterad länk.  
2. På sidan **Affärsenhetslista** väljer du affärsenhet och sedan åtgärden **Genomsnittskurs (manuell)**.  
3. På sidan **Ändra valutakurser** har innehållet i fältet **Relationsvalutakurs** kopierats från tabellen **Valutakurs**, men det går att ändra värdet. Stäng sidan.  
4. Välj åtgärden **Slutkurs**.  
5. På fältet **Relations- valutakurs belopp** anger du valutakursen.

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Inkludera eller exkludera dimensioner

Du kan konsolidera dimensionsinformation såväl som redovisningskonton.

* På de aktuella dimensionerna anger du fältet **Konsolideringskod** eller lämnar fältet tomt.
  * Om du vill utesluta en dimension i konsolideringen lämnar du fältet **Konsolideringskod** tomt i dimensionen, och väljer inte dimensioner i fälten **Kopiera dimensioner** i några som helst konsolideringsfunktioner eller rapporter.
  * Lämna fältet **Konsolideringskod** tomt om du vill inkludera dimensionsinformation i konsolideringen. Konsolideringen fungerar dock endast om dimensionsvärdena i affärsenheten är samma som i det konsoliderade företaget.
  * För att konsolidera dimensionsvärdekoden i affärsenheten med en annan dimensionsvärdekod i det konsoliderade företaget fyller du i fältet **Konsolideringskod** för dimensionerna.  
* Lägg till dimensioner på relevanta redovisningskonton.

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Exkludera ett företag från konsolidering

Om du inte vill inkludera en affärsenhet i konsolideringen kan du exkludera den. Om du vill göra det, öppnar du affärsenhetskortet och avmarkerar kryssrutan **Konsolidera**.

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Inkludera ett delvis ägt företag i konsolideringen

Om du bara äger en del av ett företag kan inkludera en procentandel av varje transaktion som motsvarar den procentandel som du äger. Om du äger 70 % av företaget kommer konsolideringen till exempel att innehålla 70 SEK av en faktura på 100 SEK. Om du vill ange hur stor procentandel av företaget du äger går du till affärsenhetskortet och anger procentsatsen i fältet **Konsolideringsgrad %**.  

## <a name="see-also"></a>Se även

[Konsolidera ekonomiska data från flera företag](finance-consolidated-company-reporting.md)  
[Hantera koncerninterna transaktioner](intercompany-manage.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportera affärsdata till Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
