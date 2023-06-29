---
title: Konfigurera synkronisering av kontakter med Outlook för Business Central lokal
description: Lär dig hur du konfigurerar Business Central lokal miljö för att synkronisera kontakter i Business Central och Outlook.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/04/2023
ms.custom: bap-template
---

# <a name="set-up-contact-sync-with-outlook-for-business-central-on-premises"></a><a name="set-up-contact-sync-with-outlook-for-business-central-on-premises"></a>Konfigurera synkronisering av kontakter med Outlook för Business Central lokal

I den här artikeln lär du dig att konfigurera [!INCLUDE[prod_short](includes/prod_short.md)] lokal för att synkronisera kontakter i [!INCLUDE[prod_short](includes/prod_short.md)] med kontakter i Outlook. Om du vill ha mer information kan du gå till [Synkronisera kontakter i Business Central med kontakter i Microsoft Outlook](admin-synchronize-outlook-contacts.md).

## <a name="introduction"></a><a name="introduction"></a>Introduktion

Synkronisering av kontakter kräver att protokollet OAuth 2.0 används för autentisering med Exchange Online. Tidigare stöddes även grundläggande autentisering, men det är inaktuellt och stöds inte längre med Exchange Online. Du kan läsa mer om avskrivningen på [Utfasning av grundläggande autentisering i Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Den här ändringen innebär att synkroniseringen av kontakter i Business Central kan ha slutat fungera i din lokala miljö. I den här artikeln får du veta hur du får den att fungera igen.

## <a name="prerequisites"></a><a name="prerequisites"></a>Förutsättningar

- Exchange Online, antingen en fristående version eller genom Microsoft 365 abonnemang  
- Åtkomst till Azure Active Directory (Azure AD) klientorganisation som används av Exchange Online
- [!INCLUDE[prod_short](includes/prod_short.md)]-användare har ett Microsoft 365 eller Exchange Online e-postkonto som tilldelats deras konton i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan kontrollera denna inställning i avsnittet **Microsoft 365-autentisering** i användarprofilen i listan **Användare**. 

## <a name="set-up-contact-sync"></a><a name="set-up-contact-sync"></a>Ställ in synkronisering av kontakter

Slutför följande steg för att ställa in synkronisering av kontakter. Om du kör [!INCLUDE[prod_short](includes/prod_short.md)] våren 2019 (v.14), du måste göra ett extra steg som antingen ändrar programkoden eller skapar en anslutning till Power BI.

1. <a name="registerapp"></a>Registrera en app för Exchange Online API i din Azure AD-klientorganisation.

   I det här steget lägger du till en registrerad app i Azure AD-klientorganisation för ditt Microsoft 365- eller Exchange Online-abonnemang. Precis som andra Azure-tjänster som arbetar med Business Central kräver Exchange Online en registrerad app i Azure AD. Den registrerade appen tillhandahåller autentisering och autentiseringstjänster mellan Business Central och Exchange Online.

   Följ de detaljerade instruktionerna i hjälpen för utvecklare och IT-proffs på [Registrera ett program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Tänk på följande saker när du går igenom instruktionerna:

   - Om du redan har registrerat ett program som en del av en integration med en annan Microsoft-produkt, till exempel Power BI, kan du återanvända den registrerade appen. I det här fallet behöver du bara konfigurera appen med Office 365 Exchange Online behörigheter som beskrivs i nästa punkt.

   - Konfigurera det registrerade programmet med följande delegerade behörigheter till Office 365 Exchange Online API:

     - Contacts.ReadWrite
     - EWS.AccessAsUser.All

2. För [!INCLUDE[prod_short](includes/prod_short.md)] version 14 gör du något av följande:

   - Ändra sidan 6700 genom att ändra `FALSE` till `TRUE` i följande kodrad i `OnPageOpen` utlösaren:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Skapa ny sida med följande kod i OnPageOpen-utlösaren:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Konfigurera Power BI genom att följa instruktionerna i [Ställ in Business Central lokal för Power BI integration](admin-powerbi-setup.md#setup).

   När den lösning du har valt är på plats ber du användarna att köra antingen den nya/ändrade sidan eller [ansluta till Power BI](across-working-with-powerbi.md#connect). De behöver bara utföra detta steg en gång.

## <a name="next-steps"></a><a name="next-steps"></a>Nästa steg

[Synkronisera kontakter i Business Central med kontakter i Microsoft Outlook](admin-synchronize-outlook-contacts.md)  
