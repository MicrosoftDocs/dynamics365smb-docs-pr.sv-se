---
title: Ansluta Power BI till Finance and Operations, Business edition | Microsoft Docs
description: "Att få insyn, affärslogik och KPI:er från dina Finance and Operations, Business edition-data är enkelt med Power BI och innehållspaketen för Finance and Operations, Business edition."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 02/05/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: aff8d95b13f795fa12d3146e5613712fb3baf9b4
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-finance-and-operations-business-edition-content-packs"></a><span data-ttu-id="53589-103">Ansluta Power BI till innehållspaket för Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="53589-103">Connecting Power BI to Finance and Operations, Business edition Content Packs</span></span>
<span data-ttu-id="53589-104">Att få insikter om dina Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data är enkelt med Power BI och Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innehållspaketen.</span><span class="sxs-lookup"><span data-stu-id="53589-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="53589-105">Power BI hämtar dina data och skapar sedan en förinstallerad instrumentbräda och rapporter baserade på den data.</span><span class="sxs-lookup"><span data-stu-id="53589-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="53589-106">Du måste ha ett giltigt konto med Dynamics 365 och med Power BI.</span><span class="sxs-lookup"><span data-stu-id="53589-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="53589-107">Dessutom måste du hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="53589-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="53589-108">Innehållspaket för Power BI kräver behörighet till de tabeller som data ska hämtas ifrån.</span><span class="sxs-lookup"><span data-stu-id="53589-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="53589-109">Mer information om kraven beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="53589-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="53589-110">Så här ansluter du</span><span class="sxs-lookup"><span data-stu-id="53589-110">How to Connect</span></span>
1. <span data-ttu-id="53589-111">Välj **Hämta Data** längst ned i den vänstra navigeringsrutan.</span><span class="sxs-lookup"><span data-stu-id="53589-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="53589-112">![Navigera för att hämta data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="53589-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="53589-113">I rutan **Tjänster**, markera **Hämta**.</span><span class="sxs-lookup"><span data-stu-id="53589-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="53589-114">Då öppnas ett fönster med **AppSource** och **Program för Power BI-program**.</span><span class="sxs-lookup"><span data-stu-id="53589-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="53589-115">![Välj innehållspaket bland onlinetjänsterna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="53589-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="53589-116">Markera **Program** i fliken **Program för Power BI-program**, välj det innehåll för **Microsoft Dynamics 365 for Finance and Operations** som du vill använda och välj sedan **Hämta nu**.</span><span class="sxs-lookup"><span data-stu-id="53589-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 for Finance and Operations** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="53589-117">![Välj Dynamics 365 for Finance and Operations, Business edition och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="53589-117">![Select Dynamics 365 for Finance and Operations, Business edition and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="53589-118">Ange namnet på *ditt företag* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] när du uppmanas att göra så.</span><span class="sxs-lookup"><span data-stu-id="53589-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="53589-119">Detta är inte visningsnamnet.</span><span class="sxs-lookup"><span data-stu-id="53589-119">This is not the display name.</span></span>  
<span data-ttu-id="53589-120">![Välj Dynamics 365 for Finance and Operations, Business edition och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="53589-120">![Select Dynamics 365 for Finance and Operations, Business edition and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="53589-121">När anslutningen har genomförts kommer instrumentpanel, rapport och datauppsättning automatiskt att laddas till din Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="53589-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="53589-122">När laddningen är slutförd kommer panelerna att uppdateras med information från ditt konto.</span><span class="sxs-lookup"><span data-stu-id="53589-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="53589-123">![Välj Dynamics 365 for Finance and Operations, Business edition och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="53589-123">![Select Dynamics 365 for Finance and Operations, Business edition  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="53589-124">Vad nu?</span><span class="sxs-lookup"><span data-stu-id="53589-124">What Now?</span></span>

- <span data-ttu-id="53589-125">Försök med att [ställa en fråga i rutan Frågor och svar](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) högst upp i instrumentpanelen.</span><span class="sxs-lookup"><span data-stu-id="53589-125">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>  
- <span data-ttu-id="53589-126">[Ändra panelerna](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) på instrumentpanelen.</span><span class="sxs-lookup"><span data-stu-id="53589-126">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="53589-127">[Välj en panel](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) för att öppna den underliggande rapporten.</span><span class="sxs-lookup"><span data-stu-id="53589-127">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="53589-128">Din datauppsättning schemaläggs att uppdateras dagligen, men du kan ändra uppdateringsschemat eller uppdatera det på begäran med hjälp av **Uppdatera nu**.</span><span class="sxs-lookup"><span data-stu-id="53589-128">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="53589-129">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="53589-129">System Requirements</span></span>
<span data-ttu-id="53589-130">För att importera dina [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data i Power BI måste du ha behörighet till de webbtjänster som används för att hämta data.</span><span class="sxs-lookup"><span data-stu-id="53589-130">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="53589-131">De webbtjänster som krävs för respektive innehållspaket är:</span><span class="sxs-lookup"><span data-stu-id="53589-131">The web services required for each content pack include:</span></span>

<span data-ttu-id="53589-132">**Microsoft Dynamics 365 for Finance and Operations, Business edition – CRM**</span><span class="sxs-lookup"><span data-stu-id="53589-132">**Microsoft Dynamics 365 for Finance and Operations, Business edition – CRM**</span></span>
- <span data-ttu-id="53589-133">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="53589-133">SalesOpportunities</span></span>
- <span data-ttu-id="53589-134">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="53589-134">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="53589-135">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Sales**</span><span class="sxs-lookup"><span data-stu-id="53589-135">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Sales**</span></span>
- <span data-ttu-id="53589-136">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="53589-136">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="53589-137">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="53589-137">SalesDashboard</span></span>
- <span data-ttu-id="53589-138">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="53589-138">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="53589-139">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Finance**</span><span class="sxs-lookup"><span data-stu-id="53589-139">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Finance**</span></span>
- <span data-ttu-id="53589-140">Power BIFinance</span><span class="sxs-lookup"><span data-stu-id="53589-140">PowerBIFinance</span></span>
- <span data-ttu-id="53589-141">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="53589-141">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="53589-142">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Jobs**</span><span class="sxs-lookup"><span data-stu-id="53589-142">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Jobs**</span></span>
- <span data-ttu-id="53589-143">Projektlista</span><span class="sxs-lookup"><span data-stu-id="53589-143">Job List</span></span>
- <span data-ttu-id="53589-144">Projektplaneringsrader</span><span class="sxs-lookup"><span data-stu-id="53589-144">Job Planning Lines</span></span>
- <span data-ttu-id="53589-145">Projektaktivitetsrader</span><span class="sxs-lookup"><span data-stu-id="53589-145">Job Task Lines</span></span>

<span data-ttu-id="53589-146">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Customers List**</span><span class="sxs-lookup"><span data-stu-id="53589-146">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Customers List**</span></span>
- <span data-ttu-id="53589-147">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="53589-147">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="53589-148">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="53589-148">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="53589-149">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="53589-149">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="53589-150">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="53589-150">SalesDashboard</span></span>
- <span data-ttu-id="53589-151">Power BI kundlista</span><span class="sxs-lookup"><span data-stu-id="53589-151">Power_BI_Customer_List</span></span>
- <span data-ttu-id="53589-152">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="53589-152">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="53589-153">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Items List**</span><span class="sxs-lookup"><span data-stu-id="53589-153">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Items List**</span></span>
- <span data-ttu-id="53589-154">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="53589-154">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="53589-155">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="53589-155">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="53589-156">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="53589-156">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="53589-157">Artiklar</span><span class="sxs-lookup"><span data-stu-id="53589-157">Items</span></span>
- <span data-ttu-id="53589-158">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="53589-158">SalesDashboard</span></span>
- <span data-ttu-id="53589-159">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="53589-159">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="53589-160">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="53589-160">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Vendors List**</span></span>
- <span data-ttu-id="53589-161">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="53589-161">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="53589-162">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="53589-162">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="53589-163">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="53589-163">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="53589-164">Artiklar</span><span class="sxs-lookup"><span data-stu-id="53589-164">Items</span></span>
- <span data-ttu-id="53589-165">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="53589-165">SalesDashboard</span></span>
- <span data-ttu-id="53589-166">Power BI kundlista</span><span class="sxs-lookup"><span data-stu-id="53589-166">Power_BI_Customer_List</span></span>
- <span data-ttu-id="53589-167">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="53589-167">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="53589-168">Power BI leverantörslista</span><span class="sxs-lookup"><span data-stu-id="53589-168">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="53589-169">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="53589-169">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="53589-170">Webbtjänster</span><span class="sxs-lookup"><span data-stu-id="53589-170">Web Services</span></span>
<span data-ttu-id="53589-171">Ett enkelt sätt att hitta webbtjänsterna är att söka efter webbtjänster via [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="53589-171">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="53589-172">Se till att rutan Publicera markeras i lista för de webbtjänster som anges ovan.</span><span class="sxs-lookup"><span data-stu-id="53589-172">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="53589-173">Felsökning</span><span class="sxs-lookup"><span data-stu-id="53589-173">Troubleshooting</span></span>
<span data-ttu-id="53589-174">Instrumentbrädan för Power BI förlitar sig på de publicerade webbtjänsterna som visas ovan, och kommer att innehålla data från demonstrationsföretaget eller ditt eget företag om du importerar data från den aktuella finanslösningen.</span><span class="sxs-lookup"><span data-stu-id="53589-174">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="53589-175">Men om något går fel kommer denna sektion att ge en tillfällig lösning för de vanligaste problemen.</span><span class="sxs-lookup"><span data-stu-id="53589-175">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="53589-176">Felaktigt företagsnamn</span><span class="sxs-lookup"><span data-stu-id="53589-176">Incorrect Company Name</span></span>  
<span data-ttu-id="53589-177">Ett vanligt fel är att ange företagets visningsnamn i stället för namnet på företaget.</span><span class="sxs-lookup"><span data-stu-id="53589-177">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="53589-178">Söka efter **Företag** för att hitta företagsnamnet.</span><span class="sxs-lookup"><span data-stu-id="53589-178">To find the company name search for **Companies**.</span></span> <span data-ttu-id="53589-179">Använda fältet **Namn** när du anger företagets namn.</span><span class="sxs-lookup"><span data-stu-id="53589-179">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="53589-180">Felaktigt användarnamn och lösenord</span><span class="sxs-lookup"><span data-stu-id="53589-180">Incorrect User Name and Password</span></span>  
<span data-ttu-id="53589-181">Användarnamn och lösenord som används för att ansluta blir desamma som används för att ansluta till ditt Microsoft Office 365-konto.</span><span class="sxs-lookup"><span data-stu-id="53589-181">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="53589-182">Innehållspaketen kräver också att du har ett Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto.</span><span class="sxs-lookup"><span data-stu-id="53589-182">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="53589-183">När du har angett dina autentiseringsuppgifter upptäcker vi automatiskt eventuella Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innehavare som du har tillgång till.</span><span class="sxs-lookup"><span data-stu-id="53589-183">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="53589-184">Om du inte har ett licensierat eller Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto eller en utvärderingsversion visas ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="53589-184">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="53589-185">Nyckeln matchade inte några rader i tabellen</span><span class="sxs-lookup"><span data-stu-id="53589-185">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="53589-186">Om du anger ogiltiga företagsnamn i samband med anslutningsprocessen kan du få felmeddelandet ”nyckeln matchar inte har några rader i tabellen”.</span><span class="sxs-lookup"><span data-stu-id="53589-186">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="53589-187">Ange rätt företagsnamn och försök ansluta igen.</span><span class="sxs-lookup"><span data-stu-id="53589-187">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="53589-188">Se även</span><span class="sxs-lookup"><span data-stu-id="53589-188">See Also</span></span>
[<span data-ttu-id="53589-189">Kom igång med Power BI</span><span class="sxs-lookup"><span data-stu-id="53589-189">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="53589-190">[Power BI - Grundläggande begrepp](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span><span class="sxs-lookup"><span data-stu-id="53589-190">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="53589-191">[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="53589-191">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="53589-192">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="53589-192">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="53589-193">[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="53589-193">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="53589-194">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="53589-194">Finance</span></span>](finance.md)  
<span data-ttu-id="53589-195">[Ställa in rapportering för [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="53589-195">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

