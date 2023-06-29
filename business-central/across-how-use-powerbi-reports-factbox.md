---
title: Visa egna Power BI-rapporter
description: Du kan använda Power BI Faktabox för att visa Power BI-rapporter och få extra inblick i postdata i nyckellistor.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 06/11/2021
ms.author: jswymer
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-"></a><a name="creating-power-bi-reports-for-displaying-list-data-in-"></a>Skapa Power BI-rapporter för att visa listdata i [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] omfattar en Power BI-Faktabox kontrollelement på många viktiga sidor. Syftet med denna faktabox är att visa Power BI-rapporter som är relaterade till poster i listorna, vilket ger extra inblick i data. Idén är att när du förflyttar dig mellan raderna i listan uppdateras rapporten för vald post.

[!INCLUDE[prod_long](includes/prod_long.md)] är redo med några av dessa rapporter. Du kan också skapa egna anpassade rapporter som visas i den här faktaboxen. Att skapa dessa rapporter liknar andra rapporter. Men det finns några designregler som du måste följa för att se till att rapporterna visas som förväntat. Dessa regler förklaras i den här artikeln.

> [!NOTE]
> För allmän information om skapande och publicering Power BI-rapporter för Business Central, se [Skapa Power BI-rapporter för att visa [!INCLUDE [prod_long](includes/prod_long.md)] data](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a><a name="prerequisites"></a>Förutsättningar

- Ett Power BI-konto.
- Power BI Desktop.

<!-- 
For more information about getting started, see [Use [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a><a name="create-a-report-for-a-list-page"></a>Skapa en rapport för en listsida

1. Starta Power BI Desktop.
2. Välj **Hämta data** och börja välja datakälla för rapporten.

    Ange listsidorna Business Central som innehåller de data du vill ha i rapporten. Om du till exempel vill skapa en rapport för listan **Försäljningsfakturor** inkluderar du sidor som är relaterade till försäljning.

    Mer information finns i anvisningarna [Lägg till [!INCLUDE[prod_short](includes/prod_short.md)] som datakälla i Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).

3. Ange rapportfiltret.

    Om du vill uppdatera datan för vald post i listan lägger du till ett filter i rapporten. Filtret måste innehålla ett fält i datakällan som används för att unikt identifiera varje post i listan. I utvecklartermer är det här fältet i *primära nyckeln*. Oftast är primärnyckeln för en lista **nr.** .

    Så här ställer du in filtret:

    1. I fältet **Filter** väljer du primärnyckelfältet i listan över tillgängliga fält.
    2. Dra fältet till fönstret **Filter** och släpp det i rutan **Filter på alla sidor**.
    3. Ställ in **Filtertypen** på **Grundläggande filtrering**. Det får inte vara ett sid-, visuellt eller avancerat filter.

    ![Ange rapportfiltret för rapporten Försäljningsfakturaaktivitet.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. Designa rapportlayouten.

    Skapa layouten genom att dra fält och lägga till visualiseringar. Mer information finns i [vyn Arbeta med rapport i Power BI Desktop](/power-bi/create-reports/desktop-report-view) i Power BI-dokumentationen.

5. Se nästa avsnitt om hur ändrar storlek på rapporten och använder flera sidor.

6. Spara och namnge rapporten.

    Ge rapporten ett namn som innehåller namnet på den listsida som är kopplad till rapporten, precis som i klienten. Namnet är inte skiftlägeskänsligt. Anta att rapporten gäller listsidan **Försäljningsfakturor**. I det här fallet ska du ta med ordet **försäljningsfakturor** någonstans i namnet, till exempel **mina försäljningsfakturor.pbix** eller **mina_försäljningsfakturor_lista.pbix**.

    Denna namngivningskonvention är inget krav. Den underlättar emellertid valet av rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]. När valsidan för rapporter öppnas från en listsida filtreras den automatiskt baserat på sidans namn. Filtret har syntaxen: `@*<caption>*`, till exempel `@*Sales Invoices*`. Denna filtrering sker i syfte att begränsa den rapport som visas. Användare som vill få en komplett lista över de rapporter som finns tillgängliga i Power BI kan rensa filtret.

7. När du är klar publicerar du rapporten som vanligt.

    Mer information finns i [Publicera en rapport](across-how-use-financials-data-source-powerbi.md#publish-reports).

8. Testa rapporten.

    När rapporten har publicerats på arbetsytan bör den vara tillgänglig från Power BI-faktaboxen på listsidan i [!INCLUDE[prod_short](includes/prod_short.md)].

    Så här testar du det.

    1. Öppna [!INCLUDE[prod_short](includes/prod_short.md)] och gå till listsidan.
    2. Om du inte ser Power BI Faktabox, gå till det åtgärdsfältet och väljer **Åtgärder** > **Visa** > **Visa/dölj Power BI-rapporter**.
    3. I Power BI Faktabox, välj **Välj rapporter**, välj rutan **Aktivera** för rapporten och välj sedan **OK**.

    Om rapporten är korrekt utformad visas den.  

## <a name="set-the-report-size-and-color"></a><a name="set-the-report-size-and-color"></a>Ställa in rapportens storlek och färg

Storleken på rapporten måste anges till 325 x 310 pixlar. Denna storlek tillhandahåller rapportens korrekta dimensioner på det tillgängliga utrymmet för Power BI FactBox-kontrollen i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du vill definiera storleken på rapporten, lägger du fokus utanför rapportens layoutområde och klickar på ikonen färgrulle.

![Ange rapportens bredd och höjd för rapporten Försäljningsfakturaaktivitet.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Du kan ändra bredd och höjd på rapporten genom att välja **anpassaval** i fältet **typ**.

Om du vill att rapportens bakgrund ska smälta samman med bakgrundsfärgen i Power BI FactBox-kontrollen anger du rapportens bakgrundsfärg som *#FFFFFF* (vit). 

> [!TIP]
> Använd [!INCLUDE [prod_short](includes/prod_short.md)]-temafilen för att skapa rapporter med samma färgformatering som [!INCLUDE [prod_short](includes/prod_short.md)]-apparna. Mer information finns i [Använda [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemat](across-how-use-financials-data-source-powerbi.md#theme).

## <a name="reports-with-multiple-pages"></a><a name="reports-with-multiple-pages"></a>Rapporter med flera sidor

Du kan skapa en rapport med flera sidor med Power BI. För rapporter som visas med listsidor rekommenderas emellertid inte att dessa har mer än en sida. Power BI FactBox visar endast rapportens första sida.

## <a name="fixing-problems"></a><a name="fixing-problems"></a>Åtgärda problem

Detta avsnitt förklarar hur du åtgärdar problem som du kan stöta på när du försöker visa en Power BI-rapport för en listsida i [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a><a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a>Du kan inte se Power BI Faktabox på en listsida

Som standard är Power BI Faktabox dold från vyn. För att visa Faktabox på en sida, från åtgärdsfältet och väljer **Åtgärder** > **Visa** > **Visa/dölj Power BI-rapporter**.

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a><a name="you-cant-see-the-report-in-the-select-report-pane"></a>Rapporter kan inte visas på fönstret Välj rapport.

Rapportens namn innehåller inte listsidans namn som visas. Rensa filtret om du vill få en komplett lista över tillgängliga Power BI-rapporter.  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Rapporten laddas in men är tom, ofiltrerad eller felaktigt filtrerad.

Bekräfta att rapportens filter innehåller korrekt primärnyckel. I de flesta fall består detta fält av fältet **Nr.** , men i tabellen **G/L-post** måste du till exempel använda fältet **Inläggsnr.**.

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Rapporten laddas men visar en oväntad sida

Bekräfta att den sida du vill visa är den första sidan i rapporten.  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Rapporten visas med en oönskad grå ram eller är för stor/för liten

Kontrollera att rapportens storlek är 325 pixlar x 310 pixlar. Spara rapporten och uppdatera sedan listsidan.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a>Se även

[Aktivera dina affärsdata för Power BI](admin-powerbi.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakälla](across-how-use-financials-data-source-powerbi.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Ekonomi](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
