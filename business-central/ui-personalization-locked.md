---
title: Varför kan jag inte anpassa en sida? | Microsoft Docs
description: Förklarar varför du inte kan anpassa en sida, och vad du kan göra om du vill låsa upp den för att anpassa den.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 24f5dba76e5a3921c0e4c4c621192f7d95c017bf
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774745"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="a39a6-103">Varför är en sida låst för anpassning?</span><span class="sxs-lookup"><span data-stu-id="a39a6-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="a39a6-104">Det finns två villkor som hindrar dig från att anpassa en sida.</span><span class="sxs-lookup"><span data-stu-id="a39a6-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="a39a6-105">Antingen är sidan låst (vilket indikeras av ikonen ![Anpassa lås](media/personalization-lock-icon.png "Anpassa lås")) eller spärrad (vilket indikeras av ikonen ![Anpassning spärrad](media/personalization-blocked-icon.png "Anpassning spärrad")).</span><span class="sxs-lookup"><span data-stu-id="a39a6-105">Either the page is locked (as indicated by the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) icon or it is blocked (as indicated by the ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="a39a6-106">Låst för att anpassa</span><span class="sxs-lookup"><span data-stu-id="a39a6-106">Locked from Personalizing</span></span>

<span data-ttu-id="a39a6-107">Om det finns en ikon ![Anpassa lås](media/personalization-lock-icon.png "Anpassa lås") i banderollen **Anpassa** när du öppnar en sida, betyder det att du för tillfället inte kan göra några fler anpassningsändringar på sidan.</span><span class="sxs-lookup"><span data-stu-id="a39a6-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page, this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="a39a6-108">Det finnas två orsaker till detta:</span><span class="sxs-lookup"><span data-stu-id="a39a6-108">There can be two reasons for this:</span></span>

1. <span data-ttu-id="a39a6-109">Du har anpassat sidan tidigare, men det har gjorts med hjälp av en tidigare version av produkten.</span><span class="sxs-lookup"><span data-stu-id="a39a6-109">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="a39a6-110">Vi har ändrat hur anpassningen fungerar i bakgrunden sedan senaste gången du anpassade sidan.</span><span class="sxs-lookup"><span data-stu-id="a39a6-110">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="a39a6-111">Tyvärr fungerade inte det gamla och det nya sättet tillsammans.</span><span class="sxs-lookup"><span data-stu-id="a39a6-111">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="a39a6-112">Hittills har du bara använt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] för att anpassa sidan.</span><span class="sxs-lookup"><span data-stu-id="a39a6-112">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="a39a6-113">Låsa upp sidan</span><span class="sxs-lookup"><span data-stu-id="a39a6-113">Unlocking the Page</span></span>

<span data-ttu-id="a39a6-114">Om du vill låsa upp en sida och fortsätta anpassa den väljer du ikonen ![Anpassa lås](media/personalization-lock-icon.png "Anpassa lås") och sedan åtgärden **Lås upp**.</span><span class="sxs-lookup"><span data-stu-id="a39a6-114">If you want to unlock a page and continue personalizing it, choose the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon, and then choose the **Unlock** action.</span></span>  

<span data-ttu-id="a39a6-115">Innan du låser upp sidan, ska du tänka på följande:</span><span class="sxs-lookup"><span data-stu-id="a39a6-115">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="a39a6-116">Den aktuella anpassningen på sidan kommer att tas bort.</span><span class="sxs-lookup"><span data-stu-id="a39a6-116">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="a39a6-117">Sidan går tillbaka till sin ursprungliga layout och du måste börja om från början.</span><span class="sxs-lookup"><span data-stu-id="a39a6-117">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="a39a6-118">I [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] kommer sidan att behållas som den är och påverkas inte av de nya anpassningar i Business Central-klienten.</span><span class="sxs-lookup"><span data-stu-id="a39a6-118">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="a39a6-119">Sedan kommer anpassningen i [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] och Business Central-klienten att vara helt skilda från varandra.</span><span class="sxs-lookup"><span data-stu-id="a39a6-119">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="a39a6-120">Blockerad från att anpassa</span><span class="sxs-lookup"><span data-stu-id="a39a6-120">Blocked from Personalizing</span></span>

<span data-ttu-id="a39a6-121">Om det finns en ikon för ![Anpassning spärrad](media/personalization-blocked-icon.png "Anpassning spärrad") i banderollen **Anpassning** innebär detta att du spärras från att utgöra några anpassningar på sidan.</span><span class="sxs-lookup"><span data-stu-id="a39a6-121">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the **Personalizing** banner, this means that you are blocked from doing any personalization to the page.</span></span>

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

<span data-ttu-id="a39a6-122">Orsaken till detta är att det rollcenter eller den roll som för närvarande är associerad med ditt användarkonto ändrar sidan specifikt för din roll.</span><span class="sxs-lookup"><span data-stu-id="a39a6-122">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="a39a6-123">Kontakta administratören om du behöver hjälp.</span><span class="sxs-lookup"><span data-stu-id="a39a6-123">Contact your administrator for assistance.</span></span> <span data-ttu-id="a39a6-124">Du kan också försöka växla till ett rollcenter som innehåller rollspecifika roller för den här sidan.</span><span class="sxs-lookup"><span data-stu-id="a39a6-124">Alternatively, try switching to a Role Center that does include role-tailoring for this page.</span></span> <span data-ttu-id="a39a6-125">Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="a39a6-125">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a39a6-126">Se även</span><span class="sxs-lookup"><span data-stu-id="a39a6-126">See Also</span></span>
[<span data-ttu-id="a39a6-127">Anpassa din arbetsyta</span><span class="sxs-lookup"><span data-stu-id="a39a6-127">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="a39a6-128">Anpassa sidor för profiler</span><span class="sxs-lookup"><span data-stu-id="a39a6-128">Customize Pages for Profiles</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="a39a6-129">Ändra grundinställningar</span><span class="sxs-lookup"><span data-stu-id="a39a6-129">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="a39a6-130">Ändra vilka funktioner som visas</span><span class="sxs-lookup"><span data-stu-id="a39a6-130">Change Which Features are Displayed</span></span>](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]