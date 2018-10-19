---
title: "Spåra användaraktivitetet i en ändringslogg | Microsoft Docs"
description: "Du kan aktivera en användarlogg så att du har en historik över alla ändringar som gjorts i spårade tabeller."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ab9696a3cc14970def764b2741d50dbcd5207460
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="logging-changes-in-business-central"></a><span data-ttu-id="915cc-103">Logga ändringar i Business Central</span><span class="sxs-lookup"><span data-stu-id="915cc-103">Logging Changes in Business Central</span></span>
<span data-ttu-id="915cc-104">Du kan aktivera ändringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)] så att du får en historik över aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="915cc-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="915cc-105">Loggen är baserad på ändringar av data i tabeller som du spårar. I ändringsloggen sorteras poster kronologiskt och visar de ändringar som har gjorts i fälten i de angivna posterna.</span><span class="sxs-lookup"><span data-stu-id="915cc-105">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="915cc-106">I ändringsloggen samlas alla ändringar som gjorts i tabellen.</span><span class="sxs-lookup"><span data-stu-id="915cc-106">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="915cc-107">Arbeta med ändringsloggen</span><span class="sxs-lookup"><span data-stu-id="915cc-107">Working with the Change Log</span></span>
<span data-ttu-id="915cc-108">Ett vanligt problem i många ekonomisystem är att ta reda på var fel och ändringar av data har sina ursprung.</span><span class="sxs-lookup"><span data-stu-id="915cc-108">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="915cc-109">Det kan vara allt från ett felaktigt kundtelefonnummer till en felaktig bokföring i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="915cc-109">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="915cc-110">Med ändringsloggen kan du spåra alla direkta ändringar som användare gör av data i databasen.</span><span class="sxs-lookup"><span data-stu-id="915cc-110">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="915cc-111">Du måste ange vad du vill att systemet ska logga för varje tabell och fält och därefter måste du aktivera ändringsloggen.</span><span class="sxs-lookup"><span data-stu-id="915cc-111">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="915cc-112">Du aktiverar och avaktiverar ändringsloggen i fönstret **Ändringslogg inställning**.</span><span class="sxs-lookup"><span data-stu-id="915cc-112">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="915cc-113">Du kan aktivera eller inaktivera ändringsloggen, denna aktivitet loggas så du kan alltid se vilken användare som har inaktiverat respektive återaktiverat ändringsloggen.</span><span class="sxs-lookup"><span data-stu-id="915cc-113">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="915cc-114">Denna loggningsfunktion går inte att stänga av.</span><span class="sxs-lookup"><span data-stu-id="915cc-114">This cannot be turned off.</span></span>  

<span data-ttu-id="915cc-115">I fönstret **Ändringslogginställningar** om du väljer åtgärden **Tabeller** kan du ange vilka tabeller som du vill spåra ändringar för och vilka ändringar som ska spåras. [!INCLUDE[d365fin](includes/d365fin_md.md)] spårar även nummer av systemtabeller.</span><span class="sxs-lookup"><span data-stu-id="915cc-115">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="915cc-116">När du har skapat ändringsloggen och aktiverat den, och gjort en ändring av data, kan du visa och filtrera ändringen i fönstret **Ändringslogg transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="915cc-116">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="915cc-117">Om du vill ta bort transaktioner kan du göra det i fönstret **ta bort ändringsloggtransaktioner**, där du kan ange filter baserat på datum och tider.</span><span class="sxs-lookup"><span data-stu-id="915cc-117">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="915cc-118">Se även</span><span class="sxs-lookup"><span data-stu-id="915cc-118">See Also</span></span>
[<span data-ttu-id="915cc-119">Ändra grundinställningar</span><span class="sxs-lookup"><span data-stu-id="915cc-119">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="915cc-120">Sortering</span><span class="sxs-lookup"><span data-stu-id="915cc-120">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="915cc-121">Använda Söka efter sida eller rapport</span><span class="sxs-lookup"><span data-stu-id="915cc-121">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="915cc-122">[Hantera användare och behörigheter](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="915cc-122">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="915cc-123">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="915cc-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

