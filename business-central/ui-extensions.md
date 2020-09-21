---
title: Installera tillägg för att anpassa Business Central | Microsoft Docs
description: Lär dig mer om att lägga till funktioner och att anpassa Business Central genom att installera tillägg.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765927"
---
# <a name="customizing-business-central-using-extensions"></a><span data-ttu-id="c1830-103">Anpassa Business Central med tillägg</span><span class="sxs-lookup"><span data-stu-id="c1830-103">Customizing Business Central Using Extensions</span></span>

<span data-ttu-id="c1830-104">Du kan ändra [!INCLUDE[d365fin](includes/d365fin_md.md)] genom att installera tillägg som lägger till funktioner, ändrar beteende eller ger dig tillgång till nya onlinetjänster.</span><span class="sxs-lookup"><span data-stu-id="c1830-104">You can change [!INCLUDE[d365fin](includes/d365fin_md.md)] by installing extensions that add functionality, changes behavior, or gives you access to new online services, for example.</span></span>

> [!NOTE]
> <span data-ttu-id="c1830-105">Om du vill installera tillägg från AppSource eller lägga till tillägg per klientorganisation måste du ha rätt behörigheter.</span><span class="sxs-lookup"><span data-stu-id="c1830-105">To install extensions from AppSource or add per-tenant extensions, you must have the right permissions.</span></span> <span data-ttu-id="c1830-106">Du måste antingen vara medlem i användargruppen D365 Tilläggshant. eller så måste du ha behörighetsuppsättningen D365 Tilläggshant.</span><span class="sxs-lookup"><span data-stu-id="c1830-106">You must either be a member of the D365 EXTENSION MGMT user group or you must have the D365 EXTENSION MGMT permission set.</span></span> <span data-ttu-id="c1830-107">Om du är administratör kan du tilldela användargrupper och behörigheter till andra användare i företaget.</span><span class="sxs-lookup"><span data-stu-id="c1830-107">If you are an administrator, you can assign user groups and permissions to other users in your company.</span></span><br /><br />
<span data-ttu-id="c1830-108">Om du vill använda funktionen som tillhandahålls av ett tillägg, till exempel att öppna sidor, köra rapporter, välja åtgärder och så vidare, måste du koppla behörighetsuppsättningarna som installeras som en del av tillägget.</span><span class="sxs-lookup"><span data-stu-id="c1830-108">To use the functionality that is provided by an extension, such as opening pages, running reports, selecting actions, and so on, you must be assigned the permission sets that are installed as part of the extension.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="c1830-109">Överföring av tillägg per innehavare och installation av AppSource-tillägg stöds inte via sidan **Tilläggshantering** för lokala installationer.</span><span class="sxs-lookup"><span data-stu-id="c1830-109">The upload of per-tenant extensions and the installation of AppSource extensions is not supported through the **Extension Management** page for on-premise installations.</span></span>

<span data-ttu-id="c1830-110">När du först startar först [!INCLUDE[d365fin](includes/d365fin_md.md)], har du dessutom några tillägg installerade.</span><span class="sxs-lookup"><span data-stu-id="c1830-110">When you first launch [!INCLUDE[d365fin](includes/d365fin_md.md)], some extensions are already installed for you.</span></span> <span data-ttu-id="c1830-111">Med tiden kommer fler tillägg att göras tillgängliga till dig, och du kan då välja om du vill använda tillägg eller inte.</span><span class="sxs-lookup"><span data-stu-id="c1830-111">Over time, more extensions will be made available to you, and you can then choose if you want to use the extension or not.</span></span>

<span data-ttu-id="c1830-112">Till exempel ger Microsoft ett tillägg som ger integrering med PayPal Payments Standard.</span><span class="sxs-lookup"><span data-stu-id="c1830-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span> <span data-ttu-id="c1830-113">Detta tillägg instalelras dessutom som standard.</span><span class="sxs-lookup"><span data-stu-id="c1830-113">This extension is installed by default.</span></span>
<span data-ttu-id="c1830-114">Men om ett annat tillägg är tillgängligt som erbjuder integrering med en annan utbetalningtjänst, kan du installera det nya tillägget och sedan välja vilka av de två tjänsterna som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c1830-114">But if another extension is made available that offers integration with another payment service, you can install the new extension and then choose which of the two services to use.</span></span>  

<span data-ttu-id="c1830-115">Du hanterar tilläggen på sidan **Tilläggshantering**.</span><span class="sxs-lookup"><span data-stu-id="c1830-115">You manage the extensions on the **Extension Management** page.</span></span> <span data-ttu-id="c1830-116">Du kan öppna den här sidan från startsidan.</span><span class="sxs-lookup"><span data-stu-id="c1830-116">You can access this page from Home.</span></span> <span data-ttu-id="c1830-117">Du kan också välja ikonen **Sök efter sidan eller rapporten** ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") i övre högra hörnet och ange **tillägg** och välj sedan den relaterade länken.</span><span class="sxs-lookup"><span data-stu-id="c1830-117">Alternatively, choose the **Search for Page or Report** icon ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") in the top right corner, enter **Extension**, and then choose the related link.</span></span> <span data-ttu-id="c1830-118">Mer information finns i [Installera och avinstallera tillägg](ui-extensions-install-uninstall.md).</span><span class="sxs-lookup"><span data-stu-id="c1830-118">For more information, see [Installing and Uninstalling Extensions](ui-extensions-install-uninstall.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="c1830-119">Om du tror att du borde ha åtkomst till ett tillägg, men dess funktioner inte går att hitta kontrollerar du sidan **tilläggshantering** om tillägget inte finns, kan du installera det enligt vad som beskrivs i följande avsnitt.</span><span class="sxs-lookup"><span data-stu-id="c1830-119">If you think you should have access to an extension but you cannot find its functionality, check the **Extension Management** page - if the extension is not listed there, you can install it as described in the following section.</span></span>  

> [!NOTE]  
> <span data-ttu-id="c1830-120">Tillägg är inte tillgängliga i AppSource så snart vi meddelar en uppdatering.</span><span class="sxs-lookup"><span data-stu-id="c1830-120">New extensions are not available in AppSource immediately after we announce an update.</span></span> <span data-ttu-id="c1830-121">Du kan hålla utkik efter tilläggen på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span><span class="sxs-lookup"><span data-stu-id="c1830-121">You can keep an eye out for the extensions at  [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span></span>

## <a name="see-also"></a><span data-ttu-id="c1830-122">Se även</span><span class="sxs-lookup"><span data-stu-id="c1830-122">See Also</span></span>

[<span data-ttu-id="c1830-123">Utökning av Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="c1830-123">Extending Dynamics 365 Business Central</span></span>](about-develop-extensions.md)  
[<span data-ttu-id="c1830-124">Business Central-tillägg från andra leverantörer</span><span class="sxs-lookup"><span data-stu-id="c1830-124">Business Central Extensions by Other Providers</span></span>](ui-extensions-other.md)  
[<span data-ttu-id="c1830-125">Skapa tjänsten Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="c1830-125">Set Up the Envestnet Yodlee Bank Feeds Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="c1830-126">Så här aktiverar du kundutbetalning via PayPal</span><span class="sxs-lookup"><span data-stu-id="c1830-126">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md)  
[<span data-ttu-id="c1830-127">Migrera affärsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="c1830-127">Migrating Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="c1830-128">Konfigurera tillägget GetAddress.io för postnummer i Storbritannien</span><span class="sxs-lookup"><span data-stu-id="c1830-128">Setting Up the GetAddress.io UK Postal Code extension</span></span>](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
<span data-ttu-id="c1830-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)]-tillägg från andra leverantörer](ui-extensions-other.md)</span><span class="sxs-lookup"><span data-stu-id="c1830-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensions by Other Providers](ui-extensions-other.md)</span></span>  
[<span data-ttu-id="c1830-130">Komma igång</span><span class="sxs-lookup"><span data-stu-id="c1830-130">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
