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
ms.date: 11/14/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 59afb06e9d43bdadc5ceacf563a9e6faf7439b7b
ms.openlocfilehash: bc56e07a540c24f53b88651ad2b2ff5e1e56a571
ms.contentlocale: sv-se
ms.lasthandoff: 12/05/2018

---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="8f6ef-103">Revision av ändringar i Business Central</span><span class="sxs-lookup"><span data-stu-id="8f6ef-103">Auditing Changes in Business Central</span></span>

<span data-ttu-id="8f6ef-104">Du kan aktivera ändringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)] så att du får en historik över aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="8f6ef-105">Loggen är baserad på ändringar av data i tabeller som du spårar. På sidan **Poster i ändringslogg** sorteras poster kronologiskt och visar de ändringar som har gjorts i fälten i de angivna posterna.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-105">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="8f6ef-106">I ändringsloggen samlas alla ändringar som gjorts i tabellen.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-106">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="8f6ef-107">En användares ändringar visas inte i **ändringsloggtransaktioner** förrän sessionen har startats om, vilket sker i följande fall:</span><span class="sxs-lookup"><span data-stu-id="8f6ef-107">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="8f6ef-108">Sessionen har upphört att gälla och har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-108">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="8f6ef-109">Användaren valde ett annat företag eller rollcenter.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-109">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="8f6ef-110">Den användaren har loggat ut och in igen.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-110">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="8f6ef-111">Arbeta med ändringsloggen</span><span class="sxs-lookup"><span data-stu-id="8f6ef-111">Working with the Change Log</span></span>

<span data-ttu-id="8f6ef-112">Ett vanligt problem i många ekonomisystem är att ta reda på var fel och ändringar av data har sina ursprung.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-112">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="8f6ef-113">Det kan vara allt från ett felaktigt kundtelefonnummer till en felaktig bokföring i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-113">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="8f6ef-114">Med ändringsloggen kan du spåra alla direkta ändringar som användare gör av data i databasen.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-114">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="8f6ef-115">Du måste ange vad du vill att systemet ska logga för varje tabell och fält och därefter måste du aktivera ändringsloggen.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-115">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="8f6ef-116">Du aktiverar och avaktiverar ändringsloggen på sidan **Ändringslogg inställning**.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-116">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="8f6ef-117">När en användare aktiverar eller inaktiverar ändringsloggen, loggas denna aktivitet så du kan alltid se vilken användare som har inaktiverat respektive återaktiverat ändringsloggen.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-117">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="8f6ef-118">På sidan **Ändringslogginställningar** om du väljer åtgärden **Tabeller** kan du ange vilka tabeller som du vill spåra ändringar för och vilka ändringar som ska spåras. [!INCLUDE[d365fin](includes/d365fin_md.md)] spårar även nummer av systemtabeller.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-118">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="8f6ef-119">När du har skapat ändringsloggen och aktiverat den, och gjort en ändring av data, kan du visa och filtrera ändringen på sidan **Ändringslogg transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-119">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="8f6ef-120">Om du vill ta bort transaktioner kan du göra det på sidan **ta bort ändringsloggtransaktioner**, där du kan ange filter baserat på datum och tider.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-120">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8f6ef-121">Se även</span><span class="sxs-lookup"><span data-stu-id="8f6ef-121">See Also</span></span>
[<span data-ttu-id="8f6ef-122">Ändra grundinställningar</span><span class="sxs-lookup"><span data-stu-id="8f6ef-122">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="8f6ef-123">Sortering</span><span class="sxs-lookup"><span data-stu-id="8f6ef-123">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="8f6ef-124">Använda Söka efter sida eller rapport</span><span class="sxs-lookup"><span data-stu-id="8f6ef-124">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="8f6ef-125">[Hantera användare och behörigheter](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="8f6ef-125">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="8f6ef-126">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f6ef-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

