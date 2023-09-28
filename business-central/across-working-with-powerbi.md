---
title: Arbeta med Power BI-rapporter i Business Central| Microsoft Docs
description: 'Hämta insikter, business intelligence och KPI:er från dina Business Central-data med hjälp av Power BI.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="work-with-power-bi-reports-in-"></a>Arbeta med Power BI-rapporter i [!INCLUDE [prod_short](includes/prod_short.md)]

I den här artikeln får du lära dig det grundläggande inom att visa Power BI-rapporter i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="overview"></a>Översikt

Power BI-rapporter ger dig insikter i [!INCLUDE[prod_short](includes/prod_short.md)]. Olika sidor i [!INCLUDE [prod_short](includes/prod_short.md)] omfattar en Power BI-rapportdel som kan visa Power BI-rapporter. Rollcentret är en typisk sida som visar en Power BI-rapportdel. Vissa listsidor, exempelvis **Objekt**, omfattar också en Power BI-del.

[!INCLUDE [prod_short](includes/prod_short.md)] fungerar tillsammans med Power BI-tjänsten. Rapporter som ska visas i [!INCLUDE [prod_short](includes/prod_short.md)] lagras i en Power BI-tjänst. I [!INCLUDE [prod_short](includes/prod_short.md)] kan du växla mellan den rapport som visas i Power BI-delen till valfri Power BI-rapport som finns i din Power BI-tjänst. Första gången du loggar in på [!INCLUDE [prod_short](includes/prod_short.md)] och ända fram tills du ansluter till en Power BI-tjänst kommer delarna att vara tomma enligt följande:

![Power BI-del i Business Central.](./media/power-bi-part.png)

## <a name="get-started"></a>Kom igång

### <a name="prerequisites"></a>Förutsättningar

Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt måste det aktiveras för Power BI-integrering. Denna uppgift utförs vanligtvis av en administratör. Mer information finns i [Konfigurera [!INCLUDE[prod_short](includes/prod_short.md)] lokalt för Power BI-integrering](admin-powerbi-setup.md#setup).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] har redan konfigurerats för integrering med Power BI.

### <a name="sign-up-power-bi"></a>Registrera dig för Power BI

Innan du kan använda Power BI med [!INCLUDE[prod_short](includes/prod_short.md)] måste du registrera dig för Power BI-tjänsten. Gå till [https://powerbi.microsoft.com](https://powerbi.microsoft.com) om du inte redan har registrerat dig. När du registrerar dig använder du din e-postadress för arbetet samt ditt lösenord.

## <a name="connect-to-power-bi---one-time-only"></a><a name="connect"></a>Anslut till Power BI – endast en gång

När du loggar in på [!INCLUDE [prod_short](includes/prod_short.md)] för första gången kan du komma att se en tom Power BI-del på olika sidor (som visas i föregående illustration). Det första du måste göra är att ansluta till ditt Power BI-konto. När du väl är ansluten kan du se rapporterna. Du behöver bara utföra detta steg en enda gång.

1. Välj länken **Komma igång med Power BI** i delen **Power BI-rapporter**.
2. **Konfigurera Power BI-rapporter i Business Central** assisterad konfiguration startar. Välj **Nästa** om du vill fortsätta.
3. På sidan **Kontrollera din Power BI-licens**. Gör något av följande:

    - Om du ännu inte har registrerat dig för Power BI väljer du [Gå till Power BI hemsidan](https://powerbi.microsoft.com). Registrera dig för ett konto och kom sedan tillbaka till [!INCLUDE[prod_short](includes/prod_short.md)] och avsluta konfigurationen.

    - Om du redan har en licens väljer du **Nästa**.
4. På nästa sida [!INCLUDE[prod_short](includes/prod_short.md)] laddas nu en demorapport upp till Power BI. Detta tar några minuter, så det görs i bakgrunden. Om du vill slutföra installationen väljer du **Nästa** och **Slutför** sedan .

Anslutningsprocessen startar. I samband med processen kommunicerar [!INCLUDE [prod_short](includes/prod_short.md)] med Power BI-tjänsten i syfte att avgöra om du har ett giltigt Power BI-konto och -licens. När din licens väl har verifierats kommer förvald Power BI-rapport att visas på sidan. Om ingen rapport visas kan du välja en rapport i avsnittet.

> [!TIP]
> Med [!INCLUDE [prod_short](includes/prod_short.md)] online kommer detta steg automatiskt att ladda upp Power BI-standardrapporter som används i [!INCLUDE [prod_short](includes/prod_short.md)] till din Power BI-arbetsyta.

#### <a name="from--on-premises"></a>Från [!INCLUDE [prod_short](includes/prod_short.md)] lokalt

Ansluta till Power BI från [!INCLUDE [prod_short](includes/prod_short.md)] liknar att göra det online. På sidan **TJÄNSTEBEHÖRIGHETER FÖR AZURE ACTIVE DIRECTORY** kan du emellertid uppmanas att bevilja åtkomst till Power BI-tjänster. Välj **Auktorisera Azure-tjänster** och sedan **Godkänn** om du vill bevilja åtkomst.

När du väl är ansluten kan du välja en rapport i Power BI-delen på olika sidor.

## <a name="work-with-power-bi-reports"></a>Arbeta med Power BI-rapporter

### <a name="show-reports-on-list-pages"></a>Visa rapporter på listsidor

[!INCLUDE[prod_long](includes/prod_long.md)] omfattar en Power BI-FactBox på flertalet viktiga listsidor. Denna faktabox ger ytterligare insikter kring datan i listan. I takt med att du förflyttar dig mellan raderna i listan uppdateras samt filtreras rapporten för vald post.

Mer information om hur du skapar rapporter för listasidor finns i [Skapa Power BI-rapporter för visning av listdata i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

> [!TIP]
> Om du inte ser Power BI-faktaboxen kan det hända att en är dold på arbetsytan på grund av anpassning. Välj ikonen ![Inställningar.](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och välj sedan åtgärden **Anpassa**. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).
>
> Om du har en äldre version av Business Central går du till åtgärdsfältet och väljer **Åtgärder** > **Visa** > **Visa/Dölj Power BI-rapporter**.

### <a name="switch-reports"></a>Växla rapporter

En Power BI-del på en sida kan visa valfri Power BI-rapport som gjort tillgänglig för dig. Om du vill växla till en annan rapport väljer du åtgärden **Välj rapport** i kommandolistrutan högst upp i delen.  

Sidan **Power BI-rapporturval** visar en lista över samtliga Power BI-rapporter som du har åtkomst till. Listan hämtas från alla egna arbetsytor eller arbetsytor som har delats med dig i Power BI-tjänsten. Markera rutan **Aktivera** för samtliga rapporter som du vill visa på sidan, och välj sedan **OK**. Du återgår då till sidan och den senast aktiverade rapporten visas. I kommandolistrutan använder du kommandona **Föregående** och **Nästa** för att navigera mellan olika rapporter.  

### <a name="get-more-reports"></a>Få fler rapporter

Om du inte kan se några rapporter på sidan **Power BI-rapporturval**, eller om du inte kan se den rapport du vill, väljer du **Hämta rapporter**. Med hjälp av denna åtgärd kan du söka efter rapporter från två olika platser: *Min organisation* eller *Tjänster*.

- Välj **Min organisation** för att gå till Power BI-tjänsterna. Härifrån kan du visa de rapporter som finns inom din organisation och som du är berättigad att visa. Du kan sedan lägga till dem i din arbetsyta.
- Välj **tjänster** för att gå till Microsoft AppSource där du kan installera Power BI-appar.  

> [!TIP]
> Om du har Power BI Desktop kan du också skapa nya Power BI-rapporter. När dessa rapporter väl har publicerats på din Power BI-arbetsyta kommer de också att visas på sidan **Power BI-rapporturval**.  

### <a name="manage-and-modify-reports"></a>Hantera och ändra rapporter

Du kan utföra ändringar i en rapport i Power BI-delen. De ändringar som du utför publiceras sedan i Power BI-tjänsten. Om rapporten delas med andra användare kommer dessa också att se förändringarna, förutsatt att du inte sparar ändringarna i en ny rapport.

Om du vill ändra en rapport väljer du åtgärden **Hantera rapport** i kommandolistrutan i Power BI-delen. Du kan därefter börja göra dina ändringar. När du är färdig med dina ändringar väljer du **Arkiv** > **Spara**. Om det rör sig om en delad rapport och du inte vill genomföra ändringen för samtliga användare väljer du **Spara som**.

När du återgår till rollcentret visas den uppdaterade rapporten. Om du har använt **Spara som** måste du välja **Välj rapport** och sedan aktivera den nya rapporten för att visa den.

> [!NOTE]
> Denna funktion är ej tillgänglig med [!INCLUDE [prod_short](includes/prod_short.md)] lokalt.

### <a name="upload-reports"></a><a name="upload"></a>Ladda upp rapporter

Power BI-rapporter kan distribueras bland användarna som .pbix-filer. Om du har .pbix-filer kan du ladda upp och dela dessa med samtliga [!INCLUDE [prod_short](includes/prod_short.md)]-användare. Rapporterna delas i respektive företag i [!INCLUDE [prod_short](includes/prod_short.md)].  

Om du vill ladda upp en rapport väljer du åtgärden **Ladda upp rapport** i kommandolistrutan i delen **Power BI-rapporter**. Leta sedan upp den .pbix-fil som anger de rapporter du vill dela. Du kan ändra standardnamn på filen.  

När rapporten laddas upp till din Power BI-arbetsyta kommer den automatiskt att laddas upp även till andra användares Power BI-arbetsytor.

> [!NOTE]
> För att kunna ladda upp en rapport måste du ha användarbehörigheten SUPER i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan heller inte ladda upp rapporter med [!INCLUDE [prod_short](includes/prod_short.md)] lokalt. Med den lokala versionen laddar du upp rapporter direkt till din Power BI-arbetsyta. Mer information finns i [Arbeta med [!INCLUDE [prod_short](includes/prod_short.md)]-data i Power BI](across-working-with-business-central-in-powerbi.md).

## <a name="fixing-problems"></a>Åtgärda problem

Om något går fel innehåller det här avsnittet emellertid lösningar för de flesta vanliga problem.  

### <a name="you-dont-have-a-power-bi-account"></a>Du har inget Power BI-konto

Inget Power BI-konto har konfigurerats. Om du vill ha et giltigt Power BI-konto måste du ha en licens, och du måste dessutom tidigare ha loggat in på Power BI för att skapa en Power BI-arbetsyta.

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Meddelande: Det finns inga aktiverade rapporter. markera Välj rapport för att visa en lista över rapporter som kan visas.

Detta meddelande visas om den förvalda rapporten inte lyckas distribuera din Power BI-arbetsyta. Alternativt har de distribuerats men inte uppdaterats korrekt. Gå till rapporten på din Power BI-arbetsyta och välj **Datauppsättning** och **Inställningar**, och uppdatera sedan autentiseringsuppgifterna manuellt. När datauppsättningen har uppdaterats går du tillbaka till [!INCLUDE[prod_short](includes/prod_short.md)] och väljer rapporten manuellt på sidan **Välj rapporter**.

#### <a name="you-cant-see-a-report-on-the-select-report-page-on-a-list-page"></a>Du kan inte se en rapport på sidan Välj rapport på en listsida

Detta beror troligen på att rapportens namn inte innehåller listsidans namn. Rensa filtret om du vill få en komplett lista över tillgängliga Power BI-rapporter.

## <a name="see-also"></a>Se även

[Business Central och Power BI](admin-powerbi.md)  
[Skapa Power BI-rapporter för att visa [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md)  
[Power BI-integreringskomponent och arkitekturöversikt för [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Arbeta med [!INCLUDE [prod_short](includes/prod_short.md)]-data i Power BI](across-working-with-business-central-in-powerbi.md)  
[Power BI för konsumenter](/power-bi/consumer/end-user-consumer)  
[Power BI-tjänstens "nya utseende"](/power-bi/service-new-look)  
[Snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Dokumentation om Power BI](/power-bi/)  
[Affärsstöd](bi.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Importera affärsdata från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakälla](across-how-use-financials-data-source-powerapps.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
