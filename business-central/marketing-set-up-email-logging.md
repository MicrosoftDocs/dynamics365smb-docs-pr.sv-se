---
title: Konfigurera e-postloggning
description: Lär dig hur du kan omvandla e-postinteraktioner mellan säljare och kunder till verkliga affärsmöjligheter.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 03/22/2022
ms.search.form: 1680, 1811, 5076
ms.author: bholtorf
ms.openlocfilehash: fc755362a5b29cca9eb8e8e403374e173cff3630
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516141"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Spåra utbyte av e-postmeddelanden mellan säljare och kontakter
Få ut mer av kommunikationen mellan dina säljare och kunder genom att förvandla e-postutbyten till praktiska möjligheter. [!INCLUDE[prod_short](includes/prod_short.md)] kan tillsammans med Exchange Online spara en logg över de inkommande och utgående meddelandena. Du kan visa och analysera innehållet i varje meddelande på sidan **Interaktionslogg**.

> [!NOTE]
> I 2022 utgivningscykel 1 har vi strömlinjeformat processer för att konfigurera e-postloggning för att öka flexibiliteten och säkerheten. Om du är en ny kund som använder den versionen använder du den nya upplevelsen. Om du är en befintlig kund vilar din användning av den nya versionen på om administratören har aktiverat funktionsuppdateringen **E-postloggning med Microsoft Graph API** i **Funktionshantering**. Mer information finns i [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management).

> [!IMPORTANT]
> För [!INCLUDE[prod_short](includes/prod_short.md)] online kräver den nya erfarenheten att [!INCLUDE[prod_short](includes/prod_short.md)] och Exchange Online finns i samma klientorganisation.

## <a name="to-set-up-email-logging"></a>Så här konfigurerar du e-postloggning
Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **E-postloggning med Microsoft Graph API**. Om funktionsuppdateringen inte är aktiverad följer du anvisningarna på fliken **Aktuell upplevelse**.

## <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience)

### <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Konfigurera gemensamma mappar och regler för e-postloggning i Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Därefter ansluter du [!INCLUDE[prod_short](includes/prod_short.md)] med Exchange Online.

## <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience)
### <a name="set-up-a-shared-mailbox-and-rules-for-email-logging-in-exchange-online"></a>Konfigurera en delad brevlåda och regler för e-postinloggning i Exchange Online

> [!NOTE]
> För dessa åtgärder krävs administratörsåtkomst för Exchange Online.

Förbered en delad postlåda i Exchange administrationscenter. Du kan också använda Exchange Online PowerShell. Mer information finns i [skapa en delad postlåda](/microsoft-365/admin/email/create-a-shared-mailbox) eller [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Om du använder Exchange Management PowerShell är dina ändringar tillgängliga i Exchange administrationscenter efter en fördröjning. Förseningen kan vara i flera timmar.

### <a name="add-a-user-account-for-members-of-the-shared-mailbox"></a>Lägga till ett användarkonto för medlemmar i den delade postlådan
Det konto som du ska använda för e-postloggning är ett Exchange Online-konto. Det schemalagda jobbet kommer att använda kontot för att ansluta till den delade postlådan och bearbeta e-postmeddelanden. Det här kontot ska inte kopplas till en specifik person. Lägg till e-postkontot till medlemmarna för den delade postlådan. Mer information finns i avsnittet [Använd EAC för att redigera delegering av delad postlådan](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### <a name="allow-other-users-to-see-logged-emails"></a>Låta andra användare se loggade e-postmeddelanden
Du kan tillåta en annan användare att öppna ett e-postmeddelande i Exchange som är relaterat till en interaktionsloggtransaktionen från [!INCLUDE[prod_short](includes/prod_short.md)]. Det gör du genom att ge användaren ``Read`` behörighet till mappen **Arkiv** i den delade postlådan. Mer information finns också i [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### <a name="create-mail-flow-rules"></a>Skapa regler för e-postflöde
Regler för e-postflöde du söker efter specifika villkor i meddelanden och utför åtgärder för dem. Skapa två postflödesregler baserad på informationen i följande tabell. Mer information finns i [Hantera postflödesregler i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) och [Åtgärder för postflödesregler i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Syfte  |Name  |Använd regeln om …  |Gör följande …  |
|---------|---------|---------|---------|
|En regel för inkommande e-post     |Logga e-post som skickats till den här organisationen|Avsändaren finns utanför organisationen och mottagaren finns inne i organisationen|Skicka hemlig kopia det e-postkonto som har angetts för den delade brevlådan.|
|En regel för utgående e-post     |Logga e-post som skickats från den här organisationen|Avsändaren finns inne i organisationen och mottagaren finns utanför organisationen.|Skicka hemlig kopia det e-postkonto som har angetts för den delade brevlådan.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] behandlar endast meddelanden i mappen Inkorgen i den delade postlådan. Om en regel flyttar meddelanden från inkorgen till en annan mapp kommer dessa meddelanden inte att behandlas. Dessutom ignoreras meddelanden i mappen skräppost. 

---

## <a name="setting-up-prod_short-to-log-email-messages"></a>Ställa in [!INCLUDE[prod_short](includes/prod_short.md)] för att logga e-postmeddelanden
Dessa steg är desamma för både den aktuella och den nya upplevelsen.

Kom igång med e-postloggning i två enkla steg:

1. Anslut [!INCLUDE[prod_short](includes/prod_short.md)] till Exchange Online för din Microsoft 365-prenumeration. Exchange Online hanterar dina e-postmeddelanden. Detta steg är enkelt att utföra med hjälp av en guide för assisterad konfiguration. Du behöver bara ha administratörsbehörigheter för ditt administratörskonto i Microsoft 365. Du startar guiden genom att gå till sidan **Assisterad konfiguration** och sedan väljer guiden **Konfigurera e-postloggning**.  

2. Kontrollera att e-postadresserna för dina säljare och kontakter i [!INCLUDE[prod_short](includes/prod_short.md)] är giltiga. Det gör du genom att för varje kund eller säljare öppna kortet **Kontakt** eller **Säljare/Inköpare** och titta i fältet **E-post**.

> [!Tip]
> När du har slutfört stegen i guiden kan du kontrollera om kopplingen har lyckats. Beroende på om du använder den nuvarande eller nya upplevelsen gör du något av följande: 
>
> * **Aktuell upplevelse**: Sök efter **Marknadsföringsinställning**, välj **Åtkomst**, sedan **Funktioner** och **Validera konfiguration för e-postloggning**.
> * **Ny erfarenhet**: Sök efter **E-postloggning**, välj **Åtgärder** och välj **Validera konfiguration**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Visa e-postutbyten i interaktionsloggen

[!INCLUDE[prod_short](includes/prod_short.md)] skapar en transaktion på sidan **Interaktionslogg** varje gång en säljare och en kontakt utbyter e-postmeddelanden. Om du vill visa interaktionsloggen öppnar du kortet **Kontakt**, väljer **Relaterat**, väljer sedan **Historik** och därefter **Interaktionslogg**. Det finns några saker som du kan göra med posterna i loggen, till exempel:

- Visa innehållet i e-postmeddelandet som utbytts genom att välja **Bearbeta** och sedan **Visa bilagor**.
- Förvandla ett e-postutbyte till en affärsmöjlighet. Om en transaktion verkar lovande kan du omvandla den till en affärsmöjlighet och sedan hantera förloppet fram till en försäljning. Om du vill göra ett e-postutbyte till en affärsmöjlighet kan du välja post och sedan **processer** och sedan **skapa affärsmöjlighet**. Mer information finns i [Hantera försäljningsmöjligheter](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>Ansluta lokala versioner till Microsoft Exchange

Du kan ansluta [!INCLUDE[prod_short](includes/prod_short.md)] lokalt till Exchange lokalt eller Exchange Online för e-postloggning. För båda versioner av Exchange finns inställningar för anslutningen tillgängliga på sidan **Marknadsföringsinställning**. För Exchange Online kan du också använda en assisterad konfigurationsguide.

> [!IMPORTANT]
> Den nya upplevelsen stöder inte en anslutning till Exchange lokalt. Om du måste använda Exchange lokalt ska du inte aktivera funktionsuppdateringen för den nya upplevelsen.

## <a name="connecting-to-exchange-on-premises"></a>Ansluta till Exchange lokalt
## <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience)
För att ansluta till [!INCLUDE[prod_short](includes/prod_short.md)] lokalt till Exchange lokalt kan du på sidan **Marknadsföringsinställning** använda **Basic** som **Autentiseringstyp** och sedan ange autentiseringsuppgifter för användarkontot för Exchange lokalt. Slå sedan på brytaren **Aktiverad** för att starta loggningen av e-post.

## <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience)
Den nya upplevelsen stöder inte en anslutning till Exchange lokalt.

---

## <a name="connecting-to-exchange-online"></a>Ansluta till Exchange Online
För att ansluta till Exchange Online måste du registrera ett program i Azure Active Directory. Ange program-ID, nyckelvalvshemlighet och omdirigerings-URL som ska användas för registreringen. URL-adressen för omdirigering anges i förväg och bör användas för de flesta installationer. Mer information finns i [Så här registrerar du ett program Azure AD för anslutning från Business Central till Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Du måste också ansluta till **OAuth2** som **Autentiseringstyp**. Du måste också registrera ett program i Azure Active Directory. Ange program-ID, nyckelvalvshemlighet och omdirigerings-URL som ska användas för registreringen. URL-adressen för omdirigering fylls i förväg och bör användas för de flesta installationer. Mer information finns i Så här registrerar du ett program i Azure AD för anslutning från Business Central till Exchange Online nedan.

Du måste ställa in installationen för att använda HTTPS. Mer information finns i [Konfigurera SSL för att skydda anslutningen till Business Central webbklienten](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Om du konfigurerar servern så att den får en annan startsida kan du alltid ändra URL-adressen. Klientens hemlighet kommer att sparas som en krypterad sträng i databasen.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Så här registrerar du ett program i Azure AD för att ansluta från Business Central till Exchange Online
Följande åtgärder förutsätter att du använder Azure Active Directory för att hantera identiteter och åtkomst. Mer information finns i [Snabbstart: registrera ett program med Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). 

## <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience) 
Följande åtgärder förutsätter att du använder Azure Active Directory för att hantera identiteter och åtkomst. Mer information finns i [Snabbstart: registrera ett program med Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). Om du inte använder Azure Active Directory, se [använda en annan identitets- och åtkomsthanteringstjänst](marketing-set-up-email-logging.md#use-another-identity-and-access-management-service). 

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
8. Välj **Översikt** och leta sedan reda på **App (klient-ID)**-värdet. Värdet **App-ID (klient)** är klient-ID för din app. Du måste ange det klient-ID antingen på **sidan för marknadsföringsinställning**, i fältet **Klient-ID**, eller lagra det på en säker plats och tillhandahålla den i en händelseprenumeration.
9. I [!INCLUDE[prod_short](includes/prod_short.md)] konfigurerar du e-postloggning på sidan **Marknadsföringsinställning** eller använder guiden **Assisterad konfiguration för e-postloggning** för att få hjälp med processen.
    * Ange användarens e-postkonto å dens vägnar för vilken det schemalagda jobbet ska ansluta till Exchange Online och bearbeta e-postmeddelanden. Användaren måste ha en giltig licens för Exchange Online.
    * Tillhandahålla webbadressen (URL) för ditt Exchange Online. Vanligtvis är denna URL den domän som du angav i användarens e-postadress.
    * Tillhandahåll **Sökväg till kömapp** och **Sökväg för lagringsmapp**.
10. Aktivera brytaren **Aktiverad** för att börja logga e-post.
11. Logga in med ditt administratörskonto för Azure Active Directory (detta konto måste ha en giltig licens för Exchange och vara administratör i ditt Exchange Online). När du har loggat in måste du tillåta att ditt registrerade program loggar in Exchange Online på ditt företags vägnar. Du måste ange ett medgivande för att slutföra installationen.

   > [!NOTE]
   > Om du inte uppmanas att logga in med ditt administratörskonto beror detta förmodligen på att popup-fönster blockeras. Du kan logga in med popup-fönster från https://login.microsoftonline.com.

## <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience)
1. I Azure Portal, under **Hantera**, väljer du **Autentisering**.
2. Under **Omdirigerings-URL** lägger du till den omdirigerings-URL som anges på sidan **e-postloggning** i [!INCLUDE[prod_short](includes/prod_short.md)]. Om fältet för omdirigeringsadressen på sidan E-postloggning är tom hittar du den föreslagna omdirigeringsadressen på sidan **Assisterad konfiguration**. För att öppna sidan, på sidan **e-postloggning** välj **Åtgärder** och **Assisterad konfiguration**.

    > [!NOTE]
    > Om du inte anger omdirigerings-URL:en kan du göra det senare genom att välja **Lägg till en plattform** och sedan välja **Webb** för att lägga till webb-appen och omdirigeringsadressen.

3. Under **Hantera**, välj **API-behörigheter** och välj **Microsoft Graph** och välj **Delegerad behörighet**.
4. Använd sökrutan för att söka efter och välja **e-post** och lägg sedan till **Mail.ReadWrite.Shared** behörighet. 
5. Under **Hantera**, välj **Certifikat och hemligheter** och skapa sedan en ny hemlighet för ditt program. Du kommer att använda hemligheten antingen i fältet **klienthemlighet** på sidan **E-postloggning** i [!INCLUDE[prod_short](includes/prod_short.md)].
6. Välj **Översikt** och leta sedan reda på **App (klient-ID)**-värdet. Detta är klient-ID:t för ditt program. Du måste ange den antingen i fältet **klient-ID** på sidan **e-postloggning**.
7. I [!INCLUDE[prod_short](includes/prod_short.md)] konfigurerar du e-postloggning på sidan **E-postloggning** eller använder guiden **Assisterad konfiguration** för att få hjälp.

### <a name="use-another-identity-and-access-management-service"></a>Använda en annan identitets- och åtkomsthanteringstjänst
Om du inte använder Azure Active Directory för att hantera identiteter och åtkomst behöver du en viss hjälp från en utvecklare. Om du hellre vill lagra program-ID och hemlighet på en annan plats kan du lämna fälten klient-ID och klienthemlighet tomma och skriva ett tillägg för att hämta ID och hemlighet från platsen. Du kan tillhandahålla hemligheten i samband med körning genom att prenumerera på händelserna OnGetEmailLoggingClientId och OnGetEmailLoggingClientSecret i codeunit 1641, "Konfigurera e-postloggning".

---

## <a name="to-start-logging-email"></a>Så här börjar du logga e-post
1. För att börja logga e-post, på **e-postloggning** vänd växlingsknappen **Aktiverad**.
2. Logga in med det Exchange Online konto som det schemalagda jobbet kommer att använda för att ansluta till den delade postlådan och bearbeta e-postmeddelanden.

    > [!NOTE]
    > Om du inte uppmanas att logga in på Exchange Online konto kan det bero på att din webbläsare blockerar popup-fönster. Du kan logga in med popup-fönster från https://login.microsoftonline.com.

## <a name="to-stop-logging-email"></a>Så här slutar du logga e-post
## <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience)
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Marknadsföringsinställning** och väljer sedan relaterad länk.
1. Stäng av brytaren **Aktiverad**.

## <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience)
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikon, anger du **E-postloggning** och väljer sedan relaterad länk.
2. Stäng av brytaren **Aktiverad**.

---

## <a name="to-change-the-user-account-used-for-email-logging"></a>Så här ändrar du vilket användarkonto som ska användas för e-postloggning
Om du använder den nya upplevelsen kan du ändra vilket användarkonto som ska användas för e-postloggning. Det aktuella gränssnittet stöder inte detta.

## <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience) 
Inaktivera din nuvarande inställning, ändra användaren på sidan för **e-postloggning** och aktivera sedan e-postloggning igen. Du kan också köra den assisterade installationsguiden igen.

## <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience)
### <a name="prod_short-online"></a>[!INCLUDE[prod_short](includes/prod_short.md)] Online
1. Logga in på [!INCLUDE[prod_short](includes/prod_short.md)] med det konto som det schemalagda jobbet kommer att använda för att ansluta till den delade postlådan och bearbeta e-postmeddelanden. Det här kontot måste ha åtkomst till både [!INCLUDE[prod_short](includes/prod_short.md)] och Exchange Online.
2. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikon, anger du **E-postloggning** och väljer sedan relaterad länk. 
3. Välj **relaterad** och sedan **Jobbkötransaktion**.
4. Starta om jobbet **E-postloggning**.

### <a name="prod_short-on-premises"></a>[!INCLUDE[prod_short](includes/prod_short.md)] lokalt
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ikon, anger du **E-postloggning** och väljer sedan relaterad länk. 
2. Välj **åtgärder** och **förnya token**.
3. Logga in med det Exchange Online konto som det schemalagda jobbet kommer att använda för att ansluta till den delade postlådan och bearbeta e-postmeddelanden.

## <a name="see-also"></a>Se även
[Hantera relationer](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]