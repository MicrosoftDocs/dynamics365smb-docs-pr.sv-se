---
title: Visa anpassade Power BI-rapporter för Business Central-data | Microsoft Docs
description: Du kan använda Power BI-rapporter för att få ytterligare information om data i listor.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6c818940357ed21a994e7553517989a0c16accec
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379279"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a>Skapa Power BI-rapporter för att visa listdata i [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] omfattar ett FactBox-styrelement på ett antal viktiga listsidor som ger ytterligare insikt i listdatan. När du flyttar mellan rader i listan uppdateras rapporten och filtrerats för den valda transaktionen. Du kan skapa anpassade rapporter och visa dessa i denna kontroll. Det finns emellertid några regler som måste följas för att rapporterna ska fungera som förväntat.  

## <a name="prerequisites"></a>Förutsättningar

- Ett Power BI-konto.
- Power BI Desktop.

Mer information om hur du kommer igång finns i [Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakälla](across-how-use-financials-data-source-powerbi.md).

## <a name="defining-the-report-data-set"></a>Definiera rapportens datauppsättning

Ange den datakälla som innehåller datan som är relaterad till listan. För att kunna skapa en rapport för Sales-listan måste du säkerställa att datauppsättningen innehåller säljrelaterad information.  

## <a name="defining-the-report-filter"></a>Definiera rapportfiltret

Om du vill uppdatera datan för vald post i listan lägger du till ett filter i rapporten. Detta filter måste omfatta ett fält för den datakälla som används som *primär nyckel*. Oftast är primärnyckeln för en lista **nr.** .

Om du vill definiera ett filter för rapporten, markera primärnyckel i listan över tillgängliga fält och dra och släpp fältet i avsnittet **rapportfilter**. Filtret måste vara ett grundläggande rapportfilter som definierats för alla sidor. Det får inte vara ett sid-, visuellt eller avancerat filter.

![Ange rapportfiltret för rapporten Försäljningsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a>Ställa in rapportens storlek och färg

Storleken på rapporten måste anges till 325 x 310 pixlar. Denna storlek tillhandahåller rapportens korrekta dimensioner på det tillgängliga utrymmet för Power BI FactBox-kontrollen i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du vill definiera storleken på rapporten, lägger du fokus utanför rapportens layoutområde och klickar på ikonen färgrulle.

![Ange rapportens bredd och höjd för rapporten Försäljningsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Du kan ändra bredd och höjd på rapporten genom att välja **anpassaval** i fältet **typ**.

Om du vill att rapportens bakgrund ska smälta samman med bakgrundsfärgen i Power BI FactBox-kontrollen anger du rapportens bakgrundsfärg som *#FFFFFF*. 

## <a name="using-reports-with-multiple-pages"></a>Använda rapporter med flera sidor

Du kan skapa en rapport med flera sidor med Power BI. För rapporter som visas med listsidor rekommenderas emellertid inte att dessa har mer än en sid. Power BI FactBox visar endast rapportens första sida.

## <a name="naming-the-report"></a>Namnge rapporten

Ge rapporten ett namn som innehåller namnet på den listsida som är kopplad till rapporten. Om rapporten exempelvis avser listsidan **Leverantör** ska du inkludera ordet *leverantör* någonstans i namnet.  

Denna namngivningskonvention är inget krav. Den underlättar emellertid valet av rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]. När valsidan för rapporter öppnas från en listsida filtreras den automatiskt baserat på sidans namn. Denna filtrering sker i syfte att begränsa den rapport som visas. Användare som vill få en komplett lista över de rapporter som finns tillgängliga i Power BI kan rensa filtret.  

## <a name="fixing-problems"></a>Åtgärda problem

Detta avsnitt ger dig lösningarna på de vanligaste problem som kan uppstå när du skapar Power BI-rapporten.  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a>Rapporter kan inte visas på sidan Välj rapport.

Detta beror troligen på att rapportens namn inte innehåller listsidans namn. Rensa filtret om du vill få en komplett lista över tillgängliga Power BI-rapporter.  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Rapporten laddas in men är tom, ofiltrerad eller felaktigt filtrerad.

Bekräfta att rapportens filter innehåller korrekt primärnyckel. I de flesta fall består detta fält av fältet **Nr.** , men i tabellen **G/L-post** måste du till exempel använda fältet **Inläggsnr.**.

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Rapporten laddas men visar en oväntad sida

Bekräfta att den sida du vill visa är den första sidan i rapporten.  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Rapporten visas med en oönskad grå ram eller är för stor/för liten

Kontrollera att rapportens storlek är 325 pixlar x 310 pixlar. Spara rapporten och uppdatera sedan listsidan.  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Aktivera dina affärsdata för Power BI](admin-powerbi.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI datakälla](across-how-use-financials-data-source-powerbi.md)  
[Komma igång](product-get-started.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Ekonomi](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]