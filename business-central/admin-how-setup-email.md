---
title: Skapa ett e-postkonto i Business Central | Microsoft Docs
description: Beskriver hur du ansluter e-postkonton till Business Central så att du kan skicka utgående meddelanden utan att behöva öppna någon annan app.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, email, Office 365, connector
ms.date: 06/15/2020
ms.author: bholtorf
ms.openlocfilehash: 44fb1f467b0b44c41456a64c8de3f5ae9dc85786
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752756"
---
# <a name="set-up-email"></a>Konfigurera e-post
Personer på företag skickar information och dokument, till exempel försäljnings- och inköpsorder och fakturor, via e-post varje dag. Administratörer kan göra detta enklare genom att ansluta ett eller flera e-postkonton till [!INCLUDE[prod_short](includes/prod_short.md)], så att du kan skicka dokument utan att behöva öppna någon e-postapp. Du kan skapa varje meddelande individuellt med grundläggande formateringsverktyg, till exempel teckensnitt, format, färger och så vidare, och bifoga filer på upp till 100 MB. Administratörer kan också skapa rapportlayout som endast innehåller nyckelinformation från dokument. Mer information finns i [Skicka dokument via e-post](ui-how-send-documents-email.md).

E-postfunktionen i [!INCLUDE[prod_short](includes/prod_short.md)] gäller endast för utgående meddelanden. Det går inte att ta emot svar, det vill säga, det finns ingen inkorg i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt måste du skapa en app-registrering för [!INCLUDE[prod_short](includes/prod_short.md)] i Azure Portal innan du kan konfigurera e-post. App-registreringen gör det möjligt för [!INCLUDE[prod_short](includes/prod_short.md)] att auktorisera och autentisera med din e-postleverantör. Mer information finns i [Konfigurera e-post för Business Central lokalt](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). I [!INCLUDE[prod_short](includes/prod_short.md)] online hanterar vi detta åt dig.

## <a name="required-permissions"></a>Behörigheter som krävs
För att kunna konfigurera e-post måste du ha behörighetsinställningen **E-POSTKONFIGURATION**. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md). 

## <a name="adding-email-accounts"></a>Lägga till e-postkonton
Du lägger till e-postkonton via tillägg som möjliggör att konton från olika providrar ansluter till [!INCLUDE[prod_short](includes/prod_short.md)]. Med hjälp av standardtilläggen kan du använda konton från Microsoft Exchange Online, men det kan finnas andra tillägg som låter dig ansluta konton från andra leverantörer, t. ex. Gmail.

När du har lagt till ett e-postkonto kan du ange fördefinierade affärsscenarier där kontot ska användas för att skicka e-post. Du kan t. ex. ange att alla användare skickar försäljnings dokument från ett visst konto och inköpsdokument från ett annat. Mer information finns i [Tilldela e-postscenarier till e-postkonton](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

I följande tabell beskrivs de e-posttillägg som är tillgängliga som standard.

|Tillägg  |Beskrivning  |Exempel på när du kan använda  |
|---------|---------|---------|
|**Microsoft 365**|Alla skickar e-post från en delad postlåda i Exchange Online.|När alla meddelanden kommer från samma avdelning, t. ex. genom att din försäljningsorganisation skickar meddelanden från ett sales@cronus.com-konto. Detta innebär att du måste skapa en delad postlåda i administrationscentret för Office 365. Mer information finns i [Delade postlådor](/Exchange/collaboration/shared-mailboxes/shared-mailboxes.md).|
|**Aktuell användare**|Alla skickar e-post från det konto som de använde för att logga in på [!INCLUDE[prod_short](includes/prod_short.md)].|Tillåt kommunikation från enskilda konton.|
|**Annat (SMTP)**|Använd SMTP-protokoll för att skicka e-post.|Tillåt kommunikation via din SMTP-e-postserver. |

> [!NOTE]
> Tilläggen **Microsoft 365** och **Aktuell användare** använder de konton som du har angett för användare i administrationscentret för Microsoft 365 för din Office 365-prenumeration. Användarna måste ha en giltig licens för Exchange Online för att kunna skicka e-post med hjälp av tilläggen. 

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="legacy-smtp-settings-and-the-email---smtp-connector-extension"></a>Äldre SMTP-inställningar och tillägget för e-post/SMTP-anslutning
Om du redan använder [!INCLUDE[prod_short](includes/prod_short.md)] och har konfigurerat e-post via den äldre SMTP-konfigurationen kan du fortsätta att använda din konfiguration parallellt med tillägget för e-post/SMTP-anslutning. När vi uppdaterar din [!INCLUDE[prod_short](includes/prod_short.md)] till nästa version kommer vi att kopiera de äldre SMTP-inställningarna till tillägget för e-post/SMTP-anslutning. När du är klar kan administratören aktivera de förbättrade e-postfunktionerna, så kan du börja använda tillägget för e-post/SMTP-anslutning. Mer information finns i [Om funktionshantering](/dynamics365/business-central/dev-itpro/administration/feature-management.md#about-feature-management). Det finns emellertid ingen synkronisering mellan anslutningstillägget för SMTP och de äldre inställningarna. Om du ändrar SMTP-inställningarna i tillägget bör du utföra samma ändringar i den äldre SMTP-konfigurationen eller vice versa.

> [!NOTE]
> Om du har anpassningar som är beroende av den äldre SMTP-funktionen för e-post finns det en chans att något kommer att gå fel med dina anpassningar om du börjar använda e-posttillägg. Vi rekommenderar att du installerar och testar tilläggen innan du aktiverar funktionsväxeln för förbättrade e-postfunktioner.

## <a name="add-email-accounts"></a>Lägg till e-postkonton
Med den assisterade konfigurationsguiden för **Konfigurera e-post** kan du snabbt komma igång med e-post.

> [!NOTE]
> Du måste ha ett standardkonto för e-post, även om du bara lägger till ett enda konto. Standardkontot kommer att användas för alla e-postscenarier som inte har tilldelats något konto. Mer information finns i [Tilldela e-postscenarier till e-postkonton](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Konfigurera e-postkonton** och välj sedan tillhörande länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Office 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Tilldela e-scenarier till e-postkonton
E-postscenarier är processer som involverar att skicka ett dokument, t. ex. en försäljnings- eller inköpsorder, eller ett meddelande, till exempel en inbjudan till en extern revisor. Du kan använda specifika e-postkonton för specifika scenarier. Du kan t. ex. ange att alla användare alltid ska skicka försäljningsdokument från ett konto, inköpsdokument från ett annat, samt lager- eller produktionsdokument från ett tredje konto. Du kan tilldela, tilldela om och ta bort scenarier när du vill, men du kan bara tilldela ett scenario till ett enda e-postkonto åt gången. Standardkontot för e-post kommer att användas för alla scenarier som inte har tilldelats något konto.
 
<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents"></a>Konfigurera återanvändbara e-posttexter och layouter för försäljnings- och inköpsdokument
Du kan använda rapporter för att inkludera nyckelinformation från försäljnings- och inköps dokument i texter för e-post. I den här proceduren beskrivs hur du ställer in rapporten **Försäljning – Faktura** för bokförda försäljningsfakturor, men processen liknar den för andra rapporter.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Rapportval, försäljning** och välj sedan tillhörande länk.
2. På sidan **Rapportval, försäljning** i fältet **Användning** väljer du **Faktura**.
3. På en ny rad i fältet **Rappport-ID** väljer du t.ex. standardrapport 1306.
4. Markera kryssrutan **Använd för e-postbrödtex**.
5. Välj fältet **Layoutkod för brödtext i e-post** och välj sedan en layout från den nedrullningsbara listan.

    Rapportlayouter definierar både formatet och innehållet i brödtexten i e-mailet, inklusive texter som exempelvis hälsningar eller instruktioner som föregår dokumentinformationen. Alla tillgängliga rapportlayouter visas om du väljer **Välj från fullständig lista**.
6. Om du vill visa eller redigera den layout som e-mailets brödtext baseras på väljer du layout på sidan **Anpassade rapportlayouter** och väljer sedan åtgärden **Redigera layout**.
7. Om du vill erbjuda dina kunder att betala elektroniskt för försäljning kan du konfigurera relaterad betaltjänst, till exempel PayPal, och sedan ha PayPal-information och -hyperlänk infogade i e-mailets brödtext. Mer information finns i [Så här aktiverar du kundbetalningar via PayPal](sales-how-enable-payment-service-extensions.md).
8. Välj knappen **OK**.

Nu när du till exempel väljer åtgärden **Skicka** på sidan **Bokförd försäljningsfaktura** kommer e-postbrödtexten att innehålla information om dokumentet i rapport 1306 som föregås av utformad standardtext enligt den rapportlayout du valde i steg 5.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Använda en ersättningsavsändaradress i utgående e-postmeddelanden
Om du använder äldre SMTP-inställningar kan du använda funktionerna **Skicka som** eller **Skicka åt** från Microsoft Exchange för ändra avsändaradressen på utgående meddelanden. [!INCLUDE[prod_short](includes/prod_short.md)] använder SMTP-kontot för att autentisera till Exchange, men kommer antingen att ersätta avsändarens adress med den som du anger eller ändra den med "åt".

Nedan följer exempel på hur Skicka som och Skicka åt används i [!INCLUDE[prod_short](includes/prod_short.md)]:

 * När du skickar dokument som inköps- eller försäljningsorder till leverantörer och kunder vill du kanske visa dem för att komma från adressen _noreply@yourcompanyname.com_.
 * När arbetsflödet skickar en godkännandeförfrågan via e-post med hjälp av e-postadressen till den som efterfrågar meddelandet.

> [!Note]
> Du kan bara använda ett konto för att ersätta avsändaradresser. Det innebär att du inte kan ha en ersättningsadress för att inköpsprocesser, och en annan för försäljningsprocesser.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Att ange ersättningsavsändaradress för alla utgående e-postmeddelanden
1. I **administrationscenter för Exchange** för ditt Microsoft 365-konto hittar du den postlåda som ska användas som ersättningsadress, kopiera sedan eller gör en notering av adressen. Om du behöver en ny adress går du till administrationscentret för Microsoft 365 för att skapa en ny användare och ställa in postlådan.
2. I [!INCLUDE[prod_short](includes/prod_short.md)] välj ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **SMTP-postinställningar** och välj sedan relaterad länk.
3. I fältet **Skicka som** anger du ersättningsadressen.
4. Kopiera eller anteckna adressen i fältet **användar-ID**.
5. I **administrationscenter för Exchange** hittar du postlådan som ska användas som ersättningsadress och anger sedan adressen från fältet **Användar-ID** i **Skicka som**. Mer information finns i [Använd EAC för att tilldela behörighet till enskilda mailboxar](/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Så här använder du ersättningsadressen i arbetsflöde för godkännande
1. I [!INCLUDE[prod_short](includes/prod_short.md)] välj ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") ange **SMTP-postinställningar** och välj sedan relaterad länk.
2. Kopiera eller anteckna adressen i fältet **användar-ID**.
3. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användarinställningar för godkännande** och välj sedan relaterad länk.
4. I **administrationscenter för Exchange** hittar du postlådan för varje användare som finns på sidan **Användarinställningar för godkännande** och i fältet **Skicka som** anger du adressen från fältet **Användar-ID** för sidan **SMTP-postinställningar** i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Hantera behörigheter förmottagare](/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. I [!INCLUDE[prod_short](includes/prod_short.md)] välj ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") ange **SMTP-postinställningar** och välj sedan relaterad länk.
6. Aktivera ersättning genom att aktivera växling **Tillåt avsändarens ersättning**.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] avgör vilken adress som ska visas i följande ordning: <br><br> 1. Adressen som anges i fältet **e-post** på sidan **Användarinställningar för godkännande** för meddelanden i ett arbetsflöde. <br> 2. Adressen som anges i fältet **skicka som** på sidan **SMTP-postinställningar**. <br> 3. Adressen som anges i fältet **Användar-ID** på sidan **SMTP-postinställningar**.

## <a name="set-up-document-sending-profiles"></a>Skapa dokumentutskicksprofiler
Du kan ställa in en önskad metod för att skicka försäljningsdokument för varje enskild kund så att du inte behöver välja ett leveransalternativ . till exempel om du vill skicka dokumentet via e-post eller som ett elektroniskt dokument – varje gång du skickar ett dokument. Mer information finns i [Skapa Dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Konfigurera gemensamma mappar och regler för e-postloggning i Exchange Online
Få ut mer av kommunikationen mellan säljare och dina befintliga eller potentiella kunder genom att följa upp e-postutbyten och sedan omvandla dem till olika affärsmöjligheter. För mer information, se [Spåra utbyte av e-postmeddelanden mellan säljare och kontakter](marketing-set-up-email-logging.md).  

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Därefter ansluter du [!INCLUDE[prod_short](includes/prod_short.md)] med Exchange Online. För mer information, se [Spåra utbyte av e-postmeddelanden mellan säljare och kontakter](marketing-set-up-email-logging.md).  

## <a name="setting-up-email-for-business-central-on-premises"></a>Konfigurera e-post för Business Central lokalt 
[!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan integreras med tjänster som baseras på Microsoft Azure. Du kan till exempel använda Cortana Intelligence för smartare kassaflödesprognoser, Power BI för att visualisera verksamheten och Exchange Online för att skicka e-post. Integreringen med dessa tjänster baseras på en programregistrering i Azure Active Directory. Programregistreringen tillhandahåller autentisering och autentiseringstjänster för kommunikation. Om du vill använda e-postfunktionerna i [!INCLUDE[prod_short](includes/prod_short.md)] lokalt måste du registrera [!INCLUDE[prod_short](includes/prod_short.md)] som en app i Azure-portalen och sedan ansluta [!INCLUDE[prod_short](includes/prod_short.md)] till programregistreringen. Följande avsnitt beskriver hur du gör detta.

### <a name="create-an-app-registration-for-prod_short-in-azure-portal"></a>Skapa en programregistrering för [!INCLUDE[prod_short](includes/prod_short.md)] i Azure Portal
De steg som ingår när du registrerar [!INCLUDE[prod_short](includes/prod_short.md)] i Azure Portal beskrivs i [Registrera ett program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). De inställningar som är specifika för e-postfunktionen är de delegerade behörigheter som du ger din programregistrering. Följande register anger minimibehörigheterna.

|API/behörighetsnamn  |Typ  |Beskrivning  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Delegerades|Logga in och läs användarprofilen.         |
|Microsoft Graph / Mail.ReadWrite |Delegerades|Skriv e-postmeddelanden.         |
|Microsoft Graph / Mail.Send|Delegerades|Skicka e-postmeddelanden.         |
|Microsoft Graph / offline_access|Delegerades|Behåll medgivande för dataåtkomst. <!--need to verify this-->|

> [!TIP]
> Notera följande information när du skapar din appregistrering. Du kommer att behöva den för att ansluta [!INCLUDE[prod_short](includes/prod_short.md)] till din app-registrering.
> 
> * Program-ID (klient) 
> * Omdirigerings-URI (valfritt)
> * Klienthemlighet

Allmänna riktlinjer om hur du registrerar en app finns i [Snabbstart: Registrera en app med Microsofts identitetsplattform](/azure/active-directory/develop/quickstart-register-app.md). 

### <a name="connect-prod_short-to-your-app-registration"></a>Anslut [!INCLUDE[prod_short](includes/prod_short.md)] till dina app-registrering
När du har registrerat ditt program i Azure Portal använder du den assisterade konfigurationen **AAD-registrering för e-postprogram** i [!INCLUDE[prod_short](includes/prod_short.md)] för att ansluta [!INCLUDE[prod_short](includes/prod_short.md)] till det.

1. I [!INCLUDE[prod_short](includes/prod_short.md)] väljer du ![Glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och anger **AAD-registrering för e-postprogram** innan du väljer tillhörande länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Om du ansluter för första gången kan du också köra den assisterade konfigurationsguiden **Konfigurera e-post**. Guiden kommer att kräva information för att ansluta till din programregistrering. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Azure Active Directory, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Azure AD Directory - Multitenant)** or **Accounts in any organizational directory (Any Azure AD Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Azure Active Directory, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## <a name="see-also"></a>Se även
[Delade postlådor i Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som din företagsinkorg i Outlook](admin-outlook.md)  
[Få [!INCLUDE[prod_short](includes/prod_short.md)] på min mobila enhet](install-mobile-app.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]