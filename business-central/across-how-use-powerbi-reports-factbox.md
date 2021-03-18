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
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="ec3d0-103">Skapa Power BI-rapporter för att visa listdata i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="ec3d0-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="ec3d0-104">omfattar ett FactBox-styrelement på ett antal viktiga listsidor som ger ytterligare insikt i listdatan.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-104">includes a FactBox control element on a number of key list pages that provide additional insight into the data in the list.</span></span> <span data-ttu-id="ec3d0-105">När du flyttar mellan rader i listan uppdateras rapporten och filtrerats för den valda transaktionen.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-105">As you move between rows in the list, the report is updated and filtered for the selected entry.</span></span> <span data-ttu-id="ec3d0-106">Du kan skapa anpassade rapporter och visa dessa i denna kontroll.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-106">You can create custom reports to display in this control.</span></span> <span data-ttu-id="ec3d0-107">Det finns emellertid några regler som måste följas för att rapporterna ska fungera som förväntat.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-107">However, there are a few rules to follow to ensure that reports work as expected.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="ec3d0-108">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="ec3d0-108">Prerequisites</span></span>

- <span data-ttu-id="ec3d0-109">Ett Power BI-konto.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-109">A Power BI account.</span></span>
- <span data-ttu-id="ec3d0-110">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-110">Power BI Desktop.</span></span>

<span data-ttu-id="ec3d0-111">Mer information om hur du kommer igång finns i [Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakälla](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="ec3d0-111">For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).</span></span>

## <a name="defining-the-report-data-set"></a><span data-ttu-id="ec3d0-112">Definiera rapportens datauppsättning</span><span class="sxs-lookup"><span data-stu-id="ec3d0-112">Defining the report data set</span></span>

<span data-ttu-id="ec3d0-113">Ange den datakälla som innehåller datan som är relaterad till listan.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-113">Specify the data source that contains the data related to the list.</span></span> <span data-ttu-id="ec3d0-114">För att kunna skapa en rapport för Sales-listan måste du säkerställa att datauppsättningen innehåller säljrelaterad information.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-114">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>  

## <a name="defining-the-report-filter"></a><span data-ttu-id="ec3d0-115">Definiera rapportfiltret</span><span class="sxs-lookup"><span data-stu-id="ec3d0-115">Defining the report filter</span></span>

<span data-ttu-id="ec3d0-116">Om du vill uppdatera datan för vald post i listan lägger du till ett filter i rapporten.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-116">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="ec3d0-117">Detta filter måste omfatta ett fält för den datakälla som används som *primär nyckel*.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-117">The filter must include a field of the data source that's used as the *primary key*.</span></span> <span data-ttu-id="ec3d0-118">Oftast är primärnyckeln för en lista **nr.**</span><span class="sxs-lookup"><span data-stu-id="ec3d0-118">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="ec3d0-119">.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-119">field.</span></span>

<span data-ttu-id="ec3d0-120">Om du vill definiera ett filter för rapporten, markera primärnyckel i listan över tillgängliga fält och dra och släpp fältet i avsnittet **rapportfilter**.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-120">To define a filter for the report, select the primary key from the list of available fields, and then drag and drop that field into the **Report Filter** section.</span></span> <span data-ttu-id="ec3d0-121">Filtret måste vara ett grundläggande rapportfilter som definierats för alla sidor.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-121">The filter must be a basic report filter that's defined for all pages.</span></span> <span data-ttu-id="ec3d0-122">Det får inte vara ett sid-, visuellt eller avancerat filter.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-122">It can't be page, visual, or advanced filter.</span></span>

![Ange rapportfiltret för rapporten Försäljningsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a><span data-ttu-id="ec3d0-124">Ställa in rapportens storlek och färg</span><span class="sxs-lookup"><span data-stu-id="ec3d0-124">Setting the report size and color</span></span>

<span data-ttu-id="ec3d0-125">Storleken på rapporten måste anges till 325 x 310 pixlar.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-125">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="ec3d0-126">Denna storlek tillhandahåller rapportens korrekta dimensioner på det tillgängliga utrymmet för Power BI FactBox-kontrollen i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="ec3d0-126">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="ec3d0-127">Om du vill definiera storleken på rapporten, lägger du fokus utanför rapportens layoutområde och klickar på ikonen färgrulle.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-127">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Ange rapportens bredd och höjd för rapporten Försäljningsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="ec3d0-129">Du kan ändra bredd och höjd på rapporten genom att välja **anpassaval** i fältet **typ**.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-129">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="ec3d0-130">Om du vill att rapportens bakgrund ska smälta samman med bakgrundsfärgen i Power BI FactBox-kontrollen anger du rapportens bakgrundsfärg som *#FFFFFF*.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-130">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF*.</span></span> 

## <a name="using-reports-with-multiple-pages"></a><span data-ttu-id="ec3d0-131">Använda rapporter med flera sidor</span><span class="sxs-lookup"><span data-stu-id="ec3d0-131">Using reports with multiple pages</span></span>

<span data-ttu-id="ec3d0-132">Du kan skapa en rapport med flera sidor med Power BI.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-132">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="ec3d0-133">För rapporter som visas med listsidor rekommenderas emellertid inte att dessa har mer än en sid.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-133">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="ec3d0-134">Power BI FactBox visar endast rapportens första sida.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-134">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="naming-the-report"></a><span data-ttu-id="ec3d0-135">Namnge rapporten</span><span class="sxs-lookup"><span data-stu-id="ec3d0-135">Naming the report</span></span>

<span data-ttu-id="ec3d0-136">Ge rapporten ett namn som innehåller namnet på den listsida som är kopplad till rapporten.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-136">Give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="ec3d0-137">Om rapporten exempelvis avser listsidan **Leverantör** ska du inkludera ordet *leverantör* någonstans i namnet.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-137">For example, if the report is for the **Vendor** list page, include the word *vendor* somewhere in the name.</span></span>  

<span data-ttu-id="ec3d0-138">Denna namngivningskonvention är inget krav.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-138">This naming convention isn't a requirement.</span></span> <span data-ttu-id="ec3d0-139">Den underlättar emellertid valet av rapporter i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="ec3d0-139">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="ec3d0-140">När valsidan för rapporter öppnas från en listsida filtreras den automatiskt baserat på sidans namn.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-140">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="ec3d0-141">Denna filtrering sker i syfte att begränsa den rapport som visas.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-141">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="ec3d0-142">Användare som vill få en komplett lista över de rapporter som finns tillgängliga i Power BI kan rensa filtret.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-142">Users can clear the filter to get a full list of reports available in Power BI.</span></span>  

## <a name="fixing-problems"></a><span data-ttu-id="ec3d0-143">Åtgärda problem</span><span class="sxs-lookup"><span data-stu-id="ec3d0-143">Fixing problems</span></span>

<span data-ttu-id="ec3d0-144">Detta avsnitt ger dig lösningarna på de vanligaste problem som kan uppstå när du skapar Power BI-rapporten.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-144">This section provides a workaround for the most typical problems that can occur when you create the Power BI report.</span></span>  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a><span data-ttu-id="ec3d0-145">Rapporter kan inte visas på sidan Välj rapport.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-145">You can't see a report on the Select Report page</span></span>

<span data-ttu-id="ec3d0-146">Detta beror troligen på att rapportens namn inte innehåller listsidans namn.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-146">It's probably because the report's name doesn't contain the name of the list page.</span></span> <span data-ttu-id="ec3d0-147">Rensa filtret om du vill få en komplett lista över tillgängliga Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-147">Clear the filter to get a full list of Power BI reports available.</span></span>  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="ec3d0-148">Rapporten laddas in men är tom, ofiltrerad eller felaktigt filtrerad.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-148">Report is loaded but blank, not filtered or filtered incorrectly</span></span>

<span data-ttu-id="ec3d0-149">Bekräfta att rapportens filter innehåller korrekt primärnyckel.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-149">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="ec3d0-150">I de flesta fall består detta fält av fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="ec3d0-150">In most cases, this field is the **No.**</span></span> <span data-ttu-id="ec3d0-151">, men i tabellen **G/L-post** måste du till exempel använda fältet **Inläggsnr.**.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-151">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="ec3d0-152">Rapporten laddas men visar en oväntad sida</span><span class="sxs-lookup"><span data-stu-id="ec3d0-152">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="ec3d0-153">Bekräfta att den sida du vill visa är den första sidan i rapporten.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-153">Verify that the page you want displayed is the first page in your report.</span></span>  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="ec3d0-154">Rapporten visas med en oönskad grå ram eller är för stor/för liten</span><span class="sxs-lookup"><span data-stu-id="ec3d0-154">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="ec3d0-155">Kontrollera att rapportens storlek är 325 pixlar x 310 pixlar.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-155">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="ec3d0-156">Spara rapporten och uppdatera sedan listsidan.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-156">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="ec3d0-157">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="ec3d0-157">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="ec3d0-158">Se även</span><span class="sxs-lookup"><span data-stu-id="ec3d0-158">See Also</span></span>

[<span data-ttu-id="ec3d0-159">Aktivera dina affärsdata för Power BI</span><span class="sxs-lookup"><span data-stu-id="ec3d0-159">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="ec3d0-160">[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI datakälla](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="ec3d0-160">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="ec3d0-161">Komma igång</span><span class="sxs-lookup"><span data-stu-id="ec3d0-161">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="ec3d0-162">[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="ec3d0-162">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="ec3d0-163">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="ec3d0-163">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]