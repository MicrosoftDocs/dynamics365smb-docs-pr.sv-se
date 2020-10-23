---
title: Tillägget Momsgruppshantering | Microsoft Docs
description: Du kan samarbeta med andra företag för att skapa en momsgrupp och agera som antingen en medlem av eller representant för gruppen vid rapportering av moms.
author: bholtorf
manager: annbe
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: VAT, value added tax, report
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: 5dfadee976ce39e7d7ead2c09d907050682b4a7f
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989422"
---
# <a name="the-vat-group-management-extension"></a>Tillägget Momsgruppshantering

Du kan koppla ett eller flera företag i ditt land för att konsolidera momsrapportering under ett enda registreringsnummer. Denna typ av ordning kallas *Momsgrupp*. Du kan interagera med gruppen som en medlem av eller representant för gruppen.

## <a name="forming-a-vat-group"></a>Skapa en momsgrupp
Medlemmar i momsgrupper och grupprepresentanten kan använda guiden för assisterad konfiguration av **Momsgruppshantering** för att definiera deras engagemang i gruppen och upprätta en anslutning mellan deras [!INCLUDE[d365fin](includes/d365fin_md.md)]-klientorganisationer. Gruppmedlemmarna kommer att använda anslutningen för att skicka in sina momsreturer till gruppens representant. Representanten kommer att skicka in moms till skattemyndigheter för gruppens räkning med en enda momsretur. 

## <a name="vat-group-constellations"></a>Momsgruppskonstellationer
Kommunikationen sker från gruppmedlemmar till representanten. Grupprepresentanten visar ett API som gör det möjligt för medlemmar att skicka momsreturer till momsgruppens representant. 
[!INCLUDE[d365fin](includes/d365fin_md.md)] stöder momsreturer inom gruppen för företag som använder lokalt eller onlinebaserat [!INCLUDE[d365fin](includes/d365fin_md.md)], och i vilken kombination som helst. Inställningarna för kommunikationen beror på konstellationen. I följande avsnitt beskrivs hur du ställer in olika gruppkonstellationer.

I följande lista visas rekommenderad ordning för hur du lägger upp en momsgrupp:

1. Skapa konfigurationen i Azure Active Directory. Mer information finns i [Krav för autentisering](ui-extensions-vat-group.md#requirements-for-authentication).
2. Dela den tekniska informationen om medlemmar i momsgruppen och representanten måste ansluta sina [!INCLUDE[d365fin](includes/d365fin_md.md)]-klientorganisationer.

  Vanligtvis har momsgruppens representant den här informationen, till exempel namnet på den momsgruppsrepresentantens miljö som momsgruppens medlemmar ska skicka moms till.
3. Skapa användare i momsgruppsrepresentantens [!INCLUDE[d365fin](includes/d365fin_md.md)] som momsgruppens medlemmar kan använda för att autentisera och ansluta.
4. Kör guiden för assisterad konfiguration **Konfigurera Momsgruppshantering** för att ansluta momsgruppens medlemmar.

  Guiden kräver viss information från momsgruppens representant. Mer information finns i avsnittet [Konfigurera momsgruppsmedlem](#vat-group-member-setup). Anteckna **gruppmedlems-ID** för varje momsgruppsmedlem. Representanten behöver dessa ID för att lägga till företagen i momsgruppen.
5. Konfigurera tillägget Momsgruppshantering i momsgruppsrepresentantens [!INCLUDE[d365fin](includes/d365fin_md.md)] med hjälp av guiden för assisterad konfiguration **Konfigurera Momsgruppshantering**. 

> [!NOTE]
> Om gruppmedlemmar vill ansluta till momsgruppens representant behöver de en användare med åtkomst till momsgruppsrepresentantens [!INCLUDE[d365fin](includes/d365fin_md.md)]. Momsgruppens representant måste skapa minst en användare för detta, men av säkerhetsskäl rekommenderar vi att du skapar en användare för varje momsgruppsmedlem. Se till att distribuera autentiseringsuppgifter för dessa användare till momsgruppsmedlemmarna på ett säkert sätt.

## <a name="understanding-the-vat-group-management-setup"></a>Förstå konfigurationen av Momsgruppshantering

Momsgruppens representant visar ett API som momsgruppsmedlemmar kan använda för att ansluta till sin [!INCLUDE[d365fin](includes/d365fin_md.md)]-kientorganisation och skicka in momsreturer. Momsgruppsmedlemmar kan ofta använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i separata Azure Active Directory-klientorganisationer. Därför behövs fler inställningar för att upprätta en anslutning mellan momsgruppsmedlemmen och representantens [!INCLUDE[d365fin](includes/d365fin_md.md)]. 
  
Momsgruppsmedlemmar ansluter till representanten genom att anropa en webbtjänst på momsgruppsrepresentantens klientorganisation. Anroparen måste autentiseras med hjälp av OAuth. När tillägget Momsgruppshantering har konfigurerats ombeds du att autentisera till momsgruppens representant för att hämta och spara ett åtkomsttoken. Detta åtkomsttoken används när momsreturer skickas till en momsgruppsrepresentant. 

Autentiseringen hanteras av Azure Active Directory, så din konfiguration måste genomföras i momsgruppsrepresentantens Azure Active Directory för att tillåta anslutningar. En Azure Active Directory-appregistrering måste konfigureras med åtkomst till momsgruppsrepresentantens [!INCLUDE[d365fin](includes/d365fin_md.md)]. Detta gäller även om momsgruppens representant använder lokalt [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dessutom måste du konfigurera enkel inloggning om momsgruppens representant använder lokalt [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> Under en begränsad tid stöds även autentisering med en åtkomstnyckel till webbtjänster. Mer information finns i [Föråldrade funktioner i utgivningscykel 1 år 2021](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#deprecated-features-in-2021-release-wave-1).

## <a name="requirements-for-authentication"></a>Krav för autentisering 
När momsgruppens representant använder webbaserat eller lokalt [!INCLUDE[d365fin](includes/d365fin_md.md)] kan momsgruppsmedlemmar använda Azure Active Directory för att autentisera när de skickar momsreturer till momsgruppens representant. Om momsgruppsmedlemmarna också använder [!INCLUDE[d365fin](includes/d365fin_md.md)] online kan momsgruppsmedlemmen autentisera med de angivna autentiseringsuppgifterna och slutpunktsinformationen. Mer information finns i [Konfigurera momsgruppsmedlem](ui-extensions-vat-group.md#vat-group-member-setup).

Momsgruppsmedlemmar som har lokalt [!INCLUDE[d365fin](includes/d365fin_md.md)] måste konfigurera en appregistrering i Azure Active Directory för momsgruppsrepresentantens [!INCLUDE[d365fin](includes/d365fin_md.md)]-klientorganisation. Appregistreringen gör att momsgruppsrepresentantens [!INCLUDE[d365fin](includes/d365fin_md.md)] online kan autentisera gruppmedlemmen. Mer information finns i [Snabbstart: registrera ett program med Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app).

När du skapar appregistrering i Azure Active Directory måste du ange följande.

* I avsnittet **Autentisering** lägger du till **Webb** som en plattform och använder följande **omdirigerings-URL**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* I avsnittet **Autentisering**, i alternativet för att välja **Kontotyper som stöds**, väljer du **Konton i organisationens katalog (en Azure AD-katalog – flera klientorganisationer)**.
* I avsnittet **Certifikat och hemligheter** skapar du en ny klienthemlighet och antecknar värdet. Momsgruppsmedlemmarna kommer att behöva hemligheten när de konfigurerar anslutningen till gruppens representant.
* I avsnittet **API-behörigheter** lägger du till behörigheter till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Aktivera delegerad åtkomst till **Financials.ReadWrite.All** och **user_impersonation**.
* I avsnittet **Översikt** antecknar du **Applikation-ID (klient)**. Momsgruppsmedlemmarna kommer att behöva detta ID när de konfigurerar anslutningen till gruppens representant. 

## <a name="vat-group-member-setup"></a>Konfigurera momsgruppsmedlem
Konfigurera momsgruppsmedlemmen genom att starta guiden för assisterad konfiguration **Konfigurera Momsgruppshantering**. 

> [!NOTE]
> Innan du börjar bör du kontakta momsgruppens representant och be om följande information om deras [!INCLUDE[d365fin](includes/d365fin_md.md)]-klientorganisation:
>
> * API-URL
> * Namnet på företaget 
> * Klient-ID
> * Klienthemlighet
> * Inloggningsuppgifter för den dedikerade användaren 

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **momsgrupp** och välj sedan relaterad länk.
2. Om du vill definiera företagets momsgruppsroll väljer du **Medlem** och väljer sedan **Nästa**.
3. Kopiera värdet i fältet **Gruppmedlems-ID** och dela det med momsgruppens representant så att de kan lägga till ditt företag som en godkänd medlem i gruppen.
4. Lägg till **API-URL:en** från momsgruppens representant. URL:en formateras vanligen så här: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Till exempel `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`. 
5. Lägg till [!INCLUDE[d365fin](includes/d365fin_md.md)]-företagsnamnet för momsgruppens representant, till exempel *CRONUS UK Ltd*.
6. Välj **Autentiseringstyp**, välj **OAuth2** och välj sedan **Nästa**.
7. I fältet **Klient-ID** anger du ID för momsgruppens representant.
8. I fältet **Klienthemlighet från momsgruppens representant** anger du den hemlighet som tillhandahålls av momsgruppens representant.
9. I fältet **Slutpunkt för OAuth 2.0-utfärdare** anger du *https://login.microsoftonline.com/common/oauth2*.
10. I fältet **URL för OAuth 2.0-resurs** anger du *https://api.businesscentral.dynamics.com/*.
11. I fältet **Omdirigerings-URL för OAuth 2.0** anger du *https://businesscentral.dynamics.com/OAuthLanding.htm*. 
12. När du har angett de olika fälten väljer du **Nästa** och anger sedan de autentiseringsuppgifter som tillhandahölls av momsgruppens representant.
13. Välj den momsrapportkonfiguration som du använder när du rapporterar moms till myndigheter i ditt land.

  I Storbritannien skulle t.ex. momsrapportkonfigurationen ställas in så att den rapporterar moms till HMRC. Tillägget Momsgruppshantering kopierar den här inställningen, men ersätter den inskickade codeunit med en som stöder inlämning till momsgruppens representant i stället för skattemyndigheterna. Denna codeunit tillhandahålls av Microsoft. Välj **Nästa** när du är klar.

## <a name="using-the-vat-group-management-features"></a>Använda funktionerna för momsgruppshantering

Momsgruppsmedlemmar använder standardprocesser för att förbereda momsreturer. Den enda skillnaden är att välja rapportversionen **VATGROUP**, som skickar momsreturen till momsgruppens representant i stället för myndigheterna. Mer information finns i [Om momsreturrapporten](/business-central/finance-how-report-vat#about-the-vat-return-report).

I följande avsnitt beskrivs uppgifterna som momsgruppsrepresentanter måste utföra.

### <a name="vat-group-submissions"></a>Momsgruppens inlämningar

På sidan **Momsgruppens inlämningar** visas de momsreturer som medlemmar har skickat in. Sidan fungerar som en utkastplats för inskickade objekt tills momsgruppens representant inkluderar dem i en momsretur för gruppen. Du kan öppna inlämningarna för att granska momsen för de enskilda rutorna som rapporteras av momsgruppsmedlemmen.

### <a name="creating-a-group-vat-return"></a>Skapa en gruppmomsretur

Om du vill rapportera moms för gruppens räkning skapar du momsretur enbart för ditt företag på sidan **Momsreturer**. I efterhand ska du inkludera de senaste momsinlämningarna från momsgruppsmedlemmar genom att välja åtgärden **Ta med gruppmoms**.  

När momsgruppsrepresentantens momsretur har skickats till myndigheterna för hela gruppens räkning, kör du normalt åtgärden **Beräkna och bokför momsavräkning**. Denna åtgärd avslutar öppna momstransaktioner och överför belopp till kontot för momsavräkning. Den här åtgärden tar för närvarande inte hänsyn till gruppinlämningar. Det innebär att endast momstransaktioner för momsgruppsrepresentantens företag bokförs. Momsgruppsmedlemmarnas inlämningsbelopp måste bokföras i momsavräkningsbeloppet manuellt, så att momsgruppsrepresentantens momsavräkningskonto återspeglar det ansvar som har rapporterats till myndigheterna. Det här beteendet ändras i en kommande uppdatering av [!INCLUDE[d365fin](includes/d365fin_md.md)], så att hela gruppen moms (totalt belopp på rapportraderna i momsreturen) kvittas. 

> [!NOTE]
> Momsgruppsmedlemmar kan korrigera inskickade momsreturer så länge som grupprepresentanten inte har släppt momsreturen för gruppen. Om du vill göra en korrigering måste momsgruppsmedlemmen skapa en ny momsretur för momsreturperioden och skicka den till momsgruppens representant. På momsgruppsrepresentantens sida kommer den senaste momsreturen att inkluderas på sidan **Momsretur**. 

## <a name="see-also"></a>Se även
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Ställa in moms](finance-setup-vat.md)
