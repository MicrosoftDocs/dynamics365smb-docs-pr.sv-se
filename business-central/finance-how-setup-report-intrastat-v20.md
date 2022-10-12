---
title: Skapa och rapportera Intrastat
description: Lär dig hur du konfigurerar funktioner för rapportering av Intrastat och att rapportera handel med företag i andra EU-länder.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.search.form: 308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 8451, 12202, 31077
ms.date: 05/23/2022
ms.author: bholtorf
ms.openlocfilehash: 5b54581c14d960b5cc52a896b41e7d7a864ee38d
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608337"
---
# <a name="set-up-and-report-intrastat"></a>Skapa och rapportera Intrastat

Alla företag i Europeiska unionen måste rapportera sin handel med andra länder/regioner inom EU. I Sverige måste du rapportera transport av varor till de statistiska myndigheterna varje månad. I programmet kallas detta för intrastatrapportering. Du använder sidan **Intrastatjournal** när du vill fylla i periodiska intrastatrapporter.

[!INCLUDE[intrastat-2022w2](includes/intrastat-2022w2.md)]

## <a name="required-and-optional-setups"></a>Nödvändiga och frivilliga inställningar

> [!IMPORTANT]
> Kundkort och leverantörskort innehåller ett fält, typ av **Intrastat-partnertyp**, som har samma alternativ värden som fältet **Partnertyp**: *"" (tom)*, *Företag* och *Person*. Fältet **Intrastat partnertyp** har ersatt **Partnertyp** i Intrastat-rapportering. **Partnertyp** används i SEPA för att definiera SEPA för direktdebitering (Core eller B2B). **Typ av Intrastat-partner** används endast för Intrastat-rapportering. På så sätt kan du ange olika värden för de två fälten om det behövs.
>
> Observera dock att om fältet **Typ av Intrastat-partner** lämnas tomt används värdet från fältet **partnertyp** för Intrastat-rapportering.

Innan du kan använda intrastatjournalen för att rapportera Intrastat-information, finns det flera saker som du måste ställa in:  

* **Intrastat-inställning**: Sidan Intrastat-inställningar används för att aktivera Intrastat-rapportering och ange standardvärden för rapporten. Du kan ange om du behöver rapportera Intrastat från leveranser (utskick), inleveranser (ankomst) eller båda beroende på tröskelvärden som anges i de lokala bestämmelserna. Du kan också ange standardtransaktionstyper för vanliga och returnerade dokument, som används för transaktionsrapportering.
* **Intrastatjournalmallar**: du måste ställa in de intrastatjournalmallar och intrastatjournaler som du kommer att använda. Eftersom intrastat rapporteras månadsvis måste skapa 12 intrastatjournaler baserade på samma mall.  
* **Artikelkoder**: Tull- och skattemyndigheterna har fastställt numeriska koder som klassificera artiklar och tjänster. Du kan ange koder för artiklar.
* **Koder för transaktionstyp**: länder och regioner har olika koder för olika typer av Intrastat-transaktioner, till exempel ordinär inköp och försäljning, byte av returnerade varor och byte av inte returnerade varor. Ställ in alla koder som gäller för ditt land/din region. Använd dessa koder på snabbfliken **Utlandshandel** på försäljnings- och inköpsdokument, samt när du bearbetar returer.

    > [!NOTE]
    > Från och med januari 2022 kräver Intrastat olika transaktionskoder för utskick till privatpersoner eller icke momsregistrerade företag och momsregistrerade företag. För att uppfylla detta krav rekommenderar vi att du granskar och/eller lägger till nya transaktionskoder på sidan **Transaktionstyper** enligt kraven i ditt land. Du bör också granska och uppdatera fältet **Intrastat partnertyp** till *Person* för privatpersoner eller icke momsregistrerade företag på relevant **Kund**-sida. Om du är osäker på vilken Intrastat partnertyp eller transaktionstyp du ska använda rekommenderar vi att du frågar en expert i ditt land eller din region.

* **Transportsätt**: det finns sju, ensiffrig kod för Intrastat transportsätt. **1** för sjötransport, **2** för järnvägstransport, **3** för vägtransport, **4** flygtransport, **5** för brev, **7** för fasta installationer och **9** för egen framdrivning (t. ex. transport av en bil genom att köra den). [!INCLUDE[prod_short](includes/prod_short.md)] kräver inte dessa koder, men vi rekommenderar att beskrivningarna ger liknande betydelse.  
* **Transaktionsspecifikationer**: Använd dessa för att komplettera beskrivningar från transaktionstyperna.  
* **Ursprungsland**: Använd ISO alpha-koderna med två bokstäver för det land där varan erhölls eller producerades. Om varan har producerats i mer än ett land, är ursprungslandet det sista land där den bearbetades.
* **Moms-identifieringsnummer för partneroperatören i den importerande medlemsstaten**: Det här är moms-ID-numret för partneroperatören i den importerande medlemsstaten. Moms-ID används också vid utbyte av data inom EU-export mellan medlemsstater och gör det möjligt för medlemsstaterna att tilldela mottagna data till det importerande företaget i det egna landet. Rapporteringsenheter måste ange moms-ID för det företag som deklarerat förvärv av varor inom unionen i den importerande medlemsstaten.

> [!NOTE]
> Det moms-ID för affärspartner som ska användas kan variera, beroende på affärsomständigheterna. Till exempel skiljer sig det ID som ska användas för t. ex. kedjeförsäljning, där en leverantör säljer en produkt till ett annat land och det företaget sedan säljer artikeln till en annan verksamhet i samma land, trepartshandel o.s.v. Om du är osäker på vilket moms-ID du ska använda rekommenderar vi att du frågar en expert i ditt land eller din region.

Du kan även ställa in:

* **Områden**: Använd dessa för att komplettera uppgifterna om länder och regioner.  
* **In-/ utförselplatser**: Använd dessa för att ange platser där du kan skicka eller ta emot artiklar till eller från andra länder. Flygplatsen Heathrow är ett exempel på en in-/utförselplats. Du kan ange in-/utförselplatser på försäljnings- och inköpsdokument på snabbfliken **Utlandshandel**. Informationen kopieras också från artikeltransaktionerna när du skapar intrastatjournalen.  

### <a name="to-set-up-intrastat-templates-and-batches"></a>Så här ställer du in intrastatjournalmallar och intrastatjournaler

Batch-jobbet Intrastat inkluderar endast artikeltransaktioner, inte redovisningstransaktioner. Om du har redovisningstransaktioner som bör ingå i intrastatrapporteringen måste du ange dem manuellt. Om du till exempel köper en dator från ett annat land eller en annan region inom EU, placeras den inte på lager utan bokförs på ett redovisningskonto. Den här typen av transaktioner måste registreras manuellt i intrastatjournalen.  

Du kan exportera transaktionerna till en fil som du kan skicka till de intrastatmyndigheterna. Du kan även skriva ut en rapport, lägga till informationen manuellt i formulären från myndigheterna och sedan skicka informationen.

> [!NOTE]
> Vi rekommenderar att du skapar en intrastatjournal varje månad.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Intrastatjournalmallar** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Skapa en mall för varje Intrastatformulär som du använder.  
3. För att skapa mallar, välj åtgärden **Journaler**.  
4. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Skapa en mall för varje Intrastatformulär som du använder.

> [!NOTE]
> I fältet **statistikperiod** anger du statistikperioden med fyra siffror varav de första två siffrorna representerar året och följande två siffror motsvarar månaden. Skriv till exempel 1706 för juni 2017.

### <a name="to-set-up-transport-methods"></a>Så här ställer du in transportsätt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Transportmetoder** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-which-intrastat-report-fields-are-mandatory"></a>Om du vill ställa in vilka Intrastatrapportfält som är obligatoriska

I vissa länder, exempelvis Spanien och Storbritannien, kräver myndigheterna att Intrastatrapporter omfattar, exempelvis leveransmetod för inköp eller andra värden när försäljningen är över ett visst gränsvärde. På sidan **Intrastat-inställningar** kan du ange att **Kontrollisteinställningar för Intrastat** anger obligatoriska fält på sidan **Intrastatjournal**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Intrastatinställningar** och väljer sedan relaterad länk.
2. Välj åtgärden **Kontrollisteinställningar för Intrastat**.
3. På sidan **Kontrollisteinställningar för Intrastat** väljer du **fältnamnet** för att välja det Intrastatrapportfält som du vill ska vara obligatoriskt.

### <a name="czechia"></a>Tjeckien

För tjeckiska företag måste du också ställa in artikelkoder och koder för transaktionstyp.  

#### <a name="to-set-up-commodity-codes"></a>Så här skapar du artikelkoder

Alla artiklar som du köper eller säljer måste ha en artikelkod.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikelkoder** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Om du vill tilldela en artikel en artikelkod, går du till sidan **artikelkort**, expanderar snabbfliken **kostnader och bokföring** och anger koden i fältet **Artikelkod**.

### <a name="italy"></a>Italien

För italienska företag måste du också ställa in artikelkoder och koder för transaktionstyp.  

#### <a name="to-set-up-transaction-nature-codes"></a>Så här skapar du koder av transaktionstyp

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Koder för transaktionstyp** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Om du ofta använder en kod av transaktionstyp kan göra du den till standard. Gör detta genom att gå till sidan **Intrastatinställningar** och välja koden.

## <a name="to-report-intrastat"></a>Att rapportera intrastat

När du har fyllt i Intrastatjournalen kan du köra åtgärden **Checklisterapport** när du vill kontrollera att all information i journalen är korrekt. Obligatoriska fält som du har angett på sidan **Kontrollisteinställningar för Intrastat** som saknar värden visas i faktaboxen Fel och varning på sidan **Intrastatjournal**. Därefter kan du skriva ut en intrastatrapport som ett formulär eller skapa en fil som ska skickas till skattemyndigheten i Sverige.  

### <a name="to-fill-in-intrastat-journals"></a>Så här fyller du i intrastatjournaler

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Intrastatjournal** och väljer sedan relaterad länk.  
2. På sidan **Intrastatjournal** i fältet **Journalnamn** väljer du relevant journal och sedan knappen **OK**.  
3. Välj åtgärden **Föreslå rader**. Fälten **Startdatum** och **Slutdatum** innehåller redan de datum som angavs för statistikperioden i journalen.  
4. I fältet **Omkostnad reglering %** kan du ange ett värde i procent som täcker transport och försäkring. Om du gör detta är innehållet i fältet **Statistiskt värde** i journalen proportionellt sett högre.  
5. Välj **OK** när du vill starta batchjobbet.  

När du kör batch-jobbet hämtas alla artikeltransaktioner inom statistikperioden och infogas som rader i intrastatjournalen. Du kan redigera raderna efter behov.  

> [!IMPORTANT]  
> Med batch-jobbet hämtas endast de transaktioner som innehåller en lands-/regionkod som en intrastatkod har angetts för på sidan **Länder/regioner**. Därför måste du ange intrastatkoder för de lands-/regionkoder som du vill köra batch-jobbet för. Batchjobbet ställer in fältet **Partners moms-ID** till *QV999999999999* för privatpersoner eller icke momsregistrerade företag (kunder med fältet **Intrastat partnertyp** inställt på *Person*), och det använder värdet för fältet **Transaktionstyp** på den bokförda artikeltransaktionen eller projekttransaktionen.

### <a name="to-modify-intrastat-journals-lines"></a>Så här ändrar du Intrastatjournalens rader

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Intrastatjournal** och väljer sedan relaterad länk.  
2. På sidan **Intrastatjournal** i fältet **Journalnamn** väljer du relevant journal och sedan knappen **OK**.  
3. Fönstret med användarfilter för att filtrera Intrastatjournalens rader utifrån kriterier. Filtrera till exempel efter **Partners moms-ID-** fält med värdet *QV 999999999999*.
4. Välj ikonen **Dela** ![Dela en sida i en annan app.](media/share-icon.png) och välj **Redigera i Excel**
5. I Excel ändrar du Intrastatjournalens rader som du har filtrerat bort. Till exempel kan du ändra värdena i fältet **Transaktionstyp**.  
6. Publicera de ändringar som du har gjort i Excel tillbaka till [!INCLUDE[prod_short](includes/prod_short.md)]

> [!NOTE]
> I [!INCLUDE[prod_short](includes/prod_short.md)]-versioner som inte har stöd för [**Redigera i Excel**](across-work-with-excel.md#edit-in-excel) för journaler, kan du skapa konfigurationspaket för att exportera och importera Intrastatjournal-rader i Excel. Mer information finns i [Migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsinnehållet.

### <a name="report-intrastat-on-a-form-or-a-file"></a>Rapportera intrastat på ett formulär eller en fil

Du måste skriva ut rapporten **Intrastat – formulär** för att erhålla den information som behövs i INTRASTAT-formuläret från de statistiska myndigheterna. Innan du kan göra detta måste du lägga upp intrastatjournalen och fylla i den. Om du både har försäljnings- och inköpstransaktioner måste du fylla i ett separat formulär för varje typ, vilket innebär att du måste skriva ut rapporten två gånger.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Intrastatjournaler** och väljer sedan relaterad länk.  
2. På sidan **Intrastatjournal** väljer du den relevanta journalen i fältet **Journalnamn**.  
3. Om du inte redan har fyllt i journalen gör du det nu, antingen manuellt eller genom att välja åtgärden **Föreslå rader**.  
4. Välj åtgärden **skriver ut intrastatjournal**.  
5. På snabbfliken **Intrastatjournalrad** lägger du till filtret **Typ** och anger om det är **Inleverans** eller **Utleverans**.  
6. Välj **skicka till** för att skriva ut rapporten.  

### <a name="report-intrastat-in-a-file"></a>Rapportera intrastat i en fil

Du kan skicka Intrastat-rapporten som en fil. Innan du skapar filen kan du skriva ut en kontrollrapport som innehåller samma information som filen.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Intrastatjournal** och väljer sedan relaterad länk.  
2. På sidan **Intrastatjournal** väljer du den relevanta journalen i fältet **Journalnamn**.  
3. Om du inte redan har fyllt i journalen gör du det nu, antingen manuellt eller genom att välja åtgärden **Föreslå rader**.  
4. Välj åtgärden **Skapa fil**.  
5. På sidan med batch-jobb väljer du knappen **OK**.  
6. Välj **Spara**.  
7. Bläddra till den plats där du vill spara filen och skriv filnamnet. Klicka på  **Spara**.

> [!NOTE]
> När en rad i rapporten Intrastat har en extra enhet, visas inte artikelns vikt eftersom det här värdet inte är obligatoriskt.

## <a name="reorganize-intrastat-journals"></a>Omorganisera intrastatjournaler

Eftersom du måste skicka en INTRASTAT-rapport varje månad och skapa en ny journal för varje rapport kommer det sannolikt att finnas många journaler. Journalraderna tas inte bort automatiskt. Om du vill kan du ordna om journalnamnen med jämna mellanrum. Du gör detta genom att ta bort de journaler som inte längre behövs. Även journalraderna i de här journalerna tas bort.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Intrastatjournaler** och väljer sedan relaterad länk.  
2. Om du vill visa alternativen väljer du fältet **Journalnamn**.  
3. Välj journalerna som tas bort, och välj sedan knappen **Ta bort**.  

## <a name="tariff-numbers"></a>EU tull statistiknr

I många länder fastställer tullen och skattemyndigheterna åttasiffriga koder för olika typer av artiklar. För att artikeltransaktioner ska innehålla nödvändig information när programmet importerar dem till intrastatjournalraden, måste du ha angett statistiknumret på sidan **EU tull statistiknr**. Ta reda på koderna för de artikeltyper som ditt företag handlar med och skriv in dem på sidan **EU tull statistiknr**.

Lägg till alla koder du har användning för på sidan **EU tull statistiknr**. Du måste fylla i koderna på artikelkortet innan du börjar att bokföra. När du har lagt upp koderna anger du dem i fältet **EU tull statistiknr** på artikelkortet. Du måste även fylla i fältet **Nettovikt** på artikelkortet.

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Se även

[Ekonomihantering](finance.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
