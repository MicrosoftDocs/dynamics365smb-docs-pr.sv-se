---
title: GIFI-koder i Kanada | Microsoft Docs
Description: "I Kanada kan du ställa in General Index of Financial Information (GIFI)-koder och tilldela dem till redovisningskonton"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-gifi-codes-in-canada"></a><span data-ttu-id="8e32a-103">Så här arbetar du med GIFI-koder i Kanada</span><span class="sxs-lookup"><span data-stu-id="8e32a-103">How to: Work With GIFI Codes in Canada</span></span>
<span data-ttu-id="8e32a-104">Skatteinformation kan inkludera redovisningskonton, rapporter, resultaträkningar, balansräkningar och rapporter över balanserad vinst och förlust.</span><span class="sxs-lookup"><span data-stu-id="8e32a-104">Fiscal information can include general ledger accounts, reports, income statements, balance sheets, and statements of retained earnings.</span></span> <span data-ttu-id="8e32a-105">Skatteinformation grupperas med hjälp av koder.</span><span class="sxs-lookup"><span data-stu-id="8e32a-105">Fiscal information is classified using codes.</span></span> <span data-ttu-id="8e32a-106">Hanteringen av koder hjälper regeringen att bearbeta information, förbereda sig för elektronisk arkivering och validera skatteinformation elektroniskt.</span><span class="sxs-lookup"><span data-stu-id="8e32a-106">The use of codes helps the government to process information, prepare for electronic filing, and validate tax information electronically.</span></span> <span data-ttu-id="8e32a-107">Hanteringen av koder hjälper också statistiska organisationer att arbeta mer effektivt, eftersom den ekonomiska informationen är mer lättillgänglig.</span><span class="sxs-lookup"><span data-stu-id="8e32a-107">The use of codes also helps statistical organizations to work more efficiently, as financial information is more readily available.</span></span> <span data-ttu-id="8e32a-108">Mer information finns i [Webbplatsen för Canada Revenue Agency](http://www.cra-arc.gc.ca/).</span><span class="sxs-lookup"><span data-stu-id="8e32a-108">For more information, see the [Canada Revenue Agency website](http://www.cra-arc.gc.ca/).</span></span>

<span data-ttu-id="8e32a-109">Canada Revenue Agency använder det allmänna indexet av koder för ekonomisk information (GIFI) för att elektroniskt samla, verifiera och bearbeta ekonomisk information och skatteinformation.</span><span class="sxs-lookup"><span data-stu-id="8e32a-109">The Canada Revenue Agency uses General Index of Financial Information (GIFI) codes to collect, validate, and process financial and tax information electronically.</span></span> <span data-ttu-id="8e32a-110">Det är bäst att endast tilldela GIFI-koder för bokföringskonton så att all summering görs av ditt skattförberedelseprogram.</span><span class="sxs-lookup"><span data-stu-id="8e32a-110">It is a best practice to assign GIFI codes only to posting accounts, so that all totaling is done by your tax preparation software.</span></span>

<span data-ttu-id="8e32a-111">När ett konto är kopplat till en GIFI-kod, rapporteras den till Revenue Agency med den koden.</span><span class="sxs-lookup"><span data-stu-id="8e32a-111">When an account is associated with a GIFI code, it is reported to the revenue agency under that code.</span></span> <span data-ttu-id="8e32a-112">Flera konton kan använda samma GIFI-kod, men varje konto kan endast ha en GIFI-kod.</span><span class="sxs-lookup"><span data-stu-id="8e32a-112">Multiple accounts can all have the same GIFI code, but each account can have only one GIFI code.</span></span>

<span data-ttu-id="8e32a-113">Du kan exportera information om saldo per GIFI-kod och spara den exporterade filen i Excel, vilket är användbart för att överföra information till ditt skattförberedelseprogram.</span><span class="sxs-lookup"><span data-stu-id="8e32a-113">You can export balance information by GIFI code and save the exported file in Excel, which is useful for transferring information to your tax preparation software.</span></span>

## <a name="to-set-up-gifi-codes"></a><span data-ttu-id="8e32a-114">Så här skapar du GIFI-koder:</span><span class="sxs-lookup"><span data-stu-id="8e32a-114">To set up GIFI codes</span></span>
<span data-ttu-id="8e32a-115">I Dynamics NAV måste du lägga upp GIFI-koder för redovisningskonton, rapporter, balansräkningar, inkomstark och rapporter över balanserad vinst och förlust.</span><span class="sxs-lookup"><span data-stu-id="8e32a-115">In Dynamics NAV, you must set up GIFI codes for general ledger accounts, reports, balance sheets, income sheets, and statements of retained earnings.</span></span>

1. <span data-ttu-id="8e32a-116">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **GIFI-koder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8e32a-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **GIFI Codes**, and then choose the related link.</span></span>
2. <span data-ttu-id="8e32a-117">I fönstret **GIFI-koder** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8e32a-117">In the **GIFI Codes** window, choose the **New** action.</span></span>
3. <span data-ttu-id="8e32a-118">Skapa GIFI-koder, genom att fylla i fälten.</span><span class="sxs-lookup"><span data-stu-id="8e32a-118">Set up GIFI codes by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a><span data-ttu-id="8e32a-119">Om du vill koppla GIFI-koder med redovisningskonton</span><span class="sxs-lookup"><span data-stu-id="8e32a-119">To associate GIFI codes with G/L accounts</span></span>
<span data-ttu-id="8e32a-120">Om du vill rapportera ekonomiska information med GIFI-kod, måste varje GIFI-kod vara kopplad till korrekta konton i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="8e32a-120">To report financial information by GIFI code, each GIFI code must be associated with the appropriate accounts in the chart of accounts.</span></span>

1. <span data-ttu-id="8e32a-121">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kontoplan** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8e32a-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="8e32a-122">Välj ett relevant redovisningskonto och välj sedan åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="8e32a-122">Select a relevant general ledger account, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="8e32a-123">På snabbfliken **Kostnadsredovisning** i fältet **GIFI-kod** väljer du lämplig GIFI-kod.</span><span class="sxs-lookup"><span data-stu-id="8e32a-123">On the **Cost Accounting** FastTab, in the **GIFI Code** field, select an appropriate GIFI code.</span></span>

## <a name="to-view-account-balances-using-the-gifi-code-report"></a><span data-ttu-id="8e32a-124">Om du vill visa kontosaldon som använder GIFI-kodrapport</span><span class="sxs-lookup"><span data-stu-id="8e32a-124">To view account balances using the GIFI code report</span></span>
<span data-ttu-id="8e32a-125">Du kan granska kontosaldon per GIFI-kod, genom att använda rapporten **kontosaldon per GIFI-kod**.</span><span class="sxs-lookup"><span data-stu-id="8e32a-125">You can review your account balances by GIFI code by using the **Account Balances by GIFI Code** report.</span></span>

1. <span data-ttu-id="8e32a-126">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **kontosaldon per GIFI-kod** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8e32a-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Balances by GIFI Code**, and then choose the related link.</span></span>
2. <span data-ttu-id="8e32a-127">Ange vad som ska ingå i rapporten genom att fylla i fälten.</span><span class="sxs-lookup"><span data-stu-id="8e32a-127">Specify what to include in the report by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="8e32a-128">Välj knappen **Skriv ut** eller **Förhandsgranska**.</span><span class="sxs-lookup"><span data-stu-id="8e32a-128">Choose the **Print** or the **Preview** button.</span></span>

## <a name="to-export-balance-information-using-gifi-codes"></a><span data-ttu-id="8e32a-129">Så här exporterar du saldoinformation med hjälp av GIFI-koder</span><span class="sxs-lookup"><span data-stu-id="8e32a-129">To export balance information using GIFI codes</span></span>
<span data-ttu-id="8e32a-130">Du kan exportera saldoinformation med hjälp av GIFI-koder och spara den exporterade filen i Excel.</span><span class="sxs-lookup"><span data-stu-id="8e32a-130">You can export balance information using GIFI codes and save the exported file in Excel.</span></span> <span data-ttu-id="8e32a-131">Du kan ändra, spara eller ta bort filen.</span><span class="sxs-lookup"><span data-stu-id="8e32a-131">You can modify, save, or delete the file.</span></span> <span data-ttu-id="8e32a-132">Du kan använda den för att överföra information till ditt skattförberedelseprogram.</span><span class="sxs-lookup"><span data-stu-id="8e32a-132">You can use the file to transfer information to your tax preparation software.</span></span>

1. <span data-ttu-id="8e32a-133">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **GIFI-koder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8e32a-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Export GIFI Info. to Excel**, and then choose the related link.</span></span>
2. <span data-ttu-id="8e32a-134">Ange vad du vill exportera till Excel, genom att fylla i fälten.</span><span class="sxs-lookup"><span data-stu-id="8e32a-134">Specify what to export to Excel by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="8e32a-135">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e32a-135">Choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="8e32a-136">Excel-filen har följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="8e32a-136">The Excel file has the following characteristics:</span></span>

* <span data-ttu-id="8e32a-137">Saldot avrundas till den närmaste procentsatsen, men cellvärdet behåller samma procentsats som i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="8e32a-137">The balance is rounded to the nearest percentage, but the cell value maintains the same percentage as it does in the general ledger.</span></span>
* <span data-ttu-id="8e32a-138">Negativa nummer representeras av positiva nummer i hakparenteser.</span><span class="sxs-lookup"><span data-stu-id="8e32a-138">Negative numbers are represented as positive number in brackets.</span></span> <span data-ttu-id="8e32a-139">-123 anges därför som (123).</span><span class="sxs-lookup"><span data-stu-id="8e32a-139">Accordingly, -123 is represented as (123).</span></span>

## <a name="see-also"></a><span data-ttu-id="8e32a-140">Se även</span><span class="sxs-lookup"><span data-stu-id="8e32a-140">See Also</span></span>
<span data-ttu-id="8e32a-141">[Ekonomi](finance.md) </span><span class="sxs-lookup"><span data-stu-id="8e32a-141">[Finance](finance.md) </span></span>  
[<span data-ttu-id="8e32a-142">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="8e32a-142">Setting Up Finance</span></span>](finance-setup-finance.md)

