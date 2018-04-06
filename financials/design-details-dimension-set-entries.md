---
title: "Designdetaljer - Dimensionsuppsättningstransaktioner | Microsoft Docs"
description: "Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna som används för att designa om lagrings- och bokföringsfunktioner för dimensionstransaktioner."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 17fd783bd44faa914d473aae35ddc31145c181ef
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="bd139-103">Designdetaljer: Dimensionsuppsättningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="bd139-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="bd139-104">Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna som används för att designa om lagrings- och bokföringsfunktioner för dimensionstransaktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bd139-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the dimension entry storing and posting feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="bd139-105">Dokumentationen börjar med att beskriva begreppsmässiga översikter av revideringen.</span><span class="sxs-lookup"><span data-stu-id="bd139-105">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="bd139-106">Sedan förklaras den tekniska arkitekturen för att visa hur revideringen utförs.</span><span class="sxs-lookup"><span data-stu-id="bd139-106">Then it explains the technical architecture to show how the redesign is made.</span></span> <span data-ttu-id="bd139-107">Slutligen innehåller den kodexempel för att förbereda dig för dimensionskodflyttning och uppgradering.</span><span class="sxs-lookup"><span data-stu-id="bd139-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="bd139-108">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="bd139-108">In This Section</span></span>  
[<span data-ttu-id="bd139-109">Översikt över dimensionsuppsättningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="bd139-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="bd139-110">Designdetaljer: Söka efter dimensionskombinationer</span><span class="sxs-lookup"><span data-stu-id="bd139-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="bd139-111">Designdetaljer: Tabellstruktur</span><span class="sxs-lookup"><span data-stu-id="bd139-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="bd139-112">Designdetaljer: Kodenhet 408 Dimension Management</span><span class="sxs-lookup"><span data-stu-id="bd139-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="bd139-113">Designdetaljer: Kodexempel på ändrade mönster i ändringar</span><span class="sxs-lookup"><span data-stu-id="bd139-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

