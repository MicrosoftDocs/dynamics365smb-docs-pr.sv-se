---
title: Administrativa aktiviteter i Dynamics 365 | Microsoft Docs
description: "Vissa uppgifter i [!INCLUDE[d365fin](includes/d365fin_md.md)] kräver central administration och inställningar. Se vad de är och lär dig vad du ska göra."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 09c3460a50088098bfe5c2fb633e76dccbac0794
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="setup-and-administration-in-dynamics-365-for-financials"></a><span data-ttu-id="b8047-104">Installation och administration i Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="b8047-104">Setup and Administration in Dynamics 365 for Financials</span></span>
<span data-ttu-id="b8047-105">Central administration utförs vanligtvis av en roll i företaget.</span><span class="sxs-lookup"><span data-stu-id="b8047-105">Central administration tasks are usually performed by one role in the company.</span></span> <span data-ttu-id="b8047-106">Omfattningen av dessa uppgifter kan vara beroende av företagets storlek och administratörens ansvarsområden.</span><span class="sxs-lookup"><span data-stu-id="b8047-106">The scope of these tasks can depend on the company's size and the administrator's job responsibilities.</span></span> <span data-ttu-id="b8047-107">Dessa uppgifter kan omfatta att hantera databassynkronisering av projekt och e-postköer, konfigurera användare, anpassa användargränssnittet och hantera krypteringsnycklar.</span><span class="sxs-lookup"><span data-stu-id="b8047-107">These tasks can include managing database synchronization of job and email queues, setting up users, customizing the user interface, and managing encryption keys.</span></span>  

<span data-ttu-id="b8047-108">Det är viktigt att ange rätt inställningsvärden från början för att en ny verksamhetsprogramvara ska fungera effektivt.</span><span class="sxs-lookup"><span data-stu-id="b8047-108">Entering the correct setup values from the start is important to the success of any new business software.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="b8047-109"> innehåller ett antal assisterade installationer som hjälper dig att ställa in grundläggande information.</span><span class="sxs-lookup"><span data-stu-id="b8047-109"> includes a number of setup guides that help you set up core data.</span></span> <span data-ttu-id="b8047-110">Mer information finns i [Lägga upp för Dynamics 365 for Financials](setup.md).</span><span class="sxs-lookup"><span data-stu-id="b8047-110">For more information, see [Setting Up Dynamics 365 for Financials](setup.md).</span></span>

<!--Whether you use [!INCLUDE[rim](../../includes/rim_md.md)] to implement setup values or you manually enter them in the new company, you can support your setup decisions with some general recommendations for selected setup fields that are known to potentially cause the solution to be inefficient if defined incorrectly.-->  

<span data-ttu-id="b8047-111">En superanvändare eller administratör kan konfigurera ramverket för datautbyte så att användare kan exportera och importera data i bank- och lönesystemfiler, till exempel för olika processer av likviditetsstyrning.</span><span class="sxs-lookup"><span data-stu-id="b8047-111">A super user or an administrator can set up the Data Exchange Framework to enable users to export and import data in bank and payroll files, for example for various cash management processes.</span></span>  

<span data-ttu-id="b8047-112">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="b8047-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="b8047-113">**Om du vill**</span><span class="sxs-lookup"><span data-stu-id="b8047-113">**To**</span></span>|<span data-ttu-id="b8047-114">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="b8047-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="b8047-115">Lägg till användargrupper och hantera behörigheter, åtkomst till data, tilldela roller.</span><span class="sxs-lookup"><span data-stu-id="b8047-115">Add users, manage permissions and access to data, assign roles.</span></span>|[<span data-ttu-id="b8047-116">Användare, profiler och rollcenter i Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="b8047-116">Users, Profiles, and Role Centers in Dynamics 365 for Financials</span></span>](admin-users-profiles-roles.md)|  
|<span data-ttu-id="b8047-117">Spåra alla direkta ändringar som användarna gör av data i databasen för att kunna identifiera var fel och dataändringar härrör från.</span><span class="sxs-lookup"><span data-stu-id="b8047-117">Track all direct modifications that users make to data in the database to identify the origin of errors and data changes.</span></span>|[<span data-ttu-id="b8047-118">Logga ändringar i Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="b8047-118">Logging Changes in Dynamics 365 for Financials</span></span>](across-log-changes.md)|  
|<span data-ttu-id="b8047-119">Stöd inställningsalternativ med rekommendationer för valda fält som eventuellt orsakar att lösningen är ineffektiv, om fältet felaktigt inställt</span><span class="sxs-lookup"><span data-stu-id="b8047-119">Support your setup decisions with recommendations for selected fields that are known to potentially cause the solution to be inefficient if set up incorrectly</span></span>|[<span data-ttu-id="b8047-120">Skapa komplexa moduler med hjälp av bästa metoder</span><span class="sxs-lookup"><span data-stu-id="b8047-120">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)|  
|<span data-ttu-id="b8047-121">Visa sidor, kodenheter och frågor som webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="b8047-121">Expose pages, codeunits, and queries as web services.</span></span>|[<span data-ttu-id="b8047-122">Så här: Publicerar du en webbtjänst</span><span class="sxs-lookup"><span data-stu-id="b8047-122">How to: Publish a Web Service</span></span>](across-how-publish-web-service.md)|  
|<span data-ttu-id="b8047-123">Skapa en SMTP-server för att aktivera e-postkommunikation i och utanför Dynamics 365 for Financials.</span><span class="sxs-lookup"><span data-stu-id="b8047-123">Set up an SMTP server to enable e-mail communication in and out of Dynamics 365 for Financials</span></span>| [<span data-ttu-id="b8047-124">Så här: Konfigurera e-post manuellt eller med hjälp av Assisterad konfiguration</span><span class="sxs-lookup"><span data-stu-id="b8047-124">How to: Set Up Email Manually or Using the Assisted Setup</span></span>](madeira-how-setup-email.md)|  
|<span data-ttu-id="b8047-125">Ange enstaka eller återkommande begäranden om att köra rapporter eller kodenheter.</span><span class="sxs-lookup"><span data-stu-id="b8047-125">Enter single or recurring requests to run reports or codeunits.</span></span>|[<span data-ttu-id="b8047-126">Använd jobbköer för att schemalägga uppgifter</span><span class="sxs-lookup"><span data-stu-id="b8047-126">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)|  
|<span data-ttu-id="b8047-127">Hantera, ta bort eller komprimera dokument</span><span class="sxs-lookup"><span data-stu-id="b8047-127">Manage, delete, or compress documents</span></span>|[<span data-ttu-id="b8047-128">Hantera dokument</span><span class="sxs-lookup"><span data-stu-id="b8047-128">Manage Documents</span></span>](admin-manage-documents.md)|  
|<span data-ttu-id="b8047-129">Skapa en ny affärsenhet med hjälp av mallar</span><span class="sxs-lookup"><span data-stu-id="b8047-129">Set up a new business unit using templates</span></span>|<span data-ttu-id="b8047-130">[Skapa nya företag i [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)</span><span class="sxs-lookup"><span data-stu-id="b8047-130">[Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)</span></span>|  

## <a name="see-also"></a><span data-ttu-id="b8047-131">Se även</span><span class="sxs-lookup"><span data-stu-id="b8047-131">See Also</span></span>
[<span data-ttu-id="b8047-132">Översikt över affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="b8047-132">Overview of Business Functionality</span></span>](madeira-business-functionality.md)  
[<span data-ttu-id="b8047-133">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="b8047-133">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="b8047-134">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b8047-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="b8047-135">[Välkommen till [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="b8047-135">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  
