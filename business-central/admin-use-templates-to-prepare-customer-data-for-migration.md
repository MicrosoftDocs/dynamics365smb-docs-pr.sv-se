---
title: Förbereda migrering av kunddata med mallar
description: Med RapidStart Services kan du använda konfigurationsfiler för att strukturera befintliga kunddata innan du migrerar huvuddata till det nya företaget i Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 8620
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: d9a90c0680d079a87436cea227becfa46435efd5
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522254"
---
# <a name="prepare-to-migrate-customer-data-with-templates"></a>Förbereda migrering av kunddata med mallar

När du har importerat och kopplat inställningsdatan i den nya databasen, kan du börja migrera kundens befintliga huvuddata, till exempel artikel- och kundnummer samt namn. För att se till att dessa data, skapas snabbt och exakt i det nya företaget, måste du använda mallar för att strukturera data.  

Vanligtvis skapar du datamallar för följande huvuddatatabeller:  

- **Kontakt**  
- **Kund**  
- **Artikel**  
- **Leverantör**  

Du kan dock skapa en mall struktur för, och koppla dem till valfri tabell i [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!TIP]  
> Du kan också använda datamallar för dagliga operationer för att skapa nya poster som baseras på mallar. Dessa datamallar fungerar bara för de huvuddata tabellerna som stöds. Mer information finns i exempelvis [Registrera nya artiklar](inventory-how-register-new-items.md).  

När du importerar kunddata från en fil, på samma sätt som för objekt, hämtas obligatoriska fältdata från den länkade datamallen. När du skapar en ny artikel anger du endast allmän information som namn, beskrivning och pris, och hämtar resten av obligatoriska fältdata från en vald datamall.

När du skapar en ny huvuddatapost, till exempel ett kundkort, är vissa fält obligatoriska och måste fyllas i. Du kan gruppera de flesta obligatoriska fält, till exempel bokföringsmallar och betalningsvillkor, för att skapa huvuddata registrerar enklare och stabilare. Du kan till exempel gruppera obligatoriska fält för tabell 18, **Kund**, som **Inrikes**, **Utrikes** eller **Exportera** typer.

> [!NOTE]
> Fält av BLOB-typen kan inte exporteras/importeras med Excel.

## <a name="to-select-a-data-template"></a>Så här väljer du en datamall

När du väljer en befintlig datamall måste du utvärderar om de mallar som du skapat för det nya företaget är tillräckliga för kunden. Granska fälten och värdena för att bestämma vilka mallar som är lämpligt för ett nytt företag.  

> [!TIP]  
> Med dessa datamallar kan du också snabbt skapa nya poster. Använd dem för snabbare och mer korrekt dataskapande. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfigurationsmallar** och väljer sedan relaterad länk.  
2. På sidan **Konfigurationsmallar** väljer du en datamall i listan och sedan åtgärden **Redigera**.  

Om standardmallarna inte uppfyller behoven kan du skapa nya mallar eller lägga till fält i en befintlig mall. Om standardmallarna är tillräckliga, kan du använda dem för att skapa transaktioner som baseras på huvuddatamallar.

## <a name="to-create-a-new-data-template"></a>Skapa en ny datamall.

Du kan skapa en ny datamall, om standardmallarna inte inte uppfyller behoven för ditt nya företag.  

> [!TIP]
> Om du skapar fler än en kan det vara praktiskt att anta en namnpraxis för fältet **Kod**.

Varje mall består av en rubrik och en rad för varje fält som ska ingå i mallen. När du skapar en mall, kan du ange vilka fält som alltid ska användas för data av en viss typ. Du kan till exempel skapa olika kundmallar som ska kopplas till olika kundtyper. När du skapar kunden som använder en mall kan du använda malldata för att fylla i vissa fält i förväg.

### <a name="to-copy-an-existing-data-template"></a>Kopiera en befintlig datamall

Du kan snabbt skapa en ny datamall genom att kopiera information från en befintlig datamall, som du sedan redigerar.

1. Öppna sidan **konfigurationsmallar**.
2. Välj åtgärden **Ny**.
3. Fyll i fältet **Kod**.
4. Välj åtgärden **Kopiera konfigurationsmall**.
5. På sidan **konfigurationsmallar**, markera en befintlig mall som du vill kopiera och välj sedan knappen **OK**.

Tabell-ID, tabellnamn och rader på den befintliga datamallen infogas i den nya mallen.

### <a name="to-create-a-data-template-header-manually"></a>Så här skapar du ett datamallhuvud manuellt

1. Öppna sidan **konfigurationsmallar**.
2. Välj åtgärden **Ny**.
3. Fyll i fältet **Kod**.
4. I fältet **Tabell-ID** anger du den tabell som denna mall avser. Fältet **Tabellnamn** fylls i automatiskt när fältet **Tabell-ID** ställs in.

### <a name="to-create-a-data-template-line-manually"></a>Så här skapar du en datamallrad manuellt

1. På första raden väljer du fältet **Fältnamn**. På sidan **Fältlista** visas en lista över tabellens fält.
2. Markera ett fält och välj sedan knappen **OK**. Fältet **Fälttext** fylls i med fältnamnet.
3. I fältet **Standardvärde** anger du ett lämpligt värde. I vissa fall kan du behöva använda ett värde som inte finns tillgängligt i databasen. I så fall kan du markera kryssrutan **Hoppa över relationskontroll** för att göra det möjligt att applicera data utan fel.

    > [!TIP]  
    > Eftersom fältet **Standardvärde** inte har ett uppslag till motsvarande [!INCLUDE[prod_short](includes/prod_short.md)]-fältalternativ kopierar och klistrar du in det värde som du vill ha från den relaterade sidan till mallen.

4. Markera kryssrutan **obligatorisk** om användare måste fylla i det aktuella området.

    > [!NOTE]
    > Kryssrutan är endast för information. Ingen affärslogik behövs. Till exempel kan användare inte skicka en faktura om postgrupper inte har konfigurerats. Du kan välja kryssrutan **obligatorisk** för de här fälten för att fylla i dem och därmed undvika en bokföringsfel senare.
5. I fältet **Referens** anger du nödvändig information om fältet.
6. Välj **OK**.

## <a name="to-export-to-a-template-in-excel"></a>För att exportera till en mall i Excel

Du kan skapa en Excel-arbetsbok att använda som mall baserat på strukturen i en tabell för en befintlig databas, snabbt och effektivt. Du kan sedan använda mallen för att samla ihop kunddata i ett konsekvent format för senare import till [!INCLUDE[prod_short](includes/prod_short.md)].

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Konfigurationsformulär** och väljer sedan relaterad länk.
2. Lägg till en tabell i listan eller välj en befintlig tabell. Mer information finns i [Administrera företagskonfigurationer i ett kalkylark](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Välj åtgärden **Visa fält** för att definiera de fält i tabellen som du vill ta med i mallen.
4. Välj åtgärden **Exportera till mall**.
5. Ange ett namn och spara Excel-filen. Excel-arbetsboken öppnas automatiskt.

Nu kan du ange kunddata i Excel-bladet. Om du har exporterat flera tabeller är varje tabell ett eget blad. Spara arbetsboken innan du fortsätter med nästa process.

> [!NOTE]  
> Följande fel kan uppstå om du kör en engelsk version av Excel men har konfigurerat regionala inställningar för ett annat språk än engelska: "Gammalt format eller ogiltig bibliotekstyp." Kontrollera om språkpaketet för språket som används har installerats för att åtgärda felet.

## <a name="to-import-from-a-template-in-excel"></a>Så här kan du importera från en mall i Excel

1. På sidan **Konfigurationsformulär** och sedan väljer du åtgärden **Importera från mall**.
2. Navigera till mallkalkylarket som du har skapat och klicka på åtgärden **Öppna**.
3. Om du vill lägga till insamlade kunddata i databasen väljer du åtgärden **Koppla Data**.

När du kopplar data från en mall i Excel till en undertabell som även har en konfigurationsmall kopplad till sig i konfigurationspaketet, kopplas standardfältvärdena från konfigurationsmallen också.

En transaktion med data som kopplas på det här sättet är fullständig eftersom den består av data som har angetts av användaren i Excel plus standardvärden som anges i konfigurationsmallen.

> [!NOTE]
> Om data i tabellerna i konfigurations paketet innehåller datum, till exempel bokföringsdatum på fakturor, tas datumen med i den tidszon som anges i [!INCLUDE[prod_short](includes/prod_short.md)]. 


## <a name="to-create-a-record-from-a-configuration-template"></a>Så här skapar du en post från en konfigurationsmall

Du kan använda strukturen av data som finns i datamallarna för att konvertera din information till poster i databasen, en efter en. För att kunna göra det använder du funktionen **Skapa instans**. Detta är en miniatyrversion av datamigreringsprocessen och kan vara användbar för att skapa prototyper eller hantera mindre dataskapningsuppgifter.  

Nedan visas hur du skapar ett artikelkort från en artikeldatamall. Du kan skapa en post från en datamall med samma procedur.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Konfigurationsmallar** och väljer sedan relaterad länk.  
2. Välj mallen **Artikel** och sedan åtgärden **Redigera**. För mer information, se [Att skapa en datamall](admin-use-templates-to-prepare-customer-data-for-migration.md#to-create-a-new-data-template).
3. Välj åtgärden **Skapa instans**. Ett artikelkort skapas.  
4. Välj knappen **OK**.  
5. För att granska det nya artikelkortet, välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
6. Öppna det nya artikelkortet.  
7. Expandera olika snabbflikar och verifiera att informationen skapas rätt på dem.  

## <a name="to-use-conversion-templates"></a>Använda konverteringsmallar

Du kan konvertera kontakter till kunder, leverantörer och anställda. 

### <a name="to-convert-a-contact-into-a-customer-vendor-or-employee"></a>Så här konverterar du en kontakt till en kund, leverantör eller anställd
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") , ange **Kontakter** och välj sedan rätt kontaktperson. 
2. På kontaktkortet väljer du **Åtgärder**, därefter **Funktioner** och sedan **Skapa som kund, leverantör, bank eller anställd**.


## <a name="to-use-a-configuration-template-on-a-record"></a>Så här använder du en konfigurationsdatamall på en post

Du kan koppla en datamall till valfri post, som finns i [!INCLUDE[prod_short](includes/prod_short.md)] och använda den här metoden för att ändra en transaktion. Men när du gör det, skriver du över befintliga värden i transaktionen med de i mallen. Därför bör du vara försiktig när du kopplar en mall till befintliga poster.

> [!WARNING]  
> Funktionen **Koppla mall** skriver över befintliga data i en post. Om den här funktionen används i huvuddataflytt, kommer den att skriva över importerade data när du skapar poster.

Följande procedur baseras på ett nytt kundkort.  

1. Skapa en kund. Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).
2. På sidan **Kundkort** väljer du åtgärden **Tillämpa mall**.  
3. På sidan **Kundmallar** markerar du en av mallarna och väljer sedan knappen **OK**.  

Standardvärdena från den valda kundmallen förs in på kundkortet.

> [!NOTE]
> Du kan inte använda Använd mall för att tömma fält på kunder, leverantörer och liknande. Du måste istället använda funktionen **Redigera i Excel**. Mer information finns i [Redigera i Excel](across-work-with-excel.md#edit-in-excel).

## <a name="see-also"></a>Se även

[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)  
[Registrera nya kunder](sales-how-register-new-customers.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]