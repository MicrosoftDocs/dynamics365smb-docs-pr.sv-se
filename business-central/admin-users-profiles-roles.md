---
title: Hantera användare och roller | Microsoft Docs
description: Lär dig hantera användare och rollcenter i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 08/02/2019
ms.author: edupont
ms.openlocfilehash: 27a57490101195f8dc05cc39538260e7db5e46af
ms.sourcegitcommit: 5bcc5f95e450ee9a3d9f7a380e592a5e75c4185b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/05/2019
ms.locfileid: "1858226"
---
# <a name="understanding-users-roles-and-profiles"></a><span data-ttu-id="ea10d-103">Förstå användare, roller och profiler</span><span class="sxs-lookup"><span data-stu-id="ea10d-103">Understanding Users, Roles, and Profiles</span></span>

<span data-ttu-id="ea10d-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)] läggs användare till av en administratör som också ger användare tillgång till områden i [!INCLUDE[d365fin](includes/d365fin_md.md)] som de behöver i sitt arbete.</span><span class="sxs-lookup"><span data-stu-id="ea10d-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="ea10d-105">Åtkomst till funktioner styrs genom *användargrupper* och *profiler (roller)*.</span><span class="sxs-lookup"><span data-stu-id="ea10d-105">Access to functionality is managed through *user groups* and *profiles (roles)*.</span></span> <span data-ttu-id="ea10d-106">Som administratör kan du tilldela och ändra profiler i [!INCLUDE[d365fin](includes/d365fin_md.md)]-prenumeration och du kan lägga till och ta bort användare som en del av din användargrupp.</span><span class="sxs-lookup"><span data-stu-id="ea10d-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="ea10d-107">Lägga till användare</span><span class="sxs-lookup"><span data-stu-id="ea10d-107">Adding Users</span></span>

<span data-ttu-id="ea10d-108">Om du vill lägga till användare i [!INCLUDE[d365fin](includes/d365fin_md.md)] online, måste företagets Office 365-administratör först skapa användare i Office 365 Admin Center.</span><span class="sxs-lookup"><span data-stu-id="ea10d-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="ea10d-109">Mer information finns i [Lägg till användare till Office 365 för företag](https://aka.ms/CreateOffice365Users)</span><span class="sxs-lookup"><span data-stu-id="ea10d-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="ea10d-110">Administratören kan sedan tilldela behörigheter till varje användare och användargrupper.</span><span class="sxs-lookup"><span data-stu-id="ea10d-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="ea10d-111">Mer information finns i [Hantera användare och behörigheter](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="ea10d-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

<span data-ttu-id="ea10d-112">De mest kraftfulla behörigheter som en användare kan ha är behörighetsuppsättningen SUPER.</span><span class="sxs-lookup"><span data-stu-id="ea10d-112">The most powerful permissions that a user can have is the SUPER permission set.</span></span> <span data-ttu-id="ea10d-113">Varje företag måste ha minst en användare med denna behörighet, men det är bäst att ge behörighet till alla användare som matchar arbetsbehoven i [!INCLUDE[prodshort](includes/prodshort.md)] och inte mer än så.</span><span class="sxs-lookup"><span data-stu-id="ea10d-113">Each company must have at least one user with this permission set, but it is a best practice to give each user permissions that match their work needs in [!INCLUDE[prodshort](includes/prodshort.md)] and not more than that.</span></span> <span data-ttu-id="ea10d-114">Detta säkerställer att användare endast har tillgång till data som är relevanta för arbetet, t.ex.</span><span class="sxs-lookup"><span data-stu-id="ea10d-114">This helps ensure that users only have access to data that is relevant to their work, for example.</span></span>  

> [!TIP]
> <span data-ttu-id="ea10d-115">Det är bäst att kontrollera att Office 365 administratören också har behörighetsuppsättningen SUPER [!INCLUDE[prodshort](includes/prodshort.md)]eftersom det underlättar många administrativa uppgifter, inklusive inställning av integrering med andra program.</span><span class="sxs-lookup"><span data-stu-id="ea10d-115">It's a best practice to make sure that the Office 365 administrator also has the SUPER permission set in [!INCLUDE[prodshort](includes/prodshort.md)] because that makes many administrative tasks easier, including setting up integration with other apps.</span></span>

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="ea10d-116">Användare av lokala distributioner</span><span class="sxs-lookup"><span data-stu-id="ea10d-116">Users of on-premises deployments</span></span>

<span data-ttu-id="ea10d-117">Vid lokal distribution av [!INCLUDE[d365fin](includes/d365fin_md.md)], kan administratören välja mellan olika autentiseringsmetoder för användare.</span><span class="sxs-lookup"><span data-stu-id="ea10d-117">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="ea10d-118">När du sedan skapar en användare, tillhandahåller du olika information beroende på vilken autentiseringstyp du använder i den specifika [!INCLUDE[server](includes/server.md)]-instansen.</span><span class="sxs-lookup"><span data-stu-id="ea10d-118">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="ea10d-119">Mer information finns på [autentisering och autentisering](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i avsnittet Administration av utvecklare och ITPro-innehåll för [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ea10d-119">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles-roles"></a><span data-ttu-id="ea10d-120">Profiler (roller)</span><span class="sxs-lookup"><span data-stu-id="ea10d-120">Profiles (Roles)</span></span>

<span data-ttu-id="ea10d-121">Personer i företaget som har tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)] är tilldelade en roll som ger åtkomst till ett *Rollcenter*.</span><span class="sxs-lookup"><span data-stu-id="ea10d-121">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a role that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="ea10d-122">Profiler är samlingar av [!INCLUDE[d365fin](includes/d365fin_md.md)]-användare som delar samma roll.</span><span class="sxs-lookup"><span data-stu-id="ea10d-122">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same role.</span></span> <span data-ttu-id="ea10d-123">Ett rollcenter är startpunkten och startsidan för [!INCLUDE[d365fin](includes/d365fin_md.md)] som ger dig snabb åtkomst till dina viktigaste uppgifter och visar olika kunskap och nyckeltal (KPI) om ändringarna.</span><span class="sxs-lookup"><span data-stu-id="ea10d-123">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ea10d-124">I den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] online kan du inte lägga till, redigera eller ta bort profiler.</span><span class="sxs-lookup"><span data-stu-id="ea10d-124">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

### <a name="CreateProfile"></a><span data-ttu-id="ea10d-125">Så här skapar du en profil:</span><span class="sxs-lookup"><span data-stu-id="ea10d-125">To create a profile</span></span>

1.  <span data-ttu-id="ea10d-126">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Profiler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ea10d-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profiles**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="ea10d-127">På sidan **Profiler** väljer du åtgärden **Ny** för att öppna sidan **Nytt profilkort**.</span><span class="sxs-lookup"><span data-stu-id="ea10d-127">On the **Profiles** page, choose the **New** action to open the **New Profile Card** page.</span></span>  

3.  <span data-ttu-id="ea10d-128">I fältet **Profil-ID**, ange ett namn som beskriver den påtänkta rollen för användaren.</span><span class="sxs-lookup"><span data-stu-id="ea10d-128">In the **Profile ID** field, enter a name that describes the intended role of the users.</span></span>  

4.  <span data-ttu-id="ea10d-129">I fältet **Beskrivning** anger du en beskrivning av profil-ID:t, t.ex. **Orderhandläggare**.</span><span class="sxs-lookup"><span data-stu-id="ea10d-129">In the **Description** field, enter a description of the Profile ID, for example, **Order Processor**.</span></span>  

5.  <span data-ttu-id="ea10d-130">Ange fältet **Rollcenter-ID** till det rollcentret som du vill tilldela profilen.</span><span class="sxs-lookup"><span data-stu-id="ea10d-130">Set the **Role Center ID** field to the Role Center that you want to assign to the profile.</span></span>  

<span data-ttu-id="ea10d-131">Proceduren som används för att ändra en befintlig profil är samma, förutom att du väljer en befintlig profil på sidan **Profiler** i stället för att välja åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ea10d-131">The procedure for modifying an existing profile is the same, except you select an existing profile on the **Profiles** page instead of choosing the **New** action.</span></span>  


### <a name="copy-a-profile"></a><span data-ttu-id="ea10d-132">Kopiera en profil</span><span class="sxs-lookup"><span data-stu-id="ea10d-132">Copy a profile</span></span>
<span data-ttu-id="ea10d-133">Kopiera en profil kan spara tid, om du vill använda liknande inställningar på en profil, och du endast vill ändra några få inställningar.</span><span class="sxs-lookup"><span data-stu-id="ea10d-133">Copying a profile can save you time if you want to use similar settings on a profile and you only want to change a few settings.</span></span>

1.  <span data-ttu-id="ea10d-134">Öppna den profil som du vill kopiera och välj sedan åtgärden **Kopiera profil**.</span><span class="sxs-lookup"><span data-stu-id="ea10d-134">Open the profile that you want to copy, and then choose the **Copy Profile** action.</span></span>

2.  <span data-ttu-id="ea10d-135">Skriv namnet på profilen som du vill kopiera i fältet **Nytt profil-ID**.</span><span class="sxs-lookup"><span data-stu-id="ea10d-135">In **New Profile ID** field, enter a name for the profile that you want to copy.</span></span>

3.  <span data-ttu-id="ea10d-136">Ange fältet **Ny profilomfattning** till något av följande:</span><span class="sxs-lookup"><span data-stu-id="ea10d-136">Set the **New Profile Scope** field to one of the following:</span></span>

    - <span data-ttu-id="ea10d-137">**Systemet** så att den nya profilen är tillgänglig för alla innehavare av databaser som använder programmet.</span><span class="sxs-lookup"><span data-stu-id="ea10d-137">**System** to make the new profile available to all tenant databases that use the application.</span></span>
    - <span data-ttu-id="ea10d-138">**Klientorganisation** så att den nya profilen är tillgänglig bara för den aktuella klientorganisationens databas.</span><span class="sxs-lookup"><span data-stu-id="ea10d-138">**Tenant** to make the new profile available to just the current tenant database.</span></span>
4. <span data-ttu-id="ea10d-139">Välj knappen **OK** när du är klar.</span><span class="sxs-lookup"><span data-stu-id="ea10d-139">Choose the **OK** button when done.</span></span>

### <a name="ExportImportProfile"></a><span data-ttu-id="ea10d-140">Exportera och importera profiler</span><span class="sxs-lookup"><span data-stu-id="ea10d-140">Export and import profiles</span></span>

<span data-ttu-id="ea10d-141">Du kan exportera och importera profiler som XML-filer till och från en [!INCLUDE[d365fin](includes/d365fin_md.md)]-databas.</span><span class="sxs-lookup"><span data-stu-id="ea10d-141">You can export and import profiles as XML files to and from the a [!INCLUDE[d365fin](includes/d365fin_md.md)] database.</span></span> <span data-ttu-id="ea10d-142">Exportera och importera en profil låter dig spara tid när du konfigurerar användargränssnittet eftersom du kan återanvända en befintlig profilkonfiguration i stället för att konfigurera en profil från början.</span><span class="sxs-lookup"><span data-stu-id="ea10d-142">Exporting and importing a profile can save you time when configuring the user interface because you reuse an existing profile configuration instead of having to configure a profile from scratch.</span></span> <span data-ttu-id="ea10d-143">Om du har en profil som är konfigurerad i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-databas och du vill återanvända hela eller delar av samma profilkonfigurationer i en annan databas, kan du exportera profiler till en XML-fil.</span><span class="sxs-lookup"><span data-stu-id="ea10d-143">If you have a profile that is configured in a [!INCLUDE[d365fin](includes/d365fin_md.md)] database and you would like to reuse all or some of the same profile configurations in another database, you can export the profile to an XML file.</span></span> <span data-ttu-id="ea10d-144">Du kan sedan importera XML-filen för profilen i den andra databasen.</span><span class="sxs-lookup"><span data-stu-id="ea10d-144">Then, you can import the profile XML file into the other database.</span></span>

-   <span data-ttu-id="ea10d-145">Om du vill exportera en profil, kan du antingen välja åtgärden **Exportera profiler** från sidan **Profillista** eller **Profilkort** eller söka efter och öppna sidan **Exportera profiler**.</span><span class="sxs-lookup"><span data-stu-id="ea10d-145">To export a profile, you can either choose the **Export Profiles** action from the **Profile List** or **Profile Card** page or you can search for and open the **Export Profiles** page.</span></span> <span data-ttu-id="ea10d-146">Spara XML-filen till en plats på datorn eller i nätverket.</span><span class="sxs-lookup"><span data-stu-id="ea10d-146">Save the XML file to a location on your computer or network.</span></span>

-   <span data-ttu-id="ea10d-147">Om du vill importera en profil, kan du antingen välja åtgärden **Importera profil** från sidan **Profillista** eller söka efter och öppna sidan **Importera profiler**.</span><span class="sxs-lookup"><span data-stu-id="ea10d-147">To import a profile, you can either choose the **Import Profile** action from the **Profile List** page, or you can search for and open the **Import Profiles** page.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="ea10d-148">Du kan inte importera en profil som redan finns i databasen, även om XML-filen har ett annat namn eller annat innehåll.</span><span class="sxs-lookup"><span data-stu-id="ea10d-148">You cannot import a profile that already exists in the database, even though the XML file is named differently or has different content.</span></span> <span data-ttu-id="ea10d-149">Du måste ta bort den befintliga profilen innan du kan importera den nya profilen.</span><span class="sxs-lookup"><span data-stu-id="ea10d-149">You must delete the existing profile before you can import the new profile.</span></span>


## <a name="configuration-and-personalization"></a><span data-ttu-id="ea10d-150">Konfiguration och anpassning</span><span class="sxs-lookup"><span data-stu-id="ea10d-150">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

<span data-ttu-id="ea10d-151">Användare anpassa användargränssnittet för sin egen version genom att anpassa användargränssnittet under sin egen användarinloggning.</span><span class="sxs-lookup"><span data-stu-id="ea10d-151">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="ea10d-152">Den här anpassningen kan tas bort av administratören.</span><span class="sxs-lookup"><span data-stu-id="ea10d-152">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="ea10d-153">Mer information finns i [Anpassa arbetsytan](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="ea10d-153">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="ea10d-154">Se även</span><span class="sxs-lookup"><span data-stu-id="ea10d-154">See Also</span></span>  
[<span data-ttu-id="ea10d-155">Hantera användare och behörigheter</span><span class="sxs-lookup"><span data-stu-id="ea10d-155">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="ea10d-156">Hantera anpassning som administratör</span><span class="sxs-lookup"><span data-stu-id="ea10d-156">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="ea10d-157">Anpassa din arbetsyta</span><span class="sxs-lookup"><span data-stu-id="ea10d-157">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
