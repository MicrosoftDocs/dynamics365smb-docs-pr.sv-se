---
title: Ställa in moms
description: 'Se till att du korrekt beräknar, bokför och rapporterar om moms för försäljning och inköp. Vi rekommenderar att du använder den assisterade konfigurationsguiden för att ställa in momsen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '10, 118, 391, 470, 471, 472, 575, 734, 747, 748, 1877,'
ms.date: 01/31/2023
ms.author: bholtorf
---

# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Konfigurera beräknings- och bokföringsmetoder för moms

Konsumenter och företag betalar moms när de köper varor eller tjänster. Momsbeloppet att betala kan variera beroende på flera faktorer. I [!INCLUDE[prod_short](includes/prod_short.md)] ställer du in moms för att ange de satser som ska användas för beräkning av momsbelopp baserat på följande parametrar:

* Vem du säljer till  
* Vem du köper från  
* Vad du säljer  
* Vad du köper  

Du kan ställa in momsberäkningar manuellt, men det kan vara svårt och tidsödande. Annars skulle vara mycket emkelt att använda olika momssatser av misstag, och göra felaktiga momsrapporter. För att göra momsinställningen enklare rekommenderar vi att du använder den assisterade **momsinställning** som finns i produkten. 

Om du vill ställa in momsberäkningar själv eller bara vill ha information om varje steg, innehåller denna artikel beskrivningar av varje steg:  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="set-up-vat-using-the-assisted-setup-guide-recommended"></a>Ställ in moms med hjälp av guiden för assisterad konfiguration (rekommenderas)

> [!NOTE]
> Du kan endast använda guiden **Momsinställning** om du har skapat ett *Mitt företag* och inte har bokfört transaktioner som inkluderar moms.

Så här startar du den assisterade konfigurationsguiden:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **assisterad konfiguration**. 
2. Välj **Ställ in moms** och slutför stegen.
3. När du har slutfört den assisterade konfigurationen går du till sidan **Bokföringsinställning för moms** och kontrollerar om du behöver fylla i ytterligare fält enligt de lokala kraven för din version av [!INCLUDE [prod_short](includes/prod_short.md)]. Läs mer i [Lokal funktionalitet i Business Central](about-localization.md).  

### <a name="check-the-vat-posting-setup"></a>Kontrollera bokföringsinställningar för moms

För att hjälpa dig komma igång snabbt meddelar [!INCLUDE [prod_short](includes/prod_short.md)] dig om redovisningskonton saknas i bokföringsmallar eller bokföringsinställningar, till exempel sidan **Bokföringsinställningar för moms**. Du kan ändra den här typen av meddelande med hjälp av meddelandet *Redovisningskonton som saknas i bokföringsmall eller inställning* på sidan **Mina meddelanden**. Gå helt enkelt till sidan **Mina inställningar** och välj sedan *Ändra när jag erhåller meddelanden.* länk.  

Om du väljer ett sådant meddelande skapar [!INCLUDE [prod_short](includes/prod_short.md)] automatiskt dessa bokföringsinställningar baserat på bokföringsmallarna i det dokument eller den journal som du arbetar med.  

I detta skede kanske du bara fyller i de saknade redovisningskontona. När du senare sedan finjusterar installationen ytterligare kanske du inser att konfigurationen var fel. [!INCLUDE [prod_short](includes/prod_short.md)] tillåter inte borttagning av momsbokföringsinställningar och allmänna bokföringsinställningar när transaktioner skapas baserade på sådana konfigurationer. Från och med 2022 års utgivningscykel 1 kan du använda fältet **Spärrat** i fönstret **Bokföringsinställningar för moms** för att förhindra att användare av misstag använder en konfiguration som inte längre är relevant för nya bokföringar.

## <a name="set-up-a-default-vat-date-for-documents-and-journals"></a>Ställ in ett standarddatum för moms för dokument och journaler

Momsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] baseras på **momsdatumet** för att ta med momstransaktioner i momsrapporter under en momsperiod. Momsdatumet kan ändras i alla dokument och journaler, men du måste ange ett standardvärde för momsdatumet.

> [!NOTE]
> När du har bokfört dokumentet eller journalen visas **momsdatumet** på **Momstransaktioner** och **Redovisningstransaktioner** samt på det bokförda dokumentet.

Så här ställer du in ett standardvärde för ett momsdatum:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Redovisningsinställningar** och välj sedan relaterad länk.  
2. På snabbfliken **Allmänt**, i fältet **Standarddatum för moms**, väljer du antingen **Bokföringsdatum** eller **Dokumentdatum**.
3. Stäng sidan.  

> [!NOTE]
> Som standard är **standarddatumet för moms** **bokföringsdatumet**.

### <a name="enabling-or-disabling-the-vat-date-feature"></a>Aktivera eller inaktivera funktionen momsdatum

För vissa länder/regioner krävs att företag använder ett visst momsdatum, men andra länder/regioner är inte det. Vissa länder/regioner kräver också att företag ändrar moms datumet i särskilda situationer efter att de har bokförts, men andra länder tillåter inte ändringar av momsdatum. Om du vill tillåta olika kontexter kan du välja om du vill använda den här funktionen och i så fall i vilken grad.

Så här ställer du in nivån för användning av momsdatum:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Redovisningsinställningar** och välj sedan relaterad länk.  
2. På snabbfliken **Allmänt** i fältet **Användning av momsdatum** anger du i vilken grad du vill använda funktionen för momsdatum. Du kan välja mellan en av följande typer:

| Typ | Beskrivning |
|--------------------|-----------------------------------------|
| **Använd alla funktioner för momsdatum** | Allt som har att göra med **momsdatumet** fungerar som standard, så att du får maximalt **momsdatum**. Du kan ställa in datumet, ändra det i dokument, rapportera baserat på det och ändra datumet efter bokföringen så länge som perioden inte är stängd eller skyddad med tillåtna datum för bokföring. |
| **Använd men tillåt inte ändringar** | Allt som hör till **momsdatumet** fungerar som standard med ett undantag. Du kan inte ändra **momsdatumet** i **momstransaktioner**. |
| **Använder inte funktionen för momsdatum** | [!INCLUDE [prod_short](includes/prod_short.md)] döljs och gör fälten för **momsdatum** inte tillgängliga i dokument, journaler och transaktioner. **Standardmomsdatumet** kommer att konfigureras som **bokföringsdatum**. |

3. Stäng sidan.

> [!IMPORTANT]
> Även om du väljer alternativet **Använder inte funktionen för momsdatum**, [!INCLUDE [prod_short](includes/prod_short.md)] används **momsdatumet** i bakgrunden. Eftersom **Standarddatum för moms** konfigureras som **Bokföringsdatum** och du inte kan ändra det i det här fallet, får du samma funktion som om du inte använder den här funktionen. Fälten för **momsdatum** tas bort från alla sidor, men fältet finns fortfarande kvar i tabeller och rapporter som fungerar baserat på det.

### <a name="limiting-periods-for-posting-and-changing-the-vat-date"></a>Begränsa perioder för bokföring och ändring av momsdatumet

Du kan hindra andra från att bokföra eller ändra momstransaktioner inom ett visst datumintervall. Du anger begränsningen med hjälp av två inställningar:

* Baserat på stängd **momsreturperiod**
* Baserat på fälten **Tillåt bokföring fr.o.m.** och **Tillåt bokföring t.o.m.**.

#### <a name="to-limit-posting-based-on-vat-return-period"></a>Så här begränsar du bokföring baserat på momsreturperiod

1. Välj ![glödlampan som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Redovisningsinställningar** och välj sedan relaterad länk.  
2. Snabbfliken **Allmänt** i fältet **Kontrollera momsperiod** ange graden av kontrollen för period för momsretur. Alternativen beskrivs i tabellen nedan.

| Typ | Beskrivning |
|--------------------|-----------------------------------------|
| **Spärra bokföring inom stängd och varna för frisläppt period** | Hindra andra från att bokföra ett dokument eller en journal, eller ändra momstransaktioner, som har ett momsdatum inom en stängd **momsreturperiod**. [!INCLUDE [prod_short](includes/prod_short.md)] en varning visas också om **Period för momsretur** är öppen, men statusen för **momsreturen** är **släppt** eller **skickad**. |
| **Spärra bokföring inom stängd period** | Hindra andra från att bokföra ett dokument eller en journal, eller ändra momstransaktioner, som har ett momsdatum inom en stängd **momsreturperiod**. |
| **Varna vid bokföring i stängd period** | Visa en varning, men spärra inte bokföring, om du vill bokföra ett dokument eller en journal som har ett momsdatum inom en stängd **momsreturperiod**. |
| **Inaktiverat** | Ingen åtgärd utförs baserat på en stängd  **momsreturperiod**. |

#### <a name="to-limit-posting-based-on-allow-fromto-period"></a>Så här begränsar du bokföring baserat på tillåt från/till-period

Du kan ställa in begränsningar på företaget eller specifika användarnivåer.

Så här begränsar du alla bokföringar för hela företaget:

1. Välj ![glödlampan som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Redovisningsinställningar** och välj sedan relaterad länk.  
2. På snabbfliken **Allmänt** anger du **Tillåt bokföring från** ange från vilket momsdatum du tillåter bokföring. Bokföra ett dokument eller en journal med ett momsdatum före detta datum är inte tillåtet.  
3. På snabbfliken **Allmänt** anger du **Tillåt bokföring till** ange till vilket momsdatum du tillåter bokföring. Bokföra ett dokument eller en journal med ett momsdatum efter detta datum är inte tillåtet.

Så här begränsar du bokföring för en viss användare:

1. Välj ![glödlampan som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Användarinställning** och väljer sedan relaterad länk.  
2. I fältet **Användar-ID** anger du den användare som ska tillåtas bokföra under en viss period.  
3. I fältet **Tillåt bokföring från** ange från vilket momsdatum du tillåter bokföring. Bokföra ett dokument eller en journal med ett momsdatum före detta datum är inte tillåtet.
4. I fältet **Tillåt bokföring till** ange till vilket momsdatum du tillåter bokföring. Bokföra ett dokument eller en journal med ett momsdatum efter detta datum är inte tillåtet.

## <a name="set-up-vat-registration-numbers-for-your-country-or-region"></a>Så här skapar du momsregistreringsnummer för land / region

För att garantera att användaren anger ett giltigt momsregistreringsnummer kan du ange format för momsregistreringsnummer som används i de länder eller regioner där du bedriver verksamhet. [!INCLUDE[prod_short](includes/prod_short.md)] visar ett felmeddelande när någon gör fel eller använder ett format som är felaktigt för landet / regionen.

Om du vill skapa momsregistreringsnummer, gör då så här:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 2.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **länder/regioner**.
2. Välj land eller region, och välj sedan åtgärden **Format för momsreg.nr.**.
3. I fältet **Format** anger du formatet genom att ange ett eller flera av följande tecken:  

* **#** Kräver ett tal med en enda siffra.  
* **@** Kräver en bokstav. Detta format är inte skiftlägeskänsliga.  
* **?** Alla tecken tillåtna.  

    > [!TIP]
    > Du kan använda andra tecken förutsatt att dessa förekommer i landets/regionens format. Om du behöver inkludera en punkt eller ett bindestreck mellan olika uppsättningar siffror kan du exempelvis definiera formatet som ##.####.### or @@-###-###.  

## <a name="set-up-vat-business-posting-groups"></a>Skapa rörelsebokföringsmallar för moms

Rörelsebokföringsmallar för moms representerar de marknader där du gör affärer med kunder och leverantörer och definierar hur moms beräknas och bokförs på varje marknad. Exempel på momsrörelsebokföringsmallar är **Inhemsk** och **Europeiska unionen (EU)**.  

Använd koder som är lätta att komma ihåg och som beskriver rörelsebokföringsmallen som t. ex. **EU**, **Icke-EU** eller **Inhemsk**. Varje kod måste vara unik, vilket innebär att du kan ställa in så många koder som du vill, men du kan inte använda samma kod mer än en gång i en tabell.

Om du vill konfigurera rörelsebokföringsmall för moms, gör du följande steg:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Moms rörelsebokföringsmall** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs.

Du kan skapa standardrörelsebokföringsmallar för moms genom att koppla rörelsebokföringsmallar för moms till generella rörelsebokföringsmallar. [!INCLUDE[prod_short](includes/prod_short.md)] tilldelar automatiskt rörelsebokföringsmallen för moms när du tilldelar rörelsebokföringsmallen till ett kund-, leverantörs- eller redovisningskonto.

## <a name="set-up-vat-product-posting-groups"></a>Skapa produktbokföringsmallar för moms

Produktbokföringsmallar för moms representerar objekten och resurser och som köper och säljer, och bestämmer hur du beräknar och bokför typen av artikel eller resurs.

Det är praktiskt att använda koder som är lätta att komma ihåg och som beskriver satsen som **ej moms** eller **noll**, **moms10** eller **reducerad** 10 % moms och **moms25** eller **standard** för 25 %.

Om du vill konfigurera rörelsebokföringsmall för moms, gör du följande steg:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Moms produktbokföringsmallar** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Kombinera momsbokföringsmallar i momsbokföringsinställningar

[!INCLUDE[prod_short](includes/prod_short.md)] beräknar momsbeloppen på försäljning och inköp utifrån momsbokföringsinställningar som är kombinationer av rörelsebokföringsmallar för moms och produktbokföringsmallar för moms. För varje kombination kan du fylla i momsprocent, momsberäkningstyp och redovisningskonton för bokföring av moms som relaterar till försäljning, inköp och omvänd moms. Du kan också ange om momsbelopp ska omberäknas när en kassarabatt används eller tas emot.  

Du kan registrera så många kombinationer som du vill. Om du vill gruppera kombinationer av momsbokföringsinställningar med liknande attribut kan du ange ett **Moms-ID** för varje grupp och tilldela ID:t till gruppmedlemmarna.

Om du vill kombinera momsbokföringsinställningar gör du följande:

1. Välj ![glödlampan som öppnar funktionen Berätta 5.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokföringsinställningar för moms** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Tilldela momsbokföringsmallar som standard till flera enheter

Om du vill använda samma momsbokföringsmallar för flera poster kan du skapa [!INCLUDE[prod_short](includes/prod_short.md)] för att göra detta som standard. Detta kan göras på ett par sätt:

* Du kan tilldela rörelsebokföringsmallar för moms till generella rörelsebokföringsmallar eller kund- och leverantörsmallar
* Du kan tilldela produktbokföringsmallar för moms från generella produktbokföringsmallar  

Rörelsebokföringsmallen eller produktbokföringsmallen för moms tilldelas när du väljer en rörelse- eller produktbokföringsmall för en kund, leverantör, artikel eller resurs.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Tilldela momsbokföringsmallar till konton, kunder, leverantörer, artiklar och resurser

I följande avsnitt beskrivs hur du tilldelar momsbokföringsmallar till enskilda enheter.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Så här tilldelar du momsbokföringsmallar till individuella redovisningskonton

1. Välj ![glödlampan som öppnar funktionen Berätta 6.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.  
2. Öppna kortet **redovisningskontokortet** för det kontot.  
3. På snabbfliken **bokföring** i fältet **Typ av bokföring** väljer du antingen **försäljning** eller **inköp**.  
4. Välj momsbokföringsmallar för försäljnings- eller inköpskontot.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>För att tilldela rörelsebokföringsmallar för moms till kunder och leverantörer

1. Välj ![glödlampan som öppnar funktionen Berätta 7.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** eller **Leverantör** och väljer sedan relaterad länk.  
2. På kortet **Kund** eller **Leverantör** expanderar du snabbfliken **Fakturering**.  
3. Välj rörelsebokföringsmallar för moms.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>För att tilldela produktbokföringsmallar till individuella artiklar och resurser

1. Välj ![glödlampan som öppnar funktionen Berätta 8.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikel** eller **Resurs** och väljer sedan relaterad länk.  
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

1. Välj ![glödlampan som öppnar funktionen Berätta 9.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Momsklausuler** och väljer sedan relaterad länk.  
2. På sidan **momsklusuler** skapar du en ny rad.  
3. I fältet **Kod** anger du en identifierare för klausulen. Du använder den här koden för att tilldela klausulen till momsbokföringsmallar.  
4. I fältet **Beskrivning** anger du den text för momsundantag som ska visas i dokument som kan inkludera moms. I fältet **Beskrivning 2** anger du ytterligare text om det behövs. Texten kommer visas på nya dokumentrader.
5. Välj åtgärden **Beskrivning efter dokumenttyp**.
6. På sidan **Momsklausuler per dokumenttyp** fyller du i fälten för att ange vilken momsbefrielsetext som ska visas för vilken dokumenttyp.  
7. Tillval: Om du vill tilldela momsklausulen till en momsbokföringsinställning direkt väljer du **Inställningar**, och väljer sedan klausulen. Om du vill vänta kan du tilldela klausulen vid ett senare tillfälle på sidan **Bokföringsinställningar för moms**.  
8. Valfritt: Att ange hur man översätter momsklausulen, välj åtgärden **översättningar**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Så här tilldelar du en momsklausul till en momsbokföringsinställning

1. Välj ![glödlampan som öppnar funktionen Berätta 10.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokföringsinställningar för moms** och väljer sedan relaterad länk.  
2. I kolumnen **momsklausul** väljer du klausul för varje momsbokföringsinställning som den gäller för.  

### <a name="to-specify-translations-for-vat-clauses"></a>Att ange översättningar för momsklausuler

1. Välj ![glödlampan som öppnar funktionen Berätta 11.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Momsklausuler** och väljer sedan relaterad länk.  
2. Välj åtgärden **Översättningar**.  
3. I fältet **språkkod** välj det språk du översätta till.  
4. I fältet **Beskrivning** och **Beskrivning 2** anger du översättning av beskrivningarna. Denna text visas i det översatta momsrapportdokument.  

### <a name="to-specify-extended-text-for-vat-clauses"></a>För att ange utökad text för momsklausuler

> [!NOTE]  
> Om landet eller regionen kräver längre text för momsklausuler än standardversionen stöder kan du ange den längre texten för momsklausuler som *extratext* så att den skrivs ut på försäljnings- och inköpsrapporterna.  

1. Välj ![glödlampan som öppnar funktionen Berätta 11.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Momsklausuler** och väljer sedan relaterad länk.  
2. Välj åtgärden **Extratexter**.  
3. Välj åtgärden **Ny**.  
4. Fyll i fälten **Språkkod** och **Beskrivning**.  
5. Alternativt kan du välja fältet **Alla språkkoder** eller ange det relevanta språket i **språkkod** om du använder språkkoder.  
6. Fyll i fältet **Startdatum** och fältet **Slutdatum** om du vill begränsa den period under vilken extratexten ska användas.  
7. På raderna **Text**, skriv den utökade texten för dina momsklausuler.  
8. Markera relevanta fält för dokumenttyperna där du vill att extratexten ska skrivas ut.  
9. Stäng sidan.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Skapa en momsbokföringsinställning för hantering av importmoms

Du använder funktionen för *importmoms* när du bokför ett dokument där hela beloppet är moms. Du använder detta om du får en faktura med moms för importerade varor från skattemyndigheterna.  

Så här anger du koder för importmoms:  

1. Välj ![glödlampan som öppnar funktionen Berätta 12.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Moms produktbokföringsmallar** och väljer sedan relaterad länk.  
2. På sidan Bokföringsmallar för momsprodukter anger du en ny produktbokföringsmall för importmoms.  
3. Välj ![glödlampan som öppnar funktionen Berätta 13.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokföringsinställningar för moms** och väljer sedan relaterad länk.  
4. På sidan Bokföringsmallar för momsprodukter skapar du en ny rad eller använder valfri befintlig rörelsebokföringsmall för moms i kombination med den nya produktbokföringsmallen för moms för importmoms.  
5. I fältet **Momsberäkningstyp**väljer du **enbart moms**.  
6. Ange det redovisningskonto som ska användas för att bokföra importmoms i fältet **Ingående moms**. Alla andra konton är valfria.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Använda omvänd moms för handel mellan länder/regioner inom EU

En del företag måste använda omvänd moms när de handlar med andra företag. Regeln gäller för inköp från länder/regioner inom EU och försäljning till länder/regioner inom EU.  

> [!NOTE]  
> Denna regel gäller vid handel med företag som är registrerade som momspliktiga i ett annat land eller en annan region inom EU. Om du handlar direkt med konsumenter i andra länder/regioner inom EU bör du kontakta skattemyndigheterna för att få information om gällande momsregler.  

> [!TIP]  
> Du kan verifiera att ett företag som är registrerat som momspliktigt i ett annat EU-land/region genom att använda tjänsten validering av EU-momsregistreringsnummer. Tjänsten är tillgänglig utan kostnad i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [kontrollera momsregistreringsnummer](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countries-or-regions"></a>Försäljning till länder eller regioner inom EU

Ingen moms beräknas på försäljning till momspliktiga företag i andra länder/regioner inom EU. Du måste rapportera värdet för försäljningar till länder/regioner inom EU separat i momsrapporten.  

För att korrekt beräkna moms på försäljning till länder/regioner inom EU bör du:  

* Lägg upp en rad för försäljning med samma information för inköp. Om du redan har lagt upp rader på sidan **Bokföringsinställning** för moms för inköp från andra länder/regioner inom EU kan du även använda dessa rader för försäljning.  
* Tilldela rörelsebokföringsmallar för moms i fältet **Moms rörelsebokföringsmall** på snabbfliken **Fakturering** på leverantörskortet för varje EU-leverantör. Du bör också ange kunden momsregistreringsnummer i fältet **Momsregistreringsnr** på Snabbfliken **Utlandshandel**.  

När du bokför en försäljning till en kund i ett annat land eller en annan region inom EU beräknas momsbeloppet och en momstransaktion skapas med informationen om omvänd moms och nettobeloppet (det belopp som används för att beräkna momsbeloppet). Inga transaktioner bokförs på momskontona i redovisningen.

Om du vill använda en kombination av momsrörelsebokföringsmall och momsproduktbokföringsmall för rapportering som tjänster i de periodiska momsrapporterna, markera då fältet **EU-tjänst**.

> [!NOTE]  
> Fältet **EU-tjänst** gäller endast för momsrapporter. Fältet är inte relaterat till funktionerna **Tjänstedeklaration** eller **Intrastat för tjänster**.

## <a name="vat-rounding-for-documents"></a>Momsavrundning för dokument

Belopp i dokument som ännu inte har bokförts avrundas och visas på ett sätt som motsvarar den slutliga avrundningen av belopp som faktiskt bokförs. Moms beräknas för ett färdigt dokument, vilket innebär att moms som beräknas baseras på summan av alla rader med samma moms-id i dokumentet.  

## <a name="set-up-vat-reporting"></a>Konfigurera momsrapportering

Du måste ställa in information om hur skattemyndigheterna i ditt land eller din region kräver att du skickar in momsrapporter. Följande steg visar vilken information som används oftast. Du kan emellertid behöva ytterligare åtgärder för ditt land eller din region. Mer information finns i relevant artikel i avsnittet *Lokala funktioner* i panelen till vänster.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-also"></a>Se även

[Ställa in momsrapportmallar och momsrapportnamn](finance-how-setup-vat-statement.md)  
[Ställa in icke-realiserad moms](finance-setup-unrealized-vat.md)  
[Rapportera moms till skattemyndigheterna](finance-how-report-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Arbeta med ändringsverktyget för momssats](finance-how-use-vat-rate-change-tool.md)  
[Kontrollera momsregistreringsnummer](finance-how-validate-vat-registration-number.md)  
[Lokal funktionalitet i Business Central](about-localization.md)  
[Momsrapportering i tyska versionen](LocalFunctionality/Germany/vat-reporting.md)  
[Belgisk moms](LocalFunctionality/Belgium/belgian-vat.md)  
[Italiensk moms](LocalFunctionality/Italy/italian-vat.md)  
[Ställa in elektroniska moms- och ICP-deklarationer i den nederländska versionen](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)  
[Momsrapporter i den spanska versionen](LocalFunctionality/Spain/vat-reports.md)  
[Ställ in momsbokföring för varor och tjänster i den australiska versionen](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)  
[Moms i den tjeckiska versionen](LocalFunctionality/Czech/finance-vat.md)  
[Momsrapportering i den norska versionen](LocalFunctionality/Norway/norwegian-vat-reporting.md)  
[Rapportera moms på varor och tjänster samt harmoniserad försäljningsmoms i Kanada](LocalFunctionality/Canada/sales-tax-goods-services.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
