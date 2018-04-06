---
title: "Så här skapar du ingående saldon för journalen | Microsoft Docs"
description: "Business Central innehåller flera batch-jobb som tillhandahålls som hjälp vid överföringen av bakåtkompatibla kontosaldon till ett nykonfigurerat företag. Du kan enkelt överföra data med bokföring i journaler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fc8e8f34220643b7cd3fd357aea3807641cee911
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="745b1-104">Skapa ingående saldon för journalen</span><span class="sxs-lookup"><span data-stu-id="745b1-104">Create Journal Opening Balances</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="745b1-105"> innehåller flera batch-jobb som tillhandahålls som hjälp vid överföringen av bakåtkompatibla kontosaldon till ett nytt konfigurerat företag.</span><span class="sxs-lookup"><span data-stu-id="745b1-105"> includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="745b1-106">Det är enkelt att överföra dessa data för kundjournalen, leverantörsjournalen, artikeljournalen och redovisningsjournalen.</span><span class="sxs-lookup"><span data-stu-id="745b1-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="745b1-107">Det första steget är att skapa ett konfigurationspaket som innehåller inställningstabeller för dessa journaler.</span><span class="sxs-lookup"><span data-stu-id="745b1-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="745b1-108">I följande procedur förutsätts att detta steg har utförts.</span><span class="sxs-lookup"><span data-stu-id="745b1-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="745b1-109">(Mer information finns i [Skapa redovisningsjournaler](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="745b1-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="745b1-110">Denna procedur beskriver de efterföljande stegen, bland annat koppling av paketet som tillhandahålls av en partner.</span><span class="sxs-lookup"><span data-stu-id="745b1-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="745b1-111">Innan du börjar rekommenderar vi att du går till implementerings-rollcentret för RapidStart Services då detta ger rätt sammanhang för ditt konfigurationsarbete.</span><span class="sxs-lookup"><span data-stu-id="745b1-111">Before you start, make sure that you are on the RapidStart Services Implementer Role Center page as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="745b1-112">Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="745b1-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="745b1-113">Så här kan du koppla transaktionerna i en journal till ett nytt företag</span><span class="sxs-lookup"><span data-stu-id="745b1-113">To apply the entries in a journal to a new company</span></span>  
1. <span data-ttu-id="745b1-114">Konfigurera ett nytt företag och koppla ett konfigurationspaket till det.</span><span class="sxs-lookup"><span data-stu-id="745b1-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="745b1-115">Mer information finns i [Konfigurera ett företag med RapidStart-guiden](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="745b1-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="745b1-116">Det nya företaget innehåller inte information om IB till journalen.</span><span class="sxs-lookup"><span data-stu-id="745b1-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="745b1-117">Öppna konfigurationskalkylarket och importera befintliga data om kunder, artiklar, leverantörer och redovisningen.</span><span class="sxs-lookup"><span data-stu-id="745b1-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="745b1-118">Mer information finns också i [Så här migrerar du kunddata](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="745b1-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  
3. <span data-ttu-id="745b1-119">Välj exempelvis åtgärden **Skapa redovisningsjournalrader**.</span><span class="sxs-lookup"><span data-stu-id="745b1-119">Choose, for example, the **Create G/L Journal Lines** action.</span></span>  
4. <span data-ttu-id="745b1-120">Fyll i snabbfliken **Alternativ** och ange filter efter behov.</span><span class="sxs-lookup"><span data-stu-id="745b1-120">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="745b1-121">Skriv till exempel ett namn i fältet **Journalmall**.</span><span class="sxs-lookup"><span data-stu-id="745b1-121">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="745b1-122">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="745b1-122">Choose the **OK** button.</span></span> <span data-ttu-id="745b1-123">Posterna är nu i journalen, men beloppen är tomma.</span><span class="sxs-lookup"><span data-stu-id="745b1-123">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="745b1-124">Exportera journaltabellen till Excel och ange bokförings- och motkontoinformationen manuellt från bakåtkompatibla data.</span><span class="sxs-lookup"><span data-stu-id="745b1-124">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="745b1-125">Importera och koppla tabellinformationen till det nya företaget.</span><span class="sxs-lookup"><span data-stu-id="745b1-125">Import and apply the table information into the new company.</span></span> <span data-ttu-id="745b1-126">Journalraderna är klara för bokföring.</span><span class="sxs-lookup"><span data-stu-id="745b1-126">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="745b1-127">Välj journalradtabellen i konfigurationskalkylarket och välj sedan åtgärden **Databasdata**.</span><span class="sxs-lookup"><span data-stu-id="745b1-127">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="745b1-128">Granska informationen och välj sedan åtgärden **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="745b1-128">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="745b1-129">Upprepa stegen för att importera och bokföra alla ingående saldon.</span><span class="sxs-lookup"><span data-stu-id="745b1-129">Repeat the steps to import and post any other opening balances.</span></span>  

## <a name="see-also"></a><span data-ttu-id="745b1-130">Se även</span><span class="sxs-lookup"><span data-stu-id="745b1-130">See Also</span></span>  
[<span data-ttu-id="745b1-131">Koppla konfigurationen till nya företag</span><span class="sxs-lookup"><span data-stu-id="745b1-131">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="745b1-132">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="745b1-132">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="745b1-133">Administration</span><span class="sxs-lookup"><span data-stu-id="745b1-133">Administration</span></span>](admin-setup-and-administration.md)

