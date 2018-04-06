---
title: "Om att ställa in moms | Microsoft Docs"
description: "Se till att du korrekt beräknar, bokför och rapporterar om moms för försäljning och inköp."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/20/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 08f1e6c446e60d7b0ff6876f568f31278ed23287
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---

# <a name="setting-up-calculations-and-posting-methods-for-value-added-tax"></a>Förbereda beräknings- och bokföringsmetoder för moms
Konsumenter och företag betalar moms när de köper varor eller tjänster. Momsbeloppet att betala kan variera beroende på flera faktorer. I [!INCLUDE[d365fin](includes/d365fin_md.md)] ställer du in moms för att ange de satser som ska användas för beräkning av momsbelopp baserat på följande:

* Vem du säljer till  
* Vem du köper från  
* Vad du säljer  
* Vad du köper  

Du kan ställa in momsberäkningar manuellt, men det kan vara svårt och tidsödande. Om du vill göra det enklare, finns det en assisterade konfigurationsguid med namnet **momsinställning** som hjälper dig med stegen. Vi rekommenderar att du använder den assisterade konfigurationsguiden för att ställa in momsen.

> [!NOTE]  
>   Du kan endast använda guiden om du har skapat ett Mitt företag och inte har bokfört transaktioner som inkluderar moms. Annars skulle vara mycket emkelt att använda olika momssatser av misstag, och göra felaktiga momsrapporter.  

Om du vill ställa in momsberäkningar själv eller bara vill ha information om varje steg innehåller i det här avsnittet beskrivningar av varje steg.

## <a name="to-use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Använd den assisterade konfigurationsguiden för att ställa in momsen (rekommenderat).
Vi rekommenderar att du använder den assisterade konfigurationsguiden för att ställa in momsen i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Så här startar du den assisterade konfigurationsguiden:
1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten") och ange **Assisterad konfiguration**.  
2. Välj **Ställa in moms**.

## <a name="to-set-up-vat-registration-numbers-for-your-country-or-region"></a>Så här skapar du momsregistreringsnummer för land / region
För att garantera att användaren anger ett giltigt momsregistreringsnummer kan du ange format för momsregistreringsnummer som används i de länder eller regioner där du bedriver verksamhet. [!INCLUDE[d365fin](includes/d365fin_md.md)] visar ett felmeddelande när någon gör fel eller använder ett format som är felaktigt för landet / regionen.

Om du vill skapa momsregistreringsnummer, gör då så här:
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport") och ange **Länder/regioner**.
2. Välj land eller region, och välj sedan åtgärden **Format för momsreg.nr.**.
3. I fältet **Format** anger du formatet genom att ange ett eller flera av följande tecken:  

    |----|----| | # | Kräver ett tal med en enda siffra. | | @ | Kräver en bokstav. Dessa är inte skiftlägeskänsliga. | | ? | Alla tecken tillåtna. |

    > [!Tip]
    > Du kan använda andra tecken förutsatt att dessa förekommer i landets/regionens format. Om du till exempel behöver inkludera en punkt eller ett bindestreck mellan olika uppsättningar siffror kan du exempelvis definiera formatet som ##. ####. ### eller @@-###-###.  

## <a name="to-set-up-vat-business-posting-groups"></a>Så här skapar du rörelsebokföringsmallar för moms
Rörelsebokföringsmallar för moms representerar de marknader där du gör affärer med kunder och leverantörer och definierar hur moms beräknas och bokförs på varje marknad. Exempel på momsrörelsebokföringsmallar är **Inhemsk** och **Europeiska unionen (EU)**.  

Använd koder som är lätta att komma ihåg och som beskriver rörelsebokföringsmallen som t.ex. **EU**, **Icke-EU** eller **Inhemsk**. Koden måste vara unik. Du kan ställa in så många koder som du vill, men du kan inte använda samma kod mer än en gång i en tabell.

Om du vill konfigurera rörelsebokföringsmall för moms, gör du följande steg:

1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **rörelsebokföringsmall för moms**, och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs.

Du kan skapa standardrörelsebokföringsmallar för moms genom att koppla rörelsebokföringsmallar för moms till generella rörelsebokföringsmallar. [!INCLUDE[d365fin](includes/d365fin_md.md)] tilldelar automatiskt rörelsebokföringsmallen för moms när du tilldelar rörelsebokföringsmallen till ett kund-, leverantörs- eller redovisningskonto.

## <a name="to-set-up-vat-product-posting-groups"></a>Så här skapar du produktbokföringsmallar för moms
Produktbokföringsmallar för moms representerar objekten och resurser och som köper och säljer, och bestämmer hur du beräknar och bokför typen av artikel som köps in eller säljs.  
Det är praktiskt att använda koder som är lätta att komma ihåg och som beskriver satsen som **ej moms** eller **noll**, **moms10** eller **reducerad** 10 % moms och **moms25** eller **standard** för 25 %.

Om du vill konfigurera rörelsebokföringsmall för moms, gör du följande steg:

1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **rörelsebokföringsmall för moms**, och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs.

## <a name="to-combine-vat-posting-groups-in-vat-posting-setups"></a>Kombinera momsbokföringsmallar i momsbokföringsinställningar
[!INCLUDE[d365fin](includes/d365fin_md.md)] beräknar momsbeloppen på försäljning och inköp utifrån momsbokföringsinställningar som är kombinationer av rörelsebokföringsmallar för moms och produktbokföringsmallar för moms. För varje kombination kan du fylla i momsprocent,  momsberäkningstyp och redovisningskonton för bokföring av moms som relaterar till försäljning, inköp och omvänd moms. Du kan också ange om momsbelopp ska omberäknas när en kassarabatt används eller tas emot.  

Du kan registrera så många kombinationer som du vill. Om du vill gruppera kombinationer av momsbokföringsinställningar med liknande attribut kan du ange ett **Moms-ID** för varje grupp och tilldela ID:t till gruppmedlemmarna.

Om du vill kombinera momsbokföringsinställningar gör du följande:

1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **rörelsebokföringsmall för moms**, och välj sedan relaterad länk.
2. Fyll i fälten om det behövs.

## <a name="to-assign-vat-posting-groups-by-default-to-multiple-entities"></a>Tilldela momsbokföringsmallar som standard till flera enheter
Om du vill använda samma momsbokföringsmallar för flera poster kan du skapa [!INCLUDE[d365fin](includes/d365fin_md.md)] för att göra detta som standard. Detta kan göras på ett par sätt:

* Du kan tilldela rörelsebokföringsmallar för moms till generella rörelsebokföringsmallar eller kund- och leverantörsmallar
* Du kan tilldela produktbokföringsmallar för moms från generella produktbokföringsmallar  

Rörelsebokföringsmallen eller produktbokföringsmallen för moms tilldelas när du väljer en rörelse- eller produktbokföringsmall för en kund, leverantör, artikel eller resurs.

## <a name="to-assign-vat-posting-groups-to-individual-accounts-customers-vendors-items-and-resources"></a>Tilldela momsbokföringsmallar till enskilda konton, kunder, leverantörer, artiklar och resurser
I följande avsnitt beskrivs hur du tilldelar momsbokföringsmallar till enskilda enheter.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Så här tilldelar du momsbokföringsmallar till individuella redovisningskonton
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kontoplan** och välj sedan relaterad länk.  
2. Öppna kortet **redovisningskontokortet** för det kontot.  
3. På snabbfliken **bokföring** i fältet **Typ av bokföring** väljer du antingen **försäljning** eller **inköp**.  
5. Välj momsbokföringsmallar för försäljnings- eller inköpskontot.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>För att tilldela rörelsebokföringsmallar för moms till kunder och leverantörer  
1. Välj ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "ikonen Sök efter sida eller rapport"), ange **Kund** eller **Leverantör** och välj sedan relaterad länk.  
2. På kortet **Kund** eller **Leverantör** expanderar du snabbfliken **Fakturering**.  
3. Välj rörelsebokföringsmallar för moms.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>För att tilldela produktbokföringsmallar till individuella artiklar och resurser  
1. Välj den ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten") ikon, ange **Artikeln** eller **Resursen**, och välj sedan relaterad länk.  
2. Gör något av följande:  

* På kortet **Item**  expandera snabbfliken **pris och bokföring** och välj **visa fler** för att visa fältet **Moms produktbokföringsmall**.  
* På kortet **Resurs** expanderar du snabbfliken **Fakturering**.  
3. Välj produktbokföringsmallen med moms.  

## <a name="to-set-up-clauses-to-explain-the-use-of-non-standard-vat-rates"></a>Ställ in klausuler som förklarar hur icke-standardmässiga momssatser används
Du konfigurerar en momsklausul som beskriver information om vilken typ av moms som tillämpas. Informationen kan krävas av Myndighetsregleringar. När du registrerar en momsklausul och associera den med en momsbokföringsinställning, visas momsklausulen på alla utskrivna försäljningsdokument som använder momsbokföringsinställningsmallen.

Om det behövs kan du också ange hur man konverterar momsklausuler till andra språk. När du sedan skapar och skriver ut ett försäljningsdokument som innehåller ett moms-ID, kommer dokumentet att ta med den översatta momsklausulen. Den språkkod som anges på kundkortet bestämmer språket.

Du kan ändra eller ta bort en momsklausul och dina ändringar kommer visas i en generarad rapporten. [!INCLUDE[d365fin](includes/d365fin_md.md)] sparar dock ingen historik över ändringen. I rapporten skrivs momsklausulbeskrivningarna ut, och visas för alla rader i rapporten tillsammans med momsbeloppet och nettobeloppet. Om en momsklausul inte har angetts för alla rader på försäljningsdokumentet, utelämnas hela avsnittet, när rapporten skrivs ut.

### <a name="to-set-up-vat-clauses"></a>Så här konfigurerar du momsklausuler
1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **rörelsebokföringsmall för moms**, och välj sedan relaterad länk.  
2. På sidan **momsklusuler** skapar du en ny rad.  
3. I fältet **Kod** anger du en identifierare för klausulen. Du använder den här koden för att tilldela klausulen till momsbokföringsmallar.  
4. I fältet **beskrivning** anger du den text som ska visas i dokument som kan inkludera moms. I fältet **Beskrivning 2** anger du ytterligare text om det behövs. Texten visas på nya rader.  
5. Tillval: Om du vill tilldela momsklausulen till en momsbokföringsinställning direkt väljer du **inställningar**, och väljer sedan klausulen. Om du vill vänta kan du tilldela klausulen vid ett senare tillfälle på sidan Momsbokföringsinställningar.  
6. Valfritt: Att ange hur man översätter momsklausulen, välj åtgärden **översättningar**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Så här tilldelar du en momsklausul till en momsbokföringsinställning
1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **rörelsebokföringsmall för moms**, och välj sedan relaterad länk.  
2. I kolumnen **momsklausul** väljer du klausul för varje momsbokföringsinställning som den gäller för.  

### <a name="to-specify-translations-for-vat-clauses"></a>Att ange översättningar för momsklausuler
1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **rörelsebokföringsmall för moms**, och välj sedan relaterad länk.  
2. Välj åtgärden **Översättningar**.  
3. I fältet **språkkod** välj det språk du översätta till.  
4. I fältet **Beskrivning** och **Beskrivning 2** anger du översättning av beskrivningarna. Denna text visas i det översatta momsrapportdokument.  

## <a name="to-create-a-vat-posting-setup-to-handle-import-vat"></a>Skapa en momsbokföringsinställning för hantering av importmoms
Du använder funktionen för importmoms när du bokför ett dokument där hela beloppet är moms. Du använder detta om du får en faktura med moms för importerade varor från skattemyndigheterna.  

Så här anger du koder för importmoms:  
1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **rörelsebokföringsmall för moms**, och välj sedan relaterad länk.  
2. På sidan Moms produktbokföringsmallar anger du en ny produktbokföringsmall för importmoms.  
3. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **rörelsebokföringsmall för moms**, och välj sedan relaterad länk.  
4. På sidan Moms bokföringsinställningar skapar du en ny rad eller använder valfri befintlig rörelsebokföringsmall för moms i kombination med den nya produktbokföringsmallen för moms för importmoms.  
5. I fältet **Momsberäkningstyp**väljer du **enbart moms**.  
6. Ange det redovisningskonto som ska användas för att bokföra importmoms i fältet **Ingående moms**. Alla andra konton är valfria.  

## <a name="to-verify-vat-registration-numbers"></a>Kontrollera momsregistreringsnummer
Det är viktigt att momsregistreringsnummer för kunder, leverantörer och kontakter är giltiga. Till exempel ändrar företag sin skatteskuldstatus och i vissa länder kan skattemyndigheterna be dig lämna rapporter som t.ex. EG-försäljningslisterapport som anger de momsregistreringsnummer som du använder när du gör affärer.

Europeiska kommissionen har en tjänst för VIES momsnummervalidering på sin webbplats som är offentlig och kostnadsfri. [!INCLUDE[d365fin](includes/d365fin_md.md)] kan spara dig det steget och låter dig använda VIES-tjänsten för verifiering och spåra momsregistreringsnummer för kunder, leverantörer och kontakter direkt från kund-, leverantörs- och kontaktkort. Tjänsten i [!INCLUDE[d365fin](includes/d365fin_md.md)] heter **Valideringstjänst för EU momsreg.nr.**. Den är tillgänglig på sidan **Anslutningar till tjänst**, och du kan börja använda den direkt. Registrering behövs inte och tjänsten är gratis.

> [!Note]
> Om du vill aktivera valideringstjänsten för EU momsreg.nr. måste du ha administratörsrättigheter.

När du använder vår tjänst registrerar vi en historik över momsregistreringsnummer och kontroller för varje kund, leverantör eller kontakt i **momsregistreringslogga**, så att du enkelt kan spåra dem. Loggen är unik för varje kund. Loggen är användbar för att verifierat att det aktuella momsregistreringsnumret är korrekt. När du verifierar ett momsregistreringsnummer kommer kolumnen **begär ID** i loggen att visa att du har vidtagit åtgärder.

Du kan se momsregistreringsloggen på kund-, leverantör- eller kontaktkorten på snabbfliken **fakturering** genom att välja sökknappen i **Momsregistreringsnr.**  

Tjänsten kan också spara tid när du skapar en kund eller leverantör. Om du känner till kundens momsregistreringsnummer kan du ange det i fältet **Momsregistreringsnr** på korten för kunden eller leverantören, och vi ska fylla i kundens namn åt dig. Vissa länder har dessutom företagsadresser i ett strukturerat format. I dessa länder fyller vi även i addressen.  

> [!NOTE]  
> Det finns ett par saker att komma ihåg om tjänsten VIES momsnummervalidering:

* Den här tjänsten använder http-protokoll, vilket betyder att data som har överförts via tjänsten inte har krypteras.  
* Det kan uppstå avbrott för den här tjänsten som inte Microsoft ansvarar för. Tjänsten är en del av ett omfattande EU-nätverk av nationella register för moms.

## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Använda omvänd moms för handel mellan länder/regioner inom EU
En del företag måste använda omvänd moms när de handlar med andra företag. Regeln gäller för inköp från länder/regioner inom EU och försäljning till länder/regioner inom EU.  

> [!NOTE]  
> Denna regel gäller vid handel med företag som är registrerade som momspliktiga i ett annat land eller en annan region inom EU. Om du handlar direkt med konsumenter i andra länder/regioner inom EU bör du kontakta skattemyndigheterna för att få information om gällande momsregler.  

> [!TIP]  
> Du kan verifiera att ett företag som är registrerat som momspliktigt i ett annat EU-land genom att använda tjänsten validering av EU-momsregistreringsnummer. Tjänsten är tillgänglig utan kostnad i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i delen _Kontrollera momsregistreringsnummer_ i det här avsnittet.

### <a name="sales-to-eu-countries-or-regions"></a>Försäljning till länder eller regioner inom EU
Ingen moms beräknas på försäljning till momspliktiga företag i andra länder/regioner inom EU. Du måste rapportera värdet för försäljningar till länder/regioner inom EU separat i momsrapporten.  

För att korrekt beräkna moms på försäljning till länder/regioner inom EU bör du:  

* Lägg upp en rad för försäljning med samma information för inköp. Om du redan har lagt upp rader på sidan Moms bokföringsinställning för inköp från andra länder/regioner inom EU kan du även använda dessa rader för försäljning.  
* Tilldela rörelsebokföringsmallar för moms i fältet **Moms rörelsebokföringsmall** på snabbfliken **Fakturering** på leverantörskortet för varje EU-leverantör. Du bör också ange kunden momsregistreringsnummer i fältet **Momsregistreringsnr** på Snabbfliken **Utlandshandel**.  

När du bokför en försäljning till en kund i ett annat land eller en annan region inom EU beräknas momsbeloppet och en momstransaktion skapas med informationen om omvänd moms och nettobeloppet (det belopp som används för att beräkna momsbeloppet). Inga poster bokförs på momskontona i redovisningen.

## <a name="understanding-vat-rounding-for-documents"></a>Förstå momsavrundning för dokument
Belopp i dokument som ännu inte har bokförts avrundas och visas på ett sätt som motsvarar den slutliga avrundningen av belopp som faktiskt bokförs. Moms beräknas för ett färdigt dokument, vilket innebär att moms som beräknas baseras på summan av alla rader med samma moms-id i dokumentet.

## <a name="understanding-the-vat-rate-conversion-process"></a>Förstå konverteringen av momssatsen  
Verktyget för momsändring utför momssatskonvertering för huvuddata, journaler och order på olika sätt. De valda huvuddata och journalerna uppdateras med den nya allmänna produktbokföringsmallen eller produktbokföringsmallen för moms. Om en order har levererats helt eller delvis, kommer de levererade artiklarna behålla den aktuella produktbokföringsmallen eller produktbokföringsmallen för moms. En ny orderrad skapas för de olevererade artiklarna och uppdateras för att stämma med den nuvarande och nya momsen eller allmänna produktbokföringsmallen. Dessutom ska artikelomkostnadsfördelningar, reservationer och artikelspårningsinformation uppdateras.  

Det finns dock några saker som inte räknar om verktyget:

* Försäljnings- eller inköpsorder och fakturor där leveranser har bokförts. Dessa dokumentet bokförs med hjälp av den aktuella momssatsen.  
* Dokument som har bokförda förskottsfakturor. Du har till exempel gjort eller tagit emot förskottsbetalningar för fakturor som inte har slutförts innan du använder ändringsverktyget för momssats. I det här fallet blir det en differens mellan momsen som har förfallit och momsen som har betalats i förskottsbetalningar när fakturan har slutförts. Ändringsverktyget för momssats hoppar över dessa dokument och du måste uppdatera dem manuellt.  
* Direktleveranser eller specialorder  
* Försäljnings- eller inköpsorder med lagerintegration om de är delvis levererade eller mottagna.  
* Servicekontrakt  

### <a name="to-prepare-vat-rate-change-conversions"></a>Så här förbereder du konverteringar av momssatser  
Innan du skapar ändringsverktyget för momssats, måste du göra följande förberedelser.

* Om du har transaktioner som används olika satser måste de delas upp i olika grupper, antingen genom att skapa nya redovisningskonton för varje sats eller genom att använda datafilter för att gruppera transaktioner efter sats.  
* Om du skapar nya redovisningskonton, måste du skapa nya generella bokföringsmallar.  
* Om du vill reducera antalet dokumentet som konverteras, bokför så många dokument som möjligt och minska ej bokförda dokument till en minimum.  
* Säkerhetskopiera data.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Så här ställer du in ändringsverktyget för momssats  
1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Inställningar för ändring av momssats**, och välj sedan relaterad länk.  
2. På snabbflikarna **Huvuddata**, **Journaler** och **Dokument**, välj en bokföringsmall i alternativlistan för nödvändiga fält.  

### <a name="to-set-up-product-posting-group-conversion"></a>Så här skapar du konvertering av produktbokföringsmallar  
1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Inställningar för ändring av momssats**, och välj sedan relaterad länk.  
2. På sidan **Inställningar för ändring av momssats** på fliken **Start** i gruppen **Process**, antingen **Moms prod.bokf.mall, konv.** eller **Produktbokföringsmall, konv.**.  
3. I fältet  **Från kod**, ange den aktuella bokföringsmallen.  
4. I fältet **Till kod** anger du den nya bokföringsgruppen.  

### <a name="to-perform-vat-rate-change-conversion"></a>Utföra konvertering för ändring av momssats  
Du använder momssatsändringsverktyget till rätta ändringar i standardsatsen för moms. Du utför moms och generella bokföringsmallkonverteringar för att ändra momssatser och underhålla exakt momsrapportering. Beroende på inställningen görs följande ändringar:  

* Moms- och bokföringsmallar konverteras.  
* Ändringar genomförs i redovisningskonton, kunder, leverantörer, öppna dokument, journalrader, o.s.v.  

> [!IMPORTANT]  
>  Innan du utför konverteringen av momssats, kan du testa konverteringen. Följ instruktionerna nedan för att göra det, men du måste avmarkera **utför konvertering** och **Ändringsverktyget för momssats har slutförts**. Under testkonverteringen avmarkerades fältet **konverterad** i tabellen **Ändringsloggtransaktion för momssats** och fältet **konverteras datum** i tabellen **Ändringsloggtransaktion för momssats** är tom. Välj **Ändringsloggtransaktion för momssats** för att visa resultatet av testkonverteringen. Kontrollera varje transaktion, innan du utför konverteringen. Kontrollera särskilt transaktioner som använder en gammal momssats.     

1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **ändring av momssats**, och sedan länken **Inställningar för ändring av momssats**.  
2. Kontrollera att du har ställt in konverteringen för momsproduktbokföringsmall eller produktbokföringsmall.  
3. Markera kryssrutan **utför konvertering**.  

    > [!IMPORTANT]  
    >  Avmarkera kryssrutan **Ändringsverktyget för momssats har slutförts**. Kryssrutan markeras automatiskt, när konverteringen av momssats slutförs.  

4. Välj åtgärden **Konvertera**.  
5. Välj **Ändringsloggtransaktion för momssats** på fliken **Start** i gruppen **Process** för att visa resultatet av konverteringen.  

> [!IMPORTANT]  
>  När konverteringen är klar markeras fältet **konverterad** i tabellen **Ändringsloggtransaktion för momssats** och **konverteras datum** i den **Ändringsloggtransaktion för momssats** fylls i med konverteringsdatumet.  

## <a name="see-also"></a>Se även  
[Ställa in orealiserad mervärdesskatt](finance-setup-unrealized-vat.md)  
[Så här: rapportera moms till skattemyndigheterna](finance-how-report-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  

