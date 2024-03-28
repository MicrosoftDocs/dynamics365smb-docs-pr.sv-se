---
title: Byta till ett annat företag eller annan miljö
description: Om du arbetar i flera organisationer kan du snabbt växla mellan olika miljöer och företag.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'environments, companies, tenants, organization'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/16/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Byta till ett annat företag eller annan miljö

[!INCLUDE [prod_short](includes/prod_short.md)] finns i många olika länder/regioner och stöder många olika typer av organisationer. Organisationen kan välja att organisera arbetet i [!INCLUDE [prod_short](includes/prod_short.md)] i flera *företag* och *miljöer*. I den här artikeln får du hjälp att förstå de viktigaste skillnaderna och hur du arbetar med dem.

## Om företag och miljöer

[!INCLUDE [company_environment](includes/company_environment.md)]

> [!TIP]
> Om du ofta byter mellan olika företag eller arbetar med [!INCLUDE[prod_short](includes/prod_short.md)] inifrån en annan app som exempelvis Microsoft Teams, kan det vara lätt att tappa orienteringen. För att du ska kunna hålla reda på saker och ting kan du lägga till ett märke som visar företagsnamnet, detta så att du snabbt kan kontrollera att du befinner dig på rätt plats. För mer information, se [Visa en företagsbricka](admin-company-information.md#badge).
> 
> Beroende på webbläsaren kan du också fästa de olika företagen i ditt favoritfält.  

<!--
[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]-->

## Funktioner för att byta företag eller miljö

Det finns några funktioner som du kan använda för att byta företag eller miljö medan du arbetar. I följande tabell jämförs funktionens funktioner, som beskrivs närmare i de avsnitt som följer.

|Funktion|Växla företag|Växla miljö|Växla i ny flik i webbläsaren| Tillgänglig lokalt|
|-------|--------------|------------------|-------------------------|----------------------|
|[Företagsväxlare](#use-the-company-switcher)|![bock](media/check.png "kontroll")|![bock](media/check.png "kontroll")|![bock](media/check.png "kontroll")|![bock](media/check.png "kontroll")|
|[Appstartare](#use-the-app-launcher)||![bock](media/check.png "kontroll")|![bockmarkering](media/check.png "kontroll")||
|[Mina inställningar](#use-my-settings)|![bockmarkering](media/check.png "kontroll")|||![bock](media/check.png "kontroll")|
|[Företagsnav](#use-company-hub)|![bock](media/check.png "kontroll")|![bock](media/check.png "kontroll")|![bock](media/check.png "kontroll")||

## Använd företagsväxlaren

Att använda företagsväxlaren är troligen det snabbaste och mest mångsidiga sättet att byta företag. Företagsväxlaren är en ruta som är lätt tillgänglig från valfri sida. I fönstret får du en översikt över alla företag i alla miljöer som du har tillgång till, och du kan växla direkt till någon av dem&mdash;antingen på samma flik i webbläsaren eller på en ny. Det är särskilt användbart när du arbetar i många företag i olika miljöer.

1. I övre högra hörnet, nära sökikonen, visas antingen standardföretagsikonen, som t.ex ![företagsikon Launcher.](media/ui-experience/company-icon.png "Visar företagsväxlingsikonen som används när det finns en enda miljö") och ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Visar företagsväxlingsikonen som används när det finns flera miljöer") eller en [anpassad bricka](admin-company-information.md#badge) för det företag som du arbetar med för närvarande. Välj ikonen för att öppna företagsväxlaren.

   :::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Visar företagsväxlarikonen i sidhuvudet till Business Central-klienten.":::  

   > [!TIP]
   > Du kan också använda kortkommandot <kbd>Crtl</kbd>+<kbd>O</kbd> för att öppna fönstret.
2. I rutan **Tillgängliga företag** väljer du det företag som du vill byta till, väljer pilen **Växla** och väljer sedan ett av följande alternativ:

   |Alternativ|Description|
   |------|-----------|
   |Ändra|Öppnar rollcentret för det valda företaget i samma webbläsare som du arbetar i. Företaget blir standardföretag som öppnas i Business Central tills du växlar igen eller ändrar företaget med hjälp av **Mina inställningar**. |
   |Öppna på en ny flik|Öppnar rollcentret för det valda företaget i en ny flik i webbläsaren och håller det ursprungliga företaget öppet i en annan flik.|
   |Öppna på ny flik och gå till samma sida|Det här alternativet är endast aktivt på listsidor, till exempel kunder, försäljningsorder eller artiklar. Då öppnas samma lista, men för det valda företaget, i en ny flik i webbläsaren. |

> [!TIP]
> Välj <kbd>F5</kbd> om du vill uppdatera listan över miljöer och företag.

## Använd appstartaren

När du har loggat in på [!INCLUDE[prod_short](includes/prod_short.md)] visas de miljöer som du har åtkomst till på startsidan för Office.com.  

1. Välj ikonen **Appstartare** ![Appstartare.](media/app-launcher-icon.png "Programmarstartbild ger till gång till fler funktioner").
2. I rutan som öppnas söker du efter och väljer [!INCLUDE[prod_short](includes/prod_short.md)]. Om du inte ser [!INCLUDE[prod_short](includes/prod_short.md)], välj **Alla appar**, ange sedan **Business Central** i rutan **Sökning**.

   :::image type="content" source="media/app-launcher-bc-tile.png" alt-text=" Microsoft 365 programmarstartbild visar Business Central-panelen.":::  

3. Om det finns mer än en miljö blir du ombedd att välja vilken miljö du vill ha åtkomst till.

<!--
The following image shows tiles for accessing production and sandbox environments on the Dynamics 365 Home page.

:::image type="content" source="media/app-picker-environments.png" alt-text="The Dynamics 365 Home page showing production and sandbox environments.":::
-->
## Använd Mina inställningar

När du är inloggad i [!INCLUDE[prod_short](includes/prod_short.md)] kan du snabbt byta till ett annat företag i samma miljö. När du har bytt blir det företag du väljer standardföretag och öppnas nästa gång du loggar in.

1. I det övre högra hörnet väljer du ikonen **Inställningar** ![Inställningar.](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och väljer sedan åtgärden **Mina inställningar**.

    > [!TIP]
    > Du kan också använda kortkommandot <kbd>Alt</kbd>+<kbd>T</kbd> för att snabbt öppna sidan mina inställningar.

2. På sidan **Mina inställningar** i fältet **Företag** välj företaget.  
3. Välj **OK**.

> [!TIP]
> Ett bra sätt att gå direkt till standardföretaget när du loggar in, och att inte behöva ange en miljö, är att lägga till URL-adressen i listan med favoriter när du har loggat in.

## Använd företagsnav

*Företagsnavet* är ett mycket specialiserat rollcenter som ger en ekonomisk översikt över företag och miljöer. Företagsnavet är tillgängligt som ett [tillägg](ui-extensions-company-hub.md) för att ge en instrumentpanel med sammanfattningsdata för varje företag som du har tillgång till. På hemsidan visas ekonomiska KPI:er samt en direkt länk till de enskilda miljöerna och företagen. Mer information finns i [Hantera arbete över flera företag i företagsnavet](company-hub.md).

[![Visar företagsnavsidan som innehåller en lista över alla företag.](media/company-hub.png)](media/company-hub.png#lightbox)  

## Se även

[Skapa nya företag i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Miljöer och företag (endast på engelska)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  
[Företagsinformation](admin-company-information.md)  
[Administrationscenter för Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
