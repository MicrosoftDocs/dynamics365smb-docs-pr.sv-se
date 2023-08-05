---
title: Hämtar Business Central-tillägget för Excel
description: Lär dig mer om hur du skaffar användarna Business Central-tilläggsprogram för Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.search.form: 1480
ms.search.keywords: 'Excel, add-in, centralized deployment, M365 admin center, individual acquisition, appsource'
ms.date: 10/07/2021
ms.author: jswymer
---
# Hämta Business Central-tillägget för Excel

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett tillägg för Excel som låter användare välja en **redigering i Excel** på vissa sidor för att öppna data i ett Excel-kalkylblad. Denna åtgärd är en annan än åtgärden **Öppna i Excel** eftersom den låter användare utföra ändringar i Excel och sedan återpublicera ändringarna i [!INCLUDE[prod_short](includes/prod_short.md)]

## Översikt

### Om tillägget

Tillägget kallas **Microsoft Dynamics Office-tillägg** och det kan installeras från [Office Store (AppSource)](https://appsource.microsoft.com/). När tillägget är installerat finns åtgärden **redigera i Excel** tillgänglig på de flesta list-och list dels sidor från ikonen **dela** ![Dela en sida i en annan app](media/share-icon.png). Mer information om hur du använder tillägg finns i [Visa och redigera i Excel från Business Central](across-work-with-excel.md).

> [!NOTE]
> Tillägget fungerar endast i Windows, inte macOS.

### Om distribution som administratör

Med [!INCLUDE[prod_short](includes/prod_short.md)] online finns det några distributionsalternativ som du kan använda för att hämta tillägget till användarna. Ett alternativ är *individuell anskaffning*, där du kan låta användarna installera själva tillägget. Med det här alternativet måste användarna ha behörighet att hämta filer från Office Store. Ett annat alternativ är att konfigurera *centraliserad distribution* i administrationscentret för Microsoft 365 så att tillägget automatiskt distribueras till hela organisationen, grupperna eller specifika användare. Centraliserad distribution gör det möjligt att få tillägget till användarna om organisationen inte ger användare åtkomst till Office Store.

För slutanvändaren skiljer sig installations upplevelsen från de två distributions scenarierna:

- Med individuellt förvärv, första gången användare väljer åtgärden **Redigera i Excel** öppnas fönstret **Nytt Office-tillägg** i Excel. För att du ska kunna installera tillägget väljer användaren att **lita på det här tillägget**, som i sin tur installerar tillägget direkt från Office Store. Användarna loggas sedan in för att [!INCLUDE[prod_short](includes/prod_short.md)] använda sitt användarnamn och lösenord.

- Med centraliserad distribution är det första gången användare väljer åtgärden **redigera i Excel**, tillägget installeras automatiskt i Excel från centraliserad distribution, inte till Office Store. Det enda som användarna behöver göra är att logga in på [!INCLUDE[prod_short](includes/prod_short.md)]

Med båda dessa distributionsalternativ är tillägget automatiskt konfigurerat för att ansluta till [!INCLUDE[prod_short](includes/prod_short.md)]. Ett tredje distributionsalternativ är en manuell installation av tillägget direkt från Excel. Med det här alternativet måste användarna konfigurera tillägget för att ansluta till [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="switch"></a>Växling från enskilda förvärv till centraliserad distribution eller på annat sätt

När du ändrar från ett enskilt förvärv av tillägget till centraliserad distribution eller tvärtom måste Excel-filer som användare skapat före övergången påverkas. Efter över gången kan användare fortfarande öppna eventuella Excel-kalkylblad som tidigare skapats med åtgärden **redigera i Excel** eller skapats manuellt genom att konfigurera Excel-tillägget. Men de kan inte uppdatera data i filen från Business Central eller push-uppdateringar till Business Central

Det här tillståndet orsakas av att varje Excel-fil tilldelas en tilläggsidentifierare. I över gången till eller från centraliserad distribution tilldelas ett annat ID, så det tidigare-ID:t blockeras.

## Förberedelse (endast lokalt)

[!INCLUDE[prod_short](includes/prod_short.md)] lokal kräver att miljön är konfigurerad för tillägget. Om så inte är fallet kommer åtgärden **redigera i Excel** inte att vara tillgänglig för användarna. Mer information finns i [skapa Excel-tillägget för redigering av Business Central data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) i hjälpen för utvecklare och IT-proffs.

## Distribuera tillägget med hjälp av centraliserad distribution

Centraliserad distribution är en funktion i administratörscentret för Microsoft 365 som du använder för att automatiskt installera tillägg i användarnas Office-appar, som Excel. För att hjälpa dig med centraliserad distribution [!INCLUDE[prod_short](includes/prod_short.md)] inkluderar assisterad konfiguration **Excel-tillägget centraliserad installation**.

### Innan du börjar

- Mer information om hur du förhindrar att användare hämtar från Office Store finns i [Hantera tillägg i administrationscenter](/microsoft-365/admin/manage/manage-addins-in-the-admin-center).
- Kontrol lera att centraliserad distribution fungerar för organisationen. Mer information finns i [avgöra om centraliserad distribution av tillägg fungerar för organisationen](/microsoft-365/admin/manage/centralized-deployment-of-add-ins)
- Om du övergår från enskild anskaffning läser du [Växla från enskild anskaffning till centraliserad distribution](#switch)

> [!NOTE]
> Om du aktiverar centraliserad distribution påverkas funktioner som använder Excel-tillägget, till exempel åtgärden **redigera i Excel**. Detta påverkar inte andra Excel-relaterade funktioner och behörigheter som har tilldelats användare i [!INCLUDE[prod_short](includes/prod_short.md)]

### Konfigurera centraliserad distribution för tillägg

Du arbetar i både [!INCLUDE[prod_short](includes/prod_short.md)] och administrationscentret för Microsoft 365.

1. I [!INCLUDE[prod_short](includes/prod_short.md)] välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikonen, ange **Excel-tillägget centraliserad distribution** och sedan väljer du relaterad länk.
2. Läs informationen på sidan **konfiguration av Business Central Excel-tillägg** och välj **Nästa**.
3. Logga in på [administrationscentret för Microsoft 365 ](https://go.microsoft.com/fwlink/?linkid=2163967) och gå sedan till **Integrerade appar**<!--**Add-ins**-->.

    Gör på följande sätt för att konfigurera tillägget för distribution från Office Store: 
    1. Välj **Hämta appar** för att öppna Office Store (AppSource). <!--**Deploy Add-in** 5. In the **Deploy a new add-in**, select **Choose from the store**.-->
    2. Sök efter **Microsoft Dynamics Office-tillägget** och välj **Hämta nu**. <!--On the **Select add-in** page, search for and select **Microsoft Dynamics Office Add-in** > **Add** > **Continue**.-->
    3. På sidan **Lägg till användare** ange vilka användare som du vill distribuera tillägget för och välj **Nästa**.<!--On the **Configure add-in**, specify the users that you want to deploy the add-in for.-->
    4. Granska **Godkänn begäran om behörigheter**, välj **Nästa** > **Slutför distribution**.
    5. Vänta tills den gröna bockmarkeringen bredvid **distribuerad** visas för tillägget och välj sedan **klar**. <!--Select **Deploy** and wait til successful, then **Next** > **Continue**.-->

       Tillägget visas på sidan **tillägg**. Mer information om distribution av tillägg i administrationscentret för Microsoft 365 finns i [Distribuera tillägg i aministrationscentret](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).
4. Gå tillbaka till den assisterade konfigurationen för **Centraliserad distribution för Excel-tillägg** i [!INCLUDE[prod_short](includes/prod_short.md)] och välj **Nästa**.
5. Aktivera **Använd centraliserad distribution** och klicka på **Slutför** .

    Om du inte aktiverar denna växel [!INCLUDE[prod_short](includes/prod_short.md)] hämtas tillägget direkt från Office Store.

När du är klar kan du alltid ändra distributionen i administrationscentret för Microsoft 365, som att tilldela fler användare. Mer information om distribution av tillägg i administrationscentret finns i [Distribuera tillägg i administrationscentret](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).

> [!IMPORTANT]
> Om du har mer än en miljö måste du köra assisterad konfiguration för **centraliserad distribution av Excel-tillägg** för varje miljö som du vill använda centraliserad distribution för. Du behöver emellertid inte konfigurera den centraliserade distributionen i Microsoft 365 på nytt. Det enda du behöver göra är att aktivera växeln **Använd centraliserad distribution** i guiden assisterad konfiguration. 

> [!NOTE]
> Det kan ta upp till 24 timmar innan användaren distribuerar tillägget automatiskt i Excel för användare.

## <a name="install"></a>Individuellt anskaffning: installera tillägget manuellt för egen användning

I de flesta fall installeras tillägget automatiskt när du öppnar Excel från Business Central, eller så uppmanas du att installera det. Det kan emellertid finnas fall där du måste installera tillägget manuellt.

1. Öppna Excel och öppna sedan en Excel-arbetsbok.
2. I menyn **Infoga** välj **Tillägg** > **Hämta tillägg**
3. Gå till **administrativt hanterat** och sök efter **Microsoft Dynamics Office-tillägg**. Om du ser där, markerar du den och väljer **Lägg till**. Om det inte visas går du till **Store** och söker efter *Microsoft Dynamics Office-tillägget* och följer instruktionerna på skärmen för att lägga till det.

När tillägget installeras visas det som en panel i Excel. Nu ska vi konfigurera anslutningen.

### Konfigurera Business Central anslutning

Om en användare inte kan ansluta automatiskt kan du häva blockeringen av dem genom att be dem göra följande:

1. I **Microsoft Dynamics** tilläggsrutan i Excel, välj **Lägg till serverinformation**. Om den inte visas väljer du ![knappen fler alternativ i Excel.](media/cogwheel.png) ikon högst upp för att öppna dialogrutan för alternativ. 
2. För [!INCLUDE[prod_short](includes/prod_short.md)] online, ange **Server-URL** till `https://exceladdinprovider.smb.dynamics.com`. För [!INCLUDE[prod_short](includes/prod_short.md)] lokal, ange URL för webbklienten som `https://myBCserver/190`.
3. Klicka på **OK** och bekräfta sedan att appen har laddats om.
4. När du uppmanas, logga in med ditt Business Central användarnamn och lösenord.
5. Välj alternativt den miljö och det företag du vill ansluta till.

Tilläggen är nu anslutna till [!INCLUDE [prod_short](includes/prod_short.md)], och du kan redigera data samt publicera ändringarna i [!INCLUDE [prod_short](includes/prod_short.md)].  

## Förbereda enheter och nätverk för Excel-tillägget

Nätverkstjänster som proxyservrar och brandväggar måste tillåta operationsföljd mellan varje klientenhet som tillägget är installerat på och många serviceslutpunkter. En lista över slutpunkter finns i [förbereda nätverket för Excel-tillägget](/dynamics365/business-central/dev-itpro/administration/configuring-network-for-addins).

## Felsökning

Ibland kan användare köra ett problem med Excel-tillägget. Det här avsnittet innehåller tips om hur du häver blockeringen av användare under vissa omständigheter.

|Problem  |Lösning eller problemlösning  |Kommentarer  |
|---------|---------|---------|
|Tillägget startar inte <br><br>Användaren får till exempel meddelandet "tillägg i varning: det här tillägget är inte längre tillgängligt." när du försöker använda tillägget. Det här problemet kan uppstå om den centraliserade distributionen är korrekt konfigurerad, men användaren inte har tilldelats åtkomst.|Kontrollera om tillägget distribueras centralt. Du kan även kontrollera om användaren har blockerats för att installeras lokalt. | Administratören kan konfigurera Office så att användarna inte kan hämta tillägg. I dessa fall måste administratören distribuera tillägget centralt. Mer information finns i [distribuera tillägg i administrationscenter](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).|
|Data läses inte in i Excel|Desta anslutningen genom att öppna ytterligare en lista i Excel från [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan dessutom öppna arbetsboken i Excel i en webbläsare.|Om användaren har angett ett företagsnamn som innehåller specialtecken kan tillägget inte ansluta. |
|Data kan inte publiceras tillbaka till [!INCLUDE [prod_short](includes/prod_short.md)].|Testa anslutningen genom att öppna arbetsboken i Excel i en webbläsare. |Ibland kan ett tillägg blockera publiceringsjobbet. Om sidan har utökats eller anpassats tar du bort tilläggen och försöker igen.|
|Datumen är felaktiga  |Datum och tid kan visas i Excel i ett annat format än [!INCLUDE [prod_short](includes/prod_short.md)]. Detta tillstånd innebär inte att informationen är inkorrekt, och datan i [!INCLUDE [prod_short](includes/prod_short.md)] blir inte rörig.|         |
|För vissa listsidor orsakar fel vid redigering av flera rader i Excel. Det här problemet kan uppstå om OData-anrop innehåller FlowFields och fält utanför repeater-kontrollen.|På sidan **webbtjänster** markerar du kryssrutorna **Uteslut icke-redigerbara FlowFields** och **Uteslut fält utanför repeater** för den publicerade sidan. Om du markerar dessa kryssrutor utesluter du icke-redigerbara FlowFields och fält från eTag-beräkningen. |Dessa kryssrutor är som standard dolda. Om du vill visa dem på sidan **webbtjänster** använder du [anpassning](/dynamics365/business-central/ui-personalization-user). |
|Användare kan inte längre logga in i tillägget. När de försöker logga in avbryts åtgärden utan att slutföras.| Det här problemet kan orsakas av en uppdatering som vi gjort i tillägget, någon gång i juli 2022. Mer information och en korrigering finns i [ändra konfigurationen för Excel-tillägget så att den stöder 2022-uppdateringen för juli](/dynamics365/business-central/dev-itpro/administration/update-excel-addin-configuration).|Gäller [!INCLUDE [prod_short](includes/prod_short.md)] endast lokalt|

<!--
## Deploy the Excel add-in for Business Central online

For [!INCLUDE [prod_short](includes/prod_short.md)] online, the administrator can deploy the add-in for all users. But users can also install the add-in themselves, provided they have permission to configure their Office experience.  

> [!TIP]
> In some organizations, administrators cannot deploy add-ins centrally. For more information, see [Determine if Centralized Deployment of add-ins works for your organization](/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).

### To deploy the Excel add-in for all users

1. As the administrator, sign in to the Microsoft commercial website and find the add-in at [https://appsource.microsoft.com/product/office/WA104379629](https://appsource.microsoft.com/product/office/WA104379629).
2. Choose the **Get it now** button.

    You'll be redirected to the Microsoft 365 admin center.
3. In the left panel, go to **Settings**, and then choose **Add-ins**.
4. In the **Configure add-in** pane, specify which users to grant access to the add-in.
5. Save your changes.


### To add the Excel add-in locally

1. Open Excel, and then open any Excel workbook.
2. On the **Insert** menu, choose **Office Add-ins**, and then choose **Admin managed** or **Store** as appropriate.
3. Search for *Dynamics Office Add-In*, and then install the add-in.

When the add-in is installed, it shows up as a panel in Excel. Next, you must configure the connection.

> [!TIP]
> If the workbook is not automatically saved to the user's OneDrive, then recommend them to save all workbooks that they export from [!INCLUDE [prod_short](includes/prod_short.md)].When they open the workbook again, the connection is still available, so they do not have to configure the connection again.

> [!NOTE]
> In certain deployments, the administrator must configure network access to unblock the Excel add-in. For more information, see [Preparing Your Network for the Excel Add-In](configuring-network-for-addins.md).-->

## Se relaterad [Microsoft utbildning](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Se även

[Analysera bokslut i Microsoft Excel](finance-analyze-excel.md)  
[Arbeta med Business Central](ui-work-product.md)  
[Förbättringar av Excel-integrering i 2019 utgivningsplan, våg 2](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
