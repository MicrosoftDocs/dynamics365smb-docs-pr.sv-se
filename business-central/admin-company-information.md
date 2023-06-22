---
title: 'Företagsinformation, översikt'
description: 'På sidan Företagsinformation anges grundläggande information om en affärsenhet, till exempel namn, adresser och leveransinformation.'
author: edupont04
ms.topic: conceptual
ms.search.form: 1
ms.date: 08/31/2022
ms.author: edupont
---

# <a name="company-information-overview" />Företagsinformation, översikt

[!INCLUDE[prod_short](includes/prod_short.md)] organiserar affärsenheter i *företag*. För varje företag måste du fylla i en del av den grundläggande företagsinformationen och relevant information på sidan **Företagsinformation**. Informationen på sidan [**Företagsinformation**](https://businesscentral.dynamics.com/?page=1) används i dokument, exempelvis fakturasidhuvuden. Du kan skapa flera företag, t.ex. ett moderbolag och ett dotterbolag.  

Om företagets inventeringslager finns på en annan adress än företagets huvudkontor kan du fylla i de olika leveransadressfälten och fältet **Platskod** på snabbfliken **Leverans**. Informationen i dessa fält skriv därefter ut på t.ex. inköpsorder så att leverantörer kan skicka artiklarna till rätt plats.  

För respektive företag som du skapar måste du fylla i sidan **Företagsinformation** samt sidan **Redovisningsinställning**. Du måste också ställa in respektive område i [!INCLUDE [prod_short](includes/prod_short.md)], till exempel sidan **Försäljningsinställningar** för respektive företag. Läs mer i [Översikt över uppgifter som ska konfigureras [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

Sidan **Företagsinformation** innehåller olika fält och snabbflikar, beroende på land. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] I följande tabell beskrivs de mest använda snabbflikarna.

[!INCLUDE [admin-company-info-fasttabs](includes/admin-company-info-fasttabs.md)]

När du har fyllt i informationen kan du stänga sidan.  

## <a name="working-with-multiple-companies" />Arbeta med flera företag

Om din version av [!INCLUDE [prod_short](includes/prod_short.md)] inkluderar flera företag, kanske användarna vill använda *företagetsbrickor* för att snabbt kunna identifiera och hålla reda på vilket företag de arbetar i just nu. För mer information, se [Visa en företagsbricka](#badge).

Det finns några funktioner som du kan använda för att växla mellan företag medan du arbetar, som företagsväxlaren (<kbd>Ctrl</kbd>+<kbd>O</kbd>). Läs mer i [Byta till ett annat företag eller en annan miljö](ui-organization-switch.md).

## <a name="a-namebadgeadisplay-a-company-badge" /><a name="badge"></a>Visa en företagsbricka

När det finns mer än ett företag eller miljö visas företagsväxlaren i det övre högra hörnet av programfältet, nära sökikonen i programfältet. Som standard använder företaget en standardföretagsbricka, t.ex ![företagsikon Launcher.](media/ui-experience/company-icon.png "Visar företagsväxlingsikonen som används när det finns en enda miljö") och ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Visar företagsväxlingsikonen som används när det finns flera miljöer").

:::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Visar företagsväxlarikonen i sidhuvudet till Business Central-klienten.":::  

Med hjälp av sidan **Företagsinformation** kan du ersätta standardföretagsikonen med en anpassad bricka per företag, om företagsbrickan gör det enklare för användare att identifiera företaget de arbetar i.

1. I snabbfliken **Företagsbricka** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
2. När du är klar uppdaterar du webbläsaren (tryck på <kbd>Ctrl</kbd>+<kbd>F5</kbd>) för att uppdatera brickan i klienten.  

> [!NOTE]
> Företagsväxlaren infördes i utgivningscykel 2 år 2022, version 21. I tidigare versioner används företagsbrickan inte för växling av företag. Den visas i det övre högra hörnet på de flesta sidorna, även om det bara finns ett företag. Om du väljer det här alternativet visas företagets fullständiga namn och miljöns namn.

## <a name="change-company-display-name" />Ändra företagets visningsnamn

Företagsnamnet visas alltid i det övre vänstra hörnet och fungerar som en åtgärd som du kan välja att gå tillbaka till rollcentret. Du kan ändra det här namnet på sidan **företagsinformation**.

1. Välja ![Kugghjulsikon för att öppna menyn Inställningar.](media/ui-experience/settings_icon_small.png) och sedan åtgärden **Företagsinformation**.
2. Ange det nya företagsnamnet i fältet **Namn**.
3. Lämna sidan. Systemet startas om och det nya företaget visas i det övre vänstra hörnet.

## <a name="experience" />Upplevelse

Standardgränssnittet i utvärderingsversionen av [!INCLUDE [prod_short](includes/prod_short.md)] innehåller inte alla funktioner. Du kan aktivera den fullständiga upplevelsen på sidan **Företagsinformation**. Mer information finns i [ändra vilka funktioner som visas](ui-experiences.md).  

## <a name="see-related-microsoft-trainingtrainingmodulescreate-new-companies-dynamics--business-central" />Se relaterad [Microsoft utbildning](/training/modules/create-new-companies-dynamics-365-business-central/)

## <a name="see-also" />Se även

[Översikt över arbetsuppgifter att ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Företagsinformation – Snabbstart](quick-start-company-information.md)  
[Ställa in företagsinformation i Italien](LocalFunctionality/Italy/how-to-set-up-company-information.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Skapa nya företag](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
