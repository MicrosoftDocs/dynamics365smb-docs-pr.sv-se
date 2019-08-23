---
title: Varför kan jag inte anpassa en sida? | Microsoft Docs
description: Förklarar varför du inte kan anpassa en sida, och vad du kan göra om du vill låsa upp den för att anpassa den.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 1a3edaca2e76388d82ea8991c3196410dd9c7288
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796773"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="9fc78-103">Varför är en sida låst för anpassning?</span><span class="sxs-lookup"><span data-stu-id="9fc78-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="9fc78-104">Det finns två villkor som hindrar dig från att anpassa en sida.</span><span class="sxs-lookup"><span data-stu-id="9fc78-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="9fc78-105">Antingen är sidan låst (som indikeras av ![anpassa lås](media/personalization-lock-icon.png "anpassa lås")) eller spärrad (som indikeras av ![anpassning spärrad](media/personalization-blocked-icon.png "anpassning spärrad")).</span><span class="sxs-lookup"><span data-stu-id="9fc78-105">Either the page is locked (as indicated by ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) or it is blocked (as indicated by ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked")).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="9fc78-106">Låst för att anpassa</span><span class="sxs-lookup"><span data-stu-id="9fc78-106">Locked from Personalizing</span></span>

<span data-ttu-id="9fc78-107">Om det finns en ikon ![anpassa lås](media/personalization-lock-icon.png "anpassa lås") i banderollen **anpassa** när du öppnar en sida (enligt bilden), betyder det att du för tillfället inte kan göra några fler anpassningsändringar på sidan.</span><span class="sxs-lookup"><span data-stu-id="9fc78-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page (as shown), this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<span data-ttu-id="9fc78-108">![Anpassa låsning](media/personalization-locked.png "Anpassa låsning")</span><span class="sxs-lookup"><span data-stu-id="9fc78-108">![Personalize Lock](media/personalization-locked.png "Personalize lock")</span></span>


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="9fc78-109">Det finnas två orsaker till detta:</span><span class="sxs-lookup"><span data-stu-id="9fc78-109">There can be two reasons for this:</span></span>

1. <span data-ttu-id="9fc78-110">Du har anpassat sidan tidigare, men det har gjorts med hjälp av en tidigare version av produkten.</span><span class="sxs-lookup"><span data-stu-id="9fc78-110">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="9fc78-111">Vi har ändrat hur anpassningen fungerar i bakgrunden sedan senaste gången du anpassade sidan.</span><span class="sxs-lookup"><span data-stu-id="9fc78-111">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="9fc78-112">Tyvärr fungerade inte det gamla och det nya sättet tillsammans.</span><span class="sxs-lookup"><span data-stu-id="9fc78-112">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="9fc78-113">Hittills har du bara använt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] för att anpassa sidan.</span><span class="sxs-lookup"><span data-stu-id="9fc78-113">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="9fc78-114">Låsa upp sidan</span><span class="sxs-lookup"><span data-stu-id="9fc78-114">Unlocking the Page</span></span>

<span data-ttu-id="9fc78-115">Om du vill låsa upp en sida och fortsätta anpassa den, välj ![anpassa lås](media/personalization-lock-icon.png "anpassa lås") och sedan **lås upp**.</span><span class="sxs-lookup"><span data-stu-id="9fc78-115">If you want to unlock a page and continue personalizing it, choose ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock"), and then **Unlock**.</span></span>  

<span data-ttu-id="9fc78-116">Innan du låser upp sidan, ska du tänka på följande:</span><span class="sxs-lookup"><span data-stu-id="9fc78-116">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="9fc78-117">Den aktuella anpassningen på sidan kommer att tas bort.</span><span class="sxs-lookup"><span data-stu-id="9fc78-117">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="9fc78-118">Sidan går tillbaka till sin ursprungliga layout och du måste börja om från början.</span><span class="sxs-lookup"><span data-stu-id="9fc78-118">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="9fc78-119">I [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] kommer sidan att behållas som den är och påverkas inte av de nya anpassningar i Business Central-klienten.</span><span class="sxs-lookup"><span data-stu-id="9fc78-119">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="9fc78-120">Sedan kommer anpassningen i [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] och Business Central-klienten att vara helt skilda från varandra.</span><span class="sxs-lookup"><span data-stu-id="9fc78-120">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="9fc78-121">Blockerad från att anpassa</span><span class="sxs-lookup"><span data-stu-id="9fc78-121">Blocked from Personalizing</span></span>

<span data-ttu-id="9fc78-122">Om det finns en ikon för ![anpassning spärrad](media/personalization-blocked-icon.png "anpassning spärrad") i anpassningsbanderoll innebär detta att du blockeras från att göra alla anpassningar till sidan.</span><span class="sxs-lookup"><span data-stu-id="9fc78-122">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the Personalizing banner, this means that you are blocked from doing any personalization to the page.</span></span>

<span data-ttu-id="9fc78-123">![Anpassa spärrad](media/personalization-blocked.png "Anpassa spärrad")</span><span class="sxs-lookup"><span data-stu-id="9fc78-123">![Personalize blocked](media/personalization-blocked.png "Personalize lock")</span></span>

<span data-ttu-id="9fc78-124">Orsaken till detta är att det rollcenter eller den roll som för närvarande är associerad med ditt användarkonto ändrar sidan specifikt för din roll.</span><span class="sxs-lookup"><span data-stu-id="9fc78-124">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="9fc78-125">Kontakta administratören om du behöver hjälp eller, om det passar, kan du försöka att byta till ett rollcenter (från [**Mina inställningar**](https://businesscentral.dynamics.com?page=9176 "gå direkt till sidan användare inställningar i Business Central")) som innehåller rollanpassning för sidan.</span><span class="sxs-lookup"><span data-stu-id="9fc78-125">Please contact your administrator for assistance or, if it makes sense, try switching to a Role Center (from  [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central")) that does include role-tailoring for this page.</span></span>

## <a name="see-also"></a><span data-ttu-id="9fc78-126">Se även</span><span class="sxs-lookup"><span data-stu-id="9fc78-126">See Also</span></span>
[<span data-ttu-id="9fc78-127">Anpassa din arbetsyta</span><span class="sxs-lookup"><span data-stu-id="9fc78-127">Personalizing Your Workspace</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="9fc78-128">Hantera anpassning</span><span class="sxs-lookup"><span data-stu-id="9fc78-128">Managing Personalization</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="9fc78-129">Ändra grundinställningar</span><span class="sxs-lookup"><span data-stu-id="9fc78-129">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="9fc78-130">Ändra vilka funktioner som visas</span><span class="sxs-lookup"><span data-stu-id="9fc78-130">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
