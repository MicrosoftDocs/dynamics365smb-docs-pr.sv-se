---
title: "Hantera anpassning som administratör i Business Central | Microsoft Docs"
description: "Lär dig mer om att anpassa användargränssnittet så att det passar ditt sätt att arbeta."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 78eea4df6f25772063cef5770eb1dcb433bee012
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="4bef7-103">Hantera anpassning som administratör</span><span class="sxs-lookup"><span data-stu-id="4bef7-103">Managing Personalization as an Administrator</span></span>
<span data-ttu-id="4bef7-104"><!--NAV in the Web client--> Användare kan anpassa sin arbetsyta efter eget behov.</span><span class="sxs-lookup"><span data-stu-id="4bef7-104"><!--NAV in the Web client--> Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="4bef7-105">Som administratör kan du styra och hantera anpassning genom att inaktivera användare för att anpassa egna sidor och ta bort alla anpassningar på sidan som användare har gjort.</span><span class="sxs-lookup"><span data-stu-id="4bef7-105">As an administrator, you can control and manage personalization by disabling the ability for users to personalize pages and clearing any page personalizations that users have made.</span></span>

## <a name="disable-personalization-for-a-profile"></a><span data-ttu-id="4bef7-106">Inaktivera anpassningar för en profil</span><span class="sxs-lookup"><span data-stu-id="4bef7-106">Disable personalization for a profile</span></span>
<span data-ttu-id="4bef7-107">Du kan förhindra alla användare som tillhör en viss profil från att anpassa sidorna.</span><span class="sxs-lookup"><span data-stu-id="4bef7-107">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>
1.  <span data-ttu-id="4bef7-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Profiler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4bef7-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2.  <span data-ttu-id="4bef7-109">Välj den profil i listan som du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="4bef7-109">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="4bef7-110">Välj kryssrutan **Inaktivera anpassning** och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="4bef7-110">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="clear-user-personalizations"></a><span data-ttu-id="4bef7-111">Rensa användaranpassning</span><span class="sxs-lookup"><span data-stu-id="4bef7-111">Clear user personalizations</span></span>

<span data-ttu-id="4bef7-112">Ta bort sidann för anpassningsändringar gör att sidan återställs till sin ursprungliga layout innan alla anpassningar gjordes.</span><span class="sxs-lookup"><span data-stu-id="4bef7-112">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="4bef7-113">Det finns två sätt att ta bort de anpassningar som användare har gjort på sidor: med hjälp av fönstret **Ta bort användaranpassning** och använda fönstret **Anv.anpassningskort**.</span><span class="sxs-lookup"><span data-stu-id="4bef7-113">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** window and using the **User Personalization Card** window.</span></span>

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="4bef7-114">Ta bort användaranpassningar genom att använda sidan ta bort användaranpassning</span><span class="sxs-lookup"><span data-stu-id="4bef7-114">Clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="4bef7-115">Fönstret **Ta bort användaranpassning** låter dig ta bort anpassningen på per sida-basis, för varje enskild användare.</span><span class="sxs-lookup"><span data-stu-id="4bef7-115">The **Delete User Personalization** window enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1.  <span data-ttu-id="4bef7-116">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Ta bort användaranpassning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4bef7-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="4bef7-117">Sidan visar en lista över alla sidor som har anpassats och användaren den tillhör.</span><span class="sxs-lookup"><span data-stu-id="4bef7-117">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="4bef7-118">Ett kryss i kolumnen **Äldre anpassning** anger att anpassningen har skett i en äldre version av [!INCLUDE[d365fin](includes/d365fin_md.md)], som hanterade anpassningen på ett annat sätt än som nu sker.</span><span class="sxs-lookup"><span data-stu-id="4bef7-118">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="4bef7-119">Användare som försöker anpassa dessa sidor hindras från att göra detta såvida de inte väljer att låsa upp sidan.</span><span class="sxs-lookup"><span data-stu-id="4bef7-119">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="4bef7-120">Mer information finns i [Anledningen till att anpassningen är låst för en sida](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="4bef7-120">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="4bef7-121">Markera den transaktion som du vill radera och välj sedan åtgärden **Radera**.</span><span class="sxs-lookup"><span data-stu-id="4bef7-121">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="4bef7-122">Användaren kommer att se ändringarna nästa gång de loggar in.</span><span class="sxs-lookup"><span data-stu-id="4bef7-122">The user will see the changes the next time they sign-in.</span></span>

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="4bef7-123">Ta bort användaranpassningar genom att använda sidan användaranpassningskort</span><span class="sxs-lookup"><span data-stu-id="4bef7-123">Clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="4bef7-124">Fönstret **Anv.anpassningskort** låter dig ta bort anpassningen på alla sidor för en specifik användare.</span><span class="sxs-lookup"><span data-stu-id="4bef7-124">The **User Personalization Card** window enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="4bef7-125">Detta kräver skrivbehörighet för tabellen 2000000072 **Profil**.</span><span class="sxs-lookup"><span data-stu-id="4bef7-125">This requires write permission to Table 2000000072 **Profile**.</span></span>

1.  <span data-ttu-id="4bef7-126">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användaranpassning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4bef7-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="4bef7-127">Fönstret **användaranpassning** visar alla användare som eventuellt har anpassade sidor.</span><span class="sxs-lookup"><span data-stu-id="4bef7-127">The **User Personalization** window lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="4bef7-128">Om du inte hittar en användare i listan, innebär det att de inte har några anpassade sidor.</span><span class="sxs-lookup"><span data-stu-id="4bef7-128">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="4bef7-129">Välj den användare från listan, välj åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="4bef7-129">Select the user from the list, and then choose the **Edit** action.</span></span>

3.  <span data-ttu-id="4bef7-130">På fliken **Åtgärder**, välj **Ta bort anpassade sidor**.</span><span class="sxs-lookup"><span data-stu-id="4bef7-130">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="4bef7-131">Användaren kommer att se ändringarna nästa gång de loggar in.</span><span class="sxs-lookup"><span data-stu-id="4bef7-131">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="4bef7-132">Se även</span><span class="sxs-lookup"><span data-stu-id="4bef7-132">See Also</span></span>
[<span data-ttu-id="4bef7-133">Anpassa din arbetsyta</span><span class="sxs-lookup"><span data-stu-id="4bef7-133">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="4bef7-134">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4bef7-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4bef7-135">Ändra grundinställningar</span><span class="sxs-lookup"><span data-stu-id="4bef7-135">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="4bef7-136">Ändra vilka funktioner som visas</span><span class="sxs-lookup"><span data-stu-id="4bef7-136">Changing Which Features are Displayed</span></span>](ui-experiences.md)  

