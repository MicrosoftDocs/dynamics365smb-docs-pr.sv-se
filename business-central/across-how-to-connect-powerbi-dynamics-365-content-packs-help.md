---
title: "Så här ansluter du Power BI till Business Central | Microsoft Docs"
description: "Det är enkelt att få insikter, affärsinformation och KPI:er från dina Business Central-data med Power BI och innehållspaketet för Business Central."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 448b8fa9d1b239f98c7ca3700b9f7f56f08d7854
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a><span data-ttu-id="b5102-103">Ansluta Power BI till innehållspaket för Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="b5102-103">Connecting Power BI to Dynamics 365 Business Central Content Packs</span></span>
<span data-ttu-id="b5102-104">Att få insikter om dina Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data är enkelt med Power BI och Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innehållspaketen.</span><span class="sxs-lookup"><span data-stu-id="b5102-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="b5102-105">Power BI hämtar dina data och skapar sedan en förinstallerad instrumentbräda och rapporter baserade på den data.</span><span class="sxs-lookup"><span data-stu-id="b5102-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

<span data-ttu-id="b5102-106">Du måste ha ett giltigt konto med Dynamics 365 och med Power BI.</span><span class="sxs-lookup"><span data-stu-id="b5102-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="b5102-107">Du måste även hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) om du vill skapa egna Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="b5102-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) if you wish to create your own Power BI reports.</span></span> <span data-ttu-id="b5102-108">Innehållspaket för Power BI kräver behörighet till de tabeller som data ska hämtas ifrån.</span><span class="sxs-lookup"><span data-stu-id="b5102-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="b5102-109">Mer information om kraven beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="b5102-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="b5102-110">Så här ansluter du</span><span class="sxs-lookup"><span data-stu-id="b5102-110">How to Connect</span></span>
1. <span data-ttu-id="b5102-111">Välj **Hämta Data** längst ned i den vänstra navigeringsrutan.</span><span class="sxs-lookup"><span data-stu-id="b5102-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="b5102-112">![Navigera för att hämta data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="b5102-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>

<span data-ttu-id="b5102-113">Du kan också starta från Dynamics 365 Business Edition.</span><span class="sxs-lookup"><span data-stu-id="b5102-113">You may also get starting from within Dynamics 365 Business Edition.</span></span> <span data-ttu-id="b5102-114">Från Rollcentret navigerar du till **Rapportval** i rollcenterdelen för Power BI.</span><span class="sxs-lookup"><span data-stu-id="b5102-114">From the role center, navigate to **Report Selection** in the Power BI Role Center part.</span></span> <span data-ttu-id="b5102-115">Välj antingen **Service** eller **Min organisation** i menyfliken.</span><span class="sxs-lookup"><span data-stu-id="b5102-115">Select either **Service** or **My Organization** from the ribbon.</span></span> <span data-ttu-id="b5102-116">När något av ovanstående åtgärder är markerade förs du till antingen galleriet Organisation i Power BI eller till tjänstebiblioteket i Power BI, vilket även filtreras att bara visa innehållspaket relaterade till [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b5102-116">When either of these actions are selected, you will be taken to either the Organization gallery in Power BI or to the services library in Power BI, which will also be filtered to only display content packs related to [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span>

2. <span data-ttu-id="b5102-117">I rutan **Tjänster**, markera **Hämta**.</span><span class="sxs-lookup"><span data-stu-id="b5102-117">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="b5102-118">Då öppnas ett fönster med **AppSource** och **Program för Power BI-program**.</span><span class="sxs-lookup"><span data-stu-id="b5102-118">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="b5102-119">![Välj innehållspaket bland onlinetjänsterna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="b5102-119">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="b5102-120">Markera **Program** i fliken **Program för Power BI-program**, välj det innehållspaket för **Microsoft Dynamics 365 Business Central** som du vill använda och välj sedan **Hämta nu**.</span><span class="sxs-lookup"><span data-stu-id="b5102-120">Select **Apps** from the **Apps for Power BI apps** tab, choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="b5102-121">![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="b5102-121">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="b5102-122">Ange namnet på *ditt företag* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] när du uppmanas att göra så.</span><span class="sxs-lookup"><span data-stu-id="b5102-122">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="b5102-123">Detta är inte visningsnamnet.</span><span class="sxs-lookup"><span data-stu-id="b5102-123">This is not the display name.</span></span> <span data-ttu-id="b5102-124">Företagsnamnet finns på sidan ”Företag” i din [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-instans.</span><span class="sxs-lookup"><span data-stu-id="b5102-124">The company name can be found on the 'Companies' page within your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] instance.</span></span> 
<span data-ttu-id="b5102-125">![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="b5102-125">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="b5102-126">När anslutningen har genomförts kommer instrumentpanel, rapport och datauppsättning automatiskt att laddas till din Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="b5102-126">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="b5102-127">När hämtningen är slutförd kommer panelerna att uppdateras med information från ditt [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-företag.</span><span class="sxs-lookup"><span data-stu-id="b5102-127">When completed, the tiles will update with data from your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] company.</span></span>
<span data-ttu-id="b5102-128">![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="b5102-128">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="b5102-129">Vad nu?</span><span class="sxs-lookup"><span data-stu-id="b5102-129">What Now?</span></span>

- <span data-ttu-id="b5102-130">Försök med att [ställa en fråga i rutan Frågor och svar](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) högst upp i instrumentpanelen.</span><span class="sxs-lookup"><span data-stu-id="b5102-130">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>
- <span data-ttu-id="b5102-131">[Ändra panelerna](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) på instrumentpanelen.</span><span class="sxs-lookup"><span data-stu-id="b5102-131">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="b5102-132">[Välj en panel](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) för att öppna den underliggande rapporten.</span><span class="sxs-lookup"><span data-stu-id="b5102-132">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="b5102-133">Din datauppsättning schemaläggs att uppdateras dagligen, men du kan ändra uppdateringsschemat eller uppdatera det på begäran med hjälp av **Uppdatera nu**.</span><span class="sxs-lookup"><span data-stu-id="b5102-133">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="b5102-134">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="b5102-134">System Requirements</span></span>
<span data-ttu-id="b5102-135">För att importera dina [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data i Power BI måste du ha behörighet till de webbtjänster som används för att hämta data.</span><span class="sxs-lookup"><span data-stu-id="b5102-135">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="b5102-136">De webbtjänster som krävs för respektive innehållspaket är:</span><span class="sxs-lookup"><span data-stu-id="b5102-136">The web services required for each content pack include:</span></span>

## <a name="role-center-reports"></a><span data-ttu-id="b5102-137">Rollcenter-rapporter</span><span class="sxs-lookup"><span data-stu-id="b5102-137">Role Center Reports</span></span>

<span data-ttu-id="b5102-138">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="b5102-138">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="b5102-139">Försäljningsmöjligheter</span><span class="sxs-lookup"><span data-stu-id="b5102-139">Sales Opportunities</span></span>
- <span data-ttu-id="b5102-140">Excel-mallen för Visa företag</span><span class="sxs-lookup"><span data-stu-id="b5102-140">Excel Template View Company</span></span>
- <span data-ttu-id="b5102-141">Rapportetiketter för Power BI</span><span class="sxs-lookup"><span data-stu-id="b5102-141">Power BI Report Labels</span></span>

<span data-ttu-id="b5102-142">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="b5102-142">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="b5102-143">Power BIFinance</span><span class="sxs-lookup"><span data-stu-id="b5102-143">PowerBIFinance</span></span>
- <span data-ttu-id="b5102-144">Excel-mallen för Visa företag</span><span class="sxs-lookup"><span data-stu-id="b5102-144">Excel Template View Company</span></span>
- <span data-ttu-id="b5102-145">Rapportetiketter för Power BI</span><span class="sxs-lookup"><span data-stu-id="b5102-145">Power BI Report Labels</span></span>

<span data-ttu-id="b5102-146">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="b5102-146">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="b5102-147">Projektlista</span><span class="sxs-lookup"><span data-stu-id="b5102-147">Job List</span></span>
- <span data-ttu-id="b5102-148">Projektplaneringsrader</span><span class="sxs-lookup"><span data-stu-id="b5102-148">Job Planning Lines</span></span>
- <span data-ttu-id="b5102-149">Projektaktivitetsrader</span><span class="sxs-lookup"><span data-stu-id="b5102-149">Job Task Lines</span></span>
- <span data-ttu-id="b5102-150">Rapportetiketter för Power BI</span><span class="sxs-lookup"><span data-stu-id="b5102-150">Power BI Report Labels</span></span>
- <span data-ttu-id="b5102-151">Excel-mallen för Visa företag</span><span class="sxs-lookup"><span data-stu-id="b5102-151">Excel Template View Company</span></span>

<span data-ttu-id="b5102-152">**Microsoft Dynamics 365 Business Central - Sales**</span><span class="sxs-lookup"><span data-stu-id="b5102-152">**Microsoft Dynamics 365 Business Central - Sales**</span></span>
- <span data-ttu-id="b5102-153">Instrumentbräda för försäljning</span><span class="sxs-lookup"><span data-stu-id="b5102-153">Sales Dashboard</span></span>
- <span data-ttu-id="b5102-154">Excel-mallen för Visa företag</span><span class="sxs-lookup"><span data-stu-id="b5102-154">Excel Template View Company</span></span>
- <span data-ttu-id="b5102-155">Rapportetiketter för Power BI</span><span class="sxs-lookup"><span data-stu-id="b5102-155">Power BI Report Labels</span></span>

## <a name="list-page-reports"></a><span data-ttu-id="b5102-156">Rapporter för listsida</span><span class="sxs-lookup"><span data-stu-id="b5102-156">List Page Reports</span></span> 

<span data-ttu-id="b5102-157">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="b5102-157">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="b5102-158">Artikelförsäljning efter kund</span><span class="sxs-lookup"><span data-stu-id="b5102-158">Item Sales by Customer</span></span>
- <span data-ttu-id="b5102-159">Power BI artikelinköpslista</span><span class="sxs-lookup"><span data-stu-id="b5102-159">Power BI Item Purchase List</span></span>
- <span data-ttu-id="b5102-160">Power BI artikelförsäljningslista</span><span class="sxs-lookup"><span data-stu-id="b5102-160">Power BI Item Sales List</span></span>
- <span data-ttu-id="b5102-161">Instrumentbräda för försäljning</span><span class="sxs-lookup"><span data-stu-id="b5102-161">Sales Dashboard</span></span>
- <span data-ttu-id="b5102-162">Power BI kundlista</span><span class="sxs-lookup"><span data-stu-id="b5102-162">Power BI Customer List</span></span>
- <span data-ttu-id="b5102-163">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="b5102-163">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="b5102-164">Rapportetiketter för Power BI</span><span class="sxs-lookup"><span data-stu-id="b5102-164">Power BI Report Labels</span></span> 

<span data-ttu-id="b5102-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span><span class="sxs-lookup"><span data-stu-id="b5102-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span></span>
- <span data-ttu-id="b5102-166">Power BI redovisningsbelopplista</span><span class="sxs-lookup"><span data-stu-id="b5102-166">Power BI GL Amount List</span></span>
- <span data-ttu-id="b5102-167">Power BI budgeterat redovisningsbelopp</span><span class="sxs-lookup"><span data-stu-id="b5102-167">Power BI GL Budgeted Amount</span></span>
- <span data-ttu-id="b5102-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="b5102-168">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="b5102-169">Rapportetiketter för Power BI</span><span class="sxs-lookup"><span data-stu-id="b5102-169">Power BI Report Labels</span></span>

<span data-ttu-id="b5102-170">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="b5102-170">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="b5102-171">Artikelförsäljning efter kund</span><span class="sxs-lookup"><span data-stu-id="b5102-171">Item Sales by Customer</span></span>
- <span data-ttu-id="b5102-172">Power BI artikelinköpslista</span><span class="sxs-lookup"><span data-stu-id="b5102-172">Power BI Item Purchase List</span></span>
- <span data-ttu-id="b5102-173">Power BI artikelförsäljningslista</span><span class="sxs-lookup"><span data-stu-id="b5102-173">Power BI Item Sales List</span></span>
- <span data-ttu-id="b5102-174">Instrumentbräda för försäljning</span><span class="sxs-lookup"><span data-stu-id="b5102-174">Sales Dashboard</span></span>
- <span data-ttu-id="b5102-175">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="b5102-175">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="b5102-176">Rapportetiketter för Power BI</span><span class="sxs-lookup"><span data-stu-id="b5102-176">Power BI Report Labels</span></span>

<span data-ttu-id="b5102-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span><span class="sxs-lookup"><span data-stu-id="b5102-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span></span>
- <span data-ttu-id="b5102-178">Power BI projektlista</span><span class="sxs-lookup"><span data-stu-id="b5102-178">Power BI Jobs List</span></span>
- <span data-ttu-id="b5102-179">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="b5102-179">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="b5102-180">Rapportetiketter för Power BI</span><span class="sxs-lookup"><span data-stu-id="b5102-180">Power BI Report Labels</span></span>

<span data-ttu-id="b5102-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span><span class="sxs-lookup"><span data-stu-id="b5102-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span></span>
- <span data-ttu-id="b5102-182">Power BI inköpslista</span><span class="sxs-lookup"><span data-stu-id="b5102-182">Power BI Purchase List</span></span>
- <span data-ttu-id="b5102-183">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="b5102-183">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="b5102-184">Rapportetiketter för Power BI</span><span class="sxs-lookup"><span data-stu-id="b5102-184">Power BI Report Labels</span></span>

<span data-ttu-id="b5102-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span><span class="sxs-lookup"><span data-stu-id="b5102-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span></span>
- <span data-ttu-id="b5102-186">Power BI försäljningslista</span><span class="sxs-lookup"><span data-stu-id="b5102-186">Power BI Sales List</span></span>
- <span data-ttu-id="b5102-187">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="b5102-187">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="b5102-188">Rapportetiketter för Power BI</span><span class="sxs-lookup"><span data-stu-id="b5102-188">Power BI Report Labels</span></span>


<span data-ttu-id="b5102-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="b5102-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="b5102-190">Power BI artikelinköpslista</span><span class="sxs-lookup"><span data-stu-id="b5102-190">Power BI Item Purchase List</span></span>
- <span data-ttu-id="b5102-191">Power BI artikelförsäljningslista</span><span class="sxs-lookup"><span data-stu-id="b5102-191">Power BI Item Sales List</span></span>
- <span data-ttu-id="b5102-192">Power BI leverantörslista</span><span class="sxs-lookup"><span data-stu-id="b5102-192">Power BI Vendor List</span></span>
- <span data-ttu-id="b5102-193">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="b5102-193">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="b5102-194">Rapportetiketter för Power BI</span><span class="sxs-lookup"><span data-stu-id="b5102-194">Power BI Report Labels</span></span>

## <a name="web-services"></a><span data-ttu-id="b5102-195">Webbtjänster</span><span class="sxs-lookup"><span data-stu-id="b5102-195">Web Services</span></span>
<span data-ttu-id="b5102-196">Ett enkelt sätt att hitta webbtjänsterna är att söka efter webbtjänster via [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b5102-196">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="b5102-197">Se till att rutan Publicera markeras i lista för de webbtjänster som anges ovan.</span><span class="sxs-lookup"><span data-stu-id="b5102-197">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b5102-198">Felsökning</span><span class="sxs-lookup"><span data-stu-id="b5102-198">Troubleshooting</span></span>
<span data-ttu-id="b5102-199">Instrumentbrädan för Power BI förlitar sig på de publicerade webbtjänsterna som visas ovan, och kommer att innehålla data från demonstrationsföretaget eller ditt eget företag om du importerar data från den aktuella finanslösningen.</span><span class="sxs-lookup"><span data-stu-id="b5102-199">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="b5102-200">Men om något går fel kommer denna sektion att ge en tillfällig lösning för de vanligaste problemen.</span><span class="sxs-lookup"><span data-stu-id="b5102-200">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="b5102-201">Felaktigt företagsnamn</span><span class="sxs-lookup"><span data-stu-id="b5102-201">Incorrect Company Name</span></span>  
<span data-ttu-id="b5102-202">Ett vanligt fel är att ange företagets visningsnamn i stället för namnet på företaget.</span><span class="sxs-lookup"><span data-stu-id="b5102-202">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="b5102-203">Söka efter **Företag** för att hitta företagsnamnet.</span><span class="sxs-lookup"><span data-stu-id="b5102-203">To find the company name search for **Companies**.</span></span> <span data-ttu-id="b5102-204">Använda fältet **Namn** när du anger företagets namn.</span><span class="sxs-lookup"><span data-stu-id="b5102-204">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="b5102-205">Felaktigt användarnamn och lösenord</span><span class="sxs-lookup"><span data-stu-id="b5102-205">Incorrect User Name and Password</span></span>  
<span data-ttu-id="b5102-206">Användarnamn och lösenord som används för att ansluta blir desamma som används för att ansluta till ditt Microsoft Office 365-konto.</span><span class="sxs-lookup"><span data-stu-id="b5102-206">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="b5102-207">Innehållspaketen kräver också att du har ett Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto.</span><span class="sxs-lookup"><span data-stu-id="b5102-207">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="b5102-208">När du har angett dina autentiseringsuppgifter upptäcker vi automatiskt eventuella Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innehavare som du har tillgång till.</span><span class="sxs-lookup"><span data-stu-id="b5102-208">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="b5102-209">Om du inte har ett licensierat eller Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto eller en utvärderingsversion visas ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="b5102-209">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="b5102-210">Nyckeln matchade inte några rader i tabellen</span><span class="sxs-lookup"><span data-stu-id="b5102-210">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="b5102-211">Om du anger ogiltiga företagsnamn i samband med anslutningsprocessen kan du få felmeddelandet ”Nyckeln matchar inga rader i tabellen”.</span><span class="sxs-lookup"><span data-stu-id="b5102-211">If you enter a non-valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="b5102-212">Ange rätt företagsnamn och försök ansluta igen.</span><span class="sxs-lookup"><span data-stu-id="b5102-212">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5102-213">Se även</span><span class="sxs-lookup"><span data-stu-id="b5102-213">See Also</span></span>
[<span data-ttu-id="b5102-214">Kom igång med Power BI</span><span class="sxs-lookup"><span data-stu-id="b5102-214">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[<span data-ttu-id="b5102-215">Power BI - Grundläggande koncept</span><span class="sxs-lookup"><span data-stu-id="b5102-215">Power BI - Basic Concepts</span></span>](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[<span data-ttu-id="b5102-216">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="b5102-216">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="b5102-217">Komma igång</span><span class="sxs-lookup"><span data-stu-id="b5102-217">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="b5102-218">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="b5102-218">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="b5102-219">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="b5102-219">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="b5102-220">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="b5102-220">Finance</span></span>](finance.md)  
<span data-ttu-id="b5102-221">[Ställa in rapportering för [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="b5102-221">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

