---
title: Varningar och felmeddelanden
description: Lär dig hur du felsöker och hittar lösningar på felmeddelanden när du arbetar i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fa01f29859b8076ffd9b7786a619ef932903b8d9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779488"
---
# <a name="warnings-and-error-messages-in-dynamics-365-business-central"></a><span data-ttu-id="17e39-103">Varningar och felmeddelanden i Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="17e39-103">Warnings and Error Messages in Dynamics 365 Business Central</span></span>

<span data-ttu-id="17e39-104">Under din arbetsdag kan du se meddelanden i [!INCLUDE [prod_short](includes/prod_short.md)] om att något gick fel eller att det inte var möjligt att bokföra någonting t. ex.</span><span class="sxs-lookup"><span data-stu-id="17e39-104">During your work day, you might see notifications in [!INCLUDE [prod_short](includes/prod_short.md)] that something went wrong, or that it was not possible to post something, for example.</span></span> <span data-ttu-id="17e39-105">I många fall gör meddelandet det enkelt att lösa ärendet eller att återställa de ändringar som du har gjort.</span><span class="sxs-lookup"><span data-stu-id="17e39-105">In many cases, the notification makes it easy to resolve the matter, or to roll back any changes that you made.</span></span> <span data-ttu-id="17e39-106">I andra fall kanske du inte har den information som du behöver för att få en avblockering.</span><span class="sxs-lookup"><span data-stu-id="17e39-106">In other cases, you might not have have the information that you need to get unblocked.</span></span> <span data-ttu-id="17e39-107">I den här artikeln finns tips om hur du gör framsteg.</span><span class="sxs-lookup"><span data-stu-id="17e39-107">This article provides tips on how to make progress.</span></span>  

## <a name="in-product-user-assistance"></a><span data-ttu-id="17e39-108">Användarhjälp i produkten</span><span class="sxs-lookup"><span data-stu-id="17e39-108">In-product user assistance</span></span>

<span data-ttu-id="17e39-109">Standardversionen av [!INCLUDE [prod_short](includes/prod_short.md)] innehåller beskrivningar av de flesta fält, kolumner och åtgärder som du kan komma åt när du väljer namnet.</span><span class="sxs-lookup"><span data-stu-id="17e39-109">The default version of [!INCLUDE [prod_short](includes/prod_short.md)] includes descriptions for most fields, columns, and actions that can be accessed when you choose the name.</span></span> <span data-ttu-id="17e39-110">I kombination med undervisningstips för viktiga sidor, beskrivande rubriker och instruktionstext är dessa beskrivningar eller bildtexter vår aktuella implementering av *inbäddat användarstöd*, som är en viktig princip i dagens programvarudesign.</span><span class="sxs-lookup"><span data-stu-id="17e39-110">In combination with teaching tips for important pages, descriptive captions, and instructional text, these tooltips, or callouts, are our current implementation of *embedded user assistance*, which is an important principle in today's world of software design.</span></span>  

<span data-ttu-id="17e39-111">Om du har en fråga om ett fält eller något annat element i användargränssnittet, väljer du namnet och en kort beskrivning visas.</span><span class="sxs-lookup"><span data-stu-id="17e39-111">If you have a question about a field or another element of the user interface, choose the name, and a short description will appear.</span></span> <span data-ttu-id="17e39-112">Välj länken *Mer information* om det inte räcker.</span><span class="sxs-lookup"><span data-stu-id="17e39-112">Choose the *Learn more* link if that is not enough.</span></span>  

<span data-ttu-id="17e39-113">Mer information finns i [Dynamics 365 Business Central användarhjälpsmodell](/dynamics365/business-central/dev-itpro/user-assistance) i administrationsinnehållet för [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="17e39-113">For more information, see [Dynamics 365 Business Central User Assistance Model](/dynamics365/business-central/dev-itpro/user-assistance) in the administration content for [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>  

## <a name="help-and-support-page"></a><span data-ttu-id="17e39-114">Hjälp- och supportsida</span><span class="sxs-lookup"><span data-stu-id="17e39-114">Help and Support page</span></span>

<span data-ttu-id="17e39-115">I [!INCLUDE[prod_short](includes/prod_short.md)] ger hjälpmenyalternativet (frågetecken i övre högra hörnet) dig tillgång till sidan **Hjälp och support** där du hittar länkar till resurser som kan hjälpa dig att hitta svaren på dina frågor.</span><span class="sxs-lookup"><span data-stu-id="17e39-115">In [!INCLUDE[prod_short](includes/prod_short.md)], the Help menu item (the question mark in the top right corner) gives you access to the **Help and Support** page, where you can find links to resources that can help you find answers to your questions.</span></span> <span data-ttu-id="17e39-116">Mer information finns i [Resurser för Hjälp och support](product-help-and-support.md).</span><span class="sxs-lookup"><span data-stu-id="17e39-116">For more information, see [Resources for Help and Support](product-help-and-support.md).</span></span>  

## <a name="help-others"></a><span data-ttu-id="17e39-117">Hjälpa andra</span><span class="sxs-lookup"><span data-stu-id="17e39-117">Help others</span></span>

<span data-ttu-id="17e39-118">Om du är administratör eller superanvändare kan du hjälpa andra genom att söka efter felmeddelanden på sidan **Felmeddelanderegister** eller i administrationscentret.</span><span class="sxs-lookup"><span data-stu-id="17e39-118">If you are an administrator or superuser, you can help others by looking up error messages in the **Error Message Register** page or in the administration center.</span></span> <span data-ttu-id="17e39-119">I många fall handlar varningen eller felmeddelandet om installation eller avsaknad av behörighet och liknande problem som superanvändaren eller administratören kan hjälpa till med.</span><span class="sxs-lookup"><span data-stu-id="17e39-119">In many cases, the warning or error message is about setup or lack of permission and similar issues that the superuser or administrator can easily help with.</span></span> <span data-ttu-id="17e39-120">I andra fall kanske du måste inspektera sidorna för att identifiera orsaken.</span><span class="sxs-lookup"><span data-stu-id="17e39-120">In other cases, you might have to inspect pages to identify the cause.</span></span> <span data-ttu-id="17e39-121">Mer information finns i avsnittet [Söka efter teknisk information](/dynamics365/business-central/dev-itpro/administration/manage-technical-support#finding-technical-information) i administrationsinnehållet för [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="17e39-121">For more information, see [Finding technical information](/dynamics365/business-central/dev-itpro/administration/manage-technical-support#finding-technical-information) in the administration content for [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>  

## <a name="see-also"></a><span data-ttu-id="17e39-122">Se även</span><span class="sxs-lookup"><span data-stu-id="17e39-122">See Also</span></span>

[<span data-ttu-id="17e39-123">Resurser för hjälp och support</span><span class="sxs-lookup"><span data-stu-id="17e39-123">Resources for Help and Support</span></span>](product-help-and-support.md)  
[<span data-ttu-id="17e39-124">Vanliga frågor och svar</span><span class="sxs-lookup"><span data-stu-id="17e39-124">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="17e39-125">Vanliga frågor om Berätta</span><span class="sxs-lookup"><span data-stu-id="17e39-125">Tell Me FAQ</span></span>](ui-search-faq.md)  
[<span data-ttu-id="17e39-126">Vanliga frågor och svar om sökning och filtrering</span><span class="sxs-lookup"><span data-stu-id="17e39-126">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.md)  
[<span data-ttu-id="17e39-127">Vanliga frågor om Kopiera och klistra in</span><span class="sxs-lookup"><span data-stu-id="17e39-127">Copy and Paste FAQ</span></span>](faq-copy-paste.yml)  
[<span data-ttu-id="17e39-128">Ändra grundinställningar</span><span class="sxs-lookup"><span data-stu-id="17e39-128">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="17e39-129">Gör dig redo att göra affärer</span><span class="sxs-lookup"><span data-stu-id="17e39-129">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]