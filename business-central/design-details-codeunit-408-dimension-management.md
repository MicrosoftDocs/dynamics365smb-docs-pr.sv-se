---
title: Designdetaljer - Kodenhet 408 Dimension Management | Microsoft Docs
description: Kodenhet 408 DimensionManagement är ett funktionsbibliotek som hanterar gemensamma uppgifter som är kopplade till dimensioner, till exempel kopiering från en tabell till en annan eller från ett dokument till ett annat.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-dimension-set-entries
ms.openlocfilehash: 1b0238fb26b71310b1f02e15be7d7040832ca644
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2019
ms.locfileid: "938520"
---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="04b40-103">Designdetaljer: Kodenhet 408 Dimension Management</span><span class="sxs-lookup"><span data-stu-id="04b40-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="04b40-104">Kodenhet 408 DimensionManagement är ett funktionsbibliotek som hanterar gemensamma uppgifter som är kopplade till dimensioner, till exempel kopiering från en tabell till en annan eller från ett dokument till ett annat.</span><span class="sxs-lookup"><span data-stu-id="04b40-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="04b40-105">I det här avsnittet beskrivs funktionerna som har ändrats i Microsoft Dynamics NAV 2013 R2 vad som måste göras i funktionerna.</span><span class="sxs-lookup"><span data-stu-id="04b40-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="04b40-106">Många operationer tas bort, eftersom det inte finns något behov av att kopiera mellan dimensionstabeller.</span><span class="sxs-lookup"><span data-stu-id="04b40-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="04b40-107">Ändrade funktioner</span><span class="sxs-lookup"><span data-stu-id="04b40-107">Modified Functions</span></span>  

|<span data-ttu-id="04b40-108">Funktionsnamn</span><span class="sxs-lookup"><span data-stu-id="04b40-108">Function Name</span></span>|<span data-ttu-id="04b40-109">Ändringsbeskrivning</span><span class="sxs-lookup"><span data-stu-id="04b40-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="04b40-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="04b40-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="04b40-111">Nya funktion som ersätter övriga kontrollfunktioner och tar emot ett dimensionsuppsättnings-ID som ett argument istället för en dimensionstabell.</span><span class="sxs-lookup"><span data-stu-id="04b40-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="04b40-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="04b40-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="04b40-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="04b40-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="04b40-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="04b40-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="04b40-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="04b40-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="04b40-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="04b40-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="04b40-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="04b40-117">CheckDimValueComb</span></span>|<span data-ttu-id="04b40-118">Ta bort.</span><span class="sxs-lookup"><span data-stu-id="04b40-118">Delete.</span></span> <span data-ttu-id="04b40-119">All förbrukning ska ändras till CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="04b40-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="04b40-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="04b40-120">GetDefaultDim</span></span>|<span data-ttu-id="04b40-121">Ändra för att returnera en heltaldimensionsuppsättnings-ID istället för en uppsättning poster.</span><span class="sxs-lookup"><span data-stu-id="04b40-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="04b40-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="04b40-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="04b40-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="04b40-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="04b40-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="04b40-126">Ändra för att arbeta med DimSetID - > ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="04b40-127">Borttagna funktioner</span><span class="sxs-lookup"><span data-stu-id="04b40-127">Deleted Functions</span></span>  
 <span data-ttu-id="04b40-128">Funktioner som tagits bort från kodmodul 408 i samband med funktionen Dimensionsuppsättningstransaktioner anges nedan.</span><span class="sxs-lookup"><span data-stu-id="04b40-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="04b40-129">Under uppgraderingen av programkoden från Microsoft Dynamics NAV 2009 eller tidigare versioner till Microsoft Dynamics NAV 2016, är följande funktioner inte tillgängliga i Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="04b40-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="04b40-130">Om du har anpassningar som använder en eller flera av funktionerna måste du uppgradera koden därefter.</span><span class="sxs-lookup"><span data-stu-id="04b40-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="04b40-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="04b40-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="04b40-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="04b40-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="04b40-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="04b40-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="04b40-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="04b40-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="04b40-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="04b40-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-136">InsertDocDim</span></span>  

 <span data-ttu-id="04b40-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="04b40-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="04b40-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="04b40-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="04b40-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="04b40-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="04b40-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="04b40-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="04b40-141">InsertServContractDim</span></span>  

 <span data-ttu-id="04b40-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="04b40-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="04b40-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="04b40-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="04b40-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-144">GetDocDim</span></span>  

 <span data-ttu-id="04b40-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-145">GetProdDocDim</span></span>  

 <span data-ttu-id="04b40-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="04b40-146">TypeToTableID1</span></span>  

 <span data-ttu-id="04b40-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="04b40-147">TypeToTableID2</span></span>  

 <span data-ttu-id="04b40-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="04b40-148">TypeToTableID3</span></span>  

 <span data-ttu-id="04b40-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="04b40-149">TypeToTableID4</span></span>  

 <span data-ttu-id="04b40-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="04b40-150">TypeToTableID5</span></span>  

 <span data-ttu-id="04b40-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="04b40-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-152">DeleteDocDim</span></span>  

 <span data-ttu-id="04b40-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="04b40-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="04b40-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="04b40-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="04b40-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="04b40-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="04b40-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="04b40-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="04b40-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="04b40-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="04b40-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-160">ShowDocDim</span></span>  

 <span data-ttu-id="04b40-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-161">SaveDocDim</span></span>  

 <span data-ttu-id="04b40-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="04b40-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="04b40-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="04b40-164">ShowTempDim</span></span>  

 <span data-ttu-id="04b40-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="04b40-165">SaveTempDim</span></span>  

 <span data-ttu-id="04b40-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="04b40-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="04b40-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="04b40-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="04b40-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="04b40-168">SaveServContractDim</span></span>  

 <span data-ttu-id="04b40-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="04b40-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="04b40-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="04b40-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="04b40-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="04b40-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="04b40-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="04b40-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="04b40-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="04b40-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="04b40-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="04b40-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="04b40-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="04b40-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="04b40-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="04b40-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="04b40-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="04b40-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="04b40-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="04b40-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="04b40-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="04b40-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="04b40-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="04b40-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="04b40-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="04b40-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="04b40-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="04b40-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="04b40-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="04b40-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="04b40-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="04b40-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="04b40-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="04b40-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="04b40-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="04b40-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="04b40-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="04b40-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="04b40-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="04b40-198">TestDimValue</span></span>  

 <span data-ttu-id="04b40-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="04b40-199">TestNewDimValue</span></span>  

 <span data-ttu-id="04b40-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="04b40-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="04b40-201">(Ta bort eftersom tabellen ItemBudgetDim har tagits bort.)</span><span class="sxs-lookup"><span data-stu-id="04b40-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="04b40-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="04b40-202">GetServContractDim</span></span>  

 <span data-ttu-id="04b40-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="04b40-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="04b40-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="04b40-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="04b40-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="04b40-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="04b40-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="04b40-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="04b40-207">Se även</span><span class="sxs-lookup"><span data-stu-id="04b40-207">See Also</span></span>
 <span data-ttu-id="04b40-208">[Designdetaljer: Dimensionsuppsättningstransaktioner](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="04b40-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="04b40-209">[Designdetaljer: Översikt över dimensionsuppsättningstransaktioner](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="04b40-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="04b40-210">[Designdetaljer: Söka efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="04b40-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="04b40-211">[Designdetaljer: Tabellstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="04b40-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="04b40-212">Designdetaljer: Kodexempel på ändrade mönster i ändringar</span><span class="sxs-lookup"><span data-stu-id="04b40-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
