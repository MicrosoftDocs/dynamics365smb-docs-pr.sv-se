---
title: "Så här importerar och exporterar du data i SIE-format (Standard Import Export)"
description: Du kan importera och exportera redovisningsdata i SIE-format (Standard Import Export).
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8bfe55ccdb495f72d14c2bff2fad8b69f8b51c63
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="import-and-export-data-in-standard-import-export-format"></a><span data-ttu-id="b861a-103">Importera och exportera data i SIE-format (Standard Import Export)</span><span class="sxs-lookup"><span data-stu-id="b861a-103">Import and Export Data in Standard Import Export Format</span></span>
<span data-ttu-id="b861a-104">Du kan importera och exportera redovisningsdata i SIE-format (Standard Import Export).</span><span class="sxs-lookup"><span data-stu-id="b861a-104">You can import and export general ledger data according to the standard import export (SIE) format.</span></span> <span data-ttu-id="b861a-105">Genom att ange SIE-dimensioner och -filtyper kan du ange vilken detaljnivå import- eller exporttransaktionerna ska ha.</span><span class="sxs-lookup"><span data-stu-id="b861a-105">By specifying SIE dimensions and file types, you can specify the level of detail covered by import or export transactions.</span></span> <span data-ttu-id="b861a-106">Mer information finns i [SIE-grupp](https://go.microsoft.com/fwlink/?LinkID=164870&clcid=0x41d).</span><span class="sxs-lookup"><span data-stu-id="b861a-106">For more information, see [Standard Import Export Group](https://go.microsoft.com/fwlink/?LinkID=164870&clcid=0x41d).</span></span>  

## <a name="to-import-data-in-sie-format"></a><span data-ttu-id="b861a-107">Så här importerar du data i SIE-format</span><span class="sxs-lookup"><span data-stu-id="b861a-107">To import data in SIE format</span></span>  

1.  <span data-ttu-id="b861a-108">Välj ikonen ![Söka efter sida eller rapport](../../media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **SIE-import** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b861a-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **SIE Import**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b861a-109">Fyll i fälten enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="b861a-109">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="b861a-110">Fält</span><span class="sxs-lookup"><span data-stu-id="b861a-110">Field</span></span>|<span data-ttu-id="b861a-111">Description</span><span class="sxs-lookup"><span data-stu-id="b861a-111">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="b861a-112">**Redovisningsjournalmall**</span><span class="sxs-lookup"><span data-stu-id="b861a-112">**Gen. Journal Template**</span></span>|<span data-ttu-id="b861a-113">Välj en redovisningsjournalmall.</span><span class="sxs-lookup"><span data-stu-id="b861a-113">Select a general journal template.</span></span>|  
    |<span data-ttu-id="b861a-114">**Redovisningsjournal**</span><span class="sxs-lookup"><span data-stu-id="b861a-114">**Gen. Journal Batch**</span></span>|<span data-ttu-id="b861a-115">Välj en redovisningsjournal.</span><span class="sxs-lookup"><span data-stu-id="b861a-115">Select a general journal batch.</span></span>|  
    |<span data-ttu-id="b861a-116">**Dimensioner**</span><span class="sxs-lookup"><span data-stu-id="b861a-116">**Dimensions**</span></span>|<span data-ttu-id="b861a-117">Markera SIE-dimensionerna du vill importera.</span><span class="sxs-lookup"><span data-stu-id="b861a-117">Select the SIE dimensions to import.</span></span>|  
    |<span data-ttu-id="b861a-118">**Infoga redovisningskonto**</span><span class="sxs-lookup"><span data-stu-id="b861a-118">**Insert G/L Account**</span></span>|<span data-ttu-id="b861a-119">Välj det här alternativet om redovisningskontot i importfilen saknas i kontoplanen och måste skapas under importprocessen.</span><span class="sxs-lookup"><span data-stu-id="b861a-119">Select if the general ledger account in the import file is missing in the chart of accounts and needs to be set up during the import process.</span></span>|  
    |<span data-ttu-id="b861a-120">**Använd nummerserie för dok.nr**</span><span class="sxs-lookup"><span data-stu-id="b861a-120">**Use Number Series for Doc. No.**</span></span>|<span data-ttu-id="b861a-121">Välj det här alternativet om det inte finns något dokumentnummer i importfilen.</span><span class="sxs-lookup"><span data-stu-id="b861a-121">Select if a document number is not provided in the import file.</span></span>|  

3. <span data-ttu-id="b861a-122">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b861a-122">Choose the **OK** button.</span></span>
4. <span data-ttu-id="b861a-123">Välj en fil att importera.</span><span class="sxs-lookup"><span data-stu-id="b861a-123">Select the file to import.</span></span>  

## <a name="to-export-data-in-sie-format"></a><span data-ttu-id="b861a-124">Så här exporterar du data i SIE-format</span><span class="sxs-lookup"><span data-stu-id="b861a-124">To export data in SIE format</span></span>  

1.  <span data-ttu-id="b861a-125">Välj ikonen ![Söka efter sida eller rapport](../../media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **SIE-import** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b861a-125">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **SIE Export**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b861a-126">Välj lämpliga filter på snabbfliken **Redovisningskonto**.</span><span class="sxs-lookup"><span data-stu-id="b861a-126">On the **G/L Account** FastTab, choose the appropriate filters.</span></span>  
3.  <span data-ttu-id="b861a-127">Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Alternativ**.</span><span class="sxs-lookup"><span data-stu-id="b861a-127">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="b861a-128">Fält</span><span class="sxs-lookup"><span data-stu-id="b861a-128">Field</span></span>|<span data-ttu-id="b861a-129">Description</span><span class="sxs-lookup"><span data-stu-id="b861a-129">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="b861a-130">**Filtyp**</span><span class="sxs-lookup"><span data-stu-id="b861a-130">**File Type**</span></span>|<span data-ttu-id="b861a-131">Välj typen av fil du vill skapa.</span><span class="sxs-lookup"><span data-stu-id="b861a-131">Select the type of file to be created.</span></span> <span data-ttu-id="b861a-132">Välj något av följande alternativ:</span><span class="sxs-lookup"><span data-stu-id="b861a-132">Select from one of the following options:</span></span><br /><br /> <span data-ttu-id="b861a-133">-   **År - Slutsaldon** - Innehåller årligt utgående saldo för alla konton i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="b861a-133">-   **Year - End Balances** - Contains the annual account balance carried forward for all accounts in the chart of accounts.</span></span><br /><span data-ttu-id="b861a-134">-   **Periodiska saldon** - Innehåller årligt utgående saldo och månatliga förändringar för alla konton i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="b861a-134">-   **Periodic Balances** - Contains the annual account balance carried forward and monthly changes for all accounts in the chart of accounts.</span></span><br /><span data-ttu-id="b861a-135">-   **Objektsaldon** - Innehåller årligt utgående kontosaldo, månatliga förändringar och saldon på objektnivån, till exempel kostnadsenheter och projekt, för alla konton i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="b861a-135">-   **Object Balances** - Contains the annual account balance carried forward, monthly changes, and balances on the object level, such as cost units and projects, for all accounts in the chart of accounts.</span></span><br /><span data-ttu-id="b861a-136">-   **Transaktioner** - Innehåller alla redovisningstransaktioner för perioden.</span><span class="sxs-lookup"><span data-stu-id="b861a-136">-   **Transactions** - Contains all the general ledger entries for the period.</span></span>|  
    |<span data-ttu-id="b861a-137">**Kontakt**</span><span class="sxs-lookup"><span data-stu-id="b861a-137">**Contact**</span></span>|<span data-ttu-id="b861a-138">Ange kontaktperson.</span><span class="sxs-lookup"><span data-stu-id="b861a-138">Enter the contact person.</span></span> <span data-ttu-id="b861a-139">Fältet är ett tillval.</span><span class="sxs-lookup"><span data-stu-id="b861a-139">This field is optional.</span></span>|  
    |<span data-ttu-id="b861a-140">**Kommentarer**</span><span class="sxs-lookup"><span data-stu-id="b861a-140">**Comments**</span></span>|<span data-ttu-id="b861a-141">Beskriv filens innehåll.</span><span class="sxs-lookup"><span data-stu-id="b861a-141">Describe the content of the file.</span></span>|  
    |<span data-ttu-id="b861a-142">**Dimensioner**</span><span class="sxs-lookup"><span data-stu-id="b861a-142">**Dimensions**</span></span>|<span data-ttu-id="b861a-143">Markera dimensionerna du vill exportera.</span><span class="sxs-lookup"><span data-stu-id="b861a-143">Select the dimensions to export.</span></span>|  
    |<span data-ttu-id="b861a-144">**Räkenskapsår**</span><span class="sxs-lookup"><span data-stu-id="b861a-144">**Fiscal Year**</span></span>|<span data-ttu-id="b861a-145">Ange räkenskapsåret.</span><span class="sxs-lookup"><span data-stu-id="b861a-145">Enter the fiscal tax year.</span></span>|

4. <span data-ttu-id="b861a-146">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="b861a-146">Choose the **OK** button.</span></span>
5. <span data-ttu-id="b861a-147">Välj knappen **Öppna** eller **Spara** för att bestämma var den exporterade filen ska placeras.</span><span class="sxs-lookup"><span data-stu-id="b861a-147">Choose the **Open** or **Save** button to decide where to place the exported file.</span></span>

## <a name="see-also"></a><span data-ttu-id="b861a-148">Se även</span><span class="sxs-lookup"><span data-stu-id="b861a-148">See Also</span></span>  
 <span data-ttu-id="b861a-149">[SIE-grupp](https://go.microsoft.com/fwlink/?LinkID=164870&clcid=0x41d) </span><span class="sxs-lookup"><span data-stu-id="b861a-149">[Standard Import Export Group](https://go.microsoft.com/fwlink/?LinkID=164870&clcid=0x41d) </span></span>  
 [<span data-ttu-id="b861a-150">Lokal funktionalitet för Sverige</span><span class="sxs-lookup"><span data-stu-id="b861a-150">Sweden Local Functionality</span></span>](sweden-local-functionality.md)

