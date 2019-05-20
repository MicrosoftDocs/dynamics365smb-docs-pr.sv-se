---
title: Ändra hur rapporten ska se ut genom att välja en annan layout | Microsoft Docs
description: Du kan använda olika layouter för en rapport och växla mellan layouter för att ändra utseendet på en rapport.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: f24f1cd24a31ddbd0b455b876821ae0173a677c3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249448"
---
# <a name="change-which-layout-is-currently-used-on-a-report"></a><span data-ttu-id="58de1-103">Ändra den layout som används i en rapport för närvarande</span><span class="sxs-lookup"><span data-stu-id="58de1-103">Change Which Layout is Currently Used on a Report</span></span>
<span data-ttu-id="58de1-104">En rapport kan ställas in med fler än en rapportlayout som du kan växla mellan.</span><span class="sxs-lookup"><span data-stu-id="58de1-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="58de1-105">Beroende på layouterna som finns tillgängliga för en rapport kan du välja att använda en inbyggd RDLC-rapportlayout, en inbyggd Word-rapportlayout eller en anpassad layout.</span><span class="sxs-lookup"><span data-stu-id="58de1-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="58de1-106">Mer information om RDLC- och Word-rapportlayouter, inbyggda och anpassade layouter och mer finns i [Hantera rapportlayouter](ui-manage-report-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="58de1-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

> [!TIP]  
> <span data-ttu-id="58de1-107">Dokumentrapporter (inte listor) som använder en Word-rapportlayout är vanligtvis snabbare än de med en RDLC-rapportlayout.</span><span class="sxs-lookup"><span data-stu-id="58de1-107">Document reports (not lists) that use a Word report layout are typically faster than those that use an RDLC report layout.</span></span> <span data-ttu-id="58de1-108">Om du har möjlighet att välja mellan ett ord eller en RDLC-rapportlayout för en dokumentrapport kan du alltså använda Word-rapportlayouten för bästa prestanda.</span><span class="sxs-lookup"><span data-stu-id="58de1-108">So if you have the option to choose between a Word or RDLC report layout for a document report, use the Word report layout for the best performance.</span></span>  

## <a name="to-change-the-layout-that-is-used-on-a-report"></a><span data-ttu-id="58de1-109">Så här ändrar du layout som används i en rapport</span><span class="sxs-lookup"><span data-stu-id="58de1-109">To change the layout that is used on a report</span></span>
1. <span data-ttu-id="58de1-110">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Val av rapportlayout** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="58de1-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="58de1-111">Sidan **Val av rapportlayout** visar alla rapporter som är tillgängliga i företaget som har angetts i fältet Företag högst upp på sidan.</span><span class="sxs-lookup"><span data-stu-id="58de1-111">The **Report Layout Selection** page lists all the reports that are available for the company that is specified in the Company field at the top of the page.</span></span> <span data-ttu-id="58de1-112">Fältet Vald layout anger den layout som används i rapporten för närvarande.</span><span class="sxs-lookup"><span data-stu-id="58de1-112">The Selected Layout field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="58de1-113">Ange fältet **Företag** fältet högst upp på sidan till företaget som inkluderar rapporten.</span><span class="sxs-lookup"><span data-stu-id="58de1-113">Set the **Company** field at the top of the page to the company that includes the report.</span></span>
3. <span data-ttu-id="58de1-114">I raden för rapporten i listan och anger du fältet **Vald layout** till ett av följande alternativ för att ändra layouten som används för en rapport:</span><span class="sxs-lookup"><span data-stu-id="58de1-114">To change the layout that is used by a report, in the row for the report in the list, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="58de1-115">RDLC (inbyggd), använder den inbyggda RDLC-rapportlayouten i rapporten.</span><span class="sxs-lookup"><span data-stu-id="58de1-115">RDLC (built-in), uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="58de1-116">Word (inbyggd), använder den inbyggda Word-rapportlayouten i rapporten.</span><span class="sxs-lookup"><span data-stu-id="58de1-116">Word (built-in), uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="58de1-117">Anpassad använder en anpassad layout i rapporten.</span><span class="sxs-lookup"><span data-stu-id="58de1-117">Custom, uses a custom layout on the report.</span></span>  
     <span data-ttu-id="58de1-118">Du kan se vilka anpassade layouter som är tillgängliga för rapporten i faktaboxen Rapportlayoutdelar.</span><span class="sxs-lookup"><span data-stu-id="58de1-118">You can see which custom layouts are available for the report in the Report Layouts Part FactBox.</span></span> <span data-ttu-id="58de1-119">Om det inte finns några anpassade layouter för rapporten, måste du skapa en först.</span><span class="sxs-lookup"><span data-stu-id="58de1-119">If there are no custom layouts for the report, then you will have to create one first.</span></span> <span data-ttu-id="58de1-120">Om du väljer det här alternativet, gå vidare till nästa procedur för att ange den anpassade layout som du vill använda.</span><span class="sxs-lookup"><span data-stu-id="58de1-120">If you choose this option, go to the next procedure to specify the custom layout that you want to use.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="58de1-121">Om du väljer **RDLC (inbyggt)** eller **Word (inbyggt)** och du får ett felmeddelande att rapporten inte har en layout för den angivna typen, måste du välja ett annat layoutalternativ eller skapa en anpassad rapportlayout av den typ som du vill använda.</span><span class="sxs-lookup"><span data-stu-id="58de1-121">If you choose **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span>

<span data-ttu-id="58de1-122">Om du har valt en inbyggd RDLC- eller Word-rapportlayout krävs ingen mer åtgärd och layouten används i när rapporten körs nästa gång.</span><span class="sxs-lookup"><span data-stu-id="58de1-122">If you selected a built-in RDLC or Word report layout, then no further action is required and the layout will be used the next time the report is run.</span></span>

## <a name="to-specify-a-custom-layout-on-a-report"></a><span data-ttu-id="58de1-123">Så här anger du en anpassad layout på en rapport</span><span class="sxs-lookup"><span data-stu-id="58de1-123">To specify a custom layout on a report</span></span>
1. <span data-ttu-id="58de1-124">Du anger vilken anpassad layout som ska användas i rapporten på sidan **Anpassad rapportlayout**.</span><span class="sxs-lookup"><span data-stu-id="58de1-124">You specify which custom layout to use on the report from the **Custom Report Layouts** page.</span></span> <span data-ttu-id="58de1-125">Om sidan **Anpassad rapportlayout** inte är öppet väljer du sökknappen i fältet **Rapportlayoutbeskrivning**.</span><span class="sxs-lookup"><span data-stu-id="58de1-125">If the **Custom Report Layouts** page is not open, then in the **Report Layout Description** field, choose the lookup button.</span></span>
2. <span data-ttu-id="58de1-126">På sidan **Rapportlayoutbeskrivning** markera raden för anpassad layout som du vill använda, och stäng sedan sidan.</span><span class="sxs-lookup"><span data-stu-id="58de1-126">On the **Custom Report Layouts** page, select the row for custom layout that you want to use, and then close the page.</span></span>

<span data-ttu-id="58de1-127">Du återgår till sidan **Val av rapportlayout**.</span><span class="sxs-lookup"><span data-stu-id="58de1-127">You return to the **Report Layout Selection** page.</span></span> <span data-ttu-id="58de1-128">Namnet på den valda anpassade layouten visas i fältet **Anpassad layoutbeskrivning**.</span><span class="sxs-lookup"><span data-stu-id="58de1-128">The name of the selected custom layout displays in the **Custom Layout Description** field.</span></span> <span data-ttu-id="58de1-129">Den anpassade layouten används nästa gången som du kör rapporten.</span><span class="sxs-lookup"><span data-stu-id="58de1-129">The custom layout will be used the next time that you run the report.</span></span>

## <a name="see-also"></a><span data-ttu-id="58de1-130">Se även</span><span class="sxs-lookup"><span data-stu-id="58de1-130">See Also</span></span>
[<span data-ttu-id="58de1-131">Hantera rapportlayouter</span><span class="sxs-lookup"><span data-stu-id="58de1-131">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="58de1-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="58de1-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
