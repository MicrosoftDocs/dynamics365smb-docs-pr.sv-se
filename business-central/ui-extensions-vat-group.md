---
title: Tillägget Momsgruppshantering för Storbritannien
description: Du kan samarbeta med andra företag för att skapa en momsgrupp där alla medlemmar rapporterar moms i en enda retur.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, value added tax, report
ms.search.forms: ''
ms.date: 05/24/2022
ms.author: bholtorf
ms.openlocfilehash: c5757a78a44e3cdc2f6100c42b5105734928837b
ms.sourcegitcommit: 7a6efcbae293c024ca4f6622c82886decf86c176
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/02/2022
ms.locfileid: "8841926"
---
# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>Tillägget Momsgruppshantering för Storbritannien

Du kan ansluta ett eller flera företag i ditt land för att kombinera momsrapportering under ett enda registreringsnummer. Denna typ av ordning kallas *Momsgrupp*. Du kan interagera med gruppen som en medlem av eller representant för gruppen.

## <a name="forming-a-vat-group"></a>Skapa en momsgrupp
Medlemmar i momsgrupper och grupprepresentanten kan använda guiden för assisterad konfiguration av **Momsgruppshantering** för att definiera deras engagemang i gruppen och upprätta en anslutning mellan deras [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisationer. Gruppmedlemmarna kommer att använda anslutningen för att skicka in sina momsreturer till gruppens representant. Representanten kommer att skicka in moms till skattemyndigheter för gruppens räkning med en enda momsretur. 

## <a name="license-requirements"></a>Licenskrav
Deltagare i gruppen måste vara licensierade att använda [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan inte använda gästkonton i momsgrupper. 

* För att beräkna och skicka momsreturer måste användaren vara en fullständig Business Central-användare.
* Om du vill logga in och utföra grundläggande uppgifter, till exempel skapa konton, kan du ha Dynamics 365 Business Central teammedlemslicens.

## <a name="vat-group-constellations"></a>Momsgruppskonstellationer
Kommunikationen sker från gruppmedlemmar till representanten. Grupprepresentanten visar ett API URL som gör det möjligt för medlemmar att skicka momsreturer till momsgruppens representant. 
[!INCLUDE[prod_short](includes/prod_short.md)] stöder momsreturer inom gruppen för företag som använder lokalt eller onlinebaserat [!INCLUDE[prod_short](includes/prod_short.md)], och i vilken kombination som helst. Inställningarna för kommunikationen beror på konstellationen. I den här artikeln beskrivs olika gruppkonstellationer.

I följande lista visas rekommenderad ordning för hur du lägger upp en momsgrupp:

1. Skapa konfigurationen i Azure Active Directory. Mer information finns i [Krav för autentisering](ui-extensions-vat-group.md#requirements-for-authentication).
2. Dela den tekniska informationen om medlemmar i momsgruppen och representanten måste ansluta sina [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisationer. Vanligtvis har momsgruppens representant den här informationen, till exempel namnet på den momsgruppsrepresentantmiljö som momsgruppens medlemmar ska skicka moms till.
3. Skapa användare som VAT-gruppmedlemmar kan använda för att autentisera när de ansluter till momsgrupprepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]. Användarna måste ha fullständiga användarlicenser för [!INCLUDE[prod_short](includes/prod_short.md)].
4. Kör guiden för assisterad konfiguration **Konfigurera Momsgruppshantering** för att ansluta momsgruppens medlemmar.

  Guiden kräver viss information från momsgruppens representant. Mer information finns i [Konfigurera momsgruppsmedlemmar](#set-up-vat-group-members). Anteckna **gruppmedlems-ID** för varje momsgruppsmedlem. Representanten behöver dessa ID för att lägga till företagen i momsgruppen.
5. Konfigurera tillägget Momsgruppshantering i momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)] med hjälp av guiden för assisterad konfiguration **Konfigurera Momsgruppshantering**. 

> [!NOTE]
> Om gruppmedlemmar vill ansluta till momsgruppens representant behöver de en användare med åtkomst till momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]. Momsgruppens representant måste skapa minst en användare för detta, men av säkerhetsskäl rekommenderar vi att du skapar en användare för varje momsgruppsmedlem. Se till att distribuera autentiseringsuppgifter för dessa användare till momsgruppsmedlemmarna på ett säkert sätt. Det här är ett system användar konto som inte är relaterat till en faktisk person.

## <a name="about-the-vat-group-management-setup"></a>Om konfigurationen av Momsgruppshantering

Den representativa momsgrupp som visar ett API för att gruppera medlemmar. Medlemmarna använder API för att ansluta till representantens [!INCLUDE[prod_short](includes/prod_short.md)] innehavare och skicka in momsreturer. Momsgruppsmedlemmar kan ofta använda [!INCLUDE[prod_short](includes/prod_short.md)] i separata Azure Active Directory-klientorganisationer. Därför behövs en inställning för att ansluta momsgruppsmedlemmen och representantens [!INCLUDE[prod_short](includes/prod_short.md)]. 
  
Momsgruppsmedlemmar ansluter till representanten genom att anropa en webbtjänst på momsgruppsrepresentantens klientorganisation. Anroparen måste autentiseras med hjälp av OAuth2. När tillägget Momsgruppshantering har konfigurerats ombeds du att autentisera till momsgruppens representant för att hämta och spara ett åtkomsttoken. Detta åtkomsttoken används när momsreturer skickas till en momsgruppsrepresentant. 

## <a name="construct-the-api-url"></a>Konstruera API-URL
1. I Business Central administratörscenter för representantens klientorganisation väljer du **Miljöer**.
2. I avsnittet **Detaljer** kopiera **URL**.
3. Öppna Anteckningar och klistra in URL-adressen. Ersätt **https://businesscentral.dynamics.com** med **https://api.businesscentral.dynamics.com/v2.0**.

## <a name="requirements-for-authentication"></a>Krav för autentisering 
> [!NOTE]
> Detta kräver autentiseringsuppgifter för en administratörs konto som har fullständig användarlicens för [!INCLUDE[prod_short](includes/prod_short.md)].

När momsgruppens representant använder webbaserat eller lokalt [!INCLUDE[prod_short](includes/prod_short.md)] måste momsgruppsmedlemmar använda Azure Active Directory för att autentisera användare när de skickar momsreturer till momsgruppens representant. För [!INCLUDE[prod_short](includes/prod_short.md)] lokal måste medlemmar konfigurera enkel inloggning. Mer information finns i [Konfigurera Azure Active Directory autentisering med WS-Federation](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool). Om momsgruppsmedlemmarna också använder [!INCLUDE[prod_short](includes/prod_short.md)] online kan momsgruppsmedlemmen autentisera med de angivna autentiseringsuppgifterna och slutpunktsinformationen. Mer information finns i [Konfigurera momsgruppsmedlemmar](ui-extensions-vat-group.md#set-up-vat-group-members).

Momsgruppsmedlemmar som har lokalt [!INCLUDE[prod_short](includes/prod_short.md)] måste konfigurera en appregistrering i Azure Active Directory för momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisation. Appregistreringen gör att momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)] online kan autentisera gruppmedlemmen. Mer information finns i [Snabbstart: registrera ett program med Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app).

När du skapar appregistrering i Azure Active Directory måste du ange följande information.

* I avsnittet **Autentisering** lägger du till **Webb** som en plattform och använder följande **omdirigerings-URL**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* I avsnittet **Autentisering**, i alternativet för att välja **Kontotyper som stöds**, väljer du **Konton i organisationens katalog (en Azure AD-katalog – flera klientorganisationer)**.
* I avsnittet **Certifikat och hemligheter** skapar du en ny klienthemlighet och antecknar värdet. Momsgruppsmedlemmarna kommer att behöva hemligheten när de konfigurerar anslutningen till gruppens representant.
* I avsnittet **API-behörigheter** lägger du till behörigheter till [!INCLUDE[prod_short](includes/prod_short.md)]. Aktivera delegerad åtkomst till **Financials.ReadWrite.All** och **user_impersonation**.
* I avsnittet **Översikt** antecknar du **Applikation-ID (klient)**. Momsgruppsmedlemmarna kommer att behöva detta ID när de konfigurerar anslutningen till gruppens representant. 

## <a name="set-up-vat-group-members"></a>Ställ in medlemmar i momsgruppen
> [!IMPORTANT]
> Medlemsföretagen i momsgruppen behöver inte ansluta till HMRC eftersom de rapporterar via gruppens representant.

Innan du börjar bör du kontakta momsgruppens representant och be om följande information om deras [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisation:

* API-URL
* Namnet på företaget 
* Klient-ID
* Klienthemlighet
* Inloggningsuppgifter för den dedikerade användaren 

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Konfigurera hantering av momsgrupper** och väljer sedan relaterad länk.
2. I fältet **Roll för momsgrupp**, ange om du är medlem i gruppen eller gruppens representant. Välj **Medlem** om du vill fungera som en gruppmedlem och skicka momsreturer till grupprepresentanten i stället för till skattemyndigheten och väljer sedan **Nästa**.
3. Kopiera värdet i fältet **Gruppmedlems-ID** och dela det med momsgruppens representant så att de kan lägga till ditt företag som en godkänd medlem i gruppen.
4. I fältet **Grupprepresentantens produktversion** anger du den version av [!INCLUDE[prod_short](includes/prod_short.md)] som representanten använder.
5. I fältet **Grupprepresentantens företag**, ange företagsnamnet för momsgruppens representant. Till exempel, **CRONUS UK Ltd**.
6. I fältet **Autentiseringstyp**, välj alternativet för **OAuth2**. Om momsgruppens representant använder [!INCLUDE[prod_short](includes/prod_short.md)] online, ange **Grupprepresentant som använder Business Central Online** och välj sedan **Nästa**. Beroende på om representanten använder [!INCLUDE[prod_short](includes/prod_short.md)] online eller lokal följer du dessa steg i avsnitten [Momsgruppsrepresentant använder Business Central Online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) eller [Momsgruppsrepresentant använder Business Central lokalt](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premesis).

### <a name="vat-group-representative-uses-business-central-online"></a>Momsgrupprepresentant som använder Business Central Online
1. Ange de användarautentiseringsuppgifter som angavs av momsgruppens representant och lägg till de behörigheter som krävs.
2. Välj den konfiguration för momsrapport som för närvarande används för att skicka momsreturer till skattemyndigheterna. När du är klar med inställningarna kommer [!INCLUDE[prod_short](includes/prod_short.md)] att skapa en ny konfiguration baserat på det här alternativet och använder konfigurationen för att skicka momsreturer till momsgruppens representant.  
3. Lägg till **API-URL:en** från momsgruppens representant. URL:en formateras vanligen så här: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Till exempel `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.

### <a name="vat-group-representative-uses-business-central-on-premesis"></a>Momsgrupprepresentant som använder Business Central lokal
1. I fältet **klient-ID** anger du klient-ID:t från programregistreringen i Azure Active Directory.
2. I fältet **klienthemlighet** anger du klienthemligheten från programregistreringen i Azure Active Directory.
3. I fältet **OAuth 2.0-utfärdare** anger du `https://login.microsoftonline.com/common/oauth2`.
4. I fältet **URL för OAuth 2.0-resurs** anger du `https://api.businesscentral.dynamics.com/`.
5. I fältet **Omdirigerings-URL för OAuth 2.0** anger du `https://businesscentral.dynamics.com/OAuthLanding.htm`.
6. När du har angett de olika fälten väljer du **Nästa** och anger sedan de autentiseringsuppgifter som tillhandahölls av momsgruppens representant.
7. Välj den momsrapportkonfiguration som du använder när du rapporterar moms till myndigheter i ditt land.

## <a name="set-up-the-vat-group-representative"></a>Skapa en momsgruppsrepresentant
> [!NOTE]
> För lokal stöder vi bara en enskild innehavare av representant för gruppen.

> [!IMPORTANT]
> Representantföretaget måste aktivera **HMRC momsinställningar** på sidan **Tjänstanslutningar**. Representanter måste också hämta momsreturperioder från HMRC.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Konfigurera hantering av momsgrupper** och väljer sedan relaterad länk.
2. I fältet **Roll för momsgrupp**, ange om du är medlem i gruppen eller gruppens representant. Välj **Representant** om du vill fungera som en momsgrupps representant och skicka momsreturer till gruppens skattemyndighet och väljer sedan **Nästa**.
3. I fältet **Momsavräkningskonto** anger du det konto som du använder för momsavräkningar.
4. I rutan **Rutnummer för moms att betala** anger du rutan som representerar det totala återstående momsbeloppet från en momsgruppsinlämning.
5. I fältet **Redovisningsjournalmall för gruppavräkning** anger du den allmänna journalmall som används för dokumentet för att bokföra gruppmomsen på avräkningskontot.
6. I fältet **godkända medlemmar** visas det antal gruppmedlemmar som har ställts in för att skicka momsreturer till representanten. Om du vill lägga till nya medlemmar väljer du numret för att öppna sidan **Godkända medlemmar**.
7. Om du vill lägga till nya medlemmar lägger du till följande information på sidan **Godkända medlemmar för momsgrupp**:
    1. I fältet **Gruppmedlems-ID** anger du en identifierare för gruppmedlemmen.
    2. I fältet **Gruppmedlemsnamn**, ange namnet på gruppmedlemmen. 
    3. I fältet **Företag**, ange från vilket företag gruppmedlemmen ska lämna momsdeklarationer i [!INCLUDE[prod_short](includes/prod_short.md)]. Till exempel, **CRONUS UK Ltd**.
    4. Ange företagets kontaktinformation.

## <a name="use-the-vat-group-management-features"></a>Använda funktionerna för momsgruppshantering
Momsgruppsmedlemmar använder standardprocesser för att förbereda momsreturer. Den enda skillnaden är att välja rapportversionen **VATGROUP**, som skickar momsreturen till momsgruppens representant i stället för myndigheterna. Mer information finns i [Om momsreturrapporter](finance-how-report-vat.md#vatreturn).

I följande avsnitt beskrivs uppgifterna som momsgruppsrepresentanter måste utföra.

### <a name="vat-group-submissions"></a>Momsgruppens inlämningar

På sidan **Momsgruppens inlämningar** visas de momsreturer som medlemmar har skickat in. Sidan fungerar som en utkastplats för inskickade objekt tills momsgruppens representant inkluderar dem i en momsretur för gruppen. Du kan öppna inlämningarna för att granska momsen för de enskilda rutorna som rapporteras av momsgruppsmedlemmen. 

> [!TIP]
> På sidan **Perioder för momsretur** visar fältet **Överföringar från gruppmedlemmar** visar hur många deklarationer medlemmar har lämnat. För att säkerställa att detta nummer är uppdaterat, välj åtgärden **Hämta momsretur**.

### <a name="creating-a-group-vat-return"></a>Skapa en gruppmomsretur

Om du vill rapportera moms för gruppens räkning skapar du momsretur enbart för ditt företag på sidan **Momsreturer**. I efterhand ska du inkludera de senaste momsinlämningarna från momsgruppsmedlemmar genom att välja åtgärden **Ta med gruppmoms**.  

När momsgruppsrepresentantens momsretur har skickats till myndigheterna för hela gruppens räkning, kör du normalt åtgärden **Beräkna och bokför momsavräkning**. Denna åtgärd avslutar öppna momstransaktioner och överför belopp till kontot för momsavräkning. Den här åtgärden tar för närvarande inte hänsyn till gruppinlämningar. <!--Has this changed?--> Endast momstransaktioner för momsgruppsrepresentantens företag bokförs. Momsgruppsmedlemmarnas inlämningsbelopp måste bokföras i momsavräkningsbeloppet manuellt, så att momsgruppsrepresentantens momsavräkningskonto återspeglar det ansvar som har rapporterats till myndigheterna. Det här beteendet ändras i en kommande uppdatering av [!INCLUDE[prod_short](includes/prod_short.md)], så att hela gruppen moms (totalt belopp på rapportraderna i momsreturen) kvittas. <!--Has this behavior changed?-->

> [!NOTE]
> Momsgruppsmedlemmar kan korrigera inskickade momsreturer så länge som grupprepresentanten inte har släppt momsreturen för gruppen. Om du vill göra en korrigering måste momsgruppsmedlemmen skapa en ny momsretur för momsreturperioden och skicka den till momsgruppens representant. På momsgruppsrepresentantens sida kommer den senaste momsreturen att inkluderas på sidan **Momsretur**. 

> [!IMPORTANT]
> Funktionen momsgrupp stöds endast på de marknader där [!INCLUDE[prod_short](includes/prod_short.md)] använder en momsram som består av momsreturer och perioder för momsreturer. Du kan inte använda momsgrupper på andra marknader som har andra implementeringar av lokal momsrapportering, till exempel Österrike, Tyskland, Italien, Spanien och Schweiz. 

## <a name="see-also"></a>Se även
[Storbritannien funktion i brittiska versionen](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Göra skatt digitalt i Storbritannien](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Ställa in moms](finance-setup-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
