---
title: "Ändra hur rapporten ska se ut genom att välja en annan layout | Microsoft Docs"
description: "Du kan använda olika layouter för en rapport och växla mellan layouter för att ändra utseendet på en rapport."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 677b7319baff476671c4c8ade4afed843f936c36
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-change-which-layout-is-currently-used-on-a-report"></a><span data-ttu-id="d2b40-103">Så här ändrar du vilken layout som används i en rapport för närvarande</span><span class="sxs-lookup"><span data-stu-id="d2b40-103">How to: Change Which Layout is Currently Used on a Report</span></span>
<span data-ttu-id="d2b40-104">En rapport kan ställas in med fler än en rapportlayout som du kan växla mellan.</span><span class="sxs-lookup"><span data-stu-id="d2b40-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="d2b40-105">Beroende på layouterna som finns tillgängliga för en rapport kan du välja att använda en inbyggd RDLC-rapportlayout, en inbyggd Word-rapportlayout eller en anpassad layout.</span><span class="sxs-lookup"><span data-stu-id="d2b40-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="d2b40-106">Mer information om RDLC- och Word-rapportlayouter, inbyggda och anpassade layouter och mer finns i [Hantera rapportlayouter](ui-manage-report-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="d2b40-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

## <a name="to-change-the-layout-that-is-used-on-a-report"></a><span data-ttu-id="d2b40-107">Så här ändrar du layout som används i en rapport</span><span class="sxs-lookup"><span data-stu-id="d2b40-107">To change the layout that is used on a report</span></span>
1. <span data-ttu-id="d2b40-108">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Val av rapportlayout** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d2b40-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="d2b40-109">I fönstret **Val av rapportlayout** visas alla rapporter som är tillgängliga i företaget som har angetts i fältet Företag högst upp i fönstret.</span><span class="sxs-lookup"><span data-stu-id="d2b40-109">The **Report Layout Selection** window lists all the reports that are available for the company that is specified in the Company field at the top of the window.</span></span> <span data-ttu-id="d2b40-110">Fältet Vald layout anger den layout som används i rapporten för närvarande.</span><span class="sxs-lookup"><span data-stu-id="d2b40-110">The Selected Layout field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="d2b40-111">Ange fältet **Företag** fältet högst upp i fönstret till företaget som inkluderar rapporten.</span><span class="sxs-lookup"><span data-stu-id="d2b40-111">Set the **Company** field at the top of the window to the company that includes the report.</span></span>
3. <span data-ttu-id="d2b40-112">I raden för rapporten i listan och anger du fältet **Vald layout** till ett av följande alternativ för att ändra layouten som används för en rapport:</span><span class="sxs-lookup"><span data-stu-id="d2b40-112">To change the layout that is used by a report, in the row for the report in the list, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="d2b40-113">RDLC (inbyggd), använder den inbyggda RDLC-rapportlayouten i rapporten.</span><span class="sxs-lookup"><span data-stu-id="d2b40-113">RDLC (built-in), uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="d2b40-114">Word (inbyggd), använder den inbyggda Word-rapportlayouten i rapporten.</span><span class="sxs-lookup"><span data-stu-id="d2b40-114">Word (built-in), uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="d2b40-115">Anpassad använder en anpassad layout i rapporten.</span><span class="sxs-lookup"><span data-stu-id="d2b40-115">Custom, uses a custom layout on the report.</span></span>  
     <span data-ttu-id="d2b40-116">Du kan se vilka anpassade layouter som är tillgängliga för rapporten i faktaboxen Rapportlayoutdelar.</span><span class="sxs-lookup"><span data-stu-id="d2b40-116">You can see which custom layouts are available for the report in the Report Layouts Part FactBox.</span></span> <span data-ttu-id="d2b40-117">Om det inte finns några anpassade layouter för rapporten, måste du skapa en först.</span><span class="sxs-lookup"><span data-stu-id="d2b40-117">If there are no custom layouts for the report, then you will have to create one first.</span></span> <span data-ttu-id="d2b40-118">Om du väljer det här alternativet, gå vidare till nästa procedur för att ange den anpassade layout som du vill använda.</span><span class="sxs-lookup"><span data-stu-id="d2b40-118">If you choose this option, go to the next procedure to specify the custom layout that you want to use.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="d2b40-119">Om du väljer **RDLC (inbyggt)** eller **Word (inbyggt)** och du får ett felmeddelande att rapporten inte har en layout för den angivna typen, måste du välja ett annat layoutalternativ eller skapa en anpassad rapportlayout av den typ som du vill använda.</span><span class="sxs-lookup"><span data-stu-id="d2b40-119">If you choose **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span>

<span data-ttu-id="d2b40-120">Om du har valt en inbyggd RDLC- eller Word-rapportlayout krävs ingen mer åtgärd och layouten används i när rapporten körs nästa gång.</span><span class="sxs-lookup"><span data-stu-id="d2b40-120">If you selected a built-in RDLC or Word report layout, then no further action is required and the layout will be used the next time the report is run.</span></span>

## <a name="to-specify-a-custom-layout-on-a-report"></a><span data-ttu-id="d2b40-121">Så här anger du en anpassad layout på en rapport</span><span class="sxs-lookup"><span data-stu-id="d2b40-121">To specify a custom layout on a report</span></span>
1. <span data-ttu-id="d2b40-122">Du anger vilken anpassad layout som ska användas i rapporten i fönstret **Anpassad rapportlayout**.</span><span class="sxs-lookup"><span data-stu-id="d2b40-122">You specify which custom layout to use on the report from the **Custom Report Layouts** window.</span></span> <span data-ttu-id="d2b40-123">Om fönstret **Anpassad rapportlayout** inte är öppet väljer du sökknappen i fältet **Rapportlayoutbeskrivning**.</span><span class="sxs-lookup"><span data-stu-id="d2b40-123">If the **Custom Report Layouts** window is not open, then in the **Report Layout Description** field, choose the lookup button.</span></span>
2. <span data-ttu-id="d2b40-124">I fönstret **Rapportlayoutbeskrivning** markera raden för anpassad layout som du vill använda, och stäng sedan fönstret.</span><span class="sxs-lookup"><span data-stu-id="d2b40-124">In the **Custom Report Layouts** window, select the row for custom layout that you want to use, and then close the window.</span></span>

<span data-ttu-id="d2b40-125">Du återgår till fönstret **Val av rapportlayout**.</span><span class="sxs-lookup"><span data-stu-id="d2b40-125">You return to the **Report Layout Selection** window.</span></span> <span data-ttu-id="d2b40-126">Namnet på den valda anpassade layouten visas i fältet **Anpassad layoutbeskrivning**.</span><span class="sxs-lookup"><span data-stu-id="d2b40-126">The name of the selected custom layout displays in the **Custom Layout Description** field.</span></span> <span data-ttu-id="d2b40-127">Den anpassade layouten används nästa gången som du kör rapporten.</span><span class="sxs-lookup"><span data-stu-id="d2b40-127">The custom layout will be used the next time that you run the report.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2b40-128">Se även</span><span class="sxs-lookup"><span data-stu-id="d2b40-128">See Also</span></span>
[<span data-ttu-id="d2b40-129">Hantera rapportlayouter</span><span class="sxs-lookup"><span data-stu-id="d2b40-129">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="d2b40-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d2b40-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

