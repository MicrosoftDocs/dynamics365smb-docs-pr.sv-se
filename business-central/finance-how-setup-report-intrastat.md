---
title: Ställa in Intrastat-rapporter
description: Lär dig hur du konfigurerar funktioner för rapportering av Intrastat och att rapportera handel med företag i andra EU-länder.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.search.form: 308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077
ms.date: 09/02/2022
ms.author: altotovi
ms.openlocfilehash: b6adddb338af36f07abe4c6cb67c8113657ccb7c
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605495"
---
# <a name="set-up-intrastat-reporting"></a>Ställa in Intrastat-rapporter

Alla företag i Europeiska unionen (EU) måste rapportera sin handel med andra länder/regioner inom EU. I Sverige måste företag rapportera transport av varor till de statistiska myndigheterna varje månad, och rapporten måste levereras till skattemyndigheterna. Intrastat är det system som används för att samla in statistik över varor inom dessa länder/regioner. Du använder **Intrastat-rapport** för att slutföra periodisk rapportering för Intrastat (vanligen månadsvis), samla in, registrera och rapportera handel med varor enligt lokal lagstiftning.

Intrastat-rapportering grundar sig på de grundläggande EU-bestämmelser som gäller för alla länder. I praktiken finns det emellertid vissa skillnader i de enskilda länderna. Varje land har sina egna regler för exakt vad som ska rapporteras och på vilket sätt.

> [!NOTE]
> Intrastat-uppgifter gäller inte förflyttning av tjänster mellan länder, utan endast varor (artiklar och anläggningstillgångar). Om den lokala regeringen kräver registrering av transport av tjänster mellan länder kan du göra detta med hjälp av funktionen **Servicedeklaration**.
>
> Denna funktion förväntas vara tillgänglig från november 2022 som en app i [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646), så om du vill använda den måste du först installera den på sidan **Tilläggshantering**.

> [!IMPORTANT]
> I den här artikeln behandlas den nya Intrastat-erfarenheten från [!INCLUDE[prod_short](includes/prod_short.md)] version 21. Kontakta administratören för att få information om vilken version ditt företag använder och för att aktivera de nya funktionerna.
>
> Läs den föregående versionens artikel för Intrastat-inställning och -användning på [Inställning och rapportering av Intrastat](finance-how-setup-report-intrastat-v20.md).

## <a name="enable-the-new-intrastat-experience"></a>Aktivera den nya Intrastat-upplevelsen

I utgivningscykel 2 år 2022 innehåller [!INCLUDE[prod_short](includes/prod_short.md)] en omdesignad Intrastat-upplevelse med utökade funktioner. Om den nya Intrastat-funktionen inte är aktiverad i din miljö kan den aktiveras manuellt av en administratör på sidan **Funktionshantering**.

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Funktionshantering** och väljer sedan relaterad länk.
2. På sidan **Funktionshantering** väljer du raden **Funktionsuppdatering: Ersätt den befintliga Intrastat-funktionaliteten med det nya Intrastat-tillägget**. Lär dig mer om funktionshantering på [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management) i administrationsinnehållet.
3. I kolumnen **Aktivera för** väljer du **Alla användare**.
4. Läs förklaringen till hur systemet kommer att uppgraderas och välj **Ja** om du godkänner det.
5. Välj **Nästa** så får du en grundläggande konfiguration för Intrastat. Läs mer om Intrastat-konfigurationen i avsnittet [Intrastat-konfiguration](#intrastat-configuration).
6. När du är klar med konfigurationen väljer du **Slutför** för att börja använda den nya Intrastat-upplevelsen.

> [!IMPORTANT]
> Tänk på att du inte kan använda gamla och nya upplevelser parallellt. Innan du aktiverar tillägget i en produktionsmiljö bör du först aktivera och testa den här funktionen i en sandboxmiljö med en kopia av produktionsdata, innan du gör detta i en produktionsmiljö. När du har aktiverat en ny användarupplevelse i produktionsmiljön kan du inte återgå till den gamla Intrastat-funktionen.

> [!NOTE]
> Det räcker med att aktivera funktionen som beskrivs ovan, beroende på var företaget finns. För länder med särskilda funktioner för Intrastat-rapportering bör du aktivera den landsspecifika Intrastat-appen utöver kärntillägget.

## <a name="intrastat-configuration"></a>Intrastat-konfiguration

Innan du kan använda Intrastat-rapporter måste du ställa in flera konfigurationer.

### <a name="intrastat-reporting-setup"></a>Konfiguration av Intrastat-rapporter

Sidan **Konfiguration av Intrastat-rapporter** används för att aktivera Intrastat-rapportering och ange standarder för det. Du kan ange om du behöver rapportera Intrastat från leveranser (utskick), inleveranser (ankomst) eller båda beroende på tröskelvärden som anges i de lokala bestämmelserna. Du kan också ange standardtransaktionstyper för vanliga och returnerade dokument, som används för transaktionsrapportering.

Skapa Intrastat-rapportering:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Konfiguration av Intrastat-rapporter** och väljer sedan relaterad länk.
2. Öppna snabbfliken **Allmänt** och fyll i nödvändiga fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] I tabellen nedan beskrivs några av nyckelfälten:

   | Fält | Description |
   | --- | --- |
   | **Rapportera inleveranser** | Anger att du måste inkludera ankomst av mottagna varor i Intrastat-rapporter. |
   | **Rapportera utleveranser** | Anger att du måste inkludera utleveranser av skickade varor i Intrastat-rapporter. |
   | **Utleveranser baserade på**  | Anger vilka rader i Intrastat-rapporten som ska hämtas, baserat på landskoden. Du kan välja ett av alternativen: **Försäljningsland**, **Faktureringsland** eller **Leveransland**. |
   | **Momsregistreringsnummer baserat på** | Anger vilket momsnummer som ska hämtas för Intrastat-rapporten, baserat på kund-/leverantörskoden. Du kan välja ett av alternativen: **Kundmoms** eller **Faktureras moms**. |
   | **Företagets registrerade momsnummer** | Anger hur företagets momsregistreringsnummer exporteras till Intrastat-filen. Du kan välja ett av följande alternativ: momsregistreringsnr, lägga till EU-landkoden som prefix och ta bort EU-landkoden från momsregistreringsnr. |
   | **Leverantörens registrerade momsnummer** | Anger hur leverantörens momsregistreringsnummer exporteras till Intrastat-filen. Du kan välja ett av följande alternativ: momsregistreringsnr, lägga till EU-landkoden som prefix och ta bort EU-landkoden från momsregistreringsnr. |
   | **Kundens registrerade momsnummer** | Anger hur kundens momsregistreringsnummer exporteras till Intrastat-filen. Du kan välja ett av följande alternativ: momsregistreringsnr, lägga till EU-landkoden som prefix och ta bort EU-landkoden från momsregistreringsnr. |
   | **Hämta partnermoms** | Anger typen av **Intrastat-rapport** rad som partnerns momsregistreringsnummer uppdateras från. Beroende på de lokala behoven kan du välja endast för inleverans, endast för leverans eller för båda typerna av rader. |
3. Öppna snabbfliken **Standardtransaktioner** och fyll i nödvändiga fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] I tabellen nedan beskrivs några av nyckelfälten:

   | Fält | Description |
   | --- | --- |
   | **Standardtransaktionsyp** | Anger standardtransaktionstypen för vanliga försäljningsutleveranser, serviceutleveranser och inköpsinleveranser. |
   | **Standardtransaktionstyp – Returer** | Anger standardtransaktionstypen för försäljningsreturer, servicereturer och inköpsreturer. |
   | **Standardmomsnummer för privatperson** | Anger standard för privatpersons momsnummer om den privata personen måste ha ett dedikerat momsnummer i Intrastat-rapporten. |
   | **Standardmomsnummer för trepartshandel** | Anger standardmomsnumret för trepartshandel om du inte har momsnumret. |
   | **Standardmoms för okänt tillstånd** | Anger standardmomsnumret för ett okänt tillstånd. |
   | **Kod för standardland/-region** | Anger standardkoden för mottagarland. |
4. Öppna snabbfliken **Rapportering** och fyll i nödvändiga fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] I tabellen nedan beskrivs några av nyckelfälten:

   | Fält | Description |
   | --- | --- |
   | **Def.kod för datautbyte** | Anger koden för datautbytesdefinitionen som ska generera Intrastat-filen. Det fungerar bara om fältet **Dela filer för inleverans/utleverans** är inställt på **Nej**. |
   | **Dela filer för inleverans/utleverans** | Anger om inleveranser och utleveranser ska rapporteras i två separata filer. |
   | **Zip-fil(er)** | Anger om rapportfilerna ska läggas till i .zip-filen. |
   | **Def.kod för datautbyte – Inleverans** | Anger koden för datautbytesdefinitionen som ska generera Intrastat-filen för mottagna varor. Det fungerar bara om fältet **Dela filer för inleverans/utleverans** är inställt på **Ja**. |
   | **Def.kod för datautbyte – Utleverans** | Anger koden för datautbytesdefinitionen som ska generera Intrastat-filen för levererade varor. Det fungerar bara om fältet **Dela filer för inleverans/utleverans** är inställt på **Ja**. |
5. Öppna snabbfliken **Numrering** för att konfigurera **Intrastat-nr**.

### <a name="set-up-a-reporting-file"></a>Konfigurera en rapporteringsfil

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Datautbytesdefinition** och välj relaterad länk.
2. Välj åtgärden **Ny**.
3. På snabbfliken **Allmänt** beskriver du datautbytesdefinitionen, datafiltypen, kolumnavgränsaren, relaterade codeunits, XMLport och andra fält genom att fylla i fälten.
4. På snabbfliken **Raddefinitioner** beskriver du formateringen för raderna i datafilen genom att fylla i fälten baserat på fältet **Radtyp** och där du behöver definiera antalet kolumner för den här raden.
5. På snabbfliken **Kolumndefinitioner** fyller du i raden för varje planerad kolumn. Du kan definiera kolumnnamn, datatyper ( *text*, *datum* eller *decimal*), längd på raden med fast bredd som innehåller kolumnen om filen är av typen Fast text och andra parametrar.
6. Välj åtgärden **Fältmappning** på snabbfliken **Raddefinitioner** för att öppna sidan **Fältmappning**.
7. Skapa den nya transaktionen och på snabbfliken **Allmänt** väljer du rätt **tabell-ID** (för **Intrastat-rapportrad**, välj 4812), och fyll sedan i fler fält.
   1. Ange nyckelindexet som ska användas för att sortera källposterna före export i fältet **Nyckelindex**.
   2. Välj korrekt **mappnings-codeunit**.
8. På snabbfliken **Fältmappning** lägger du till kolumner som du tidigare konfigurerat i snabbfliken **Kolumndefinitioner** och lägger sedan till följande:
   1. Ange **fält-ID** för varje kolumn.
   2. Ange **omvandlingsregeln** för varje kolumn som du behöver den för. Anger regeln för att omvandla importerad text till ett värde som stöds innan det kan mappas till det angivna fältet i [!INCLUDE[prod_short](includes/prod_short.md)]. När du väljer ett värde i det här fältet anges det exakta värdet i fältet **Omvandlingsregel** i **Mappningsbuff. för datautbytesfält** och vice versa.
9. Om du vill gruppera transaktioner baserat på vissa kolumner väljer du de fält som du vill använda för gruppering på snabbfliken **Fältgruppering**.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] levereras med den förinställda datautbytesdefinitionen för Intrastat för alla lokaliserade länder. Läs mer om att skapa en ny datautbytesdefinition i artikeln [Ställa in datautbytesdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

### <a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a>Ange obligatoriska fält med checklistan för Intrastat-rapporter

I vissa länder kräver myndigheterna att Intrastatrapporter omfattar, exempelvis leveransmetod för inköp eller andra värden när försäljningen är över ett visst gränsvärde.

Så här anger du obligatoriska fält och/eller värden på sidan **Intrastat-rapport**:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfiguration av Intrastat-rapporter** och väljer sedan relaterad länk.
2. Välj åtgärden **Checklista för Intrastat-rapport**.
3. Lägg till de rader som behövs för att kontrollera dem enligt följande instruktioner:
   1. Ställ in fältet **Fältnr** på ett fält som måste kontrolleras så att det inte är tomt.
   2. Fyll i fältet **Filteruttryck** om så krävs, baserat på följande regler:
      1. När du öppnar **Filtersida** väljer du det **filter** du behöver för kontroll.
      2. Gå till nästa steg och välj ett värde som är relaterat till det **filter** som du har använt.
      3. Om du har fler filter som måste fyllas i för ett visst fält, kan du lägga till ytterligare ett filter på samma sätt.
      4. När du har angett filtren för det valda fältet klickar du på **OK**.
   3. Välj fältet **Återfört filteruttryck** för att ange att kontrollen av fälten endast utförs på de rader som inte matchar filteruttrycket. Om raden inte filtreras ignoreras det här fältet.

> [!NOTE]
> När du öppnar **Filtersida** från raden **Filteruttryck** kan du använda alla standardfilteruttryck som relaterar till det fält som du vill filtrera.
>
> Var försiktig med att ställa in valideringsregler, eftersom de kan skilja sig från land till land.

## <a name="use-custom-codeunits-in-intrastat-reporting"></a>Använd anpassade codeunits i Intrastat-rapportering

Om du vill ändra hur Intrastat fungerar och standardkonfigurationen inte räcker kan du anpassa systemet genom att utöka standardfunktionerna. Om du behöver ändra Intrastat-beteendet ytterligare kan du skapa egna codeunits. När du skapar codeunits måste du dock göra ytterligare ändringar för att kunna använda dem. Så här konfigurerar du systemet för att använda egna objekt:

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfiguration av momsrapporter** och väljer sedan relaterad länk.
2. Lägg till en ny rad på sidan **Konfiguration av momsrapporter**.
3. I fältet **Typ av momsrapport** väljer du alternativet **Intrastat-rapport**.
4. I fältet **Momsrapportversion** anger du versionen på rapporten.
5. Sedan kan du lägga till dina codeunits för följande alternativ: a. I fältet **Föreslå rader Codeunit-ID** anger du ny codeunit för förslag av rader i Intrastat-rapportrader.
   b. I fältet **Innehåll Codeunit-ID** anger du ny codeunit för export av data som en fil med hjälp av datautbytesdefinition.
   c. I fältet **Validera Codeunit-ID** anger du nya codeunits för att validera resultat i Intrastat-rapportrader.

> [!IMPORTANT]
>
> Raden måste vara tom om du använder standard-codeunits. Du bör endast skapa en rad och konfigurera den om du har utvecklat egna codeunits.

## <a name="other-intrastat-configurations"></a>Andra Intrastat-konfigurationer

> [!IMPORTANT]
> Kundkort och leverantörskort innehåller ett fält, **Typ av Intrastat-partner**, som har samma alternativvärden som fältet **Partnertyp**: "" (tom), *Företag* och *Person*. Fältet **Intrastat partnertyp** har ersatt **Partnertyp** i Intrastat-rapportering. Fältet **Partnertyp** används i SEPA (Single Euro Payments Area) för att definiera SEPA för direktdebitering (Core eller B2B). Fältet **Typ av Intrastat-partner** används endast för Intrastat-rapportering. På så sätt kan du ange olika värden för de två fälten om det behövs.
>
> Om fältet **Typ av Intrastat-partner** lämnas tomt används värdet från fältet **Partnertyp** för Intrastat-rapportering.

Utom för **Konfiguration av Intrastat-rapport**, **Datautbytesdefinitioner** och **Checklista för Intrastat-rapporter** måste du också konfigurera andra inställningar:

| Sida | Description |
| ---- | ----------- |
| **Länder/regioner** | Innan du börjar använda Intrastat-rapporter måste du också konfigurera sidan **Länder/regioner**. På den här sidan måste du lägga till **Kod för EU-land/region** och **Intrastatkod** för att ange en kod för landet/regionen som du vill ha handel med, eftersom det används i Intrastat-rapportering. |
| **EU tull statistiknr** | I många länder fastställer tullen och skattemyndigheterna åttasiffriga koder för olika artiklar. Du måste ange artikelkoden på sidan **EU tull statistiknr** för att artikeltransaktioner ska innehålla den information som krävs när den importeras till Intrastatjournalraden. Ta reda på koderna för de artiklar som ditt företag handlar med och skriv in dem på sidan **EU tull statistiknr**. |
| **Transportsätt** | Det finns sju ensiffriga koder för Intrastat-transportsätt. **1** för sjötransport, **2** för järnvägstransport, **3** för vägtransport, **4** flygtransport, **5** för brev, **7** för fasta installationer och **9** för egen framdrivning (t.ex. transport av en bil genom att köra den). [!INCLUDE[prod_short](includes/prod_short.md)] kräver inte dessa specifika koder, men vi rekommenderar att beskrivningarna ger liknande betydelse. |
| **Transaktionstyper** | Länder och regioner har olika koder för olika typer av Intrastat-transaktioner, till exempel ordinära inköp och försäljning, byte av returnerade varor och byte av inte returnerade varor. Ställ in alla koder som gäller för ditt land/din region. Dessa koder används sedan på snabbfliken **Utlandshandel** på försäljnings- och inköpsdokument, samt när du bearbetar returer. |
| **Transaktionsspecifikationer** | Skapa koder som komplement till beskrivning av transaktionstyp. |
  > [!NOTE]
  > Från och med januari 2022 kräver Intrastat olika transaktionskoder för utskick till privatpersoner eller icke momsregistrerade företag och momsregistrerade företag. För att uppfylla detta krav rekommenderar vi att du granskar och/eller lägger till nya transaktionskoder på sidan **Transaktionstyper** enligt kraven i ditt land. Du bör också granska och uppdatera fältet **Intrastat partnertyp** till *Person* för en privatperson eller icke momsregistrerat företag på relevant **Kund**-sida. Om du är osäker på vilken Intrastat-partnertyp eller transaktionstyp du ska använda rekommenderar vi att du frågar en expert i ditt land eller din region.

| **Fält** | **Beskrivning** |
| --------- | --------------- |
| **Nettovikt** | Vikt är en av de grundläggande konfigurationerna som är relaterad till Intrastat-rapportering eftersom **Total vikt** är obligatorisk för rapportering. För att vara redo för detta behov måste du även fylla i fältet **Nettovikt** på artikel- eller anläggningstillgångskortet. |
| **Kod för tillverkningsland** | Använd ISO alpha-koderna på artikel- eller anläggningstillgångskortet med två bokstäver för det land där varan erhölls eller producerades. Om varan har producerats i mer än ett land, är ursprungslandet det sista land där den bearbetades. |
| **Momsidentifieringsnummer för partneroperatör i den importerande medlemsstaten** | Detta är momsidentifieringsnumret för partneroperatören i den importerande medlemsstaten. Moms-ID används också vid utbyte av data inom EU-export mellan medlemsstater och gör det möjligt för medlemsstaterna att tilldela mottagna data till det importerande företaget i det egna landet. Rapporteringsenheter måste ange moms-ID för det företag som deklarerat förvärv av varor inom unionen i den importerande medlemsstaten. |

Du kan även ställa in:

* **Artikelkoder**: Tull- och skattemyndigheterna har fastställt numeriska koder som klassificera artiklar och tjänster. Du kan ange koder för artiklar.
* **Områden**: Kompletterande uppgifter om länder och regioner.
* **In-/utförselplatser**: Ange platser där du kan skicka eller ta emot artiklar till eller från andra länder. En flygplats är ett exempel på en in-/utförselplats. Du kan ange in-/utförselplatser på försäljnings- och inköpsdokument på snabbfliken **Utlandshandel**. Informationen kopieras också från artikeltransaktionerna när du skapar intrastatjournalen.
* **Kompletterande måttenhet**: Varuantalet för Intrastat-rapportering kan vara nettovikten (i kg) eller en kompletterande enhet. Om det krävs kompletterande enheter måste de konfigureras för artiklar och anläggningstillgångar.

#### <a name="set-up-transport-methods"></a>Konfigurera transportsätt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Transportmetoder** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="set-up-transaction-nature-codes"></a>Skapa koder av transaktionstyp

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Transaktionstyper** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="other-related-configurations"></a>Andra relaterade konfigurationer

Innan du använder funktionen Intrastat-rapportering måste du konfigurera vissa fält på kortet för artikel, anläggningstillgång, kund och leverantör.

#### <a name="item-cards"></a>Artikelkorten

Så här lägger du upp all nödvändig information om Intrastat på artikelkort:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. Markera det objekt som du vill konfigurera.
3. Expandera snabbfliken **Kostnader och bokföring** och fyll i **EU tull statistiknr**, **Kompletterande måttenhet** och **Kod för tillverkningsland/-region**.
4. Expandera snabbfliken **Lager** och ange decimalvärdet i fältet **Nettovikt**.

> [!NOTE]
> Du kan använda andra måttenheter som kompletterande måttenhet. Om detta inte är samma som **basmåttenheten**, måste du konfigurera måttenheten på sidan **Måttenheter för artikel**.

#### <a name="fixed-asset-cards"></a>Anläggningstillgångskort

Så här lägger du upp all nödvändig information om Intrastat på anläggningstillgångskort:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Välj anläggningstillgången som du vill konfigurera.
3. Expandera snabbfliken **Intrastat** och fyll i fälten **EU tull statistiknr**, **Nettovikt** och **Kompletterande måttenhet**.

> [!NOTE]
> Du kan använda andra måttenheter som kompletterande måttenhet. Oavsett vilken **måttenhetskod** du väljer kommer dess **kvantitet** i Intrastat-rapporter alltid att vara 1.

#### <a name="vendor-cards"></a>Leverantörskort

Innan du använder en leverantör i Intrastat-rapportering måste du ha en särskild **lands-/regionkod** och **momsregistreringsnr** för var och en av dem, utöver ytterligare information på sidan **Leverantörskort**:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.
2. Markera den leverantör som du vill konfigurera.
3. På snabbfliken **Intrastat** kan du ange standardvärden för fälten **Standardtransaktionsyp**, **Standardtransaktionstyp – Returer** och **Standardtransportsätt**.
4. Expandera snabbfliken **Betalningar** och välj alternativet i fältet **Intrastat-partnertyp** för att ange om leverantören är en person eller ett företag i Intrastat-rapportering.

#### <a name="customer-cards"></a>Kundkort

Innan du använder en kund i Intrastat-rapportering måste du ha en särskild **lands-/regionkod** och **momsregistreringsnr** för var och en av dem, utöver ytterligare information på sidan **Kundkort**:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Markera den kund som du vill konfigurera.
3. På snabbfliken **Intrastat** kan du ange standardvärden för fälten **Standardtransaktionsyp**, **Standardtransaktionstyp – Returer** och **Standardtransportsätt**.
4. Expandera snabbfliken **Betalningar** och välj alternativet i fältet **Intrastat-partnertyp** för att ange om leverantören är en person eller ett företag i Intrastat-rapportering.

#### <a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a>Exkludera artiklar och anläggningstillgångar från Intrastat-rapportering

Om det finns en orsak till att en viss artikel eller anläggningstillgång ska uteslutas från Intrastat-rapportering måste du ändra ett alternativ på deras kort.

##### <a name="exclude-an-item-from-intrastat-reporting"></a>Undanta en artikel från Intrastat-rapportering

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. Markera det objekt som du vill konfigurera.
3. Expandera snabbfliken **Kostnad och bokföring** och välj sedan fältet **Uteslut från Intrastat-rapport**.

##### <a name="exclude-a-fixed-asset-from-intrastat-reporting"></a>Exkludera en anläggningstillgång från Intrastat-rapportering

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Välj anläggningstillgången som du vill konfigurera.
3. Expandera snabbfliken **Intrastat** och välj sedan fältet **Uteslut från Intrastat-rapport**.

## <a name="country-specific-intrastat-setup"></a>Landsspecifika Intrastat-inställningar

<!-- PM's note: Currently, we will add only the 'Overview' topic; the topic 'Manage Intrastat Country Specifics' and country details will wait until 21.1 when I update with all country-based details -->

Kraven på Intrastat är likartade i alla medlemsstater i EU, även om det finns viktiga undantag. I teorin bör bestämmelserna tillämpas på samma sätt i alla medlemsstater. Det finns emellertid skillnader i genomförandet, eftersom vissa medlemsstater ger riktlinjer för hur de allmänna principerna i förordningen bör tillämpas i särskilda situationer (t.ex. handelsprover, varureturer etc.). Dessa riktlinjer kan ge olika resultat för olika situationer i EU:s medlemsstater. Vissa länder har därför en viss extra specifik information som skiljer sig från andra länder, och de har också ett annat filformat för rapportering.

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Se även

[Intrastat-rapportering Business Central](finance-how-report-intrastat.md)  
[Ekonomihantering](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
