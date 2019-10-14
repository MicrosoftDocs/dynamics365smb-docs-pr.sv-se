---
title: Fel sökning av synkroniseringsfel | Microsoft Docs
description: Innehåller vägledning för att identifiera och lösa synkroniseringsfel.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 729a767c0cb4bb330a463e14c7eb6a4f8fd7d909
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304273"
---
# <a name="troubleshooting-synchronization-errors"></a><span data-ttu-id="566fd-103">Felsöka synkroniseringsfel</span><span class="sxs-lookup"><span data-stu-id="566fd-103">Troubleshooting Synchronization Errors</span></span>
<span data-ttu-id="566fd-104">Det finns många rörliga delar som används för att integrera [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] och ibland kan det bli fel.</span><span class="sxs-lookup"><span data-stu-id="566fd-104">There are lots of moving parts involved in integrating [!INCLUDE[d365fin](includes/d365fin_md.md)] with [!INCLUDE[crm_md](includes/crm_md.md)], and sometimes things go wrong.</span></span> <span data-ttu-id="566fd-105">I det här avsnittet beskrivs några vanliga fel som uppstår och du får tips om hur du åtgärdar dem.</span><span class="sxs-lookup"><span data-stu-id="566fd-105">This topic points out some of the typical errors that occur and gives some pointers for how to fix them.</span></span>

<span data-ttu-id="566fd-106">Fel inträffar ofta antingen på grund av något som en användare har gjort för att sammanföra poster, eller något är fel med hur integreringen har upprättats.</span><span class="sxs-lookup"><span data-stu-id="566fd-106">Errors often occur either because of something that a user has done to coupled records or something is wrong with how the integration is set up.</span></span> <span data-ttu-id="566fd-107">För fel som rör kopplade poster kan användare matcha dem själva.</span><span class="sxs-lookup"><span data-stu-id="566fd-107">For errors related to coupled records, users can resolve those themselves.</span></span> <span data-ttu-id="566fd-108">Dessa fel orsakas av åtgärder som att ta bort en post i en, men inte både och, affärsappar och sedan synkronisera.</span><span class="sxs-lookup"><span data-stu-id="566fd-108">These errors are caused by actions such as deleting a record in one, but not both, business apps and then synchronizing.</span></span> <span data-ttu-id="566fd-109">För mer information, se [Visa status för en synkronisering](admin-how-to-view-synchronization-status.md).</span><span class="sxs-lookup"><span data-stu-id="566fd-109">For more information, see [View the Status of a Synchronization](admin-how-to-view-synchronization-status.md).</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

<span data-ttu-id="566fd-110">Fel som rör hur integreringen ställs in kräver vanligt vis en administratörs uppmärksamhet.</span><span class="sxs-lookup"><span data-stu-id="566fd-110">Errors that are related to how the integration is set up typically require an administrator's attention.</span></span> <span data-ttu-id="566fd-111">Du kan visa dessa fel på sidan **Integreringssynkroniseringsfel**.</span><span class="sxs-lookup"><span data-stu-id="566fd-111">You can view these errors on the **Integration Synchronization Errors** page.</span></span> <span data-ttu-id="566fd-112">Exempel på typiska problem är:</span><span class="sxs-lookup"><span data-stu-id="566fd-112">Examples of some typical issues include:</span></span>  
  
* <span data-ttu-id="566fd-113">De behörigheter och roller som tilldelats till användare är felaktiga.</span><span class="sxs-lookup"><span data-stu-id="566fd-113">The permissions and roles assigned to users are not correct.</span></span>  
* <span data-ttu-id="566fd-114">Administratörskontot har angetts som integrationsanvändare.</span><span class="sxs-lookup"><span data-stu-id="566fd-114">The administrator account was specified as the integration user.</span></span>  
* <span data-ttu-id="566fd-115">Lösenordet för integrationsanvändaren anges för att kräva en ändring när användaren loggar in.</span><span class="sxs-lookup"><span data-stu-id="566fd-115">The integration user’s password is set to require a change when the user signs in.</span></span>  
* <span data-ttu-id="566fd-116">Valutakurserna för valutor har inte angetts i den ena eller den andra appen.</span><span class="sxs-lookup"><span data-stu-id="566fd-116">The exchange rates for currencies are not specified in one or the other app.</span></span>  
  
<span data-ttu-id="566fd-117">Du måste lösa felen manuellt, men det finns ett par sätt på vilka sidan kan hjälpa dig.</span><span class="sxs-lookup"><span data-stu-id="566fd-117">You must manually resolve the errors, but there are a few ways in which the page helps you.</span></span> <span data-ttu-id="566fd-118">Som exempel:</span><span class="sxs-lookup"><span data-stu-id="566fd-118">For example:</span></span>  

* <span data-ttu-id="566fd-119">Fälten **Källa** och **mål** kan innehålla länkar till posten där felet hittades.</span><span class="sxs-lookup"><span data-stu-id="566fd-119">The **Source** and **Destination** fields may contain links to the record where the error was found.</span></span> <span data-ttu-id="566fd-120">Klicka på länken för att öppna posten och undersöka felet.</span><span class="sxs-lookup"><span data-stu-id="566fd-120">Click the link to open the record and investigate the error.</span></span>  
* <span data-ttu-id="566fd-121">Åtgärderna **Ta bort transaktioner som är äldre än 7 dagar** och **Ta alla transaktioner** rensar listan.</span><span class="sxs-lookup"><span data-stu-id="566fd-121">The **Delete Entries Older than 7 Days** and the **Delete All Entries** actions will clean up the list.</span></span> <span data-ttu-id="566fd-122">Vanligtvis använder du dessa åtgärder när du har löst orsaken till ett fel som påverkar många poster.</span><span class="sxs-lookup"><span data-stu-id="566fd-122">Typically, you use these actions after you have resolved the cause of an error that affects many records.</span></span> <span data-ttu-id="566fd-123">Var försiktig.</span><span class="sxs-lookup"><span data-stu-id="566fd-123">Use caution, however.</span></span> <span data-ttu-id="566fd-124">De här åtgärderna kan ta bort fel som fortfarande är relevanta.</span><span class="sxs-lookup"><span data-stu-id="566fd-124">These actions might delete errors that are still relevant.</span></span>

## <a name="see-also"></a><span data-ttu-id="566fd-125">Se även</span><span class="sxs-lookup"><span data-stu-id="566fd-125">See Also</span></span>
<span data-ttu-id="566fd-126">[Integrera med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span><span class="sxs-lookup"><span data-stu-id="566fd-126">[Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span></span>  
<span data-ttu-id="566fd-127">[Ställa in konton för integrering med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span><span class="sxs-lookup"><span data-stu-id="566fd-127">[Setting Up User Accounts for Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span></span>  
<span data-ttu-id="566fd-128">[Ställ in en anslutning till [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span><span class="sxs-lookup"><span data-stu-id="566fd-128">[Set Up a Connection to [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span></span>  
[<span data-ttu-id="566fd-129">Koppla och synkronisera poster manuellt</span><span class="sxs-lookup"><span data-stu-id="566fd-129">Couple and Synchronize Records Manually</span></span>](admin-how-to-couple-and-synchronize-records-manually.md)  
[<span data-ttu-id="566fd-130">Visa status för en synkronisering</span><span class="sxs-lookup"><span data-stu-id="566fd-130">View the Status of a Synchronization</span></span>](admin-how-to-view-synchronization-status.md)  