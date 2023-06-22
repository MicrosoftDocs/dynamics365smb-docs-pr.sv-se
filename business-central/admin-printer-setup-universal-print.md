---
title: Konfigurera skrivare för Universell utskrift
description: Lär dig mer om hur du kan använda Universell utskrift för att ange molnutskrift i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---

# <a name="set-up-universal-print-printers" />Konfigurera skrivare för Universell utskrift

Universell utskrift är en Microsoft 365-prenumerationstjänst som körs helt på Microsoft Azure. Med den här funktionen får du centraliserad utskriftshantering via Universell utskrift-portalen. [!INCLUDE[prod_short](includes/prod_short.md)] gör skrivarinställningar i Universell utskrift tillgängliga för klientanvändare via tillägget **Universell utskrift-integrering**.

![Inställning av Universell utskrift.](media/Universal-Print-arch.png)

Den fullständiga installationen kräver att du arbetar både i Microsoft Azure med [Azure-portal](https://portal.azure.com) och i [!INCLUDE[prod_short](includes/prod_short.md)]. Inställningarna delas upp mellan två huvuduppgifter enligt beskrivningen i den här artikeln:

1. I Microsoft Azure ställ in Universell utskrift och lägg till skrivare du vill använda i Business Central till dela skrivare. Gå till [detta avsnitt](#set-up-universal-print-and-printers-in-microsoft-azure).
2. I  [!INCLUDE[prod_short](includes/prod_short.md)] lägger du till skrivarna i utskriftsresurserna i Universell utskrift. Gå till [det här avsnittet ](#add-printers-in-business-central-online) för online eller [här](#add-printers-in-business-central-on-premises) för lokalt.

## <a name="prerequisites" />Förutsättningar

- Skrivare som stöds

  [!INCLUDE[prod_short](includes/prod_short.md)] stöder samma skrivare som Universell utskrift, som kan vara antingen Universell utskrift-kompatibla eller icke-kompatibla skrivare. Icke-kompatibla skrivare kan inte kommunicera direkt med Universell utskrift, så de kräver extra anslutningsprogram vara, som tillhandahålls av Universell utskrift. Vissa äldre skrivare kanske inte stöds. 

- Universell utskrift:

  - En Universell utskrift-prenumeration/licens för organisationen.

    Läs mer i [Licens för Universell utskrift](/universal-print/fundamentals/universal-print-license).

  - Du har rollerna **Utskriftsadministratör** (eller Utskriftshantering) och **Global administratör** i Azure.

    För att kunna hantera Universell utskrift måste ditt konto ha rollerna **Utskriftsadministratör** (eller Utskriftshantering) and **Global administratör** i Azure AD. Dessa roller behövs bara för att hantera Universell utskrift. De krävs inte av de som använder skrivarna från [!INCLUDE[prod_short](includes/prod_short.md)].

- [!INCLUDE[prod_short](includes/prod_short.md)] online och lokal:

  - [!INCLUDE[prod_short](includes/prod_short.md)] utgivningscykel 1 år 2021 eller senare.
  - Tillägget **Universell utskrift-integrering** är installerat.

    Tillägget publiceras och installeras som standard som en del av [!INCLUDE[prod_short](includes/prod_short.md)] online och lokalt. Du kan kontrollera om den är installerad på sidan **Tilläggshantering**. Läs mer i [Installera och avinstallera tillägg i Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] endast lokalt:
  - Azure Active Directory (AD) eller NavUserPassword-autentisering har konfigurerats.
    > [!NOTE]
    >  Det universella fil tillägget stöder inte autentisering mellan tjänster (S2S). En inloggad användare måste skicka utskrifter till den universella utskriftstjänsten via Graph API.
  - Ett program för Business Central har registrerats i din Azure AD-klientorganisation och [!INCLUDE[prod_short](includes/prod_short.md)].

    Precis som andra Azure-tjänster som fungerar med [!INCLUDE[prod_short](includes/prod_short.md)] kräver Universell utskrift en appregistrering för [!INCLUDE[prod_short](includes/prod_short.md)] i Azure AD. Programregistreringen tillhandahåller autentisering och autentiseringstjänster mellan [!INCLUDE[prod_short](includes/prod_short.md)] och Universell utskrift.

    Din distribution kanske redan använder en appregistrering för andra Azure-tjänster som Power BI. Om så är fallet ska du använda den befintliga appregistreringen även för Universell utskrift, i stället för att lägga till en ny. Det enda du behöver göra i det här fallet är att ändra appregistreringen så att den innehåller relevanta utskriftsbehörigheter för Microsoft Graph API: **PrinterShare.ReadBasic.All**, **PrintJob.Create** och **PrintJob.ReadBasic.** 

    Om du vill registrera en app och ställa in lämpliga behörigheter följer du de steg som beskrivs i [Registrera ett program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

## <a name="set-up-universal-print-and-printers-in-microsoft-azure" />Konfigurera Universell utskrift och skrivare i Microsoft Azure

Innan du kan börja hantera Universell utskrift-skrivare i Business Central finns det flera uppgifter för att Universell utskrift ska kunna köras i Azure med de skrivare du vill använda.

För detaljerade instruktioner om hur du installerar, se [Komma igång: Ställ in Universell utskrift](/universal-print/fundamentals/universal-print-getting-started) i Universell utskrift-dokumentation. Här följer en översikt över de steg du måste utföra. De flesta av dessa steg är gjorda på Azure-portalen.

1. Tilldela Universell utskrift-licenser till dig själv och andra användare.

    Hur du tilldelar licensen beror på om du integrerar med Business Central online eller lokal.

    - Med [!INCLUDE[prod_short](includes/prod_short.md)] online tilldelar du licenser genom att använda Microsoft 365-administrationscentret.

      Läs mer i [Hjälp för Microsofts administrationscenter – tilldela licenser till användare](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Med [!INCLUDE[prod_short](includes/prod_short.md)] lokala fördelar tilldelar du licenser i din Azure-klient med hjälp av Azure-portalen.

      Läs mer i [Azure Directory – Tilldela eller ta bort licenser i Azure Active Directory-portalen](/azure/active-directory/fundamentals/license-users-groups).

2. Installera anslutningsprogrammet för Universell utskrift för att registrera skrivare som inte kan kommunicera direkt med Universell utskrift.

    De flesta skrivare på marknaden kan inte kommunicera med Universell utskrift direkt, så du måste installera anslutningsprogrammet för Universell utskrift. Läs mer i [Installera anslutningsprogrammet för Universell utskrift](/universal-print/fundamentals/universal-print-connector-installation).

3. Registrera dina skrivare i Universell utskrift.

    Att registrera en skrivare gör Universell utskrift medveten om skrivaren.

    - Följ instruktionerna från skrivartillverkaren för skrivare som kan kommunicera direkt med Universell utskrift.

    - För andra skrivare registrerar du skrivarna med hjälp av anslutningsprogrammet för Universell utskrift. 

      Läs mer i [Skrivarregistrering](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Ändra skrivaregenskaper (valfritt)

    När en skrivare har registrerats kan du visa och ändra skrivaregenskaperna, som standardinställningar.

    Läs mer i [Hantera skrivarinställningar med hjälp av portalen för Universell utskrift](/universal-print/portal/configure-printer-settings).

5. Dela skrivare med användare.

    Alla skrivare som du vill använda i [!INCLUDE[prod_short](includes/prod_short.md)] måste läggas till i *dela skrivare* i Universell utskrift. Alla användare som behöver ha tillgång till skrivaren måste läggas till som medlem av dela skrivare. Läs mer i [Dela en skrivare](/universal-print/portal/share-printers).

    > [!TIP]
    > Du kan alltid lägga till eller ta bort användare senare. Läs mer i [Skrivarbehörigheter](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).

6. Aktivera dokumentkonvertering.

    Med Universell utskrift återges innehåll som ska skrivas ut i XPS-format. Vissa äldre skrivare på marknaden stöder inte rendering av XPS-innehåll&mdash;i många fall endast PDF-format. Utskrift till dessa skrivare misslyckas om inte Universell utskrift är inställt för att konvertera dokument till det skrivarstödda formatet.

    Läs mer i [Översikt över dokumentkonvertering](/universal-print/portal/document-conversion).

Nu kan du lägga till skrivarna till [!INCLUDE[prod_short](includes/prod_short.md)], konfigurera standardskrivare för rapporter och skriva ut.  

## <a name="add-printers-in-business-central-online" />Lägga till skrivare i Business Central Online

När du har ställt in och delat skrivare i Universell utskrift kan du lägga till dem i [!INCLUDE[prod_short](includes/prod_short.md)] för användning. Det finns två sätt att lägga till skrivare på Universell skrivare. Du kan lägga till alla skrivarna på en gång eller individuellt, en i taget.

Lägga till skrivare individuellt vill du installera samma Universell skrivare i [!INCLUDE[prod_short](includes/prod_short.md)] mer än en gång. För varje skrivare som har lagts till kan du ändra utskriftsinställningarna, t.ex. papperskassett, storlek och orientering. På så sätt kan du konfigurera skrivare för olika rapporter och dokument som har särskilda krav på utdata.

> [!NOTE]
> Använder du [!INCLUDE[prod_short](includes/prod_short.md)] lokalt? I så fall går du till [nästa avsnitt](#add-printers-in-business-central-on-premises), första gången konfigurationen är något annorlunda.  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Utskriftshantering** och väljer sedan relaterad länk.
2. Välj **Universell utskrift** och välj sedan något av följande alternativ:

   - **Lägg till alla skrivare för Universell utskrift** som inte redan har lagts till. Du kan använda det här alternativet även om det redan finns skrivare som har lagts till.
   - **Lägga till en skrivare för Universell utskrift** om du vill lägga till en viss skrivare.  
3. Följ instruktionerna på skärmen.

    - Om du väljer **Lägg till alla skrivare för Universell utskrift**, sedan startar inställningen av **Lägg till skrivare för Universell utskrift**. 

    - Om du väljer **Lägg till alla skrivare för Universell utskrift**, sedan visas sidan av **Skrivare för Universell utskrift**. Fyll i fältet **Namn**, välj **...** bredvid fältet **Utskriftsdelning i Universell utskrift** för att välja skrivare som har Universell utskrift. Fyll i återstående fält om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

När du har lagt till en skrivare kan du visa och ändra dess inställningar från sidan **Skrivarhantering**. Markera bara skrivaren och välj sedan **Redigera skrivarinställningar**.

## <a name="add-printers-in-business-central-on-premises" />Lägga till skrivare i Business Central lokal

<!--With [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, unlike online, users aren't automatically authenticated with the registered app in Azure used for the Universal Print service. So, before any Business Central user (including admins) can add or even use Universal Print printers, they'll have to authenticate with the Azure app and grant access to the Universal Print service. The following procedure describes how to initiate this authentication flow. Each user typically only has to do this task once.-->

Innan en användare kan lägga till eller använda skrivare med Universell utskrift i Business Central måste de tillåta åtkomst till de Azure-tjänster som används vid universell utskrift och ge dem behörighet att använda data och åtgärder som:

- Logga in och läsa användarprofilen
- Läsa grundläggande information om utskriftsjobb
- Skapa utskriftsjobb

Detta görs vanligtvis första gången de ansluter till den Azure-registrerade app som används för universell utskrift. I Business Central Online utförs det här auktoriseringsflödet sömlöst utan användarinteraktion. Men Business Central lokalt fungerar annorlunda. Det kräver att du, eller någon annan användare som vill använda skrivare med universell utskrift, initierar autentiseringsflödet &mdash;normalt endast en gång. Det mest direkta sättet beskrivs i följande steg. Ett mindre direkt sätt är att ansluta till en annan integrerad tjänst som använder samma Azure-registrerade app, som Power BI eller OneDrive. Varje användare behöver normalt bara utföra den här uppgiften en gång.

> [!NOTE]
> Om du är administratör rekommenderar vi att du utför uppgiften innan andra användare. Därefter ska du informera användare som behöver använda skrivarna med universell utskrift. Om den Azure-registrerade appen för universell utskrift kräver administrativt medgivande för API-behörigheter är det enklare om du ger tillstånd åt organisationen. Du kan bevilja administrativt godkännande från Azure-portalen eller när du kör stegen som följer. 

<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->
### <a name="connect-to-universal-print-for-the-first-time" />Anslut till universell utskrift för första gången

Utför dessa steg för att ansluta till den universella utskriftstjänsten för första gången.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Utskriftshantering** och väljer sedan relaterad länk.
2. Välj **Universell utskrift** > **Lägg till alla skrivare med universell utskrift** för att starta guiden för assisterad konfiguration **Lägg till installationshandbok för skrivare med universell utskrift** (guide).
3. Följ instruktionerna på skärmen tills du kommer till sidan TJÄNSTBEHÖRIGHETER FÖR AZURE ACTIVE DIRECTORY.

    <!--The AZURE ACTIVE DIRECTORY SERVICE PERMISSIONS page appears. You'll be prompted to give consent to Azure Services. You'll be lead through the process of verifying your Azure AD setup, checking your Universal Print license, and then adding the printers.-->

   ![Visar sidan TJÄNSTBEHÖRIGHETER FÖR AZURE ACTIVE DIRECTORY](media/azure-ad-services-permissions.png "Visar sidan TJÄNSTBEHÖRIGHETER FÖR AZURE ACTIVE DIRECTORY")

4. Markera länken för att **Verifiera Azure-tjänster**.

   1. Om sidan **Behörighet som krävs** visas, läs den ordentligt och välj **Acceptera** för att acceptera och fortsätta. Om du kör som administratör kan du välja  **medgivande för organisationens räkning** om du vill samtycka till alla användare.

      ![Visar sidan Azure behörighet som krävs](media/azure-ad-permissions-requested.png "Visar sidan Azure behörighet som krävs").

   2. Logga in på med ditt användarnamn och lösenord om du uppmanas till det.

5. När auktoriseringen är klar kommer du tillbaka till sidan **Lägg till skrivare med universell utskrift**. Välj **Nästa** > **Slutför** om du vill slutföra installationen.

När du har lagt till en skrivare kan du visa och ändra dess inställningar från sidan **Skrivarhantering**. Markera bara skrivaren och välj sedan **Redigera skrivarinställningar**.

När du har slutfört den inledande inloggningen kan du skriva ut rapporter och andra utskriftsjobb med hjälp av skrivarna med universell utskrift Mer information finns i [Skriva ut en rapport](ui-work-report.md#PrintReport). Om du vill lägga till, ta bort eller ändra någon skrivare går du bara tillbaka till sidan **utskrifts hantering** och väljer **Universell utskrift**.

## <a name="common-problems-and-resolutions" />Vanliga problem och lösningar

I det här avsnittet får du lära dig om vanliga problem som användarna kan uppleva när de försöker installera eller använda skrivare med universell utskrift.

### <a name="you-dont-have-access-to-the-printer-your-printer" />Du har inte åtkomst till skrivaren \<your-printer\>.

Om en användare får meddelandet när han eller hon försöker skriva ut ett dokument på en skrivare som använder universell utskrift, kan det bero på något av följande:

- Användaren har inte den universella utskriftslicens som tilldelats deras Microsoft 365 eller Azure Active AD-konto. 
- Användaren är inte tilldelad till skrivardelning i universell utskrift.
- (Lokal) Den Azure app-registrering som används för universell utskrift fungerar inte eller har nyligen ändrats sedan användaren senast loggade in.
- (Lokal) Användaren har inte loggat in på Azure registrerad app för appen för universell utskrift och skickats för första gången.

## <a name="there-was-an-error-fetching-printers-shared-to-you" />Det gick inte att hämta skrivare som delats med dig.

Om en användare får detta meddelande när han försöker lägga till en skrivare för Universell utskrift från sidan **Skrivarhantering**. Det beror vanligtvis på att de ännu inte har loggat in på den Azure-registrerade appen för Universell utskrift-appen och gett sitt samtycke för första gången. 
<!--
### <a name="troubleshooting" />Troubleshooting

#### <a name="you-dont-see-the-a-printer-in-the" />You don't see the a printer in the

The printer is not shared in Universal Print.

### <a name="you-get-an-error-when-tryong-to-add-all-or-a-single-printer" />You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## <a name="could-not-upload-the-document-to-print-job-" />Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps




-->

## <a name="next-steps" />Nästa steg
[Ställa in standardskrivare](ui-specify-printer-selection-reports.md).

## <a name="see-also" />Se även

[Översikt över skrivare](admin-printer-setup-overview.md)  
[Konfigurera e-postskrivare](admin-printer-setup-email.md)
[Skriva ut en rapport](ui-work-report.md#PrintReport)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Kör batchjobb](ui-how-run-batch-jobs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
