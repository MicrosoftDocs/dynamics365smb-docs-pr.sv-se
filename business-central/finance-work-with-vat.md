---
title: Så här arbetar du med moms på försäljning och inköp
description: 'I den här artikeln beskrivs olika sätt att arbeta med moms både manuellt och med automatisk installation, för att hjälpa dig att uppfylla de land/regionsspecifika bestämmelserna.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'VAT, sales, purchases'
ms.search.form: '7, 118, 130, 142, 459, 460, 525'
ms.date: 05/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="work-with-vat-on-sales-and-purchases"></a>Arbeta med moms på försäljning och inköp

Om landet eller regionen kräver att du beräknar och rapporterar mervärdesskatt (moms) på försäljnings- och inköpstransaktioner kan du ställa in [!INCLUDE[prod_short](includes/prod_short.md)] för att beräkna moms. Mer information finns i [ställa in beräkningar och bokföring av metoder för moms](finance-setup-vat.md).

Det finns emellertid vissa momsrelaterade uppgifter som du kan göra manuellt. Du kan t. ex. behöva korrigera ett bokfört belopp om du upptäcker att en leverantör använder en annan avrundningsmetod.  

> [!TIP]
> Du kan låta [!INCLUDE[prod_short](includes/prod_short.md)] validera momsregistreringsnummer och annan företagsinformation när du skapar eller uppdaterar dokument. Mer information finns i [validera momsregistreringsnummer](finance-how-validate-vat-registration-number.md).

## <a name="calculating-and-displaying-vat-amounts-on-sales-and-purchase-documents"></a>Beräkna och visa momsbelopp i försäljnings- och inköpsdokument

När du väljer ett artikelnummer i fältet **Nr**. i ett försäljnings-eller inköpsdokument fyller [!INCLUDE[prod_short](includes/prod_short.md)] i fälten **Enhetspris** och **Radbelopp**. Enhetspriset kommer antingen från kortet **Artikel** eller från artikelpriserna för artikeln och kunden. [!INCLUDE[prod_short](includes/prod_short.md)] beräknar radbeloppet när du anger en kvantitet för raden.  

Om du vill att enhetspriser och radbelopp ska inkludera moms – till exempel om du säljer till detaljhandelskonsumenter – markerar du kryssrutan **Priser inklusive moms** i dokumentet. Mer information finns i [Inkludera eller exkludera moms på priser och radbelopp](#including-or-excluding-vat-in-prices-and-line-amounts). 

Du kan beräkna och visa momsbelopp i försäljnings- och inköpshandlingar på olika sätt. Skillnaden beror på vilken typ av kund eller leverantör du har att göra med. Du kan också ändra det momsbelopp som har beräknats manuellt, exempelvis för att detta ska matcha det momsbelopp som har beräknats av leverantören för en given transaktion.

### <a name="including-or-excluding-vat-in-prices-and-line-amounts"></a>Inkludera eller exkludera moms för priser och radbelopp

Om du väljer kryssrutan **Priser inklusive moms** på ett försäljningsdokument inkluderar fälten **Enhetspris** och **Radbelopp** moms. Som standard ingår inte moms i värdena i dessa fält. Namnen på fälten visar om priserna inkluderar moms.  

Du kan lägga upp en standarduppsättning av **Priser inklusive moms** för alla försäljningsdokument för en kund i fältet **Priser inklusive moms** på **Kund**-kortet. Du kan också lägga upp att artikelpriser ska anges inklusive eller exklusive moms. Normalt är priserna på artikelkortet exklusive moms.

Följande tabell innehåller en översikt över hur enhetsprisbeloppen för ett försäljningsdokument beräknas när du inte har lagt upp priser på sidan **Försäljningspriser**:  

|**Fältet Försäljningspris inklusive moms på artikelkortet**|**Fältet Priser inkl. moms**|**Utförd åtgärd**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Inte aktivt|Inte aktivt|**Enhetspriset** på artikelkortet kopieras till fältet **Enhetspris exkl. moms** på försäljningsraderna.|  
|Inte aktivt|Aktivt|Momsbeloppet beräknas per enhet och läggs till **enhetspriset** på artikelkortet. Detta totala enhetspris anges sedan i **fältet Enhetspris inkl. moms** på försäljningsraderna.|  
|Aktivt|Inte aktivt|Programmet beräknas momsbeloppet som inkluderas i fältet **Enhetspris** på **artikelkortet** med hjälp av den momsprocentsats i förhållande till rörelsebokföringsmallen för moms (pris) samt produktbokföringsmallen för moms. **Enhetspris** på artikelkortet, minus momsbeloppet, anges sedan i **Enhetspris exl. moms** på försäljningsraderna. Mer information finns i [Använda rörelsebokföringsmallar för moms och kundprisgrupper](finance-work-with-vat.md#using-vat-business-posting-groups-and-customer-price-groups).|  
|Aktivt|Aktivt|**Enhetspriset** på artikelkortet kopieras till fältet **Enhetspris inkl. moms**.|

#### <a name="using-vat-business-posting-groups-and-customer-price-groups"></a>Använda rörelsebokföringsmallar för moms och kundprisgrupper

Om du vill att moms ska ingå i priserna kan du använda rörelsebokföringsmallar för moms för att beräkna beloppet baserat på momsbokföringsinställningarna för gruppen. Mer information finns i [Konfigurera bokföringsmallar för moms](finance-setup-vat.md#set-up-vat-business-posting-groups).

Beroende på vad du vill göra kan du tilldela en rörelsebokföringsmall för moms till kunder eller försäljningsdokument på följande sätt:

* Om du vill använda samma momssats för alla kunder kan du välja en grupp i fältet **Rörelsebokföringsmall för moms (pris)** på sidan **Försäljningsinställningar**.
* Om du vill använda en momssats för en specifik kund kan du välja en grupp i fältet **Rörelsebokföringsmall för moms (pris)** på sidan **Kundkort**. 
* Om du vill använda en momssats för en specifik grupp kunder kan du välja en grupp i fältet **Rörelsebokföringsmall för moms (pris)** på sidan **Kundprisgrupp**. Detta kan till exempel vara användbart när du vill att ett pris ska gälla för alla kunder i en viss geografisk region eller en viss bransch.
* På alla försäljningsdokument i fältet **Rörelsebokföringsmall för moms**. Momsbeloppet som anges för gruppen används endast för det dokument som du för tillfället arbetar med.

> [!NOTE]
> Om du inte anger någon grupp i fältet **Rörelsebokföringsmall för moms (pris)** kommer inte att inkluderas i priser.

#### <a name="examples"></a>Exempel

Faktorer såsom det land eller den region som du säljer till, eller vilken typ av branscher du säljer till, kan påverka det momsbelopp som du måste redovisa. En restaurang kan till exempel debitera 6 % moms för måltider som äts på plats, och 17 % för avhämtming. Detta gör du genom att skapa en rörelsebokföringsmall för moms (pris) för på plats och en för avhämtning.

## <a name="working-with-vat-date"></a>Arbeta med momsdatum

### <a name="vat-date-in-documents"></a>Momsdatum i dokument

När du skapar nya försäljnings- eller inköpsdokument baseras **momsdatumet** på inställningen i fältet **Standarddatum för moms** på sidan **Redovisningsinställningar**. Det här standardvärdet kan vara samma som **Bokföringsdatum** eller **Dokumentdatum**. Om du behöver ett annat momsdatum kan du manuellt ändra värdet i fältet **Momsdatum**. När du bokför dokumentet visas **momsdatumet** i bokföringsdokumentet och i moms-och redovisningstransaktionerna.

> [!NOTE]
> Om fältet **Momsdatum** inte är tillgängligt i dina dokument eller journaler, betyder **Använd inte funktionen för momsdatum** väljs fältet **Användning av momsdatum** på sidan **Redovisningsinställningar**.  

> [!IMPORTANT]
> Om du konfigurerar **Kontrollera momsperiod** i **Redovisningsinställningar** som **Spärra bokföring inom stängd period** eller **Spärra bokföring inom stängd och varna för frisläppt period**, du kan bokföra dokument eller journal endast om datumet i fältet **Momsdatum** som inte finns i en stängd period i **Momsreturperioder**. Även om perioden i **Momsreturperioder** är öppen, kan du få en varning baserad på **Momsreturstatus** och konfiguration i **Kontrollera momsperiod**.

> [!IMPORTANT]
> Från och med version 23.1 kan du välja att förhindra eller tillåta bokföring av **Momsdatum** för särskilda dataintervall med hjälp av fältet **Tillåt momsdatum från** och **Tillåt momsdatum till To** i **Momsinställningar** och **Användarinställningar**. Om du använder äldre versioner kan du förhindra eller tillåta bokföring av **Momsdatum** för särskilda dataintervall med hjälp av fältet **Tillåt bokföring från** och **Tillåt bokföring till** i **Redovisningsinställningar** och **Användarinställningar**.  

> [!NOTE]
> Om du lämnar **Momsdatum** tomt, [!INCLUDE [prod_short](includes/prod_short.md)] används standardkonfigurationen från **Standardmomsdatumet** i **Redovisningsinställningar** som **Momsdatum** i den bokförda transaktionen.  

### <a name="modifying-the-vat-date-in-posted-entries"></a>Ändra momsdatum i bokförda transaktioner

Vid behov kan du ändra de bokförda dokumenten för momsdatumet. För att ändra datumet i fältet **momsdatum** för bokförda dokument, följ stegen nedan:

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **momstransaktioner** och väljer sedan relaterad länk. 
2. Hitta transaktionen med fel momsdatum.  
3. Klicka på åtgärden **Redigera lista** och ange sedan korrekt datum i fältet **Momsdatum**.  
4. När du stänger sidan kommer det nya momsdatumet ändras i relaterade **redovisningstransaktioner** och i det bokförda dokumentet.  

> [!NOTE]
> Du kan ändra fältet **Momsdatum** i **Momstransaktioner** endast om ditt aktuella datum inte är i en stängd momsreturperiod. Även om perioden i **Momsreturperioder** är öppen, kan du få en varning baserad på **Momsreturstatus**.  

> [!NOTE]
> Om dokumentet har fler än en **Momstransaktion** behöver du bara ändra värdet i fältet **Momsdatum** i en transaktion som är kopplad till dokumentet. För att hålla transaktionerna konsekventa ändrar [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt momsdatumet i momstransaktioner som hör till den här transaktionen. [!INCLUDE [prod_short](includes/prod_short.md)] uppdaterar **momsdatumet** i andra tabeller (redovisningstransaktioner och dokument) uppdateras, men endast relaterade till den här transaktionen.  

## <a name="correcting-vat-amounts-manually-on-sales-and-purchase-documents"></a>Manuellt korrigera momsbelopp i försäljnings- och inköpsdokument

Du kan korrigera redan bokförda momstransaktioner så att du kan ändra det totala beloppet för utgående eller ingående moms utan att ändra nettobeloppet. Om du t.ex. tar emot en faktura från en leverantör med ett felaktigt momsbelopp.  

Även om du har ställt in en eller flera kombinationer för hantering av importmoms, måste du skapa minst en produktbokföringsmall för moms. Du kan till exempel ge det namnet **KORREKT** för korrigeringssyfte, om du inte kan använda samma redovisningskonto i **Ingående moms** på momsbokföringsinställningsraden. Mer information finns i [Ställa in beräkningar och bokföring av metoder för moms](finance-setup-vat.md).

Om en kassarabatt har beräknats baserad på ett fakturabelopp inklusive moms kan du återställa den del av momsbeloppet som utgörs av kassarabatten när kassarabatten beviljas. Observera att du måste aktivera fältet **Justering för kassarabatt** i både redovisningsinställningarna generellt och i momsbokföringsinställningarna för särskilda kombinationer av rörelsebokföringsmallar för moms och produktbokföringsmallar för moms.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-sales-documents"></a>Så här ställer du in systemet för manuell momsregistrering i försäljningsdokument

Följ dessa steg för att aktivera manuella momsändringar på försäljningsdokument. Stegen är liknande på sidan **Inköpsinställningar**.

1. På sidan  **Redovisningsinställningar** ange en  **Max. tillåten momsdifferens** mellan det belopp som har beräknats automatiskt och det manuella beloppet.  
2. På sidan **Tillåt momsdifferens** aktiverar du reglaget **Försäljningsinställningar** .  

### <a name="to-adjust-vat-for-a-sales-document"></a>Så här justerar du moms för ett försäljningsdokument

1. Öppna den aktuella försäljningsordern.  
2. Välj åtgärden **Statistik**.  
3. På snabbfliken **Fakturering** väljer du värde i fältet **Antal momsrader**.
4. Redigera fältet **Momsbelopp**.   

> [!NOTE]  
> Det totala momsbeloppet för fakturan visas på raderna grupperade per moms-ID. Du kan justera beloppet i fältet **Momsbelopp**på raderna för varje moms-ID. När du ändrar fältet **Momsbelopp** utförs en kontroll för att undersöka att du inte har ändrat momsen med mer än det belopp som du har angett som maximal tillåten differens. Om beloppet ligger utanför intervallet i **Max. tillåten momsdifferens** visas en varning som anger den maximala tillåtna differensen. Du kommer inte att kunna fortsätta förrän beloppet justeras inom godkända parametrar. Klicka på **OK** och ange ett annat **Momsbelopp** som ligger inom det tillåtna intervallet. Om momsdifferensen är lika med eller lägre än den maximala tillåtna differensen fördelas momsen proportionellt över dokumentraderna som har samma moms-ID.  

## <a name="calculating-vat-manually-using-journals"></a>Manuell momsberäkning med hjälp av journaler

Du kan också justera momsbelopp i redovisnings-, försäljnings- och inköpsjournaler. Du kan behöva göra en justering om du anger en leverantörsfaktura i journalen och momsbeloppet som [!INCLUDE[prod_short](includes/prod_short.md)] beräknade och momsbeloppet på den leverantörsfaktura du har tagit emot skiljer sig.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-general-journals"></a>Så här ställer du in systemet för manuell momsregistrering i redovisningsjournaler

Du måste utföra följande steg innan du kan ange moms manuellt i en redovisningsjournal.  

1. På sidan  **Redovisningsinställningar** ange en  **Max. tillåten momsdifferens** mellan det belopp som har beräknats automatiskt och det manuella beloppet.  
2. På sidan **Redovisningsjournalmallar** markerar du kryssrutan **Tillåt momsdifferens** för den relevanta journalen.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-sales-and-purchase-journals"></a>Så här ställer du in systemet för manuell momsregistrering i försäljnings- och inköpsjournaler

Du måste utföra följande steg innan du kan ange moms manuellt i en försäljnings- och inköpsjournal.

1. På sidan **Inköpsinställningar** markerar du kryssrutan **Tillåt momsdifferens**.  
2. Upprepa steg 1 för sidan **Försäljningsinställningar**.
3. När du har slutfört den inställning kan du justera fältet **Momsbelopp** i redovisningsjournalraden eller fältet **Momsbelopp bal.** i försäljnings- eller inköpsjournalen så att det motsvarar momsbeloppet på fakturan. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerar att differensen inte är större än det angivna maxbeloppet.  

> [!NOTE]  
> Om differensen är större visas en varning som anger den maximala tillåtna differensen. Innan du fortsätter måste du justera beloppet. Klicka på **OK** och ange ett annat belopp som ligger inom det tillåtna intervallet. Om momsdifferensen är lika med eller lägre än den maximala tillåtna differensen visar [!INCLUDE[prod_short](includes/prod_short.md)] differensen i fältet **Momsdifferens**.  

## <a name="posting-import-vat-with-purchase-invoices"></a>Bokföra du importmoms med inköpsfakturor
I stället för att använda journaler för att bokföra en importmomsfaktura, kan du använda en inköpsfaktura.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Konfigurera inköp för bokföring av fakturor med specificerad importmoms

1. Skapa ett leverantörskort för den importavdelning som skickar importmomsfakturan till dig. **Gen. rörelsebokföringsmall** och **Moms rörelsebokföringsmall** måste ställas in på samma sätt som redovisningskontot för importmomsen.  
2. Skapa en **produktbokföringsmall** för importmomsen och skapa **produktbokf.mall för standardmoms** för den kopplade **produktbokföringsmallen** för importmomsen.  
3. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.  
4. Välj redovisningskontot för importmoms och välj sedan åtgärden **Redigera**.  
5. På snabbfliken **Bokföring**  i fältet **Produktbokföringsmall** för importmomsen. [!INCLUDE[prod_short](includes/prod_short.md)] fyller automatiskt i **Moms, produktbokföringsmall**.  
6. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Bokföringsinställningar** och välj sedan relaterad länk.  
7. Skapa en kombination av **Gen. rörelsebokföringsmall** för skattemyndigheterna och **Produktbokföringsmall** för importmoms. Välj importmervärdeskattredovisningskontot för den här kombinationen i fältet **Inköpskonto**.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-after-you-complete-the-setup"></a>Så här skapar du en ny faktura för leverantören när du har slutfört inställningen

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsfakturor** och väljer sedan relaterad länk.  
2. Skapa en ny inköpsfaktura.  
3. I fältet **Inköpsleverantörsnr** markerar du leverantören och klickar på **OK**.  
4. I inköpsraden, i fältet **Typ** välj **Redovisningskonto**, och i fältet **Nr.** markera redovisningskontot för importmoms.  
5. I fältet **Antal** anger du **1**.  
6. I fältet **Inköpspris exkl. moms** skriver du in momsbeloppet.  
7. Bokföra fakturan  

## <a name="processing-certificates-of-supply"></a>Behandla leveransintyg

När du säljer varor till en kund i ett annat EU-land/region, måste du skicka kunden ett leveransintyg som kunden måste signera och returnera till dig. Följande tillvägagångssätt används för att behandla leveransintyg för försäljningsutleveranser, men samma moment gäller för serviceleveranser av artiklar och returutleveranser till leverantörer.  

### <a name="to-view-certificate-of-supply-details"></a>Så här visar du information om leveransintyg
1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokförda försäljningsutleveranser** och väljer sedan relaterad länk.  
2. Välj den relevanta försäljningsutleveransen till en kund i ett annat EU-land/-region.  
3. Välj **Information om leveransintyg**.  
4. Som standard, om den momsbokföringsmall som har ställts in för kunden har kryssrutan **Leveransintyg krävs** markerad, så är fältet **Status** angett till **Obligatoriskt**. Du kan uppdatera fältet för att visa om intyget har tagits emot från kunden.  

> [!Note]  
>  Om inställningen av momsbokföringsmallen inte har kryssrutan **Leveransintyg krävs** markerad skapas en post, och fältet **Status** får värdet **Ej tillämpbart**. Du kan uppdatera fältet för att visa rätt information om status. Du kan manuellt ändra statusen från **Ej tillämpbart** till **Obligatoriskt**och från **Obligatoriskt** till **Ej tillämpbart** efter behov.  

   När du uppdaterar fältet **Status** till **Obligatoriskt**, **Inlevererat**eller **Ej inlevererat**, skapas ett certifikat.  

> [!TIP]  
>  Du kan använda sidan **Leveransintyg** för att få en vy över alla bokförda utleveranser som ett leveransintyg har skapats för.  

5. Välj **Skriv ut leveransintyg**.  

> [!Note]  
> Du kan granska och skriva ut dokumentet. När du väljer **Skriv ut leveransintyg** och skriver ut dokumentet, väljs kryssrutan **Utskrivet** automatiskt. Dessutom, om den inte redan har angetts, uppdateras statusen för intyget till **Obligatoriskt**. Du inkluderar det utskrivna intyget med utleveransen.  

### <a name="to-print-a-certificate-of-supply"></a>Så här skriver du ut ett leveransintyg

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokförda försäljningsutleveranser** och väljer sedan relaterad länk.  
2. Välj den relevanta försäljningsutleveransen till en kund i ett annat EU-land/-region.  
3. Välj **Skriv ut leveransintyg**.  

> [!NOTE]  
> Alternativt kan du skriva ut ett intyg från fönstret **Leveransintyg**.  

4. Aktivera reglaget **Utskriftsradinformation** om du vill inkludera information från raderna i utleveransdokumentet på leveransintyget.  
5. Om du vill ha [!INCLUDE[prod_short](includes/prod_short.md)] skapa certifikat för postade försändelser som inte hade ett, aktivera reglaget **Skapa leveransintyg om de inte redan skapats**. När du har aktiverat reglaget upprättas nya certifikat för alla bokförda utleveranser som inte har intyg i det valda intervallet  
6. Som standard gäller filterinställningarna för utleveransdokumentet som du har valt. Fyll i information om filter för att välja ett visst leveransintyg som du vill skriva ut.  
7. På sidan **Leveransintyg** väljer du åtgärden **Skriv utPrint** för att skriva ut rapporten eller välja åtgärden **Förhandsgranska** för att visa den på skärmen.  

   > [!Note]  
   > Fältet **leveransintygstatus** och **Utskrivet** är uppdaterade för leveransen på sidan **leveransintyg**.  

8. Du måste skicka det utskrivna leveransintyget till kunden för signatur.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Så här uppdaterar du statusen för ett leveransintyg för en utleverans

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokförda försäljningsutleveranser** och väljer sedan relaterad länk.  
2. Välj den relevanta försäljningsutleveransen till en kund i ett annat EU-land/-region.  
3. I fältet **Status** väljer du önskat alternativ.  

   Om kunden har returnerat det undertecknade leveransintyget väljer du **Inlevererat**. Fältet **Inleveransdatum** uppdateras. Som standard anges inleveransdatumet till aktuellt arbetsdatum.  

   Du kan ändra datumet för att visa datumet då du fick kundens signerade leveransintyg. Du kan också lägga till en länk till det undertecknade intyget med hjälp av standardkoppling för [!INCLUDE[prod_short](includes/prod_short.md)].  

   Om kunden inte returnerar det undertecknade leveransintyget väljer du **Ej inlevererad**. Du måste sedan skicka kunden en ny faktura som omfattar moms, eftersom skattemyndigheten inte accepterar originalfakturan.  

Om du vill visa en grupp av certifikat startar du från på sidan **Leveransintyg** och uppdaterar sedan information om status för utestående intyg när du tar emot dem från kunderna. Den uppdaterade informationen kan vara användbar när du vill söka efter alla intyg som har en viss status, till exempel **Obligatoriskt**, för vilka du vill uppdatera statusen till **Ej inlevererat**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Så här uppdaterar du statusen för en grupp med leveransintyg

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Leveransintyg** och väljer den relaterade länken.  
2. Filtrera fältet **Status** fältet till värdet som du vill ha för att skapa listan över intyg som du vill hantera.  
3. Om du vill uppdatera information om status, Välj **Redigera lista**.  
4. I fältet **Status** väljer du önskat alternativ.  

   Om kunden har returnerat det undertecknade leveransintyget väljer du **Inlevererat**. Fältet **Inleveransdatum** uppdateras. Som standard anges inleveransdatumet till aktuellt arbetsdatum.  

   Du kan ändra datumet för att visa datumet då du fick det signerade leveransintyget. Du kan också lägga till en länk till det undertecknade intyget med hjälp av standarddokumentkoppling för [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]
> Du kan inte skapa ett nytt leveransintyg på sidan **Leveransintyg** när du navigerar till den med den här proceduren. Om du vill skapa ett intyg för en leverans som inte var inställd för att kräva en öppnar du den bokförda försäljningsutleveransen och använder någon av de två procedurer som beskrivs tidigare:  
>
> * Så här skapar du manuellt ett leveransintyg  
> * Så här skriver du ut ett leveransintyg.

## <a name="see-also"></a>Se även

[Förbereda beräknings- och bokföringsmetoder för moms](finance-setup-vat.md)  
[Rapportera moms till skattemyndigheterna](finance-how-report-vat.md)  
[Validera ett momsregistreringsnummer](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
