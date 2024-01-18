---
title: Konfigurera OneDrive-integration med Business Central lokalt
description: Lär dig mer om hur du ställer in Business Central lokalt för att integrera med OneDrive för företag.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 12/12/2023
ms.author: jswymer
---
# Konfigurera OneDrive-integration med Business Central lokalt

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

I den här artikeln beskrivs hur du konfigurerar OneDrive-integration med Business Central lokalt. Till skillnad från [!INCLUDE[prod_short](includes/prod_short.md)] online ställs kopplingen mellan Business Central och OneDrive för företag inte in automatiskt. Om anslutningen inte är konfigurerad kan användarna inte använda funktionerna OneDrive.

Det finns två aktiviteter som måste utföras för att konfigurera OneDrive-integrationen.

- Den första uppgiften innebär att registrera ett program (app) på din Microsoft Entra-klientorganisation för din Microsoft 365-plan. Den registrerade appen används för autentisering. Den här uppgiften utförs vanligtvis i Azure-portalen och i Business Central-webbklienten.
- Den andra uppgiften innebär att konfigurera anslutningen till OneDrive-URL-adressen och att aktivera OneDrive-funktionerna i Business Central. Den här uppgiften utförs i Business Central-webbklienten. Det görs annorlunda för version 21 än för versionerna 19 och 20. Version 21 introducerar en ny **OneDrive-konfiguration** som ersätter **SharePoint-anslutningskonfigurationen**.  

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan endast kopplas till OneDrive som finns i Microsoft i molnet. Anslutning till [!INCLUDE[prod_short](includes/prod_short.md)] lokalt till lagringsplatsen mina webbplatser för SharePoint server stöds inte.

## <a name="registerapp"></a>Registrera ett program i Microsoft Entra ID för OneDrive-integrering

I den här uppgiften lägger du till en registrerad app för Business Central i din Microsoft Entra-klientorganisation för ditt Microsoft 365-abonnemang. Precis som andra Azure-tjänster som arbetar med Business Central kräver OneDrive ett registrerat program i Microsoft Entra ID. Den registrerade appen tillhandahåller autentisering och autentiseringstjänster mellan Business Central och SharePoint som används av OneDrive.

Detaljerad information om hur du slutför det här steget finns i [Registrera ett program i Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) i hjälpen för utvecklare och proffs.

När du registrerar programmet bör du tänka på följande:

- Om du redan har registrerat ett program som en del av en integration med en annan Microsoft-produkt, till exempel Power BI, kan du återanvända den registrerade appen. Om så är fallet behöver du bara ange SharePoint-behörigheterna för den befintliga registrerade appen.

- Se till att konfigurera den registrerade appen med följande delegerade behörigheter till SharePoint API:

    - AllSites.FullControl
    - User.ReadWrite.All
    
    För Business Central 2021utgivningscykel 2 (version 19) anger du dessa behörigheter istället:
    
    - AllSites.Write
    - MyFiles.Write
    - User.Read.All 

- Om du använder Business Central version 19 eller 20 kopierar **Program-ID (klient)** och **klienthemligheten** som används av den registrerade appen. Du behöver informationen i nästa uppgift.

## <a name="url"></a>Hämta din OneDrive-URL

[!INCLUDE[onedrive-url](includes/onedrive-url.md)]

## Konfigurera OneDrive-anslutningen i version 21 och senare

Använd den här proceduren om du använder Business Central 2022, utgivningscykel 2 (version 21) eller senare.

### Förutsättningar

- Indirekt, ändra och ta bort (imd) behörighet i tabellen **Dokumentservicescenario** som minimum

### Kör OneDrive-konfiguration

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger **OneDrive-konfiguration** och välj sedan relaterad länk.
2. Första gången du kör assisterad konfiguration kan du se **Din integritet**. Läs informationen på sidan och om du godkänner villkoren väljer du **Godkänn** för att fortsätta.
3. På sidan **Konfigurera filhantering** har du följande alternativ att välja bland:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

4. På sidan **Konfigurera Business Central** anger du OneDrives URL i fältet **OneDrive-URL**.

   [Hur gör jag för att hitta URL:en till OneDrive?](#url)
5. Välj **Testanslutning** och vänta på resultaten.
   - Om testet lyckas väljer du **Klart** och sedan är du klar att sätta igång.
   - Om testet misslyckas får du ett meddelande som beskriver problemet. Oftast har problemet med den angivna URL:en att göra. Välj **OK** för att gå tillbaka till sidan **Konfigurera Business Central**, kontrollera URL:en och försök igen.
   - Om du inte redan har konfigurerat det Microsoft Entra ID-registrerade programmet öppnas guiden för **Konfigurera Microsoft Entra ID**.
6. När det är slutfört accepteras sekretessmeddelandet för OneDrive-integration för alla användare. Om du vill ändra det så att användarna måste acceptera eller avböja själva, går du till sidan **Sekretessmeddelandestatus** och väljer **Låt användaren bestämma** för OneDrive-integrationen. Användare kommer då att uppmanas att godkänna eller avböja sekretessmeddelandet första gången de använder OneDrive-funktionerna. Mer information finns i [Sekretessmeddelanden](privacy-notices-status.md).

## Konfigurera anslutningen i [!INCLUDE[prod_short](includes/prod_short.md)] version 19 och 20

Använd den här proceduren om du använder Business Central 2022, utgivningscykel 1 (version 20), eller 2021, utgivningscykel 2 (version 19).
> [!IMPORTANT]
> Genom att konfigurera den här funktionen kan du också aktivera äldre funktioner som skickar filer till OneDrive.  
>
>* Excel-filen kopieras automatiskt till funktionen öppna i Excel till OneDrive och sedan öppnas den i Excel Online. 
>* När du exporterar en rapport till en fil kopieras filen automatiskt till OneDrive och sedan öppnas den i Excel Online, Word Online eller OneDrive. 
>* Andra funktioner kan också öppnas automatiskt i OneDrive.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Microsoft SharePoint Konfiguration av inställningen** och väljer sedan relaterad länk.
2. I fältet **Beskrivning** anger du en beskrivning för anslutningen som **OneDrive**.
3. I fältet **Mapp** anger du **Business Central**.
4. I fältet **Plats** anger du URL för din OneDrive.

   [Hur gör jag för att hitta URL:en till OneDrive?](#url)
5. I fältet **Klient-ID** anger du klient-ID från den registrerade appen.
6. I fältet **Klienthemlighet** anger du hemligheten från den registrerade appen. 

> [!IMPORTANT]
> Sidan **SharePoint-anslutningskonfiguration** används för att konfigurera flera äldre funktioner. I avsnittet **Allmänt** konfigureras anslutningen till OneDrive och avsnittet **Delade dokument** dirigerar om filer till SharePoint i stället. **SharePoint-anslutningskonfiguration** är inaktuell och kommer att tas bort i kommande versioner. Vi rekommenderar att du inte konfigurerar avsnittet **delade dokument**. Mer information finns i [Föråldrade funktioner i basappen ](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup).

## Efter uppgradering till version 21

När du uppgraderar till version 21 eller senare kommer den befintliga anslutningen till OneDrive som konfigurerats på sidan **SharePoint-anslutningskonfiguration** fortfarande att fungera. Men eftersom sidan **SharePoint-anslutningskonfiguration** kommer att tas bort i version 23, rekommenderar vi att du växlar till den nya OneDrive-integrationen, enligt beskrivningen i nästa avsnitt. Om du gör detta byte nu blir det enklare när **SharePoint-anslutningskonfigurationen** tas bort. Dessutom kan du använda guiden för assisterad konfiguration **OneDrive-konfiguration** för att hantera de OneDrive-funktioner som är tillgängliga för användarna.

## Växla från äldre SharePoint till ny OneDrive-integration 

Om du vill växla till den nya OneDrive-integrationen kör du guiden för assisterad konfiguration **OneDrive-konfiguration**, som du kan öppna direkt eller från den äldre sidan **SharePoint-anslutningskonfiguration**. Den assisterade konfigurationen **OneDrive-konfiguration** leder dig genom övergången och ger information om förändringarna längs vägen.

Innan du sätter igång med bytet eller när du gör det, ska du läsa nästa avsnitt för att lära dig mer om vissa aspekter och överväganden i processen. 

### <a name="onedrivesetupmigration"></a>Om att växla till den nya OneDrive-integrationen

Utöver OneDrive-integration kan Business Central också integreras med andra tjänster, t.ex Power BI och Universell utskrift. Integrering med dessa andra tjänster kräver också en registrerad Microsoft Entra-app för autentisering. Microsoft Entra-appen som används av dessa tjänster konfigureras i den assisterade konfigurationen **Konfigurera dina Microsoft Entra-konton**. När du växlar från den äldre SharePoint-anslutningskonfigurationen ändrar den assisterade konfigurationen **OneDrive-konfiguration** din OneDrive-integration så att den också använder den assisterade konfigurationen **Konfigurera dina Microsoft Entra-konton**&mdash;så att alla integrationer använder samma Microsoft Entra-app.

Den här ändringen har betydelse vid växling till den nya OneDrive-integreringen, beroende på om det redan finns ett Microsoft-program konfigurerat i den assisterade konfigurationen för **Konfigurera dina Microsoft Entra-konton**. 

> [!IMPORTANT]
> När du har växlat till den nya OneDrive-konfigurationen kan du inte längre använda sidan **SharePoint-anslutningskonfiguration** för att konfigurera OneDrive-integrationen.

#### Så påverkar ändringarna integrationen

Den assisterade konfigurationen **OneDrive-konfiguration** använder alltid appen som har konfigurerats i den assisterade konfigurationen **Konfigurera dina Microsoft Entra-konton**, om sådan finns. När du kör den assisterade konfigurationen **OneDrive-konfiguration** jämför den appen som har konfigurerats i **Konfigurera dina Microsoft Entra-konton** med den app som har konfigurerats i **SharePoint-anslutningskonfiguration**.

> [!TIP]
> På sidan **SharePoint-anslutningskonfiguration** och i den assisterade konfigurationen **Konfigurera dina Microsoft Entra-konton** identifieras Microsoft Entra-appen genom **klient-ID**.

- Om appen i **Konfigurera dina Microsoft Entra-konton** skiljer sig från appen i **SharePoint-anslutningskonfiguration** ändras OneDrive-integrationen så att den använder appen i **Konfigurera dina Microsoft Entra-konton**.

   Vid **OneDrive-konfigurationen** medan du gör bytet visas ett meddelande som ser ut ungefär så här: 

  `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This means the client id will change to NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN, you may want to test it has the correct permissions.`

  `NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN` representerar klient-ID för appen i **Konfigurera dina Microsoft Entra-konton** som OneDrive-integrationen har växlats till. 

  > [!IMPORTANT]
  > Om ny OneDrive-integration ska fungera efter att du har gjort bytet måste du ge appen behörighet till SharePoint API i Azure Portal. Du kan göra detta steg innan eller efter du växlar till den nya OneDrive-konfigurationen. Mer information finns i avsnittet [Registrera ett program i Microsoft Entra ID för OneDrive-integrering](#registerapp).

- Om appen i **Konfigurera dina Microsoft Entra-konton** är densamma som appen i **SharePoint-anslutningskonfiguration**, använder OneDrive-integrationen samma app som förut, förutom från konfigurationen i **Konfigurera dina Microsoft Entra-konton**.

   Vid **OneDrive-konfigurationen** medan du gör bytet visas ett meddelande som ser ut ungefär så här:

    `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This has already been configured with the same client id (5F78CADE-19C0-49BF-AF84-306D0579B50E).`

- Om ingen app har konfigurerats i **Konfigurera dina Microsoft Entra-konton** använder OneDrive-integrationen samma app som förut.

   Den assisterade konfigurationen **OneDrive-konfiguration** kopierar appkonfigurationen till **Konfigurera dina Microsoft Entra-konton**, så att den används för andra integrationer som kan göras senare.

   Vid **OneDrive-konfigurationen** medan du gör bytet visas ett meddelande som ser ut ungefär så här:

   `The Microsoft Entra application used for authentication will be configured for all Business Central integrations`.

### Kör OneDrive-konfigurationen för att växla till den nya OneDrive-integrationen

1. Öppna antingen sidan **OneDrive-konfiguration** eller sidan **SharePoint-anslutningskonfiguration**.
2. Om du använder sidan **SharePoint-anslutningskonfiguration** väljer du **Gå till ny OneDrive-konfiguration** i meddelandet längst upp på sidan.
3. Följ guiden för assisterad konfiguration **OneDrive-konfiguration**.
4. När du kommer till sidan **Konfigurera filhantering** väljer du ett av följande alternativ för att aktivera funktioner:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

5. På sidan **Konfigurera Business Central** visas samma URL som används av den befintliga OneDrive-integrationen. Du kan ändra URL vid behov.
6. Välj **Testanslutning** och följ instruktionerna.

   Om testet lyckas väljer du **Klart** och sedan är du klar att sätta igång. Annars kan du lösa problemet med hjälp av meddelandena på sidan.

## Se även
[Business Central och OneDrive för företag-integration](across-onedrive-overview.md)  
[Öppna Business Central-filer i OneDrive](across-share-onedrive.md)  
[OneDrive Vanliga frågor och svar](admin-onedrive-faq.md)

