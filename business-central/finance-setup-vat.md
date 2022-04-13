---
title: Ställa in moms
description: Se till att du korrekt beräknar, bokför och rapporterar om moms för försäljning och inköp. Vi rekommenderar att du använder den assisterade konfigurationsguiden för att ställa in momsen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.search.form: 10, 1877, 470, 471, 472
ms.date: 03/04/2022
ms.author: bholtorf
ms.openlocfilehash: 285f0f224853837e2aac6553c34d366afb09f08a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519231"
---
# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Konfigurera beräknings- och bokföringsmetoder för moms

Konsumenter och företag betalar moms när de köper varor eller tjänster. Momsbeloppet att betala kan variera beroende på flera faktorer. I [!INCLUDE[prod_short](includes/prod_short.md)] ställer du in moms för att ange de satser som ska användas för beräkning av momsbelopp baserat på följande parametrar:

* Vem du säljer till  
* Vem du köper från  
* Vad du säljer  
* Vad du köper  

Du kan ställa in momsberäkningar manuellt, men det kan vara svårt och tidsödande. Om du vill göra det enklare, finns det en assisterade konfigurationsguid med namnet **momsinställning** som hjälper dig med stegen. Vi rekommenderar att du använder den assisterade konfigurationsguiden för att ställa in momsen.

> [!NOTE]  
> Du kan endast använda guiden om du har skapat ett Mitt företag och inte har bokfört transaktioner som inkluderar moms. Annars skulle vara mycket emkelt att använda olika momssatser av misstag, och göra felaktiga momsrapporter.  

Om du vill ställa in momsberäkningar själv eller bara vill ha information om varje steg, innehåller denna artikel beskrivningar av varje steg.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Använd den assisterade konfigurationsguiden för att ställa in momsen (rekommenderat)

Vi rekommenderar att du använder den assisterade konfigurationsguiden för att ställa in momsen i [!INCLUDE[prod_short](includes/prod_short.md)].

Så här startar du den assisterade konfigurationsguiden:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **assisterad konfiguration**.  
2. Välj **Ställ in moms** och slutför stegen.
3. När du har slutfört den assisterade konfigurationen går du till sidan **Bokföringsinställning för moms** och kontrollerar om du behöver fylla i ytterligare fält enligt de lokala kraven för din version av [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Lokala funktioner i Business Central](about-localization.md).  

### <a name="check-the-vat-posting-setup"></a>Kontrollera bokföringsinställningar för moms

För att hjälpa dig komma igång snabbt visar [!INCLUDE [prod_short](includes/prod_short.md)] dig meddelanden om redovisningskonton saknas i bokföringsmallar eller bokföringsinställningar, till exempel sidan **Bokföringsinställningar för moms**. Du kan ändra den här typen av meddelande med hjälp av meddelandet *Redovisningskonton som saknas i bokföringsmall eller inställning* på sidan **Mina meddelanden**. Gå helt enkelt till sidan **Mina inställningar** och välj sedan *Ändra när jag erhåller meddelanden.* länk.  

Om du väljer ett sådant meddelande skapar [!INCLUDE [prod_short](includes/prod_short.md)] automatiskt dessa bokföringsinställningar baserat på bokföringsmallarna i det dokument eller den journal som du arbetar med.  

I detta skede kanske du bara fyller i de saknade redovisningskontona. När du senare sedan finjusterar installationen ytterligare kanske du inser att konfigurationen var fel. [!INCLUDE [prod_short](includes/prod_short.md)] tillåter inte borttagning av momsbokföringsinställningar och allmänna bokföringsinställningar när transaktioner skapas baserade på sådana konfigurationer. Från och med 2022 års utgivningscykel 1 kan du använda fältet **Spärrat** i fönstret **Bokföringsinställningar för moms** för att förhindra att användare av misstag använder en konfiguration som inte längre är relevant för nya bokföringar.

## <a name="set-up-vat-registration-numbers-for-your-country-or-region"></a>Så här skapar du momsregistreringsnummer för land / region

För att garantera att användaren anger ett giltigt momsregistreringsnummer kan du ange format för momsregistreringsnummer som används i de länder eller regioner där du bedriver verksamhet. [!INCLUDE[prod_short](includes/prod_short.md)] visar ett felmeddelande när någon gör fel eller använder ett format som är felaktigt för landet / regionen.

Om du vill skapa momsregistreringsnummer, gör då så här:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 2.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **länder/regioner**.
2. Välj land eller region, och välj sedan åtgärden **Format för momsreg.nr.**.
3. I fältet **Format** anger du formatet genom att ange ett eller flera av följande tecken:  

* **#** Kräver ett tal med en enda siffra.  
* **@** Kräver en bokstav. Detta format är inte skiftlägeskänsliga.  
* **?** Alla tecken tillåtna.  

    > [!Tip]
    > Du kan använda andra tecken förutsatt att dessa förekommer i landets/regionens format. Om du till exempel behöver inkludera en punkt eller ett bindestreck mellan olika uppsättningar siffror kan du exempelvis definiera formatet som ##.####.### or @@-###-###.  

## <a name="set-up-vat-business-posting-groups"></a>Skapa rörelsebokföringsmallar för moms

Rörelsebokföringsmallar för moms representerar de marknader där du gör affärer med kunder och leverantörer och definierar hur moms beräknas och bokförs på varje marknad. Exempel på momsrörelsebokföringsmallar är **Inhemsk** och **Europeiska unionen (EU)**.  

Använd koder som är lätta att komma ihåg och som beskriver rörelsebokföringsmallen som t. ex. **EU**, **Icke-EU** eller **Inhemsk**. Koden måste vara unik. Du kan ställa in så många koder som du vill, men du kan inte använda samma kod mer än en gång i en tabell.

Om du vill konfigurera rörelsebokföringsmall för moms, gör du följande steg:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Moms rörelsebokföringsmall** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs.

Du kan skapa standardrörelsebokföringsmallar för moms genom att koppla rörelsebokföringsmallar för moms till generella rörelsebokföringsmallar. [!INCLUDE[prod_short](includes/prod_short.md)] tilldelar automatiskt rörelsebokföringsmallen för moms när du tilldelar rörelsebokföringsmallen till ett kund-, leverantörs- eller redovisningskonto.

## <a name="set-up-vat-product-posting-groups"></a>Skapa produktbokföringsmallar för moms

Produktbokföringsmallar för moms representerar objekten och resurser och som köper och säljer, och bestämmer hur du beräknar och bokför typen av artikel som köps in eller säljs.  
Det är praktiskt att använda koder som är lätta att komma ihåg och som beskriver satsen som **ej moms** eller **noll**, **moms10** eller **reducerad** 10 % moms och **moms25** eller **standard** för 25 %.

Om du vill konfigurera rörelsebokföringsmall för moms, gör du följande steg:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Moms produktbokföringsmallar** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Kombinera momsbokföringsmallar i momsbokföringsinställningar

[!INCLUDE[prod_short](includes/prod_short.md)] beräknar momsbeloppen på försäljning och inköp utifrån momsbokföringsinställningar som är kombinationer av rörelsebokföringsmallar för moms och produktbokföringsmallar för moms. För varje kombination kan du fylla i momsprocent, momsberäkningstyp och redovisningskonton för bokföring av moms som relaterar till försäljning, inköp och omvänd moms. Du kan också ange om momsbelopp ska omberäknas när en kassarabatt används eller tas emot.  

Du kan registrera så många kombinationer som du vill. Om du vill gruppera kombinationer av momsbokföringsinställningar med liknande attribut kan du ange ett **Moms-ID** för varje grupp och tilldela ID:t till gruppmedlemmarna.

Om du vill kombinera momsbokföringsinställningar gör du följande:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 5.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokföringsinställningar för moms** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Tilldela momsbokföringsmallar som standard till flera enheter

Om du vill använda samma momsbokföringsmallar för flera poster kan du skapa [!INCLUDE[prod_short](includes/prod_short.md)] för att göra detta som standard. Detta kan göras på ett par sätt:

* Du kan tilldela rörelsebokföringsmallar för moms till generella rörelsebokföringsmallar eller kund- och leverantörsmallar
* Du kan tilldela produktbokföringsmallar för moms från generella produktbokföringsmallar  

Rörelsebokföringsmallen eller produktbokföringsmallen för moms tilldelas när du väljer en rörelse- eller produktbokföringsmall för en kund, leverantör, artikel eller resurs.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Tilldela momsbokföringsmallar till konton, kunder, leverantörer, artiklar och resurser

I följande avsnitt beskrivs hur du tilldelar momsbokföringsmallar till enskilda enheter.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Så här tilldelar du momsbokföringsmallar till individuella redovisningskonton

1. Välj den ![Glödlampa som öppnar funktionen Berätta 6.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.  
2. Öppna kortet **redovisningskontokortet** för det kontot.  
3. På snabbfliken **bokföring** i fältet **Typ av bokföring** väljer du antingen **försäljning** eller **inköp**.  
4. Välj momsbokföringsmallar för försäljnings- eller inköpskontot.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>För att tilldela rörelsebokföringsmallar för moms till kunder och leverantörer

1. Välj den ![Glödlampa som öppnar funktionen Berätta 7.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** eller **Leverantör** och väljer sedan relaterad länk.  
2. På kortet **Kund** eller **Leverantör** expanderar du snabbfliken **Fakturering**.  
3. Välj rörelsebokföringsmallar för moms.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>För att tilldela produktbokföringsmallar till individuella artiklar och resurser

1. Välj den ![Glödlampa som öppnar funktionen Berätta 8.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikel** eller **Resurs** och väljer sedan relaterad länk.  
2. Gör något av följande:  

    * På kortet **Item**  expandera snabbfliken **pris och bokföring** och välj **visa fler** för att visa fältet **Moms produktbokföringsmall**.  
    * På kortet **Resurs** expanderar du snabbfliken **Fakturering**.  
3. Välj produktbokföringsmallen med moms.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Ange satser som förklarar momsbefrielse eller icke-standardiserade momssatser

Du konfigurerar en momsklausul som beskriver information om vilken typ av moms som tillämpas. Informationen kan krävas av Myndighetsregleringar. När du registrerar en momsklausul och associera den med en momsbokföringsinställning, visas momsklausulen på alla utskrivna försäljningsdokument som använder momsbokföringsinställningsmallen.

Om det behövs kan du också ange hur man konverterar momsklausuler till andra språk. När du sedan skapar och skriver ut ett försäljningsdokument som innehåller ett moms-ID, kommer dokumentet att ta med den översatta momsklausulen. Den språkkod som anges på kundkortet bestämmer språket.

När icke-standardmässiga momssatser används i olika typer av dokument, t. ex. fakturor eller kreditnotor, behöver företagen vanligtvis inkludera en undantagstext (momsklausul) som anger varför en reducerad momssats eller noll-momssats har beräknats. Du kan definiera olika momsklausuler som ska ingå i affärsdokumenten per dokumenttyp, t. ex. faktura eller kreditnota. Det gör du på sidan **Momsklausuler per dokumenttyp**.

Du kan ändra eller ta bort en momsklausul och dina ändringar kommer visas i en generarad rapporten. [!INCLUDE[prod_short](includes/prod_short.md)] sparar dock ingen historik över ändringen. I rapporten skrivs momsklausulbeskrivningarna ut, och visas för alla rader i rapporten tillsammans med momsbeloppet och nettobeloppet. Om en momsklausul inte har angetts för alla rader på försäljningsdokumentet, utelämnas hela avsnittet, när rapporten skrivs ut.

### <a name="to-set-up-vat-clauses"></a>Så här konfigurerar du momsklausuler

1. Välj den ![Glödlampa som öppnar funktionen Berätta 9.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Momsklausuler** och väljer sedan relaterad länk.  
2. På sidan **momsklusuler** skapar du en ny rad.  
3. I fältet **Kod** anger du en identifierare för klausulen. Du använder den här koden för att tilldela klausulen till momsbokföringsmallar.  
4. I fältet **Beskrivning** anger du den text för momsundantag som ska visas i dokument som kan inkludera moms. I fältet **Beskrivning 2** anger du ytterligare text om det behövs. Texten kommer visas på nya dokumentrader.
5. Välj åtgärden **Beskrivning efter dokument typ**.
6. På sidan **Momsklausuler per dokumenttyp** fyller du i fälten för att ange vilken momsbefrielsetext som ska visas för vilken dokumenttyp.  
7. Tillval: Om du vill tilldela momsklausulen till en momsbokföringsinställning direkt väljer du **Inställningar**, och väljer sedan klausulen. Om du vill vänta kan du tilldela klausulen vid ett senare tillfälle på sidan **Bokföringsinställningar för moms**.  
8. Valfritt: Att ange hur man översätter momsklausulen, välj åtgärden **översättningar**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Så här tilldelar du en momsklausul till en momsbokföringsinställning

1. Välj den ![Glödlampa som öppnar funktionen Berätta 10.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokföringsinställningar för moms** och väljer sedan relaterad länk.  
2. I kolumnen **momsklausul** väljer du klausul för varje momsbokföringsinställning som den gäller för.  

### <a name="to-specify-translations-for-vat-clauses"></a>Att ange översättningar för momsklausuler

1. Välj den ![Glödlampa som öppnar funktionen Berätta 11.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Momsklausuler** och väljer sedan relaterad länk.  
2. Välj åtgärden **Översättningar**.  
3. I fältet **språkkod** välj det språk du översätta till.  
4. I fältet **Beskrivning** och **Beskrivning 2** anger du översättning av beskrivningarna. Denna text visas i det översatta momsrapportdokument.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Skapa en momsbokföringsinställning för hantering av importmoms

Du använder funktionen för *importmoms* när du bokför ett dokument där hela beloppet är moms. Du använder detta om du får en faktura med moms för importerade varor från skattemyndigheterna.  

Så här anger du koder för importmoms:  

1. Välj den ![Glödlampa som öppnar funktionen Berätta 12.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Moms produktbokföringsmallar** och väljer sedan relaterad länk.  
2. På sidan Bokföringsmallar för momsprodukter anger du en ny produktbokföringsmall för importmoms.  
3. Välj den ![Glödlampa som öppnar funktionen Berätta 13.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokföringsinställningar för moms** och väljer sedan relaterad länk.  
4. På sidan Bokföringsmallar för momsprodukter skapar du en ny rad eller använder valfri befintlig rörelsebokföringsmall för moms i kombination med den nya produktbokföringsmallen för moms för importmoms.  
5. I fältet **Momsberäkningstyp** väljer du **enbart moms**.  
6. Ange det redovisningskonto som ska användas för att bokföra importmoms i fältet **Ingående moms**. Alla andra konton är valfria.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Använda omvänd moms för handel mellan länder/regioner inom EU

En del företag måste använda omvänd moms när de handlar med andra företag. Regeln gäller för inköp från länder/regioner inom EU och försäljning till länder/regioner inom EU.  

> [!NOTE]  
> Denna regel gäller vid handel med företag som är registrerade som momspliktiga i ett annat land eller en annan region inom EU. Om du handlar direkt med konsumenter i andra länder/regioner inom EU bör du kontakta skattemyndigheterna för att få information om gällande momsregler.  

> [!TIP]  
> Du kan verifiera att ett företag som är registrerat som momspliktigt i ett annat EU-land genom att använda tjänsten validering av EU-momsregistreringsnummer. Tjänsten är tillgänglig utan kostnad i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [kontrollera momsregistreringsnummer](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countries-or-regions"></a>Försäljning till länder eller regioner inom EU

Ingen moms beräknas på försäljning till momspliktiga företag i andra länder/regioner inom EU. Du måste rapportera värdet för försäljningar till länder/regioner inom EU separat i momsrapporten.  

För att korrekt beräkna moms på försäljning till länder/regioner inom EU bör du:  

* Lägg upp en rad för försäljning med samma information för inköp. Om du redan har lagt upp rader på sidan Bokföringsinställning för moms för inköp från andra länder/regioner inom EU kan du även använda dessa rader för försäljning.  
* Tilldela rörelsebokföringsmallar för moms i fältet **Moms rörelsebokföringsmall** på snabbfliken **Fakturering** på leverantörskortet för varje EU-leverantör. Du bör också ange kunden momsregistreringsnummer i fältet **Momsregistreringsnr** på Snabbfliken **Utlandshandel**.  

När du bokför en försäljning till en kund i ett annat land eller en annan region inom EU beräknas momsbeloppet och en momstransaktion skapas med informationen om omvänd moms och nettobeloppet (det belopp som används för att beräkna momsbeloppet). Inga poster bokförs på momskontona i redovisningen.

## <a name="vat-rounding-for-documents"></a>Momsavrundning för dokument

Belopp i dokument som ännu inte har bokförts avrundas och visas på ett sätt som motsvarar den slutliga avrundningen av belopp som faktiskt bokförs. Moms beräknas för ett färdigt dokument, vilket innebär att moms som beräknas baseras på summan av alla rader med samma moms-id i dokumentet.  

## <a name="set-up-vat-reporting"></a>Konfigurera momsrapportering

Du måste ställa in information om hur skattemyndigheterna i ditt land eller din region kräver att du skickar in momsrapporter. Följande steg visar vilken information som används oftast. Du kan emellertid behöva ytterligare åtgärder för ditt land eller din region. Mer information finns i relevant artikel i avsnittet *Lokala funktioner* i panelen till vänster.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-also"></a>Se även

[Ställa in momsrapportmallar och momsrapportnamn](finance-how-setup-vat-statement.md)  
[Ställa in orealiserad mervärdesskatt](finance-setup-unrealized-vat.md)  
[Rapportera moms till skattemyndigheterna](finance-how-report-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Arbeta med ändringsverktyget för momssats](finance-how-use-vat-rate-change-tool.md)  
[Kontrollera momsregistreringsnummer](finance-how-validate-vat-registration-number.md)  
[Lokal funktionalitet i Business Central](about-localization.md)  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
