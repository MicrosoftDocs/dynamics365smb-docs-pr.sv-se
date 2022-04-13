---
title: Migrera kunddata
description: Du kan migrera befintliga kunddata från ett befintligt system till Business Central med hjälp av en guide för assisterad konfiguration. Du kan också använda Excel och RapidStart Services.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 1799, 1807, 8632, 1800, 1340, 8614, 8615
ms.date: 02/18/2022
ms.author: edupont
ms.openlocfilehash: 492ec993dfbf33f90fc601b1d6f8f27319ee39c9
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515725"
---
# <a name="migrate-customer-data"></a>Migrera kunddata

Du kan migrera befintliga kunddata från ett befintligt ERP-system till [!INCLUDE[prod_short](includes/prod_short.md)] online med hjälp av molnmigreringsprocessen för versioner som stöds. Du kan också migrera till [!INCLUDE [prod_short](includes/prod_short.md)] lokalt med hjälp av datamigreringsverktygen i RapidStart Services och sedan växla till molnet. Mer information finns i [Migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administratörsinnehållet (endast på engelska).  

I den här artikeln tittar vi på de konfigurationsfiler som du kan exportera från och importera till [!INCLUDE [prod_short](includes/prod_short.md)]. Innehållet har skrivits med lokala distributioner i åtanke.  

> [!NOTE]
> Fält av BLOB-typen kan inte exporteras/importeras med Excel.

Sidan **Flyttningsöversikt** och **Konfigurationskalkylark** ger åtkomst till funktioner och vyer för alla uppgifter som avser datamigrering. Vi rekommenderar att du migrerar en tabell i taget för att hantera beroenden i dina data. I flytta kan du också nå huvuddatatabellerna, som innehåller information om kunder, leverantörer, artiklar, kontakter och redovisningen.  

## <a name="to-import-configuration-packages"></a>Så här importerar du konfigurationspaket
När du skapar ett nytt företag, kan du importera företagsinställningar för det nya företaget. Du importerar inställningarna från en .rapidstart-fil, vilket levererar paketinnehållen i ett komprimerat format. En motsvarande uppsättning standarddatamigreringstabeller importeras. Datauppsättningen innehåller huvuddatatabeller och inställningsdatatabellerna. Den första uppgiften vid datamigrering är att utvärdera om standardflyttningsinställningen uppfyller det nya företagets behov.

> [!NOTE]  
>  Du kan inte byta namn på en fil som inte redan är ett RapidStart Services konfigurationspaket som en .rapidstart-konfigurationspaketfil och sedan försöka importera den. Om du försöker att göra det, kommer du att få ett felmeddelande.  

Innan du börjar måste du kontrollera att du har behörighet att köra RapidStart Services-objekten. Du kan till exempel ha behörighetsgrupperna SUPER eller D365 RAPIDSTART. Vi rekommenderar också att du är på ett Rollcenter med länkar till RapidStart Services, till exempel Rollcenter för administration. Mer information finns i [Att ändra rollen](ui-change-basic-settings.md#to-change-the-role).  

> [!IMPORTANT]  
> När du exporterar och importerar konfigurationspaket mellan två företagsdatabaser ska databaserna ha samma schema för att alla data säkert ska överföras korrekt. Det betyder att databaserna ska ha samma tabell- och fältstruktur, där tabellerna har samma primärnycklar och fälten har samma ID och datatyper.  
>
>  Du kan importera ett konfigurationspaket som har exporterats från en databas och har ett annat schema än i måldatabasen. Men alla tabeller och fält i konfigurationspaketet som saknas i måldatabasen importeras inte.
>
> Tabeller med olika primärnycklar och fält med olika datatyper importeras inte heller korrekt. Om t. ex. konfigurationspaketet innehåller tabellen **50000 Kund** som har primärnyckeln **Code20** och databasen som du importerar paketet till innehåller tabellen **50000 Kundbankkonto** som har primärnyckeln **Code20 + Code 20** importeras inte data.  

1. Öppna det nya företaget.  
2. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfigurationspaket** och väljer sedan relaterad länk.  
3. Välj åtgärden **Importera paket**. Navigera till det .rapidstart-paket som du vill importera och klicka på åtgärden **Öppna**. Under importen expanderas paketinnehållen, och paketposten skapas.  

    När importen är klar kan du visa antalet konfigurationstabeller som har importerats i fältet **Antal tabeller**.  
4. Om du vill granska listan över konfigurationstabeller väljer du åtgärden **Visa**.  
5. Använd paketet genom att välja åtgärden **Koppla paket**.  

    > [!NOTE]  
    >  Informationen om datamigreringen baseras på konfigurationsmallar, om du anger en. Du måste först uppdatera mallen för att ändra listan över fält.  

6.  Om du vill granska fältvalen markerar du en tabell, klickar på fliken **Rader** fliken och väljer åtgärden **Fält**. Jämför och granska antalet fält som är tillgängliga mot antalet fält där data har kopplats.  

Om urvalet av tabeller inte uppfyller dina behov, kan du skapa en eller flera nya datamigreringsfiler. Om filerna är tillräckliga kan du fortsätta datamigreringen med hjälp av Excel- eller XML-filer.

## <a name="to-create-a-data-migration-file"></a>Så här skapar du en datamigreringsfil

Du kan skapa nya datamigreringsfiler och anpassa dem för att stödja din verksamhet.  

> [!TIP]
> En fil kan dock endast användas för att migrera ett fält som har egenskapsuppsättningen **FieldClass** inställd på **Normal**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfigurationspaket** och väljer sedan relaterad länk.  
2. Markera och öppna paketet som du vill använda för att flytta data och välj sedan åtgärden **Hämta tabeller**. Sidan **Hämta pakettabell** öppnas.  
3. I fältet **TableID** anger du ett tabellnummer eller väljer ett tabell-id i listan, till exempel, tabell **Kund**. Fälten **Tabellnamn** fylls i automatiskt.  
4. Välj den nya flyttningstabellen, klicka på fliken **tabeller** och välj åtgärden **Fält**. Sidan **Flyttningsfält** öppnas.  
5. Rensa kryssrutan **Inkludera fält** för de fält som du inte vill importera och klicka sedan på åtgärden **Ange inkluderade** eller **Rensa inkluderade**.  

> [!IMPORTANT]  
>  Om kryssrutan **Inkludera fält** är markerad som standard, är det fältet del av primärnyckeln. Urvalet ska inte tas bort, eftersom eventuella fel kan inträffa, och posten då inte kan importeras.  
>
>  Om du anger ett fält som har ett samband med en annan tabell, väljs kryssrutan **Validera fält** automatiskt. Validering kan leda till uppdatering av andra fält i denna och andra tabeller och körs i fältnummerordning.  

En ny flyttningstabell skapas.  

## <a name="to-export-data-migration-files"></a>Så här exporterar du datamigreringsfiler
När du har bestämt vilka tabeller du vill överföra kunddata till, exporterar du filerna.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfigurationspaket** och väljer sedan relaterad länk.  
2. Markera och öppna paketet som du vill använda för export.
3. Markera den eller de tabell(er) som du vill exportera och klicka sedan på åtgärden **Exportera till Excel**.
4. Spara den exporterade Excel-filen.  
5. Upprepa den här proceduren för alla relevanta datamigreringstabeller. Om du väljer flera tabellerna samtidigt sker exporten av deras data till en gemensam arbetsbok.  

Om tabellen är tom innehåller datamigreringsfilen tomma celler för fält som du valde när du väljer eller skapar flyttningstabeller för ditt nya företag. Om den markerade datamigreringstabellen innehåller data ska den exporteras.  

## <a name="to-map-values-to-be-used-during-import"></a>Så här mappar du värden som ska användas vid import
När du använder data som har importerats från Excel eller från ett RapidStart-paket behandlar och hanterar [!INCLUDE[prod_short](includes/prod_short.md)] mappningen utifrån tabellrelationer:  

- Om du definierar en mappning direkt för ett fält i en tabell använder [!INCLUDE[prod_short](includes/prod_short.md)] den.  

- Om fältet har en relation till en annan tabell söker [!INCLUDE[prod_short](includes/prod_short.md)] efter den mappning som definierats för primärnyckelfältet i den relaterade tabellen. Den relaterade tabellen måste dock ingå i konfigurationspaketet.  

- Om mappningen av information har definierats på båda platserna, direkt för fältet och för primärnyckeln i den relaterade tabellen, kommer [!INCLUDE[prod_short](includes/prod_short.md)] att söka efter mappningen på båda platserna.  

- Om samma mappningar definieras direkt för ett fält och i den relaterade tabellen, men har olika nya värden, får den mappning som definieras direkt för fältet prioritet över den mappning som definieras för tabellen som fältet refererar till.  

I följande procedurer ska du granska i förväg vilka värden som du vill bibehålla under flyttningsprocessen. För att utföra följande procedurer kommer du att behöva datamigreringsfiler (.xlsx) som du har exporterat från [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [så här: exportera flyttningstabeller](admin-migrate-customer-data.md#to-export-data-migration-files).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfigurationspaket** och väljer sedan relaterad länk.
2. Öppna paketet för det aktuella företaget.  
3. Välj tabellen som du vill mappa värden för, och på fliken **Tabeller** väljer du sedan åtgärden **Fält**.  
4. För varje fält som du vill koppla väljer du åtgärden **Mappa**.  
5. Ange värdet som du vill ändra i fältet **Gammalt värde**. Ange värdet som du vill att det gamla värdet ska ändras till i fältet **Nytt värde**. Välj knappen **OK**.  
6. Importera kunddata. Mer information finns också i [Så här importerar du kunddata](admin-migrate-customer-data.md#to-import-customer-data).
7. Se om det finns några fel rapporterade i fältet **Antal paketfel**. Om det finns söker du ned för att visa fel. Sidan **Konfig. paketposter** öppnas.
8. Välj åtgärden **Visa fel**. Du får då följande fel: **XX är inget giltigt alternativ. Giltiga alternativ är: XX**. Välj **OK**.  
9. Använd den mappning som du har ställt in genom att välja åtgärden **Koppla Data**.  

### <a name="mapping-example"></a>Mappningsexempel  
Följande exempel visar hur [!INCLUDE[prod_short](includes/prod_short.md)] implementerar mappning av definitioner.  

1. Skapa en konfigurationstabell som har en **säljare/köpare**-tabell Definiera en mappning för fältet **Kod**.  
2. Lägg till ytterligare tabeller i paketet, till exempel **Kund** och **Leveratör**. Dessa båda tabeller refererar till tabell **Säljare/köpare** via fälten **Säljarkod** och **Köparkod**.  
3. När du kopplar data beaktas även den mappning du angav för fältet **Kod** i tabellen **Säljare/köpare** vid bearbetningen av fälten **Säljarkod** och **Köparkod**.

## <a name="to-add-additional-values-to-prod_short"></a>Så här lägger du till ytterligare värden i [!INCLUDE[prod_short](includes/prod_short.md)]  
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfigurationspaket** och väljer sedan relaterad länk.  
2. Välj tabellen som du vill lägga till ytterligare värden i, och på fliken **Tabeller** väljer du sedan åtgärden **Fält**.  
3. Välj kryssrutan som du vill att [!INCLUDE[prod_short](includes/prod_short.md)] ska tillåta ytterligare värden för vid migrering **Skapa saknade koder**.  
4. Importera kunddata. Mer information finns också i [Så här importerar du kunddata](admin-migrate-customer-data.md#to-import-customer-data).

## <a name="to-clean-up-and-process-data-before-applying-data"></a>Så här rensar du upp och bearbetar data innan du kopplar data
I vissa fall kan det hända att du vill rensa upp kunddata och bearbeta dem, innan du kopplar dem till databasen. Om du vill göra det, använd batch-jobbet **Konfig.paket – behandla** för att åtgärda fel som exempelvis:  

- Konvertera data och decimaler till det format som krävs av de regionala inställningarna på en användares dator.  
- Ta bort inledande/efterföljande blanksteg eller specialtecken.  

När du har kört batchjobbet, använd följande procedur för att bearbeta datan.  

1. Öppna konfigurationspaketet för företaget.  
2. Välj åtgärden **Bearbeta data**.  
3. Använd den mappning som du har ställt in genom att välja åtgärden **Koppla Data**.

## <a name="to-migrate-customer-data"></a>Så här kan du flytta kunddata
När du har exporterat en flyttningstabell blir ditt nästa steg att skriva in kundens bakåtkompatibla data. För att underlätta dina arbetsuppgifter kan du dra nytta av XML behandlingsverktygen som ingår i Excel. Du kan även använda inbyggda Excel funktioner för att hjälp med dataformatering och för att ange data i rätt cell.

Om du behöver hjälp med XML så aktiverar du fliken **Utvecklare** i Excel-balken och väljer sedan åtgärden **Källa** för att visa XML-uppställningen för din flyttningstabell såsom den visas i Excel.

Följande procedur baseras på en Excel-blad som du har skapat för datamigrering. Mer information finns i [så här: exportera flyttningstabeller](admin-migrate-customer-data.md#to-export-data-migration-files).

> [!IMPORTANT]  
> Ändra inte kolumnerna i Excel-kalkylarken. Om de flyttats, ändras eller tas bort, kan kalkylarket inte importeras till [!INCLUDE[prod_short](includes/prod_short.md)].

1. Öppna den exporterade datafilen i Excel. Det finns ett kalkylark med namnet på tabellen.
2. Byt namn på Blad1 för att ange att detta kalkylark ska användas för att omformar data. Kopiera huvudraden utan formatering från den exporterade tabellen till den nya kalkylarket.
3. Kopiera alla dina kunddata på ett tredje kalkylark. Byt namn på bladet och kalla det Bakåtkompatibla data.
4. Gör en Excel formel för att koppla data i omformnings kalkylarket mellan fälten i den exporterade kalkylarket och de bakåtkompatibla data för kunden.
5. När du har mappat alla data kopierar du dataintervallet till tabellkalkylarket.
6. Spara filen och se till att du inte ändrar filtypen.

Nu är du redo att importera datamigreringsfilerna som innehåller bakåtkompatibla data för kunder till [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-import-customer-data"></a>Så här importerar du kunddata
När kunddatan har registrerats i datamigreringsfilerna i Excel importerar du filerna till [!INCLUDE[prod_short](includes/prod_short.md)].

1. Öppna sidan **Konfig. paketkort**.
2. Välj tabellen som du vill importera data för, och på fliken **Tabeller** väljer du sedan åtgärden **Importera från Excel**.
3. Leta upp och öppna filen du vill importera data från.
4. På sidan **Konfig. förhandsgranskning av paket** granskar du det innehåll som ska importeras.

    Sidan **Konfig. förhandsgranskning av paket** ger en överblick av Excel-filinnehåll som ska importeras. Där finns även information om att ett nytt konfigurationpaket har skapats eller en befintlig har uppdaterats och om nya konfigurationspaketrader (tabeller) har skapats eller om ett befintligt uppdateras.    
5. Välj åtgärden **Importera**.

Data från filen importeras till tabellerna i konfigurationspaketet. I fältet **Antal paketposter** kan du visa antalet poster som har importerats. Dessutom kan du visa antalet flyttningsfel.

## <a name="to-validate-customer-data"></a>Så här validerar du kunddata
Kunddata måste valideras innan du kan kopplar transaktioner till [!INCLUDE[prod_short](includes/prod_short.md)]-databasen.  

> [!NOTE]  
>  Oftast skapas inte inte felaktiga data i databasen. Programmet kan dock blockeras tillfälligt, om en importerad flyttningstabell innehåller fel.  

1. På sidan **Flyttningsöversikt**, granska fältet **antal migreringsfel** för att se om några fel inträffade under importen.  
2. Om det finns fel väljer du flyttningstabellen och sedan, på fliken **Tabeller**, väljer du åtgärden **Fel**. Kryssrutan **Ogiltig** är markerad för varje transaktion som har ett fel.  
3. Markera en rad och välj sedan åtgärden **Visa fel** för att visa fel.  

    Fältet **Feltext** innehåller orsaken för felet. Fältet **Fältrubrik** innehåller fältrubriken på det fält som innehåller fel.  
4.  För att korrigera ett fel eller på annat sätt göra en uppdatering: på sidan **Flyttningsöversikt**, välj åtgärden **Flyttningspost** och sedan på sidan **Flyttningspost**, korrigerar du posten som innehåller felet.  

När du har gjort en korrigering, tas posten bort från listan över poster på sidan **Flyttningsdatafel**.  

Nu är du redo för att koppla kundens data till databasen.  

## <a name="to-apply-customer-data"></a>Så här tillämpar du kunddata
När du har importerat alla datamigreringsposter med giltiga, felfria data kan du tillämpa posterna i databasen [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Öppna sidan **Konfigurationspaket**.  
2. Välj tabellen för den datamigreringsfil som du vill koppla och välj sedan åtgärden **Koppla data**.

I fältet **Antal paketposter** kan du visa antalet databasposter som har skapats. I fältet **Antal databasposter** kan du bekräfta att rätt antal poster har skapats, detta genom att välja länken i fältet.  

Kundföretagets databas är nu skapad, och grunddata har importerats. Ditt nästa steg i implementeringsprocessen går ut på att utbilda användare, definiera processer, skapa ytterligare data, anpassa rapporter, och så vidare.

## <a name="see-also"></a>Se även  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]