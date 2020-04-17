---
title: Designdetaljer - Bokföring av rad i redovisningsjournalen | Microsoft Docs
description: Detta avsnitt ger en inblick i de koncept och principer som används för att omdesigna funktionen för bokföring av rader i redovisningsjournalen i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1a8654b53dec476b175101a4d9c08f15ab3d6d6f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185378"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="badd2-103">Designdetaljer: Bokföring av rad i redovisningsjournalen</span><span class="sxs-lookup"><span data-stu-id="badd2-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="badd2-104">Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna som används för att designa om funktionen för bokföring av rader i redovisningsjournalen i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="badd2-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="badd2-105">Revideringen gör kodmodul 12 enklare och mer stabil.</span><span class="sxs-lookup"><span data-stu-id="badd2-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="badd2-106">Dokumentationen börjar med att beskriva begreppsmässiga översikter av revideringen.</span><span class="sxs-lookup"><span data-stu-id="badd2-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="badd2-107">Sedan förklaras den tekniska arkitekturen för att visa de ändringar som revideringen medför.</span><span class="sxs-lookup"><span data-stu-id="badd2-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="badd2-108">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="badd2-108">In This Section</span></span>  
[<span data-ttu-id="badd2-109">Översikt över bokföring av rad i redovisningsjournalen</span><span class="sxs-lookup"><span data-stu-id="badd2-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="badd2-110">Designdetaljer: Bokföringsgränssnittsstruktur</span><span class="sxs-lookup"><span data-stu-id="badd2-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="badd2-111">Designdetaljer: Bokföringsmotorstruktur</span><span class="sxs-lookup"><span data-stu-id="badd2-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="badd2-112">Ändringar i kodmodul 12: Mappa globala variabler för bokföring av rad i redovisningsjournalen</span><span class="sxs-lookup"><span data-stu-id="badd2-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="badd2-113">Ändringar i kodmodul 12: ändringar i bokföringsprocedurer i redovisningsjournalen</span><span class="sxs-lookup"><span data-stu-id="badd2-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="badd2-114">Se även</span><span class="sxs-lookup"><span data-stu-id="badd2-114">See Also</span></span>  
[<span data-ttu-id="badd2-115">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="badd2-115">Working with General Journals</span></span>](ui-work-general-journals.md)
