---
title: Granskningsändringar | Microsoft Docs
description: Du kan aktivera en användarlogg så att du har en historik över alla ändringar som gjorts i spårade tabeller. Du kan även spåra aktiviteter med vissa typer av aktivitetsloggar.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 43aea054ce4e66e9108f408d96c2eb491351b382
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304942"
---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="4654a-104">Revision av ändringar i Business Central</span><span class="sxs-lookup"><span data-stu-id="4654a-104">Auditing Changes in Business Central</span></span>

<span data-ttu-id="4654a-105">Du kan aktivera ändringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)] så att du får en historik över aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="4654a-105">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="4654a-106">Loggen är baserad på ändringar av data i tabeller som du spårar. På sidan **Poster i ändringslogg** sorteras poster kronologiskt och visar de ändringar som har gjorts i fälten i de angivna posterna.</span><span class="sxs-lookup"><span data-stu-id="4654a-106">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="4654a-107">I ändringsloggen samlas alla ändringar som gjorts i tabellen.</span><span class="sxs-lookup"><span data-stu-id="4654a-107">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="4654a-108">En användares ändringar visas inte i **ändringsloggtransaktioner** förrän sessionen har startats om, vilket sker i följande fall:</span><span class="sxs-lookup"><span data-stu-id="4654a-108">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="4654a-109">Sessionen har upphört att gälla och har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="4654a-109">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="4654a-110">Användaren valde ett annat företag eller rollcenter.</span><span class="sxs-lookup"><span data-stu-id="4654a-110">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="4654a-111">Den användaren har loggat ut och in igen.</span><span class="sxs-lookup"><span data-stu-id="4654a-111">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="4654a-112">Arbeta med ändringsloggen</span><span class="sxs-lookup"><span data-stu-id="4654a-112">Working with the Change Log</span></span>

<span data-ttu-id="4654a-113">Ett vanligt problem i många ekonomisystem är att ta reda på var fel och ändringar av data har sina ursprung.</span><span class="sxs-lookup"><span data-stu-id="4654a-113">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="4654a-114">Det kan vara allt från ett felaktigt kundtelefonnummer till en felaktig bokföring i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="4654a-114">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="4654a-115">Med ändringsloggen kan du spåra alla direkta ändringar som användare gör av data i databasen.</span><span class="sxs-lookup"><span data-stu-id="4654a-115">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="4654a-116">Du måste ange vad du vill att systemet ska logga för varje tabell och fält och därefter måste du aktivera ändringsloggen.</span><span class="sxs-lookup"><span data-stu-id="4654a-116">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="4654a-117">Du aktiverar och avaktiverar ändringsloggen på sidan **Ändringslogg inställning**.</span><span class="sxs-lookup"><span data-stu-id="4654a-117">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="4654a-118">När en användare aktiverar eller inaktiverar ändringsloggen, loggas denna aktivitet så du kan alltid se vilken användare som har inaktiverat respektive återaktiverat ändringsloggen.</span><span class="sxs-lookup"><span data-stu-id="4654a-118">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="4654a-119">På sidan **Ändringslogginställningar** om du väljer åtgärden **Tabeller** kan du ange vilka tabeller som du vill spåra ändringar för och vilka ändringar som ska spåras. [!INCLUDE[d365fin](includes/d365fin_md.md)] spårar även nummer av systemtabeller.</span><span class="sxs-lookup"><span data-stu-id="4654a-119">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="4654a-120">När du har skapat ändringsloggen och aktiverat den, och gjort en ändring av data, kan du visa och filtrera ändringen på sidan **Ändringslogg transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="4654a-120">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="4654a-121">Om du vill ta bort transaktioner kan du göra det på sidan **ta bort ändringsloggtransaktioner**, där du kan ange filter baserat på datum och tider.</span><span class="sxs-lookup"><span data-stu-id="4654a-121">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="working-with-activity-logs"></a><span data-ttu-id="4654a-122">Arbeta med aktivitetsloggar</span><span class="sxs-lookup"><span data-stu-id="4654a-122">Working with Activity Logs</span></span>

<span data-ttu-id="4654a-123">På vissa sidor i [!INCLUDE [prodshort](includes/prodshort.md)] kan du visa en aktivitetslogg som visar status och eventuella fel från filer som du exporterar från eller importerar till [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="4654a-123">From some pages in [!INCLUDE [prodshort](includes/prodshort.md)], you can view an activity log that shows the status and any errors from files that you export from or import into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

<span data-ttu-id="4654a-124">Informationen visas i fönstret **Aktivitetslogg** enligt kontexten den öppnas från.</span><span class="sxs-lookup"><span data-stu-id="4654a-124">The information is displayed in the **Activity Log** page, according to the context that it is opened from.</span></span> <span data-ttu-id="4654a-125">Du kan öppna fönstret från sidan **Inställning av dokumentutbytestjänst**, **Inkommande dokument**, **Bokförd försäljningsfaktura** och **Bokförd försäljningskreditnota**.</span><span class="sxs-lookup"><span data-stu-id="4654a-125">You can open the window from the **Document Exchange Service Setup**, **Incoming Document**, **Posted Sales Invoice**, and **Posted Sales Credit Memo** pages, for example.</span></span> <span data-ttu-id="4654a-126">Du kan tömma listan över loggposter eller bara rensa listan över poster som är äldre än 7 dagar.</span><span class="sxs-lookup"><span data-stu-id="4654a-126">You can empty the list of log entries, or just clear the list of entries older than 7 days.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4654a-127">Se även</span><span class="sxs-lookup"><span data-stu-id="4654a-127">See Also</span></span>
[<span data-ttu-id="4654a-128">Ändra grundinställningar</span><span class="sxs-lookup"><span data-stu-id="4654a-128">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="4654a-129">Sortering</span><span class="sxs-lookup"><span data-stu-id="4654a-129">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="4654a-130">Söka efter sidor och information med berätta</span><span class="sxs-lookup"><span data-stu-id="4654a-130">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="4654a-131">[Hantera användare och behörigheter](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="4654a-131">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="4654a-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4654a-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
