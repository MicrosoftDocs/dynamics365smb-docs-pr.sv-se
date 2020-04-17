---
title: Inspektera sidor i Business Central
description: Använd funktionen sidinspektion för att zooma in detaljer om sidans design och datakälla. Sidinspektören är perfekt för att felsöka problem med dina data.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
author: jswymer
ms.date: 04/01/2020
ms.openlocfilehash: 7790548828595838e6c2f626194d59260ef4e8ab
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187778"
---
# <a name="inspecting-pages-in-business-central"></a><span data-ttu-id="dafa2-104">Inspektera sidor i Business Central</span><span class="sxs-lookup"><span data-stu-id="dafa2-104">Inspecting Pages in Business Central</span></span>

<span data-ttu-id="dafa2-105">Funktionen för sidinspektion låter dig hämta information om en sida, ge insikt i sidans design, de olika element som utgör grunden för sidan och källan för de data som visas.</span><span class="sxs-lookup"><span data-stu-id="dafa2-105">The page inspection feature enables you to get details about a page, providing insight into the page design, the different elements that comprise the page, and the source behind the data it displays.</span></span> <span data-ttu-id="dafa2-106">Sidinspektion är särskilt utformad för administratörer, privilegierade användare, supportpersonal och utvecklare.</span><span class="sxs-lookup"><span data-stu-id="dafa2-106">Page inspection is especially designed for administrators, power users, support personnel, and developers.</span></span> <span data-ttu-id="dafa2-107">Den är perfekt för att lära sig datamodellen bakom en sida och felsökning.</span><span class="sxs-lookup"><span data-stu-id="dafa2-107">It is ideal for learning the data model behind a page and troubleshooting.</span></span> <span data-ttu-id="dafa2-108">Om det till exempel uppstår problem med en sida, kan du använda granskning på sidan för att hämta information som vidarebefordras till systemadministratören eller supportpersonal.</span><span class="sxs-lookup"><span data-stu-id="dafa2-108">For example, if you are experiencing a problem with a page, you could use page inspection to get information to pass on to your system administrator or support personnel.</span></span>

## <a name="working-with-page-inspection"></a><span data-ttu-id="dafa2-109">Arbeta med sidinspektion</span><span class="sxs-lookup"><span data-stu-id="dafa2-109">Working with Page Inspection</span></span>

<span data-ttu-id="dafa2-110">Du startar sidgranskning från sidan **hjälp och support**.</span><span class="sxs-lookup"><span data-stu-id="dafa2-110">You start page inspection from the **Help & Support** page.</span></span> <span data-ttu-id="dafa2-111">Välj frågetecknet i övre högra hörnet, välj **hjälp och support** och välj **Kontrollera sidor och data**.</span><span class="sxs-lookup"><span data-stu-id="dafa2-111">Choose the question mark in the top right corner, choose **Help & Support**, and then choose **Inspect pages and data**.</span></span> <span data-ttu-id="dafa2-112">Du kan bara använda kortkommandot **Ctrl + Alt + F1**.</span><span class="sxs-lookup"><span data-stu-id="dafa2-112">Or, you can just use the keyboard shortcut **Ctrl+Alt+F1**.</span></span>

<span data-ttu-id="dafa2-113">Rutan **sidinspektion** visas på sidan.</span><span class="sxs-lookup"><span data-stu-id="dafa2-113">The **Page inspection** pane opens on the side.</span></span> <span data-ttu-id="dafa2-114">I följande figur visas rutan **Sidinspektion** på sidan **försäljningsorder**.</span><span class="sxs-lookup"><span data-stu-id="dafa2-114">The following figure illustrates the **Page Inspection** pane on the **Sales Order** page.</span></span>

![Sidinspektion](media/page-inspection-example.png)

<span data-ttu-id="dafa2-116">När rutan **Sidinspektion** först öppnats, visas information som tillhör objektet på huvudsidan.</span><span class="sxs-lookup"><span data-stu-id="dafa2-116">When the **Page Inspection** pane first opens, it shows information that pertains to the main page object.</span></span>

<span data-ttu-id="dafa2-117">Använd tangentbord eller pekdon för att flytta markeringen till olika element på sidan.</span><span class="sxs-lookup"><span data-stu-id="dafa2-117">Use the keyboard or pointing device to move focus to different elements on the page.</span></span> <span data-ttu-id="dafa2-118">När du väljer en faktabox eller en del av huvudsidan markeras markeringsområdet med en ram och rutan **Sidinspektion** visar information om det valda elementet.</span><span class="sxs-lookup"><span data-stu-id="dafa2-118">When you select a FactBox or a part on the main page, the bounding area is highlighted by a border, and the **Page Inspection** pane shows information about the selected element.</span></span> <span data-ttu-id="dafa2-119">Till exempel föregående bild visar information om listan som en del på sidan **försäljningsorder**.</span><span class="sxs-lookup"><span data-stu-id="dafa2-119">For example, the previous figure shows information about the list part in the **Sales Order** page.</span></span> <span data-ttu-id="dafa2-120">När du navigerar mellan sidorna i programmet kommer rutan **Sidinspektion** att uppdateras automatiskt med sidinformation allt eftersom.</span><span class="sxs-lookup"><span data-stu-id="dafa2-120">As you navigate to other pages in the application, the **Page Inspection** pane will automatically update with page information as you move along.</span></span>

<span data-ttu-id="dafa2-121">För mer information om vad som ska visas i sidisnpektionen, se [Inspektera och felsöka sidor](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) i hjälpavsnittet för Business Central-utvecklare och IT-proffs.</span><span class="sxs-lookup"><span data-stu-id="dafa2-121">For more information about what is shown in page inspection, see [Inspecting and Troubleshooting Pages](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) in the Business Central Developer and IT Pro help.</span></span>

<span data-ttu-id="dafa2-122">Om du inte kan se de information som borde finnas i rutan **Sidinspektion** har du förmodligen inte behörighet, som beskrivs i nästa avsnitt.</span><span class="sxs-lookup"><span data-stu-id="dafa2-122">If you do not see the details that you expect to see in the **Page Inspection** pane, you probably do not have the required permissions, as described in the next section.</span></span>

## <a name="controlling-access-to-page-inspection-details"></a><span data-ttu-id="dafa2-123">Kontrollera åtkomst till information om sidinspektion</span><span class="sxs-lookup"><span data-stu-id="dafa2-123">Controlling Access to Page Inspection Details</span></span>

<span data-ttu-id="dafa2-124">Som administratör kan du styra åtkomsten till alla detaljer som visas i rutan **Sidinspektion** genom att konfigurera de behörigheter som användaren har.</span><span class="sxs-lookup"><span data-stu-id="dafa2-124">As an administrator, you can control access to the full details that are shown in the **Page Inspection** pane by configuring the permissions that users have.</span></span> <span data-ttu-id="dafa2-125">Om du vill ge en användarbehörighet till alla detaljer, ge användarna behörigheten **Utföra** i **System** objekt **5330**.</span><span class="sxs-lookup"><span data-stu-id="dafa2-125">To grant a user permission to the full details, give users **Execute** permission on the **System** object **5330**.</span></span> <span data-ttu-id="dafa2-126">Du kan bevilja behörighet med hjälp av en behörighetsuppsättning (som **felsöka D365**) eller en användargrupp (som **felsöka D365**).</span><span class="sxs-lookup"><span data-stu-id="dafa2-126">You can grant this permission by using a permission set (such as **D365 Troubleshoot**) or a user group (such as **D365 Troubleshoot**).</span></span> <span data-ttu-id="dafa2-127">Mer information om behörigheter finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="dafa2-127">For more information about permissions, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>

<span data-ttu-id="dafa2-128">Användare som inte har beviljats behörighet för **systemobjekt 5330** kan fortfarande få åtkomst till rutan **sidinspektion**, men de kommer endast att se fälten **Sida** och **Tabell** som visar grundläggande information att de kan vidarebefordra till deras supportteam.</span><span class="sxs-lookup"><span data-stu-id="dafa2-128">Users who are not granted permissions on **System object 5330** can still access the **Page Inspection** pane, but they will only see the **Page** and **Table** fields, which display basic details that they can pass on to their support team.</span></span>

## <a name="see-also"></a><span data-ttu-id="dafa2-129">Se även</span><span class="sxs-lookup"><span data-stu-id="dafa2-129">See Also</span></span>

<span data-ttu-id="dafa2-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dafa2-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
