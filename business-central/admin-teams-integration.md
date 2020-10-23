---
title: Hantera Microsoft Teams-integrering med Business Central| Microsoft Docs
description: Hantera Business Central-integrering med Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989364"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a><span data-ttu-id="5eb62-103">Hantera Microsoft Teams-integrering med Business Central</span><span class="sxs-lookup"><span data-stu-id="5eb62-103">Managing Microsoft Teams Integration with Business Central</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="5eb62-104">Den här artikeln innehåller en översikt över vad du kan göra som administratör för att styra Microsoft Teams-integrationen med [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="5eb62-104">This article provides an overview of what you can do as an administrator to control Microsoft Teams integration with [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

## <a name="in-microsoft-teams"></a><span data-ttu-id="5eb62-105">I Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5eb62-105">In Microsoft Teams</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="5eb62-106">Minsta krav</span><span class="sxs-lookup"><span data-stu-id="5eb62-106">Minimum requirements</span></span>

<span data-ttu-id="5eb62-107">I det här avsnittet beskrivs minimikraven för att [!INCLUDE [prodshort](includes/prodshort.md)]-appen ska fungera i Team.</span><span class="sxs-lookup"><span data-stu-id="5eb62-107">This section describes the minimum requirements for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

- <span data-ttu-id="5eb62-108">Nödvändiga licenser</span><span class="sxs-lookup"><span data-stu-id="5eb62-108">Required licenses</span></span>

    <span data-ttu-id="5eb62-109">I den här tabellen får du en översikt över de licenser som behövs för att [!INCLUDE [prodshort](includes/prodshort.md)]-appen ska fungera i Team.</span><span class="sxs-lookup"><span data-stu-id="5eb62-109">This table gives you an overview of the licenses needed for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

    |<span data-ttu-id="5eb62-110">Vad</span><span class="sxs-lookup"><span data-stu-id="5eb62-110">What</span></span>|<span data-ttu-id="5eb62-111">Team-licens</span><span class="sxs-lookup"><span data-stu-id="5eb62-111">Teams license</span></span>|<span data-ttu-id="5eb62-112">Business Central-licens</span><span class="sxs-lookup"><span data-stu-id="5eb62-112">Business Central license</span></span>|
    |----|---|---|
    |<span data-ttu-id="5eb62-113">Klistra in en länk till en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en konversation och skicka den som ett kort.</span><span class="sxs-lookup"><span data-stu-id="5eb62-113">Paste a link to a [!INCLUDE [prodshort](includes/prodshort.md)] record into a conversation, and send it as a card.</span></span>|<span data-ttu-id="5eb62-114">![bock](media/check.png "kontroll")</span><span class="sxs-lookup"><span data-stu-id="5eb62-114">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="5eb62-115">![bock](media/check.png "kontroll")</span><span class="sxs-lookup"><span data-stu-id="5eb62-115">![check mark](media/check.png "check")</span></span>|
    |<span data-ttu-id="5eb62-116">Visa ett kort i en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en konversation.</span><span class="sxs-lookup"><span data-stu-id="5eb62-116">View a card of a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="5eb62-117">![bock](media/check.png "kontroll")</span><span class="sxs-lookup"><span data-stu-id="5eb62-117">![check mark](media/check.png "check")</span></span>||
    |<span data-ttu-id="5eb62-118">Visa mer information för ett kort i en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en konversation.</span><span class="sxs-lookup"><span data-stu-id="5eb62-118">View more details of card for a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="5eb62-119">![bock](media/check.png "kontroll")</span><span class="sxs-lookup"><span data-stu-id="5eb62-119">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="5eb62-120">![bock](media/check.png "kontroll")</span><span class="sxs-lookup"><span data-stu-id="5eb62-120">![check mark](media/check.png "check")</span></span>|

- <span data-ttu-id="5eb62-121">Tillåt förhandsgranskning av URL</span><span class="sxs-lookup"><span data-stu-id="5eb62-121">Allow URL previews</span></span>

    <span data-ttu-id="5eb62-122">Principinställningen **Tillåt förhandsgranskning av URL** måste vara på.</span><span class="sxs-lookup"><span data-stu-id="5eb62-122">**Allow URL previews** policy setting must be turned on.</span></span> <span data-ttu-id="5eb62-123">Annars kan ett kort inte genereras för Business Central-länkar som klistrats in i en Team-konversation.</span><span class="sxs-lookup"><span data-stu-id="5eb62-123">Otherwise, a card can't be generated for Business Central links pasted into a Teams conversation.</span></span> <span data-ttu-id="5eb62-124">Mer information om den här inställningen finns i [Hantera meddelandeprinciper i Team](/microsoftteams/messaging-policies-in-teams).</span><span class="sxs-lookup"><span data-stu-id="5eb62-124">For more information about this setting, see [Manage messaging policies in Teams](/microsoftteams/messaging-policies-in-teams).</span></span>

### <a name="managing-the-business-central-app-optional"></a><span data-ttu-id="5eb62-125">Hantera Business Central-appen (valfritt)</span><span class="sxs-lookup"><span data-stu-id="5eb62-125">Managing the Business Central app (optional)</span></span>

<span data-ttu-id="5eb62-126">Som Team-administratör kan du hantera alla appar för organisationen, inklusive [!INCLUDE [prodshort](includes/prodshort.md)]-appen.</span><span class="sxs-lookup"><span data-stu-id="5eb62-126">As a Teams administrator, you can manage all apps for your organization, including the [!INCLUDE [prodshort](includes/prodshort.md)] app.</span></span> <span data-ttu-id="5eb62-127">Du kan godkänna eller installera [!INCLUDE [prodshort](includes/prodshort.md)]-appen för organisationen, hindra användare från att installera appen med mera.</span><span class="sxs-lookup"><span data-stu-id="5eb62-127">You can approve or install the [!INCLUDE [prodshort](includes/prodshort.md)] app for your organization, block user's from installing the app, and more.</span></span>

<span data-ttu-id="5eb62-128">Mer information finns i följande artiklar i Microsoft Teams-dokumentationen:</span><span class="sxs-lookup"><span data-stu-id="5eb62-128">For more information, see the following articles in the Microsoft Teams documentation:</span></span>

- [<span data-ttu-id="5eb62-129">Hantera dina appar i Microsoft Teams administratörscenter</span><span class="sxs-lookup"><span data-stu-id="5eb62-129">Manage your apps in the Microsoft Teams admin center</span></span>](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [<span data-ttu-id="5eb62-130">Hantera principer för appkonfiguration i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5eb62-130">Manage app setup policies in Microsoft Teams</span></span>](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a><span data-ttu-id="5eb62-131">I [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="5eb62-131">In [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="5eb62-132">Minsta krav</span><span class="sxs-lookup"><span data-stu-id="5eb62-132">Minimum requirements</span></span>

- <span data-ttu-id="5eb62-133">[!INCLUDE [prodshort](includes/prodshort.md)]-version:</span><span class="sxs-lookup"><span data-stu-id="5eb62-133">[!INCLUDE [prodshort](includes/prodshort.md)] version:</span></span>

    <span data-ttu-id="5eb62-134">[!INCLUDE [prodshort](includes/prodshort.md)] utgivningscykel 2 år 2020 (version 17) eller senare.</span><span class="sxs-lookup"><span data-stu-id="5eb62-134">[!INCLUDE [prodshort](includes/prodshort.md)] 2020 release wave 2 (version 17) or later.</span></span> <span data-ttu-id="5eb62-135">Team-integration stöds endast för [!INCLUDE [prodshort](includes/prodshort.md)] online, inte lokalt.</span><span class="sxs-lookup"><span data-stu-id="5eb62-135">Teams integration is only supported for [!INCLUDE [prodshort](includes/prodshort.md)] online; not on-premises.</span></span>

- <span data-ttu-id="5eb62-136">Codeunit **2718 sidan sammanfattning leverantör** är publicerad som en webbtjänst:</span><span class="sxs-lookup"><span data-stu-id="5eb62-136">Codeunit **2718 Page Summary Provider** is published as a web service:</span></span>

    <span data-ttu-id="5eb62-137">Denna codeunit publiceras som en webbtjänst som standard.</span><span class="sxs-lookup"><span data-stu-id="5eb62-137">This codeunit is published as a web service by default.</span></span> <span data-ttu-id="5eb62-138">Denna codeunit ingår i [!INCLUDE [prodshort](includes/prodshort.md)]-systemprogrammet.</span><span class="sxs-lookup"><span data-stu-id="5eb62-138">The codeunit is part of the [!INCLUDE [prodshort](includes/prodshort.md)] system application.</span></span> <span data-ttu-id="5eb62-139">Den används för att hämta fältdata för en [!INCLUDE [prodshort](includes/prodshort.md)]-sida som har lagts till i en Team-konversation.</span><span class="sxs-lookup"><span data-stu-id="5eb62-139">It's used to get the field data for a [!INCLUDE [prodshort](includes/prodshort.md)] page added to a Teams conversation.</span></span> 

- <span data-ttu-id="5eb62-140">Användarbehörigheter:</span><span class="sxs-lookup"><span data-stu-id="5eb62-140">User permissions:</span></span>

    <span data-ttu-id="5eb62-141">De sidor och data som användare kan visa och redigera i en Team-konversation styrs oftast av deras behörighet i [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="5eb62-141">For the most part, the pages and data that users can view and edit in a Teams conversation is controlled by their permissions in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>
    
    - <span data-ttu-id="5eb62-142">Om du vill klistra in en [!INCLUDE [prodshort](includes/prodshort.md)]-länk i en Team-konversation och låta den utökas till ett kort måste användarna åtminstone ha läsbehörighet på sidan och dess data.</span><span class="sxs-lookup"><span data-stu-id="5eb62-142">To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, users must have at least read permission on the page and its data.</span></span>
    - <span data-ttu-id="5eb62-143">När ett kort har skickats till en konversation kan alla användare i konversationen se det kortet utan behörighet till Business Central.</span><span class="sxs-lookup"><span data-stu-id="5eb62-143">Once a card is submitted into a conversation, any user in that conversation can view that card without permission to Business Central.</span></span>
    - <span data-ttu-id="5eb62-144">Om du vill visa mer information om ett kort eller öppna posten i [!INCLUDE [prodshort](includes/prodshort.md)] måste användarna ha läsbehörighet på sidan och dess data.</span><span class="sxs-lookup"><span data-stu-id="5eb62-144">To view more details for a card or open the record in [!INCLUDE [prodshort](includes/prodshort.md)], users must have read permission on the page and its data.</span></span>
    - <span data-ttu-id="5eb62-145">Användare måste ändra behörigheter för att kunna ändra data.</span><span class="sxs-lookup"><span data-stu-id="5eb62-145">To change data, user's need modify permissions.</span></span>
    
    <span data-ttu-id="5eb62-146">Mer information om behörigheter finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="5eb62-146">For information about permissions, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5eb62-147">Se även</span><span class="sxs-lookup"><span data-stu-id="5eb62-147">See Also</span></span>
[<span data-ttu-id="5eb62-148">Översikt över Business Central- och Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="5eb62-148">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="5eb62-149">[Installera [!INCLUDE [prodshort](includes/prodshort.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="5eb62-149">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="5eb62-150">Utveckling för Team-integrering</span><span class="sxs-lookup"><span data-stu-id="5eb62-150">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="5eb62-151">Komma igång</span><span class="sxs-lookup"><span data-stu-id="5eb62-151">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
