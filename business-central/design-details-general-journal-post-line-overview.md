---
title: Översikt över bokföring av rad i redovisningsjournalen | Microsoft Docs
description: Detta avsnitt introducerar ändringar i Kodmodul 12, **Gen. Jnl.-Post Line**, som utgör det huvudsakliga programobjektet för redovisningstransaktioner och är den enda plats där transaktioner för redovisning, moms samt kund- och leverantörsreskontra kan föras in.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1f6060eb7672b332fb570eb13fe027a3b58e6594
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215259"
---
# <a name="general-journal-post-line-overview"></a><span data-ttu-id="374c5-103">Översikt över bokföring av rad i redovisningsjournalen</span><span class="sxs-lookup"><span data-stu-id="374c5-103">General Journal Post Line Overview</span></span>

<span data-ttu-id="374c5-104">Kodmodul 12, **Redovisningsjnl – bokför rad**, är det större programobjektet för redovisningsbokföring och är den enda plats där redovisning, moms, kund- och leverantörsreskontraposter kan infogas.</span><span class="sxs-lookup"><span data-stu-id="374c5-104">Codeunit 12, **Gen. Jnl.-Post Line**, is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.</span></span> <span data-ttu-id="374c5-105">Den här kodmodulen används även för alla operationer av typen Verkställ, Ta bort och Återför.</span><span class="sxs-lookup"><span data-stu-id="374c5-105">This codeunit is also used for all Apply, Unapply and Reverse operations.</span></span>  
  
<span data-ttu-id="374c5-106">I Microsoft Dynamics NAV 2013 R2 har kodmodulen skapats på grund av att den hade blivit mycket stor, med cirka 7 600 kodrader.</span><span class="sxs-lookup"><span data-stu-id="374c5-106">In Microsoft Dynamics NAV 2013 R2, the codeunit was redesigned because it had become very large, with approximately 7,600 code lines.</span></span> <span data-ttu-id="374c5-107">Arkitekturen ändrades och kodmodulen har gjorts enklare och mer stabil.</span><span class="sxs-lookup"><span data-stu-id="374c5-107">The architecture was changed and the codeunit has been made simpler and more maintainable.</span></span> <span data-ttu-id="374c5-108">Denna dokumentation beskriver ändringarna och tillhandahåller information som du kanske behöver för en uppgradering.</span><span class="sxs-lookup"><span data-stu-id="374c5-108">This documentation describes the changes and provides information that you will need for upgrade.</span></span>  
  
## <a name="old-architecture"></a><span data-ttu-id="374c5-109">Gammal arkitektur</span><span class="sxs-lookup"><span data-stu-id="374c5-109">Old Architecture</span></span>  
<span data-ttu-id="374c5-110">Den gamla arkitekturen hade följande funktioner:</span><span class="sxs-lookup"><span data-stu-id="374c5-110">The old architecture had the following features:</span></span>  
  
* <span data-ttu-id="374c5-111">Tidigare använder globala variabler i stor utsträckning, vilket ökade risken för dolda fel på grund av variabler med fel omfång.</span><span class="sxs-lookup"><span data-stu-id="374c5-111">There was extensive use of global variables, which increased the possibility of hidden errors due to use of variables with the wrong scope.</span></span>  
* <span data-ttu-id="374c5-112">Många långa procedurer (med mer än 100 kodrader) som även hade hög cyklomatisk komplexitet (t. ex. många kapslade instruktioner som CASE, REPEAT och IF) användes, vilket gjorde koden mycket svår att läsa och underhålla.</span><span class="sxs-lookup"><span data-stu-id="374c5-112">There were many long procedures (with more than 100 code lines) that also had high cyclomatic complexity (that is, a lot of CASE, REPEAT, IF nested statements), which made the code very difficult to read and maintain.</span></span>  
* <span data-ttu-id="374c5-113">Flera procedurer som endast användes lokalt och endast var avsedda att användas lokalt var inte markerade som lokala.</span><span class="sxs-lookup"><span data-stu-id="374c5-113">Several procedures that were only used locally and were only meant to be used locally were not marked as local.</span></span>  
* <span data-ttu-id="374c5-114">De flesta procedurer hade inga parametrar och använde globala variabler.</span><span class="sxs-lookup"><span data-stu-id="374c5-114">Most procedures had no parameters and used global variables.</span></span> <span data-ttu-id="374c5-115">Vissa använda parametrar och åsidosatta globala variabler med lokaler.</span><span class="sxs-lookup"><span data-stu-id="374c5-115">Some used parameters and overrode global variables with locals.</span></span>  
* <span data-ttu-id="374c5-116">Kodmönster för sökning av redovisningskonton och skapande av redovisnings- och momstransaktioner standardiserades inte och varierade mellan olika platser.</span><span class="sxs-lookup"><span data-stu-id="374c5-116">Code patterns for searching the general ledger accounts and creating general ledger and VAT entries was not standardized and varied from place to place.</span></span> <span data-ttu-id="374c5-117">Det fanns dessutom mycket koddubbletter och bruten symmetri mellan kund- och leverantörskoden.</span><span class="sxs-lookup"><span data-stu-id="374c5-117">In addition, there was a lot of code duplication and broken symmetry between customer and vendor code.</span></span>  
* <span data-ttu-id="374c5-118">En stor del av koden i kodmodul 12, ungefär 30 procent, är relaterad till kassarabatt och toleransberäkningar även om dessa funktioner inte behövs i många eller länder/regioner.</span><span class="sxs-lookup"><span data-stu-id="374c5-118">A large part of the code in codeunit 12, approximately 30 percent, related to payment discount and tolerance calculations, although these features are not needed in many countries or regions.</span></span>  
* <span data-ttu-id="374c5-119">Bokföring, Koppla, Ta bort, Återför, Kassarabatt och Tolerans samt Valutakursjustering har sammanförts i kodmodul 12 med hjälp av en lång lista över globala variabler.</span><span class="sxs-lookup"><span data-stu-id="374c5-119">Posting, Apply, Unapply, Reverse, Payment Discount and Tolerance, and Exchange Rate Adjustment were married together in codeunit 12 using a long list of global variables.</span></span>  
  
### <a name="new-architecture"></a><span data-ttu-id="374c5-120">Ny arkitektur</span><span class="sxs-lookup"><span data-stu-id="374c5-120">New Architecture</span></span>  
<span data-ttu-id="374c5-121">Kodmodul 12 i [!INCLUDE[prod_short](includes/prod_short.md)] innehåller följande förbättringar:</span><span class="sxs-lookup"><span data-stu-id="374c5-121">In [!INCLUDE[prod_short](includes/prod_short.md)], codeunit 12 has had the following improvements:</span></span>  
  
* <span data-ttu-id="374c5-122">Kodmodul 12 har omstrukturerats till mindre procedurer (alla mindre än 100 kodrader).</span><span class="sxs-lookup"><span data-stu-id="374c5-122">Codeunit 12 has been refactored into smaller procedures (all less than 100 code lines).</span></span>  
* <span data-ttu-id="374c5-123">Standardiserade mönster för sökning efter redovisningskonton har implementeras genom att använda hjälpfunktioner från bokföringsmalltabeller.</span><span class="sxs-lookup"><span data-stu-id="374c5-123">Standardized patterns for the search of general ledger accounts have been implemented by using helper functions from Posting Group tables.</span></span>  
* <span data-ttu-id="374c5-124">Ett bokföringsmotorramverk har implementerats för att hantera start och avslutande av transaktioner och för att isolera skapandet i redovisningen och momstransaktioner, insamlingen av momsjustering och beräkningen av ytterligare valutabelopp.</span><span class="sxs-lookup"><span data-stu-id="374c5-124">A Posting Engine Framework has been implemented to manage the start and finish of transactions and to isolate the creation to general ledger and VAT entries, the collection of VAT adjustment, and the calculation of additional currency amounts.</span></span>  
* <span data-ttu-id="374c5-125">Kodduplicering har eliminerats.</span><span class="sxs-lookup"><span data-stu-id="374c5-125">Code duplication has been eliminated.</span></span>  
* <span data-ttu-id="374c5-126">Många hjälpfunktioner har överförts till motsvarande transaktionstabeller för kund- och leverantörsreskontra.</span><span class="sxs-lookup"><span data-stu-id="374c5-126">Many helper functions have been transferred to corresponding customer and vendor ledger entry tables.</span></span>  
* <span data-ttu-id="374c5-127">Användningen av globala variabler har minimerats så att varje procedur använder parametrar och kapslar in sin programlogik.</span><span class="sxs-lookup"><span data-stu-id="374c5-127">The use of global variables has been minimized, so that each procedure uses parameters and encapsulates its own application logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="374c5-128">Se även</span><span class="sxs-lookup"><span data-stu-id="374c5-128">See Also</span></span>

[<span data-ttu-id="374c5-129">Designdetaljer: Bokföringsgränssnittsstruktur</span><span class="sxs-lookup"><span data-stu-id="374c5-129">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="374c5-130">Designdetaljer: Bokföringsmotorstruktur</span><span class="sxs-lookup"><span data-stu-id="374c5-130">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="374c5-131">Designdetaljer: redovisningsjournalrad (Dynamics NAV)</span><span class="sxs-lookup"><span data-stu-id="374c5-131">Design Details: General Journal Post Line (Dynamics NAV)</span></span>](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]