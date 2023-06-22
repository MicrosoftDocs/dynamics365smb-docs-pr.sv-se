---
title: Ställa in företagskonsolidering
description: Lär dig hur du kan konfigurera hur data från olika företag i Business Central rapporteras till ett konsolideringsföretag.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="set-up-company-consolidation" />Ställa in företagskonsolidering

Innan du kan konsolidera redovisningstransaktionerna för två eller flera separata företag (dotterbolag) till ett konsoliderat företag måste du förbereda kontoplaner och konsolideringsföretaget.  

Det finns två sätt att ställa in konsolideringen beroende på hur komplicerat ditt företag är:

* Om du inte behöver avancerade inställningar, exempelvis med ett företag som du bara har en del av, kan du använda den assisterade konfigurationen **Företagskonsolidering** för att snabbt skapa en konsolidering. Guiden hjälper dig att följa de grundläggande stegen.
* Om du behöver mer avancerade inställningar kan du ställa in det konsoliderade företaget och koncernföretagen själv.
  * I varje affärsenhet anger du vilka redovisningskonton som ska inkluderas i konsolideringen, och ange omräkningsmetoden för konsolidering för varje konto.
  * I det konsoliderade företaget konfigurerar du ett affärsenhetskort för varje företag som ska inkluderas i konsolideringen. Affärsenhetskortet innehåller information, till exempel datumen för affärsenhetens räkenskapsår och procentandelen av varje konto som måste inkluderas i konsolideringen.

## <a name="simple-consolidation-setup" />Enkel konsolidering

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]
Om din konsolidering är enkel, till exempel eftersom du äger de koncernföretag som ska konsolideras helt, kommer den assisterade konfigurationen **Företagskonsolidering** att hjälpa dig med följande steg:

* Välj om du vill skapa ett nytt konsoliderat företag eller om du vill konsolidera data i ett företag som du har skapat för konsolideringen. Företaget bör inte innehålla transaktioner.
* Förhandsgranska resultatet. [!INCLUDE[prod_short](includes/prod_short.md)] verifierar att huvuddata och transaktioner kan överföras till det konsoliderade företaget.

Så här använder du den assisterade konfigurationsguiden:

1. I rollcentret **Revisor** väljer du åtgärden **Assisterad konfiguration**.
2. Välj **Ställ in konsolideringsrapportering** och slutför sedan varje steg i den assisterade konfigurationsguiden.

## <a name="advanced-consolidation-setup" />Avancerad konsolidering

Om du behöver mer avancerade inställningar för en konsolidering kan du konfigurera konsolideringen manuellt. Till exempel om du har kunder som du endast delvis äger eller om du har kunder som du inte vill inkludera i konsolideringen.  

### <a name="set-up-the-consolidated-company" />Konfigurera det konsoliderade företaget

Först måste du konfigurera det konsoliderade företaget. Du kan lägga upp det konsoliderade företaget i en databas på samma sätt som du lägger upp andra företag. Mer information finns i [Komma igång med att göra affärer](ui-get-ready-business.md).  

I följande lista visas de viktigaste aspekterna av det konsoliderade företaget.

1. Konfigurera kontoplan

    Mer information finns i [Ställa in eller ändra kontoplanen](finance-setup-chart-accounts.md).  

    Kontoplanen kan vara identisk över en affärsenhet och det konsoliderade företaget, eller så kan det konsoliderade företaget ha olika kontoplaner. Om en affärsenhets kontoplan skiljer sig från det konsoliderade företagets måste du ange kopplingen mellan konton på kontona i affärsenheten. Mer information finns i avsnittet [Förbereda redovisningskonton för konsolidering](#glacc).

2. Lägg till affärsenheter

    Om du vill konsolidera flera företags ekonomiska information i ett konsoliderat företag måste du ange information om dotterbolaget som affärsenhet som ska inkluderas och i vilken utsträckning som siffrorna ska inkluderas.

    Mer information finns i avsnittet [Lägga till affärsenheter](#busunit).
3. Du kan ange valutakurser när du konsoliderar de ekonomiska rapporterna för affärsenheter om de ekonomiska rapporterna är i en utländsk valuta.

    De tre valutakurser som används är **Genomsnittskurs (manuell)**, **Slutkurs** och **Senaste slutkurs**. Mer information finns i avsnittet [Ange valutakurser för konsolideringar](#exchrates).
4. Du kan konsolidera dimensionsinformation såväl som redovisningskonton.

    Mer information finns i avsnittet [Inkludera eller exkludera dimensioner](#dim).

### <a name="a-namebusunitaadd-business-units" /><a name="busunit"></a>Lägg till affärsenheter

[!INCLUDE[prod_short](includes/prod_short.md)] låter dig lägga upp en lista över affärsenheter som ska konsolideras, verifiera redovisningsinformation innan du konsoliderar dem, importera filer och generera konsolideringsrapporter.  

1. Logga in på det konsoliderade företaget.
2. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **affärsenhet** och väljer sedan relaterad länk.  
3. Välj **Ny** och fyll sedan i relevanta fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > När du fyller i fältet **startdatum** och **slutdatum**, se till att du följer GAAP-reglerna för räkenskapsperioder för affärsenheten jämfört med moderbolag.
4. Upprepa steg 3 för varje ytterligare affärsenhet

Om en utländsk valuta används för koncernföretaget måste du ange vilken valutakurs som ska användas vid konsolideringen. Dessutom måste du ange konsolideringsinformation på koncernföretagets redovisningskonton. De här processerna beskrivs i följande avsnitt.

### <a name="a-nameglaccaprepare-general-ledger-accounts-for-consolidation" /><a name="glacc"></a>Förbereda redovisningskonton för konsolidering

Kontoplanen för ett företag som ska konsolideras måste innehålla konton för konsolidering. Du måste ange vilket redovisningskonto i det konsoliderade företaget som saldot ska överföras till vid konsolideringen för varje redovisningskonto i alla företag. Detta är en koppling som gör det möjligt för företag med olika kontoplaner att konsolideras tillsammans.

Om kontoplanen i affärsenheten skiljer sig från det konsoliderade företaget måste du förbereda redovisningskonton för konsolidering. Du kan ange vilka konton som ska bokföra debet- och kreditbelopp och metoden du använder för att översätta valutor i det konsoliderade företaget. Detta är till exempel användbart om du kör rapporten ofta.

1. I varje affärsenhet [!INCLUDE [prod_short](includes/prod_short.md)], välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.  
2. Öppna kortet för kontot och fyll sedan i fälten på snabbfliken **konsolidering**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="a-nameexchratesaspecify-exchange-rates-for-consolidations" /><a name="exchrates"></a>Ange valutakurs för konsolidering

Om en affärsenhet har en annan valuta än det konsoliderade företaget, måste du ange valutakurser för metoder för varje konto innan du konsoliderar. För varje konto bestämmer innehållet i **Konsoliderad omräkningsmetod** valutakursen. I det konsoliderade företaget, på varje affärsenhetskort, i fältet **Valutakurstabell**, anger du om konsolideringen ska använda valutakurser från affärsenheten eller det konsoliderade företaget. Om du använder valutakurser från det konsoliderade företaget kan du ändra valutakurserna för en affärsenhet. För affärsenheter, om fältet **Valutakurstabell** innehåller **Lokal** kan du ändra valutakursen från affärsenhetskortet. Valutakurserna kopieras från tabellen **Valutakurs**, men du kan ändra dem före konsolideringen.

Följande tabell beskriver valutakursmetoderna som du kan använda för konton.

|Växlingskurs | Normal användning |
|---|---|
|Genomsnittskurs (manuell) | Du kan beräkna genomsnittskurs manuellt för den period som ska konsolideras. Beräkna genomsnittet antingen som ett aritmetiskt genomsnitt eller som en bästa uppskattning och ange resultatet för varje affärsenhet. Används för resultaträkningskonton.|
|Slutkurs | Används för balansräkningskonton.|
|Senaste slutkurs | Kursen som var giltig på den utländska valutamarknaden vid den tidpunkt då balansräkningen eller resultaträkningen förbereds för. Du registrerar denna kurs för varje affärsenhet. Används för balansräkningskonton.|
|Historisk kurs | Valutakursen som användes när transaktionen genomfördes.|
|Sammansatt kurs | Den aktuella perioden omräknas med den genomsnittliga kursen och läggs till det tidigare registrerade saldot i det konsoliderade företaget. Den här metoden används vanligtvis för konton för balanserade vinstmedel eftersom de innehåller belopp från olika perioder och är därför en summa av belopp som omräknats med olika växelkurser.|
|Aktiekurs | Detta liknar **Sammansatt**. Differenser bokförs på olika redovisningskonton.|

Om du vill ange valutakurs för affärsenheter gör du följande:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **affärsenhet** och väljer sedan relaterad länk.  
2. På sidan **Affärsenhetslista** väljer du affärsenhet och sedan åtgärden **Genomsnittskurs (manuell)**.  
3. På sidan **Ändra valutakurser** har innehållet i fältet **Relationsvalutakurs** kopierats från tabellen **Valutakurs**, men det går att ändra värdet. Stäng sidan.  
4. Välj åtgärden **Slutkurs**.  
5. På fältet **Relations- valutakurs belopp** anger du valutakursen.

### <a name="a-namedimainclude-or-exclude-dimensions" /><a name="dim"></a>Inkludera eller exkludera dimensioner

Du kan konsolidera dimensionsinformation såväl som redovisningskonton.

* På de aktuella dimensionerna anger du fältet **Konsolideringskod** eller lämnar fältet tomt
  * Om du vill utesluta en dimension i konsolideringen lämnar du fältet **Konsolideringskod** tomt i dimensionen och väljer inte dimensioner i fälten **Kopiera dimensioner** i några konsolideringsfunktioner eller rapporter.
  * Lämna fältet **Konsolideringskod** tomt om du vill inkludera dimensionsinformation i konsolideringen. Konsolideringen fungerar dock endast om dimensionsvärdena i affärsenheten är samma som i det konsoliderade företaget.
  * För att konsolidera dimensionsvärdekoden i affärsenheten med en annan dimensionsvärdekod i det konsoliderade företaget fyller du i fältet **Konsolideringskod** med relevanta dimensioner.  
* Lägg till relevanta dimensioner på relevanta redovisningskonton

### <a name="a-nameexcludeaexclude-a-company-from-consolidation" /><a name="exclude"></a>Exkludera ett företag från konsolidering

Om du inte vill inkludera en affärsenhet i konsolideringen kan du exkludera den. Om du vill göra det, öppnar du affärsenhetskortet och avmarkerar kryssrutan **konsolidera**.

### <a name="a-nameincludeainclude-a-partially-owned-company-in-consolidation" /><a name="include"></a>Inkludera ett delvis ägt företag i konsolidering

Om du bara äger en del av ett företag kan inkludera en procentandel av varje transaktion som motsvarar procentandelen av det företag som du äger. Om du äger 70 % av företaget kommer konsolideringen att innehålla 70 SEK av en faktura på 100 SEK. Om du vill ange hur stor procentandel av företaget du äger går du till affärsenhetskortet och anger procentsatsen i fältet **konsolideringsgrad %**.  

## <a name="see-also" />Se även

[Konsolidera ekonomiska data från flera företag](finance-consolidated-company-reporting.md)  
[Hantera koncerninterna transaktioner](intercompany-manage.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportera affärsdata till Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
