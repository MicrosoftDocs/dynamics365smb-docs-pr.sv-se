---
title: Rapportval i Business Central
description: Mer information om hur du ställer in de rapporter som du använder för att skriva ut olika typer av dokument i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 01/18/2021
ms.author: edupont
ms.openlocfilehash: d30baa44894658c03c3deffdf24a7923293b88fd
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024643"
---
# <a name="report-selection-in-business-central"></a><span data-ttu-id="880ab-103">Rapportval i Business Central</span><span class="sxs-lookup"><span data-stu-id="880ab-103">Report Selection in Business Central</span></span>

<span data-ttu-id="880ab-104">Du kan konfigurera standardrapporter som ska användas för att skriva ut de olika dokumenten för försäljning och inköp, exempelvis order, offerter, fakturor och kreditnotor.</span><span class="sxs-lookup"><span data-stu-id="880ab-104">You can set up default reports that will be used to print the various documents for sales and purchases, such as orders, quotes, invoices, and credit memos.</span></span> <span data-ttu-id="880ab-105">Om du t. ex. har en särskild layout för försäljningsfakturor kan du ange rapporten på sidan **Rapporturval - Försäljning** så att den används för att skicka eller skriva ut försäljningsfakturor.</span><span class="sxs-lookup"><span data-stu-id="880ab-105">For example, if you have a specific layout for sales invoices, you can specify that report in the **Report Selections - Sales** page so that it will be used to send or print sales invoices.</span></span>  

<span data-ttu-id="880ab-106">Sidorna för **rapporturval** anger vilken rapport som ska skrivas ut i olika situationer.</span><span class="sxs-lookup"><span data-stu-id="880ab-106">The **Report Selections** pages specify which report will be printed in different situations.</span></span> <span data-ttu-id="880ab-107">[!INCLUDE [prod_short](includes/prod_short.md)] innehåller standardkonfigurationer, men naturligtvis kan du ändra dessa standardvärden.</span><span class="sxs-lookup"><span data-stu-id="880ab-107">[!INCLUDE [prod_short](includes/prod_short.md)] includes default configurations, but of course you can change these defaults.</span></span> <span data-ttu-id="880ab-108">Du kan också lägga till rapporter på sidorna för **Rapporturval** om du exempelvis vill skriva ut mer än en rapport per dokumenttyp.</span><span class="sxs-lookup"><span data-stu-id="880ab-108">You can also add reports to the **Report Selection** pages if you want to print more than one report per document type, for example.</span></span>  

## <a name="available-report-selections"></a><span data-ttu-id="880ab-109">Tillgängliga rapporturval</span><span class="sxs-lookup"><span data-stu-id="880ab-109">Available report selections</span></span>

<span data-ttu-id="880ab-110">[!INCLUDE [prod_short](includes/prod_short.md)] innehåller olika **Rapporturval**-sidor för olika områden.</span><span class="sxs-lookup"><span data-stu-id="880ab-110">[!INCLUDE [prod_short](includes/prod_short.md)] includes different **Report Selection** pages for different areas.</span></span> <span data-ttu-id="880ab-111">I följande tabeller beskrivs var du kan hitta information om de olika sidorna.</span><span class="sxs-lookup"><span data-stu-id="880ab-111">The following tables describes where you can find information about the different pages.</span></span>  

|<span data-ttu-id="880ab-112">Område eller uppgift</span><span class="sxs-lookup"><span data-stu-id="880ab-112">Area or task</span></span>  |<span data-ttu-id="880ab-113">Läs mer</span><span class="sxs-lookup"><span data-stu-id="880ab-113">Learn more</span></span>|
|--------------|----------|
|<span data-ttu-id="880ab-114">Exempel på hur rapporturval fungerar (försäljning)</span><span class="sxs-lookup"><span data-stu-id="880ab-114">Example of how report selection works (Sales)</span></span>|[<span data-ttu-id="880ab-115">Rapportval för försäljningsdokument</span><span class="sxs-lookup"><span data-stu-id="880ab-115">Report selection for sales documents</span></span>](#example-report-selection-for-sales-documents)|
|<span data-ttu-id="880ab-116">Standardlayout för e-post med försäljnings- och inköpsdokument</span><span class="sxs-lookup"><span data-stu-id="880ab-116">Default layout for emails with sales and purchase documents</span></span>  |[<span data-ttu-id="880ab-117">Konfigurera återanvändbara e-posttexter och layouter för försäljnings- och inköpsdokument</span><span class="sxs-lookup"><span data-stu-id="880ab-117">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|<span data-ttu-id="880ab-118">Definiera kontrollayouter</span><span class="sxs-lookup"><span data-stu-id="880ab-118">Define check layouts</span></span>     |[<span data-ttu-id="880ab-119">Välj en checklayout</span><span class="sxs-lookup"><span data-stu-id="880ab-119">Select a Check Layout</span></span>](finance-how-define-check-layouts.md) |
|<span data-ttu-id="880ab-120">Definiera rapporter för momsrapportering (Tyskland)</span><span class="sxs-lookup"><span data-stu-id="880ab-120">Define reports for VAT reporting (Germany)</span></span>|[<span data-ttu-id="880ab-121">Ställ in rapporter för moms och Intrastat</span><span class="sxs-lookup"><span data-stu-id="880ab-121">Set Up Reports for VAT and Intrastat</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> <span data-ttu-id="880ab-122">Ditt [!INCLUDE [prod_short](includes/prod_short.md)] kan lägga till ytterligare sidor för **Rapporturval**, beroende exempelvis på plats och bransch.</span><span class="sxs-lookup"><span data-stu-id="880ab-122">Your [!INCLUDE [prod_short](includes/prod_short.md)] can include additional **Report Selection** pages, depending on your location and industry, for example.</span></span> <span data-ttu-id="880ab-123">Du kan alltid kontrollera inställningarna genom att välja ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Rapportera val** och sedan välja önskad länk.</span><span class="sxs-lookup"><span data-stu-id="880ab-123">You can always check your setup by choosing the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, entering **Report Selections**, and then choose the relevant link.</span></span>

<span data-ttu-id="880ab-124">Standardversionen av [!INCLUDE [prod_short](includes/prod_short.md)] innehåller följande sidor om **Rapportavsnitt**:</span><span class="sxs-lookup"><span data-stu-id="880ab-124">The default version of [!INCLUDE [prod_short](includes/prod_short.md)] includes the following **Report Section** pages:</span></span>

* <span data-ttu-id="880ab-125">**Rapportval - Försäljning**</span><span class="sxs-lookup"><span data-stu-id="880ab-125">**Report Selection - Sales**</span></span>  
* <span data-ttu-id="880ab-126">**Rapportval - Inköp**</span><span class="sxs-lookup"><span data-stu-id="880ab-126">**Report Selection - Purchase**</span></span>  
* <span data-ttu-id="880ab-127">**Rapportval - Lager**</span><span class="sxs-lookup"><span data-stu-id="880ab-127">**Report Selection - Inventory**</span></span>  
* <span data-ttu-id="880ab-128">**Rapportval - Kassaflöde**</span><span class="sxs-lookup"><span data-stu-id="880ab-128">**Report Selection - Cash Flow**</span></span>  
* <span data-ttu-id="880ab-129">**Rapportval - Distributionslager**</span><span class="sxs-lookup"><span data-stu-id="880ab-129">**Report Selection - Warehouse**</span></span>  
* <span data-ttu-id="880ab-130">**Rapportval - Bankkonto**</span><span class="sxs-lookup"><span data-stu-id="880ab-130">**Report Selection - Bank Account**</span></span>  
* <span data-ttu-id="880ab-131">**Rapportval - Påminnelse/ränta**</span><span class="sxs-lookup"><span data-stu-id="880ab-131">**Report Selections Reminder/Finance Charge**</span></span>  

## <a name="example-report-selection-for-sales-documents"></a><span data-ttu-id="880ab-132">Exempel: Rapportval för försäljningsdokument</span><span class="sxs-lookup"><span data-stu-id="880ab-132">Example: Report selection for sales documents</span></span>

<span data-ttu-id="880ab-133">Sidan **Rapportval - Försäljning** definierar de standardrapporter som ska användas i olika scenarier för varje relaterad dokumenttyp.</span><span class="sxs-lookup"><span data-stu-id="880ab-133">The **Report Selection - Sales** page defines the default reports to use in different scenarios for each related document type.</span></span> <span data-ttu-id="880ab-134">Välj en dokumenttyp i fältet **Användning** och lägg sedan till eller granska rapportvalet.</span><span class="sxs-lookup"><span data-stu-id="880ab-134">Choose a document type in the **Usage** field, and then add or review the report selection.</span></span> <span data-ttu-id="880ab-135">Du kan konfigurera mer än en rapport och i vilken ordning rapporterna ska skickas eller skrivas ut.</span><span class="sxs-lookup"><span data-stu-id="880ab-135">You can set up more than one report and the order of sequence that the reports must be sent or printed in.</span></span>  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="880ab-136">Vissa typer av dokument kan skickas som e-postbilagor, andra inte.</span><span class="sxs-lookup"><span data-stu-id="880ab-136">Some types of document can be sent as email attachments, and others cannot.</span></span> <span data-ttu-id="880ab-137">Varje sida för **Rapporturval** visar ytterligare fält om typen stöder e-post direkt.</span><span class="sxs-lookup"><span data-stu-id="880ab-137">Each **Report Selection** page shows additional fields if the type support email out of the box.</span></span>  

<span data-ttu-id="880ab-138">På sidorna **Rapporturval - Försäljning** och **Rapporturval - Inköp** hjälper följande fält dig att konfigurera e-post:</span><span class="sxs-lookup"><span data-stu-id="880ab-138">For example, in the **Report Selection - Sales** and **Report Selection - Purchase** pages, the following fields help you set up emailing:</span></span>

|<span data-ttu-id="880ab-139">Fältnamn</span><span class="sxs-lookup"><span data-stu-id="880ab-139">Field name</span></span> |<span data-ttu-id="880ab-140">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="880ab-140">Description</span></span>  |
|-----------|-------------|
|<span data-ttu-id="880ab-141">**Använd till brödtext i e-post**</span><span class="sxs-lookup"><span data-stu-id="880ab-141">**Use for Email Body**</span></span>| <span data-ttu-id="880ab-142">Anger att sammanfattad information, t.ex. fakturanummer, förfallodatum och betalningstjänstlänken, kommer att infogas i brödtexten i det e-postmeddelande du skickar.</span><span class="sxs-lookup"><span data-stu-id="880ab-142">Specifies that summarized information, such as invoice number, due date, and payment service link, will be inserted in the body of the email that you send.</span></span>        |
|<span data-ttu-id="880ab-143">**Använd till e-postbilaga**</span><span class="sxs-lookup"><span data-stu-id="880ab-143">**Use for Email Attachment**</span></span>| <span data-ttu-id="880ab-144">Anger att det relaterade dokumentet kommer att bifogas i e-postmeddelandet.</span><span class="sxs-lookup"><span data-stu-id="880ab-144">Specifies that the related document will be attached to the email.</span></span>|
|<span data-ttu-id="880ab-145">**Beskrivning av layouten på brödtext i e-post**</span><span class="sxs-lookup"><span data-stu-id="880ab-145">**Email Body Layout Description**</span></span>|<span data-ttu-id="880ab-146">Anger den layout för e-postbrödtext som används, vanligtvis en anpassad rapportlayout.</span><span class="sxs-lookup"><span data-stu-id="880ab-146">Specifies the email body layout that is used, typically a custom report layout.</span></span> |

## <a name="see-also"></a><span data-ttu-id="880ab-147">Se även</span><span class="sxs-lookup"><span data-stu-id="880ab-147">See also</span></span>

[<span data-ttu-id="880ab-148">Konfigurera återanvändbara e-posttexter och layouter för försäljnings- och inköpsdokument</span><span class="sxs-lookup"><span data-stu-id="880ab-148">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[<span data-ttu-id="880ab-149">Välj en kontrollayout</span><span class="sxs-lookup"><span data-stu-id="880ab-149">Select a Check Layout</span></span>](finance-how-define-check-layouts.md)  
[<span data-ttu-id="880ab-150">Ställ in rapporter för moms och Intrastat (Tyskland)</span><span class="sxs-lookup"><span data-stu-id="880ab-150">Set Up Reports for VAT and Intrastat (Germany)</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[<span data-ttu-id="880ab-151">Hantera rapport- och dokumentlayouter</span><span class="sxs-lookup"><span data-stu-id="880ab-151">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
[<span data-ttu-id="880ab-152">Definiera dokumentlayout för kunder och leverantörer</span><span class="sxs-lookup"><span data-stu-id="880ab-152">Define Document Layouts for Customers and Vendors</span></span>](ui-define-customer-vendor-document-layouts.md)  
[<span data-ttu-id="880ab-153">Ställa in skrivare</span><span class="sxs-lookup"><span data-stu-id="880ab-153">Set Up Printers</span></span>](ui-specify-printer-selection-reports.md)  
