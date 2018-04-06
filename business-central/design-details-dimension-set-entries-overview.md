---
title: "Översikt över dimensionsuppsättningstransaktioner | Microsoft Docs"
description: "I det här avsnittet beskrivs hur dimensionsuppsättningstransaktioner lagras och bokförs i Dynamics 365."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1113f371caf00b693144d0ea6f74aed49bbbc9df
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="046d4-103">Översikt över dimensionsuppsättningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="046d4-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="046d4-104">I det här avsnittet beskrivs hur dimensionsuppsättningstransaktioner lagras och bokförs i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="046d4-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
## <a name="dimension-sets"></a><span data-ttu-id="046d4-105">Dimensionsuppsättningar</span><span class="sxs-lookup"><span data-stu-id="046d4-105">Dimension Sets</span></span>  
<span data-ttu-id="046d4-106">En dimensionsuppsättning en är en unik kombination av dimensionsvärden.</span><span class="sxs-lookup"><span data-stu-id="046d4-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="046d4-107">Den lagras som dimensionsuppsättningstransaktioner i databasen.</span><span class="sxs-lookup"><span data-stu-id="046d4-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="046d4-108">Varje dimensionsuppsättningstransaktion representerar ett enstaka dimensionsvärde.</span><span class="sxs-lookup"><span data-stu-id="046d4-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="046d4-109">Dimensionsuppsättningen identifieras av ett gemensamt dimensionsuppsättnings-ID som tilldelats varje dimensionsuppsättningstransaktion som tillhör dimensionsuppsättningen.</span><span class="sxs-lookup"><span data-stu-id="046d4-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  
  
<span data-ttu-id="046d4-110">Följande exempel visar när en dimensionsuppsättning som har tre dimensionsuppsättningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="046d4-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="046d4-111">Dimensionsuppsättningen identifieras av ett dimensionsuppsättnings-ID som är 108.</span><span class="sxs-lookup"><span data-stu-id="046d4-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  
  
|<span data-ttu-id="046d4-112">Dimensionsuppsättnings-ID</span><span class="sxs-lookup"><span data-stu-id="046d4-112">Dimension Set ID</span></span>|<span data-ttu-id="046d4-113">Dimensionskod</span><span class="sxs-lookup"><span data-stu-id="046d4-113">Dimension Code</span></span>|<span data-ttu-id="046d4-114">Dimensionsvärdekod</span><span class="sxs-lookup"><span data-stu-id="046d4-114">Dimension Value Code</span></span>|<span data-ttu-id="046d4-115">Dimensionsvärdesnamn</span><span class="sxs-lookup"><span data-stu-id="046d4-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="046d4-116">108</span><span class="sxs-lookup"><span data-stu-id="046d4-116">108</span></span>|<span data-ttu-id="046d4-117">OMRÅDE</span><span class="sxs-lookup"><span data-stu-id="046d4-117">AREA</span></span>|<span data-ttu-id="046d4-118">70</span><span class="sxs-lookup"><span data-stu-id="046d4-118">70</span></span>|<span data-ttu-id="046d4-119">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="046d4-119">America North</span></span>|  
|<span data-ttu-id="046d4-120">108</span><span class="sxs-lookup"><span data-stu-id="046d4-120">108</span></span>|<span data-ttu-id="046d4-121">RÖRELSEMALL</span><span class="sxs-lookup"><span data-stu-id="046d4-121">BUSINESSGROUP</span></span>|<span data-ttu-id="046d4-122">Home</span><span class="sxs-lookup"><span data-stu-id="046d4-122">HOME</span></span>|<span data-ttu-id="046d4-123">Start</span><span class="sxs-lookup"><span data-stu-id="046d4-123">Home</span></span>|  
|<span data-ttu-id="046d4-124">108</span><span class="sxs-lookup"><span data-stu-id="046d4-124">108</span></span>|<span data-ttu-id="046d4-125">AVDELNING</span><span class="sxs-lookup"><span data-stu-id="046d4-125">DEPARTMENT</span></span>|<span data-ttu-id="046d4-126">FÖRSÄLJNING</span><span class="sxs-lookup"><span data-stu-id="046d4-126">SALES</span></span>|<span data-ttu-id="046d4-127">FÖRS</span><span class="sxs-lookup"><span data-stu-id="046d4-127">Sales</span></span>|  
  
## <a name="dimension-set-entries"></a><span data-ttu-id="046d4-128">Dimensionsuppsättningstrans.</span><span class="sxs-lookup"><span data-stu-id="046d4-128">Dimension Set Entries</span></span>  
<span data-ttu-id="046d4-129">Dimensionsuppsättningar lagras i tabellen **Dimensionsuppsättnings transaktion** som dimensionsuppsättningstransaktioner med samma dimensionsuppsättnings-ID.</span><span class="sxs-lookup"><span data-stu-id="046d4-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  
  
<span data-ttu-id="046d4-130">![Dimension – översikt](media/dimensionentrynav7.png "DimensionEntryNAV7")</span><span class="sxs-lookup"><span data-stu-id="046d4-130">![Dimension Entry overview](media/dimensionentrynav7.png "DimensionEntryNAV7")</span></span>  
  
<span data-ttu-id="046d4-131">När du skapar en ny journalrad, dokumenthuvud eller dokumentrad kan du ange en kombination av dimensionsvärden.</span><span class="sxs-lookup"><span data-stu-id="046d4-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="046d4-132">I stället för att uttryckligen lagra varje dimensionsvärde i databasen tilldelas ett dimensionsuppsättnings-ID till journalraden, dokumenthuvudet eller dokumentraden för att specificera dimensionsuppsättningen.</span><span class="sxs-lookup"><span data-stu-id="046d4-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  
  
<span data-ttu-id="046d4-133">När du redigerar och stänger fönstret **Redigera dimensionsuppsättningstrans.**utförs en kontroll för att se om kombinationen av dimensionsvärden finns som en dimensionsuppsättning i tabellen.</span><span class="sxs-lookup"><span data-stu-id="046d4-133">When you edit and close the **Edit Dimension Set Entries** window, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="046d4-134">Om kombinationen finns i tabellen tilldelas motsvarande dimensionsuppsättnings-ID till journalraden, dokumenthuvudet eller dokumentraden.</span><span class="sxs-lookup"><span data-stu-id="046d4-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="046d4-135">Annars läggs en ny dimensionsuppsättning till tabellen och det nya dimensionsuppsättnings-ID:t tilldelats journalraden, dokumenthuvudet eller dokumentraden.</span><span class="sxs-lookup"><span data-stu-id="046d4-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>  
  
## <a name="performance-improvement"></a><span data-ttu-id="046d4-136">Prestandaförbättring</span><span class="sxs-lookup"><span data-stu-id="046d4-136">Performance Improvement</span></span>  
<span data-ttu-id="046d4-137">Genom att lagra dimensionsuppsättningar en gång i databasen bevaras databasplats och allmänna prestanda förbättras.</span><span class="sxs-lookup"><span data-stu-id="046d4-137">By storing dimension sets once in the database, database space is preserved, and overall performance is improved.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="046d4-138">Se även</span><span class="sxs-lookup"><span data-stu-id="046d4-138">See Also</span></span>  
<span data-ttu-id="046d4-139">[Designdetaljer: Söka efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="046d4-139">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="046d4-140">[Designdetaljer: Tabellstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="046d4-140">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
<span data-ttu-id="046d4-141">[Designdetaljer: Kodenhet 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="046d4-141">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
<span data-ttu-id="046d4-142">[Designdetaljer: Kodexempel på ändrade mönster i ändringar](design-details-code-examples-of-changed-patterns-in-modifications.md) </span><span class="sxs-lookup"><span data-stu-id="046d4-142">[Design Details: Code Examples of Changed Patterns in Modifications](design-details-code-examples-of-changed-patterns-in-modifications.md) </span></span>  
[<span data-ttu-id="046d4-143">Designdetaljer: Dimensionsuppsättningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="046d4-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   

