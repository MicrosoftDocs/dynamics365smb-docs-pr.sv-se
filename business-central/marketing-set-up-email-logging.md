---
title: Ställa in e-postloggning | Microsoft Docs
description: Lär dig hur du kan omvandla e-postinteraktioner mellan säljare och kunder till verkliga affärsmöjligheter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 5c46fc5107413c4b00b7283e29a75d835de5434e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777679"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Spåra utbyte av e-postmeddelanden mellan säljare och kontakter

Få ut mer av kommunikationen mellan säljare och dina befintliga eller potentiella kunder genom att följa upp e-postutbyten och sedan omvandla dem till olika affärsmöjligheter. [!INCLUDE[prod_short](includes/prod_short.md)] kan tillsammans med Exchange Online spara en logg över de inkommande och utgående meddelandena. Du kan visa och analysera innehållet i varje meddelande på sidan **Interaktionslogg**.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Konfigurera gemensamma mappar och regler för e-postloggning i Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Därefter ansluter du [!INCLUDE[prod_short](includes/prod_short.md)] med Exchange Online.

## <a name="setting-up-prod_short-to-log-email-messages"></a>Ställa in [!INCLUDE[prod_short](includes/prod_short.md)] för att logga e-postmeddelanden

Kom igång med e-postloggning i två enkla steg:

1. Anslut [!INCLUDE[prod_short](includes/prod_short.md)] till Exchange Online för din Microsoft 365-prenumeration. Exchange Online hanterar dina e-postmeddelanden. Detta steg är enkelt att utföra med hjälp av en guide för assisterad konfiguration. Du behöver bara ha administratörsbehörigheter för ditt administratörskonto i Microsoft 365. Du startar guiden genom att gå till **Assisterad konfiguration** och sedan välja **Konfigurera e-postloggning**.  

2. Kontrollera att du har angett giltiga e-postadresser i [!INCLUDE[prod_short](includes/prod_short.md)] för dina säljare och kontakter, beroende på om de är potentiella eller befintliga kunder. Det gör du genom att för varje kund eller säljare öppna kortet **Kontakt** eller **Säljare/Inköpare** och titta i fältet **E-post**.

> [!Tip]
> När du har slutfört stegen i guiden kan du kontrollera om kopplingen har lyckats. Sök efter **Marknadsföringsinställningar**, välj **Process**, sedan **Funktioner** och därefter **Validera konfiguration för e-postloggning**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Visa e-postutbyten i interaktionsloggen
[!INCLUDE[prod_short](includes/prod_short.md)] skapar en transaktion på sidan **Interaktionslogg** varje gång en säljare och en kontakt utbyter e-postmeddelanden. Om du vill visa interaktionsloggen öppnar du kortet **Kontakt** eller **Säljare/Inköpare** för den personen och väljer sedan **Historik** och därefter **Interaktionslogg**. Det finns några saker som du kan göra med posterna i loggen, till exempel:

- Visa innehållet i e-postmeddelandet som utbytts genom att klicka på åtgärden **Visa bilagor**.
- Omvandla ett e-postutbyte till en affärsmöjlighet – Om en transaktion verkar lovande kan du omvandla den till en affärsmöjlighet och sedan hantera förloppet fram till en försäljning. Välj posten och välj sedan åtgärden **Skapa affärsmöjlighet**. Mer information finns i [Hantera försäljningsmöjligheter](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>Ansluta lokala versioner till Microsoft Exchange
Du kan ansluta [!INCLUDE[prod_short](includes/prod_short.md)] lokalt till Exchange lokalt eller Exchange Online för e-postloggning. För båda versioner av Exchange finns inställningar för anslutningen tillgängliga på sidan **Marknadsföringsinställning**. För Exchange Online kan du också använda en assisterad konfigurationsguide. 

### <a name="connecting-to-exchange-on-premises"></a>Ansluta till Exchange lokalt
För att ansluta till [!INCLUDE[prod_short](includes/prod_short.md)] lokalt till Exchange lokalt kan du på sidan **Marknadsföringsinställning** använda **Basic** som **Autentiseringstyp** och sedan ange autentiseringsuppgifter för användarkontot för Exchange lokalt. Slå sedan på brytaren **Aktiverad** för att starta loggningen av e-post. 

### <a name="connecting-to-exchange-online"></a>Ansluta till Exchange Online
Om du vill ansluta till Exchange Online måste du använda **OAuth2** som **Autentiseringstyp**. Du måste även registrera ett program i Azure Active Directory och tillhandahålla programmets ID, nyckelvalvshemlighet samt vilken omdirigerings-URL som ska användas. URL-adressen för omdirigering fylls i förväg och bör användas för de flesta installationer. Mer information finns i [Så här registrerar du ett program Azure AD för anslutning från Business Central till Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Du måste ställa in installationen för att använda HTTPS. Mer information finns i [Konfigurera SSL för att skydda anslutningen till Business Central webbklienten](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Om du konfigurerar servern så att den får en annan startsida kan du alltid ändra URL-adressen. Klientens hemlighet kommer att sparas som en krypterad sträng i databasen.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Så här registrerar du ett program i Azure AD för att ansluta från Business Central till Exchange Online
Följande åtgärder förutsätter att du använder Azure Active Directory för att hantera identiteter och åtkomst. Mer information finns i [Snabbstart: registrera ett program med Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). Om du inte använder Azure Active Directory, se [använda en annan identitets- och åtkomsthanteringstjänst](marketing-set-up-email-logging.md#using-another-identity-and-access-management-service). 

1. I Azure Portal, under **Hantera**, väljer du **Autentisering**.
2. Under **Omdirigerings-URL** lägger du till den omdirigerings-URL som anges på sidan **Marknadsföringsinställning** i [!INCLUDE[prod_short](includes/prod_short.md)]. Om omdirigeringsadressen (URL) på sidan Marknadsföringsinställning är tom hittar du den föreslagna omdirigeringsadressen på sidan **Assisterad konfiguration för e-postloggning**.

    > [!NOTE]
    > Om du inte anger omdirigerings-URL:en kan du göra det senare genom att välja **Lägg till en plattform** och sedan välja **Webb** för att lägga till webb-appen och omdirigeringsadressen. 

3. Under **Hantera** väljer du **Manifest**.
4. Leta reda på egenskapen **requiredResourceAccess** i manifestet och lägg till följande kod i hakparenteserna ([]) för att lägga till de behörigheter som krävs. Mer information finns i [Registrera ditt program](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth#register-your-application).

```
{
    "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    "resourceAccess": [
        {
            "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
            "type": "Scope"
        },
        {
            "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
            "type": "Role"
        }
    ]
}
```

5. Välj **Spara**.
6. Under **Hantera** väljer du **API-behörigheter** och bekräftar sedan att följande behörigheter anges:  

    * EWS.AccessAsUser.All
    * full_access_as_app

7. Under **Hantera**, välj **Certifikat och hemligheter** och skapa sedan en ny hemlighet för ditt program. Du måste ange hemligheten antingen i [!INCLUDE[prod_short](includes/prod_short.md)], i fältet **Klienthemlighet** på sidan **Marknadsföringsinställning**, eller lagrar den på en säker plats och tillhandahåller den i en händelseprenumeration.
8. Välj **Översikt** och leta sedan reda på **App (klient-ID)**-värdet. Detta är klient-ID:t för ditt program. Du måste ange det antingen på **sidan för marknadsföringsinställning**, i fältet **Klient-ID**, eller lagra det på en säker plats och tillhandahålla den i en händelseprenumeration.
9. I [!INCLUDE[prod_short](includes/prod_short.md)] konfigurerar du e-postloggning på sidan **Marknadsföringsinställning** eller använder guiden **Assisterad konfiguration för e-postloggning** för att få hjälp med processen.
    * Ange användarens e-postkonto å dens vägnar för vilken det schemalagda jobbet ska ansluta till Exchange Online och bearbeta e-postmeddelanden. Användaren måste ha en giltig licens för Exchange Online.
    * Tillhandahålla webbadressen (URL) för ditt Exchange Online. Vanligtvis är detta den domän som du angav i användarens e-postadress.
    * Tillhandahåll **Sökväg till kömapp** och **Sökväg för lagringsmapp**.
10. Aktivera brytaren **Aktiverad** för att börja logga e-post.
11. Logga in med ditt administratörskonto för Azure Active Directory (detta konto måste ha en giltig licens för Exchange och vara administratör i ditt Exchange Online). När du har loggat in kommer du att uppmanas att tillåta att ditt registrerade program loggar in Exchange Online på ditt företags vägnar. Du måste ange ett medgivande för att slutföra installationen.

   > [!NOTE]
   > Om du inte uppmanas att logga in med ditt administratörskonto beror detta förmodligen på att popup-fönster blockeras. Du kan logga in med popup-fönster från https://login.microsoftonline.com.

### <a name="using-another-identity-and-access-management-service"></a>Använda en annan identitets- och åtkomsthanteringstjänst
Om du inte använder Azure Active Directory för att hantera identiteter och åtkomst behöver du en viss hjälp från en utvecklare. Om du hellre vill lagra program-ID och hemlighet på en annan plats kan du lämna fälten klient-ID och klienthemlighet tomma och skriva ett tillägg för att hämta ID och hemlighet från platsen. Du kan tillhandahålla hemligheten i samband med körning genom att prenumerera på händelserna OnGetEmailLoggingClientId och OnGetEmailLoggingClientSecret i codeunit 1641, "Konfigurera e-postloggning".

### <a name="to-stop-logging-email"></a>Så här slutar du logga e-post
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Marknadsföringsinställningar** och välj sedan relaterad länk.
2. Stäng av brytaren **Aktiverad**.

## <a name="see-also"></a>Se även
[Hantera relationer](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]