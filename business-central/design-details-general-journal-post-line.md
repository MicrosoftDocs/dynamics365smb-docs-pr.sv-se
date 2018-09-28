---
title: "Designdetaljer - Bokföring av rad i redovisningsjournalen | Microsoft Docs"
description: "Detta avsnitt ger en inblick i de koncept och principer som används för att omdesigna funktionen för bokföring av rader i redovisningsjournalen i Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 24df541a8f1d1cf5df3f53a00922ae0d88d7192f
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="b6de3-103">Designdetaljer: Bokföring av rad i redovisningsjournalen</span><span class="sxs-lookup"><span data-stu-id="b6de3-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="b6de3-104">Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna som används för att designa om funktionen för bokföring av rader i redovisningsjournalen i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b6de3-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="b6de3-105">Revideringen gör kodmodul 12 enklare och mer stabil.</span><span class="sxs-lookup"><span data-stu-id="b6de3-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="b6de3-106">Dokumentationen börjar med att beskriva begreppsmässiga översikter av revideringen.</span><span class="sxs-lookup"><span data-stu-id="b6de3-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="b6de3-107">Sedan förklaras den tekniska arkitekturen för att visa de ändringar som revideringen medför.</span><span class="sxs-lookup"><span data-stu-id="b6de3-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="b6de3-108">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="b6de3-108">In This Section</span></span>  
[<span data-ttu-id="b6de3-109">Översikt över bokföring av rad i redovisningsjournalen</span><span class="sxs-lookup"><span data-stu-id="b6de3-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="b6de3-110">Designdetaljer: Bokföringsgränssnittsstruktur</span><span class="sxs-lookup"><span data-stu-id="b6de3-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="b6de3-111">Designdetaljer: Bokföringsmotorstruktur</span><span class="sxs-lookup"><span data-stu-id="b6de3-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="b6de3-112">Ändringar i kodmodul 12: Mappa globala variabler för bokföring av rad i redovisningsjournalen</span><span class="sxs-lookup"><span data-stu-id="b6de3-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="b6de3-113">Ändringar i kodmodul 12: ändringar i bokföringsprocedurer i redovisningsjournalen</span><span class="sxs-lookup"><span data-stu-id="b6de3-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="b6de3-114">Se även</span><span class="sxs-lookup"><span data-stu-id="b6de3-114">See Also</span></span>  
[<span data-ttu-id="b6de3-115">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="b6de3-115">Working with General Journals</span></span>](ui-work-general-journals.md)

