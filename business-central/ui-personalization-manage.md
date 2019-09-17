---
title: Hantera anpassning som administratör i Business Central | Microsoft Docs
description: Lär dig mer om att anpassa användargränssnittet så att det passar ditt sätt att arbeta.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 08/16/2019
ms.author: jswymer
ms.openlocfilehash: 268d61e05f84643abe8eeeb283bd035e0247fe1c
ms.sourcegitcommit: 81b6062194bf04d8052a3cd394cc0b41e3f53e6d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2019
ms.locfileid: "1887743"
---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="77865-103">Hantera anpassning som administratör</span><span class="sxs-lookup"><span data-stu-id="77865-103">Managing Personalization as an Administrator</span></span>

<span data-ttu-id="77865-104"> Användare kan anpassa sin arbetsyta efter eget behov.</span><span class="sxs-lookup"><span data-stu-id="77865-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="77865-105">Som administratör kan du styra och hantera anpassning av:</span><span class="sxs-lookup"><span data-stu-id="77865-105">As an administrator, you control and manage personalization by:</span></span>

-   <span data-ttu-id="77865-106">Aktivera eller inaktivera funktionen anpassning för hela programmet (endast lokal installation).</span><span class="sxs-lookup"><span data-stu-id="77865-106">Enabling or disabling the personalization feature for the entire the application (on-premises installation only).</span></span>
-   <span data-ttu-id="77865-107">Aktivera eller inaktivera funktionen anpassning för användare med en viss profil.</span><span class="sxs-lookup"><span data-stu-id="77865-107">Enabling or disabling the personalization feature for users of a specific profile.</span></span>
-   <span data-ttu-id="77865-108">Ta bort alla anpassningar på sidan som användare har gjort.</span><span class="sxs-lookup"><span data-stu-id="77865-108">Clearing any page personalizations that users have made.</span></span>

## <a name="EnablePersonalization"></a><span data-ttu-id="77865-109">Så här aktiverar eller inaktiverar anpassningar (endast lokalt)</span><span class="sxs-lookup"><span data-stu-id="77865-109">To enable or disable personalization (On-Premises Only)</span></span>

<span data-ttu-id="77865-110">Som standard aktiveras inte anpassning i klienten.</span><span class="sxs-lookup"><span data-stu-id="77865-110">By default, personalization is not enabled in the client.</span></span> <span data-ttu-id="77865-111">Du aktiverar eller inaktiverar anpassningar genom att ändra konfigurationsfil (navsettings.json) för den Business Central Web Server-instans som används av klienterna.</span><span class="sxs-lookup"><span data-stu-id="77865-111">You enable or disable personalization by modifying the configuration file (navsettings.json) of the Business Central Web Server instance that serves the clients.</span></span>

1. <span data-ttu-id="77865-112">Aktivera anpassning genom att lägga till följande rad i filen navsettings.json:</span><span class="sxs-lookup"><span data-stu-id="77865-112">To enable personalization, add the following line in the navsettings.json file:</span></span>

    ```
    "PersonalizationEnabled": "true"
    ```

    <span data-ttu-id="77865-113">Ta bort den här raden om du vill inaktivera anpassningar, eller ändra den till:</span><span class="sxs-lookup"><span data-stu-id="77865-113">To disable personalization, remove this line or change it to:</span></span>

    ```
    "PersonalizationEnabled": "false"
    ```

    <span data-ttu-id="77865-114">Läs mer om hur du ändrar filen navsettings.json i [Ändra navsettings.json filen direkt](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span><span class="sxs-lookup"><span data-stu-id="77865-114">For more information about how to modify the navsettings.json file, see [Modify the navsettings.json file directly](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span></span>

2. <span data-ttu-id="77865-115">Skapa och hämta programsymboler.</span><span class="sxs-lookup"><span data-stu-id="77865-115">Generate and download the application symbols.</span></span>

    <span data-ttu-id="77865-116">Detta steg är valfritt och krävs inte för att aktivera anpassningar.</span><span class="sxs-lookup"><span data-stu-id="77865-116">This step is optional, and not required to enable personalization.</span></span> <span data-ttu-id="77865-117">Det innebär dock att nya sidor som skapas av utvecklare kan anpassas.</span><span class="sxs-lookup"><span data-stu-id="77865-117">However, it ensures that new pages that are created by developers can be personalized.</span></span>

    1. <span data-ttu-id="77865-118">Först måste du skapa symboler genom att köra kommandot finsql.exe med `generatesymbolreference`.</span><span class="sxs-lookup"><span data-stu-id="77865-118">First, you generate the symbols by running finsql.exe with `generatesymbolreference` command.</span></span> <span data-ttu-id="77865-119">Finsql.exe-filen finns i mappen för utvecklingsmiljön för [!INCLUDE[server](includes/server.md)] och Dynamics NAV (CSIDE).</span><span class="sxs-lookup"><span data-stu-id="77865-119">The finsql.exe file is located in the installation folder for the [!INCLUDE[server](includes/server.md)] and Dynamics NAV Development Environment (CSIDE).</span></span> <span data-ttu-id="77865-120">Om du vill skapa symboler, öppna kommandotolken, gå till katalogen där filen lagras och kör kommandot:</span><span class="sxs-lookup"><span data-stu-id="77865-120">To generate the symbols, open a command prompt, change to the directory where the file is store, and the run the following command:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    <span data-ttu-id="77865-121">Som exempel:</span><span class="sxs-lookup"><span data-stu-id="77865-121">For example:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    <span data-ttu-id="77865-122">Mer information finns i [Köra C/SIDE och AL sida vid sida](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span><span class="sxs-lookup"><span data-stu-id="77865-122">For more information, see [Running C/SIDE and AL Side-by-Side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span></span>

    2. <span data-ttu-id="77865-123">Konfigurera [!INCLUDE[nav_server_md](includes/nav_server_md.md)]-instansen till att **aktivera inläsning av programsymbolens referenser när servern startas** (EnableSymbolLoadingAtServerStartup).</span><span class="sxs-lookup"><span data-stu-id="77865-123">Configure [!INCLUDE[nav_server_md](includes/nav_server_md.md)] instance to **Enable loading application symbol references at server startup** (EnableSymbolLoadingAtServerStartup).</span></span> <span data-ttu-id="77865-124">Mer information finns i [Konfigurera Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span><span class="sxs-lookup"><span data-stu-id="77865-124">For more information, see [Configuring Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span></span>

## <a name="to-disable-personalization-for-a-profile"></a><span data-ttu-id="77865-125">Så här inaktiverar du anpassningar för en profil</span><span class="sxs-lookup"><span data-stu-id="77865-125">To disable personalization for a profile</span></span>

<span data-ttu-id="77865-126">Du kan förhindra alla användare som tillhör en viss profil från att anpassa sidorna.</span><span class="sxs-lookup"><span data-stu-id="77865-126">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>

1. <span data-ttu-id="77865-127">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Profiler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="77865-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="77865-128">Välj den profil i listan som du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="77865-128">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="77865-129">Välj kryssrutan **Inaktivera anpassning** och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="77865-129">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

> [!NOTE]  
> <span data-ttu-id="77865-130">I Business Central online kan du bara inaktivera anpassningar för en klientprofil, inte för systemprofiler.</span><span class="sxs-lookup"><span data-stu-id="77865-130">In Business Central online, you can only disable personalization for a tenant profile, not for system profiles.</span></span> 

## <a name="to-clear-user-personalizations"></a><span data-ttu-id="77865-131">Så här rensar du användaranpassning</span><span class="sxs-lookup"><span data-stu-id="77865-131">To clear user personalizations</span></span>

<span data-ttu-id="77865-132">Ta bort sidann för anpassningsändringar gör att sidan återställs till sin ursprungliga layout innan alla anpassningar gjordes.</span><span class="sxs-lookup"><span data-stu-id="77865-132">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="77865-133">Det finns två sätt att ta bort de anpassningar som användare har gjort på sidor: med hjälp av sidan **Ta bort användaranpassning** och använda sidan **Anv.anpassningskort**.</span><span class="sxs-lookup"><span data-stu-id="77865-133">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="77865-134">Du tar bort användaranpassningar genom att använda sidan ta bort användaranpassning</span><span class="sxs-lookup"><span data-stu-id="77865-134">To clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="77865-135">Sidan **Ta bort användaranpassning** låter dig ta bort anpassningen på per sida-basis, för varje enskild användare.</span><span class="sxs-lookup"><span data-stu-id="77865-135">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1. <span data-ttu-id="77865-136">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Ta bort användaranpassning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="77865-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="77865-137">Sidan visar en lista över alla sidor som har anpassats och användaren den tillhör.</span><span class="sxs-lookup"><span data-stu-id="77865-137">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="77865-138">Ett kryss i kolumnen **Äldre anpassning** anger att anpassningen har skett i en äldre version av [!INCLUDE[d365fin](includes/d365fin_md.md)], som hanterade anpassningen på ett annat sätt än som nu sker.</span><span class="sxs-lookup"><span data-stu-id="77865-138">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="77865-139">Användare som försöker anpassa dessa sidor hindras från att göra detta såvida de inte väljer att låsa upp sidan.</span><span class="sxs-lookup"><span data-stu-id="77865-139">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="77865-140">Mer information finns i [Anledningen till att anpassningen är låst för en sida](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="77865-140">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="77865-141">Markera den transaktion som du vill radera och välj sedan åtgärden **Radera**.</span><span class="sxs-lookup"><span data-stu-id="77865-141">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="77865-142">Användaren kommer att se ändringarna nästa gång de loggar in.</span><span class="sxs-lookup"><span data-stu-id="77865-142">The user will see the changes the next time they sign-in.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="77865-143">Du tar bort användaranpassningar genom att använda sidan användaranpassningskort</span><span class="sxs-lookup"><span data-stu-id="77865-143">To clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="77865-144">Sidan **Anv.anpassningskort** låter dig ta bort anpassningen på alla sidor för en specifik användare.</span><span class="sxs-lookup"><span data-stu-id="77865-144">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="77865-145">Detta kräver skrivbehörighet för tabellen 2000000072 **Profil**.</span><span class="sxs-lookup"><span data-stu-id="77865-145">This requires write permission to Table 2000000072 **Profile**.</span></span>

1. <span data-ttu-id="77865-146">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användaranpassning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="77865-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="77865-147">Sidan **användaranpassning** visar alla användare som eventuellt har anpassade sidor.</span><span class="sxs-lookup"><span data-stu-id="77865-147">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="77865-148">Om du inte hittar en användare i listan, innebär det att de inte har några anpassade sidor.</span><span class="sxs-lookup"><span data-stu-id="77865-148">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="77865-149">Välj den användare från listan, välj åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="77865-149">Select the user from the list, and then choose the **Edit** action.</span></span>

3. <span data-ttu-id="77865-150">På fliken **Åtgärder**, välj **Ta bort anpassade sidor**.</span><span class="sxs-lookup"><span data-stu-id="77865-150">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="77865-151">Användaren kommer att se ändringarna nästa gång de loggar in.</span><span class="sxs-lookup"><span data-stu-id="77865-151">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="77865-152">Se även</span><span class="sxs-lookup"><span data-stu-id="77865-152">See Also</span></span>
[<span data-ttu-id="77865-153">Anpassa din arbetsyta</span><span class="sxs-lookup"><span data-stu-id="77865-153">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="77865-154">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="77865-154">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="77865-155">Ändra grundinställningar</span><span class="sxs-lookup"><span data-stu-id="77865-155">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="77865-156">Ändra vilka funktioner som visas</span><span class="sxs-lookup"><span data-stu-id="77865-156">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
