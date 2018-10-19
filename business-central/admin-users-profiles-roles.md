---
title: "Hantera användare och roller | Microsoft Docs"
description: "Lär dig hantera användare och rollcenter i Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="84d35-103">Förstå användare, profiler och rollcenter</span><span class="sxs-lookup"><span data-stu-id="84d35-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="84d35-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)] läggs användare till av en administratör som också ger användare tillgång till områden i [!INCLUDE[d365fin](includes/d365fin_md.md)] som de behöver i sitt arbete.</span><span class="sxs-lookup"><span data-stu-id="84d35-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="84d35-105">Åtkomst till funktioner styrs genom *användargrupper* och *profiler*.</span><span class="sxs-lookup"><span data-stu-id="84d35-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="84d35-106">Som administratör kan du tilldela och ändra profiler i [!INCLUDE[d365fin](includes/d365fin_md.md)]-prenumeration och du kan lägga till och ta bort användare som en del av din användargrupp.</span><span class="sxs-lookup"><span data-stu-id="84d35-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="84d35-107">Lägga till användare</span><span class="sxs-lookup"><span data-stu-id="84d35-107">Adding Users</span></span>

<span data-ttu-id="84d35-108">Om du vill lägga till användare i [!INCLUDE[d365fin](includes/d365fin_md.md)] online, måste företagets Office 365-administratör först skapa användare i Office 365 Admin Center.</span><span class="sxs-lookup"><span data-stu-id="84d35-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="84d35-109">Mer information finns i [Lägg till användare till Office 365 för företag](https://aka.ms/CreateOffice365Users)</span><span class="sxs-lookup"><span data-stu-id="84d35-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="84d35-110">Administratören kan sedan tilldela behörigheter till varje användare och användargrupper.</span><span class="sxs-lookup"><span data-stu-id="84d35-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="84d35-111">Mer information finns i [Hantera användare och behörigheter](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="84d35-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="84d35-112">Användare av lokala distributioner</span><span class="sxs-lookup"><span data-stu-id="84d35-112">Users of on-premises deployments</span></span>

<span data-ttu-id="84d35-113">Vid lokal distribution av [!INCLUDE[d365fin](includes/d365fin_md.md)], kan administratören välja mellan olika autentiseringsmetoder för användare.</span><span class="sxs-lookup"><span data-stu-id="84d35-113">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="84d35-114">När du sedan skapar en användare, tillhandahåller du olika information beroende på vilken autentiseringstyp du använder i den specifika [!INCLUDE[server](includes/server.md)]-instansen.</span><span class="sxs-lookup"><span data-stu-id="84d35-114">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="84d35-115">Mer information finns på [autentisering och autentisering](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i avsnittet Administration av utvecklare och ITPro-innehåll för [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="84d35-115">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="84d35-116">Profiler</span><span class="sxs-lookup"><span data-stu-id="84d35-116">Profiles</span></span>

<span data-ttu-id="84d35-117">Personer i företaget som har tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)] är tilldelade en *profil* som ger åtkomst till ett *Rollcenter*.</span><span class="sxs-lookup"><span data-stu-id="84d35-117">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="84d35-118">Profiler är samlingar av [!INCLUDE[d365fin](includes/d365fin_md.md)]-användare som delar samma Rollcenter.</span><span class="sxs-lookup"><span data-stu-id="84d35-118">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="84d35-119">Ett rollcenter är startpunkten och startsidan för [!INCLUDE[d365fin](includes/d365fin_md.md)] som ger dig snabb åtkomst till dina viktigaste uppgifter och visar olika kunskap och nyckeltal (KPI) om ändringarna.</span><span class="sxs-lookup"><span data-stu-id="84d35-119">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="84d35-120">I den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] online kan du inte lägga till, redigera eller ta bort profiler.</span><span class="sxs-lookup"><span data-stu-id="84d35-120">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="84d35-121">Konfiguration och anpassning</span><span class="sxs-lookup"><span data-stu-id="84d35-121">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
<span data-ttu-id="84d35-122">Användare anpassa användargränssnittet för sin egen version genom att anpassa användargränssnittet under sin egen användarinloggning.</span><span class="sxs-lookup"><span data-stu-id="84d35-122">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="84d35-123">Den här anpassningen kan tas bort av administratören.</span><span class="sxs-lookup"><span data-stu-id="84d35-123">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="84d35-124">Mer information finns i [Anpassa arbetsytan](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="84d35-124">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="84d35-125">Se även</span><span class="sxs-lookup"><span data-stu-id="84d35-125">See Also</span></span>  
[<span data-ttu-id="84d35-126">Hantera användare och behörigheter</span><span class="sxs-lookup"><span data-stu-id="84d35-126">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="84d35-127">Hantera anpassning som administratör</span><span class="sxs-lookup"><span data-stu-id="84d35-127">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="84d35-128">Anpassa din arbetsyta</span><span class="sxs-lookup"><span data-stu-id="84d35-128">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

