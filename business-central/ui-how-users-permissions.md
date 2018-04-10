---
title: "Tilldela eller redigera användarbehörigheter | Microsoft Docs"
description: "Beskriver hur du lägger till Office 365-användare till Business Central och tilldelar dem behörigheter, åtkomstbehörigheter och säkerhetsinställningar."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 03/16/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 6d350a064f134c4c29938005fea966dec7cca142
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="manage-users-and-permissions"></a><span data-ttu-id="32871-103">Hantera användare och behörigheter</span><span class="sxs-lookup"><span data-stu-id="32871-103">Manage Users and Permissions</span></span>
<span data-ttu-id="32871-104">Om du vill lägga till användare i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste företagets Office 365-administratör först skapa användare i Office 365 Admin Center.</span><span class="sxs-lookup"><span data-stu-id="32871-104">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)], your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="32871-105">Mer information finns i [Lägg till användare till Office 365 för företag](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)</span><span class="sxs-lookup"><span data-stu-id="32871-105">For more information, see [Add Users to Office 365 for business](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)</span></span>

<span data-ttu-id="32871-106">När användare skapas i Office 365, kan de importeras till fönstret **Användare** med åtgärden **Få användare från Office 365**.</span><span class="sxs-lookup"><span data-stu-id="32871-106">Once users are created in Office 365, they can be imported into the **Users** window by using the **Get Users from Office 365** action.</span></span> <span data-ttu-id="32871-107">Användare tilldelas behörighetsuppsättningar beroende på planen som tilldelats användaren i Office 365.</span><span class="sxs-lookup"><span data-stu-id="32871-107">Users are assigned permission sets depending on the plan assigned to the User in Office 365.</span></span>

<span data-ttu-id="32871-108">Du kan sedan tilldela behörighetsuppsättningar för användarna för att definiera vilka databasobjekt, och därmed vilka gränssnittselement, de har tillgång till och i vilka företag.</span><span class="sxs-lookup"><span data-stu-id="32871-108">You can then proceed to assign permission sets to the users to define which database objects, and thereby which UI elements, they have access to, and in which companies.</span></span> <span data-ttu-id="32871-109">Du kan lägga till användare i användargrupper.</span><span class="sxs-lookup"><span data-stu-id="32871-109">You can add users to user groups.</span></span> <span data-ttu-id="32871-110">Detta gör det enklare att tilldela samma behörighetsuppsättning till flera användare.</span><span class="sxs-lookup"><span data-stu-id="32871-110">This makes it easier to assign the same permission sets to multiple users.</span></span>

<span data-ttu-id="32871-111">En behörighetsuppsättning är en samling behörigheter för specifika objekt i databasen.</span><span class="sxs-lookup"><span data-stu-id="32871-111">A permission set is a collection of permissions for specific objects in the database.</span></span> <span data-ttu-id="32871-112">Alla användare måste tilldelas en eller flera behörighetsuppsättningar innan de får tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="32871-112">All users must be assigned one or more permission sets before they can access [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="32871-113">Flera fördefinierade behörighetsuppsättningar levereras som standard.</span><span class="sxs-lookup"><span data-stu-id="32871-113">A number of predefined permission sets are provided by default.</span></span> <span data-ttu-id="32871-114">Du kan använda dessa behörighetsuppsättningar som redan har definierats, ändra standardbehörighetsuppsättningarna eller skapa ytterligare behörighetsuppsättningar.</span><span class="sxs-lookup"><span data-stu-id="32871-114">You can use these permission sets as already defined, modify the default permission sets, or create additional permission sets.</span></span>

<span data-ttu-id="32871-115">Administratörer kan använda fönstret **Användarinställningar** för att definiera tidsperioder som anger när användare kan bokföra och även om systemet registrerar den tidsperiod som den angivna användaren är inloggad.</span><span class="sxs-lookup"><span data-stu-id="32871-115">Administrators can use the **User Setup** window to define periods of time during which specified users are able to post, and also specify if the system logs the amount of time users are logged on.</span></span>

## <a name="to-assign-permissions-to-a-user"></a><span data-ttu-id="32871-116">Så här tilldelar du behörigheter till en användare</span><span class="sxs-lookup"><span data-stu-id="32871-116">To assign permissions to a user</span></span>
1. <span data-ttu-id="32871-117">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Användare** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="32871-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Users**, and then choose the related link.</span></span>
2. <span data-ttu-id="32871-118">Markera den användare som du vill tilldela behörighet till.</span><span class="sxs-lookup"><span data-stu-id="32871-118">Select the user that you want to assign permission to.</span></span>
<span data-ttu-id="32871-119">Eventuella behörighetsuppsättningar som redan har tilldelats till användaren visas i faktaboxen **Behörighetsuppsättningar**.</span><span class="sxs-lookup"><span data-stu-id="32871-119">Any permission sets that are already assigned to the user are displayed in the **Permission Sets** FactBox.</span></span>
3. <span data-ttu-id="32871-120">I fönstret **Inkommande dokument** väljer du åtgärden **Användarkort**.</span><span class="sxs-lookup"><span data-stu-id="32871-120">Choose the **Edit** action to open the **User Card** window.</span></span>
4. <span data-ttu-id="32871-121">På snabbfliken **Användarbehörighetsuppsättning** fyller du i fälten efter behov på en ny rad.</span><span class="sxs-lookup"><span data-stu-id="32871-121">On the **User Permission Sets** FastTab, on a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a><span data-ttu-id="32871-122">Gruppera användare i användargrupper</span><span class="sxs-lookup"><span data-stu-id="32871-122">To group users in user groups</span></span>
<span data-ttu-id="32871-123">Du kan skapa användargrupper för att hantera behörighetsuppsättningar för grupper av användare i företaget.</span><span class="sxs-lookup"><span data-stu-id="32871-123">You can set up users groups to help you manage permission sets for groups of users in your company.</span></span>

1. <span data-ttu-id="32871-124">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Användare** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="32871-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="32871-125">Alternativt kan du i fönstret **Användare** välja åtgärden **Användargrupper**.</span><span class="sxs-lookup"><span data-stu-id="32871-125">Alternatively, in the **Users** window, choose the **User Groups** action.</span></span>
3. <span data-ttu-id="32871-126">I fönstret **Användargrupp** väljer du åtgärden **Medlemmar i användargrupp**.</span><span class="sxs-lookup"><span data-stu-id="32871-126">In the **User Group** window, choose the **User Group Members** action.</span></span>
6. <span data-ttu-id="32871-127">I fönstret **Användargrupp** väljer du åtgärden **Lägg till användare**.</span><span class="sxs-lookup"><span data-stu-id="32871-127">In the **User Group Members** window, choose the **Add Users** action.</span></span>
7. <span data-ttu-id="32871-128">Om du vill lägga till ytterligare behörighetsuppsättningar väljer du i fönstret **Användargrupper** åtgärden **Behörighetsuppsättningar för användargrupp**.</span><span class="sxs-lookup"><span data-stu-id="32871-128">To add new or additional permission sets, in the **User Groups** window, choose the **User Group Permission Sets** action.</span></span>
8. <span data-ttu-id="32871-129">I fönstret **Behörighetsuppsättningar för användargrupp** på en ny rad fyller du i fälten efter behov genom att välja från befintliga behörighetsuppsättningar.</span><span class="sxs-lookup"><span data-stu-id="32871-129">In the **User Group Permission Sets** window, on a new line, fill in the fields as necessary by selecting from existing permission sets.</span></span>

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a><span data-ttu-id="32871-130">Om du vill kopiera en användargrupp och dess behörighetsuppsättningar</span><span class="sxs-lookup"><span data-stu-id="32871-130">To copy a user group and all its permission sets</span></span>
<span data-ttu-id="32871-131">Du kan kopiera alla behörighetsuppsättningar från en befintlig användargrupp till den nya användargruppen, om du snabbt vill definiera en ny användargrupp..</span><span class="sxs-lookup"><span data-stu-id="32871-131">To quickly define a new user group, you can copy all permission sets from an existing user group to your new user group.</span></span>

<span data-ttu-id="32871-132">Medlemmarna i användargruppen kopieras inte till den nya användargruppen.</span><span class="sxs-lookup"><span data-stu-id="32871-132">The user group members are not copied to the new user group.</span></span> <span data-ttu-id="32871-133">Du måste lägga till dem manuellt i efterhand.</span><span class="sxs-lookup"><span data-stu-id="32871-133">You must add them manually afterwards.</span></span>

1. <span data-ttu-id="32871-134">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Användare** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="32871-134">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="32871-135">Välj de användargrupper som du vill kopiera och välj sedan åtgärden **Kopiera användargrupp**.</span><span class="sxs-lookup"><span data-stu-id="32871-135">Select the user group that you want to copy, and then choose the **Copy User Group** action.</span></span>
3. <span data-ttu-id="32871-136">I fältet **Ny användargruppkod** anger du ett namn på den nya gruppen och väljer sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="32871-136">In the **New User Group Code** field, enter a name for the group, and then choose the **OK** button.</span></span>

<span data-ttu-id="32871-137">Användargruppen läggs till i fönstret **Användargrupper**.</span><span class="sxs-lookup"><span data-stu-id="32871-137">The new user group is added to the **User Groups** window.</span></span> <span data-ttu-id="32871-138">Fortsätt med att lägga till användare.</span><span class="sxs-lookup"><span data-stu-id="32871-138">Proceed to add users.</span></span> <span data-ttu-id="32871-139">Mer information finns i avsnittet ”För gruppanvändare i användargrupper”.</span><span class="sxs-lookup"><span data-stu-id="32871-139">For more information, see the "To group users in user groups" section.</span></span>

## <a name="to-set-up-user-time-constraints"></a><span data-ttu-id="32871-140">Så här ställer du in tidsbegränsningar för användare</span><span class="sxs-lookup"><span data-stu-id="32871-140">To set up user time constraints</span></span>
<span data-ttu-id="32871-141">Administratörer kan definiera tidsperioder som anger när användare kan bokföra och även om systemet registrerar den tidsperiod som den angivna användaren är inloggad.</span><span class="sxs-lookup"><span data-stu-id="32871-141">Administrators can define periods of time during which specified users are able to post, and also specify if the system logs the amount of time users are logged on.</span></span> <span data-ttu-id="32871-142">Administratörer kan också tilldela ansvarsenheter till användare.</span><span class="sxs-lookup"><span data-stu-id="32871-142">Administrators can also assign responsibility centers to users.</span></span> <span data-ttu-id="32871-143">För mer information, se [Arbeta med ansvarsenheter](inventory-responsibility-centers.md).</span><span class="sxs-lookup"><span data-stu-id="32871-143">For more information, see [Work with Responsibility Centers](inventory-responsibility-centers.md).</span></span>

1. <span data-ttu-id="32871-144">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Resursinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="32871-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="32871-145">I fönstret **Användarinställningar** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="32871-145">In the **User Setup** window opens, choose the **New** action.</span></span>
3. <span data-ttu-id="32871-146">I den **Användar-ID** anger du ID för en användare, och väljer fältet för att se alla aktuella Windows-användare i systemet.</span><span class="sxs-lookup"><span data-stu-id="32871-146">In the **User ID** field, enter the ID of a user, or choose the field to see all current Windows users in the system.</span></span>
4. <span data-ttu-id="32871-147">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="32871-147">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="32871-148">Se även</span><span class="sxs-lookup"><span data-stu-id="32871-148">See Also</span></span>
[<span data-ttu-id="32871-149">Gör dig redo för affärer</span><span class="sxs-lookup"><span data-stu-id="32871-149">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
[<span data-ttu-id="32871-150">Administration</span><span class="sxs-lookup"><span data-stu-id="32871-150">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="32871-151">Komma igång</span><span class="sxs-lookup"><span data-stu-id="32871-151">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="32871-152">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="32871-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
