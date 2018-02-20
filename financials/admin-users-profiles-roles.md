---
title: "Hantera användare och roller | Microsoft Docs"
description: "Lär dig hantera användare, profiler och rollcenter i Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b06c5ee737db74e5011c7854601a21bc04d8872a
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="users-profiles-and-role-centers-in-finance-and-operations-business-edition"></a><span data-ttu-id="71794-103">Användare, profiler och rollcenter i Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="71794-103">Users, Profiles, and Role Centers in Finance and Operations, Business edition</span></span>
<span data-ttu-id="71794-104">Personer i företaget som har tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)] är tilldelade en *profil* som ger åtkomst till ett *Rollcenter*.</span><span class="sxs-lookup"><span data-stu-id="71794-104">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span> <span data-ttu-id="71794-105">Som administratör kan du tilldela och ändra profiler i [!INCLUDE[d365fin](includes/d365fin_md.md)] och du kan lägga till och ta bort användare som en del av din [!INCLUDE[d365fin](includes/d365fin_md.md)]-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="71794-105">As an administrator, you can assign and change profiles in [!INCLUDE[d365fin](includes/d365fin_md.md)], and you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="71794-106">Lägga till användare</span><span class="sxs-lookup"><span data-stu-id="71794-106">Adding Users</span></span>
<span data-ttu-id="71794-107">Om du vill lägga till användare i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste företagets Office 365-administratör först skapa användare i Office 365 Admin Center.</span><span class="sxs-lookup"><span data-stu-id="71794-107">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)], your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="71794-108">Mer information finns i [Hantera användare och behörigheter](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="71794-108">For more information, see [Manage Users and Permissions](ui-how-users-permissions.md).</span></span>  

## <a name="profiles"></a><span data-ttu-id="71794-109">Profiler</span><span class="sxs-lookup"><span data-stu-id="71794-109">Profiles</span></span>
<span data-ttu-id="71794-110">Profiler är samlingar av [!INCLUDE[d365fin](includes/d365fin_md.md)]-användare som delar samma Rollcenter.</span><span class="sxs-lookup"><span data-stu-id="71794-110">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="71794-111">Ett Rollcenter är en typ av sidan som du kan tillämpa på olika delar.</span><span class="sxs-lookup"><span data-stu-id="71794-111">A Role Center is a type of page on which you can place different parts.</span></span> <span data-ttu-id="71794-112">Varje del är en behållare, i vilken du kan hosta andra sidor eller fördefinierade systemdelar, som till exempel en Outlook-del eller delar för att lägga till uppgifter, meddelanden eller noteringar.</span><span class="sxs-lookup"><span data-stu-id="71794-112">Each part is a container in which you can host other pages or pre-defined system parts, such as an Outlook part or parts for adding tasks, notifications, or notes.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="71794-113">I den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du inte lägga till, redigera eller ta bort profiler.</span><span class="sxs-lookup"><span data-stu-id="71794-113">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="71794-114">Konfiguration och anpassning</span><span class="sxs-lookup"><span data-stu-id="71794-114">Configuration and Personalization</span></span>
<span data-ttu-id="71794-115">Begreppet användargränssnittsanpassning i [!INCLUDE[d365fin](includes/d365fin_md.md)] uppdelat i två delar:</span><span class="sxs-lookup"><span data-stu-id="71794-115">The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:</span></span>  

-   <span data-ttu-id="71794-116">Konfiguration som utförs av administratören</span><span class="sxs-lookup"><span data-stu-id="71794-116">Configuration, performed by the administrator</span></span>  

-   <span data-ttu-id="71794-117">Anpassning som utförs av användare</span><span class="sxs-lookup"><span data-stu-id="71794-117">Personalization, performed by users</span></span>  

<span data-ttu-id="71794-118">Administratören konfigurerar användargränssnittet för flera användare genom att anpassa användargränssnittet för en profil som användarna tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="71794-118">The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.</span></span>  

<span data-ttu-id="71794-119">Användare anpassa användargränssnittet för sin egen version genom att anpassa användargränssnittet under sin egen användarinloggning.</span><span class="sxs-lookup"><span data-stu-id="71794-119">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="71794-120">Den här anpassningen kan tas bort av administratören.</span><span class="sxs-lookup"><span data-stu-id="71794-120">This personalization can be deleted by the administrator.</span></span>  

## <a name="see-also"></a><span data-ttu-id="71794-121">Se även</span><span class="sxs-lookup"><span data-stu-id="71794-121">See Also</span></span>  
[<span data-ttu-id="71794-122">Hantera användare och behörigheter</span><span class="sxs-lookup"><span data-stu-id="71794-122">Manage Users and Permissions</span></span>](ui-how-users-permissions.md)  
<!-- [Customize the User Interface](../customize-the-user-interface.md)   
 [Security Overview](../Security%20Overview.md)-->

