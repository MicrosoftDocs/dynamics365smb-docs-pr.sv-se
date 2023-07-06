---
title: Analysera rapportdata med Excel och XML
description: Lär dig att använda Excel och XML för att analysera en rapportdatauppsättning.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.date: 03/16/2022
ms.author: jswymer
---
# <a name="analyzing-report-data-with-excel-and-xml"></a><a name="analyzing-report-data-with-excel-and-xml"></a><a name="analyzing-report-data-with-excel-and-xml"></a>Analysera rapportdata med Excel och XML

[!INCLUDE[2021_releasewave2](includes/2021_releasewave2.md)]

Som utvecklare eller avancerade användare hjälper det att kontrollera data som genereras för en viss rapportdatauppsättning medan du skapar nya rapporter eller ändrar befintliga. För att stödja denna funktion kan du exportera en rapportdatauppsättning som rådata till en Excel-arbetsbok eller XML-fil&mdash;direkt. I Excel kan du göra ad hoc-analyser av data och diagnostisera problem.

## <a name="get-started"></a><a name="get-started"></a><a name="get-started"></a>Kom igång

För att exportera en rapportdatauppsättning till en Excel-arbetsbok eller XML-fil, öppna rapporten i klienten och välj sedan på begäran sidan **Skicka till to** > **Microsoft Excel dokument (endast data)** eller **XML-dokument**. Filen hämtas till enheten.

## <a name="more-about-excel-data-only"></a><a name="more-about-excel-data-only"></a><a name="more-about-excel-data-only"></a>Mer om Excel (endast data)

Alternativet **Microsoft Excel-dokument (endast data)** exporterar rapportresultaten och de kriterier som användes för att generera dem&mdash;men det innehåller inte rapportlayouten. Excel-filen innehåller den fullständiga datauppsättningen, som rådata, ordnade i rader och kolumner. Alla datakolumner i rapportens datauppsättning ingår, oavsett om de används i rapportlayouten eller inte.

När du har Excel-filen kan du börja analysera datan. Du kan t.ex. filtrera data och använda Power Pivot för att visa dem.

Varje gång du exporterar resultat skapas ett nytt kalkylblad. Med alternativet **Microsoft Excel-dokument (endast data)** kan du köra samma rapport och återanvända formateringsändringar. Till exempel för Power Pivot kan du köra rapporten igen för en annan tidsperiod, kopiera resultatet till kalkylbladet och sedan uppdatera kalkylbladet. Du kan också söka efter en rapporteringsapp på [AppSource](https://appsource.microsoft.com/).

> [!NOTE]
> Du kan inte exportera en rapport som har fler än 1 048 576 rader eller 16 384 kolumner. Med Business Central lokal kan maximalt antal exporterade rader vara ännu mindre. Business Central Server innehåller en konfigurationsinställning, som kallas **maximalt antal data rader som kan skickas till Excel** för att minska gränsen från det maximala värdet. Mer information finns i [Konfigurera Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) eller kontakta administratören.

## <a name="for-administrators"></a><a name="for-administrators"></a><a name="for-administrators"></a>För administratörer

- **Microsoft Excel-dokument (endast data)** introducerades som en valfri funktion i 2021 utgivningscykel 1, uppdatering 18,3. Om du vill ge användarna åtkomst till den här funktionen med utgivningscykel 1 år 2021 måste du aktivera uppdateringen av funktionen **Spara rapportdatauppsättning till Microsoft Excel-dokument** i **Funktionshantering**. Mer information finns i [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management). I utgivningscykel 2 år 2021 blev den här funktionen permanent, så du behöver inte aktivera den.

- Om du vill använda **Microsoft Exceldokument (endast data)** måste du ha behörigheten **Tillåt export av rapportdatauppsättning till Excel**. Du kan ge användarna den här behörigheten genom att tilldela någon av behörighetsuppsättningarna **Felsökningsverktyg** eller **Exportera rapport till Excel**. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  

## <a name="for-developers-and-advanced-users"></a><a name="for-developers-and-advanced-users"></a><a name="for-developers-and-advanced-users"></a>För utvecklare och erfarna användare

Alternativet **Microsoft Excel-dokument (endast data)** exporterar alla kolumner, inklusive kolumner som innehåller filter och formateringsregler för andra värden. Här följer några intressanta punkter:

- Binära data i ett fält exporteras inte som en bild.

  I kolumner som innehåller binära data kommer fälten att inkludera **binära data ({0} byte)**, där **{0}** anger antalet byte.
- Från och med Business Central 2021 utgivningscykel 2 innehåller Excel-filen också kalkylarket **rapport med metadata**.

  I det här kalkylarket visas de filter som används i rapporten och de allmänna rapport egenskaperna, som namn, ID och tilläggsinformation. Filtren visas i kolumnen **Filter (DataItem::Table::FilterGroupNo::FieldName)**. Filtren i den här kolumnen inkluderar filter som är inställda på rapportens sida med begäran. Den innehåller även filter som definierats i AL-kod, till exempel av [egenskapen DataItemLink](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) och [egenskapen DataItemTableView](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Mer information om rapportdesign finns i [rapport översikt](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Arbeta med rapporter](ui-work-report.md)  
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
