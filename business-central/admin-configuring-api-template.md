---
title: Konfigurera API-mallar | Microsoft Docs
description: Beskriver stegen du måste göra för att konfigurera API-mallar för Dynamics 365 Business Central.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: ef6b6d89ccea59de6a87c062cc6e29a27abe2c88
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "921392"
---
# <a name="configuring-api-templates"></a><span data-ttu-id="ca7de-103">Konfigurera API-mallar</span><span class="sxs-lookup"><span data-stu-id="ca7de-103">Configuring API Templates</span></span>
<span data-ttu-id="ca7de-104">API-bibliotek för [!INCLUDE[d365fin_md](includes/d365fin_md.md)] ger en förenklad representation av de underliggande enheterna.</span><span class="sxs-lookup"><span data-stu-id="ca7de-104">The API library for [!INCLUDE[d365fin_md](includes/d365fin_md.md)] provides a simplified representation of the underlying entities.</span></span> <span data-ttu-id="ca7de-105">Alla egenskaper i programmet är inte tillgängliga via den associerade API.</span><span class="sxs-lookup"><span data-stu-id="ca7de-105">All the properties in the application are not exposed through the associated API.</span></span> <span data-ttu-id="ca7de-106">Sidan **API-inställningar** låter dig definiera mallar som används för att fylla i tomma egenskaper på en enhet när du skapar en POST-åtgärd via API.</span><span class="sxs-lookup"><span data-stu-id="ca7de-106">The **API Setup** page allows you to define templates that are used to populate empty properties on an entity when you create a POST action through the API.</span></span> 

<span data-ttu-id="ca7de-107">Till exempel en konfigurationsmall har definierats för artikelenheten när en ny post skapas genom artiklarnas API, alla egenskaper för ny artikel som inte har definierats i API får fyllas på från den valda mallen.</span><span class="sxs-lookup"><span data-stu-id="ca7de-107">For example, if a configuration template is defined for the item entity, when a new item record is created through the items API, any properties for the new item that are not defined in the API call will be populated from the selected template.</span></span> <span data-ttu-id="ca7de-108">Om till exempel inget värde har angetts för fältet **Produktbokföringsmall** via API:n, men värdet som definieras i den valda mallen och sedan används den bokföringsmall som definierats i mallen till det nya objektet.</span><span class="sxs-lookup"><span data-stu-id="ca7de-108">If, for example, no value is defined for the **Gen. Prod. Posting Group** field through the API, but a value is defined in the selected template, then the posting group value defined in the template will be applied to the new item.</span></span> 

## <a name="setting-up-the-entity-template"></a><span data-ttu-id="ca7de-109">Konfigurera enhetsmall</span><span class="sxs-lookup"><span data-stu-id="ca7de-109">Setting up the Entity Template</span></span>
<span data-ttu-id="ca7de-110">Om du vill använda mallar med API-biblioteket, måste du först ställa in och ange egenskaper för mallarna.</span><span class="sxs-lookup"><span data-stu-id="ca7de-110">To use templates with the API library, you must first set up and define properties for the templates.</span></span> <span data-ttu-id="ca7de-111">Du kan ställa in dessa mallar på sidan **Konfigurationsmallar**.</span><span class="sxs-lookup"><span data-stu-id="ca7de-111">You can set up these templates on the **Configuration Templates** page.</span></span> <span data-ttu-id="ca7de-112">Mer information finns också i [Så här förbereder du migrering av kunddata](admin-use-templates-to-prepare-customer-data-for-migration.md).</span><span class="sxs-lookup"><span data-stu-id="ca7de-112">For more information, see [Prepare to Migrate Customer Data](admin-use-templates-to-prepare-customer-data-for-migration.md).</span></span> 

## <a name="assign-the-template-to-an-api"></a><span data-ttu-id="ca7de-113">Tilldela mallen till en API</span><span class="sxs-lookup"><span data-stu-id="ca7de-113">Assign the template to an API</span></span>

<span data-ttu-id="ca7de-114">Om du vill tilldela en mall till en API måste du gå igenom följande steg.</span><span class="sxs-lookup"><span data-stu-id="ca7de-114">To assign a template to an API, you must go through the following steps.</span></span>

1. <span data-ttu-id="ca7de-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **API-inställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ca7de-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **API Setup**, and choose the related link.</span></span>
2. <span data-ttu-id="ca7de-116">Välja **nytt**, och välj sedan värdet **Order** för posten.</span><span class="sxs-lookup"><span data-stu-id="ca7de-116">Choose **New**, and then choose the **Order** value for the record.</span></span>  
<span data-ttu-id="ca7de-117">Om det finns mer än en mall som har valts för en API (Sid-ID), tillämpas mallarna i den ordning som definieras i kolumnen **Order**.</span><span class="sxs-lookup"><span data-stu-id="ca7de-117">If there is more than one template selected for an API (Page ID), the templates are applied in the order defined in the **Order** column.</span></span>   
<span data-ttu-id="ca7de-118">När varje mall används, används bara fältvärden som definieras i mallen för fält som inte redan har ett värde som definierats, antingen uttryckligen i API eller i en tidigare använd mall i ordern.</span><span class="sxs-lookup"><span data-stu-id="ca7de-118">When each template is applied, field values defined in the template are only applied to fields that have not already had a value defined, either explicitly in the API, or in a previously applied template in the order.</span></span> 
3. <span data-ttu-id="ca7de-119">Välj ett värde för **Sid-ID**.</span><span class="sxs-lookup"><span data-stu-id="ca7de-119">Select a **Page ID** value.</span></span>  
<span data-ttu-id="ca7de-120">Detta är sidan för API som mallen ska användas.</span><span class="sxs-lookup"><span data-stu-id="ca7de-120">This is the page for the API to which the template will be applied.</span></span> <span data-ttu-id="ca7de-121">Sökning **Sid-ID** visar en lista över alla API:er i biblioteket.</span><span class="sxs-lookup"><span data-stu-id="ca7de-121">The **Page ID** lookup provides a list of all APIs available in the library.</span></span>
4. <span data-ttu-id="ca7de-122">Välj ett värde i fältet **Mallkod**.</span><span class="sxs-lookup"><span data-stu-id="ca7de-122">Select a value in the **Template Code** field.</span></span>  
<span data-ttu-id="ca7de-123">Mallkod är koden för den mall som definierats på sidan **Konfigurationsmallar**.</span><span class="sxs-lookup"><span data-stu-id="ca7de-123">The template code is the code for the template that was defined on the **Configuration Templates** page.</span></span> <span data-ttu-id="ca7de-124">Mallvärdena som är definierade som är kopplade till API.</span><span class="sxs-lookup"><span data-stu-id="ca7de-124">The template values defined are applied to the API.</span></span> 
5. <span data-ttu-id="ca7de-125">I fältet **villkor** anger du vilken mall som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ca7de-125">In the **Conditions** field, specify which template should be applied.</span></span>  
<span data-ttu-id="ca7de-126">Definierad mall kopplas till en ny post som skapas via API och bara om de villkor som anges i fältet **villkor** uppfylls av de värden som redan har angetts för den nya instansen av enheten.</span><span class="sxs-lookup"><span data-stu-id="ca7de-126">The defined template is applied to a new record created through the API if, and only if, the conditions defined in the **Conditions** field are met by the values already defined for the new instance of the entity.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca7de-127">Se även</span><span class="sxs-lookup"><span data-stu-id="ca7de-127">See Also</span></span>
[<span data-ttu-id="ca7de-128">API-dokumentation</span><span class="sxs-lookup"><span data-stu-id="ca7de-128">API Documentation</span></span>](/dynamics-nav/fin-graph)  
<span data-ttu-id="ca7de-129">[Utveckla anslutningsprogram för[!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span><span class="sxs-lookup"><span data-stu-id="ca7de-129">[Developing Connect Apps for [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span></span>  
[<span data-ttu-id="ca7de-130">Aktivera API:er</span><span class="sxs-lookup"><span data-stu-id="ca7de-130">Enabling the APIs</span></span>](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[<span data-ttu-id="ca7de-131">Slutpunkter för API:er</span><span class="sxs-lookup"><span data-stu-id="ca7de-131">Endpoints for the APIs</span></span>](/dynamics-nav/endpoints-apis-for-dynamics)  
[<span data-ttu-id="ca7de-132">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="ca7de-132">Setting Up a Company with RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="ca7de-133">Administration</span><span class="sxs-lookup"><span data-stu-id="ca7de-133">Administration</span></span>](admin-setup-and-administration.md)