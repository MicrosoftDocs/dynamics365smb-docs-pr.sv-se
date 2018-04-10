---
title: "Förbereda migrering av kunddata | Microsoft Docs"
description: "När du har importerat och kopplat inställningsdatan i den nya databasen, kan du börja migrera kundens befintliga huvuddata, till exempel artikel- och kundnummer samt namn. För att se till att dessa data, skapas snabbt och exakt i det nya företaget, måste du använda mallar för att strukturera data."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3cfc53c1ea3c8d30f65b2d475a8dab052519e81e
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="prepare-to-migrate-customer-data"></a><span data-ttu-id="30dfa-104">Förbereda migrering av kunddata</span><span class="sxs-lookup"><span data-stu-id="30dfa-104">Prepare to Migrate Customer Data</span></span>
<span data-ttu-id="30dfa-105">När du har importerat och kopplat inställningsdatan i den nya databasen, kan du börja migrera kundens befintliga huvuddata, till exempel artikel- och kundnummer samt namn.</span><span class="sxs-lookup"><span data-stu-id="30dfa-105">After you import and apply setup data in the new database, you can start migrating the customer’s existing master data, such as item and customer numbers and names.</span></span> <span data-ttu-id="30dfa-106">För att se till att dessa data, skapas snabbt och exakt i det nya företaget, måste du använda mallar för att strukturera data.</span><span class="sxs-lookup"><span data-stu-id="30dfa-106">To make sure that this data is created quickly and accurately in the new company, you should use templates to structure the data.</span></span>  

<span data-ttu-id="30dfa-107">Vanligtvis skapar du datamallar för följande huvuddatatabeller:</span><span class="sxs-lookup"><span data-stu-id="30dfa-107">Typically, you create data templates for the following master data tables:</span></span>  

-   <span data-ttu-id="30dfa-108">**Kontakt**</span><span class="sxs-lookup"><span data-stu-id="30dfa-108">**Contact**</span></span>  
-   <span data-ttu-id="30dfa-109">**Kund**</span><span class="sxs-lookup"><span data-stu-id="30dfa-109">**Customer**</span></span>  
-   <span data-ttu-id="30dfa-110">**Artikel**</span><span class="sxs-lookup"><span data-stu-id="30dfa-110">**Item**</span></span>  
-   <span data-ttu-id="30dfa-111">**Leverantör**</span><span class="sxs-lookup"><span data-stu-id="30dfa-111">**Vendor**</span></span>  

<span data-ttu-id="30dfa-112">Du kan dock skapa en mall struktur för, och koppla dem till valfri tabell i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="30dfa-112">However, you can create a template structure for and apply it to any table in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

> [!TIP]  
>  <span data-ttu-id="30dfa-113">Du kan också använda datamallar för dagliga operationer för att skapa nya poster som baseras på mallar.</span><span class="sxs-lookup"><span data-stu-id="30dfa-113">You can also use data templates for daily operations to create new records that are based on templates.</span></span> <span data-ttu-id="30dfa-114">Dessa datamallar fungerar bara för de huvuddata tabellerna som stöds.</span><span class="sxs-lookup"><span data-stu-id="30dfa-114">These data templates only work for the supported master data tables.</span></span> <span data-ttu-id="30dfa-115">Mer information finns i exempelvis [Registrera nya artiklar](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="30dfa-115">For more information, see, for example, [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="30dfa-116">När du importerar kunddata från en fil, på samma sätt som för objekt, hämtas obligatoriska fältdata från den länkade datamallen.</span><span class="sxs-lookup"><span data-stu-id="30dfa-116">When you import customer data, such as for items, from a file, the mandatory field data that you have specified is taken from the linked data template.</span></span> <span data-ttu-id="30dfa-117">När du skapar en ny artikel anger du endast allmän information som namn, beskrivning och pris, och hämtar resten av obligatoriska fältdata från en vald datamall.</span><span class="sxs-lookup"><span data-stu-id="30dfa-117">When you create a new item, you only enter general information such as item name, description, and price and then collect the rest of the mandatory field data from a selected data template.</span></span>  

<span data-ttu-id="30dfa-118">När du skapar en ny huvuddatapost, till exempel ett kundkort, är vissa fält obligatoriska och måste fyllas i.</span><span class="sxs-lookup"><span data-stu-id="30dfa-118">When you create a new master data record, such as a customer card, some fields are mandatory and must be filled in.</span></span> <span data-ttu-id="30dfa-119">Du kan gruppera de flesta obligatoriska fält, till exempel bokföringsgrupper och betalningsvillkor, för att skapa huvuddata registrerar enklare och stabilare.</span><span class="sxs-lookup"><span data-stu-id="30dfa-119">You can group most mandatory fields, such as posting groups and payment terms, to make creating master data records easier and more stable.</span></span> <span data-ttu-id="30dfa-120">Du kan till exempel gruppera obligatoriska fält för tabell 18, **Kund**, som **Inrikes**, **Utrikes**eller **Exportera** typer.</span><span class="sxs-lookup"><span data-stu-id="30dfa-120">For example, you can group mandatory fields for table 18, **Customer**, as **Domestic**, **Foreign**, or **Export** types.</span></span>

## <a name="to-select-a-data-template"></a><span data-ttu-id="30dfa-121">Så här väljer du en datamall</span><span class="sxs-lookup"><span data-stu-id="30dfa-121">To select a data template</span></span>
<span data-ttu-id="30dfa-122">När du väljer en befintlig datamall måste du utvärderar om de mallar som du skapat för det nya företaget är tillräckliga för kunden.</span><span class="sxs-lookup"><span data-stu-id="30dfa-122">When you select an existing data template, you must evaluate if the templates that you created for the new company are sufficient for the customer.</span></span> <span data-ttu-id="30dfa-123">Granska fälten och värdena för att bestämma vilka mallar som är lämpligt för ett nytt företag.</span><span class="sxs-lookup"><span data-stu-id="30dfa-123">Review the provided fields and values to determine which templates are appropriate for a new company.</span></span>  

> [!TIP]  
>  <span data-ttu-id="30dfa-124">Med dessa datamallar kan du också snabbt skapa nya poster.</span><span class="sxs-lookup"><span data-stu-id="30dfa-124">You can also use data templates to create new records quickly.</span></span> <span data-ttu-id="30dfa-125">Använd dem för snabbare och mer korrekt dataskapande.</span><span class="sxs-lookup"><span data-stu-id="30dfa-125">Use them for faster and more accurate data creation.</span></span> <span data-ttu-id="30dfa-126">Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="30dfa-126">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>

1. <span data-ttu-id="30dfa-127">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Konfigurationsmallar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="30dfa-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Configuration Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="30dfa-128">I fönstret **Konfig. mallista** väljer du en datamall i listan och sedan åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-128">In the **Config. Template List** window, select a data template from the list, and then choose the **Edit** action.</span></span>  

<span data-ttu-id="30dfa-129">Om standardmallarna inte uppfyller behoven kan du skapa nya mallar eller lägga till fält i en befintlig mall.</span><span class="sxs-lookup"><span data-stu-id="30dfa-129">If the default templates do not meet your needs, you can create new templates or add fields to an existing template.</span></span> <span data-ttu-id="30dfa-130">Om standardmallarna är tillräckliga, kan du använda dem för att skapa transaktioner som baseras på huvuddatamallar.</span><span class="sxs-lookup"><span data-stu-id="30dfa-130">If the default templates are sufficient, you can use them to create records based on master data templates.</span></span>

## <a name="to-create-a-data-template"></a><span data-ttu-id="30dfa-131">För att skapa en datamall</span><span class="sxs-lookup"><span data-stu-id="30dfa-131">To create a data template</span></span>
<span data-ttu-id="30dfa-132">Du kan skapa en ny datamall, om standardmallarna inte inte uppfyller behoven för ditt nya företag.</span><span class="sxs-lookup"><span data-stu-id="30dfa-132">You can create a new data template if the default templates do not the needs of your new company.</span></span> <span data-ttu-id="30dfa-133">Om du skapar fler än en kan det vara praktiskt att anta en namnpraxis för fältet **Kod**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-133">If you are creating more than one, you may find it useful to adopt a naming convention for the **Code** field.</span></span>

<span data-ttu-id="30dfa-134">Varje mall består av ett huvud och rader.</span><span class="sxs-lookup"><span data-stu-id="30dfa-134">Each template consists of a header and lines.</span></span> <span data-ttu-id="30dfa-135">När du skapar en mall, kan du ange vilka fält som alltid ska användas för data av en viss typ.</span><span class="sxs-lookup"><span data-stu-id="30dfa-135">When you create a template, you can specify which fields to always apply to data of a certain type.</span></span> <span data-ttu-id="30dfa-136">Du kan till exempel skapa olika kundmallar som ska kopplas till olika kundtyper.</span><span class="sxs-lookup"><span data-stu-id="30dfa-136">For example, you can create different customer templates to apply to different customer types.</span></span> <span data-ttu-id="30dfa-137">När du skapar kunden som använder en mall kan du använda malldata för att fylla i vissa fält i förväg.</span><span class="sxs-lookup"><span data-stu-id="30dfa-137">When you create the customer using a template, you can use template data to prepopulate certain fields.</span></span>

### <a name="to-create-a-data-template-header"></a><span data-ttu-id="30dfa-138">Så här skapar du ett datamallhuvud</span><span class="sxs-lookup"><span data-stu-id="30dfa-138">To create a data template header</span></span>
1. <span data-ttu-id="30dfa-139">Öppna fönstret **Konfig. mallista**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-139">Open the **Config. Template List** window.</span></span>
2. <span data-ttu-id="30dfa-140">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-140">Choose the **New** action.</span></span>
3. <span data-ttu-id="30dfa-141">I fältet **Tabell-ID** anger du den tabell som denna mall avser.</span><span class="sxs-lookup"><span data-stu-id="30dfa-141">In the **Table ID** field, enter the table to which this template applies.</span></span> <span data-ttu-id="30dfa-142">Fältet **Tabellnamn** fylls i automatiskt när fältet **Tabell-ID** ställs in.</span><span class="sxs-lookup"><span data-stu-id="30dfa-142">The **Table Name** field is automatically filled in when the **Table ID** field is set.</span></span>

### <a name="to-create-a-data-template-line"></a><span data-ttu-id="30dfa-143">Så här skapar du ett datamallrad</span><span class="sxs-lookup"><span data-stu-id="30dfa-143">To create a data template line</span></span>
1. <span data-ttu-id="30dfa-144">På första raden väljer du fältet **Fältnamn**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-144">On the first line, select the **Field Name** field.</span></span> <span data-ttu-id="30dfa-145">I fönstret **Fältlista** visas en lista över tabellens fält.</span><span class="sxs-lookup"><span data-stu-id="30dfa-145">The **Field List** window displays the list of fields in the table.</span></span>
2. <span data-ttu-id="30dfa-146">Markera ett fält och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-146">Select a field, and then choose the **OK** button.</span></span> <span data-ttu-id="30dfa-147">Fältet **Fälttext** fylls i med fältnamnet.</span><span class="sxs-lookup"><span data-stu-id="30dfa-147">The **Field Caption** field is filled in with the field name.</span></span>
3. <span data-ttu-id="30dfa-148">I fältet **Standardvärde** anger du ett lämpligt värde.</span><span class="sxs-lookup"><span data-stu-id="30dfa-148">In the **Default Value** field, enter an appropriate value.</span></span> <span data-ttu-id="30dfa-149">I vissa fall kan du behöva använda ett värde som inte finns tillgängligt i databasen.</span><span class="sxs-lookup"><span data-stu-id="30dfa-149">In some cases, you may want to use a value that is not a value that is available in the database.</span></span> <span data-ttu-id="30dfa-150">I så fall kan du markera kryssrutan **Hoppa över relationskontroll** för att göra det möjligt att applicera data utan fel.</span><span class="sxs-lookup"><span data-stu-id="30dfa-150">In that case, you can select the **Skip Relation Check** check box, to make it possible to apply data without error.</span></span>

    > [!TIP]  
    > <span data-ttu-id="30dfa-151">Eftersom fältet **Standardvärde** inte har ett uppslag till motsvarande [!INCLUDE[d365fin](includes/d365fin_md.md)]-fältalternativ kopierar och klistrar du in det värde som du vill ha från den relaterade sidan till mallen.</span><span class="sxs-lookup"><span data-stu-id="30dfa-151">Since the **Default Value** field does not have a look up to the corresponding [!INCLUDE[d365fin](includes/d365fin_md.md)] field options, you copy and paste the value that you want from the related page into the template.</span></span>

    > <span data-ttu-id="30dfa-152">Markera kryssrutan **Obligatoriskt**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-152">Select the **Mandatory** check box.</span></span> <span data-ttu-id="30dfa-153">Kryssrutan är endast för information.</span><span class="sxs-lookup"><span data-stu-id="30dfa-153">The check box is informational only.</span></span> <span data-ttu-id="30dfa-154">Här får du information om att data måste skrivas in i fältet av användaren, men ingen affärslogik behövs.</span><span class="sxs-lookup"><span data-stu-id="30dfa-154">It tells you that information must be entered in the field by the user, but no business logic is enforced.</span></span> <span data-ttu-id="30dfa-155">Du kan till exempel inte fakturera och bokföra en order om bokföringsmallar inte har lagts upp.</span><span class="sxs-lookup"><span data-stu-id="30dfa-155">For example, you cannot invoice and post an order if posting groups have not been set up.</span></span> <span data-ttu-id="30dfa-156">Eftersom bokföringsmallar måste användas kan du markera kryssrutan **Obligatoriskt** för de här fälten.</span><span class="sxs-lookup"><span data-stu-id="30dfa-156">Since posting groups are required, you can select the **Mandatory** check box for those fields.</span></span>

3. <span data-ttu-id="30dfa-157">I fältet **Referens** anger du nödvändig information om fältet.</span><span class="sxs-lookup"><span data-stu-id="30dfa-157">In the **Reference** field, enter information about the field as needed.</span></span>
4. <span data-ttu-id="30dfa-158">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-158">Choose the **OK** button</span></span>

## <a name="to-export-to-a-template-in-excel"></a><span data-ttu-id="30dfa-159">För att exportera till en mall i Excel</span><span class="sxs-lookup"><span data-stu-id="30dfa-159">To export to a template in Excel</span></span>
<span data-ttu-id="30dfa-160">Du kan skapa en Excel-arbetsbok att använda som mall baserat på strukturen i en tabell för en befintlig databas, snabbt och effektivt.</span><span class="sxs-lookup"><span data-stu-id="30dfa-160">You can create an Excel workbook to serve as a template that is based on the structure of an existing database table quickly.</span></span> <span data-ttu-id="30dfa-161">Du kan sedan använda mallen för att samla ihop kunddata i ett konsekvent format för senare import till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="30dfa-161">You can then use the template to gather together customer data in a consistent format for later import into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="30dfa-162">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Konfigurationskalkylark** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="30dfa-162">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Configuration Worksheet**, and then choose the related link.</span></span>
2. <span data-ttu-id="30dfa-163">Lägg till en tabell i listan eller välj en befintlig tabell.</span><span class="sxs-lookup"><span data-stu-id="30dfa-163">Add a table to the list, or select an existing table.</span></span> <span data-ttu-id="30dfa-164">Mer information finns i [Administrera företagskonfigurationer i ett kalkylark](admin-how-to-manage-company-configuration-in-a-worksheet.md).</span><span class="sxs-lookup"><span data-stu-id="30dfa-164">For more information, see [Manage Company Configuration in a Worksheet](admin-how-to-manage-company-configuration-in-a-worksheet.md).</span></span>
3. <span data-ttu-id="30dfa-165">Definiera fälten från tabellen som ska ingå i mallen.</span><span class="sxs-lookup"><span data-stu-id="30dfa-165">Define the fields from the table that you want to include in the template.</span></span>
4. <span data-ttu-id="30dfa-166">Välj åtgärden **Exportera till mall**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-166">Choose the **Export to Template** action.</span></span>
5. <span data-ttu-id="30dfa-167">Ange ett namn och spara Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="30dfa-167">Name and save the Excel file.</span></span> <span data-ttu-id="30dfa-168">Excel-arbetsboken öppnas automatiskt.</span><span class="sxs-lookup"><span data-stu-id="30dfa-168">The Excel workbook is automatically opened.</span></span>

<span data-ttu-id="30dfa-169">Nu kan du ange kunddata i Excel-bladet.</span><span class="sxs-lookup"><span data-stu-id="30dfa-169">You can now enter customer data in the Excel worksheet.</span></span> <span data-ttu-id="30dfa-170">Om du har exporterat flera tabeller är varje tabell ett eget blad.</span><span class="sxs-lookup"><span data-stu-id="30dfa-170">If you have exported multiple tables, each table will be on its own worksheet.</span></span> <span data-ttu-id="30dfa-171">Spara arbetsboken innan du fortsätter med nästa process.</span><span class="sxs-lookup"><span data-stu-id="30dfa-171">Save the workbook before you continue with the next procedure.</span></span>

> [!NOTE]  
> <span data-ttu-id="30dfa-172">Följande fel kan uppstå om du kör en engelsk version av Excel men har konfigurerat regionala inställningar för ett annat språk än engelska: "Gammalt format eller ogiltig bibliotekstyp."</span><span class="sxs-lookup"><span data-stu-id="30dfa-172">You may encounter the following error when you run an English version of Excel, but have your regional settings configured for a non-English language: "Old format or invalid type library."</span></span> <span data-ttu-id="30dfa-173">Kontrollera om språkpaketet för språket som används har installerats för att åtgärda felet.</span><span class="sxs-lookup"><span data-stu-id="30dfa-173">To fix this error, make sure that the language pack for the non-English language is installed.</span></span>

## <a name="to-import-from-a-template-in-excel"></a><span data-ttu-id="30dfa-174">Så här kan du importera från en mall i Excel</span><span class="sxs-lookup"><span data-stu-id="30dfa-174">To import from a template in Excel</span></span>
1. <span data-ttu-id="30dfa-175">I fönstret **Konfig. kalkylark** väljer du åtgärden **Importera från mall**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-175">In the **Config. Worksheet** window, choose the **Import from Template** action.</span></span>
3. <span data-ttu-id="30dfa-176">Navigera till mallkalkylarket som du har skapat och klicka på åtgärden **Öppna**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-176">Navigate to the template worksheet that you have created, and then choose the **Open** action.</span></span>
4. <span data-ttu-id="30dfa-177">Om du vill lägga till insamlade kunddata i databasen väljer du åtgärden **Koppla Data**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-177">To add the collected customer data to the database, choose the **Apply Data** action.</span></span>

<span data-ttu-id="30dfa-178">När du kopplar data från en mall i Excel till en undertabell som även har en konfigurationsmall kopplad till sig i konfigurationspaketet, kopplas standardfältvärdena från konfigurationsmallen också.</span><span class="sxs-lookup"><span data-stu-id="30dfa-178">When you apply data from a template in Excel to a table that also has a configuration template linked to it in the configuration package, the default field values from the configuration template are also applied.</span></span>

<span data-ttu-id="30dfa-179">En transaktion med data som kopplas på det här sättet är fullständig eftersom den består av data som har angetts av användaren i Excel plus standardvärden som anges i konfigurationsmallen.</span><span class="sxs-lookup"><span data-stu-id="30dfa-179">Any record whose data is applied in this manner is complete, because it consists of data entered by a user in Excel, plus the default values specified by the configuration template.</span></span>

## <a name="to-create-a-record-from-a-configuration-template"></a><span data-ttu-id="30dfa-180">Så här skapar du en post från en konfigurationsmall</span><span class="sxs-lookup"><span data-stu-id="30dfa-180">To create a record from a configuration template</span></span>
<span data-ttu-id="30dfa-181">Du kan använda strukturen av data som finns i datamallarna för att konvertera din information till poster i databasen, en efter en.</span><span class="sxs-lookup"><span data-stu-id="30dfa-181">You can use the structure of data that is contained in the data templates to convert your information into records in the database, one-by-one.</span></span> <span data-ttu-id="30dfa-182">För att kunna göra det använder du funktionen **Skapa instans**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-182">To do so, you use the **Create Instance** function.</span></span> <span data-ttu-id="30dfa-183">Detta är en miniatyrversion av datamigreringsprocessen och kan vara användbar för att skapa prototyper eller hantera mindre dataskapningsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="30dfa-183">This is a miniature version of the data migration process and can be useful for prototyping or treating smaller data creation tasks.</span></span>  

<span data-ttu-id="30dfa-184">Nedan visas hur du skapar ett artikelkort från en artikeldatamall.</span><span class="sxs-lookup"><span data-stu-id="30dfa-184">The following steps illustrate how to create an item card from an item data template.</span></span> <span data-ttu-id="30dfa-185">Du kan skapa en post från en datamall med samma procedur.</span><span class="sxs-lookup"><span data-stu-id="30dfa-185">You can create a record from any data template using the same procedure.</span></span>  

1. <span data-ttu-id="30dfa-186">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Konfigurationsmallar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="30dfa-186">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Configuration Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="30dfa-187">Välj mallen **Artikel** och sedan åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-187">Select the **Item** template, and then choose the **Edit** action.</span></span> <span data-ttu-id="30dfa-188">För mer information, se avsnittet "Så här skapar du en datamall".</span><span class="sxs-lookup"><span data-stu-id="30dfa-188">For more information, see the "To create a data template" section.</span></span>
3. <span data-ttu-id="30dfa-189">Välj åtgärden **Skapa instans**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-189">Choose the **Create Instance** action.</span></span> <span data-ttu-id="30dfa-190">Ett artikelkort skapas.</span><span class="sxs-lookup"><span data-stu-id="30dfa-190">An item card is created.</span></span>  
4. <span data-ttu-id="30dfa-191">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-191">Choose the **OK** button.</span></span>  
5. <span data-ttu-id="30dfa-192">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Artikel** och välj sedan relaterad länk om du vill granska det nya artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="30dfa-192">To review the new item card, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
6. <span data-ttu-id="30dfa-193">Öppna det nya artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="30dfa-193">Open the new item card.</span></span>  
7. <span data-ttu-id="30dfa-194">Expandera olika snabbflikar och verifiera att informationen skapas rätt på dem.</span><span class="sxs-lookup"><span data-stu-id="30dfa-194">Expand various FastTabs, and verify that the information was created correctly on them.</span></span>  

## <a name="to-use-a-configuration-template-on-a-record"></a><span data-ttu-id="30dfa-195">Så här använder du en konfigurationsdatamall på en post</span><span class="sxs-lookup"><span data-stu-id="30dfa-195">To use a configuration template on a record</span></span>
<span data-ttu-id="30dfa-196">Du kan koppla en datamall till valfri post, som finns i [!INCLUDE[d365fin](includes/d365fin_md.md)] och använda den här metoden för att ändra en transaktion.</span><span class="sxs-lookup"><span data-stu-id="30dfa-196">You can apply a data template to any record that is in [!INCLUDE[d365fin](includes/d365fin_md.md)] and use this technique to change or modify a record.</span></span> <span data-ttu-id="30dfa-197">Men när du gör det, skriver du över befintliga värden i transaktionen med de i mallen.</span><span class="sxs-lookup"><span data-stu-id="30dfa-197">However, when you do this, you overwrite existing values in the record with those of the template.</span></span> <span data-ttu-id="30dfa-198">Därför bör du vara försiktig när du kopplar en mall till befintliga poster.</span><span class="sxs-lookup"><span data-stu-id="30dfa-198">Consequently, you should be careful when you apply a template to existing records.</span></span>

> [!WARNING]  
>  <span data-ttu-id="30dfa-199">Funktionen **Koppla mall** skriver över befintliga data i en post.</span><span class="sxs-lookup"><span data-stu-id="30dfa-199">The **Apply Template** function overwrites existing data in a record.</span></span> <span data-ttu-id="30dfa-200">Om den här funktionen används i huvuddataflytt, kommer den att skriva över importerade data när du skapar poster.</span><span class="sxs-lookup"><span data-stu-id="30dfa-200">If this function is used in master data migration, it will overwrite the imported data when you create records.</span></span>

<span data-ttu-id="30dfa-201">Följande procedur baseras på ett nytt kundkort.</span><span class="sxs-lookup"><span data-stu-id="30dfa-201">The following procedure is based on a new customer card.</span></span>  

1. <span data-ttu-id="30dfa-202">Skapa en kund.</span><span class="sxs-lookup"><span data-stu-id="30dfa-202">Create a customer.</span></span> <span data-ttu-id="30dfa-203">Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="30dfa-203">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>
2. <span data-ttu-id="30dfa-204">I fönstret **Kundkort** väljer du åtgärden **Tillämpa mall**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-204">In the **Customer Card** window, choose the **Apply Template** action.</span></span>  
3. <span data-ttu-id="30dfa-205">I fönstret**Kundmallar** markerar du en av mallarna och väljer sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="30dfa-205">In the **Customer Templates** window, select one of the templates, and then choose the **OK** button.</span></span>  

<span data-ttu-id="30dfa-206">Standardvärdena från den valda kundmallen förs in på kundkortet.</span><span class="sxs-lookup"><span data-stu-id="30dfa-206">The default values from the chosen customer template are inserted on the customer card.</span></span>

## <a name="see-also"></a><span data-ttu-id="30dfa-207">Se även</span><span class="sxs-lookup"><span data-stu-id="30dfa-207">See Also</span></span>  
[<span data-ttu-id="30dfa-208">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="30dfa-208">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="30dfa-209">Administration</span><span class="sxs-lookup"><span data-stu-id="30dfa-209">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="30dfa-210">Registrera nya kunder</span><span class="sxs-lookup"><span data-stu-id="30dfa-210">Register New Customers</span></span>](sales-how-register-new-customers.md)
