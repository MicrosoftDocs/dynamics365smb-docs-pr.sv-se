---
title: Så här skapar du anpassade konfigurationspaket för företag | Microsoft Docs
description: När verksamheten växer, kommer du antagligen att behöva förlita dig på en uppsättning företagstyper som du använder med de flesta av dina kunder. Du kan rationalisera implementeringsprocessen genom att omvandla dessa typer till företagskonfigurationspaket som är tillgängliga för återanvändning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 99fad48961dc201a25af061cf982a1c65d9446bd
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878871"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="81c73-104">Så här skapar du anpassade konfigurationspaket för företag</span><span class="sxs-lookup"><span data-stu-id="81c73-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="81c73-105">När verksamheten växer, kommer du antagligen att behöva förlita dig på en uppsättning företagstyper som du använder med de flesta av dina kunder.</span><span class="sxs-lookup"><span data-stu-id="81c73-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="81c73-106">Du kan rationalisera implementeringsprocessen genom att omvandla dessa typer till företagskonfigurationspaket som är tillgängliga för återanvändning.</span><span class="sxs-lookup"><span data-stu-id="81c73-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="81c73-107">I allmänhet skapar du ett konfigurationspaket per funktionellt område, till exempel ett paket för din produktionsfunktion.</span><span class="sxs-lookup"><span data-stu-id="81c73-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="81c73-108">Då kan du koppla och skapa nya områden i företaget efter behov</span><span class="sxs-lookup"><span data-stu-id="81c73-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="81c73-109">En annan metod är att skapa ett paket som innehåller tabellerna för definition av inställningen. Exempel:</span><span class="sxs-lookup"><span data-stu-id="81c73-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="81c73-110">Anläggningstillgånginställningar</span><span class="sxs-lookup"><span data-stu-id="81c73-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="81c73-111">Redovisningsinställningar</span><span class="sxs-lookup"><span data-stu-id="81c73-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="81c73-112">Lagerinställningar</span><span class="sxs-lookup"><span data-stu-id="81c73-112">Inventory Setup</span></span>  
-   <span data-ttu-id="81c73-113">Produktionsinställningar</span><span class="sxs-lookup"><span data-stu-id="81c73-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="81c73-114">Inköpsinställningar</span><span class="sxs-lookup"><span data-stu-id="81c73-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="81c73-115">Marknadsföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="81c73-115">Marketing Setup</span></span>  
-   <span data-ttu-id="81c73-116">Serviceinställningar</span><span class="sxs-lookup"><span data-stu-id="81c73-116">Service Setup</span></span>  
-   <span data-ttu-id="81c73-117">Försäljningsinställningar</span><span class="sxs-lookup"><span data-stu-id="81c73-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="81c73-118">Lagerstyrningsinställningar</span><span class="sxs-lookup"><span data-stu-id="81c73-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="81c73-119">Bokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="81c73-119">General Posting Setup</span></span>  
-   <span data-ttu-id="81c73-120">Bokföringsinställningar för moms</span><span class="sxs-lookup"><span data-stu-id="81c73-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="81c73-121">Lagerbokföringsinställning</span><span class="sxs-lookup"><span data-stu-id="81c73-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="81c73-122">För att se en komplett lista över inställningstabeller, välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Manuell inställning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="81c73-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="81c73-123">Så här skapar du ett anpassat konfigurationspaket för företag</span><span class="sxs-lookup"><span data-stu-id="81c73-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="81c73-124">Skapa ett nytt företag.</span><span class="sxs-lookup"><span data-stu-id="81c73-124">Create a new company.</span></span> <span data-ttu-id="81c73-125">Mer information finns i [Skapa nya företag i Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="81c73-125">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="81c73-126">Ställ in det nya företaget efter behov.</span><span class="sxs-lookup"><span data-stu-id="81c73-126">Set up the new company in the way you need.</span></span> <span data-ttu-id="81c73-127">Fyll i alla inställningstabeller som behövs.</span><span class="sxs-lookup"><span data-stu-id="81c73-127">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="81c73-128">Öppna det nya företaget.</span><span class="sxs-lookup"><span data-stu-id="81c73-128">Open the new company.</span></span>
5. <span data-ttu-id="81c73-129">Öppna sidan **Konfigurationsformulär**.</span><span class="sxs-lookup"><span data-stu-id="81c73-129">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="81c73-130">Lägg till tabellerna som du vill överföra till ett annat företag i kalkylarket.</span><span class="sxs-lookup"><span data-stu-id="81c73-130">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="81c73-131">Tilldela kalkylarksraderna till paketet.</span><span class="sxs-lookup"><span data-stu-id="81c73-131">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="81c73-132">Skapa ett frågeformulär för de mest använda inställningstabellerna.</span><span class="sxs-lookup"><span data-stu-id="81c73-132">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="81c73-133">Skapa konfigurationsmallar för att göra det lättare att skapa huvuddata, som för kunder eller artiklar.</span><span class="sxs-lookup"><span data-stu-id="81c73-133">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="81c73-134">Exportera ditt paket som en rapidstart-fil.</span><span class="sxs-lookup"><span data-stu-id="81c73-134">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="81c73-135">Se även</span><span class="sxs-lookup"><span data-stu-id="81c73-135">See Also</span></span>  
[<span data-ttu-id="81c73-136">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="81c73-136">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="81c73-137">Administration</span><span class="sxs-lookup"><span data-stu-id="81c73-137">Administration</span></span>](admin-setup-and-administration.md)
