---
title: Tillägget Momsgruppshantering för Storbritannien
description: Du kan samarbeta med andra företag för att skapa en momsgrupp där alla medlemmar rapporterar moms i en enda retur.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'VAT, value added tax, report'
ms.search.form: '4700, 4701, 4703, 4704, 4705, 4706, 4707, 4708, 4709,'
ms.date: 06/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Tillägget Momsgruppshantering för Storbritannien

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Du kan ansluta ett eller flera företag i Storbritannien för att kombinera momsrapportering under ett enda registreringsnummer. Denna typ av ordning kallas *Momsgrupp*. Du kan interagera med gruppen som en medlem av eller representant för gruppen.

## Skapa en momsgrupp

Medlemmar i momsgrupper och grupprepresentanten kan använda guiden för assisterad **konfiguration av momsgruppshantering** för att definiera deras engagemang i gruppen och upprätta en anslutning mellan deras [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisationer. Gruppmedlemmarna kommer att använda anslutningen för att skicka in sina momsreturer till gruppens representant. Gruppens representant använder en enda momsretur för att skicka in gruppens moms till skattemyndigheten.

[!INCLUDE[prod_short](includes/prod_short.md)] stöder returer inom gruppens momsreturer för företag som använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt eller online, i någon kombination som påverkar kommunikationsinställningarna mellan företag. I den här artikeln beskriver olika gruppkonfigurationer.

### Licenskrav

Deltagare i gruppen måste vara licensierade att använda [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan inte använda gästkonton i momsgrupper.

* För att beräkna och skicka momsreturer måste användaren vara en fullständig [!INCLUDE[prod_short](includes/prod_short.md)]-användare.
* Om du vill logga in och utföra grundläggande uppgifter, till exempel skapa konton, måste du ha [!INCLUDE[prod_long](includes/prod_long.md)] teammedlemslicens.

## Ställ in en momsgrupp

Följande är en rekommenderad ordning för hur administratörer använder en momsgrupp:

1. Skapa konfigurationen i [Microsoft Entra ID-konfiguration för gruppmedlemmar](#microsoft-entra-id-setup-for-group-members).
2. Dela den tekniska informationen om medlemmar i momsgruppen och grupprepresentanten måste ansluta sina [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisationer. Vanligtvis har momsgruppens representant den här informationen, till exempel [API URL](#group-api-setup) och namnet på den momsgruppsrepresentants miljö som momsgruppens medlemmar ska skicka moms till.
3. Skapa användare som VAT-gruppmedlemmar kan använda för att autentisera när de ansluter till momsgrupprepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]. Användarna måste ha fullständiga användarlicenser för [!INCLUDE[prod_short](includes/prod_short.md)].
4. Kör guiden för assisterad konfiguration **Konfigurera Momsgruppshantering** för att ansluta momsgruppens medlemmar.

   Den representativa momsgruppen måste tillhandahålla viss information för gruppmedlemmarna för att slutföra inställningarna. (Mer information finns i avsnittet [Ange momsgruppmedlemmar](#set-up-vat-group-members) nedan.) Anteckna **grupp medlems-ID** för varje momsgruppmedlem. Grupprepresentanten behöver dessa ID för att lägga till företagen i momsgruppen.
5. Konfigurera tillägget Momsgruppshantering i momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)] med hjälp av guiden för assisterad konfiguration **Konfigurera Momsgruppshantering**.

> [!NOTE]
> Om gruppmedlemmar vill ansluta till momsgruppens representant behöver de en användare med åtkomst till momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]. Momsgruppens representant måste skapa minst en användare för detta. Av säkerhetsskäl rekommenderar vi dock att de skapar en användare för varje momsgruppmedlem som kan vara ett systemanvändarkonto som inte är relaterat till en faktisk person. Se till att distribuera användarautentiseringsuppgifter för dessa användare till momsgruppsmedlemmarna på ett säkert sätt.

### Microsoft Entra ID-konfiguration för gruppmedlemmar

När momsgruppens representant använder [!INCLUDE[prod_short](includes/prod_short.md)] online eller lokalt måste momsgruppsmedlemmar använda Microsoft Entra-ID för att autentisera användare när dessa skickar momsreturer till momsgruppens representant. För [!INCLUDE[prod_short](includes/prod_short.md)] lokal måste medlemmar konfigurera enkel inloggning. Mer information finns i [Konfigurera Microsoft Entra-autentisering med WS-Federation](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool).

Om momsgruppsmedlemmarna också använder [!INCLUDE[prod_short](includes/prod_short.md)] online kan medlemmen autentisera med de angivna autentiseringsuppgifterna och den inloggningsinformation som ges av grupprepresentanten. Mer information finns i avsnittet [Ange momsgruppmedlemmar](#set-up-vat-group-members) nedan.

Momsgruppsmedlemmar med lokalt [!INCLUDE[prod_short](includes/prod_short.md)] måste konfigurera en appregistrering i Microsoft Entra-ID för momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisation. Appregistreringen gör att momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)] online kan autentisera gruppmedlemmen. Mer information finns i [Snabbstart: registrera ett program med Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app).

När momsgruppmedlemmens administratör skapar programregistreringen i Microsoft Entra ID måste denne ange följande information:

* I avsnittet **Autentisering** lägger du till **Webb** som en plattform och använder följande **omdirigerings-URL**: `https://businesscentral.dynamics.com/OAuthLanding.htm`.
* I avsnittet **Autentisering**, i alternativet för att välja **Kontotyper som stöds**, väljer du **Konton i organisationens katalog (en Microsoft Entra-katalog – flera klientorganisationer)**.
* I avsnittet **Certifikat och hemligheter** skapar du en ny klienthemlighet och antecknar värdet. Momsgruppsmedlemmarna kommer att behöva hemligheten när de konfigurerar anslutningen till gruppens representant.
* I avsnittet **API-behörigheter** lägger du till behörigheter till [!INCLUDE[prod_short](includes/prod_short.md)]. Aktivera delegerad åtkomst till **Financials.ReadWrite.All** och **user_impersonation**.
* I avsnittet **Översikt** antecknar du **Applikation-ID (klient)**. Momsgruppsmedlemmarna kommer att behöva detta ID när de konfigurerar anslutningen till gruppens representant.

### Konfigurera grupp-API

Den representativa momsgrupp skapar och levererar API för att gruppera medlemmar. Medlemmarna använder API för att ansluta till representantens [!INCLUDE[prod_short](includes/prod_short.md)] innehavare och skicka in momsreturer. Momsgruppsmedlemmar kan ofta använda [!INCLUDE[prod_short](includes/prod_short.md)] i separata Microsoft Entra-klientorganisationer. Därför behövs en inställning för att ansluta momsgruppsmedlemmen och representantens [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Detta kräver autentiseringsuppgifter för en administratörs konto som har fullständig användarlicens för [!INCLUDE[prod_short](includes/prod_short.md)].

1. I Business Central administratörscenter för representantens klientorganisation väljer du**Miljöer**.
1. Välj miljö för representanten.
1. I avsnittet **Detaljer** kopiera **URL**.
1. Öppna Anteckningar och klistra in URL-adressen. Ersätt `https://businesscentral.dynamics.com` med `https://api.businesscentral.dynamics.com/v2.0`.

## Ställ in medlemmar i momsgruppen

Momsgruppsmedlemmar ansluter till representanten genom att anropa en webbtjänst på momsgruppsrepresentantens klientorganisation. Anroparen måste autentiseras med hjälp av OAuth2. När tillägget Momsgruppshantering har konfigurerats ombeds medlemmarna att autentisera till momsgruppens representant då en åtkomsttoken genereras och sparas. Detta åtkomsttoken används när momsreturer skickas till en momsgruppsrepresentant.

> [!IMPORTANT]
> Medlemsföretagen i momsgruppen behöver inte ansluta till HMRC eftersom de rapporterar via gruppens representant.

Innan momsgruppens medlemmar startar konfigurationen (visas nedan) måste de kontakta momsgruppen som är representativ för följande information om deras [!INCLUDE[prod_short](includes/prod_short.md)] innehavare:

* API-URL
* Namnet på företaget
* Inloggningsuppgifter för den dedikerade användaren

1. I övre högra hörnet under **Inställningar** väljer du ![Inställningar](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter"). och sedan åtgärden **assisterad konfiguration**.
2. Välj åtgärden **konfigurera momsgruppshantering**.
3. I fältet **Roll för momsgrupp** välj **Medlem** sedan **Nästa**.
4. Kopiera värdet i fältet **Gruppmedlems-ID** och dela det med momsgruppens representant så att de kan lägga till ditt företag som en godkänd medlem i gruppen.
5. I fältet **Grupprepresentantens produktversion** anger du den version av [!INCLUDE[prod_short](includes/prod_short.md)] som representanten använder.
6. I fältet **API URL** anger du API URL för momsgruppens representant. URL:en formateras vanligen så här: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Till exempel `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.
7. I fältet **Grupprepresentantens företag**, ange företagsnamnet för momsgruppens representant som **CRONUS UK Ltd**.
8. I fältet **Autentiseringstyp**, välj alternativet för **OAuth2**. Om momsgruppens representant använder [!INCLUDE[prod_short](includes/prod_short.md)] online, ange **Grupprepresentant som använder Business Central Online** och välj sedan **Nästa**.

   Följ sedan stegen i antingen [Momsgruppsrepresentant använder Business Central online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) eller [Momsgruppsrepresentant använder Business Central lokalt](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premises) nedan.

### Momsgrupprepresentant använder Business Central online

1. Ange de användarautentiseringsuppgifter som angavs av momsgruppens representant och lägg till de behörigheter för att generera åtkomsttoken.
2. Välj den momsrapportkonfiguration du använder för att skicka in momsdeklarationer till de brittiska skattemyndigheterna. 

När du är klar med inställningarna kommer [!INCLUDE[prod_short](includes/prod_short.md)] att skapa en ny konfiguration baserat på det här alternativet som låter dig skicka momsreturer till momsgruppens representant.

### Momsgrupprepresentant som använder Business Central lokal

1. Ange de användarautentiseringsuppgifter som anges av moms grupps representanten och välj **Nästa**.
2. I fältet **Klient-ID** anger du klient-ID:t från programregistreringen i [Konfiguration av Microsoft Entra ID för gruppmedlemmar](#microsoft-entra-id-setup-for-group-members).
3. I fältet **Klienthemlighet** anger du klienthemligheten från programregistreringen i Microsoft Entra ID.
4. I fältet **OAuth 2.0-utfärdare** anger du `https://login.microsoftonline.com/common/oauth2`.
5. I fältet **URL för OAuth 2.0-resurs** anger du `https://api.businesscentral.dynamics.com/`.
6. I fältet **Omdirigerings-URL för OAuth 2.0** anger du `https://businesscentral.dynamics.com/OAuthLanding.htm`.
7. När du har angett de olika fälten väljer du **nästa** och bekräftar sedan autentiseringen för att generera åtkomsttoken.
8. Välj den momsrapportkonfiguration du använder för att skicka in momsdeklarationer till de brittiska skattemyndigheterna.

## Skapa en momsgruppsrepresentant

> [!NOTE]
> För lokal stöder [!INCLUDE[prod_short](includes/prod_short.md)] bara en enskild innehavare av representant för gruppen.

> [!IMPORTANT]
> Representantföretaget måste aktivera **HMRC momsinställningar** på sidan **Tjänstanslutningar**. Representanter måste också hämta momsreturperioder från HMRC.

1. I det övre högra hörnet väljer du ikonen **inställningar** ![inställningar.](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och välj åtgärden **Assisterad konfiguration**.
2. Välj åtgärden **konfigurera momsgruppshantering**.
3. I fältet **Momsgrupproller** välj **Representant** för att fungera som representant för momsgruppen, välj sedan **Nästa**.
4. I fältet **Gruppens avräkningskonto** ange det avräkningskonto som används för gruppmedlemmarnas momsbelopp. Det här kontot ska ha **resurser** som **kontokategori**.
5. I fältet **Momsavräkningskonto** anger du det konto som du använder för momsavräkningar. Det här kontot ska ha **Skulder** som **kontokategori**.
6. I rutan **Rutnummer för moms att betala** anger du rutan som representerar det totala återstående momsbeloppet från en momsgruppsinlämning.
7. I fältet **Redovisningsjournalmall för gruppavräkning** anger du den allmänna journalmall som används för att skapa dokumentet som gruppens representant bokför gruppmomsen till avräkningskontot med.
8. I fältet **godkända medlemmar** visas det antal gruppmedlemmar som har ställts in för att skicka momsreturer till grupprepresentanten. För att lägga till nya medlemmar, välj numret för att öppna **Godkända medlemmar för momsgrupp** och lägg till följande information:
    1. I fältet **Gruppmedlems-ID** ange en identifierare för gruppmedlemmen, som visas under gruppmedlem konfigurationen (läs mer i avsnittet [konfiguration av momsgruppens medlem](#set-up-vat-group-members) ovan).
    2. I fältet **Gruppmedlemsnamn**, ange namnet på gruppmedlemmen.
    3. I fältet **Företag** ange från vilket företag gruppmedlemmen ska lämna momsdeklarationer i [!INCLUDE[prod_short](includes/prod_short.md)], t.ex. **CRONUS UK Ltd**.
    4. Ange företagets kontaktinformation.

## Använda funktionerna för momsgruppshantering

Momsgruppsmedlemmar använder standardprocesser för att förbereda momsreturer. Den enda skillnaden är att medlemma måste välja rapportversionen **VATGROUP** på sidan **Momsretur** för att skicka momsreturen till momsgruppens representant i stället för myndigheterna. Läs mer [Om momsreturrapporten](finance-how-report-vat.md#vatreturn).

> [!NOTE]
> Momsgruppsmedlemmar kan korrigera inskickade momsreturer så länge som grupprepresentanten inte har släppt momsreturen för gruppen. Om du vill göra en korrigering måste momsgruppsmedlemmen skapa en ny momsretur för momsreturperioden och skicka den till momsgruppens representant. På momsgruppsrepresentantens sida kommer medlemmens senaste momsretur att ersätta den föregående och inkluderas på sidan **Momsretur**.

I följande avsnitt beskrivs uppgifterna som momsgruppsrepresentanter måste utföra för att arkivera momsreturen.

### Granska överföringar från gruppmedlemmar

På sidan **Momsgruppens inlämningar** visas de momsreturer som medlemmar har skickat in. Sidan fungerar som en utkastplats för inskickade objekt tills momsgruppens representant inkluderar dem i en momsretur för gruppen. Representanten kan öppna inlämningarna för att granska de enskilda rutorna som innehåller det belopp som rapporteras av varje momsgruppsmedlem.

> [!TIP]
> På sidan **Perioder för momsretur** visar fältet **Överföringar från gruppmedlemmar** visar hur många deklarationer medlemmar har lämnat. För att säkerställa att detta nummer är uppdaterat, välj åtgärden **Hämta momsretur**.

### Skapa en gruppmomsretur

Om du vill rapportera moms för gruppens räkning skapar du momsretur enbart för ditt företag på sidan **Momsreturer**. I efterhand ska du inkludera de senaste momsinlämningarna från momsgruppsmedlemmar genom att välja åtgärden **Ta med gruppmoms**.  

När gruppsrepresentanten har skickat gruppens moms till myndigheterna kommer representanten normalt att köra åtgärden **Beräkna och bokför momsavräkning**. Denna åtgärd avslutar öppna momstransaktioner och överför belopp till kontot för momsavräkning. Den här åtgärden tar för närvarande inte hänsyn till gruppinlämningar. Endast momstransaktioner för momsgruppsrepresentantens företag bokförs. Momsgruppsmedlemmens inlämningsbelopp måste bokföras med hjälp av åtgärden **Bokföringsgrupp för momsavstämning**.

> [!IMPORTANT]
> Funktionen momsgrupp stöds endast på de marknader där [!INCLUDE[prod_short](includes/prod_short.md)] använder en momsram som består av momsreturer och perioder för momsreturer. Du kan inte använda momsgrupper på andra marknader som har andra implementeringar av lokal momsrapportering, till exempel Österrike, Tyskland, Italien, Spanien och Schweiz.

## Problem med att aktivera multifaktorautentisering (MFA)

Om du får ett felmeddelande relaterat till auktorisering under förnyelsen av **OAuth2-token** på sidan **Momsrapportinställning** när du har aktiverat MFA utför du följande steg.  

1. Logga in på **Azure Portal** som autentiseringsadministratör.  
2. Gå till **Microsoft Entra ID**.   
3. Bläddra till **Användare** och välj sedan den användare du vill utföra en åtgärd.  
4. Välj **Autentiseringsmetoder** och välj **Kräv omregistrering av multifaktorautentisering** högst upp på sidan. 
5. Gå tillbaka till Dynamics 365 Business Central och välj att förnya token från **Momsrapportinställning**.  

Detta bör vara en engångsinställning när du har aktiverat multifaktorautentisering för den användare som valts i **Momsrapportinställning**.  

## Se även

[Storbritannien funktion i brittiska versionen](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Göra skatt digitalt i Storbritannien](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Ställa in moms](finance-setup-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Konsolidera ekonomiska data från flera företag](finance-consolidated-company-reporting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
