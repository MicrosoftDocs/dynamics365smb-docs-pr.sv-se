---
title: "Hantera användare och roller | Microsoft Docs"
description: "Lär dig hantera användare och rollcenter i Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/02/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e5efc3536203495dcec1be2f1dc680b35c39d4db
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="28900-103">Förstå användare, profiler och rollcenter</span><span class="sxs-lookup"><span data-stu-id="28900-103">Understanding Users, Profiles, and Role Centers</span></span>
<span data-ttu-id="28900-104">Personer i företaget som har tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)] är tilldelade en *profil* som ger åtkomst till ett *Rollcenter*.</span><span class="sxs-lookup"><span data-stu-id="28900-104">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span> <span data-ttu-id="28900-105">Som administratör kan du tilldela och ändra profiler i [!INCLUDE[d365fin](includes/d365fin_md.md)] och du kan lägga till och ta bort användare som en del av din [!INCLUDE[d365fin](includes/d365fin_md.md)]-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="28900-105">As an administrator, you can assign and change profiles in [!INCLUDE[d365fin](includes/d365fin_md.md)], and you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="28900-106">Lägga till användare</span><span class="sxs-lookup"><span data-stu-id="28900-106">Adding Users</span></span>
<span data-ttu-id="28900-107">Om du vill lägga till användare i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste företagets Office 365-administratör först skapa användare i Office 365 Admin Center.</span><span class="sxs-lookup"><span data-stu-id="28900-107">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)], your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="28900-108">Mer information finns i [Hantera användare och behörigheter](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="28900-108">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

## <a name="profiles"></a><span data-ttu-id="28900-109">Profiler</span><span class="sxs-lookup"><span data-stu-id="28900-109">Profiles</span></span>
<span data-ttu-id="28900-110">Profiler är samlingar av [!INCLUDE[d365fin](includes/d365fin_md.md)]-användare som delar samma Rollcenter.</span><span class="sxs-lookup"><span data-stu-id="28900-110">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="28900-111">Ett Rollcenter är en typ av sidan som du kan tillämpa på olika delar.</span><span class="sxs-lookup"><span data-stu-id="28900-111">A Role Center is a type of page on which you can place different parts.</span></span> <span data-ttu-id="28900-112">Varje del är en behållare, i vilken du kan hosta andra sidor eller fördefinierade systemdelar, som till exempel en Outlook-del eller delar för att lägga till uppgifter, meddelanden eller noteringar.</span><span class="sxs-lookup"><span data-stu-id="28900-112">Each part is a container in which you can host other pages or pre-defined system parts, such as an Outlook part or parts for adding tasks, notifications, or notes.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="28900-113">I den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du inte lägga till, redigera eller ta bort profiler.</span><span class="sxs-lookup"><span data-stu-id="28900-113">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="28900-114">Konfiguration och anpassning</span><span class="sxs-lookup"><span data-stu-id="28900-114">Configuration and Personalization</span></span>
<span data-ttu-id="28900-115">Begreppet användargränssnittsanpassning i [!INCLUDE[d365fin](includes/d365fin_md.md)] uppdelat i två delar:</span><span class="sxs-lookup"><span data-stu-id="28900-115">The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:</span></span>  

-   <span data-ttu-id="28900-116">Konfiguration som utförs av administratören</span><span class="sxs-lookup"><span data-stu-id="28900-116">Configuration, performed by the administrator</span></span>  

-   <span data-ttu-id="28900-117">Anpassning som utförs av användare</span><span class="sxs-lookup"><span data-stu-id="28900-117">Personalization, performed by users</span></span>  

<span data-ttu-id="28900-118">Administratören konfigurerar användargränssnittet för flera användare genom att anpassa användargränssnittet för en profil som användarna tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="28900-118">The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.</span></span>  

<span data-ttu-id="28900-119">Användare anpassa användargränssnittet för sin egen version genom att anpassa användargränssnittet under sin egen användarinloggning.</span><span class="sxs-lookup"><span data-stu-id="28900-119">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="28900-120">Den här anpassningen kan tas bort av administratören.</span><span class="sxs-lookup"><span data-stu-id="28900-120">This personalization can be deleted by the administrator.</span></span>  

## <a name="see-also"></a><span data-ttu-id="28900-121">Se även</span><span class="sxs-lookup"><span data-stu-id="28900-121">See Also</span></span>  
[<span data-ttu-id="28900-122">Hantera användare och behörigheter</span><span class="sxs-lookup"><span data-stu-id="28900-122">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
<!-- [Customize the User Interface](../customize-the-user-interface.md)   
 [Security Overview](../Security%20Overview.md)-->

