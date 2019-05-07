---
title: Designdetaljer - Dimensionsuppsättningstransaktioner | Microsoft Docs
description: Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna som används för att designa om lagrings- och bokföringsfunktioner för dimensionstransaktioner.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c6b66ecee87e1fd128733f541d46b97f44af0453
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "935665"
---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="e4e00-103">Designdetaljer: Dimensionsuppsättningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="e4e00-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="e4e00-104">Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna för lagrings- och bokföringsfunktioner för dimensionstransaktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e4e00-104">This documentation provides detailed technical insight into the concepts and principles of the dimension-entry storing and posting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e4e00-105">Dokumentationen börjar med att beskriva begreppsmässiga översikter.</span><span class="sxs-lookup"><span data-stu-id="e4e00-105">The documentation starts by describing conceptual overviews.</span></span> <span data-ttu-id="e4e00-106">Därefter beskrivs den tekniska arkitekturen.</span><span class="sxs-lookup"><span data-stu-id="e4e00-106">Then it explains the technical architecture.</span></span> <span data-ttu-id="e4e00-107">Slutligen innehåller den kodexempel för att förbereda dig för dimensionskodflyttning och uppgradering från versioner tidigare än Dynamics NAV 2013 R2.</span><span class="sxs-lookup"><span data-stu-id="e4e00-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade from versions earlier than Dynamics NAV 2013R2.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="e4e00-108">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="e4e00-108">In This Section</span></span>  
[<span data-ttu-id="e4e00-109">Översikt över dimensionsuppsättningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="e4e00-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="e4e00-110">Designdetaljer: Söka efter dimensionskombinationer</span><span class="sxs-lookup"><span data-stu-id="e4e00-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="e4e00-111">Designdetaljer: Tabellstruktur</span><span class="sxs-lookup"><span data-stu-id="e4e00-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="e4e00-112">Designdetaljer: Kodenhet 408 Dimension Management</span><span class="sxs-lookup"><span data-stu-id="e4e00-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="e4e00-113">Designdetaljer: Kodexempel på ändrade mönster i ändringar</span><span class="sxs-lookup"><span data-stu-id="e4e00-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
