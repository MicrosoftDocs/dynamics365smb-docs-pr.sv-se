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
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a><span data-ttu-id="97ab6-103">Ansluta Power BI till Business Central-innehållspaket</span><span class="sxs-lookup"><span data-stu-id="97ab6-103">Connecting Power BI to Business Central Content Packs</span></span>
<span data-ttu-id="97ab6-104">Att få insikter om dina Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data är enkelt med Power BI och Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innehållspaketen.</span><span class="sxs-lookup"><span data-stu-id="97ab6-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="97ab6-105">Power BI hämtar dina data och skapar sedan en förinstallerad instrumentbräda och rapporter baserade på den data.</span><span class="sxs-lookup"><span data-stu-id="97ab6-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="97ab6-106">Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Power BI.</span><span class="sxs-lookup"><span data-stu-id="97ab6-106">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Power BI.</span></span> <span data-ttu-id="97ab6-107">Dessutom måste du hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="97ab6-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="97ab6-108">Innehållspaket för Power BI kräver behörighet till de tabeller som data ska hämtas ifrån.</span><span class="sxs-lookup"><span data-stu-id="97ab6-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="97ab6-109">Mer information om kraven beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="97ab6-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="97ab6-110">Så här ansluter du</span><span class="sxs-lookup"><span data-stu-id="97ab6-110">How to Connect</span></span>
1. <span data-ttu-id="97ab6-111">Välj **Hämta Data** längst ned i den vänstra navigeringsrutan.</span><span class="sxs-lookup"><span data-stu-id="97ab6-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="97ab6-112">![Navigera för att hämta data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="97ab6-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="97ab6-113">I rutan **Tjänster**, markera **Hämta**.</span><span class="sxs-lookup"><span data-stu-id="97ab6-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="97ab6-114">Då öppnas ett fönster med **AppSource** och **Program för Power BI-program**.</span><span class="sxs-lookup"><span data-stu-id="97ab6-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="97ab6-115">![Välj innehållspaket bland onlinetjänsterna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="97ab6-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="97ab6-116">Markera **Program** i fliken **Program för Power BI-program**, välj det innehåll för **Microsoft Dynamics 365 Business Central** som du vill använda och välj sedan **Hämta nu**.</span><span class="sxs-lookup"><span data-stu-id="97ab6-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="97ab6-117">![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="97ab6-117">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="97ab6-118">Ange namnet på *ditt företag* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] när du uppmanas att göra så.</span><span class="sxs-lookup"><span data-stu-id="97ab6-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="97ab6-119">Detta är inte visningsnamnet.</span><span class="sxs-lookup"><span data-stu-id="97ab6-119">This is not the display name.</span></span>  
<span data-ttu-id="97ab6-120">![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="97ab6-120">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="97ab6-121">När anslutningen har genomförts kommer instrumentpanel, rapport och datauppsättning automatiskt att laddas till din Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="97ab6-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="97ab6-122">När laddningen är slutförd kommer panelerna att uppdateras med information från ditt konto.</span><span class="sxs-lookup"><span data-stu-id="97ab6-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="97ab6-123">![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="97ab6-123">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="97ab6-124">Vad nu?</span><span class="sxs-lookup"><span data-stu-id="97ab6-124">What Now?</span></span>

- <span data-ttu-id="97ab6-125">[Ändra panelerna](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) på instrumentpanelen.</span><span class="sxs-lookup"><span data-stu-id="97ab6-125">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="97ab6-126">[Välj en panel](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) för att öppna den underliggande rapporten.</span><span class="sxs-lookup"><span data-stu-id="97ab6-126">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="97ab6-127">Din datauppsättning schemaläggs att uppdateras dagligen, men du kan ändra uppdateringsschemat eller uppdatera det på begäran med hjälp av **Uppdatera nu**.</span><span class="sxs-lookup"><span data-stu-id="97ab6-127">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="97ab6-128">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="97ab6-128">System Requirements</span></span>
<span data-ttu-id="97ab6-129">För att importera dina [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data i Power BI måste du ha behörighet till de webbtjänster som används för att hämta data.</span><span class="sxs-lookup"><span data-stu-id="97ab6-129">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="97ab6-130">De webbtjänster som krävs för respektive innehållspaket är:</span><span class="sxs-lookup"><span data-stu-id="97ab6-130">The web services required for each content pack include:</span></span>

<span data-ttu-id="97ab6-131">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="97ab6-131">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="97ab6-132">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="97ab6-132">SalesOpportunities</span></span>
- <span data-ttu-id="97ab6-133">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="97ab6-133">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="97ab6-134">**Microsoft Dynamics 365 Business Central – Sales**</span><span class="sxs-lookup"><span data-stu-id="97ab6-134">**Microsoft Dynamics 365 Business Central – Sales**</span></span>
- <span data-ttu-id="97ab6-135">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="97ab6-135">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="97ab6-136">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="97ab6-136">SalesDashboard</span></span>
- <span data-ttu-id="97ab6-137">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="97ab6-137">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="97ab6-138">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="97ab6-138">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="97ab6-139">Power BIFinance</span><span class="sxs-lookup"><span data-stu-id="97ab6-139">PowerBIFinance</span></span>
- <span data-ttu-id="97ab6-140">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="97ab6-140">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="97ab6-141">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="97ab6-141">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="97ab6-142">Projektlista</span><span class="sxs-lookup"><span data-stu-id="97ab6-142">Job List</span></span>
- <span data-ttu-id="97ab6-143">Projektplaneringsrader</span><span class="sxs-lookup"><span data-stu-id="97ab6-143">Job Planning Lines</span></span>
- <span data-ttu-id="97ab6-144">Projektaktivitetsrader</span><span class="sxs-lookup"><span data-stu-id="97ab6-144">Job Task Lines</span></span>

<span data-ttu-id="97ab6-145">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="97ab6-145">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="97ab6-146">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="97ab6-146">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="97ab6-147">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="97ab6-147">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="97ab6-148">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="97ab6-148">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="97ab6-149">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="97ab6-149">SalesDashboard</span></span>
- <span data-ttu-id="97ab6-150">Power BI kundlista</span><span class="sxs-lookup"><span data-stu-id="97ab6-150">Power_BI_Customer_List</span></span>
- <span data-ttu-id="97ab6-151">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="97ab6-151">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="97ab6-152">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="97ab6-152">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="97ab6-153">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="97ab6-153">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="97ab6-154">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="97ab6-154">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="97ab6-155">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="97ab6-155">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="97ab6-156">Artiklar</span><span class="sxs-lookup"><span data-stu-id="97ab6-156">Items</span></span>
- <span data-ttu-id="97ab6-157">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="97ab6-157">SalesDashboard</span></span>
- <span data-ttu-id="97ab6-158">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="97ab6-158">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="97ab6-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="97ab6-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="97ab6-160">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="97ab6-160">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="97ab6-161">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="97ab6-161">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="97ab6-162">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="97ab6-162">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="97ab6-163">Artiklar</span><span class="sxs-lookup"><span data-stu-id="97ab6-163">Items</span></span>
- <span data-ttu-id="97ab6-164">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="97ab6-164">SalesDashboard</span></span>
- <span data-ttu-id="97ab6-165">Power BI kundlista</span><span class="sxs-lookup"><span data-stu-id="97ab6-165">Power_BI_Customer_List</span></span>
- <span data-ttu-id="97ab6-166">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="97ab6-166">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="97ab6-167">Power BI leverantörslista</span><span class="sxs-lookup"><span data-stu-id="97ab6-167">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="97ab6-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="97ab6-168">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="97ab6-169">Webbtjänster</span><span class="sxs-lookup"><span data-stu-id="97ab6-169">Web Services</span></span>
<span data-ttu-id="97ab6-170">Ett enkelt sätt att hitta webbtjänsterna är att söka efter webbtjänster via [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="97ab6-170">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="97ab6-171">Se till att rutan Publicera markeras i lista för de webbtjänster som anges ovan.</span><span class="sxs-lookup"><span data-stu-id="97ab6-171">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="97ab6-172">Felsökning</span><span class="sxs-lookup"><span data-stu-id="97ab6-172">Troubleshooting</span></span>
<span data-ttu-id="97ab6-173">Instrumentbrädan för Power BI förlitar sig på de publicerade webbtjänsterna som visas ovan, och kommer att innehålla data från demonstrationsföretaget eller ditt eget företag om du importerar data från den aktuella finanslösningen.</span><span class="sxs-lookup"><span data-stu-id="97ab6-173">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="97ab6-174">Men om något går fel kommer denna sektion att ge en tillfällig lösning för de vanligaste problemen.</span><span class="sxs-lookup"><span data-stu-id="97ab6-174">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="97ab6-175">Felaktigt företagsnamn</span><span class="sxs-lookup"><span data-stu-id="97ab6-175">Incorrect Company Name</span></span>  
<span data-ttu-id="97ab6-176">Ett vanligt fel är att ange företagets visningsnamn i stället för namnet på företaget.</span><span class="sxs-lookup"><span data-stu-id="97ab6-176">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="97ab6-177">Söka efter **Företag** för att hitta företagsnamnet.</span><span class="sxs-lookup"><span data-stu-id="97ab6-177">To find the company name search for **Companies**.</span></span> <span data-ttu-id="97ab6-178">Använda fältet **Namn** när du anger företagets namn.</span><span class="sxs-lookup"><span data-stu-id="97ab6-178">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="97ab6-179">Felaktigt användarnamn och lösenord</span><span class="sxs-lookup"><span data-stu-id="97ab6-179">Incorrect User Name and Password</span></span>  
<span data-ttu-id="97ab6-180">Användarnamn och lösenord som används för att ansluta blir desamma som används för att ansluta till ditt Microsoft Office 365-konto.</span><span class="sxs-lookup"><span data-stu-id="97ab6-180">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="97ab6-181">Innehållspaketen kräver också att du har ett Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto.</span><span class="sxs-lookup"><span data-stu-id="97ab6-181">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="97ab6-182">När du har angett dina autentiseringsuppgifter upptäcker vi automatiskt eventuella Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innehavare som du har tillgång till.</span><span class="sxs-lookup"><span data-stu-id="97ab6-182">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="97ab6-183">Om du inte har ett licensierat eller Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto eller en utvärderingsversion visas ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="97ab6-183">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="97ab6-184">Nyckeln matchade inte några rader i tabellen</span><span class="sxs-lookup"><span data-stu-id="97ab6-184">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="97ab6-185">Om du anger ogiltiga företagsnamn i samband med anslutningsprocessen kan du få felmeddelandet ”nyckeln matchar inte har några rader i tabellen”.</span><span class="sxs-lookup"><span data-stu-id="97ab6-185">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="97ab6-186">Ange rätt företagsnamn och försök ansluta igen.</span><span class="sxs-lookup"><span data-stu-id="97ab6-186">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="97ab6-187">Se även</span><span class="sxs-lookup"><span data-stu-id="97ab6-187">See Also</span></span>
[<span data-ttu-id="97ab6-188">Kom igång med Power BI</span><span class="sxs-lookup"><span data-stu-id="97ab6-188">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="97ab6-189">[Power BI - Grundläggande begrepp](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span><span class="sxs-lookup"><span data-stu-id="97ab6-189">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="97ab6-190">[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="97ab6-190">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="97ab6-191">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="97ab6-191">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="97ab6-192">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="97ab6-192">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="97ab6-193">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="97ab6-193">Finance</span></span>](finance.md)  
<span data-ttu-id="97ab6-194">[Ställa in rapportering för [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="97ab6-194">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

