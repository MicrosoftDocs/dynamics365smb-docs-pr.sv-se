---
title: "Förbereda migrering av kunddata | Microsoft Docs"
description: "När du har importerat och kopplat inställningsdatan i den nya databasen, kan du börja migrera kundens befintliga huvuddata, till exempel artikel- och kundnummer samt namn. För att se till att dessa data, skapas snabbt och exakt i det nya företaget, måste du använda mallar för att strukturera data."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8724bf11537b384ae88960e40f24f1d9dbbbd484
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="prepare-to-migrate-customer-data"></a>Förbereda migrering av kunddata
När du har importerat och kopplat inställningsdatan i den nya databasen, kan du börja migrera kundens befintliga huvuddata, till exempel artikel- och kundnummer samt namn. För att se till att dessa data, skapas snabbt och exakt i det nya företaget, måste du använda mallar för att strukturera data.  

Vanligtvis skapar du datamallar för följande huvuddatatabeller:  

-   **Kontakt**  
-   **Kund**  
-   **Artikel**  
-   **Leverantör**  

Du kan dock skapa en mall struktur för, och koppla dem till valfri tabell i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>  Du kan också använda datamallar för dagliga operationer för att skapa nya poster som baseras på mallar. Dessa datamallar fungerar bara för de huvuddata tabellerna som stöds. Mer information finns i exempelvis [Registrera nya artiklar](inventory-how-register-new-items.md).  

När du importerar kunddata från en fil, på samma sätt som för objekt, hämtas obligatoriska fältdata från den länkade datamallen. När du skapar en ny artikel anger du endast allmän information som namn, beskrivning och pris, och hämtar resten av obligatoriska fältdata från en vald datamall.  

När du skapar en ny huvuddatapost, till exempel ett kundkort, är vissa fält obligatoriska och måste fyllas i. Du kan gruppera de flesta obligatoriska fält, till exempel bokföringsgrupper och betalningsvillkor, för att skapa huvuddata registrerar enklare och stabilare. Du kan till exempel gruppera obligatoriska fält för tabell 18, **Kund**, som **Inrikes**, **Utrikes**eller **Exportera** typer.

## <a name="to-select-a-data-template"></a>Så här väljer du en datamall
När du väljer en befintlig datamall måste du utvärderar om de mallar som du skapat för det nya företaget är tillräckliga för kunden. Granska fälten och värdena för att bestämma vilka mallar som är lämpligt för ett nytt företag.  

> [!TIP]  
>  Med dessa datamallar kan du också snabbt skapa nya poster. Använd dem för snabbare och mer korrekt dataskapande. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationsmallar** och välj sedan relaterad länk.  
2. I fönstret **Konfig. mallista** väljer du en datamall i listan och sedan åtgärden **Redigera**.  

Om standardmallarna inte uppfyller behoven kan du skapa nya mallar eller lägga till fält i en befintlig mall. Om standardmallarna är tillräckliga, kan du använda dem för att skapa transaktioner som baseras på huvuddatamallar.

## <a name="to-create-a-data-template"></a>För att skapa en datamall
Du kan skapa en ny datamall, om standardmallarna inte inte uppfyller behoven för ditt nya företag. Om du skapar fler än en kan det vara praktiskt att anta en namnpraxis för fältet **Kod**.

Varje mall består av ett huvud och rader. När du skapar en mall, kan du ange vilka fält som alltid ska användas för data av en viss typ. Du kan till exempel skapa olika kundmallar som ska kopplas till olika kundtyper. När du skapar kunden som använder en mall kan du använda malldata för att fylla i vissa fält i förväg.

### <a name="to-create-a-data-template-header"></a>Så här skapar du ett datamallhuvud
1. Öppna fönstret **Konfig. mallista**.
2. Välj åtgärden **Ny**.
3. I fältet **Tabell-ID** anger du den tabell som denna mall avser. Fältet **Tabellnamn** fylls i automatiskt när fältet **Tabell-ID** ställs in.

### <a name="to-create-a-data-template-line"></a>Så här skapar du ett datamallrad
1. På första raden väljer du fältet **Fältnamn**. I fönstret **Fältlista** visas en lista över tabellens fält.
2. Markera ett fält och välj sedan knappen **OK**. Fältet **Fälttext** fylls i med fältnamnet.
3. I fältet **Standardvärde** anger du ett lämpligt värde. I vissa fall kan du behöva använda ett värde som inte finns tillgängligt i databasen. I så fall kan du markera kryssrutan **Hoppa över relationskontroll** för att göra det möjligt att applicera data utan fel.

    > [!TIP]  
    > Eftersom fältet **Standardvärde** inte har ett uppslag till motsvarande [!INCLUDE[d365fin](includes/d365fin_md.md)]-fältalternativ kopierar och klistrar du in det värde som du vill ha från den relaterade sidan till mallen.

    > Markera kryssrutan **Obligatoriskt**. Kryssrutan är endast för information. Här får du information om att data måste skrivas in i fältet av användaren, men ingen affärslogik behövs. Du kan till exempel inte fakturera och bokföra en order om bokföringsmallar inte har lagts upp. Eftersom bokföringsmallar måste användas kan du markera kryssrutan **Obligatoriskt** för de här fälten.

3. I fältet **Referens** anger du nödvändig information om fältet.
4. Välj **OK**.

## <a name="to-export-to-a-template-in-excel"></a>För att exportera till en mall i Excel
Du kan skapa en Excel-arbetsbok att använda som mall baserat på strukturen i en tabell för en befintlig databas, snabbt och effektivt. Du kan sedan använda mallen för att samla ihop kunddata i ett konsekvent format för senare import till [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationsformulär** och välj sedan relaterad länk.
2. Lägg till en tabell i listan eller välj en befintlig tabell. Mer information finns i [Administrera företagskonfigurationer i ett kalkylark](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Definiera fälten från tabellen som ska ingå i mallen.
4. Välj åtgärden **Exportera till mall**.
5. Ange ett namn och spara Excel-filen. Excel-arbetsboken öppnas automatiskt.

Nu kan du ange kunddata i Excel-bladet. Om du har exporterat flera tabeller är varje tabell ett eget blad. Spara arbetsboken innan du fortsätter med nästa process.

> [!NOTE]  
> Följande fel kan uppstå om du kör en engelsk version av Excel men har konfigurerat regionala inställningar för ett annat språk än engelska: "Gammalt format eller ogiltig bibliotekstyp." Kontrollera om språkpaketet för språket som används har installerats för att åtgärda felet.

## <a name="to-import-from-a-template-in-excel"></a>Så här kan du importera från en mall i Excel
1. I fönstret **Konfig. kalkylark** väljer du åtgärden **Importera från mall**.
3. Navigera till mallkalkylarket som du har skapat och klicka på åtgärden **Öppna**.
4. Om du vill lägga till insamlade kunddata i databasen väljer du åtgärden **Koppla Data**.

När du kopplar data från en mall i Excel till en undertabell som även har en konfigurationsmall kopplad till sig i konfigurationspaketet, kopplas standardfältvärdena från konfigurationsmallen också.

En transaktion med data som kopplas på det här sättet är fullständig eftersom den består av data som har angetts av användaren i Excel plus standardvärden som anges i konfigurationsmallen.

## <a name="to-create-a-record-from-a-configuration-template"></a>Så här skapar du en post från en konfigurationsmall
Du kan använda strukturen av data som finns i datamallarna för att konvertera din information till poster i databasen, en efter en. För att kunna göra det använder du funktionen **Skapa instans**. Detta är en miniatyrversion av datamigreringsprocessen och kan vara användbar för att skapa prototyper eller hantera mindre dataskapningsuppgifter.  

Nedan visas hur du skapar ett artikelkort från en artikeldatamall. Du kan skapa en post från en datamall med samma procedur.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationsmallar** och välj sedan relaterad länk.  
2. Välj mallen **Artikel** och sedan åtgärden **Redigera**. För mer information, se avsnittet "Så här skapar du en datamall".
3. Välj åtgärden **Skapa instans**. Ett artikelkort skapas.  
4. Välj knappen **OK**.  
5. För att granska de nya artikelkorten, välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.  
6. Öppna det nya artikelkortet.  
7. Expandera olika snabbflikar och verifiera att informationen skapas rätt på dem.  

## <a name="to-use-a-configuration-template-on-a-record"></a>Så här använder du en konfigurationsdatamall på en post
Du kan koppla en datamall till valfri post, som finns i [!INCLUDE[d365fin](includes/d365fin_md.md)] och använda den här metoden för att ändra en transaktion. Men när du gör det, skriver du över befintliga värden i transaktionen med de i mallen. Därför bör du vara försiktig när du kopplar en mall till befintliga poster.

> [!WARNING]  
>  Funktionen **Koppla mall** skriver över befintliga data i en post. Om den här funktionen används i huvuddataflytt, kommer den att skriva över importerade data när du skapar poster.

Följande procedur baseras på ett nytt kundkort.  

1. Skapa en kund. Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).
2. I fönstret **Kundkort** väljer du åtgärden **Tillämpa mall**.  
3. I fönstret**Kundmallar** markerar du en av mallarna och väljer sedan knappen **OK**.  

Standardvärdena från den valda kundmallen förs in på kundkortet.

## <a name="see-also"></a>Se även  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)  
[Registrera nya kunder](sales-how-register-new-customers.md)

