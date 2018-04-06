---
title: "Så här skapar du anpassade konfigurationspaket för företag | Microsoft Docs"
description: "När verksamheten växer, kommer du antagligen att behöva förlita dig på en uppsättning företagstyper som du använder med de flesta av dina kunder. Du kan rationalisera implementeringsprocessen genom att omvandla dessa typer till företagskonfigurationspaket som är tillgängliga för återanvändning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7feaa0e41cf5800ffd51d5807a90f6929492804e
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="47dfe-104">Så här skapar du anpassade konfigurationspaket för företag</span><span class="sxs-lookup"><span data-stu-id="47dfe-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="47dfe-105">När verksamheten växer, kommer du antagligen att behöva förlita dig på en uppsättning företagstyper som du använder med de flesta av dina kunder.</span><span class="sxs-lookup"><span data-stu-id="47dfe-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="47dfe-106">Du kan rationalisera implementeringsprocessen genom att omvandla dessa typer till företagskonfigurationspaket som är tillgängliga för återanvändning.</span><span class="sxs-lookup"><span data-stu-id="47dfe-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="47dfe-107">I allmänhet skapar du ett konfigurationspaket per funktionellt område, till exempel ett paket för din produktionsfunktion.</span><span class="sxs-lookup"><span data-stu-id="47dfe-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="47dfe-108">Då kan du koppla och skapa nya områden i företaget efter behov</span><span class="sxs-lookup"><span data-stu-id="47dfe-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="47dfe-109">En annan metod är att skapa ett paket som innehåller tabellerna för definition av inställningen. Exempel:</span><span class="sxs-lookup"><span data-stu-id="47dfe-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="47dfe-110">Anläggningstillgånginställningar</span><span class="sxs-lookup"><span data-stu-id="47dfe-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="47dfe-111">Redovisningsinställningar</span><span class="sxs-lookup"><span data-stu-id="47dfe-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="47dfe-112">Lagerinställningar</span><span class="sxs-lookup"><span data-stu-id="47dfe-112">Inventory Setup</span></span>  
-   <span data-ttu-id="47dfe-113">Produktionsinställningar</span><span class="sxs-lookup"><span data-stu-id="47dfe-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="47dfe-114">Inköpsinställningar</span><span class="sxs-lookup"><span data-stu-id="47dfe-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="47dfe-115">Marknadsföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="47dfe-115">Marketing Setup</span></span>  
-   <span data-ttu-id="47dfe-116">Serviceinställningar</span><span class="sxs-lookup"><span data-stu-id="47dfe-116">Service Setup</span></span>  
-   <span data-ttu-id="47dfe-117">Försäljningsinställningar</span><span class="sxs-lookup"><span data-stu-id="47dfe-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="47dfe-118">Lagerstyrningsinställningar</span><span class="sxs-lookup"><span data-stu-id="47dfe-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="47dfe-119">Bokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="47dfe-119">General Posting Setup</span></span>  
-   <span data-ttu-id="47dfe-120">Bokföringsinställningar för moms</span><span class="sxs-lookup"><span data-stu-id="47dfe-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="47dfe-121">Lagerbokföringsinställning</span><span class="sxs-lookup"><span data-stu-id="47dfe-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="47dfe-122">För att visa en fullständig list över inställningstabeller väljer du ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), öppnar **Inställningar** och väljer sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="47dfe-122">To see a complete list of setup tables, Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="47dfe-123">Så här skapar du ett anpassat konfigurationspaket för företag</span><span class="sxs-lookup"><span data-stu-id="47dfe-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="47dfe-124">Skapa en ny [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="47dfe-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="47dfe-125">***INTE MÖJLIGT Länk till hjälp för ”Skapa en ny klientorganisation***.</span><span class="sxs-lookup"><span data-stu-id="47dfe-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="47dfe-126">Skapa ett nytt företag bransch- eller lösningsmallen.</span><span class="sxs-lookup"><span data-stu-id="47dfe-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="47dfe-127">För mer information, se [Skapa ett nytt företag](admin-how-to-create-a-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="47dfe-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="47dfe-128">Ställ in det nya företaget efter behov.</span><span class="sxs-lookup"><span data-stu-id="47dfe-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="47dfe-129">Fyll i alla inställningstabeller som behövs.</span><span class="sxs-lookup"><span data-stu-id="47dfe-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="47dfe-130">Öppna det nya företaget.</span><span class="sxs-lookup"><span data-stu-id="47dfe-130">Open the new company.</span></span>
5. <span data-ttu-id="47dfe-131">Öppna fönstret **Konfigurationskalkylark**.</span><span class="sxs-lookup"><span data-stu-id="47dfe-131">Open the **Configuration Worksheet** window.</span></span>  
6.  <span data-ttu-id="47dfe-132">Lägg till tabellerna som du vill överföra till ett annat företag i kalkylarket.</span><span class="sxs-lookup"><span data-stu-id="47dfe-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="47dfe-133">Tilldela kalkylarksraderna till paketet.</span><span class="sxs-lookup"><span data-stu-id="47dfe-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="47dfe-134">Skapa ett frågeformulär för de mest använda inställningstabellerna.</span><span class="sxs-lookup"><span data-stu-id="47dfe-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="47dfe-135">Skapa konfigurationsmallar för att göra det lättare att skapa huvuddata, som för kunder eller artiklar.</span><span class="sxs-lookup"><span data-stu-id="47dfe-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="47dfe-136">Exportera ditt paket som en rapidstart-fil.</span><span class="sxs-lookup"><span data-stu-id="47dfe-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="47dfe-137">Se även</span><span class="sxs-lookup"><span data-stu-id="47dfe-137">See Also</span></span>  
[<span data-ttu-id="47dfe-138">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="47dfe-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="47dfe-139">Administration</span><span class="sxs-lookup"><span data-stu-id="47dfe-139">Administration</span></span>](admin-setup-and-administration.md)

