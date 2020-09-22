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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 511281b5f4d8c7437324ed123a5a5a62bd4cc51d
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783663"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="8d593-104">Så här skapar du anpassade konfigurationspaket för företag</span><span class="sxs-lookup"><span data-stu-id="8d593-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="8d593-105">När verksamheten växer, kommer du antagligen att behöva förlita dig på en uppsättning företagstyper som du använder med de flesta av dina kunder.</span><span class="sxs-lookup"><span data-stu-id="8d593-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="8d593-106">Du kan rationalisera implementeringsprocessen genom att omvandla dessa typer till företagskonfigurationspaket som är tillgängliga för återanvändning.</span><span class="sxs-lookup"><span data-stu-id="8d593-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="8d593-107">I allmänhet skapar du ett konfigurationspaket per funktionellt område, till exempel ett paket för din produktionsfunktion.</span><span class="sxs-lookup"><span data-stu-id="8d593-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="8d593-108">Då kan du koppla och skapa nya områden i företaget efter behov</span><span class="sxs-lookup"><span data-stu-id="8d593-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="8d593-109">En annan metod är att skapa ett paket som innehåller tabellerna för definition av inställningen. Exempel:</span><span class="sxs-lookup"><span data-stu-id="8d593-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="8d593-110">Anläggningstillgånginställningar</span><span class="sxs-lookup"><span data-stu-id="8d593-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="8d593-111">Redovisningsinställningar</span><span class="sxs-lookup"><span data-stu-id="8d593-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="8d593-112">Lagerinställningar</span><span class="sxs-lookup"><span data-stu-id="8d593-112">Inventory Setup</span></span>  
-   <span data-ttu-id="8d593-113">Produktionsinställningar</span><span class="sxs-lookup"><span data-stu-id="8d593-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="8d593-114">Inköpsinställningar</span><span class="sxs-lookup"><span data-stu-id="8d593-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="8d593-115">Marknadsföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="8d593-115">Marketing Setup</span></span>  
-   <span data-ttu-id="8d593-116">Serviceinställningar</span><span class="sxs-lookup"><span data-stu-id="8d593-116">Service Setup</span></span>  
-   <span data-ttu-id="8d593-117">Försäljningsinställningar</span><span class="sxs-lookup"><span data-stu-id="8d593-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="8d593-118">Lagerstyrningsinställningar</span><span class="sxs-lookup"><span data-stu-id="8d593-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="8d593-119">Bokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="8d593-119">General Posting Setup</span></span>  
-   <span data-ttu-id="8d593-120">Bokföringsinställningar för moms</span><span class="sxs-lookup"><span data-stu-id="8d593-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="8d593-121">Lagerbokföringsinställning</span><span class="sxs-lookup"><span data-stu-id="8d593-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="8d593-122">För att se en komplett lista över inställningstabeller, välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Manuell inställning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8d593-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="8d593-123">Var försiktig om du väljer tabeller eller fält med samma tidsdefinierade namn men som skiljer sig åt med specialtecken, till exempel %, &, <, >, (, och ).</span><span class="sxs-lookup"><span data-stu-id="8d593-123">Use caution if you choose tables or fields that have the same temporal name but are differentiated by special characters, such as %, &, <, >, (, and ).</span></span> <span data-ttu-id="8d593-124">Tabellen "XYZ" kan t.ex. innehålla fälten "Fält 1" och "Fält 1 %".</span><span class="sxs-lookup"><span data-stu-id="8d593-124">For example, table "XYZ" might contain the "Field 1" and "Field 1%" fields.</span></span>
>
> <span data-ttu-id="8d593-125">XML-processorn accepterar endast vissa specialtecken och tar bort de som inte accepteras.</span><span class="sxs-lookup"><span data-stu-id="8d593-125">The XML processor accepts only some special characters, and will remove those it does not.</span></span> <span data-ttu-id="8d593-126">Om du tar bort ett specialtecken, t.ex. %-symbolen i "Fält 1 %", resulterar det i två eller flera tabeller eller fält med samma namn och ett fel uppstår när du exporterar eller importerar ett konfigurationspaket.</span><span class="sxs-lookup"><span data-stu-id="8d593-126">If removing a special character, such as the % sign in "Field 1%," results in two or more tables or fields with the same name an error will occur when you export or import a configuration package.</span></span>

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="8d593-127">Så här skapar du ett anpassat konfigurationspaket för företag</span><span class="sxs-lookup"><span data-stu-id="8d593-127">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="8d593-128">Skapa ett nytt företag.</span><span class="sxs-lookup"><span data-stu-id="8d593-128">Create a new company.</span></span> <span data-ttu-id="8d593-129">Mer information finns i [Skapa nya företag i Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="8d593-129">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="8d593-130">Ställ in det nya företaget efter behov.</span><span class="sxs-lookup"><span data-stu-id="8d593-130">Set up the new company in the way you need.</span></span> <span data-ttu-id="8d593-131">Fyll i alla inställningstabeller som behövs.</span><span class="sxs-lookup"><span data-stu-id="8d593-131">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="8d593-132">Öppna det nya företaget.</span><span class="sxs-lookup"><span data-stu-id="8d593-132">Open the new company.</span></span>
5. <span data-ttu-id="8d593-133">Öppna sidan **Konfigurationsformulär**.</span><span class="sxs-lookup"><span data-stu-id="8d593-133">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="8d593-134">Lägg till tabellerna som du vill överföra till ett annat företag i kalkylarket.</span><span class="sxs-lookup"><span data-stu-id="8d593-134">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="8d593-135">Tilldela kalkylarksraderna till paketet.</span><span class="sxs-lookup"><span data-stu-id="8d593-135">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="8d593-136">Skapa ett frågeformulär för de mest använda inställningstabellerna.</span><span class="sxs-lookup"><span data-stu-id="8d593-136">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="8d593-137">Skapa konfigurationsmallar för att göra det lättare att skapa huvuddata, som för kunder eller artiklar.</span><span class="sxs-lookup"><span data-stu-id="8d593-137">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="8d593-138">Exportera ditt paket som en rapidstart-fil.</span><span class="sxs-lookup"><span data-stu-id="8d593-138">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8d593-139">Se även</span><span class="sxs-lookup"><span data-stu-id="8d593-139">See Also</span></span>  
[<span data-ttu-id="8d593-140">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="8d593-140">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="8d593-141">Administration</span><span class="sxs-lookup"><span data-stu-id="8d593-141">Administration</span></span>](admin-setup-and-administration.md)
