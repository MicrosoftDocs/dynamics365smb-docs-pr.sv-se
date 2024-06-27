---
title: Ställa in bokföring av koncerninterna transaktioner
description: Så här skapar du ett koncerninternt partnerskap.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 09/27/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621, 653_Primary'
ms.service: dynamics-365-business-central
---
# Ställ in koncerninterna transaktioner

Koncerninterna partnerskap gör det enklare att hantera redovisningsprocesser när två eller flera dotterbolag för ett företag ofta gör affärer med varandra. Partner kan utbyta transaktioner som försäljning och inköp samt hantera dem manuellt eller automatiskt. När en partner till exempel skickar en försäljningsjournalrad till en annan partner skapas en inköpsjournalrad för den mottagande partnern.

Den koncerninterna kontoplanen kan till exempel vara en version av den synkroniserade partnerns kontoplan. Varje partner kopplar sina konton till den koncerninterna kontoplanen. Varje partner kopplar även deras dimensioner och dimensionsvärden till de koncerninterna dimensionerna.

> [!NOTE]
> I 2023 utgivningscykel 1 har vi introducerat en förbättrad sida för **Koncernintern inställning**. Den nya sidan gör det enklare att skapa ett koncerninternt partnerskap genom att konsolidera alla inställningsuppgifter på en enda sida. Om du är en ny för [!INCLUDE [prod_short](includes/prod_short.md)], använder du redan den nya upplevelsen. Om du är en befintlig kund kan administratören aktivera funktionsväxlingen **Acceptera automatiskt koncerninterna transaktioner i redovisningsjournalen** på sidan **Funktionshantering**.
>
> Uppgifterna i den här artikeln förutsätter att funktionsväxlingen är aktiverad. Om du redan har ställt in ett koncerninternt partnerskap kan du fortsätta att använda det.

## Innan du börjar

Innan du börjar konfigurera det koncerninterna partnerskap finns det flera beslut att fatta.

|Beslut  |Beskrivning  |
|---------|---------|
|Vilken kontoplan ska ligga till grund för den koncerninterna kontoplanen?     | Samma koncerninterna kontoplan måste användas i alla koncerninterna kontoplaner. Du kan basera den koncerninterna kontoplanen på kontoplanen från ett av företagen i partnerskapet eller skapa en ny koncernintern kontoplan. Du kopplar de konton som ska användas i partnerskapet på båda sätt, så att varje partner skickar och tar emot transaktioner på rätt konton. Mer information om hur du ställer in den koncerninterna kontoplanen finns på [Ställa in koncerninterna kontoplaner](#set-up-the-intercompany-charts-of-accounts).         |
|Vilka dimensioner ska ligga till grund för de koncerninterna dimensionerna?     | Om du använder koncerninterna dimensioner måste de vara desamma för alla företag i partnerskapet. När du har angett koncerninterna dimensioner kopplar du motsvarande dimensionsvärden. Mer information om att koppla dimensionsvärden finns i [Ställa in koncerninterna dimensioner](#set-up-intercompany-dimensions).        |
|Vilka partner är kunder eller leverantörer eller båda?     |  Lära dig mer om hur du ställer in kunder och leverantörsföretag i ett koncerninternt partnerskap i [Ställa in koncerninterna partner som kunder och leverantörer](#set-up-intercompany-partners-as-customers-and-vendors).       |
|Vill du ange bankkonton som ska användas i partnerskapet?| Du kan påskynda arbetet med att registrera betalningstransaktioner genom att ange vilket bankkonto som ska användas för varje partnerföretag. Läs mer på [Ange vilka bankkonton som ska användas för koncerninterna partner](#specify-the-bank-accounts-to-use-for-intercompany-partners). |
|Hur vill du identifiera företagen i partnerskapet?     | Alla parter måste komma överens om en unik identifieringskod för koncernintern partner för varje företag. Du ska tilldela koden till kund- och leverantörskort för att identifiera relaterade transaktioner. Lär dig mer om identifierare i [Skapa nummerserier](ui-create-number-series.md).        |
|Hur vill du hantera artikelnummer?     | Om koncerninterna rader innehåller artiklar kan du använda egna artikelnummer eller lägga upp partnerns artikelnummer för artikeln. Det gör du antingen i fältet **Leverantörens artikelnr** eller i fältet **Gemensamt artikelnr** som är kopplat till artikelkortet. Du kan också använda åtgärden **artikelreferens** för att koppla artikelnummer till dina koncerninterna partnerbeskrivningar av artiklarna. Om du vill veta mer om artikelreferenser går du till [Använd artikelreferenser](inventory-how-use-item-cross-refs.md).        |
|Är resurserna involverade?     | Om koncerninterna försäljningstransaktioner inkluderar fyller du i fältet **Ink.red.ktonr konc.int partner** på den aktuella resursens resurskort. Fältet innehåller numret på det koncerninterna redovisningskontot i partnerföretaget som beloppet för resursen ska bokföras på. Om du vill ha mer information om resurser, gå till [Konfigurera resurser](projects-how-setup-resources.md).<br><br>**OBS**<br>Koncerninterna inköpstransaktioner som inkluderar resurser, anläggningstillgångar och artikelomkostnader stöds inte fullt ut. I partnerföretaget kommer fältet **Radtyp** att vara tomt på inköpsdokument rader där dessa enheter ingår. Du måste uppdatera fältet manuellt.        |

## Översikt över steg för att komma igång

På sidan **koncerninterna inställningar** kan du ställa in följande komponenter i koncerninterna transaktioner:

* Ditt företags koncerninterna inställningar.
* Företaget som ska bli synkroniseringspartner.
* Den koncerninterna kontoplanen som alla partner använder för att utbyta transaktioner.
* Mappningar mellan konton i kontoplanen och den koncerninterna kontoplanen för ankommande och avgående transaktioner för varje partner.
* De koncerninterna dimensionerna och dimensionsvärdena som ska användas och hur de kopplas till dimensioner för varje partner.
* De företag som är koncerninterna partner.
* Företag som är leverantörer eller kunder, eller både och.

## Konfigurera synkroniseringspartner

Alla partner måste använda samma koncerninterna kontoplan och vid behov samma koncerninterna dimensioner. Du kan spara tid när du ställer in partnerskap med hjälp av kontoplanen och dimensionerna för en av partnern som original plan för den koncerninterna kontoplanen och dimensionerna. Det företag som du använder som grund kallas för *synkroniseringspartner*. Synkroniseringspartnern är vanligtvis moderbolaget, men det behöver inte vara det.

På sidan **Koncernintern inställning** specificerar varje partner synkroniseringspartner i fältet **Synkroniseringspartner**. Därefter anges den koncerninterna kontoplanen och de koncerninterna dimensionerna automatiskt för dem, baserat på inställningarna för synkroniseringspartner. Partnern använder sedan sidorna **Mappning av koncernintern kontoplan** och **Mappning av koncernintern dimension** för att koppla deras kontoplan och dimensioner till koncernintern kontoplan och dimensioner och vice versa. 

> [!NOTE]
> Det är viktigt att du kopplar konton och dimensioner i båda riktningarna. Det vill säga både till den koncerninterna kontoplanen och dimensionerna och från dem till dina egna konton och dimensioner.

### Få kontakt med partner i en annan klientorganisation eller miljö

Om en eller flera partner [!INCLUDE [prod_short](includes/prod_short.md)] finns i en annan klientorganisation eller miljö finns det några extra steg för att skapa anslutningen. Stegen gäller för alla partner i en annan klientorganisation eller miljö.

* Konfigurera [!INCLUDE [prod_short](includes/prod_short.md)] som en registrerad app i Azure-portalen.
* Lägg till och aktivera appregistreringen i [!INCLUDE [prod_short](includes/prod_short.md)].
* Utbyta information om sina koncerninterna inställningar. Varje partner kan få denna information från **Koncerninterna inställningarna**, **Åtgärder**, **Anslutningsinformation**.

   |Kopiera från partnerns konfiguration  |Kopiera till dina inställningar  |
   |---------|---------|
   |URL för aktuell anslutning     |Anslutnings-URL för intern partner         |
   |Aktuellt företags-ID     |Företags-ID för intern partner         |
   |Koncerninternt ID     |Koncerninternt ID för koncernintern partner         |
   |Företagsnamn     |Företagsnamn för koncernintern partner         |

* Byt ut följande autentiseringsinställningar så att de [!INCLUDE [prod_short](includes/prod_short.md)] kan autentiseras när den ansluter. Varje partner kan få denna information från sin registrerade app. Mer information om hur du skapar en registrerad app finns i [Skapa en registrerad app i Azure-portalen](#create-a-registered-app-in-azure-portal).  

  * Klient-ID
  * Klienthemlighet
  * Tokenslutpunkt
  * Omdirigerings-URL

Kör **Koncerninterna inställningarna**, **Åtgärder**, **Anslutningsinformation** i alla företag för att ange informationen. 

#### Skapa en registrerad app i Azure-portalen

Den här processen är bara nödvändig om du vill ansluta till en partner vars [!INCLUDE [prod_short](includes/prod_short.md)] finns i en annan klientorganisation eller miljö.

> [!TIP]
> Det är en bra idé att ha en textredigerare öppen, till exempel Anteckningar, medan du skapar din registrerade app. Du behöver en del av informationen när du kör **Koncerninterna inställningarna**, **Åtgärd**, **Anslutningsinformation**, så det är bra att ha informationen till hands.

1. Gå till [Azure-portalen](https://portal.azure.com/#home).
2. Välj **Microsoft Entra ID**-tjänst.
3. Välj i navigeringsfönstret **Appregistreringar**.
4. På sidan **Appregistreringar** väljer du **ny registrering**.
5. Ge appen ett namn.
6. Välj kontotypen **Konton i organisationens katalog (en Microsoft Entra ID-klientorganisation – flera organisationer i samma installation)**.
7. För omdirigerings-URI:en går du till fältet **Välj en plattform**, väljer **Webb** och anger sedan URI:en. Till exempel \**https://businesscentral.dynamics.com/OAuthLanding.htm**.

  Om du arbetar med en inbäddad ISV kan du behöva en annan URI.

8. Registrera appen.
9. På sidan **Koncernintern app** i navigeringsfönstret väljer du **API-behörigheter**.
10. Välj åtgärden **Lägg till behörighet**.
11. På fliken **Microsoft API:er**, välj **Dynamics 365 Business Central**.
12. I fönstret **Begär API-behörigheter** väljer du **Programbehörigheter** och sedan behörigheten **API.ReadWrite.All**.
13. På sidan **koncernintern app | API-behörigheter**, välj åtgärden **Bevilja administratörsmedgivande för Contoso** och beviljar sedan medgivande.
14. Välj **Certifikat och hemligheter** i navigeringsfönstret.
15. Välj fliken **Klienthemligheter** och välj sedan **Ny klienthemlighet**.
16. I fönstret **Lägg till en klienthemlighet** anger du ett namn för hemligheten och anger när den upphör att gälla.

  > [!NOTE]
  > Alla partner som finns i olika miljöer måste förnya hemligheten innan den upphör att gälla.

  > [!IMPORTANT]
  > Kopiera ID:t i fältet **Värde** innan du lämnar den **koncerninterna appen | Sidan Certifikat och hemligheter**. Du behöver den i ett senare steg och den kommer inte att vara tillgänglig när du lämnar sidan. Klistra till exempel in värdet i en textredigerare.

17. Välj **Översikt** på navigeringsfönster.
18. Kopiera värdet från fältet **App-ID (klient)**. Klistra till exempel in värdet i en textredigerare.
19. Välj åtgärden **Slutpunkter** och kopiera sedan värdet i fältet **OAuth 2.0 tokenslutpunkt (v2)**. Klistra till exempel in värdet i en textredigerare.
20. Kopiera värdet från fältet **Katalog-ID (klientorganisation)**. Klistra till exempel in värdet i en textredigerare.
21. I det tokenvärde som du kopierade ersätter **organisationer** med det värde som du kopierade från fältet **Katalog-ID (klientorganisation)** i föregående steg.

#### Lägg till och aktivera din registrerade app i Business Central

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Microsoft Entra appkort** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Markera **Statusen** i fältet **Aktiverad** . 
4. Välj åtgärden **Bevilja samtycke**. 
5. I fältet **Behörighetsgrupp** väljer du behörighetsgrupp **D365 KONCERNINTERN CE OCH DATAÅTKOMST IC CE**.

## Ställa in den koncerninterna kontoplanen

Alla partner måste använda samma koncerninterna kontoplan och koppla kontona till den egna kontoplanen. Om ditt företags kontoplan definierar den koncerninterna kontoplanen för partnerföretagen följer du instruktionerna i det här avsnittet.

Om du använder en XML-fil som innehåller den koncerninterna kontoplanen följer du stegen i [Importera eller exportera en koncernintern kontoplan](intercompany-how-setup.md#import-or-export-an-intercompany-chart-of-accounts).  

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **koncernintern inställning** och väljer sedan relaterad länk.
2. Välj åtgärden **Koncernintern kontoplannkontoplan**.
3. För att lägga till konton, gör något av följande på **Koncernintern kontoplan**:
    * Välj **Nytt** och ange sedan varje konto på en rad på sidan.  
    * Om den koncerninterna kontoplanen ska vara identisk med eller likna den vanliga kontoplanen kan du fylla i sidan automatiskt genom att välja åtgärden **Kopiera från kontoplan**. Du kan redigera de nya raderna efter behov.
    * Om du har skapat en koncernintern kontoplan för en synkroniseringspartner, använd åtgärden **Synkroniseringsinställningar** för att kopiera dessa konton.

    > [!TIP]
    > Om du kopierar den koncerninterna kontoplanen från en synkroniseringspartner kan du med hjälp av åtgärden för **synkroniseringsinställning** uppdatera dina koncerninterna konton med eventuella ändringar som partnern gör.

Nästa steg är att koppla din kontoplan till den koncerninterna kontoplanen. Läs mer på [Koppla den koncerninterna kontoplanen till ditt företags kontoplan](#map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts).

### Importera eller exportera en koncernintern kontoplan

Synkroniseringsföretaget kan dela sin kontoplan med partner genom att exportera den till en fil. Partner kan importera filen för att hämta kontoplanen.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **koncernintern inställning** och väljer sedan relaterad länk.
2. Välj åtgärden **Koncernintern kontoplannkontoplan**.
3. På sidan **Koncernintern kontoplan** väljer du åtgärden **Importera/exportera** och väljer sedan antingen **Importera** eller **Exportera**.
4. Välj filen du vill importera eller exportera.  

Sidan **Koncernintern kontoplan** fylls i med en ny eller redigerad redovisningskontorad enligt den koncerninterna kontoplanen i filen. Alla befintliga, ej relaterade rader på sidan ändras inte.

## Koppla du den koncerninterna kontoplanen till företagets kontoplan  

När du har definierat eller importerat den koncerninterna kontoplanen kopplar du varje koncerninternt konto till ett av dina konton. På sidan **Koncernintern kontoplan** anger du hur de koncerninterna redovisningskontona i inkommande transaktioner ska kopplas till redovisningskonton från företagets kontoplan.

Om de koncerninterna kontona och dina konton har samma nummer kan du koppla kontona automatiskt.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **koncernintern inställning** och väljer sedan relaterad länk.  
2. Välj åtgärden **Koncernintern kontoplannkontoplan**.

    > [!TIP]
    > Om du vill komma åt åtgärderna på sidan kan du behöva expandera sidan till den breda layoutvyn.

3. På sidan **Koncernintern kontoplan** kan du välja åtgärden **Mappning av kontoplan**.
4. Du kan koppla kontona manuellt eller automatiskt.

    * Om du vill skapa mappningen manuellt väljer du ett konto i rutorna **Koncernintern kontoplan** och **Kontoplan för redovisning** och väljer sedan ett konto i **Redovisningsnummer.** och **Koncerninternt nummer.** .
    * För att automatiskt koppla konton som har samma nummer, välj de rader som du vill koppla, välj åtgärden **Koppla till konto med samma nummer** och välj sedan den kontoplan du vill uppdatera.

    > [!TIP]
    > Om du vill koppla många eller kanske alla konton, välj en rad, välj :::image type="icon" source="media/show-more-options-icon.png" border="false"::: och välj sedan **Välj fler**.

## Ställ in koncerninterna dimensioner

Om dina partner vill kunna utbyta transaktioner med tillhörande dimensioner måste ni komma överens om de dimensioner som ni alla kommer att använda. Synkroniseringsföretaget kan till exempel skapa en förenklad version av sina dimensioner, exportera dem till en XML-fil och sedan distribuera filen till varje partner. Varje partner kan importera XML-filen på sidan **koncerninterna dimensioner**  och sedan koppla de koncerninterna dimensionerna till deras dimensioner. Läs mer på [Koppla koncerninterna dimensioner till företagets dimensioner](#map-intercompany-dimensions-to-your-companys-dimensions).

> [!NOTE]
> Varje företag måste koppla sina dimensioner till de koncerninterna dimensionerna för utgående dokument och inkommande dokument. Det är viktigt att koppla konton i båda riktningarna och på så sätt upprätthålla enhetligheten mellan företagen.

Om partner använder den koncerninterna dimensionens synkroniseringspartner följer du instruktionerna i det här avsnittet. Om du vill dela med en XML-fil som innehåller de koncerninterna dimensionerna följer du stegen i [Importera eller exportera koncerninterna dimensioner](#import-or-export-intercompany-dimensions).

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **koncernintern inställning** och väljer sedan relaterad länk.  
2. Välj åtgärden **Koncerninterndimensioner**.
3. För att lägga till dimensioner, gör något av följande på **Koncerninterna dimensioner**:
    * Välj **ny** och ange varje dimension på en rad.  
    * Om de koncerninterna dimensionerna ska vara identisk med eller likna de vanliga dimensionerna kan du fylla i sidan automatiskt genom att välja åtgärden **Kopiera från dimensioner**. Sedan kan du redigera raderna efter behov.
    * Om du har specificerat koncerninterna dimensioner för en synkroniseringspartner, använd åtgärden **Synkroniseringsinställningar** för att kopiera dessa dimensioner.

    > [!TIP]
    > Om du kopierar de koncerninterna dimensionerna från en synkroniseringspartner kan du med hjälp av åtgärden för **synkroniseringsinställning** uppdatera dina koncerninterna dimensioner med eventuella ändringar som partnern gör.  

### Importera eller exportera koncerninterna dimensioner  

Synkroniseringsföretaget kan dela sina dimensioner med partner genom att exportera dem till en fil. Partner kan importera filen för att hämta dimensioner.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **koncernintern inställning** och väljer sedan relaterad länk.
2. Välj åtgärden **Koncerninterndimensioner**.  
3. På sidan **Koncerninterna dimensioner** väljer du åtgärden **Importera/exportera** och väljer sedan antingen **Importera** eller **Exportera**.
4. Välj filen du vill importera eller exportera.

Nästa steg är att koppla dimensionerna med de intercompany-dimensionerna. Läs mer på [Koppla koncerninterna dimensioner till företagets dimensioner](#map-intercompany-dimensions-to-your-companys-dimensions).

### Koppla koncerninterna dimensioner till företagets dimensioner

När du har angett de dimensioner du ska använda kopplar du varje koncernintern dimension med en av ditt företags dimensioner och vice versa. Använd sidan **Koppla koncerninterna dimensioner** för att ange kopplingen. Upprepa därefter proceduren för dimensionsvärdena.

* Ange hur koncerninterna dimensioner i inkommande transaktioner ska kopplas till dimensioner från företagets lista över dimensioner.
* Ange hur dina dimensioner ska översättas till koncerninterna dimensioner i *utgående transaktioner*.

Om några av de koncerninterna dimensionerna har samma koder som motsvarande dimensioner i företaget kan du koppla dimensionerna automatiskt.  

I följande steg mappar du först koncerninterna dimensioner till dimensioner för inkommande dokument i rutan **Koncerninterna dimensioner**. Därefter mappar du dimensioner till koncerninterna dimensioner för utgående dokument på sidan **Aktuella företagsdimensioner**.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **koncernintern inställning** och väljer sedan relaterad länk.
2. Välj åtgärden **Koncerninterndimensioner**.
3. På sidan **Koncerninterna dimensioner** kan du välja åtgärden **Koppla dimensioner**.
4. Du kan koppla dimensionerna manuellt eller automatiskt.

    * För att manuellt skapa kopplingen välj dimension i rutorna **Koncerninterna dimensioner** och **Aktuella företagsdimensioner** och välj sedan en dimension i fälten **Dimensionskod** och **Koncernintern dimensionskod**.
    * För att automatiskt koppla dimensioner som har samma kod, välj de rader som du vill koppla, välj åtgärden **Koppla dimensioner med samma kod** och väljer sedan de dimensioner du vill uppdatera. 

    > [!TIP]
    > Om du vill mappa många eller kanske alla dimensioner, välj en rad, välj :::image type="icon" source="media/show-more-options-icon.png" border="false"::: och välj sedan **Välj fler**.

5. Välj åtgärden **Mappning av dimensionsvärden**.
6. På sidan **Mappning av koncerninterna dimensionsvärden** liknar stegen för att skapa mappningen liknar det du precis gjorde för dimensioner.

## Ställ in koncerninterna journalmallar och journaler

Du måste skapa en redovisningsjournalmall och en redovisningsjournal som ska användas som standard för koncerninterna transaktioner. Mallen och journalen är särskilt viktiga om du accepterar koncerninterna transaktioner från partner automatiskt. Om du vill veta mer om automatiskt godtagna transaktioner går du till [Automatiskt godtagande av transaktioner från koncerninterna partner](#auto-accept-transactions-from-intercompany-partners).   

* Redovisningsjournaler använder du för att bokföra på redovisningskonton och andra konton, till exempel bank-, kund- och leverantörskonton. När du bokför med en redovisningsjournal skapas alltid transaktioner på redovisningskonton.  Använd sidan för **Koncernintern redovisningsjournal** när du vill ställa in redovisningsjournal som ska användas. Inställningarna som är specifika för koncerninterna transaktioner är de konton du anger i fälten **Konc.int. kontotyp** och **Konc.int. kontonr**.
* Med journalmallar får du en journalsida som är designad för ett specifikt syfte. Detta innebär att de fält som finns i journalmallar är sådana fält som är nödvändiga för en särskild del av programmet. På sidan **Redovisningsjournalmallar** kan du ange en mall som ska användas för koncerninterna transaktioner.

Om du vill veta mer om journalmallar och journaler går du till [Använda journalmallar och journaler](ui-work-general-journals.md#use-journal-templates-and-batches).

## Konfigurera företag för koncerninterna transaktioner

Följande åtgärder förutsätter att en synkroniseringspartner har skapats med kontoplanen och dimensionerna som den koncerninterna kontoplanen och dimensionerna ska baseras på. Du kan ställa in dem själv, men det går oftast snabbare att komma igång och det är enklare att underhålla dem med hjälp av en synkroniseringspartner. Mer information om synkroniseringspartner finns på [Ställa in en synkroniseringspartner](#set-up-a-synchronization-partner).

> [!TIP]
> Det är en bra idé att fylla i fälten på snabbfliken **Allmänt** på sidan **Koncernintern inställning** för varje partner innan du lägger till deras partners. När du lägger till partnerföretag som är i samma klientorganisation får [!INCLUDE [prod_short](includes/prod_short.md)] sin koncerninterna kod och företagsnamn från deras inställningar på snabbfliken Allmänt. Fältet **företagsnamn** kommer att bekräfta att deras koncerninterna kod är unik.

> [!NOTE]
> Om du ska använda en synkroniseringspartner lämnar du fältet **synkroniseringspartner** tomt när du ställer in det företaget för partnerskapet.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **koncernintern inställning** och väljer sedan relaterad länk.  
2. På sidan **Koncernintern inställning** fyller du i fälten på snabbfliken **Allmänt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> I [!INCLUDE[prod_short](includes/prod_short.md)] online kan du inte använda filplats för att överföra transaktioner till dina partners eftersom [!INCLUDE[prod_short](includes/prod_short.md)] inte har åtkomst till ditt lokala nätverk. Om du väljer **Filplats** i fältet **Överföringstyp** kommer fältet **Mappsökväg** inte att vara tillgängligt. Filen kommer istället att laddas ned till mappen **Hämtningar** på din dator. Du kan sedan skicka filen till någon i partnerföretaget, exempelvis via e-post. För en mer direkt process rekommenderar vi att du väljer **E-postmeddelande**.

Nästa steg är att konfigurera partnerföretag.

## Konfigurera koncerninterna partner

Varje partner måste lägga till alla andra företag i partnerskapet som partner.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **koncernintern inställning** och väljer sedan relaterad länk.
2. På snabbfliken **Koncerninterna partner** välj **Lägg till**.
3. På sidan **Koncernintern partner** fyller du i fälten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Upprepa steg 2 och 3 för alla företag i partnerskapet.

> [!NOTE]
> För koncernintern bokföring, när du har aktiverat **Godkänn transaktion automatiskt** på sidan **Koncerninternt partnerkort** undertrycket [!INCLUDE[prod_short](includes/prod_short.md)] varningar om inköpsfakturor som duplicerar den ursprungliga inköpsordern. Det är viktigt att du har en affärsprocedur för att hantera kopior. Du kan t.ex. ta bort sådana inköpsorder när inköpsfakturan inlevereras från den koncerninterna partnern.

### Skapa koncerninterna partner som kunder och leverantörer

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **koncernintern inställning** och väljer sedan relaterad länk.
2. På snabbfliken **Koncerninterna partner** öppnar du kortsidan för partnern.
3. Beroende på vad du vill göra väljer du kunden eller partnern i fältet **Kundnr.** eller fältet **Leverantörsnr.**.

    > [!NOTE]
    > Om kunden eller leverantören inte har skapats kan du välja **+ ny** på menyn för att ställa in dem. Om du vill ha mer information om hur du skapar kunder och leverantörer går du till [Registrera nya kunder](sales-how-register-new-customers.md) och [ Registrera nya leverantörer](purchasing-how-register-new-vendors.md).

    > [!TIP]
    > Du kan också ange en kund eller leverantör som koncernintern partner genom att fylla i fältet **Intern partnerkod** på sidorna **Kundkort** och **Leverantörskort**.

### Ställ in standardredovisningskonton för koncernintern partner  

När du skapar en koncernintern försäljnings- eller inköpsrad som du ska skicka som en utgående transaktion anger du ett konto från den koncerninterna kontoplanen som standard för det konto i partnerns företag som beloppet ska bokföras på. På sidan **Redovisningskontokort**, för konton som du använder regelbundet för utgående koncerninterna försäljnings- eller inköpsrader, kan du ange ett standardredovisningskonto för koncernintern partner. För kundreskontrakonton kan du till exempel ange motsvarande leverantörsreskontrakonton från den koncerninterna kontoplanen. Kontona för kundreskontra och leverantörsreskontra används som motkonto för koncernintern partner när du bokför transaktioner i koncerninterna journaler.  

När du anger ett redovisningskonto i fältet **Balanskontonr** på en koncernintern rad med **Koncernintern partner** i fältet **Kontotyp** fylls fältet **Redov. konto för konc.int. partner**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.  
2. Öppna det redovisningskonto som används för koncerninterna transaktioner och i fältet **Std.kontonr. konc.int. part.** anger du det koncerninterna redovisningskonto som partnern ska bokföra på när du bokför till redovisningskontot på den raden.
3. Upprepa steg 2 för varje konto som du ofta anger i fältet **Balanskontonr** på en rad i en koncernintern journal eller i ett koncerninternt dokument.

### Acceptera transaktioner automatiskt från koncerninterna partner

För att göra det snabbare att behandla koncerninterna transaktioner kan du ange att du automatiskt vill skapa journalrader baserat på en koncernintern partner bokförs från **Konc.int. redovisningsjournal**. Om du vill skapa inkommande och utgående transaktioner automatiskt måste du aktivera följande växlingar för varje partner:

* På sidan **Koncernintern inställning** aktivera växlingen **Automatiskt skicka transaktioner** för synkroniseringspartner. Ange sedan var mottagna koncerninterna journaltransaktioner ska skapas genom att fylla i fälten **Standardvärde för koncernintern redovisningsjournalmall** och **Standardvärde för koncernintern redovisningsjournal**.

    > [!TIP]
    > Om fältet **Standardvärde för koncernintern redovisningsjournalmall** är tomt måste du skapa en allmän journalmall som ska användas för dina koncerninterna redovisningsjournaler. Om du vill veta mer om mallar och journaler går du till [Ställ in koncerninterna journalmallar och journaler](#set-up-intercompany-general-journal-templates-and-batches)    

* På sidan **Koncernintern partner** aktiverar du växlingen **Acceptera transaktioner automatiskt**.

Journalraderna skapas åt dig, men bokförs inte.

> [!NOTE]
> Om ditt företag har använt koncerninterna funktioner i [!INCLUDE [prod_short](includes/prod_short.md)] före 2022 utgivningscykel 1, för att automatiskt acceptera transaktioner måste din administratör aktivera funktionen **Acceptera automatiskt koncerninterna transaktioner i redovisningsjournalen** till sidan **Funktionshantering**.

### Ange vilka bankkonton som ska användas för koncerninterna partner

För att underlätta snabba betalningar måste du ange ett eller flera bankkonton som ska användas för koncerninterna partner. När en partner använder en koncernintern journal för att göra en betalning, kan de ange bankkontot på raden. Bankkontot används som motkonto i det mottagande företaget som minimerar behovet av att manuellt registrera transaktioner.

* Om du vill ange vilket bankkonto som ska användas väljer du på sidan **koncernintern partner** åtgärden **Bankkonton**. På **Koncerninternt bankkontokort**, ange kontoinformation.

## Felsöka koncernintern inställning

På sidan **Koncernintern inställning**, i rutan **Diagnostik för koncerninterna inställningar** innehåller paneler som indikerar om du har ställt in alla komponenter som behövs för att utbyta koncerninterna transaktioner. Rutorna finns också i rollcentret för chef. Välj panelerna för att ta reda på vad som saknas. En översikt över de nödvändiga komponenterna finns i [Översikt över stegen för att komma igång](#overview-of-the-steps-to-get-started).

## Se även

[Hantera koncerninterna transaktioner](intercompany-manage.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
