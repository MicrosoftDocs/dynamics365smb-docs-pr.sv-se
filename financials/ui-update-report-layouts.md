---
title: Uppdatera en rapportlayout kontinuerligt | Microsoft Docs
description: "Du kan behöva uppdatera en anpassad rapportlayout som används i en rapport. Det krävs när en designändring har skett för rapportens datauppsättning, till exempel att ett fält som används i layouten har tagits bort från rapportdatauppsättningen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c94729c84470267421207a6edaa413116718f715
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="updating-report-or-document-layouts"></a><span data-ttu-id="26e21-104">Uppdatera rapport- eller dokumentlayouter</span><span class="sxs-lookup"><span data-stu-id="26e21-104">Updating Report or Document Layouts</span></span>
<span data-ttu-id="26e21-105">Ibland kan du behöva uppdatera en anpassad rapportlayout som används i en rapport.</span><span class="sxs-lookup"><span data-stu-id="26e21-105">Occasionally, you may need to update a custom report layout that is used on a report.</span></span> <span data-ttu-id="26e21-106">Det krävs när en designändring har skett för rapportens datauppsättning, till exempel att ett fält som används i layouten har tagits bort från rapportdatauppsättningen.</span><span class="sxs-lookup"><span data-stu-id="26e21-106">This is required when there has been a design change to the report's data set, for example, a field that is used in the layout has been removed from the report data set.</span></span> <span data-ttu-id="26e21-107">Om en rapportlayout kräver att uppdatering kommer du att få ett felmeddelande när du försöker att förhandsgranska, skriva ut eller spara rapporten.</span><span class="sxs-lookup"><span data-stu-id="26e21-107">If a report layout requires updating, you will get an error message when you try to preview, print or save the report.</span></span>  
  
<span data-ttu-id="26e21-108">Du kan automatiskt uppdatera rapportlayouten från felmeddelandet som visas när du kör en rapport genom att välja knappen **Ja** på felmeddelandet.</span><span class="sxs-lookup"><span data-stu-id="26e21-108">You can automatically update a report layout from the error message that appears when you run the report by choosing the **Yes** button on the error message.</span></span> <span data-ttu-id="26e21-109">Eller, innan du kör rapporter, kan du uppdatera specifika rapportlayouter eller alla anpassade rapportlayouter som kan påverkas av datauppsättningsändringar.</span><span class="sxs-lookup"><span data-stu-id="26e21-109">Or, in advance of running reports, you can update specific report layouts or all custom report layouts that might be affected by dataset changes.</span></span>  
  
<span data-ttu-id="26e21-110">Du kan också välja att testa uppdateringarna utan att tillämpa de nödvändiga ändringarna i de anpassade rapportlayouterna.</span><span class="sxs-lookup"><span data-stu-id="26e21-110">You also have the option to test updates without applying the required changes to the custom report layouts.</span></span> <span data-ttu-id="26e21-111">På så sätt kan du se vilka ändringar som kommer att tillämpas i rapportlayouten och identifiera eventuella fel i processen.</span><span class="sxs-lookup"><span data-stu-id="26e21-111">This enables you to see what changes will be applied to the report layout and identify possible issues in the process.</span></span> <span data-ttu-id="26e21-112">Från testresultaten kan du öppna de anpassade rapportlayouterna direkt och åtgärda eventuella fel.</span><span class="sxs-lookup"><span data-stu-id="26e21-112">From the test results, you can open the custom report layouts directly for editing to fix any issues.</span></span> <span data-ttu-id="26e21-113">Vi rekommenderar att du testar rapportlayoutuppdateringarna innan du tillämpar dem.</span><span class="sxs-lookup"><span data-stu-id="26e21-113">We recommend that you test the report layout update before you apply the updates.</span></span>  
  
<span data-ttu-id="26e21-114">Alla rapportdatauppsättningsändringar kan inte uppdateras automatiskt i rapportlayouter.</span><span class="sxs-lookup"><span data-stu-id="26e21-114">Not all report dataset changes can be automatically updated in the report layouts.</span></span> <span data-ttu-id="26e21-115">För vissa ändringar krävs att du redigerar rapportlayouten manuellt.</span><span class="sxs-lookup"><span data-stu-id="26e21-115">Some changes will require that you manually edit the report layout.</span></span> <span data-ttu-id="26e21-116">Mer information finns i [Begränsningar för uppdatering av anpassad rapportlayout](ui-update-report-layouts.md#UpdateLimitations).</span><span class="sxs-lookup"><span data-stu-id="26e21-116">For more information, see [Limitations of the Custom Report Layout Update](ui-update-report-layouts.md#UpdateLimitations).</span></span>  
  
## <a name="to-update-one-or-more-custom-report-layouts"></a><span data-ttu-id="26e21-117">Så här uppdaterar du en eller flera anpassade rapportlayouter</span><span class="sxs-lookup"><span data-stu-id="26e21-117">To update one or more custom report layouts</span></span>  
  
1.  <span data-ttu-id="26e21-118">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Rapportlayouter** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26e21-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Layouts**, and then choose the related link.</span></span>  
  
2.  <span data-ttu-id="26e21-119">I fönstret **rapportlayouter**, om du vill uppdatera in en viss layout i listan, väljer du layouten från listan och sedan åtgärden **uppdatera layouten**.</span><span class="sxs-lookup"><span data-stu-id="26e21-119">In the **Report Layouts** window, if you want to update a specific report, select the layout from the list, and then choose the **Update Layout** action.</span></span> <span data-ttu-id="26e21-120">Eller, om du vill uppdatera alla standardrapportlayouter för företaget, klickar du på åtgärden **uppdatera alla layouter**.</span><span class="sxs-lookup"><span data-stu-id="26e21-120">Or, if you want to update all custom report layouts for the company, choose the **Update All Layouts** action.</span></span>  

<span data-ttu-id="26e21-121">Om inga fel uppstår tillämpas uppdateringarna för rapportlayouterna.</span><span class="sxs-lookup"><span data-stu-id="26e21-121">If no errors occur, then the updates is applied to the report layouts.</span></span> <span data-ttu-id="26e21-122">Om fel uppstår visas ett meddelande med felen.</span><span class="sxs-lookup"><span data-stu-id="26e21-122">If errors occur, then a message that contains the errors appears.</span></span> <span data-ttu-id="26e21-123">Då måste du åtgärda felen genom att redigera den anpassade rapportlayouten manuellt.</span><span class="sxs-lookup"><span data-stu-id="26e21-123">You will then have to manually edit the custom report layout to fix the error.</span></span> <span data-ttu-id="26e21-124">Mer information finns i [Åtgärda fel](ui-update-report-layouts.md#FixErrors).</span><span class="sxs-lookup"><span data-stu-id="26e21-124">For more information, see [Fixing Errors](ui-update-report-layouts.md#FixErrors).</span></span>  

## <a name="to-test-custom-report-layout-updates"></a><span data-ttu-id="26e21-125">Så här testar du uppdateringar för en anpassade rapportlayout</span><span class="sxs-lookup"><span data-stu-id="26e21-125">To test custom report layout updates</span></span>  
  
1.  <span data-ttu-id="26e21-126">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Val av rapportlayout** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26e21-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
  
2.  <span data-ttu-id="26e21-127">I fönstret **Val av rapportlayout** väljer du åtgärden **Testlayoutuppdateringar**.</span><span class="sxs-lookup"><span data-stu-id="26e21-127">In the **Report Layout Selection** window, choose the **Test Layout Updates** action.</span></span>  
  
 <span data-ttu-id="26e21-128">Ändringar till rapportlayouterna testas men tillämpas inte på de faktiska rapportlayouterna.</span><span class="sxs-lookup"><span data-stu-id="26e21-128">Chnages to the report layouts are tested but not applied to the actual report layouts.</span></span> <span data-ttu-id="26e21-129">Fönstret **Uppdateringslogg för rapportlayout** visas med status för potentiella uppdateringar för varje rapportlayout.</span><span class="sxs-lookup"><span data-stu-id="26e21-129">A **Report Layout Update Log** window appears that provides the status a potential updates for each report layout.</span></span> <span data-ttu-id="26e21-130">Om det finns fel för en rapportlayout kan du öppna rapportlayouten direkt från meddelandet och åtgärda felen.</span><span class="sxs-lookup"><span data-stu-id="26e21-130">If there are errors for a report layout, you can access the report layout directly for editing from the message to fix any issues.</span></span> <span data-ttu-id="26e21-131">Mer information finns i [Åtgärda fel](ui-update-report-layouts.md#FixErrors).</span><span class="sxs-lookup"><span data-stu-id="26e21-131">For more information, see [Fixing Errors](ui-update-report-layouts.md#FixErrors).</span></span>  
  
##  <span data-ttu-id="26e21-132"><a name="UpdateLimitations"></a> Begränsningar för uppdatering av anpassad rapportlayout</span><span class="sxs-lookup"><span data-stu-id="26e21-132"><a name="UpdateLimitations"></a> Limitations of the Custom Report Layout Update</span></span>  
 <span data-ttu-id="26e21-133">Det finns flera typer av ändringar som den automatiska uppdateringen kan tillämpa för anpassade rapportlayouter. Ett fält som används i layouten kan till exempel ha tagits bort från rapportdatauppsättningen.</span><span class="sxs-lookup"><span data-stu-id="26e21-133">There are several types of changes that the automatic update can apply to custom report layouts, for example, a field that is used in the layout has been removed from the report data set.</span></span> <span data-ttu-id="26e21-134">Däremot kan den automatiska uppdateringen inte hantera följande ändringar i en rapportdatauppsättning.</span><span class="sxs-lookup"><span data-stu-id="26e21-134">However, the automatic update cannot handle the following changes to a report dataset.</span></span>  
  
1.  <span data-ttu-id="26e21-135">Borttagna fält, rubriker eller dataobjekt.</span><span class="sxs-lookup"><span data-stu-id="26e21-135">Deleted fields, labels, or data items.</span></span>  
  
2.  <span data-ttu-id="26e21-136">Dubblettfältnamn i rapportlayouten efter att namnet på fältet har ändrats i datauppsättningen.</span><span class="sxs-lookup"><span data-stu-id="26e21-136">Duplicate field names in the report layout after a field has been renamed in the dataset.</span></span> <span data-ttu-id="26e21-137">Det här ska behandlas som ett designfel.</span><span class="sxs-lookup"><span data-stu-id="26e21-137">This should be treated as a design error.</span></span>  
  
3.  <span data-ttu-id="26e21-138">Uppgraderingsscenarier där det finns flera iterationer av en rapportlayout som orsakar flera namnbytesåtgärder för samma fält, rubriker eller dataobjekt.</span><span class="sxs-lookup"><span data-stu-id="26e21-138">Upgrade scenarios where there are multiple iterations of a report layout that causes multiple rename actions on the same fields, labels or data items.</span></span>  
  
 <span data-ttu-id="26e21-139">Om något av dessa problem identifieras i uppdateringsprocessen kan inte uppdateringen tillämpas.</span><span class="sxs-lookup"><span data-stu-id="26e21-139">If the update process detects any one of these issues, the update cannot be applied.</span></span> <span data-ttu-id="26e21-140">Du måste åtgärda problemen manuellt, till exempel genom att redigera rapportlayouten i Word eller via programmering med hjälp av kodenheter för uppgradering.</span><span class="sxs-lookup"><span data-stu-id="26e21-140">You will have to fix the issues manually, for example by editing the report layout in Word, or programmatically by using upgrade codeunits.</span></span>  
  
##  <span data-ttu-id="26e21-141"><a name="FixErrors"></a> Åtgärda fel</span><span class="sxs-lookup"><span data-stu-id="26e21-141"><a name="FixErrors"></a> Fixing Errors</span></span>  
 <span data-ttu-id="26e21-142">Om du får ett felmeddelande när du uppdaterar eller testar rapportlayoutuppdateringar måste du troligtvis ändra rapportlayouten för att lösa problemet.</span><span class="sxs-lookup"><span data-stu-id="26e21-142">If you get an error message when you update or test report layout updates, you most likely will have to modify the report layout to fix the problem.</span></span> <span data-ttu-id="26e21-143">Läs felmeddelandet för att fastställa orsaken till problemet.</span><span class="sxs-lookup"><span data-stu-id="26e21-143">Read the error message to help determine the cause of the problem.</span></span>  
  
 <span data-ttu-id="26e21-144">De mest vanliga problemet inträffar när ett fält som användes på layout har tagits bort från rapportdatauppsättningen.</span><span class="sxs-lookup"><span data-stu-id="26e21-144">The most typical problem occurs when a field that is used on the layout has been removed from the report dataset.</span></span> <span data-ttu-id="26e21-145">I det här fallet visas en rad i felmeddelandet som anger att en artikel har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="26e21-145">In this case, you will see a line in the error message that states that an item has been removed.</span></span> <span data-ttu-id="26e21-146">För att lösa problemet måste du ändra layouten och ta bort fältet i fråga.</span><span class="sxs-lookup"><span data-stu-id="26e21-146">To fix this issue, you will have to modify the layout and remove the field in question.</span></span>  
  
 <span data-ttu-id="26e21-147">Mer information finns i [så här skapar du och ändrar en anpassad rapportlayout](ui-how-create-custom-report-layout.md#ModifyCustomLayout).</span><span class="sxs-lookup"><span data-stu-id="26e21-147">For more information, see [How to: Create and Modify a Custom Report Layout](ui-how-create-custom-report-layout.md#ModifyCustomLayout).</span></span>  
  
 <span data-ttu-id="26e21-148">Försök att uppdatera layouten på nytt när du har ändrat layouten.</span><span class="sxs-lookup"><span data-stu-id="26e21-148">After you modify the layout, try to update the layout again.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26e21-149">Se även</span><span class="sxs-lookup"><span data-stu-id="26e21-149">See Also</span></span>  
 [<span data-ttu-id="26e21-150">Hantera rapportlayouter</span><span class="sxs-lookup"><span data-stu-id="26e21-150">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
 [<span data-ttu-id="26e21-151">Arbeta med rapporter</span><span class="sxs-lookup"><span data-stu-id="26e21-151">Working with Reports</span></span>](ui-work-report.md)  