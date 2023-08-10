---
title: Vanliga frågor och Svar om Teams
description: Få svar på några vanliga frågor om att arbeta med Teams och Business Central.
author: jswymer
ms.author: jswymer
ms.topic: faq
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors'
ms.date: 09/28/2022
ms.custom: bap-template
---
# <a name="teams-faq"></a>Vanliga frågor och Svar om Teams

[!INCLUDE [online_only](includes/online_only.md)]

I den här artikeln besvaras några frågor som du kanske har kring arbetet med Microsoft Teams och [!INCLUDE [prod_short](includes/prod_short.md)].

## [Allmänt](#tab/general)

### <a name="how-do-i-sign-in-to-the--app-in-teams"></a>Hur loggar jag in i appen [!INCLUDE [prod_short.md](includes/prod_short.md)] i Teams?

När du har installerat appen blir du ombedd att logga in första gången du använder den när du klistrar in en [!INCLUDE [prod_short.md](includes/prod_short.md)]-länk i chattfunktionen i Teams eller när du väljer åtgärden **Detaljerad information** i Teams. Beroende på Teams-klient måste du kanske ange din behörighet för att komma åt [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="how-do-i-sign-out-of-the--app-in-teams"></a>Hur loggar jag ut från appen [!INCLUDE [prod_short.md](includes/prod_short.md)] i Teams?

Om du vill logga ut från identiteten i Teams som du använde för att ansluta till [!INCLUDE [prod_short.md](includes/prod_short.md)] går du till valfri chattdialogruta och högerklickar på ikonen [!INCLUDE [prod_short.md](includes/prod_short.md)] under denna. Välj sedan **Inställningar**. När fönstret visas kontrollerar du den aktuella inloggade identiteten och väljer sedan **Logga ut**.

### <a name="does-the-app-for-teams-connect-to--on-premises"></a>Ansluter appen för Teams till [!INCLUDE [prod_short.md](includes/prod_short.md)] lokalt?

Nr. [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams fungerar endast med [!INCLUDE [prod_short.md](includes/prod_short.md)] online. Det finns inga planer på att stödja [!INCLUDE [prod_short.md](includes/prod_short.md)]-distributionstyper &mdash;t.ex. lokalt, hybridmoln eller privatmoln&mdash;som inte Microsoft är värd för eller hanterar direkt.

### <a name="does-the-app-work-with-multiple-companies-and-environments"></a>Fungerar appen med flera företag och miljöer?

Ja. Om du vill söka efter kontakter i ett annat företag, gå till [Inställningar](across-teams-settings.md). När [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen expanderar en länk till ett kort måste länken innehålla miljö- och företagsnamn för att appen ska matcha posten i rätt företag. Du kan klistra in länkar till alla företag och miljöer som du har till gång till inom din organisation samt från det [!INCLUDE [prod_short.md](includes/prod_short.md)]-konto som du använde när du loggade in. Deltagarna i chatten kan se kortet. De kan emellertid inte se kortinformationen om de inte har behörighet till det företag eller den miljö där posten lagras.

### <a name="in-which-countries-or-regions-is-the--app-available"></a>I vilka länder eller regioner finns [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen tillgänglig?

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams begränsas inte av land eller region. Appen finns tillgänglig på alla marknader som för närvarande stöds av Teams-marknaden. 

### <a name="does-the--app-work-with-any-localization-of-include-prod_shortmd"></a>Fungerar [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen med valfri lokalisering av [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Ja. Appen är avsedd att användas vid valfri lokalisering av [!INCLUDE [prod_short.md](includes/prod_short.md)], oavsett om lokaliseringen erbjuds direkt från Microsoft eller via en partner. Läs mer på [Tillgänglighet för land/region och språk som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="which-languages-does-the--app-support"></a><a name="language"></a>Vilka språk stöder [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen?

Två saker avgör vilket språk som används för kort och kortinformation i Teams:

1. Ditt språk i Teams, som du kan se i bland dina kontoinställningar i Teams. 
2. Ditt språk i [!INCLUDE [prod_short.md](includes/prod_short.md)], som du kan se i [!INCLUDE [prod_short.md](includes/prod_short.md)]-webb klienten (se [Ändra grundläggande inställning – Språk](ui-change-basic-settings.md#language)).

I följande tabell förklaras hur upplevelsen skiljer sig åt för meddelandeförfattare och -mottagare, beroende på språkinställningar och språktillgänglighet.

|Vem|Kort|Kortinformation |
|-|----|--------------| 
|Meddelandeförfattare |Visar på det språk som har angetts för dig i Teams. Om [!INCLUDE [prod_short.md](includes/prod_short.md)] inte erbjuder samma språk visas kortet på engelska. |Visas på det språk som har angetts för dig i [!INCLUDE [prod_short.md](includes/prod_short.md)], vilket kan omfatta språk från språkprogram som tillhandahålls av partner. |
|Meddelandemottagare |Visas på meddelandets upphovspersons språk. |Visas på det språk som angetts för dig i [!INCLUDE [prod_short.md](includes/prod_short.md)]. |

Listan över språk som stöds för [!INCLUDE [prod_short.md](includes/prod_short.md)] finns i [Språk som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### <a name="does-the--app-work-with-industry-solutions"></a>Fungerar [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen med branschlösningar?

Ja. Men endast vissa funktioner i appen fungerar med [Inbäddade appar](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview):

- Appen fungerar med länkar baserade på det **\*.bc.dynamics.com**-mönster som vanligtvis används med inbäddade appar.
- Kontaktsökning är inte tillgänglig för inbäddade appar som ersätter basprogrammet från Microsoft.

### <a name="does--work-with-the-teams-mobile-app"></a>Fungerar [!INCLUDE [prod_short.md](includes/prod_short.md)] med mobilappen för Teams?

Ja. [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen kan installeras från den stationära Teams-appen eller webbläsaren, eller av en administratör för alla användare. När den är installerad är appen [!INCLUDE [prod_short.md](includes/prod_short.md)] automatiskt tillgängligt i Teams för iOS och Android. På mobila enheter kan du endast visa kort som har skickats av andra, få åtkomst till information, eller utnyttja kortet till [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappens fulla utsträckning. Du kan emellertid inte klistra in länkar som expanderas till kort när du skriver meddelanden eller söker efter kontakter. Läs mer om minimikrav för mobila enheter på [Minimikrav för att använda Business Central](product-requirements.md).

### <a name="is-the--app-for-teams-the-same-as-the-include-prod_shortmd-app-for-ios-and-android"></a>Är appen [!INCLUDE [prod_short.md](includes/prod_short.md)] för Teams samma som appen [!INCLUDE [prod_short.md](includes/prod_short.md)] för iOS och Android?

Nr. Appen för Teams är ett tillägg till Microsoft Teams och uteslutande utformat för samarbeten i Teams. Alternativt levererar [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen en rik upplevelse för att arbeta med [!INCLUDE [prod_short.md](includes/prod_short.md)]-data på dina mobila enheter.

Mobila användare uppmuntras att installera både mobilappen och appen För Teams i syfte att få ut maximalt av [!INCLUDE [prod_short.md](includes/prod_short.md)]. Med båda appar installerade kan du välja åtgärden **Öppna** på ett kort i Teams för att visa kortinformationen i [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen. Du kan läsa mer om hur du installerar mobilapparna för [!INCLUDE [prod_short.md](includes/prod_short.md)] och Teams i:

- [Skaffa Business Central på din mobila enhet](install-mobile-app.md)
- [Hämta mobilappen för Teams](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) från Microsofts support

### <a name="does-the--app-work-in-all-teams-clients"></a>Fungerar [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i alla Teams-klienter?

Nr. [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams stöds inte när den installeras som ett paket för macOS eller Linux. På dessa plattformar använder du Teams via webbläsare som stöds.

För minimikrav för [!INCLUDE [prod_short.md](includes/prod_short.md)] se [Minimikrav för att använda Business Central](product-requirements.md#teams).

Du kan läsa mer om val av Teams-klienter och hur du installerar dem i [Skaffa klienter för Microsoft Teams](/microsoftteams/get-clients) i Teams-dokumentationen.

### <a name="which-teams-client-is-best-for-"></a>Vilken Teams-klient passar bäst för [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Det finns endast smärre skillnader och begränsningar mellan Teams-klienter som kan påverka din upplevelse av [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams. När du väljer en Teams-klient bör du tänka på följande:

- Det går inte att komma åt kameran och platsen från informationsfönstret i den stationära Teams-appen.
- Det går inte att aktivera telefonnummer från informationsfönstret i Teams för iOS, Android eller i webbläsaren.
- Med hjälp av Microsoft Edge och Teams i webbläsaren kan du enkelt arbeta över flera olika identiteter och konton genom att logga in på Teams från olika profiler. Mer information om hur du använder profiler i Microsoft Edge finns i [Logga in och skapa flera profiler i Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) på Microsoft Support.

### <a name="what-is-the-best-way-for-me-to-demonstrate--and-microsoft-teams-to-prospective-customers"></a>Vilket är det bästa sättet att demonstrera [!INCLUDE [prod_short.md](includes/prod_short.md)] och Microsoft Teams för potentiella kunder?

Om du är en återförsäljarpartner kanske du vill ha en miljö som du kan visa potentiella kunder som en del av demonstrationerna i samband med förförsäljning. För att undvika att påverka Microsoft Teams inom din organisation kan du skaffa ett Microsoft 365-demokonto på [https://aka.ms/CDX](https://aka.ms/CDX). Det här kontot ger dig full kontroll över en oberoende Azure-organisation som innehåller Microsoft Teams och [!INCLUDE [prod_short.md](includes/prod_short.md)]. Läs mer på [Förbereda demonstrationsmiljöer av Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### <a name="does-the--app-for-teams-cater-to-my-customization-and-personalization"></a>Uppfyller [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams mina anpassningsbehov?

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams kan visa kort för länkar till kundsidor och -tabeller i [!INCLUDE [prod_short.md](includes/prod_short.md)], till exempel de sidor och tabeller som kommer från egna anpassade tillägg eller från AppSource.

Fälten som visas på ett kort i Teams kan också påverkas av [!INCLUDE [prod_short.md](includes/prod_short.md)]-anpassningar som har installerats för organisationen. Korten beaktar inga rollspecifika anpassningar eller användaranpassningar. I fönstret för kortinformation visas detaljerad information på samma sätt som när du ser den i [!INCLUDE [prod_short.md](includes/prod_short.md)], inklusive tillägg, rollanpassningar och användaranpassningar.

När du söker efter kontakter påverkas inte de fält som är matchade i tabellen **Kontakter** och de fält som visas i sökresultaten påverkas inte av någon anpassning.

### <a name="how-do-the-permissions-required-by-the-app-affect-my-privacy"></a>Hur påverkar de behörigheter som krävs av appen min integritet?

Innan du installerar [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams kan du granska de minsta behörigheter som krävs för att appen ska fungera. Genom att installera appen ger du appen behörighet att ta emot meddelanden och data som du tillhandahåller den, och du ger Teams behörighet att lagra och bearbeta dessa meddelanden.

Vissa [!INCLUDE [prod_short.md](includes/prod_short.md)]-funktioner kräver också att du öppnar externa länkar eller använder åtkomst till din kamera eller geografiska plats. Anta att du vill ta ett foto av en inköpsfaktura för bearbetning. Appen [!INCLUDE [prod_short.md](includes/prod_short.md)] använder inte dessa funktioner utan ditt medgivande, och de används bara av specifika funktioner i fönstret **Information**. När du använder någon av dessa funktioner för första gången visar Teams en dialogruta där du ombeds bevilja åtkomst till de enhetsfunktioner som krävs.

- På Teams-skrivbordet granskar och justerar du appbehörigheter från fönstret **Inställningar**. Välj din profilbild högst upp i appen, välj **Inställningar** > **Behörigheter** och sedan [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen.

- För Teams i webbläsaren och Teams för iOS eller Android kan du granska eller justera behörigheter från din webbläsare eller enhetsinställningar.

> [!NOTE]
> Exakt vilka [!INCLUDE [prod_short.md](includes/prod_short.md)]-funktioner som ber dig om behörigheter beror på vilka tilläggsappar och anpassningar som tillämpas på den [!INCLUDE [prod_short.md](includes/prod_short.md)]-miljö som du ansluter till.

### <a name="where-can-i-learn-about-my-privacy"></a>Var kan jag få veta mer om min sekretess?

Du kan lära dig hur Microsoft hanterar dina uppgifter i [Microsofts sekretesspolicy](https://go.microsoft.com/fwlink/?linkid=2030602). 

Kontakta administratören för information om hur din organisation hanterar sekretessen för dina data.

### <a name="how-do-i-uninstall-the--app-for-teams"></a>Hur avinstallerar jag [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams?

Om du vill ta bort appen som du har installerat åt dig själv går du till valfri chattdialogruta, letar upp [!INCLUDE [prod_short.md](includes/prod_short.md)]-ikonen därunder, högerklickar på ikonen och väljer **Avinstallera**.  

### <a name="will-microsoft-continue-to-improve-the--app-for-teams"></a>Kommer Microsoft att fortsätta att förbättra [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams?

På Microsoft lyssnar vi ständigt på feedback från våra olika användargrupper och agerar utifrån de bästa förslagen. Om du vill veta mer om vad som kommer härnäst för [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams, se [lanseringsplanen för Dynamics 365](/dynamics365-release-plan/2021wave1/).

Om du vill delta i att förbättra appen för Teams, eller har en idé som skulle förenkla arbetet eller samarbetsupplevelsen i Teams, kan du lägga till en idé eller rösta på befintliga idéer på [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

### <a name="where-can-i-find-teams-integration-inside-the-business-central-web-client"></a>Var kan jag hitta Teams-integrering i Business Central-webbklienten?

Mer information om funktionalitet i webbklienten som länkar till Teams finns i [Dela poster och sidlänkar i Microsoft Teams](across-working-with-teams.md#share-link).

## [Business Central-tabell](#tab/tabs)

### <a name="who-can-see-the-content-of-a-tab"></a><a name="who-can-view"></a>Vem kan se innehållet på en flik?

Varje person i chatten eller kanalen som har:

1. Business Central-app för Teams installerad.
2. Antingen en Business Central-licens eller har beviljats åtkomst till Business Central med hjälp av deras Microsoft 365-licens.
3. Behörighet att visa data på sidan.

### <a name="where-does-the-recommended-content-come-from"></a><a name=#recommended-content></a>Var kommer det rekommenderade innehållet från?

Det rekommenderade innehållet som du kan välja från i alternativet **flikinnehåll** på en flik är baserat på ditt rollcenter. Det rekommenderade innehållet innehåller endast listsidor, till exempel kunder, försäljningsorder och leverantörer, inte kortsida som viss kund eller leverantör.

Det rekommenderade innehållet innehåller:

- Åtgärder i den översta navigeringsmenyn i rollcentret
- Alla listsidor som du har bokmärkt.
- Om en listsida innehåller olika vyer, inklusive de vyer du har skapat, kommer du också åt dessa vyer

Du kan lägga till listsidor med det rekommenderade innehållet genom att lägga till bokmärken. Du kan också ta bort det rekommenderade innehållet genom att ta bort bokmärken. Om du vill veta mer om hur du lägger till och tar bort bokmärken, se [Bokmärk en sida eller rapport i rollcentret](ui-bookmarks.md).

Om du växlar miljön eller företaget på fliken ändras det rekommenderade innehållet utifrån det rollcenter och de bokmärken för miljön och företaget som du växlar till.

### <a name="when-i-create-a-tab-does-it-grant-permissions-to-the-people-in-the-channel-or-chat"></a>När jag skapar en flik ger den behörighet till personerna i kanalen eller chatten?

Nr. När du skapar flikar påverkas inte behörigheterna och användarna måste redan ha behörighet till dessa data när de öppnar fliken.

### <a name="can-i-chat-alongside-a-tab"></a>Kan jag chatta bredvid en flik?

Ja. Använd ikonen chatt för att starta konversationen. Konversationen associeras sedan med fliken. 

### <a name="if-i-remove-a-tab-from-a-chat-or-channel-is-any-business-central-data-deleted"></a>Om jag tar bort en flik från en chatt eller kanal, är alla Business Central data borttagna?

Nr.

### <a name="can-i-safely-rename-a-tab"></a>Kan jag byta namn på en flik?

Ja. Innehållet på fliken är inte relaterat till flikens egentliga namn. Ändra namn kommer! 

### <a name="i-need-to-work-across-tasks-in-different-windows-can-i-do-this"></a>Jag måste arbeta mellan olika uppgifter i olika fönster. Kan jag göra det?

Ja. Du kan pop ut fliken till ett eget webbläsarfönster för att visa Business Central webbklienten. 

### <a name="can-i-add-or-pin-tab-in-team-meetings"></a>Kan jag lägga till eller fästa flik i Teams-möten?

Nr. Business Central-appen för Teams stöder inte flikar i möten.

### <a name="cant-add-a-tab-if-using-isv-urls-like-bcdynamicscom-but-can-pin"></a>Det går inte att lägga till en flik med ISV-URL:er som *.bc.dynamics.com (men kan fästas)

Stöds inte.

### <a name="when-i-do-things-in-the-tab-like-navigate-resort-apply-a-filter-or-search-do-others-see-my-changes"></a>När jag gör saker på fliken, t.ex. navigera, flytta, tillämpa ett filter eller söka, kan andra se mina ändringar?

Nr. Endast fältändringar och aktiva åtgärder påverkar hur andra ser innehållet på fliken.

### <a name="does-the-tab-content-refresh-automatically-if-not-how-do-i-refresh-it"></a>Uppdateras innehållet i flikar automatiskt? Om inte, hur uppdaterar jag det?

Innehållet uppdateras inte automatiskt och de här knapparna för närvarande inte uppdateras. Det bästa sättet att uppdatera innehållet och se till att det är upp till data, lämnar du fliken och går sedan tillbaka. 

### <a name="does-this-show-lists-and-records-from-my-customizations-and-add-ons"></a>Visar du listor och poster från mina anpassningar och tilläggsprogram?

Ja. 

### <a name="when-i-add-a-tab-will-people-see-it-in-my-language"></a>Kan andra se den på mitt språk när jag lägger till en flik?

Nr. Varje användare visar flikarnas innehåll på språk-, region-och tidszons inställningarna från Business Central. 

### <a name="can-i-have-multiple-tabs-pointing-to-different-content"></a>Kan jag ha flera flikar som pekar på ett annat innehåll?

Ja.

### <a name="can-i-also-add-tabs-to-chat-with-a-single-person"></a>Kan jag också lägga till flikar för att chatta med en enda person?

Ja, så länge chatten inte är ett utkast (det vill säga att ett meddelande inte har skickats för att initiera chatten) och att den andra personen även har installerat Business Central-programmet.

### <a name="can-i-switch-companies-within-a-tab"></a>Kan jag byta företag inom en flik?

Nr. 

### <a name="is-this-different-than-using-teams-generic-ability-to-create-a-tab-that-hosts-a-website"></a>Är detta annat än att använda Teams allmänna möjlighet att skapa en flik som är värd för en webbplats?

Ja. Vi rekommenderar inte att du använder metoden. I många fall fungerar det inte för Business Central.

## [Söka efter kontakter](#tab/contacts)

### <a name="which-tables-does-the-app-search-in"></a>Vilka tabeller söker programmet?

När du söker efter kontakter från [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams kommer dina söktermer att matchas mot poster i tabellen **Kontakter** i [!INCLUDE [prod_short.md](includes/prod_short.md)]. 

### <a name="which-fields-in-the-contacts-table-can-i-search"></a>Vilka fält i tabellen kontakter kan jag söka efter?

När du skriver sökorden i sökrutan matchas termerna mot de flesta fält i tabellen **kontakter**. Fälten inkluderar till exempel fälten **Nr.**, **Namn**, **Adress**, **Telefonnr.** eller **Mobiltelefonnummer** samt **E-post**. 

Sökvillkoren matchas inte mot några anpassade fält som har lagts till i tabellen **Kontakter** efter appar och tillägg.

### <a name="do-search-results-include-companies-and-persons"></a>Omfattar sökresultaten företag och personer?

Ja. I [!INCLUDE [prod_short.md](includes/prod_short.md)] kan kontakter vara av typen **Företag** eller **Person**, där en eller flera personer kan vara kopplade till ett företag. I sökresultatet har företag och personer olika ikoner.

### <a name="do-contacts-of-any-business-relationship-appear-in-the-results"></a>Visas kontakter för alla affärsrelationer i resultatet?

Ja. Vissa kontakter kan representera kunder eller leverantörer, eller både och. Andra kontakter utan definierad affärsrelation representerar vanligtvis potentiella kunder. Kontakter med andra affärsrelationer, inklusive eventuella egna relationer som du har konfigurerat i [!INCLUDE [prod_short.md](includes/prod_short.md)], visas också i sökresultaten.

### <a name="can-i-look-up-contact-details-during-meetings"></a>Kan jag söka efter kontaktinformation under möten?

Ja. Du kan slå upp kontaktinformation, interaktionshistorik och relaterade dokument för kunden eller leverantören under ett arbetsgruppmöte eller samtal medan mötet sker utan att lämna Teams.

Du kan faktiskt slå upp kontakt uppgifter var som helst i Teams med hjälp av kommandorutan. Du kan t.ex. slå upp kontaktinformation från Teams-kalendern och hjälpa dig att skapa möten.

### <a name="how-do-i-view-my-last-interactions-with-a-contact"></a>Hur visar jag de senaste interaktionerna med en kontakt?

I informationsfönstret för en kontakt visas interaktionens loggposter. I interaktionens loggposter finns en historik över de interaktioner som organisationen har haft med den specifika kontakten. Interaktionerna kan bestå av e-post som du har bytt, samtal som du har tagit emot eller dokument som du har skickat.

För att interaktioner ska visas måste [!INCLUDE [prod_short.md](includes/prod_short.md)] konfigureras för att spåra interaktioner. Mer information om hur du loggar interaktioner finns i [Registrera interaktioner med kontakter](marketing-interactions.md).

### <a name="how-do-i-register-a-teams-call-or-meeting-as-an-interaction"></a>Hur registrerar jag ett Teams-samtal eller ett möte som en interaktion?

I detaljfönstret för en kontakt, hitta åtgärden **Skapa interaktion** och väljer från inkommande eller utgående samtal som interaktionsmallar. Du kan också skapa egna interaktionsmallar som är särskilt avsedda att användas med Teams-konversationer.

### <a name="can-i-call-a-contact-from-the--app-for-teams"></a>Kan jag ringa en kontakt från [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] har begränsad integration med Teams som anropar funktioner. Det går inte att snabbt starta ett VOIP-samtal från fönstret kontaktkort eller kontaktinformation. När du visar kontakt uppgifterna i den stationära Teams-appen kan du emellertid välja fältet telefonnummer för att ringa det numret om Teams är inställd som standard uppringningsprogram på enheten. För att du ska kunna ringa upp fasta telefon- eller mobiltelefonnummer med PSTN (det traditionella telefonsystemet) kräver Teams att du har Microsoft 365 Business Voice-appen. Mer information finns i [Vad är Microsoft 365 Business Voice?](/MicrosoftTeams/business-voice/whats-business-voice).

### <a name="how-do-i-view-recent-documents-for-a-customer-or-vendor"></a>Hur visar jag nyligen använda dokument för en kund eller leverantör?

[!INCLUDE [prod_short.md](includes/prod_short.md)] relaterar vanligtvis en kontakt med en kund- eller leverantörspost som i sin tur är relaterad till affärstransaktionsposter, såsom försäljningsnoteringar eller inköpsfakturor. Om du vill visa relaterade dokument för en kontakt, gå till detaljfönstret för kontakten, välj fältvärdet **Affärsrelationskod** eller använd åtgärderna för att navigera till tillhörande kund eller leverantör. På sidan kund eller leverantör expandera rutan Faktabox för att visa statistik för olika dokument som du kan detaljgranska ned i. Din upplevelse kan variera beroende på dina anpassningar.

### <a name="how-do-i-search-for-contacts-using-special-characters"></a>Hur söker jag efter kontakter med hjälp av specialtecken?

Du kan ange sökkriterier med nästan alla Unicode-tecken. Emellertid reserverar [!INCLUDE [prod_short.md](includes/prod_short.md)] följande symboler för andra ändamål: **=**, **.**, **\*** och **@**. Om du använder dessa symboler i sökorden kanske de inte returnerar det förväntade resultatet. Om du inte ser de förväntade resultaten omsluter du symbolerna i sökvillkoren med enkla citat tecken, till exempel **Contoso'='2**.

### <a name="how-can-i-search-contacts-stored-in-a-different-company"></a>Hur söker jag efter kontakter som är lagrade i ett annat företag?

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams kan söka efter kunder, leverantörer och andra kontakter i ett företag i taget.  
Om du vill söka efter kontakter som är lagrade i ett annat [!INCLUDE [prod_short.md](includes/prod_short.md)] företag öppnar du [Inställningar](across-teams-settings.md) och ändrar sedan miljö och företag därifrån.

### <a name="are--contacts-different-than-the-ones-in-the-teams-contacts-screen"></a>Är [!INCLUDE [prod_short.md](includes/prod_short.md)] kontakter annorlunda än de som finns på skärmen för Teams-kontakter?

Ja. Kontakter som är lagrade i [!INCLUDE [prod_short.md](includes/prod_short.md)] representerar företagskontakter som är tillgängliga för organisationen. De är kontakter med vilka du har en etablerad och väldefinierad affärsrelation, eller kontakter som representerar potentiella kunder. Dessa kontakter är vanligtvis externa kontakter. Kontakterna som visas i den kontaktlistan för Teams-uppringning är egna kontakter. De här kontakterna delas inte nödvändigtvis med andra i organisationen, och de representerar oftast kontakter som är interna för organisationen.

### <a name="does--synchronize-contacts-with-teams"></a>Synkroniserar [!INCLUDE [prod_short.md](includes/prod_short.md)]-kontakter med Teams?

Nr Kontakter som är lagrade i [!INCLUDE [prod_short.md](includes/prod_short.md)] är fortfarande åtskilda från dina kontakter som lagras i Teams.
Det finns för närvarande inga planer på att synkronisera de båda listorna.

### <a name="what-is-the-minimum-version-of--for-contact-search"></a>Vilken är den lägsta versionen för [!INCLUDE [prod_short.md](includes/prod_short.md)] för kontaktsökning?

Vid kontaktsökningen måste du ha installerat [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams version 1.0.4 eller senare och du är ansluten till [!INCLUDE [prod_short.md](includes/prod_short.md)]-miljöer med version 18 eller senare.

### <a name="can-i-search-from-my-mobile-device"></a>Kan jag söka från min mobila enhet?

Kontaktsökningen är inte tillgänglig från Teams för iOS och Teams för Android för tillfället.

### <a name="which-permissions-do-i-need-for-contact-search"></a>Vilken behörighet behöver jag för kontaktsökning?

Om du vill söka efter kontakter måste du ha behörighet på objektnivå tabellen **Kontakter** i [!INCLUDE [prod_short.md](includes/prod_short.md)] företag som genomsöks. Om du vill visa informationsfönstret för en kontakt måste du minst ha behörigheten läsa på sidan **Kontakt** i [!INCLUDE [prod_short.md](includes/prod_short.md)] företaget och andra relaterade objekt.

### <a name="can-i-use-contact-search-if-im-a-delegated-admin"></a>Kan jag använda kontaktsökning om jag är en delegerad administratör?

Ja. Du kan också söka efter kontakter och kontaktuppgifter om du har en delegerad administratörsroll i en organisation.

### <a name="is-contact-search-affected-by-api-limits"></a>Påverkas kontaktsökningen av API-gränser?

Ja. Sökning efter kontakter från Teams baseras på [!INCLUDE [prod_short.md](includes/prod_short.md)] v2.0 API:er och med förbehåll för API-gränser som hanterar användning. Du kan läsa mer om gränserna med [aktuella API-begränsningar](/dynamics-nav/api-reference/v2.0/dynamics-current-limits).

### <a name="why-does-it-sometimes-ask-me-to-set-up-the-app"></a>Varför uppmanas jag ibland att ställa in appen?

När du har loggat in på [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams för första gången kommer appen att försöka bestämma ditt prioriterade företag i [!INCLUDE [prod_short.md](includes/prod_short.md)]. Om appen inte kan bestämma företaget måste du kanske gå till **Inställningarna** och välja det företag som du vill söka i. Denna situation inträffar exempelvis om du har tillgång till flera företag i olika miljöer i organisationen. I så fall måste du välja företag innan du kan börja söka.  

Appen kan också be dig att besöka **Inställningarna** om du inte har någon [!INCLUDE [prod_short.md](includes/prod_short.md)]-prenumeration, inga [!INCLUDE [prod_short.md](includes/prod_short.md)]-miljöer eller om ditt konto saknar [!INCLUDE [prod_short.md](includes/prod_short.md)]-licens.

### <a name="id-like-to-search-for-items-or-records-from-other-tables-can-i-do-this-from-teams"></a>Jag vill söka efter objekt eller poster från andra tabeller. Kan jag göra detta från Teams?

Det går inte att söka i andra tabeller just nu. [!INCLUDE [prod_short.md](includes/prod_short.md)]-app för Teams söker endast [!INCLUDE [prod_short.md](includes/prod_short.md)] kontaktlistan som kan inkludera leverantörer, kunder och andra kontakter.

Om du vill se sökfunktionerna för att ta med andra tabeller, uppmuntrar vi communityn att lägga till en idé eller rösta på befintliga idéer på https://aka.ms/BusinessCentralIdeas.

## [Arbeta med kort](#tab/cards)

### <a name="which-types-of-links-does-the-app-support"></a>Vilka typer av länkar har appen stöd för?

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams reagerar på de flesta [!INCLUDE [prod_short.md](includes/prod_short.md)]-länkar för webbklienter. När länken refererar till en enskild post på en sida visar kortet fält för den posten. De sidtyper som stöds är: 

- Kortsidor, till exempel artikelkortet
- Dokumentsidor, till exempel försäljningsorderdokument
- ListPlus-sidor som representerar en enda post som består av andra poster, till exempel ett utdrag för bankkontoavstämning
- Enkla listsidor där en post inte ger möjlighet att gå djupare ned på en separat informations sida, till exempel listan över postnummer

När du klistrar in en länk till rotwebbklientens URL, till exempel https://businesscentral.dynamics.com, visar kortet istället information som hjälper nya användare att komma igång med åtkomst till [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="how-do-i-delete-a-card-i-sent-to-a-chat"></a>Hur tar jag bort ett kort som jag skickat till en chatt?

Du kan inte ta bort ett kort som du redan har skickat till chatten. Du kan emellertid ta bort hela meddelandet som kortet ingår i.

Som meddelandets upphovsperson kan du ta bort alla meddelanden som du har skickat till chatten med en person, grupp eller kanal &mdash; såvida inte administratören har ställt in policyer som förhindrar att meddelanden tas bort. Om du modererar en kanal i egenskap av kanalägare kan administratören också ha gett dig behörighet att ta bort alla meddelanden i kanalen, inklusive de meddelanden som skickats av andra användare.

När du tar bort ett meddelande som innehåller ett kort raderas eller påverkas inga data i [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="do-cards-always-show-up-to-date-information"></a>Visar kort alltid aktuell information?

Nr Fältvärdena på ett kort i Teams, inklusive eventuella bilder, baseras på de data som är tillgängliga när kortet skickades till chatten. [!INCLUDE [prod_short.md](includes/prod_short.md)]-korten uppdateras inte automatiskt i Teams. 

### <a name="why-dont-cards-show-more-information-instead-of-just-the-page-name-and-details-button"></a>Varför visar inte kort mer information istället för bara sidnamnet och informationsknappen?

En administratör kan ha konfigurerat Teams-integration så att kort inte visar data om poster. Mer information finns i [Visa eller dölja postdata på kort](admin-teams-integration.md#show-or-hide-record-data-on-cards).

### <a name="will-others-see-my-card-if-they-dont-have-the--app-for-teams"></a>Kommer andra att se mitt kort om de inte har [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams?

När du skriver och skickar ett meddelande till chatten som innehåller ett kort kommer alla användare att se kortet&mdash;även om de inte har installerat [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams.

### <a name="how-do-i-find-out-which-company-a-card-in-teams-belongs-to"></a>Hur tar jag reda på vilket företag ett kort i Teams tillhör?

Om du arbetar i olika [!INCLUDE [prod_short.md](includes/prod_short.md)]-företag kan du prata med administratören om hur du aktiverar en företagsbricka för respektive företag. När den här iögonfallande ledtråden är aktiverad visas den i alla informationsfönster i Teams, och visar det företag och den miljö som posten tillhör. Mer information om hur du skapar företagsbrickor finns i [Visa en företagsbricka](admin-company-information.md#badge).

## [Arbeta med kortinformation](#tab/carddetails)

### <a name="where-is-the-save-button-in-the-details-window-in-teams"></a>Var finns knappen Spara i informationsfönstret Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] sparar automatiskt de ändringar som du gör i ett fält så fort du lämnar fältet. Om du vill lämna ett fält klickar/trycker du någonstans utanför fältet eller använder tabbtangenten för att flytta till nästa fält. När data visas i en dialogruta i informationsfönstret kan du behöva klicka på **OK**-knappen för att [!INCLUDE [prod_short.md](includes/prod_short.md)] ska spara ändringarna.

### <a name="if-i-choose-to-view-details-for-a-card-will-other-users-see-my-details-window"></a>Kan andra användare se mitt informationsfönster om jag väljer att visa information om ett kort?

Nr Även om alla i chatten eller mötet kan visa själva kortet, visas informationsfönstret bara för dig på enheten när du väljer **Detaljer**. Andra användare måste välja **Detaljer** om de vill visa informationsfönstret på sina enheter.

### <a name="can-i-start-a-teams-call-from-the-details-window-in-teams"></a>Kan jag starta ett Teams-samtal från informationsfönstret i Teams?

Ja. Om du använder Teams skrivbordsapp startar ett samtal genom att välja det länkade uppringningsnumret i ett fält för telefonnummer, t. ex. fältet **Mobilnummer** på **Kontakt**-kortet. Teams måste vara din valda uppringnings-app.

För att kunna ringa lokala eller internationella fasta telefoner och mobiltelefoner kräver Teams att du har en Business Voice-licens för företagssamtal. Du måste också ange Teams som samtalslösning. Mer information finns i [Planera din Teams-röstlösning](/microsoftteams/cloud-voice-landing-page) i Teams-dokumentationen.

### <a name="can-i-print-documents-from-the-details-window-in-teams"></a>Kan jag skriva ut dokument från informationsfönstret i Teams?

Ja. Du skriver ut rapporter och andra dokument med sedvanliga [!INCLUDE [prod_short.md](includes/prod_short.md)]-utskriftsfunktioner och alla molnskrivare som har aktiverats på sidan för **skrivarhantering** i [!INCLUDE [prod_short.md](includes/prod_short.md)]. Det går inte att skriva ut från Teams till lokala skrivare som din klientenhet känner till, till exempel skrivare som du vanligtvis skriver ut via från din webbläsare. Därför kan du inte skriva ut från fönstret för rapportförhandsgranskning, utan endast från huvudsidan för rapportbegäran, direkt till molnskrivarna.

Mer information om hur du konfigurerar molnskrivare finns i [Konfigurera skrivare](ui-specify-printer-selection-reports.md).

### <a name="can-i-access-the-camera-from-the-details-window-in-teams"></a>Kan jag komma åt kameran från informationsfönstret i Teams?

Ja. Alla [!INCLUDE [prod_short.md](includes/prod_short.md)]-funktioner i informationsfönstret som använder kameran är tillgängliga för alla Teams-klienter.

### <a name="can-i-access-my-location-from-the-details-window-in-teams"></a><a name="location"></a>Kan jag komma åt min plats från informationsfönstret i Teams?

Om du använder funktioner i [!INCLUDE [prod_short.md](includes/prod_short.md)] som har tillgång till dina aktuella platskoordinater, till exempel kartor, måste du använda Teams i webbläsaren eller mobilappen för Teams. Platsen är inte tillgänglig när du använder den stationära Teams-appen.

### <a name="how-do-i-open-the-details-in-a-new-window"></a>Hur gör jag för att öppna informationen i ett nytt fönster?

Att visa fönstret Detaljer som ett separat fönster är användbart när du vill arbeta med flera aktiviteter eller för att arbeta med affärs data samtidigt som du kan använda Teams-chatt och andra Teams-funktioner. Om du vill öppna information i ett eget fönster väljer du **öppna i webbläsare** på ellips-menyn (**...**) i det övre högra hörnet av fönstret.

## [Samarbeta med gäster](#tab/collaborating)

### <a name="can-i-share-cards-with-users-outside-my-organization"></a>Kan jag dela kort med användare utanför organisationen?

Ja. När du skriver och skickar ett meddelande som innehåller ett kort, kommer alla mottagare i chatten att se kortet &mdash; även om de är gäster eller externa för organisationen. Gäster kan också öppna informationsfönstret om de har fått behörighet att komma åt dessa data i [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="is-the-experience-any-different-for-users-that-are-guests"></a>Skiljer sig upplevelsen för gästanvändare?

Ja. Att bjuda in gästanvändare från utanför organisationen att delta i chatten eller en kanal ger dem en liknande, men inte identisk upplevelse jämfört med användarna inom organisationen. När en gäst får ett meddelande som innehåller ett kort kan de se det. Gäster kan också öppna sidan Detaljer om de har fått behörighet att komma åt dessa data i [!INCLUDE [prod_short.md](includes/prod_short.md)] och tilldelats en [!INCLUDE [prod_short.md](includes/prod_short.md)]-licens i organisationen.

Om du väljer informationslänken på ett Business Central-kort loggar du in på miljön från vilken kortet delades, förutsatt att du har tillstånd till miljön.

Gästanvändare kan inte använda kontaktsökning eftersom de är bundna till den ursprungliga klientorganisationen och stöder för närvarande inte sådana delegerade scenarier.

När en gäst skriver ett meddelande kommer länkar till din [!INCLUDE [prod_short.md](includes/prod_short.md)] inte att utökas till kort.

Information om andra likheter och skillnader mellan gäster och teammedlemmar finns i [Gästupplevelser i Teams](/MicrosoftTeams/guest-experience) i Teams-dokumentationen.

### <a name="how-does-a-guest-user-install-the--app"></a>Hur installerar en gästanvändare [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen?

Gäster har inte åtkomst till app-marknaden för egen installation av appar. Appen kan emellertid installeras automatiskt för dem enligt organisationens policyer. Ett annat sätt för en gästanvändare att installera [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen är när de tar emot ett chattmeddelande som innehåller ett [!INCLUDE [prod_short.md](includes/prod_short.md)]-kort. I det här fallet väljer användaren knappen **Detaljer** eller menyn på kortet och installerar sedan [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen så att den kan användas i din organisation. När du har installerat appen får användaren ingen automatisk behörighet att hämta data från din [!INCLUDE [prod_short.md](includes/prod_short.md)].

## [Dela till Teams](#tab/share)

### <a name="does-share-to-teams-send-a-compact-card"></a>Skickar delning till Teams ett kompakt kort?

Ja. Länken utökas automatiskt till ett kort om du har installerat Business Central-appen för Teams. 

### <a name="will-recipients-receive-the-message-from-me-or-from-a-business-central-service-account"></a>Kan mottagarna ta emot meddelandet från mig eller från ett konto för Business Central-tjänsten?

När du använder dela till Teams skickas meddelandet till en person, grupp eller kanal, på samma sätt som när du själv har skickat meddelandet Microsoft Teams. Mottagarna ser meddelandet från dig på deras prioriterade arbets grupps klient och kan reagera och reagera på samma sätt som om de normalt sett är ett meddelande från dig. 

### <a name="is-share-to-teams-available-in-business-central-on-premises"></a>Är delar till Teams som finns tillgängliga i Business Central lokal?

Nr På samma sätt som i [!INCLUDE [prod_short.md](includes/prod_short.md)] appen för Teams kan den här funktionen bara användas för webbklienten i [!INCLUDE [prod_short.md](includes/prod_short.md)] onlineläge. Det finns inga planer på att stödja [!INCLUDE [prod_short.md](includes/prod_short.md)]-distributionstyper &mdash;t. ex. lokalt, hybridmoln eller privatmoln&mdash;som inte Microsoft är värd för eller hanterar direkt.

### <a name="does-share-to-teams-grant-permissions-to-recipients"></a>Tilldelar Teams arbetsgrupper behörigheter till mottagare?

Nr När du delar med en person, grupp eller kanal påverkas inte behörigheterna. Användare som redan har behörighet att visa sidan och data som är riktade av länken kan göra det. Användare som inte har behörighet att visa sidor och data, eller inte har någon [!INCLUDE [prod_short.md](includes/prod_short.md)] licens, visas ett felmeddelande. 
 
### <a name="must-i-have-the-teams-desktop-app-installed-to-use-share-to-teams"></a>Måste jag ha Teams skrivbordsapp installerad för att kunna använda Dela till Teams?

Nr Allt du behöver är ett giltigt konto som har åtkomst till Microsoft Teams. 

### <a name="is-share-to-teams-available-in-all-business-central-clients"></a>Är delar till Teams som finns tillgängliga i alla Business Central-klienter?

I det här läget är dela till Teams tillgänglig på skrivbord webbklienten, i informationsfönstret i Teams och när du öppnar en sida i ett nytt fönster från Outlook-tillägget.

### <a name="where-do-i-find-share-to-teams-in-business-central"></a>Var hittar jag dela till Teams i Business Central?

**Dela till Teams åtgärd** finns i **Dela** på alla sidor, till exempel kort- och dokumentsidor, list- eller kalkylbladssidor, inklusive anpassade sidor. Åtgärden är inte tillgänglig i dialogrutor eller sidor som visas som dialogrutor, till exempel uppslagssidor eller guider.

---
## <a name="see-also"></a>Se även

[Integreringsöversikt för [!INCLUDE [prod_short](includes/prod_short.md)] och Microsoft Teams](across-teams-overview.md)  
[Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)  
[Söka efter kunder, leverantörer och andra kontakter från Microsoft Teams](across-search-contacts-teams.md)  
[Dela poster i Microsoft Teams](across-working-with-teams.md)  
[Felsöka Teams](admin-teams-troubleshooting.md)  
[Ändra företag och andra inställningar i Teams](across-teams-settings.md)  
[Utveckling för Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
