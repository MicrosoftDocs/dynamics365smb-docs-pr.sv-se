---
title: Vanliga frågor och Svar om Teams
description: Få svar på några vanliga frågor om att arbeta med Teams och Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors
ms.date: 01/26/2021
ms.author: jswymer
ms.openlocfilehash: 79b6069ffb4c73d783b2c05d3a44a55763805a52
ms.sourcegitcommit: 1c9eec7554305603d688bf85ce3986d0b1f72ede
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/26/2021
ms.locfileid: "5068440"
---
# <a name="teams-faq"></a>Vanliga frågor och Svar om Teams

[!INCLUDE [online_only](includes/online_only.md)]

I den här artikeln besvaras några frågor som du kanske har kring arbetet med Teams och [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[Allmänt](#tab/general)

### <a name="how-do-i-sign-in-to-the-prod_shortmd-app-in-teams"></a>Hur loggar jag in i appen [!INCLUDE [prod_short.md](includes/prod_short.md)] i Teams? 

När du har installerat appen blir du ombedd att logga in första gången du klistrar in en [!INCLUDE [prod_short.md](includes/prod_short.md)]-länk i chattfunktionen i Teams eller när du väljer åtgärden **Detaljerad information** i Teams. Beroende på Teams-klient måste du kanske ange din behörighet för att komma åt [!INCLUDE [prod_short.md](includes/prod_short.md)]. 

### <a name="how-do-i-sign-out-of-the-prod_shortmd-app-in-teams"></a>Hur loggar jag ut från appen [!INCLUDE [prod_short.md](includes/prod_short.md)] i Teams? 

Om du vill logga ut från din aktuella användaridentitet i Teams som du använder för att ansluta till [!INCLUDE [prod_short.md](includes/prod_short.md)] går du till valfri chattdialogruta och väljer ikonen [!INCLUDE [prod_short.md](includes/prod_short.md)] under denna. När fönstret visas kontrollerar du den aktuella inloggade identiteten och väljer sedan **Logga ut** . Om du använder Teams i webbläsaren loggas du också ut från alla [!INCLUDE [prod_short.md](includes/prod_short.md)]-webbklienter i samma webbläsarfönster.

### <a name="does-the-app-for-teams-connect-to-prod_shortmd-on-premises"></a>Ansluter appen för Teams till [!INCLUDE [prod_short.md](includes/prod_short.md)] lokalt? 

Nr [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams fungerar endast med [!INCLUDE [prod_short.md](includes/prod_short.md)] online. Det finns inga planer på att stödja [!INCLUDE [prod_short.md](includes/prod_short.md)]-distributionstyper &mdash;t. ex. lokalt, hybridmoln eller privatmoln&mdash;som inte Microsoft är värd för eller hanterar direkt.

### <a name="does-the-app-work-with-multiple-companies-and-environments"></a>Fungerar appen med flera företag och miljöer? 

Ja. När [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen expanderar en länk till ett kort måste länken innehålla miljö- och företagsnamn för att appen ska matcha posten i rätt företag. Du kan klistra in länkar till alla företag och miljöer som du har till gång till inom din organisation samt från det [!INCLUDE [prod_short.md](includes/prod_short.md)]-konto som du använde när du loggade in. Deltagarna i chatten kan se kortet. De kan emellertid inte se kortinformationen om de inte har behörighet till det företag eller den miljö där posten lagras.

### <a name="in-which-countries-or-regions-is-the-prod_shortmd-app-available"></a>I vilka länder eller regioner finns [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen tillgänglig? 

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams begränsas inte av land eller region. Appen finns tillgänglig på alla marknader som för närvarande stöds av Teams-marknaden. 

### <a name="does-the-prod_shortmd-app-work-with-any-localization-of-prod_shortmd"></a>Fungerar [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen med valfri lokalisering av [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Ja. Appen är avsedd att användas vid valfri lokalisering av [!INCLUDE [prod_short.md](includes/prod_short.md)], oavsett om lokaliseringen erbjuds direkt från Microsoft eller via en partner. För mer information, se [Tillgänglighet för land/region och språk som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="which-languages-does-the-prod_shortmd-app-support"></a><a name="language"></a>Vilka språk stöder [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen?
<!--TODO Run by Mike -->

Två saker avgör vilket språk som används för kort och kortinformation i Teams:

1. Ditt språk i Teams, som du kan se i bland dina kontoinställningar i Teams. 
2. Ditt språk i [!INCLUDE [prod_short.md](includes/prod_short.md)], som du kan använda för att visa [!INCLUDE [prod_short.md](includes/prod_short.md)]-webb klienten (se [Ändra grundläggande inställning – Språk](ui-change-basic-settings.md#language)).

I följande tabell förklaras hur upplevelsen skiljer sig åt för meddelandeförfattare och -mottagare, beroende på språkinställningar och språktillgänglighet.

|Vem|Kort|Kortinformation |
|-|----|--------------| 
|Meddelandeförfattare |Visar på det språk som har angetts för dig i Teams. Om [!INCLUDE [prod_short.md](includes/prod_short.md)] inte erbjuder samma språk visas kortet på engelska. |Visas på det språk som angetts för dig i [!INCLUDE [prod_short.md](includes/prod_short.md)].  som kan inkludera språk från språk-appar tillhandahållna av partners. |
|Meddelandemottagare |Visas på meddelandets upphovspersons språk. |Visas på det språk som angetts för dig i [!INCLUDE [prod_short.md](includes/prod_short.md)]. |

Listan över språk som stöds för [!INCLUDE [prod_short.md](includes/prod_short.md)] finns i [Språk som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### <a name="where-can-i-find-teams-integration-inside-the-prod_shortmd-web-client"></a>Var kan jag hitta Teams-integrering i [!INCLUDE [prod_short.md](includes/prod_short.md)]-webbklienten? 

Det finns för närvarande varken inbäddning av Teams-kontroller eller Teams-funktioner i [!INCLUDE [prod_short.md](includes/prod_short.md)]-webbklienten eller andra klienter.  

### <a name="does-prod_shortmd-work-with-the-teams-mobile-app"></a>Fungerar [!INCLUDE [prod_short.md](includes/prod_short.md)] med mobilappen för Teams?

Ja. [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen kan installeras från den stationära Teams-appen eller webbläsaren, eller av en administratör för alla användare. När [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen väl har installerats är den automatiskt tillgängligt i Teams för iOS och Android. På mobila enheter kan du visa kort som har skickats av andra, få åtkomst till information, eller utnyttja kortet till [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappens fulla utsträckning. Du kan emellertid inte klistra in länkar som expanderas till kort när du skriver meddelanden. För minimikrav för mobila enheter, se [Minimikrav för att använda Business Central](product-requirements.md).

### <a name="is-the-prod_shortmd-app-for-teams-the-same-as-the-prod_shortmd-app-for-ios-and-android"></a>Är [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams samma som [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för iOS och Android? 

Nr Appen för Teams är ett tillägg till Microsoft Teams och uteslutande utformat för samarbetsupplevelser som dyker upp i Teams. [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen ger å andra sidan en rik upplevelse som du kan använda för att arbeta med [!INCLUDE [prod_short.md](includes/prod_short.md)]-data på dina mobila enheter.

Mobila användare uppmuntras att installera både mobilappen och appen För Teams i syfte att få ut maximalt av [!INCLUDE [prod_short.md](includes/prod_short.md)]. Med båda appar installerade kan du välja åtgärden **Öppna** på ett kort i Teams för att visa kortinformationen i [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen. Information om hur du installerar mobilapparna för [!INCLUDE [prod_short.md](includes/prod_short.md)] och Teams finns i:

- [Skaffa Business Central på din mobila enhet](install-mobile-app.md)
- [Hämta mobilappen för Teams](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) från Microsofts support

### <a name="does-the-prod_shortmd-app-work-in-all-teams-clients"></a>Fungerar [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i alla Teams-klienter?

Nr [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams stöds inte när den installeras som ett paket för macOS eller Linux. På dessa plattformar kan du istället använda Teams via webbläsare som stöds.

För minimikrav för [!INCLUDE [prod_short.md](includes/prod_short.md)] se [Minimikrav för att använda Business Central](product-requirements.md#teams).

Mer information om val av Teams-klienter och hur du installerar dem finns i [Skaffa klienter för Microsoft Teams](/microsoftteams/get-clients) i Teams-dokumentationen.

### <a name="which-teams-client-is-best-for-prod_shortmd"></a>Vilken Teams-klient passar bäst för [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Det finns endast smärre skillnader och begränsningar mellan Teams-klienter som kan påverka din upplevelse av [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams. När du väljer en Teams-klient bör du tänka på följande:

- Det går inte att komma åt kameran och platsen från informationsfönstret i den stationära Teams-appen 
- Med hjälp av Microsoft Edge och Teams i webbläsaren kan du enkelt arbeta över flera olika identiteter och konton genom att logga in på Teams från olika profiler. Mer information om hur du använder profiler i Microsoft Edge finns i [Logga in och skapa flera profiler i Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) på Microsoft Support.

### <a name="what-is-the-best-way-for-me-to-demonstrate-prod_shortmd-and-microsoft-teams-to-prospective-customers"></a>Vilket är det bästa sättet att demonstrera [!INCLUDE [prod_short.md](includes/prod_short.md)] och Microsoft Teams för potentiella kunder?

Om du är en återförsäljarpartner kanske du vill ha en miljö som du kan visa potentiella kunder som en del av demonstrationerna i samband med förförsäljning. För att undvika att påverka Microsoft Teams inom din organisation kan du skaffa ett Microsoft 365-demokonto på [https://aka.ms/CDX](https://aka.ms/CDX). Det här kontot ger dig full kontroll över en oberoende Azure-organisation som innehåller Microsoft Teams och [!INCLUDE [prod_short.md](includes/prod_short.md)]. Mer information finns i [Förbereda demonstrationsmiljöer av Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### <a name="does-the-prod_shortmd-app-for-teams-cater-for-my-customization-and-personalization"></a>Uppfyller [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams mina anpassningsbehov?

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams kan visa kort för länkar till kundsidor och -tabeller i [!INCLUDE [prod_short.md](includes/prod_short.md)], till exempel de sidor och tabeller som kommer från egna anpassade tillägg eller från AppSource.

Fälten som visas på ett kort i Teams kan också påverkas av [!INCLUDE [prod_short.md](includes/prod_short.md)]-anpassningar som har installerats för organisationen. Korten beaktar inga rollspecifika anpassningar eller användaranpassningar. I fönstret för kortinformation visas detaljerad information på samma sätt som när du ser den i [!INCLUDE [prod_short.md](includes/prod_short.md)], inklusive eventuella tillägg, rollanpassningar och användaranpassningar.

### <a name="where-can-i-learn-about-my-privacy"></a>Var kan jag få veta mer om min sekretess? 

Du kan lära dig hur Microsoft hanterar dina uppgifter i [Microsofts sekretesspolicy](https://go.microsoft.com/fwlink/?linkid=2030602). 

Kontakta administratören för information om hur din organisation hanterar sekretessen för dina data. 

### <a name="how-do-i-uninstall-the-prod_shortmd-app-for-teams"></a>Hur avinstallerar jag [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams? 

Om du vill ta bort appen som du har installerat åt dig själv går du till valfri chattdialogruta, letar upp [!INCLUDE [prod_short.md](includes/prod_short.md)]-ikonen därunder, högerklickar på ikonen och väljer Avinstallera.  

### <a name="will-microsoft-continue-to-improve-the-prod_shortmd-app-for-teams"></a>Kommer Microsoft att fortsätta att förbättra [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams?

På Microsoft lyssnar vi ständigt på feedback från våra olika användargrupper och agerar utifrån de bästa förslagen. Om du vill veta mer om vad som kommer härnäst för [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams, se då [lanseringsplanen för Dynamics 365](https://aka.ms/dynamics365releaseplan).

Om du vill delta i att förbättra appen för Teams, eller har en fantastisk idé som skulle förenkla arbetet eller samarbetsupplevelsen i Teams, kan du lägga till en idé eller rösta på befintliga idéer på [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="working-with-cards"></a>[Arbeta med kort](#tab/cards)

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

### <a name="will-others-see-my-card-if-they-dont-have-the-prod_shortmd-app-for-teams"></a>Kommer andra att se mitt kort om de inte har [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams? 

När du skriver och skickar ett meddelande till chatten som innehåller ett kort kommer alla användare att se kortet, även om de inte har installerat [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen för Teams.

## <a name="working-with-card-details"></a>[Arbeta med kortinformation](#tab/carddetails)

### <a name="where-is-the-save-button-in-the-details-window-in-teams"></a>Var finns knappen Spara i informationsfönstret Teams? 

[!INCLUDE [prod_short.md](includes/prod_short.md)] sparar automatiskt de ändringar som du gör i ett fält så fort du lämnar fältet. Om du vill lämna ett fält klickar/trycker du någonstans utanför fältet eller använder tabbtangenten för att flytta till nästa fält. När data visas i en dialogruta i informationsfönstret kan du behöva klicka på **OK**-knappen för att [!INCLUDE [prod_short.md](includes/prod_short.md)] ska spara ändringarna.

### <a name="if-i-choose-to-view-details-for-a-card-will-other-users-see-my-details-window"></a>Kan andra användare se mitt informationsfönster om jag väljer att visa information om ett kort? 

Nr Även om alla i chatten kan visa själva kortet, visas informationsfönstret bara för dig på enheten när du väljer **Detaljer**. Andra användare måste välja **Detaljer** om de vill visa informationsfönstret på sina enheter.

### <a name="can-i-start-a-teams-call-from-the-details-window-in-teams"></a>Kan jag starta ett Teams-samtal från informationsfönstret i Teams? 

Ja. Du kan starta ett samtal genom att välja det länkade uppringningsnumret i ett fält för telefonnummer, t. ex. fältet **Mobilnummer** på **Kontakt**-kortet. Teams måste vara din valda uppringnings-app.

För att kunna ringa lokala eller internationella fasta telefoner och mobiltelefoner från Teams måste du ha en Teams-licens för företagssamtal. Du måste också ange Teams som samtalslösning. Mer information finns i [Planera din Teams-röstlösning](/microsoftteams/cloud-voice-landing-page) i Teams-dokumentationen.

### <a name="can-i-print-documents-from-the-details-window-in-teams"></a>Kan jag skriva ut dokument från informationsfönstret i Teams? 

Ja. Du skriver ut rapporter och andra dokument med sedvanliga [!INCLUDE [prod_short.md](includes/prod_short.md)]-utskriftsfunktioner och alla molnskrivare som har aktiverats på sidan för **skrivarhantering** i [!INCLUDE [prod_short.md](includes/prod_short.md)]. Det går inte att skriva ut från Teams till lokala skrivare som din klientenhet känner till, till exempel skrivare som du vanligtvis skriver ut via från din webbläsare. Därför kan du inte skriva ut från fönstret för rapportförhandsgranskning, utan endast från huvudsidan för rapportbegäran, direkt till molnskrivarna.

Mer information om hur du konfigurerar molnskrivare finns i [Konfigurera skrivare](ui-specify-printer-selection-reports.md).

### <a name="can-i-access-the-camera-from-the-details-window-in-teams"></a>Kan jag komma åt kameran från informationsfönstret i Teams? 

Ja. Alla [!INCLUDE [prod_short.md](includes/prod_short.md)]-funktioner i informationsfönstret som använder kameran är tillgängliga för alla Teams-klienter.

### <a name="can-i-access-my-location-from-the-details-window-in-teams"></a><a name="location"></a>Kan jag komma åt min plats från informationsfönstret i Teams?

Om du använder funktioner i [!INCLUDE [prod_short.md](includes/prod_short.md)] som har tillgång till dina aktuella platskoordinater, till exempel kartor, måste du använda Teams i webbläsaren eller mobilappen för Teams. Platsen är inte tillgänglig när du använder den stationära Teams-appen. 

## <a name="collaborating-with-guests"></a>[Samarbeta med gäster ](#tab/collaborating)

### <a name="can-i-share-cards-with-users-outside-my-organization"></a>Kan jag dela kort med användare utanför organisationen? 

Ja. När du skriver och skickar ett meddelande som innehåller ett kort, kommer alla mottagare i chatten att se kortet &mdash; även om de är gäster eller externa för organisationen. Gäster kan också öppna informationsfönstret om de har fått behörighet att komma åt dessa data i [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="is-the-experience-any-different-for-users-that-are-guests"></a>Skiljer sig upplevelsen för gästanvändare?

Ja. Att bjuda in gästanvändare från utanför organisationen att delta i chatten eller en kanal ger dem en liknande, men inte identisk upplevelse jämfört med användarna inom organisationen. När en gäst får ett meddelande som innehåller ett kort kan de se det. Gäster kan också öppna fönstret Detaljer om de har fått behörighet att komma åt dessa data i [!INCLUDE [prod_short.md](includes/prod_short.md)] och tilldelats en [!INCLUDE [prod_short.md](includes/prod_short.md)]-licens i organisationen. När en gäst skriver ett meddelande kommer länkar till din [!INCLUDE [prod_short.md](includes/prod_short.md)] inte att utökas till kort.

Information om andra likheter och skillnader mellan gäster och gruppmedlemmar finns i [Gästupplevelser i Teams](/MicrosoftTeams/guest-experience) i Teams-dokumentationen.

### <a name="how-does-a-guest-user-install-the-prod_shortmd-app"></a>Hur installerar en gästanvändare [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen? 

Gäster har inte åtkomst till app-marknaden för egen installation av appar. Appen kan emellertid installeras automatiskt för dem enligt organisationens policyer. Ett annat sätt för en gästanvändare att installera [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen är när de tar emot ett chattmeddelande som innehåller ett [!INCLUDE [prod_short.md](includes/prod_short.md)]-kort. I det här fallet väljer användaren knappen **Detaljer** eller menyn på kortet och installerar sedan [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen så att den kan användas i din organisation. När du har installerat appen får användaren ingen automatisk behörighet att hämta data från din [!INCLUDE [prod_short.md](includes/prod_short.md)].

<!--TODO - check with Mike on this -->
---

## <a name="see-also"></a>Se även

[Integreringsöversikt för [!INCLUDE [prod_short](includes/prod_short.md)] och Microsoft Teams](across-teams-overview.md)  
[Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)  
[Felsöka Teams](admin-teams-troubleshooting.md)  
[Utveckling för Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  