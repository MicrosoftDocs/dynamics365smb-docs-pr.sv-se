---
title: Tilldela och hantera uppgifter | Microsoft Docs
description: "Lär dig hur du tilldelar uppgifter till användare, till exempel en beräkning i Dynamics 365 Business edition"
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 08/24/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 520c0b169eb9c5f24cbf8b42096c731d77acd7de
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---
# <a name="defining-user-tasks"></a><span data-ttu-id="30aa1-103">Definiera användaruppgifter</span><span class="sxs-lookup"><span data-stu-id="30aa1-103">Defining User Tasks</span></span>
<span data-ttu-id="30aa1-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du skapa uppgifter som påminner dig om arbetet som ska utföras.</span><span class="sxs-lookup"><span data-stu-id="30aa1-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], you can create tasks to remind you of work to be done.</span></span> <span data-ttu-id="30aa1-105">Du kan skapa uppgifter åt dig själv, men du kan också tilldela uppgifter till andra eller tilldela en uppgift för någon annan i organisationen.</span><span class="sxs-lookup"><span data-stu-id="30aa1-105">You can create tasks for yourself, but you can also assign tasks to others or be assigned a task by someone else in your organization.</span></span>  

## <a name="managing-user-tasks"></a><span data-ttu-id="30aa1-106">Hantera användaruppgifter</span><span class="sxs-lookup"><span data-stu-id="30aa1-106">Managing User Tasks</span></span>
<span data-ttu-id="30aa1-107">FÖnstret **användaruppgifter** visar alla uppgifter och du kan enkelt skapa och tilldela nya uppgifter.</span><span class="sxs-lookup"><span data-stu-id="30aa1-107">The **User Tasks** window shows all tasks, and you can easily create and assign new tasks.</span></span> <span data-ttu-id="30aa1-108">När du skapar en uppgift kan du ange start- och förfallodatum och du kan lägga till en länk till fönstret i [!INCLUDE[d365fin](includes/d365fin_md.md)] där användaren måste göra arbetet.</span><span class="sxs-lookup"><span data-stu-id="30aa1-108">When you create a task, you can specify the start date and due date, and you can add a link to the window in [!INCLUDE[d365fin](includes/d365fin_md.md)] where the user must do the work.</span></span>  

<span data-ttu-id="30aa1-109">Du kan till exempel skapa en uppgift för dig själv för att visa alla bokförda försäljningsfakturor.</span><span class="sxs-lookup"><span data-stu-id="30aa1-109">For example, you can create a task for yourself to view all posted sales invoices.</span></span> <span data-ttu-id="30aa1-110">Om så är fallet kan du länka uppgiften till sidan 143, bokförda försäljningsfakturor.</span><span class="sxs-lookup"><span data-stu-id="30aa1-110">In that case, you link the task to page 143, Posted Sales Invoices.</span></span>  

<span data-ttu-id="30aa1-111">![Exempel på en användaruppgift](media/across-user-tasks/sample-user-task.png "exempel på en användaruppgift")</span><span class="sxs-lookup"><span data-stu-id="30aa1-111">![Example of a User Task](media/across-user-tasks/sample-user-task.png "Example of a user task")</span></span>

> [!TIP]  
>  <span data-ttu-id="30aa1-112">Använd sökfunktionen i fältet **Sida** fält och använd fältet **Sök efter sidan eller rapporten** för att hitta sidan du vill ha.</span><span class="sxs-lookup"><span data-stu-id="30aa1-112">Use the look-up in the **Page** field and then use the **Search for Page or Report** field to find the page that you want.</span></span> <span data-ttu-id="30aa1-113">Mer information finns i [söka efter en sida eller rapport](ui-search.md).</span><span class="sxs-lookup"><span data-stu-id="30aa1-113">For more information, see [Searching for a Page or Report](ui-search.md).</span></span>  

### <a name="picking-up-user-tasks"></a><span data-ttu-id="30aa1-114">Plocka upp användaruppgifter</span><span class="sxs-lookup"><span data-stu-id="30aa1-114">Picking Up User Tasks</span></span>
<span data-ttu-id="30aa1-115">I chef, bokföringsansvarig och rollcenter för redovisare visar en panel pågående uppgifter som har tilldelats den användaren.</span><span class="sxs-lookup"><span data-stu-id="30aa1-115">In the Business Manager, Bookkeeper, and Accountant Role Centers, a tile shows pending tasks that are assigned to that user.</span></span> <span data-ttu-id="30aa1-116">Om du vill välja en uppgift, väljer du den bara från listan över väntande användaruppgifter.</span><span class="sxs-lookup"><span data-stu-id="30aa1-116">To pick up a task, simply choose it from the list of pending user tasks.</span></span> <span data-ttu-id="30aa1-117">I menyfliken öppnar länken **Gå till uppgiftsobjekt** fönstret där du kan utföra arbetet.</span><span class="sxs-lookup"><span data-stu-id="30aa1-117">In the ribbon, the link **Go to Task Item** opens the window where you can do the work.</span></span>  

<span data-ttu-id="30aa1-118">När du har slutfört en uppgift bara markerar du den som slutförd.</span><span class="sxs-lookup"><span data-stu-id="30aa1-118">When you have completed a task, simply mark it as completed.</span></span>  

### <a name="deleting-user-tasks"></a><span data-ttu-id="30aa1-119">Ta bort användaruppgifter</span><span class="sxs-lookup"><span data-stu-id="30aa1-119">Deleting User Tasks</span></span>
<span data-ttu-id="30aa1-120">Om du vill ta bort flera eller vissa användaruppgifter kan du använda rapporten **ta bort aktiviteter för användare**.</span><span class="sxs-lookup"><span data-stu-id="30aa1-120">If you want to bulk delete all or some user tasks, you can use the **Delete User Tasks** report.</span></span> <span data-ttu-id="30aa1-121">På formuläret för begäran lägger du till filter för att ta reda på vilka uppgifter som måste tas bort.</span><span class="sxs-lookup"><span data-stu-id="30aa1-121">In the request page, you can set filters to determine which tasks must be deleted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="30aa1-122">Se även</span><span class="sxs-lookup"><span data-stu-id="30aa1-122">See Also</span></span>
[<span data-ttu-id="30aa1-123">Sök efter sida eller rapport</span><span class="sxs-lookup"><span data-stu-id="30aa1-123">Searching for a Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="30aa1-124">[Revisorupplevelse i [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span><span class="sxs-lookup"><span data-stu-id="30aa1-124">[Accountant Experiences in [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span></span>  

