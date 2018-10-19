---
title: Anpassa Business Central | Microsoft Docs
description: "Lär dig mer om att lägga till funktioner och att anpassa Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, add-in, extend, customize
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 63ba198a761b0c79c51ac94d36314310e330fc58
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="customizing-business-central"></a><span data-ttu-id="789cb-103">Anpassa Business Central</span><span class="sxs-lookup"><span data-stu-id="789cb-103">Customizing Business Central</span></span>
<span data-ttu-id="789cb-104">Det finns olika sätt att anpassa programmet så att du och dina arbetskamrater får tillgång till det innehåll, funktioner och uppgifter som du verkligen behöver, på ett sätt som passar ert dagliga arbete bäst.</span><span class="sxs-lookup"><span data-stu-id="789cb-104">There are different ways to customize the application to give you and your colleagues access to the features, functionality, and data that you need most, in a manner that bests suits your daily work.</span></span> <span data-ttu-id="789cb-105">De som ser ändringarna förlitar sig på vad du gör, enligt vad som beskrivs i denna tabell.</span><span class="sxs-lookup"><span data-stu-id="789cb-105">Those who see the changes will depend on what you do, as described in this table.</span></span>

| <span data-ttu-id="789cb-106">Detta kan du göra</span><span class="sxs-lookup"><span data-stu-id="789cb-106">What you can do</span></span>    |  <span data-ttu-id="789cb-107">Description</span><span class="sxs-lookup"><span data-stu-id="789cb-107">Description</span></span>  |  <span data-ttu-id="789cb-108">Vem som kan se ändringarna</span><span class="sxs-lookup"><span data-stu-id="789cb-108">Who sees the changes</span></span>  |  <span data-ttu-id="789cb-109">Mer information</span><span class="sxs-lookup"><span data-stu-id="789cb-109">More information</span></span>  |
|-----|---------------|---------|-------|
|<span data-ttu-id="789cb-110">Installera ett tillägg</span><span class="sxs-lookup"><span data-stu-id="789cb-110">Install an extension</span></span>|<span data-ttu-id="789cb-111">Tillägg är som små program som lägger till funktioner, ändrar beteende, ger tillgång till nya onlinetjänster med mera.</span><span class="sxs-lookup"><span data-stu-id="789cb-111">Extensions are like small applications that add functionality, change behavior, provide access to new online services, and more.</span></span> <span data-ttu-id="789cb-112">Till exempel ger Microsoft ett tillägg som ger integrering med PayPal Payments Standard.</span><span class="sxs-lookup"><span data-stu-id="789cb-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span>|<span data-ttu-id="789cb-113">Alla användare i alla företag.</span><span class="sxs-lookup"><span data-stu-id="789cb-113">All users in all companies.</span></span>|[<span data-ttu-id="789cb-114">Anpassa med tillägg</span><span class="sxs-lookup"><span data-stu-id="789cb-114">Customizing Using Extensions</span></span>](ui-extensions.md)|
|<span data-ttu-id="789cb-115">Ändra vilka element i användargränssnittet som visas.</span><span class="sxs-lookup"><span data-stu-id="789cb-115">Change which UI elements are visible.</span></span>|<span data-ttu-id="789cb-116">Inställningen **Upplevelse** anger hur stor del av funktionen som visas i användargränssnittet.</span><span class="sxs-lookup"><span data-stu-id="789cb-116">The **Experience** setting determines how much of the functionality is displayed in the user interface.</span></span> <span data-ttu-id="789cb-117">Välj mellan grundläggande och premium.</span><span class="sxs-lookup"><span data-stu-id="789cb-117">Choose between Essential and Premium.</span></span>|<span data-ttu-id="789cb-118">Alla användare i ett visst företag.</span><span class="sxs-lookup"><span data-stu-id="789cb-118">All users in a specific company.</span></span>|[<span data-ttu-id="789cb-119">Ändra vilka funktioner som visas</span><span class="sxs-lookup"><span data-stu-id="789cb-119">Changing Which Features are Displayed</span></span>](ui-experiences.md)|
|<span data-ttu-id="789cb-120">Anpassa din arbetsyta</span><span class="sxs-lookup"><span data-stu-id="789cb-120">Personalize your workspace</span></span>|<span data-ttu-id="789cb-121">Ändra layout och innehåll på dina sidor.</span><span class="sxs-lookup"><span data-stu-id="789cb-121">Change the layout and content of your pages.</span></span>|<span data-ttu-id="789cb-122">Bara du.</span><span class="sxs-lookup"><span data-stu-id="789cb-122">Only you.</span></span>|[<span data-ttu-id="789cb-123">Anpassa din arbetsyta</span><span class="sxs-lookup"><span data-stu-id="789cb-123">Personalizing Your Workspace</span></span>](ui-personalization-user.md)|

> [!NOTE]
> <span data-ttu-id="789cb-124">Alla funktionsbeskrivningar i användardokumentationen för [!INCLUDE[d365fin](includes/d365fin_md.md)] antar **Premium**-upplevelsen, vilket innebär beskrivningarna som omfattar hela gränssnittselement.</span><span class="sxs-lookup"><span data-stu-id="789cb-124">All feature descriptions in user documentation for [!INCLUDE[d365fin](includes/d365fin_md.md)] assumes the **Premium** experience, meaning the descriptions cover the full scope of UI elements.</span></span> <span data-ttu-id="789cb-125">Därför kan användare med **grundläggande** upplevelsen i vissa avsnitt läsa om funktionerna och delar av användargränssnittet som inte visas i deras användargränssnitt.</span><span class="sxs-lookup"><span data-stu-id="789cb-125">Therefore, users with the **Essential** experience may in some topics read about functionality and UI elements that are not visible in their user interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="789cb-126">Se även</span><span class="sxs-lookup"><span data-stu-id="789cb-126">See Also</span></span>
<span data-ttu-id="789cb-127">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="789cb-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

