---
title: Tillägget Momsgruppshantering
description: Du kan samarbeta med andra företag för att skapa en momsgrupp och agera som antingen en medlem av eller representant för gruppen vid rapportering av moms.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: VAT, value added tax, report
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: f385cd6dc2186a2e492eb7c045639ec34185237c
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8382563"
---
# <a name="the-vat-group-management-extension"></a>Tillägget Momsgruppshantering

Du kan koppla ett eller flera företag i ditt land för att konsolidera momsrapportering under ett enda registreringsnummer. Denna typ av ordning kallas *Momsgrupp*. Du kan interagera med gruppen som en medlem av eller representant för gruppen.

## <a name="forming-a-vat-group"></a>Skapa en momsgrupp
Medlemmar i momsgrupper och grupprepresentanten kan använda guiden för assisterad konfiguration av **Momsgruppshantering** för att definiera deras engagemang i gruppen och upprätta en anslutning mellan deras [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisationer. Gruppmedlemmarna kommer att använda anslutningen för att skicka in sina momsreturer till gruppens representant. Representanten kommer att skicka in moms till skattemyndigheter för gruppens räkning med en enda momsretur. 

## <a name="vat-group-constellations"></a>Momsgruppskonstellationer
Kommunikationen sker från gruppmedlemmar till representanten. Grupprepresentanten visar ett API som gör det möjligt för medlemmar att skicka momsreturer till momsgruppens representant. 
[!INCLUDE[prod_short](includes/prod_short.md)] stöder momsreturer inom gruppen för företag som använder lokalt eller onlinebaserat [!INCLUDE[prod_short](includes/prod_short.md)], och i vilken kombination som helst. Inställningarna för kommunikationen beror på konstellationen. I följande avsnitt beskrivs hur du ställer in olika gruppkonstellationer.

I följande lista visas rekommenderad ordning för hur du lägger upp en momsgrupp:

1. Skapa konfigurationen i Azure Active Directory. Mer information finns i [Krav för autentisering](ui-extensions-vat-group.md#requirements-for-authentication).
2. Dela den tekniska informationen om medlemmar i momsgruppen och representanten måste ansluta sina [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisationer. Vanligtvis har momsgruppens representant den här informationen, till exempel namnet på den momsgruppsrepresentantmiljö som momsgruppens medlemmar ska skicka moms till.
3. Skapa användare i momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)] som momsgruppens medlemmar kan använda för att autentisera och ansluta.
4. Kör guiden för assisterad konfiguration **Konfigurera Momsgruppshantering** för att ansluta momsgruppens medlemmar.

  Guiden kräver viss information från momsgruppens representant. Mer information finns i avsnittet [Konfigurera momsgruppsmedlem](#vat-group-member-setup). Anteckna **gruppmedlems-ID** för varje momsgruppsmedlem. Representanten behöver dessa ID för att lägga till företagen i momsgruppen.
5. Konfigurera tillägget Momsgruppshantering i momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)] med hjälp av guiden för assisterad konfiguration **Konfigurera Momsgruppshantering**. 

> [!NOTE]
> Om gruppmedlemmar vill ansluta till momsgruppens representant behöver de en användare med åtkomst till momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]. Momsgruppens representant måste skapa minst en användare för detta, men av säkerhetsskäl rekommenderar vi att du skapar en användare för varje momsgruppsmedlem. Se till att distribuera autentiseringsuppgifter för dessa användare till momsgruppsmedlemmarna på ett säkert sätt.

## <a name="understanding-the-vat-group-management-setup"></a>Förstå konfigurationen av Momsgruppshantering

Momsgruppens representant visar ett API som momsgruppsmedlemmar kan använda för att ansluta till sin [!INCLUDE[prod_short](includes/prod_short.md)]-kientorganisation och skicka in momsreturer. Momsgruppsmedlemmar kan ofta använda [!INCLUDE[prod_short](includes/prod_short.md)] i separata Azure Active Directory-klientorganisationer. Därför behövs fler inställningar för att upprätta en anslutning mellan momsgruppsmedlemmen och representantens [!INCLUDE[prod_short](includes/prod_short.md)]. 
  
Momsgruppsmedlemmar ansluter till representanten genom att anropa en webbtjänst på momsgruppsrepresentantens klientorganisation. Anroparen måste autentiseras med hjälp av OAuth. När tillägget Momsgruppshantering har konfigurerats ombeds du att autentisera till momsgruppens representant för att hämta och spara ett åtkomsttoken. Detta åtkomsttoken används när momsreturer skickas till en momsgruppsrepresentant. 

Autentiseringen hanteras av Azure Active Directory, så din konfiguration måste genomföras i momsgruppsrepresentantens Azure Active Directory för att tillåta anslutningar. En Azure Active Directory-appregistrering måste konfigureras med åtkomst till momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]. Detta gäller även om momsgruppens representant använder lokalt [!INCLUDE[prod_short](includes/prod_short.md)]. Dessutom måste du konfigurera enkel inloggning om momsgruppens representant använder lokalt [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Under en begränsad tid stöds även autentisering med en åtkomstnyckel till webbtjänster. Mer information finns i [Föråldrade funktioner i utgivningscykel 1 år 2021](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#deprecated-features-in-2021-release-wave-1).

## <a name="requirements-for-authentication"></a>Krav för autentisering 
När momsgruppens representant använder webbaserat eller lokalt [!INCLUDE[prod_short](includes/prod_short.md)] kan momsgruppsmedlemmar använda Azure Active Directory för att autentisera när de skickar momsreturer till momsgruppens representant. Om momsgruppsmedlemmarna också använder [!INCLUDE[prod_short](includes/prod_short.md)] online kan momsgruppsmedlemmen autentisera med de angivna autentiseringsuppgifterna och slutpunktsinformationen. Mer information finns i [Konfigurera momsgruppsmedlem](ui-extensions-vat-group.md#vat-group-member-setup).

Momsgruppsmedlemmar som har lokalt [!INCLUDE[prod_short](includes/prod_short.md)] måste konfigurera en appregistrering i Azure Active Directory för momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisation. Appregistreringen gör att momsgruppsrepresentantens [!INCLUDE[prod_short](includes/prod_short.md)] online kan autentisera gruppmedlemmen. Mer information finns i [Snabbstart: registrera ett program med Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app).

När du skapar appregistrering i Azure Active Directory måste du ange följande.

* I avsnittet **Autentisering** lägger du till **Webb** som en plattform och använder följande **omdirigerings-URL**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* I avsnittet **Autentisering**, i alternativet för att välja **Kontotyper som stöds**, väljer du **Konton i organisationens katalog (en Azure AD-katalog – flera klientorganisationer)**.
* I avsnittet **Certifikat och hemligheter** skapar du en ny klienthemlighet och antecknar värdet. Momsgruppsmedlemmarna kommer att behöva hemligheten när de konfigurerar anslutningen till gruppens representant.
* I avsnittet **API-behörigheter** lägger du till behörigheter till [!INCLUDE[prod_short](includes/prod_short.md)]. Aktivera delegerad åtkomst till **Financials.ReadWrite.All** och **user_impersonation**.
* I avsnittet **Översikt** antecknar du **Applikation-ID (klient)**. Momsgruppsmedlemmarna kommer att behöva detta ID när de konfigurerar anslutningen till gruppens representant. 

## <a name="vat-group-member-setup"></a>Konfigurera momsgruppsmedlem
Konfigurera momsgruppsmedlemmen genom att starta guiden för assisterad konfiguration **Konfigurera Momsgruppshantering**. 

> [!NOTE]
> Innan du börjar bör du kontakta momsgruppens representant och be om följande information om deras [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisation:
>
> * API-URL
> * Namnet på företaget 
> * Klient-ID
> * Klienthemlighet
> * Inloggningsuppgifter för den dedikerade användaren 

1. Om du vill definiera företagets momsgruppsroll väljer du **Medlem** och väljer sedan **Nästa**.
2. Kopiera värdet i fältet **Gruppmedlems-ID** och dela det med momsgruppens representant så att de kan lägga till ditt företag som en godkänd medlem i gruppen.
3. Lägg till **API-URL:en** från momsgruppens representant. URL:en formateras vanligen så här: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Till exempel `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`. 
4. Lägg till [!INCLUDE[prod_short](includes/prod_short.md)]-företagsnamnet för momsgruppens representant, till exempel *CRONUS UK Ltd*.
5. Välj **Autentiseringstyp**, välj **OAuth2** och välj sedan **Nästa**.
6. I fältet **Klient-ID** anger du ID för momsgruppens representant.
7. I fältet **Klienthemlighet från momsgruppens representant** anger du den hemlighet som tillhandahålls av momsgruppens representant.
8. I fältet **OAuth 2.0-utfärdare** anger du `https://login.microsoftonline.com/common/oauth2`.
9. I fältet **URL för OAuth 2.0-resurs** anger du `https://api.businesscentral.dynamics.com/`.
10. I fältet **Omdirigerings-URL för OAuth 2.0** anger du `https://businesscentral.dynamics.com/OAuthLanding.htm`. 
11. När du har angett de olika fälten väljer du **Nästa** och anger sedan de autentiseringsuppgifter som tillhandahölls av momsgruppens representant.
12. Välj den momsrapportkonfiguration som du använder när du rapporterar moms till myndigheter i ditt land.

  I Storbritannien skulle t. ex. momsrapportkonfigurationen ställas in så att den rapporterar moms till HMRC. Tillägget Momsgruppshantering kopierar den här inställningen, men ersätter den inskickade codeunit med en som stöder inlämning till momsgruppens representant i stället för skattemyndigheterna. Denna codeunit tillhandahålls av Microsoft. Välj **Nästa** när du är klar.

## <a name="using-the-vat-group-management-features"></a>Använda funktionerna för momsgruppshantering

Momsgruppsmedlemmar använder standardprocesser för att förbereda momsreturer. Den enda skillnaden är att välja rapportversionen **VATGROUP**, som skickar momsreturen till momsgruppens representant i stället för myndigheterna. Mer information finns i [Om momsreturrapporter](finance-how-report-vat.md#vatreturn).

I följande avsnitt beskrivs uppgifterna som momsgruppsrepresentanter måste utföra.

### <a name="vat-group-submissions"></a>Momsgruppens inlämningar

På sidan **Momsgruppens inlämningar** visas de momsreturer som medlemmar har skickat in. Sidan fungerar som en utkastplats för inskickade objekt tills momsgruppens representant inkluderar dem i en momsretur för gruppen. Du kan öppna inlämningarna för att granska momsen för de enskilda rutorna som rapporteras av momsgruppsmedlemmen.

### <a name="creating-a-group-vat-return"></a>Skapa en gruppmomsretur

Om du vill rapportera moms för gruppens räkning skapar du momsretur enbart för ditt företag på sidan **Momsreturer**. I efterhand ska du inkludera de senaste momsinlämningarna från momsgruppsmedlemmar genom att välja åtgärden **Ta med gruppmoms**.  

När momsgruppsrepresentantens momsretur har skickats till myndigheterna för hela gruppens räkning, kör du normalt åtgärden **Beräkna och bokför momsavräkning**. Denna åtgärd avslutar öppna momstransaktioner och överför belopp till kontot för momsavräkning. Den här åtgärden tar för närvarande inte hänsyn till gruppinlämningar. Det innebär att endast momstransaktioner för momsgruppsrepresentantens företag bokförs. Momsgruppsmedlemmarnas inlämningsbelopp måste bokföras i momsavräkningsbeloppet manuellt, så att momsgruppsrepresentantens momsavräkningskonto återspeglar det ansvar som har rapporterats till myndigheterna. Det här beteendet ändras i en kommande uppdatering av [!INCLUDE[prod_short](includes/prod_short.md)], så att hela gruppen moms (totalt belopp på rapportraderna i momsreturen) kvittas. 

> [!NOTE]
> Momsgruppsmedlemmar kan korrigera inskickade momsreturer så länge som grupprepresentanten inte har släppt momsreturen för gruppen. Om du vill göra en korrigering måste momsgruppsmedlemmen skapa en ny momsretur för momsreturperioden och skicka den till momsgruppens representant. På momsgruppsrepresentantens sida kommer den senaste momsreturen att inkluderas på sidan **Momsretur**. 

> [!IMPORTANT]
> Funktionen momsgrupp stöds endast på de marknader där [!INCLUDE[prod_short](includes/prod_short.md)] använder en momsram som består av momsreturer och perioder för momsreturer. Du kan inte använda momsgrupper på andra marknader som har andra implementeringar av lokal momsrapportering, till exempel Österrike, Tyskland, Italien, Spanien och Schweiz. 

## <a name="see-also"></a>Se även

[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Ställa in moms](finance-setup-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Göra skatt digitalt i Storbritannien](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Norsk momsrapportering i norska versionen](LocalFunctionality/Norway/norwegian-vat-reporting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
