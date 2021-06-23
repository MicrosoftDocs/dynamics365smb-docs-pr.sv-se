---
title: Visa anpassade Power BI-rapporter för Business Central-data
description: Du kan använda Power BI-rapporter för att få ytterligare information om data i listor.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/26/2021
ms.author: jswymer
ms.openlocfilehash: d2ce2588604ae676ba8b2cb73878a2d8dfd32b63
ms.sourcegitcommit: 652e4b0e1a09bff265014d9f8eb3b038ab0db79e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087700"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="80a49-103">Skapa Power BI-rapporter för att visa listdata i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="80a49-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="80a49-104">omfattar en Power BI-Faktabox kontrollelement på många viktiga sidor.</span><span class="sxs-lookup"><span data-stu-id="80a49-104">includes a Power BI FactBox control element on many key list pages.</span></span> <span data-ttu-id="80a49-105">Syftet med denna faktabox är att visa Power BI-rapporter som är relaterade till poster i listorna, vilket ger extra inblick i data.</span><span class="sxs-lookup"><span data-stu-id="80a49-105">The purpose of this FactBox is to display Power BI reports that are related to records in the lists, providing extra insight into the data.</span></span> <span data-ttu-id="80a49-106">Idén är att när du förflyttar dig mellan raderna i listan uppdateras rapporten för vald post.</span><span class="sxs-lookup"><span data-stu-id="80a49-106">The idea is that as you move between rows in the list, the report updates for the selected entry.</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="80a49-107">är redo med några av dessa rapporter.</span><span class="sxs-lookup"><span data-stu-id="80a49-107">comes ready with some of these reports.</span></span> <span data-ttu-id="80a49-108">Du kan också skapa egna anpassade rapporter som visas i den här faktaboxen.</span><span class="sxs-lookup"><span data-stu-id="80a49-108">You can also create your own custom reports that display in this FactBox.</span></span> <span data-ttu-id="80a49-109">Att skapa dessa rapporter liknar andra rapporter.</span><span class="sxs-lookup"><span data-stu-id="80a49-109">Creating these reports is similar to other reports.</span></span> <span data-ttu-id="80a49-110">Men det finns några designregler som du måste följa för att se till att rapporterna visas som förväntat.</span><span class="sxs-lookup"><span data-stu-id="80a49-110">But there are a few design rules you'll have to follow to make sure the reports display as expected.</span></span> <span data-ttu-id="80a49-111">Dessa regler förklaras i den här artikeln.</span><span class="sxs-lookup"><span data-stu-id="80a49-111">These rules are explained in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="80a49-112">För allmän information om skapande och publicering Power BI-rapporter för Business Central, se [Skapa Power BI-rapporter för att visa [!INCLUDE [prod_long](includes/prod_long.md)] data](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="80a49-112">For general information about creating and publishing Power BI reports for Business Central, see [Building Power BI Reports to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="80a49-113">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="80a49-113">Prerequisites</span></span>

- <span data-ttu-id="80a49-114">Ett Power BI-konto.</span><span class="sxs-lookup"><span data-stu-id="80a49-114">A Power BI account.</span></span>
- <span data-ttu-id="80a49-115">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="80a49-115">Power BI Desktop.</span></span>

<!-- 
For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a><span data-ttu-id="80a49-116">Skapa en rapport för en listsida</span><span class="sxs-lookup"><span data-stu-id="80a49-116">Create a report for a list page</span></span>

1. <span data-ttu-id="80a49-117">Starta Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="80a49-117">Start Power BI Desktop.</span></span>
2. <span data-ttu-id="80a49-118">Välj **Hämta data** och börja välja datakälla för rapporten.</span><span class="sxs-lookup"><span data-stu-id="80a49-118">Select **Get Data**, and start choosing the data source for the report.</span></span>

    <span data-ttu-id="80a49-119">Ange listsidorna Business Central som innehåller de data du vill ha i rapporten.</span><span class="sxs-lookup"><span data-stu-id="80a49-119">Specify the Business Central list pages that contain the data that you want in the report.</span></span> <span data-ttu-id="80a49-120">Om du till exempel vill skapa en rapport för listan **Försäljningsfakturor** inkluderar du sidor som är relaterade till försäljning.</span><span class="sxs-lookup"><span data-stu-id="80a49-120">For example, to create a report for the **Sales Invoices** list, include pages related to sales.</span></span>

    <span data-ttu-id="80a49-121">Mer information finns i anvisningarna [Lägg till [!INCLUDE[prod_short](includes/prod_short.md)] som datakälla i Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span><span class="sxs-lookup"><span data-stu-id="80a49-121">For more information, follow the instructions [Add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span></span>

3. <span data-ttu-id="80a49-122">Ange rapportfiltret.</span><span class="sxs-lookup"><span data-stu-id="80a49-122">Set the report filter.</span></span>

    <span data-ttu-id="80a49-123">Om du vill uppdatera datan för vald post i listan lägger du till ett filter i rapporten.</span><span class="sxs-lookup"><span data-stu-id="80a49-123">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="80a49-124">Filtret måste innehålla ett fält i datakällan som används för att unikt identifiera varje post i listan.</span><span class="sxs-lookup"><span data-stu-id="80a49-124">The filter must include a field of the data source that's used to uniquely identify each record in the list.</span></span> <span data-ttu-id="80a49-125">I utvecklartermer är det här fältet i *primära nyckeln*.</span><span class="sxs-lookup"><span data-stu-id="80a49-125">In developer terms, this field is the *primary key*.</span></span> <span data-ttu-id="80a49-126">Oftast är primärnyckeln för en lista **nr.**</span><span class="sxs-lookup"><span data-stu-id="80a49-126">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="80a49-127">.</span><span class="sxs-lookup"><span data-stu-id="80a49-127">field.</span></span>

    <span data-ttu-id="80a49-128">Så här ställer du in filtret:</span><span class="sxs-lookup"><span data-stu-id="80a49-128">To set the filter, do the following steps:</span></span>

    1. <span data-ttu-id="80a49-129">I fältet **Filter** väljer du primärnyckelfältet i listan över tillgängliga fält.</span><span class="sxs-lookup"><span data-stu-id="80a49-129">In the **Filters**, select the primary key field from the list of available fields.</span></span>
    2. <span data-ttu-id="80a49-130">Dra fältet till fönstret **Filter** och släpp det i rutan **Filter på alla sidor**.</span><span class="sxs-lookup"><span data-stu-id="80a49-130">Drag the field to **Filters** pane and drop it in the **Filters on all pages** box.</span></span>
    3. <span data-ttu-id="80a49-131">Ställ in **Filtertypen** på **Grundläggande filtrering**.</span><span class="sxs-lookup"><span data-stu-id="80a49-131">Set the **Filter type** to **Basic filtering**.</span></span> <span data-ttu-id="80a49-132">Det får inte vara ett sid-, visuellt eller avancerat filter.</span><span class="sxs-lookup"><span data-stu-id="80a49-132">It can't be page, visual, or advanced filter.</span></span>

    ![Ange rapportfiltret för rapporten Försäljningsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. <span data-ttu-id="80a49-134">Designa rapportlayouten.</span><span class="sxs-lookup"><span data-stu-id="80a49-134">Design the report layout.</span></span>

    <span data-ttu-id="80a49-135">Skapa layouten genom att dra fält och lägga till visualiseringar.</span><span class="sxs-lookup"><span data-stu-id="80a49-135">Create the layout by dragging fields and adding visualizations.</span></span> <span data-ttu-id="80a49-136">Mer information finns i [vyn Arbeta med rapport i Power BI Desktop](/power-bi/create-reports/desktop-report-view) i Power BI-dokumentationen.</span><span class="sxs-lookup"><span data-stu-id="80a49-136">For more information, see, [Work with Report view in Power BI Desktop](/power-bi/create-reports/desktop-report-view) in the Power BI documentation.</span></span>

5. <span data-ttu-id="80a49-137">Se nästa avsnitt om hur ändrar storlek på rapporten och använder flera sidor.</span><span class="sxs-lookup"><span data-stu-id="80a49-137">See the next sections about sizing the report and using multiple pages.</span></span>

6. <span data-ttu-id="80a49-138">Spara och namnge rapporten.</span><span class="sxs-lookup"><span data-stu-id="80a49-138">Save and name the report.</span></span>

    <span data-ttu-id="80a49-139">Ge rapporten ett namn som innehåller namnet på den listsida som är kopplad till rapporten, precis som i klienten.</span><span class="sxs-lookup"><span data-stu-id="80a49-139">Give the report a name that contains the name of the list page associated with the report, as it is in the client.</span></span> <span data-ttu-id="80a49-140">Namnet är inte skiftlägeskänsligt.</span><span class="sxs-lookup"><span data-stu-id="80a49-140">The name isn't case-sensitive though.</span></span> <span data-ttu-id="80a49-141">Anta att rapporten gäller listsidan **Försäljningsfakturor**.</span><span class="sxs-lookup"><span data-stu-id="80a49-141">Suppose the report is for the **Sales Invoices** list page.</span></span> <span data-ttu-id="80a49-142">I det här fallet ska du ta med ordet **försäljningsfakturor** någonstans i namnet, till exempel **mina försäljningsfakturor.pbix** eller **mina_försäljningsfakturor_lista.pbix**.</span><span class="sxs-lookup"><span data-stu-id="80a49-142">In this case, include the words **sales invoices** somewhere in the name, like **my sales invoices.pbix** or **my_Sales Invoices_list.pbix**.</span></span>

    <span data-ttu-id="80a49-143">Denna namngivningskonvention är inget krav.</span><span class="sxs-lookup"><span data-stu-id="80a49-143">This naming convention isn't a requirement.</span></span> <span data-ttu-id="80a49-144">Den underlättar emellertid valet av rapporter i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="80a49-144">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="80a49-145">När valsidan för rapporter öppnas från en listsida filtreras den automatiskt baserat på sidans namn.</span><span class="sxs-lookup"><span data-stu-id="80a49-145">When the report selection page opens from a list page, it's automatically applied a filter based on the page name.</span></span> <span data-ttu-id="80a49-146">Filtret har syntaxen: `@*<caption>*`, till exempel `@*Sales Invoices*`.</span><span class="sxs-lookup"><span data-stu-id="80a49-146">The filter has the syntax: `@*<caption>*`,  like `@*Sales Invoices*`.</span></span> <span data-ttu-id="80a49-147">Denna filtrering sker i syfte att begränsa den rapport som visas.</span><span class="sxs-lookup"><span data-stu-id="80a49-147">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="80a49-148">Användare som vill få en komplett lista över de rapporter som finns tillgängliga i Power BI kan rensa filtret.</span><span class="sxs-lookup"><span data-stu-id="80a49-148">Users can clear the filter to get a full list of reports available in Power BI.</span></span>

7. <span data-ttu-id="80a49-149">När du är klar publicerar du rapporten som vanligt.</span><span class="sxs-lookup"><span data-stu-id="80a49-149">When you're done, publish the report as usual.</span></span>

    <span data-ttu-id="80a49-150">Mer information finns i [Publicera en rapport](across-how-use-financials-data-source-powerbi.md#publish-reports).</span><span class="sxs-lookup"><span data-stu-id="80a49-150">For more information, see [Publishing a Report](across-how-use-financials-data-source-powerbi.md#publish-reports).</span></span>

8. <span data-ttu-id="80a49-151">Testa rapporten.</span><span class="sxs-lookup"><span data-stu-id="80a49-151">Test the report.</span></span>

    <span data-ttu-id="80a49-152">När rapporten har publicerats på arbetsytan bör den vara tillgänglig från Power BI-faktaboxen på listsidan i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="80a49-152">Once the report's been published to your workspace, it should be available from the Power BI FactBox on the list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

    <span data-ttu-id="80a49-153">Så här testar du det.</span><span class="sxs-lookup"><span data-stu-id="80a49-153">To test it, do the following steps.</span></span>

    1. <span data-ttu-id="80a49-154">Öppna [!INCLUDE[prod_short](includes/prod_short.md)] och gå till listsidan.</span><span class="sxs-lookup"><span data-stu-id="80a49-154">Open [!INCLUDE[prod_short](includes/prod_short.md)] and go to the list page.</span></span>
    2. <span data-ttu-id="80a49-155">Om du inte ser Power BI Faktabox, gå till det åtgärdsfältet och väljer **Åtgärder** > **Visa** > **Visa/dölj Power BI-rapporter**.</span><span class="sxs-lookup"><span data-stu-id="80a49-155">If you don't see the Power BI FactBox, go the action bar, then select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>
    3. <span data-ttu-id="80a49-156">I Power BI Faktabox, välj **Välj rapporter**, välj rutan **Aktivera** för rapporten och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="80a49-156">In the Power BI FactBox, select **Select Reports**, select the **Enable** box for the report, then select **OK**.</span></span>

    <span data-ttu-id="80a49-157">Om rapporten är korrekt utformad visas den.</span><span class="sxs-lookup"><span data-stu-id="80a49-157">If designed correctly, the report displays.</span></span>  

## <a name="set-the-report-size-and-color"></a><span data-ttu-id="80a49-158">Ställa in rapportens storlek och färg</span><span class="sxs-lookup"><span data-stu-id="80a49-158">Set the report size and color</span></span>

<span data-ttu-id="80a49-159">Storleken på rapporten måste anges till 325 x 310 pixlar.</span><span class="sxs-lookup"><span data-stu-id="80a49-159">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="80a49-160">Denna storlek tillhandahåller rapportens korrekta dimensioner på det tillgängliga utrymmet för Power BI FactBox-kontrollen i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="80a49-160">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="80a49-161">Om du vill definiera storleken på rapporten, lägger du fokus utanför rapportens layoutområde och klickar på ikonen färgrulle.</span><span class="sxs-lookup"><span data-stu-id="80a49-161">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Ange rapportens bredd och höjd för rapporten Försäljningsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="80a49-163">Du kan ändra bredd och höjd på rapporten genom att välja **anpassaval** i fältet **typ**.</span><span class="sxs-lookup"><span data-stu-id="80a49-163">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="80a49-164">Om du vill att rapportens bakgrund ska smälta samman med bakgrundsfärgen i Power BI FactBox-kontrollen anger du rapportens bakgrundsfärg som *#FFFFFF* (vit).</span><span class="sxs-lookup"><span data-stu-id="80a49-164">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF* (white).</span></span> 

> [!TIP]
> <span data-ttu-id="80a49-165">Använd [!INCLUDE [prod_short](includes/prod_short.md)]-temafilen för att skapa rapporter med samma färgformatering som [!INCLUDE [prod_short](includes/prod_short.md)]-apparna.</span><span class="sxs-lookup"><span data-stu-id="80a49-165">Use the [!INCLUDE [prod_short](includes/prod_short.md)] theme file to build reports with the same color styling as the [!INCLUDE [prod_short](includes/prod_short.md)] apps.</span></span> <span data-ttu-id="80a49-166">Mer information finns i [Använda tillägget [!INCLUDE [prod_short](includes/prod_short.md)] rapporttema](across-how-use-financials-data-source-powerbi.md#theme).</span><span class="sxs-lookup"><span data-stu-id="80a49-166">For more information, see [Using the [!INCLUDE [prod_short](includes/prod_short.md)] report theme](across-how-use-financials-data-source-powerbi.md#theme).</span></span>

## <a name="reports-with-multiple-pages"></a><span data-ttu-id="80a49-167">Rapporter med flera sidor</span><span class="sxs-lookup"><span data-stu-id="80a49-167">Reports with multiple pages</span></span>

<span data-ttu-id="80a49-168">Du kan skapa en rapport med flera sidor med Power BI.</span><span class="sxs-lookup"><span data-stu-id="80a49-168">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="80a49-169">För rapporter som visas med listsidor rekommenderas emellertid inte att dessa har mer än en sida.</span><span class="sxs-lookup"><span data-stu-id="80a49-169">However, for reports that will display with list pages, we recommend that they don't have more than one page.</span></span> <span data-ttu-id="80a49-170">Power BI FactBox visar endast rapportens första sida.</span><span class="sxs-lookup"><span data-stu-id="80a49-170">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="fixing-problems"></a><span data-ttu-id="80a49-171">Åtgärda problem</span><span class="sxs-lookup"><span data-stu-id="80a49-171">Fixing problems</span></span>

<span data-ttu-id="80a49-172">Detta avsnitt förklarar hur du åtgärdar problem som du kan stöta på när du försöker visa en Power BI-rapport för en listsida i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="80a49-172">This section explains how to fix problems that you might run into when you try to view a Power BI report for a list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a><span data-ttu-id="80a49-173">Du kan inte se Power BI Faktabox på en listsida</span><span class="sxs-lookup"><span data-stu-id="80a49-173">You can't see the Power BI FactBox on a list page</span></span>

<span data-ttu-id="80a49-174">Som standard är Power BI Faktabox dold från vyn.</span><span class="sxs-lookup"><span data-stu-id="80a49-174">By default, the Power BI FactBox is hidden from view.</span></span> <span data-ttu-id="80a49-175">För att visa Faktabox på en sida, från åtgärdsfältet och väljer **Åtgärder** > **Visa** > **Visa/dölj Power BI-rapporter**.</span><span class="sxs-lookup"><span data-stu-id="80a49-175">To show the FactBox on a page, from the action bar, select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a><span data-ttu-id="80a49-176">Rapporter kan inte visas på fönstret Välj rapport.</span><span class="sxs-lookup"><span data-stu-id="80a49-176">You can't see the report in the Select Report pane</span></span>

<span data-ttu-id="80a49-177">Rapportens namn innehåller inte listsidans namn som visas.</span><span class="sxs-lookup"><span data-stu-id="80a49-177">The report's name doesn't contain the name of the list page that's being shown.</span></span> <span data-ttu-id="80a49-178">Rensa filtret om du vill få en komplett lista över tillgängliga Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="80a49-178">Clear the filter to get a full list of Power BI reports available.</span></span>  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="80a49-179">Rapporten laddas in men är tom, ofiltrerad eller felaktigt filtrerad.</span><span class="sxs-lookup"><span data-stu-id="80a49-179">Report is loaded but blank, not filtered, or filtered incorrectly</span></span>

<span data-ttu-id="80a49-180">Bekräfta att rapportens filter innehåller korrekt primärnyckel.</span><span class="sxs-lookup"><span data-stu-id="80a49-180">Verify the report filter contains the right primary key.</span></span> <span data-ttu-id="80a49-181">I de flesta fall består detta fält av fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="80a49-181">In most cases, this field is the **No.**</span></span> <span data-ttu-id="80a49-182">, men i tabellen **G/L-post** måste du till exempel använda fältet **Inläggsnr.**.</span><span class="sxs-lookup"><span data-stu-id="80a49-182">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="80a49-183">Rapporten laddas men visar en oväntad sida</span><span class="sxs-lookup"><span data-stu-id="80a49-183">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="80a49-184">Bekräfta att den sida du vill visa är den första sidan i rapporten.</span><span class="sxs-lookup"><span data-stu-id="80a49-184">Verify that the page you want displayed is the first page in your report.</span></span>  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="80a49-185">Rapporten visas med en oönskad grå ram eller är för stor/för liten</span><span class="sxs-lookup"><span data-stu-id="80a49-185">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="80a49-186">Kontrollera att rapportens storlek är 325 pixlar x 310 pixlar.</span><span class="sxs-lookup"><span data-stu-id="80a49-186">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="80a49-187">Spara rapporten och uppdatera sedan listsidan.</span><span class="sxs-lookup"><span data-stu-id="80a49-187">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="80a49-188">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="80a49-188">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="80a49-189">Se även</span><span class="sxs-lookup"><span data-stu-id="80a49-189">See Also</span></span>

[<span data-ttu-id="80a49-190">Aktivera dina affärsdata för Power BI</span><span class="sxs-lookup"><span data-stu-id="80a49-190">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="80a49-191">[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI datakälla](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="80a49-191">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="80a49-192">Gör dig redo att göra affärer</span><span class="sxs-lookup"><span data-stu-id="80a49-192">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="80a49-193">[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="80a49-193">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="80a49-194">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="80a49-194">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]