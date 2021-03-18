---
title: Ändra hur rapporten ska se ut genom att välja en annan layout | Microsoft Docs
description: Du kan använda olika layouter för en rapport och växla mellan layouter för att ändra utseendet på en rapport.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2785550b59e79d3bbda3a59422aabd7adac94c6e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393855"
---
# <a name="change-the-current-report-layout"></a><span data-ttu-id="e523f-103">Ändra aktuell rapportlayout</span><span class="sxs-lookup"><span data-stu-id="e523f-103">Change the Current Report Layout</span></span>
<span data-ttu-id="e523f-104">En rapport kan ställas in med fler än en rapportlayout som du kan växla mellan.</span><span class="sxs-lookup"><span data-stu-id="e523f-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="e523f-105">Beroende på layouterna som finns tillgängliga för en rapport kan du välja att använda en inbyggd RDLC-rapportlayout, en inbyggd Word-rapportlayout eller en anpassad layout.</span><span class="sxs-lookup"><span data-stu-id="e523f-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="e523f-106">Mer information om RDLC- och Word-rapportlayouter, inbyggda och anpassade layouter och mer finns i [Hantera rapportlayouter](ui-manage-report-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="e523f-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

<span data-ttu-id="e523f-107">När anpassade layouter för rapporter definieras kan du välja dem från kund- och leverantörskort för att ange att valda layouter ska användas för de dokument som du skapar för kunden eller leverantören i fråga.</span><span class="sxs-lookup"><span data-stu-id="e523f-107">When custom report layouts are defined, you can select them from customer and vendor cards to specify that the selected layouts will be used for documents that you crate for the customer or vendor in question.</span></span> <span data-ttu-id="e523f-108">Mer information finns i [definiera dokumentlayout för kunder och leverantörer](ui-define-customer-vendor-document-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="e523f-108">For more information, see [Define Document Layouts for Customers and Vendors](ui-define-customer-vendor-document-layouts.md).</span></span>

> [!TIP]  
> <span data-ttu-id="e523f-109">Dokumentrapporter (inte listor) som använder en Word-rapportlayout är vanligtvis snabbare än de med en RDLC-rapportlayout.</span><span class="sxs-lookup"><span data-stu-id="e523f-109">Document reports (not lists) that use a Word report layout are typically faster than those that use an RDLC report layout.</span></span> <span data-ttu-id="e523f-110">Om du har möjlighet att välja mellan ett ord eller en RDLC-rapportlayout för en dokumentrapport kan du alltså använda Word-rapportlayouten för bästa prestanda.</span><span class="sxs-lookup"><span data-stu-id="e523f-110">So if you have the option to choose between a Word or RDLC report layout for a document report, use the Word report layout for the best performance.</span></span>

## <a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a><span data-ttu-id="e523f-111">Ändra vilken rapportlayout som ska användas för en rapport eller ett dokument</span><span class="sxs-lookup"><span data-stu-id="e523f-111">To change which report layout to use for a report or document</span></span>
1. <span data-ttu-id="e523f-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Val av rapportlayout** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="e523f-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="e523f-113">Sidan **Val av rapportlayout** visar alla rapporter som är tillgängliga i företaget som har angetts i fältet **Företag** högst upp på sidan.</span><span class="sxs-lookup"><span data-stu-id="e523f-113">The **Report Layout Selection** page lists all the reports that are available for the company that is specified in the **Company** field at the top of the page.</span></span> <span data-ttu-id="e523f-114">Fältet **Vald layout** anger den layout som används i rapporten för närvarande.</span><span class="sxs-lookup"><span data-stu-id="e523f-114">The **Selected Layout** field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="e523f-115">Ange fältet **Företag** fältet högst upp på sidan till företaget som inkluderar rapporten.</span><span class="sxs-lookup"><span data-stu-id="e523f-115">Set the **Company** field at the top of the page to the company that includes the report.</span></span>
3. <span data-ttu-id="e523f-116">I raden för rapporten och anger du fältet **Vald layout** till ett av följande alternativ för att ändra layouten som används för en rapport:</span><span class="sxs-lookup"><span data-stu-id="e523f-116">To change the layout that is used by a report, on the row for the report, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="e523f-117">**RDLC (inbyggd)**, använder den inbyggda RDLC-rapportlayouten i rapporten.</span><span class="sxs-lookup"><span data-stu-id="e523f-117">**RDLC (built-in)**, uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="e523f-118">**Word (inbyggd)**, använder den inbyggda Word-rapportlayouten i rapporten.</span><span class="sxs-lookup"><span data-stu-id="e523f-118">**Word (built-in)**, uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="e523f-119">**Anpassad** använder en anpassad layout i rapporten.</span><span class="sxs-lookup"><span data-stu-id="e523f-119">**Custom**, uses a custom layout on the report.</span></span>  

> [!NOTE]
> <span data-ttu-id="e523f-120">Om du väljer en rapportlayout av typen **RDLC (inbyggt)** eller **Word (inbyggt)** och du får ett felmeddelande att rapporten inte har en layout för den angivna typen, måste du välja ett annat layoutalternativ eller skapa en anpassad rapportlayout av den typ som du vill använda.</span><span class="sxs-lookup"><span data-stu-id="e523f-120">If you choose a report layout of type **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span> <span data-ttu-id="e523f-121">Visa nästa procedur.</span><span class="sxs-lookup"><span data-stu-id="e523f-121">See the next procedure.</span></span>

<span data-ttu-id="e523f-122">Om du har valt en inbyggd RDLC- eller Word-rapportlayout krävs ingen mer åtgärd och layouten används i när rapporten körs nästa gång.</span><span class="sxs-lookup"><span data-stu-id="e523f-122">If you selected a built-in RDLC or Word report layout, then no further action is required, and the layout will be used the next time the report is run.</span></span>

## <a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a><span data-ttu-id="e523f-123">Så här ändrar du den anpassade layouten som ska användas för en rapportlayout</span><span class="sxs-lookup"><span data-stu-id="e523f-123">To change the custom layout to use for a report layout</span></span>
<span data-ttu-id="e523f-124">Du kanske också vill ändra den anpassade layout som används.</span><span class="sxs-lookup"><span data-stu-id="e523f-124">You may also want to change the currently used custom layout.</span></span> <span data-ttu-id="e523f-125">Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="e523f-125">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>

<span data-ttu-id="e523f-126">Alla layouter för anpassade rapporter som finns för rapportmallar i ett företag visas på sidan **Anpassa rapportlayouter**.</span><span class="sxs-lookup"><span data-stu-id="e523f-126">All custom report layouts that exist for report layouts in a company are listed on the **Custom Report Layouts** page.</span></span> <span data-ttu-id="e523f-127">På sidan **Val av rapportlayout** kan du se vilka anpassade layouter som är tillgängliga för rapporten i faktaboxen **Anpassade layouter**.</span><span class="sxs-lookup"><span data-stu-id="e523f-127">On the **Report Layout Selection** page, you can see which custom layouts are available for each report in the **Custom Layouts** FactBox.</span></span>

1. <span data-ttu-id="e523f-128">På sidan **Val av rapportlayout** på raden för den rapportlayout som du vill ändra, väl uppslagsknappen i fältet **anpassad layoutbeskrivning** .</span><span class="sxs-lookup"><span data-stu-id="e523f-128">On the **Report Layout Selection** page, on the line for the report layout that you want to change, choose the lookup button in the **Custom Layout Description** field.</span></span>
2. <span data-ttu-id="e523f-129">På sidan **Rapportlayoutbeskrivning** markera raden för anpassad layout som du vill använda, och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="e523f-129">On the **Custom Report Layouts** page, select the row for the custom layout that you want to use, and then choose the **OK** button.</span></span>

<span data-ttu-id="e523f-130">Namnet på den valda anpassade layouten visas nu i fältet **Anpassad layoutbeskrivning** kommer att användas nästa gång rapporten eller dokumentet förhandsgranskas, skrivs ut eller skickas.</span><span class="sxs-lookup"><span data-stu-id="e523f-130">The name of the selected custom layout is now shown in the **Custom Layout Description** field and will be used the next time the report or document is previewed, printed, or sent.</span></span>

<span data-ttu-id="e523f-131">Du kan nu gå till kund- och leverantörskorten för att ange vilka layouter som ska användas för olika dokument som du har för kunden eller leverantören i fråga, t. ex. orderbekräftelser eller betalningspåminnelser.</span><span class="sxs-lookup"><span data-stu-id="e523f-131">You can now go to your customer and vendor cards to specify which of the layouts to use for different documents that you crate for the customer or vendor in question, such as order confirmations or payment reminders.</span></span> <span data-ttu-id="e523f-132">Mer information finns i [definiera dokumentlayout för kunder och leverantörer](ui-define-customer-vendor-document-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="e523f-132">For more information, see [Define Document Layouts for Customers and Vendors](ui-define-customer-vendor-document-layouts.md).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="e523f-133">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="e523f-133">See Related Training at [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="e523f-134">Se även</span><span class="sxs-lookup"><span data-stu-id="e523f-134">See Also</span></span>
[<span data-ttu-id="e523f-135">Hantera rapportlayouter</span><span class="sxs-lookup"><span data-stu-id="e523f-135">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="e523f-136">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e523f-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]