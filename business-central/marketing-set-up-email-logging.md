---
title: Konfigurera e-postloggning
description: Lär dig hur du kan omvandla e-postinteraktioner mellan säljare och kunder till verkliga affärsmöjligheter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: dcenic
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect, opportunity, email'
ms.search.form: '1680, 1811, 5076'
---
# Spåra utbyte av e-postmeddelanden mellan säljare och kontakter

Få ut mer av kommunikationen mellan dina säljare och kunder genom att förvandla e-postutbyten till praktiska möjligheter. [!INCLUDE[prod_short](includes/prod_short.md)] kan tillsammans med Exchange Online spara en logg över de inkommande och utgående meddelandena. Du kan visa och analysera innehållet i varje meddelande på sidan **Interaktionslogg**.

> [!IMPORTANT]
> För [!INCLUDE[prod_short](includes/prod_short.md)] online, [!INCLUDE[prod_short](includes/prod_short.md)] och Exchange Online måste finnas på samma innehavare.

## Så här konfigurerar du e-postloggning

### Konfigurera gemensamma mappar och regler för e-postloggning i Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Därefter ansluter du [!INCLUDE[prod_short](includes/prod_short.md)] med Exchange Online.

### Konfigurera en delad brevlåda och regler för e-postinloggning i Exchange Online

> [!NOTE]
> För dessa åtgärder krävs administratörsåtkomst för Exchange Online.

Förbered en delad postlåda i Exchange administrationscenter. Du kan också använda Exchange Online PowerShell. Mer information finns i [skapa en delad postlåda](/microsoft-365/admin/email/create-a-shared-mailbox) eller [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Om du använder Exchange Management PowerShell är dina ändringar tillgängliga i Exchange administrationscenter efter en fördröjning. Förseningen kan vara i flera timmar.

### Lägga till ett användarkonto för medlemmar i den delade postlådan

Det konto som du ska använda för e-postloggning är ett Exchange Online-konto. Det schemalagda jobbet kommer att använda kontot för att ansluta till den delade postlådan och bearbeta e-postmeddelanden. Det här kontot ska inte kopplas till en specifik person. Lägg till e-postkontot till medlemmarna för den delade postlådan. Mer information finns i avsnittet [Använd EAC för att redigera delegering av delad postlådan](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### Låta andra användare se loggade e-postmeddelanden

Du kan tillåta en annan användare att öppna ett e-postmeddelande i Exchange som är relaterat till en interaktionsloggtransaktionen från [!INCLUDE[prod_short](includes/prod_short.md)]. Det gör du genom att ge användaren ``Read`` behörighet till mappen **Arkiv** i den delade postlådan. Mer information finns också i [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### Skapa regler för e-postflöde

Regler för e-postflöde du söker efter specifika villkor i meddelanden och utför åtgärder för dem. Skapa två postflödesregler baserad på informationen i följande tabell. Mer information finns i [Hantera postflödesregler i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) och [Åtgärder för postflödesregler i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Syfte  |Name  |Använd regeln om …  |Gör följande …  |
|---------|---------|---------|---------|
|En regel för inkommande e-post     |Logga e-post som skickats till den här organisationen|Avsändaren finns utanför organisationen och mottagaren finns inne i organisationen|Skicka hemlig kopia det e-postkonto som har angetts för den delade brevlådan.|
|En regel för utgående e-post     |Logga e-post som skickats från den här organisationen|Avsändaren finns inne i organisationen och mottagaren finns utanför organisationen.|Skicka hemlig kopia det e-postkonto som har angetts för den delade brevlådan.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] behandlar endast meddelanden i mappen Inkorgen i den delade postlådan. Om en regel flyttar meddelanden från inkorgen till en annan mapp kommer dessa meddelanden inte att behandlas. Dessutom ignoreras meddelanden i mappen skräppost.

## Ställa in [!INCLUDE[prod_short](includes/prod_short.md)] för att logga e-postmeddelanden

Kom igång med e-postloggning i två enkla steg:

1. Anslut [!INCLUDE[prod_short](includes/prod_short.md)] till Exchange Online för din Microsoft 365-prenumeration. Exchange Online hanterar dina e-postmeddelanden. Detta steg är enkelt att utföra med hjälp av en guide för assisterad konfiguration. Du behöver bara ha administratörsbehörigheter för ditt administratörskonto i Microsoft 365. Du startar guiden genom att gå till sidan **Assisterad konfiguration** och sedan väljer guiden **Konfigurera e-postloggning**.  

2. Kontrollera att e-postadresserna för dina säljare och kontakter i [!INCLUDE[prod_short](includes/prod_short.md)] är giltiga. Det gör du genom att för varje kund eller säljare öppna kortet **Kontakt** eller **Säljare/Inköpare** och titta i fältet **E-post**.

    > [!Tip]
    > När du har slutfört stegen i guiden kan du kontrollera om kopplingen har lyckats. Sök efter **E-postloggning**, välj **Åtgärder** och välj **Validera konfiguration**.

## Visa e-postutbyten i interaktionsloggen

[!INCLUDE[prod_short](includes/prod_short.md)] skapar en transaktion på sidan **Interaktionslogg** varje gång en säljare och en kontakt utbyter e-postmeddelanden. Om du vill visa interaktionsloggen öppnar du kortet **Kontakt**, väljer **Relaterat**, väljer sedan **Historik** och därefter **Interaktionslogg**. Det finns några saker som du kan göra med posterna i loggen, till exempel:

* Visa innehållet i e-postmeddelandet som utbytts genom att välja **Bearbeta** och sedan **Visa bilagor**.
* Förvandla ett e-postutbyte till en affärsmöjlighet. Om en transaktion verkar lovande kan du omvandla den till en affärsmöjlighet och sedan hantera förloppet fram till en försäljning. Om du vill göra ett e-postutbyte till en affärsmöjlighet kan du välja post och sedan **processer** och sedan **skapa affärsmöjlighet**. Mer information finns i [Hantera försäljningsmöjligheter](marketing-manage-sales-opportunities.md).

## Begränsningar för postlådor och mappar i Exchange Online

Det finns begränsningar för postlådor och mappar i Exchange Online, till exempel begränsningar för mappstorlekar och antalet meddelanden. Mer information finns i [Exchange Online-begränsningar](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) och [Begränsningar för offentliga mallar i Exchange Server](/Exchange/collaboration/public-folders/limits?view=exchserver-2019&preserve-view=true).

[!INCLUDE[prod_short](includes/prod_short.md)] lagrar loggade e-postmeddelanden i en mapp i Exchange Online. [!INCLUDE[prod_short](includes/prod_short.md)] lagrar även en länk till varje loggat meddelande. Länkarna öppnar de loggade meddelandena i Exchange Online från sidorna Interaktionslogg, Kontaktkort och Säljarkort i [!INCLUDE[prod_short](includes/prod_short.md)]. Om ett loggat meddelande flyttas till en annan mapp kommer länken att brytas. Ett meddelande kan till exempel flyttas manuellt eller Exchange Online kan automatiskt starta Automatisk delning när en lagringsgräns har nåtts.

Med hjälp av följande steg kan du undvika att bryta länkar till meddelanden i Exchange Online.

1. Flytta inte befintliga meddelanden till en annan mapp när du har ändrat inställningarna för e-postloggningen. Genom att behålla befintliga meddelanden där de är kommer att bevara länkarna. Länkar till meddelanden i den nya mappen blir giltiga.
2. Undvik att nå gränserna för postlådan och antalet mappar. Så här gör du om du är på väg att uppnå en gräns:
    1. Skapa en ny delad postlåda i Exchange Online.
    2. Uppdatera reglerna för e-postflöde i Exchange Online.
    3. Uppdatera inställningarna för e-postloggning i Business Central

## Ansluta lokala versioner till Microsoft Exchange

Du kan ansluta [!INCLUDE[prod_short](includes/prod_short.md)] lokalt till Exchange lokalt eller Exchange Online för e-postloggning. För båda versioner av Exchange finns inställningar för anslutningen tillgängliga på sidan **Marknadsföringsinställning**. För Exchange Online kan du också använda en assisterad konfigurationsguide.

<!-- [!IMPORTANT]
> The new experience doesn't support a connection to Exchange on-premises. If you must use Exchange on-premises, do not enable the feature update for the new experience.

## Connect to Exchange on-premises
<!--
## [Current Experience](#tab/current-experience)
To connect [!INCLUDE[prod_short](includes/prod_short.md)] on-premises to Exchange on-premises, on the **Marketing Setup** page, you can use **Basic** as the **Authentication Type**, and then enter credentials for the user account for Exchange on-premises. Then turn on the **Enabled** toggle to start logging email.

## [New Experience](#tab/new-experience)
The new experience does not support connections to Exchange on-premises.
-->
## Ansluta till Exchange Online

För att ansluta till Exchange Online måste du registrera ett program i Azure Active Directory. Ange program-ID, nyckelvalvshemlighet och omdirigerings-URL som ska användas för registreringen. URL-adressen för omdirigering anges i förväg och bör användas för de flesta installationer. Mer information finns i [Så här registrerar du ett program Azure AD för anslutning från Business Central till Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Du måste också ansluta till **OAuth2** som **Autentiseringstyp**. Du måste också registrera ett program i Azure Active Directory. Ange program-ID, nyckelvalvshemlighet och omdirigerings-URL som ska användas för registreringen. URL-adressen för omdirigering fylls i förväg och bör användas för de flesta installationer. Mer information finns i Så här registrerar du ett program i Azure AD för anslutning från Business Central till Exchange Online nedan.

Du måste ställa in installationen för att använda HTTPS. Mer information finns i [Konfigurera SSL för att skydda anslutningen till Business Central webbklienten](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Om du konfigurerar servern så att den får en annan startsida kan du alltid ändra URL-adressen. Klientens hemlighet kommer att sparas som en krypterad sträng i databasen.

### Så här registrerar du ett program i Azure AD för att ansluta från Business Central till Exchange Online

Följande åtgärder förutsätter att du använder Azure Active Directory för att hantera identiteter och åtkomst. Mer information finns i [Snabbstart: registrera ett program med Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). 

1. I Azure Portal, under **Hantera**, väljer du **Autentisering**.
2. Under **Omdirigerings-URL** lägger du till den omdirigerings-URL som anges på sidan **e-postloggning** i [!INCLUDE[prod_short](includes/prod_short.md)]. Om fältet för omdirigeringsadressen på sidan E-postloggning är tom hittar du den föreslagna omdirigeringsadressen på sidan **Assisterad konfiguration**. För att öppna sidan, på sidan **e-postloggning** välj **Åtgärder** och **Assisterad konfiguration**.

    > [!NOTE]
    > Om du inte anger omdirigerings-URL:en kan du göra det senare genom att välja **Lägg till en plattform** och sedan välja **Webb** för att lägga till webb-appen och omdirigeringsadressen.

3. Under **Hantera**, välj **API-behörigheter** och välj **Microsoft Graph** och välj **Delegerad behörighet**.
4. Använd sökrutan för att söka efter och välja **e-post** och lägg sedan till **Mail.ReadWrite.Shared** behörighet. 
5. Under **Hantera**, välj **Certifikat och hemligheter** och skapa sedan en ny hemlighet för ditt program. Du kommer att använda hemligheten antingen i fältet **klienthemlighet** på sidan **E-postloggning** i [!INCLUDE[prod_short](includes/prod_short.md)].
6. Välj **Översikt** och leta sedan reda på **App (klient-ID)**-värdet. Detta är klient-ID:t för ditt program. Du måste ange den antingen i fältet **klient-ID** på sidan **e-postloggning**.
7. I [!INCLUDE[prod_short](includes/prod_short.md)] konfigurerar du e-postloggning på sidan **E-postloggning** eller använder guiden **Assisterad konfiguration** för att få hjälp.

### Använda en annan identitets- och åtkomsthanteringstjänst

Om du inte använder Azure Active Directory för att hantera identiteter och åtkomst behöver du en viss hjälp från en utvecklare. Om du hellre vill lagra program-ID och hemlighet på en annan plats kan du lämna fälten klient-ID och klienthemlighet tomma och skriva ett tillägg för att hämta ID och hemlighet från platsen. Du kan tillhandahålla hemligheten i samband med körning genom att prenumerera på händelserna OnGetEmailLoggingClientId och OnGetEmailLoggingClientSecret i codeunit 1641, "Konfigurera e-postloggning".

## Så här börjar du logga e-post

1. För att börja logga e-post, på **e-postloggning** vänd växlingsknappen **Aktiverad**.
2. Logga in med det Exchange Online konto som det schemalagda jobbet kommer att använda för att ansluta till den delade postlådan och bearbeta e-postmeddelanden.

    > [!NOTE]
    > Om du inte uppmanas att logga in på Exchange Online konto kan det bero på att din webbläsare blockerar popup-fönster. Du kan logga in med popup-fönster från https://login.microsoftonline.com.

## Så här slutar du logga e-post

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikon, anger du **E-postloggning** och väljer sedan relaterad länk.
2. Stäng av brytaren **Aktiverad**.

## Så här ändrar du vilket användarkonto som ska användas för e-postloggning

### [!INCLUDE[prod_short](includes/prod_short.md)] Online

1. Logga in på [!INCLUDE[prod_short](includes/prod_short.md)] med det konto som det schemalagda jobbet kommer att använda för att ansluta till den delade postlådan och bearbeta e-postmeddelanden. Det här kontot måste ha åtkomst till både [!INCLUDE[prod_short](includes/prod_short.md)] och Exchange Online.
2. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikon, anger du **E-postloggning** och väljer sedan relaterad länk. 
3. Välj **relaterad** och sedan **Jobbkötransaktion**.
4. Starta om jobbet **E-postloggning**.

### [!INCLUDE[prod_short](includes/prod_short.md)] lokalt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikon, anger du **E-postloggning** och väljer sedan relaterad länk.
2. Välj **åtgärder** och **förnya token**.
3. Logga in med det Exchange Online konto som det schemalagda jobbet kommer att använda för att ansluta till den delade postlådan och bearbeta e-postmeddelanden.

## Se även
[Hantera relationer](marketing-relationship-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]