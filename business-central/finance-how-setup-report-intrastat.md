---
title: Ställa in Intrastat-rapporter
description: Denna artikel förklarar hur du konfigurerar funktioner för rapportering av Intrastat och att rapportera handel med företag i andra EU-länder/regioner.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/05/2023
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# Ställa in Intrastat-rapporter

Alla företag i Europeiska unionen (EU) måste rapportera sin handel med andra länder/regioner inom EU. I Sverige måste företag rapportera transport av varor till de statistiska myndigheterna varje månad, och rapporten måste levereras till skattemyndigheterna. Intrastat är det system som används för att samla in statistik om varor inom dessa länder/regioner. Använd Intrastat-rapporten för att slutföra periodisk rapportering för Intrastat genom att samla in, registrera och rapportera handel med varor enligt lokal lagstiftning.

Intrastat-rapportering baseras på de grundläggande EU-bestämmelser som gäller för alla länder/regioner. Det finns emellertid skillnader i de enskilda länderna/regionerna. Varje land/region har sina egna regler om vad som ska rapporteras och på vilket sätt.

> [!NOTE]
> Intrastat-uppgifter gäller inte förflyttning av tjänster mellan länder/regioner, utan endast varor. Informationen gäller i stället bara för varor som artiklar och anläggningstillgångar. Om din lokala regering kräver att du registrerar transport av tjänster mellan länder/regioner använder du funktionen **Servicedeklaration**.
>
> Den här funktionen är tillgänglig från och med den 2022 november, som en app som du kan hämta från [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). För att använda den här funktionen måste du först installera den på sidan **Tilläggshantering**.

> [!IMPORTANT]
> I den här artikeln behandlas den nya Intrastat-erfarenheten från [!INCLUDE[prod_short](includes/prod_short.md)] version 21. Kontakta administratören för att få information om vilken version ditt företag använder om du ska aktivera den nya funktionen eller inte.
>
> Läs den föregående versionens artikel för Intrastat-inställning och -användning på [Inställning och rapportering av Intrastat](finance-how-setup-report-intrastat-v20.md).

## Aktivera den nya Intrastat-upplevelsen

I utgivningscykel 2 år 2022 innehåller [!INCLUDE[prod_short](includes/prod_short.md)] en omdesignad Intrastat-upplevelse med utökade funktioner. Om den nya Intrastat-funktionen inte är aktiverad i din miljö kan den aktiveras av en administratör på sidan **Funktionshantering**.

> [!IMPORTANT]
> Du kan inte använda gamla och nya upplevelser parallellt. Innan du aktiverar tillägget i en produktionsmiljö rekommenderar vi att du först testar den i en sandboxmiljö med en kopia av produktionsdata. När du har aktiverat en ny användarupplevelse i produktionsmiljön kan du inte återgå till den gamla Intrastat-funktionen.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Funktionshantering** och väljer sedan relaterad länk.
2. På sidan **Funktionshantering** väljer du raden **Funktionsuppdatering: Ersätt den befintliga Intrastat-funktionaliteten med det nya Intrastat-tillägget**. Lär dig mer om funktionshantering på [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management).
3. I kolumnen **Aktivera för** väljer du **Alla användare**.
4. Läs förklaringen till hur systemet kommer att uppgraderas och välj sedan **Ja** för att godkänna.
5. Välj **Nästa**. Du får en grundläggande konfiguration för Intrastat. Läs mer om Intrastat-konfigurationen i avsnittet [Intrastat-konfiguration](#intrastat-configuration) senare i denna artikel.
6. När du är klar med konfigurationen väljer du **Slutför** för att börja använda den nya Intrastat-upplevelsen.

    > [!NOTE]
    > Beroende på ditt företags plats kommer det att räcka för att aktivera den tidigare beskrivna funktionen. För länder/regioner med särskilda funktioner för Intrastat-rapportering bör du aktivera den land-/regionsspecifika Intrastat-appen utöver kärntillägget.

## Intrastat-konfiguration

Innan du kan använda Intrastat-rapporter måste du ställa in flera konfigurationer.

### Konfiguration av Intrastat-rapporter

Använd sidan **Konfiguration av Intrastat-rapporter** för att aktivera och ange standardbeteende för Intrastat-rapportering. Du kan ange om du behöver rapportera Intrastat från leveranser (utskick), inleveranser (ankomst) eller båda beroende på tröskelvärden som anges i de lokala bestämmelserna. Du kan också ange standardtransaktionstyper för vanliga och returnerade dokument, som används för transaktionsrapportering.

Följ dessa steg för att ställa in Intrastat-rapportering.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") Välj ikonen ange **Konfiguration av Intrastat-rapporter** och välj sedan relaterad länk.
2.  På snabbfliken **Allmänt** väljer du eller anger fältinformation om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Följande tabell beskriver några av nyckelfälten.

   | Fält | Description |
   | --- | --- |
   | **Rapportera inleveranser** | Anger att du måste inkludera ankomst av mottagna varor i Intrastat-rapporter. |
   | **Rapportera utleveranser** | Anger att du måste inkludera utleveranser av skickade varor i Intrastat-rapporter. |
   | **Utleveranser baserade på**  | Anger landskoden baserat på vilken Intrastat-rapportraderna tas.  |
   | **Momsregistreringsnummer baserat på** | Specificerar kund- eller leverantörskoden baserat på Intrastat-rapporten, baserat på kund-/leverantörskoden.  |
   | **Företagets registrerade momsnummer** | Anger hur företagets momsregistreringsnummer exporteras till Intrastat-filen.  |
   | **Leverantörens registrerade momsnummer** | Anger hur leverantörens momsregistreringsnummer exporteras till Intrastat-filen.  |
   | **Kundens registrerade momsnummer** | Anger hur kundens momsregistreringsnummer exporteras till Intrastat-filen.  |
   | **Hämta partnermoms** | Anger typen av Intrastat-rapportrad som partnerns momsregistreringsnummer uppdateras från. Beroende på dina lokala krav kan du välja endast inleveransrad, endast leveransrader eller båda typerna av linjer. |

3.  På snabbfliken **standardtransaktioner** väljer du eller anger fältinformation om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Följande tabell beskriver några av nyckelfälten.

   | Fält | Description |
   | --- | --- |
   | **Standardtransaktionsyp** | Anger standardtransaktionstypen för vanliga försäljningsutleveranser, serviceutleveranser och inköpsinleveranser. |
   | **Standardtransaktionstyp – Returer** | Anger standardtransaktionstypen för försäljningsreturer, servicereturer och inköpsreturer. |
   | **Standardmomsnummer för privatperson** | Anger standard för privatpersons momsnummer om den privata personen måste ha ett dedikerat momsnummer i Intrastat-rapporten. |
   | **Standardmomsnummer för trepartshandel** | Anger standardmomsnumret för trepartshandel om du inte har momsnumret. |
   | **Standardmoms för okänt tillstånd** | Anger standardmomsnumret för ett okänt tillstånd. |
   | **Kod för standardland/-region** | Anger standardkoden för mottagarland. |

4.  På snabbfliken **Rapportering** väljer du eller anger fältinformation om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Följande tabell beskriver några av nyckelfälten.

   | Fält | Description |
   | --- | --- |
   | **Def.kod för datautbyte** | Anger koden för datautbytesdefinitionen som ska generera Intrastat-filen. Detta fält är endast tillgängligt om **Dela filer för inleverans/utleverans** är inställt på **Nej**. |
   | **Dela filer för inleverans/utleverans** | Anger om kvitton och utleveranser ska rapporteras i två separata filer. |
   | **Zip-fil(er)** | Anger om rapportfilerna ska läggas till i zip-filen. |
   | **Def.kod för datautbyte – Inleverans** | Anger koden för datautbytesdefinitionen som ska generera Intrastat-filen för mottagna varor. Detta fält är endast tillgängligt om **Dela filer för inleverans/utleverans** är inställt på **Ja**. |
   | **Def.kod för datautbyte – Utleverans** | Anger koden för datautbytesdefinitionen som ska generera Intrastat-filen för levererade varor. Detta fält är endast tillgängligt om **Dela filer för inleverans/utleverans** är inställt på **Ja**. |

5. På snabbfliken **Numrering**, ange ett värde i **Intrastat-nr**.

### Konfigurera en rapporteringsfil

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Datautbytesdefinition** och välj relaterad länk.
2. Välj **Ny** på snabbfliken **Allmänt** ange information om datautbytesdefinition, datafiltyp, kolumnavgränsare, relaterade kodenheter, XMLport och andra fält efter behov.
3. På snabbfliken **Raddefinitioner**, ange ett värde i fältet **Radtyp** för att beskriva formateringen av rader i datafilen och var du behöver definiera antalet kolumner för denna rad.
4. På snabbfliken **Kolumndefinitioner** fyller du i raden för varje planerad kolumn. Du kan definiera kolumnnamn, datatyper (text, datum eller decimal), längd på raden med fast bredd som innehåller kolumnen om filen är av typen *Fast text* och andra parametrar.
5. På snabbfliken **Raddefinitioner**, välj **Fältmappning**.
6. På **Fältmappning** skapa en ny post. 
7. På snabbfliken **Allmänt** väljer du värde **Tabell-ID** (för **Intrastat-rapportrad** väljer **4812**) och anger följande fältinformation:

   1. I fältet **Nyckelindex** ange nyckelindexet för att sortera källposterna före export.
   2. I fältet **Mappning codeunit**, välj ett värde.

8. På snabbfliken **Fältmappning**, lägg till de kolumner som du tidigare konfigurerat på **Kolumndefinitioner** och lägger sedan till följande:

   1. Ange värde **fält-ID** för varje kolumn.
   2. Ange värdet **omvandlingsregeln** för varje kolumn som du behöver den för. Värdet anger för att omvandla importerad text till ett värde som stöds innan det kan mappas till det angivna fältet i [!INCLUDE[prod_short](includes/prod_short.md)]. När du väljer ett värde i det här fältet anges det exakta värdet i fältet **Omvandlingsregel** i **Mappningsbuff. för datautbytesfält** tabell. (Omvänt, när ett exakt värde anges i fältet **Omvandlingsregel** i **Mappningsbuff. för datautbytesfält** tabell väljs ett värde i det här fältet.)

9. Om du vill gruppera transaktioner baserat på vissa kolumner väljer du de fält som du vill använda för gruppering på snabbfliken **Fältgruppering**.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] levereras med den förinställda datautbytesdefinitionen för Intrastat för alla lokaliserade länder/regioner. För att lära dig mer om hur du skapar en ny datautbytesdefinition i [Ställa in datautbytesdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

### Ange obligatoriska fält med checklistan för Intrastat-rapporter

I vissa länder/regioner kräver myndigheterna att Intrastatrapporter omfattar, exempelvis leveransmetod för inköp eller andra värden när försäljningen är över ett visst gränsvärde.

Så här anger du obligatoriska fält eller värden på sidan **Intrastat-rapport**, följ dessa steg:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") Välj ikonen ange **Konfiguration av Intrastat-rapporter** och välj sedan relaterad länk.
2. Välj **Checklista för Intrastat-rapport**.
3. Lägg till de rader som behövs för att kontrollera dem så här:
   1. Ställ in fältet **Fältnr** på ett fält som måste kontrolleras så att det inte är tomt.
   2. Ange ett värde i fältet **Filteruttryck** om så krävs, baserat på följande regler:

        1. När du öppnar **Filtersida** väljer du det filter du behöver för kontroll.
        2. Välj ett värde som är relaterat till det valda filtret.
        3. Om du måste fylla fler filter för det valda fältet upprepar du de föregående två stegen för att lägga till ett filter.
        4. När du har slutat ange filtren för det valda fältet väljer du **OK**.

   3. Markera kryssrutan **Återfört filteruttryck** för att ange att kontrollen av fälten endast utförs på de rader som inte matchar filteruttrycket. Om raden inte filtreras ignoreras det här fältet.

> [!NOTE]
> När du öppnar **Filtersida** från raden **Filteruttryck** kan du använda alla standardfilteruttryck som relaterar till det fält som du vill filtrera.
>
> Var försiktig när du ställer in valideringsregler, eftersom de kan skilja sig mellan olika länder/regioner.

## Använd anpassade codeunits i Intrastat-rapportering

Om du vill ändra hur Intrastat fungerar och standardkonfigurationen inte räcker kan du anpassa systemet genom att utöka standardfunktionerna. Om du behöver ändra Intrastat-beteendet ytterligare kan du skapa egna codeunits. När du skapar codeunits måste du göra ytterligare ändringar för att kunna använda dem. Så här konfigurerar du systemet för att använda egna objekt.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfiguration av momsrapporter** och väljer sedan relaterad länk.
2. Lägg till en ny rad på sidan **Konfiguration av momsrapporter**.
3. I fältet **Typ av momsrapport** väljer du **Intrastat-rapport**.
4. I fältet **Momsrapportversion** anger du versionen på rapporten.
5. Lägg till dina kodmoduler för följande alternativ:
   1. I fältet **Föreslå rader Codeunit-ID** anger du ny codeunit för förslag av rader i Intrastat-rapportrader.
   2. I fältet **Innehåll Codeunit-ID** anger du ny codeunit för export av data som en fil med hjälp av datautbytesdefinition.
   3. I fältet **Validera Codeunit-ID** anger du nya codeunits för att validera resultat i Intrastat-rapportrader.

> [!IMPORTANT]
> Raden måste vara tom om du använder standard-codeunits. Du bör endast skapa en rad och konfigurera den om du har utvecklat egna codeunits.

## Andra Intrastat-konfigurationer

Kundkort och leverantörskort innehåller fältet **Intrastat-partnertyp** som har samma alternativvärden som fältet **Partnertyp**: 

- "" (tom)
- *Företag*
- *Person*
    
Fältet **Intrastat partnertyp** har ersatt **Partnertyp** i Intrastat-rapportering. Fältet **Partnertyp** används i SEPA (Single Euro Payments Area) för att definiera SEPA för direktdebitering (Core eller B2B). Fältet **Typ av Intrastat-partner** används endast för Intrastat-rapportering. Därför kan du ange olika värden för de två fälten om det behövs.

Om fältet **Typ av Intrastat-partner** lämnas tomt används värdet från fältet **Partnertyp** för Intrastat-rapportering.

Förutom **Konfiguration av Intrastat-rapport**, **Datautbytesdefinitioner** och **Checklista för Intrastat-rapporter** måste följande inställningar också konfigureras:

| Sida | Description |
| ---- | ----------- |
| **Länder/regioner** | På sidan **Länder/regioner**, lägg till information om **EU lands-/regionskod** och **Intrastat-kod** för att ange en kod för landet/regionen som du handlar med. Den här informationen används i Intrastat-rapportering. |
| **EU tull statistiknr** | I många länder/regioner fastställer tullen och skattemyndigheterna åttasiffriga koder för olika typer av artiklar. För att ange artikelkoden på sidan **statistiknummer** för att artikeltransaktioner ska innehålla den information som krävs när den importeras till Intrastatjournalraden. Ta reda på koderna för de artiklar som ditt företag handlar med och skriv in dem på sidan **statistiknummer**. |
| **Transportsätt** | Det finns sju ensiffriga koder för Intrastat-transportmetoder **1** för sjötransport, **2**för järnvägstransport, **3** för vägtransport, **4** flygtransport, **5** för brev, **7** för fasta installationer och **9** för egen framdrivning (t.ex. transport av en bil genom att köra den). [!INCLUDE[prod_short](includes/prod_short.md)] saknar dessa specifika koder. Vi rekommenderar dock att beskrivningarna ger liknande betydelse. |
| **Transaktionstyper** | Länder och regioner har olika koder för olika typer av Intrastat-transaktioner, till exempel ordinära inköp och försäljning, byte av returnerade varor och byte av inte returnerade varor. Ställ in alla koder som gäller för ditt land/din region. Dessa koder används sedan på snabbfliken **Utlandshandel** på försäljnings- och inköpsdokument, samt när du bearbetar returer. |
| **Transaktionsspecifikationer** | Skapa koder som komplement till beskrivning av transaktionstyp. |
  
> [!NOTE]
> Från och med januari 2022 kräver Intrastat olika transaktionskoder för utskick till privatpersoner eller icke momsregistrerade företag och momsregistrerade företag. För att uppfylla detta krav rekommenderar vi att du granskar eller lägger till nya transaktionskoder på sidan **Transaktionstyper** enligt kraven i ditt land. Du bör också granska och uppdatera fältet **Intrastat partnertyp** till *Person* för en privatperson eller icke momsregistrerat företag på relevant **Kund**-sida. Om du är osäker på vilken Intrastat-partnertyp eller transaktionstyp du ska använda rekommenderar vi att du frågar en expert i ditt land eller din region.

|   Fält   |   Description   |
| --------- | --------------- |
| **Nettovikt** | Vikt är en av de grundläggande konfigurationerna som är relaterad till Intrastat-rapportering eftersom total vikt är obligatorisk för rapportering. För att vara redo för detta behov anger du ett värde i fältet **Nettovikt** på artikel- eller anläggningstillgångskortet. |
| **Kod för tillverkningsland** | Använd ISO alpha-koderna på artikel- eller anläggningstillgångskortet med två bokstäver för det land/den regionen där varan erhölls eller producerades. Om varan har producerats i mer än ett land/region, är ursprungslandet det sista land/region där den bearbetades. |
| **Momsidentifieringsnummer för partneroperatör i den importerande medlemsstaten** | Detta är momsidentifieringsnumret för partneroperatören i den importerande medlemsstaten. Moms-ID används också vid utbyte av data inom EU-export mellan medlemsstater och gör det möjligt för medlemsstaterna att tilldela mottagna data till det importerande företaget i det egna landet/regionen. Rapporteringsenheter måste ange moms-ID för det företag som deklarerat förvärv av varor inom unionen i den importerande medlemsstaten. |

Du kan även ställa in:

* **Artikelkoder**: Tull- och skattemyndigheterna har fastställt numeriska koder som klassificera artiklar och tjänster. Du kan ange koder för artiklar.
* **Områden**: Kompletterande uppgifter om länder och regioner.
* **In-/utförselplatser**: Ange platser där du kan skicka eller ta emot artiklar till eller från andra länder/regioner. En flygplats är ett exempel på en in-/utförselplats. Du kan ange in-/utförselplatser på försäljnings- och inköpsdokument på snabbfliken **Utlandshandel**. Informationen kopieras från artikeltransaktionerna när du skapar Intrastatjournalen.
* **Kompletterande måttenhet**: Varuantalet för Intrastat-rapportering kan vara nettovikten (i kg) eller en kompletterande enhet. Om det krävs kompletterande enheter måste de konfigureras för artiklar och anläggningstillgångar.

#### Konfigurera transportsätt

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Transportmetoder** och väljer sedan relaterad länk.
2. Fyll i fältinformation om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Skapa koder av transaktionstyp

1. välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Transaktionstyper** och väljer sedan relaterad länk.
2. Fyll i fältinformation om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Andra relaterade konfigurationer

Innan du använder funktionen Intrastat-rapportering måste du definiera vissa fält på kortet för artikel, anläggningstillgång, kund och leverantör.

#### Artikelkorten

Följ stegen nedan för att ställa in all nödvändig information om Intrastat på artikelkort.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk.
2. Markera det objekt som du vill konfigurera.
3. På snabbfliken **Kostnader och bokföring** i **EU tull statistiknr**, **Kompletterande måttenhet** och **Kod för tillverkningsland/-region** anger du ett värde.

    > [!NOTE]
    > För att använda en måttenhet för att komplettera basmåttenheten, konfigurera den kompletterande måttenheten på **Måttenheter för artikel**.

4. Expandera snabbfliken **Lager** i fältet **Nettovikt** och ange ett värde i decimalformat.

> [!NOTE]
> När du lägger till tariffnumret till en måttenhet som är definierad för artikeln, [!INCLUDE [prod_short](includes/prod_short.md)] fyller automatiskt i fältet **Kompletterande måttenhet**, baserat på konfigurationen av tullnummer. Du kan ändra värdet i fältet **Kompletterande måttenhet** efter behov.

#### Ställ in anläggningstillgångar för Intrastat

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Välj anläggningstillgången som du vill konfigurera.
3. På fliken **Intrastat** och fyll i fälten **EU tull statistiknr**, **Nettovikt** och **Kompletterande måttenhet** anger du ett värdet.

> [!NOTE]
> Du kan använda andra måttenheter som kompletterande måttenhet. Oavsett vilken **måttenhetskod** du väljer kommer dess **kvantitet** i Intrastat-rapporter alltid att vara 1.

#### Ställ in leverantörer för Intrastat

Innan du kan ta med en leverantör i Intrastat-rapportering, anger du deras information på sidan **Leverantörskort**. Ange till exempel ett värde för **Lands-/regionkod** och ett värde **Momsregistreringsnr.**.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.
2. Markera den leverantör som du vill konfigurera.
3. På snabbfliken **Intrastat** i fälten **Standardtransaktionsyp**, **Standardtransaktionstyp – Returer** och **Standardtransportsätt**, ange ett standardvärde för varje fält.
4. Expandera snabbfliken **Betalningar** och välj alternativet i fältet **Intrastat-partnertyp** för att ange om leverantören är en person eller ett företag i Intrastat-rapportering.

#### Ställ in kunder för Intrastat

Innan du kan ta med en kund i Intrastat-rapportering, anger du deras information på sidan **Kundkort**. Du måste till exempel ange ett värde för **Lands-/regionkod** och ett värde **Momsregistreringsnr.**.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Markera den kund som du vill konfigurera.
3. På snabbfliken **Intrastat** i fälten **Standardtransaktionsyp**, **Standardtransaktionstyp – Returer** och **Standardtransportsätt**, ange ett standardvärde för varje fält.
4. Expandera snabbfliken **Betalningar** och välj alternativet i fältet **Intrastat-partnertyp** för att ange om leverantören är en person eller ett företag i Intrastat-rapportering.

#### Exkludera artiklar och anläggningstillgångar från Intrastat-rapportering

Om det finns en orsak till att en viss artikel eller anläggningstillgång ska uteslutas från Intrastat-rapportering måste du ändra ett alternativ på deras kort.

##### Undanta en artikel från Intrastat-rapportering

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk.
2. Välj det objekt som du vill konfigurera och sedan på snabbfliken **Kostnad och bokföring** markera kryssrutan **Uteslut från Intrastat-rapport**.

##### Exkludera en anläggningstillgång från Intrastat-rapportering

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Välj anläggningstillgången som du vill konfigurera.
3. Expandera snabbfliken **Intrastat** och markera sedan kryssrutan **Uteslut från Intrastat-rapport**.

#### Ställ in statistiknummer

1. Välj ![glödlampan som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **statistiknummer** och väljer sedan relaterad länk.  
2. På sidan **statistiknummer** anger du information i fälten enligt instruktionerna i följande tabell.

    | Fält | Description |  
    |-------|-------------|
    | **Nr** | Anger statistiknummer. |
    | **Beskrivning** | Anger en beskrivning av relaterat statistiknummer. |
    | **Kompletterande enhet krävs** | Anger om tull- och skattemyndigheterna kräver information om antal och enhet för artikeln. |
    | **Konverteringsfaktor** | Anger konverteringsfaktorn för tullstatistiknumret. |
    | **Måttenhet** | Anger måttenheten för tullstatistiknummer. |

> [!NOTE]
> Om du lägger till en extra måttenhet frågar [!INCLUDE [prod_short](includes/prod_short.md)] om du vill uppdatera relaterade artiklar. Om du väljer att uppdatera relaterade artiklar uppdateras värdet **Måttenhet** på sidan **Måttenheter för artikel** för alla artiklar som har samma statistiknummer.
> 
> När du lägger till ett tariffnummer som har ett definierat värde **Måttenhet** till artikeln, lägger [!INCLUDE [prod_short](includes/prod_short.md)] automatiskt till en ny måttenhet till värdet **måttenheter för artikel** för artikeln. Värdet **Antal per måttenhet** är baserat på fältet **Avrundning för antal**.

## Ange land-/regionsspecifika Intrastat-inställningar

Kraven på Intrastat är likartade i alla medlemsstater i EU, även om det finns viktiga undantag. I teorin bör bestämmelserna tillämpas på samma sätt i alla medlemsstater. Det finns emellertid skillnader i genomförandet, eftersom vissa medlemsstater ger riktlinjer om hur du tillämpar principerna i särskilda situationer (t.ex. handelsprover, varureturer etc.). Dessa riktlinjer kan ge olika resultat för olika situationer. Därför kan informationen som länderna/regionerna måste skriva in skilja sig åt, vilket kan vara det filformat som de måste använda för rapportering.

### Österrike

För Intrastat-rapportering i Österrike krävs två olika filer för inleveranser och utleveranser. Så här kontrollerar du att installationen är korrekt.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") Välj ikonen ange **Konfiguration av Intrastat-rapporter** och välj sedan relaterad länk.  
2. På snabbfliken **Rapportering** kontrollera om **Dela filer för inleverans/utleverans** har valts. Det finns två separata värden för **Def.kod för datautbyte** som har konfigurerats. 
3. Kontrollera att fältet **zip-filer** väljs för att se till att rapportmallar läggs till i zip-filen.

Att arbeta med Intrastat-rapporter är samma sak som den globala funktionen.

<!-- ### Belgium-->

### Tjeckien

Den nya Intrastat-rapportens upplevelse för Tjeckiska republiken kommer att finnas tillgänglig från Utgivningscykel 1 2023. Under tiden kan du fortsätta att använda funktionen **Intrastat-journal**.

### Finland

I Finland finns ytterligare steg för att ställa in Intrastat. För Intrastat-rapportering i Finland krävs två olika filer för inleveranser och utleveranser. Det finns även två separata värden för **Def.kod för datautbyte** som har konfigurerats.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") Välj ikonen ange **Konfiguration av Intrastat-rapporter** och välj sedan relaterad länk.  
2. På sidan **Konfiguration av Intrastat-rapporter**, på snabbfliken **Filinställningar** anger du fältinformation enligt beskrivningen i följande tabell.

    |                 Fält              |            Description                |  
    |------------------------------------|---------------------------------------|
    | **Anpassad kod** | Anger en anpassad kod för information om inställningarna för Intrastat-filen. |
    | **Serienummer för företag.** | Anger ett serienummer för företag för information om inställningarna för Intrastat-filen. |

3. På snabbfliken **Rapportering** kontrollera om **Dela filer för inleverans/utleverans** har valts.

Att arbeta med Intrastat-rapporter är samma sak som den globala funktionen.

<!-- ### Germany-->

### Italien

En ny Intrastat-rapportupplevelse för Italien kommer att finnas tillgänglig från och med 2023 februari. Under tiden kan du fortsätta att använda funktionen **Intrastat-journal**.

<!-- ### France-->

### Sverige

För Intrastat-rapportering i Sverige krävs två olika filer för inleveranser och utleveranser. Så här kontrollerar du att installationen är korrekt.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") Välj ikonen ange **Konfiguration av Intrastat-rapporter** och välj sedan relaterad länk.  
2. På snabbfliken **Rapportering** kontrollera om **Dela filer för inleverans/utleverans** har valts. Det finns två separata värden för **Def.kod för datautbyte** som har konfigurerats.

Att arbeta med Intrastat-rapporter är samma sak som den globala funktionen.

<!-- ### United Kingdom-->

## Se relaterad utbildning på [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## Se även

[Intrastat-rapportering Business Central](finance-how-report-intrastat.md)  
[Ekonomihantering](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
