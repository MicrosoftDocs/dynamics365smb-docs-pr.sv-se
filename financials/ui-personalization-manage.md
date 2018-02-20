---
title: "Hantera anpassning som administratör i Financials | Microsoft Docs"
description: "Lär dig mer om att anpassa användargränssnittet så att det passar ditt sätt att arbeta."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4384aeb9a9e1e06ea7abc7b4eecdd1365ac2a0a0
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="be3b3-103">Hantera anpassning som administratör</span><span class="sxs-lookup"><span data-stu-id="be3b3-103">Managing Personalization as an Administrator</span></span>
<!--NAV in the Web client-->
<span data-ttu-id="be3b3-104">Användare kan anpassa sin arbetsyta efter eget behov.</span><span class="sxs-lookup"><span data-stu-id="be3b3-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="be3b3-105">Som administratör kan du styra och hantera anpassning genom att inaktivera användare för att anpassa egna sidor och ta bort alla anpassningar på sidan som användare har gjort.</span><span class="sxs-lookup"><span data-stu-id="be3b3-105">As an administrator, you can control and manage personalization by disabling the ability for users to personalize pages and clearing any page personalizations that users have made.</span></span> 

## <a name="disable-personalization-for-a-profile"></a><span data-ttu-id="be3b3-106">Inaktivera anpassningar för en profil</span><span class="sxs-lookup"><span data-stu-id="be3b3-106">Disable personalization for a profile</span></span>
<span data-ttu-id="be3b3-107">Du kan förhindra alla användare som tillhör en viss profil från att anpassa sidorna.</span><span class="sxs-lookup"><span data-stu-id="be3b3-107">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>
1.  <span data-ttu-id="be3b3-108">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Profiler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="be3b3-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profiles**, and then choose the related link.</span></span>
2.  <span data-ttu-id="be3b3-109">Välj den profil i listan som du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="be3b3-109">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="be3b3-110">Välj kryssrutan **Inaktivera anpassning** och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="be3b3-110">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="clear-user-personalizations"></a><span data-ttu-id="be3b3-111">Rensa användaranpassning</span><span class="sxs-lookup"><span data-stu-id="be3b3-111">Clear user personalizations</span></span>

<span data-ttu-id="be3b3-112">Ta bort sidann för anpassningsändringar gör att sidan återställs till sin ursprungliga layout innan alla anpassningar gjordes.</span><span class="sxs-lookup"><span data-stu-id="be3b3-112">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="be3b3-113">Det finns två sätt att ta bort de anpassningar som användare har gjort på sidor: med hjälp av sidan **Ta bort användaranpassning** och använda sidan **Anv.anpassningskort**.</span><span class="sxs-lookup"><span data-stu-id="be3b3-113">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span> 

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="be3b3-114">Ta bort användaranpassningar genom att använda sidan ta bort användaranpassning</span><span class="sxs-lookup"><span data-stu-id="be3b3-114">Clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="be3b3-115">Sidan **Ta bort användaranpassning** låter dig ta bort anpassningen på per sida-basis, för varje enskild användare.</span><span class="sxs-lookup"><span data-stu-id="be3b3-115">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span> 

1.  <span data-ttu-id="be3b3-116">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Ta bort användaranpassning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="be3b3-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="be3b3-117">Sidan visar en lista över alla sidor som har anpassats och användaren den tillhör.</span><span class="sxs-lookup"><span data-stu-id="be3b3-117">The page lists all the pages that have been personalized and the user it belongs to.</span></span> 

    >[!NOTE]
    > <span data-ttu-id="be3b3-118">Ett kryss i kolumnen **Äldre anpassning** anger att anpassningen har skett i en äldre version av [!INCLUDE[d365fin](includes/d365fin_md.md)], som hanterade anpassningen på ett annat sätt än som nu sker.</span><span class="sxs-lookup"><span data-stu-id="be3b3-118">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="be3b3-119">Användare som försöker anpassa dessa sidor hindras från att göra detta såvida de inte väljer att låsa upp sidan.</span><span class="sxs-lookup"><span data-stu-id="be3b3-119">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="be3b3-120">Mer information finns i [Anledningen till att anpassningen är låst för en sida](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="be3b3-120">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="be3b3-121">Markera den transaktion som du vill radera och välj sedan åtgärden **Radera**.</span><span class="sxs-lookup"><span data-stu-id="be3b3-121">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="be3b3-122">Användaren kommer att se ändringarna nästa gång de loggar in.</span><span class="sxs-lookup"><span data-stu-id="be3b3-122">The user will see the changes the next time they sign-in.</span></span>

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="be3b3-123">Ta bort användaranpassningar genom att använda sidan användaranpassningskort</span><span class="sxs-lookup"><span data-stu-id="be3b3-123">Clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="be3b3-124">Sidan **Anv.anpassningskort** låter dig ta bort anpassningen på alla sidor för en specifik användare.</span><span class="sxs-lookup"><span data-stu-id="be3b3-124">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="be3b3-125">Detta kräver skrivbehörighet för tabellen 2000000072 **Profil**.</span><span class="sxs-lookup"><span data-stu-id="be3b3-125">This requires write permission to Table 2000000072 **Profile**.</span></span>

1.  <span data-ttu-id="be3b3-126">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Ta bort användaranpassning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="be3b3-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="be3b3-127">Sidan **användaranpassning** visar alla användare som eventuellt har anpassade sidor.</span><span class="sxs-lookup"><span data-stu-id="be3b3-127">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="be3b3-128">Om du inte hittar en användare i listan, innebär det att de inte har några anpassade sidor.</span><span class="sxs-lookup"><span data-stu-id="be3b3-128">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span> 

2. <span data-ttu-id="be3b3-129">Välj den användare från listan, välj åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="be3b3-129">Select the user from the list, and then choose the **Edit** action.</span></span>

3.  <span data-ttu-id="be3b3-130">På fliken **Åtgärder**, välj **Ta bort anpassade sidor**.</span><span class="sxs-lookup"><span data-stu-id="be3b3-130">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="be3b3-131">Användaren kommer att se ändringarna nästa gång de loggar in.</span><span class="sxs-lookup"><span data-stu-id="be3b3-131">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="be3b3-132">Se även</span><span class="sxs-lookup"><span data-stu-id="be3b3-132">See Also</span></span>
[<span data-ttu-id="be3b3-133">Anpassa din arbetsyta</span><span class="sxs-lookup"><span data-stu-id="be3b3-133">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="be3b3-134">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="be3b3-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="be3b3-135">Ändra Rollcenter</span><span class="sxs-lookup"><span data-stu-id="be3b3-135">Change the Role Center</span></span>](change-role.md)  
<span data-ttu-id="be3b3-136">[Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)]-upplevelse](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="be3b3-136">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  

