---
title: Designdetaljer – Bokföring av rad i redovisningsjournalen | Microsoft Docs
description: Detta avsnitt ger en inblick i de koncept och principer som används för att omdesigna funktionen för bokföring av rader i redovisningsjournalen i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8492c83437be4cd850bafdaaa5dc70d00a075674
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215234"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="0f032-103">Designdetaljer: Bokföring av rad i redovisningsjournalen</span><span class="sxs-lookup"><span data-stu-id="0f032-103">Design Details: General Journal Post Line</span></span>

<span data-ttu-id="0f032-104">Dokumentationen ger en detaljerad teknisk inblick i begreppen och principerna som används för att designa om funktionen för bokföring av rader i redovisningsjournalen i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="0f032-104">This documentation provides detailed technical insight into the concepts and principles that were used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="0f032-105">Revideringen gör kodmodul 12 enklare och mer stabil.</span><span class="sxs-lookup"><span data-stu-id="0f032-105">The redesign made codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="0f032-106">Dokumentationen börjar med att beskriva begreppsmässiga översikter av revideringen.</span><span class="sxs-lookup"><span data-stu-id="0f032-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="0f032-107">Sedan förklaras den tekniska arkitekturen för att visa de ändringar som revideringen medför.</span><span class="sxs-lookup"><span data-stu-id="0f032-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="0f032-108">Informationen i det här avsnittet gäller omutformande i en tidigare version av produkten, Microsoft Dynamics NAV 2013 R2.</span><span class="sxs-lookup"><span data-stu-id="0f032-108">The information in this section applies to the redesign in an earlier version of the product, Microsoft Dynamics NAV 2013 R2.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0f032-109">I det här avsnittet</span><span class="sxs-lookup"><span data-stu-id="0f032-109">In This Section</span></span>

[<span data-ttu-id="0f032-110">Översikt över bokföring av rad i redovisningsjournalen</span><span class="sxs-lookup"><span data-stu-id="0f032-110">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="0f032-111">Designdetaljer: Bokföringsgränssnittsstruktur</span><span class="sxs-lookup"><span data-stu-id="0f032-111">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="0f032-112">Designdetaljer: Bokföringsmotorstruktur</span><span class="sxs-lookup"><span data-stu-id="0f032-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  

## <a name="see-also"></a><span data-ttu-id="0f032-113">Se även</span><span class="sxs-lookup"><span data-stu-id="0f032-113">See Also</span></span>

<span data-ttu-id="0f032-114">[Arbeta med redovisningsjournaler](ui-work-general-journals.md)
[Designdetaljer: redovisningsjournalrad (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span><span class="sxs-lookup"><span data-stu-id="0f032-114">[Working with General Journals](ui-work-general-journals.md)
[Design Details: General Journal Post Line (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]