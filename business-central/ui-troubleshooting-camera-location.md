---
title: 'Felsökning: komma åt kamera och plats'
description: I den här artikeln beskrivs felsökning av åtkomst till kamera och platsinformation i Business Central.
author: blrobl
ms.author: t-blrobl
ms.date: 10/01/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.openlocfilehash: a29b2ea19d812d60d2824c131e311c34d74612af
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760222"
---
# <a name="troubleshooting-accessing-camera-and-location"></a><span data-ttu-id="effcb-103">Felsökning: komma åt kamera och plats</span><span class="sxs-lookup"><span data-stu-id="effcb-103">Troubleshooting: Accessing Camera and Location</span></span>

<span data-ttu-id="effcb-104">Det kan uppstå problem när du försöker komma åt kamera och platsinformation för en enhet [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="effcb-104">You might come across some issues when trying to access the camera and location information of a device from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="effcb-105">Du kan hitta möjliga orsaker till det här problemet och hur du kan undvika dem i listan nedan.</span><span class="sxs-lookup"><span data-stu-id="effcb-105">You can find the possible causes behind these problems and how to work around them listed below.</span></span>

## <a name="device-must-have-camera-and-location-capabilities"></a><span data-ttu-id="effcb-106">Enheten måste ha kamera och platsfunktioner</span><span class="sxs-lookup"><span data-stu-id="effcb-106">Device must have Camera and Location Capabilities</span></span>

<span data-ttu-id="effcb-107">För att du ska kunna komma åt kameran eller en användares plats från en enhet måste enheten ha en fysisk kamera eller möjlighet att hämta platsinformation.</span><span class="sxs-lookup"><span data-stu-id="effcb-107">In order to access the camera or a user's location from a device, the device must have a physical camera or the capability to retrieve location information, respectively.</span></span>

<span data-ttu-id="effcb-108">Om enheten har funktioner för kamera och plats, men det fortfarande uppstår problem, kan vissa drivrutiner behöva uppdateras eller installeras om.</span><span class="sxs-lookup"><span data-stu-id="effcb-108">If your device has camera and location capabilities but you still encounter problems, it is possible that some drivers need updating or reinstalling.</span></span> <span data-ttu-id="effcb-109">Även om du är osäker, rekommenderar vi alltid att du uppdaterar enhetens operativsystem, drivrutiner och webbläsare till den senaste versionen för bästa möjliga upplevelse.</span><span class="sxs-lookup"><span data-stu-id="effcb-109">Even if you are unsure, we always recommend you update your device operating system, drivers, and browser to the latest version for the best experience.</span></span>

## <a name="access-permissions-not-enabled"></a><span data-ttu-id="effcb-110">Åtkomstbehörighet är inte aktiverad</span><span class="sxs-lookup"><span data-stu-id="effcb-110">Access Permissions not Enabled</span></span>

<span data-ttu-id="effcb-111">Du måste aktivera allmän åtkomst till kamera och plats från enhetens sekretessinställningar och uttryckligen ge behörighet till [!INCLUDE[prod_short](includes/prod_short.md)] för åtkomst till dem.</span><span class="sxs-lookup"><span data-stu-id="effcb-111">You must enable general access to camera and location from your device's privacy settings and explicitly give permission to  [!INCLUDE[prod_short](includes/prod_short.md)] to access them.</span></span> <span data-ttu-id="effcb-112">Om du till exempel vill visa eller ändra behörigheter för en enhet som körs på Windows går du till **Inställningar**, väljer **Sekretess** och sedan **Appbehörigheter**.</span><span class="sxs-lookup"><span data-stu-id="effcb-112">For example, to see or change permissions for a device running on Windows, go to **Settings**, choose **Privacy**, and then **App permissions**.</span></span> 

<span data-ttu-id="effcb-113">För mobila enheter måste du ge den mobila appen åtkomstbehörighet för kamera och plats till [!INCLUDE[prod_short](includes/prod_short.md)] mobilapp.</span><span class="sxs-lookup"><span data-stu-id="effcb-113">For mobile devices, you must give camera and location access permissions to the [!INCLUDE[prod_short](includes/prod_short.md)] Mobile App.</span></span> <span data-ttu-id="effcb-114">Om du vill göra det för en iOS-enhet går du till **inställningar**, väljer **sekretess** och sedan **kamera** eller **plats**.</span><span class="sxs-lookup"><span data-stu-id="effcb-114">To do so for an iOS device, go to **Settings**, choose **Privacy**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="effcb-115">För Android enheter går du till **Inställningar**, välj **Appar och meddelanden**, **Avancerat**, **Behörighetshanteraren** och **Kamera** eller **Plats**.</span><span class="sxs-lookup"><span data-stu-id="effcb-115">For Android devices go to **Settings**, choose **Apps & Notifications**, **Advanced**, **Permission Manager**, and then **Camera** or **Location**.</span></span>

<span data-ttu-id="effcb-116">Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] i en webbläsare måste du också ge [!INCLUDE[prod_short](includes/prod_short.md)] webbplatsbehörighet att komma åt kameran eller platsinformationen.</span><span class="sxs-lookup"><span data-stu-id="effcb-116">In addition, if you are using [!INCLUDE[prod_short](includes/prod_short.md)] in a browser, you must also grant the [!INCLUDE[prod_short](includes/prod_short.md)] site permission to access the camera or location information.</span></span> <span data-ttu-id="effcb-117">Om du vill visa eller ändra webbplatsbehörighet i Microsoft Edge webbläsaren, gå till **Inställningar**, välj **Webbplatsbehörigheter** och **Kamera** eller **Plats**.</span><span class="sxs-lookup"><span data-stu-id="effcb-117">To see or change a site's permissions in the Microsoft Edge browser, go to **Settings**, choose **Site Permissions**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="effcb-118">Observera att detta kan vara annorlunda i andra webbläsare.</span><span class="sxs-lookup"><span data-stu-id="effcb-118">Note that this might be different for other browsers.</span></span>

<span data-ttu-id="effcb-119">Som standard dyker enheten eller webbläsaren upp en begäran om åtkomst till dessa funktioner när användaren aktiverar dem för första gången.</span><span class="sxs-lookup"><span data-stu-id="effcb-119">By default, the device or browser will pop up a request to access these capabilities when the user activates them for the first time.</span></span>

> [!NOTE]  
> <span data-ttu-id="effcb-120">Vissa äldre webbläsare ger inte tillgång till kameran och platsen.</span><span class="sxs-lookup"><span data-stu-id="effcb-120">Some old browsers do not grant access to camera and location.</span></span> <span data-ttu-id="effcb-121">Kameran är till exempel inte tillgänglig i Internet Explorer eller den äldre Edge-webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="effcb-121">For example, camera is not available in Internet Explorer or the legacy Edge browser.</span></span>

## <a name="web-client-connection-not-secure"></a><span data-ttu-id="effcb-122">Webbklient anslutning inte säker</span><span class="sxs-lookup"><span data-stu-id="effcb-122">Web Client Connection not Secure</span></span>

<span data-ttu-id="effcb-123">Kamera- och platsfunktionerna är endast tillgängliga vid åtkomst till webbklienten via säkra SSL-anslutningar via SSL med hjälp av `https://` URI-schemat.</span><span class="sxs-lookup"><span data-stu-id="effcb-123">The camera and location capabilities are only available when accessing the Web Client through SSL secured HTTP connections, using the `https://` URI scheme.</span></span> 

<span data-ttu-id="effcb-124">Det enda undantaget anknyter till `http://localhost` används i utvecklings- och testsyfte.</span><span class="sxs-lookup"><span data-stu-id="effcb-124">The only exception is connecting to `http://localhost`, used for development and test purposes.</span></span>


## <a name="working-with-virtualization-technologies"></a><span data-ttu-id="effcb-125">Arbeta med virtualiseringsteknik</span><span class="sxs-lookup"><span data-stu-id="effcb-125">Working with Virtualization Technologies</span></span>

<span data-ttu-id="effcb-126">När du ansluter till [!INCLUDE[prod_short](includes/prod_short.md)] via fjärrskrivbord eller en annan virtualisering kanske inte åtkomsten till kameran eller platsen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="effcb-126">When connecting to [!INCLUDE[prod_short](includes/prod_short.md)] through Remote Desktop or another virtualization, the access to camera or location might not be available.</span></span> <span data-ttu-id="effcb-127">Använd i så fall det fysiska systemet i stället.</span><span class="sxs-lookup"><span data-stu-id="effcb-127">If this is the case, use the physical system instead.</span></span>

## <a name="antivirus-software"></a><span data-ttu-id="effcb-128">Antivirusprogram</span><span class="sxs-lookup"><span data-stu-id="effcb-128">Antivirus Software</span></span>
<span data-ttu-id="effcb-129">Vissa antivirusprogram blockerar som standardåtkomst till kameran och platsen.</span><span class="sxs-lookup"><span data-stu-id="effcb-129">Some antivirus software block access to camera and location by default.</span></span> <span data-ttu-id="effcb-130">Kom ihåg att kontrollera inställningarna för antivirusprogrammet.</span><span class="sxs-lookup"><span data-stu-id="effcb-130">Remember to check your antivirus software settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="effcb-131">Se även</span><span class="sxs-lookup"><span data-stu-id="effcb-131">See Also</span></span>
[<span data-ttu-id="effcb-132">Implementera kameran i AL</span><span class="sxs-lookup"><span data-stu-id="effcb-132">Implementing the Camera in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[<span data-ttu-id="effcb-133">Implementera platsen i AL</span><span class="sxs-lookup"><span data-stu-id="effcb-133">Implementing the Location in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)
