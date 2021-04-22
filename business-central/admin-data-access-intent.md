---
title: Hantera åtkomstmetoden för databas i Business Central | Microsoft-dokument
description: Ändra åtkomstmetoden för databaser för rapporter, API-sidor och frågor.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 5fe04fc290f10324105d4d9ca01e13166bf2ad8f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773085"
---
# <a name="managing-database-access-intent"></a><span data-ttu-id="b5450-103">Hantera åtkomstmetod för databas</span><span class="sxs-lookup"><span data-stu-id="b5450-103">Managing Database Access Intent</span></span> 

<span data-ttu-id="b5450-104">Som Super-användare eller administratör kan du ändra åtkomstmetoden för databaser med avseende på rapporter, sidor av typen API och frågor för att förbättra tjänstens prestanda.</span><span class="sxs-lookup"><span data-stu-id="b5450-104">As a super user or administrator, you can change the database access intent on reports, pages of the type API, and queries to improve performance of the service.</span></span>

## <a name="overview"></a><span data-ttu-id="b5450-105">Översikt</span><span class="sxs-lookup"><span data-stu-id="b5450-105">Overview</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="b5450-106">kan konfigureras för att använda skrivskyddade kopior av den primära (skrivskyddade) databasen.</span><span class="sxs-lookup"><span data-stu-id="b5450-106">can be set up to use read-only replicas of the primary (read-write) database.</span></span> <span data-ttu-id="b5450-107">Användning av en databaskopia minskar belastningen på den primära databasen.</span><span class="sxs-lookup"><span data-stu-id="b5450-107">Using the database replica reduces the load on the primary database.</span></span> <span data-ttu-id="b5450-108">I vissa fall förbättras också prestandan när du visar data på klienten.</span><span class="sxs-lookup"><span data-stu-id="b5450-108">In some cases, it will also improve the performance when viewing data in the client.</span></span> <span data-ttu-id="b5450-109">Kopior är fördelaktiga för objekt, t. ex. rapporter, frågor och API-sidor, som används för att enbart visa (men inte ändra) data.</span><span class="sxs-lookup"><span data-stu-id="b5450-109">Replicas are beneficial for objects, like reports, queries, and API pages, that are used for viewing data only, not modifying data.</span></span>

<span data-ttu-id="b5450-110">När objekt körs bestämmer databasens åtkomstmetod huruvida en skrivskyddad kopia ska användas, om någon finns tillgänglig, eller om den primära databasen ska användas.</span><span class="sxs-lookup"><span data-stu-id="b5450-110">When objects run, the database access intent determines whether to use a read-only replica, if one is available, or the primary database.</span></span> <span data-ttu-id="b5450-111">Rapporter, API-sidor och frågor utvecklas med en fördefinierad metod för databasåtkomst (se [egenskapen DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span><span class="sxs-lookup"><span data-stu-id="b5450-111">Reports, API pages, and queries are developed with a predefined database access intent (see [DatabaseAccessIntent property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span></span>

<span data-ttu-id="b5450-112">Sidan **Metodlista för databasåtkomst** kan du åsidosätta den fördefinierade metoden för databasåtkomst för objekt när de körs.</span><span class="sxs-lookup"><span data-stu-id="b5450-112">The **Database Access Intent List** page lets you override the predefined database access intent for objects when they're run.</span></span>

<span data-ttu-id="b5450-113">Inom databasterminologin kallas denna funktion vanligen för *läsningsskalning*. Mer information om avläsning och metoder för dataåtkomst i [!INCLUDE[prod_short](includes/prod_short.md)] finns i [Använda Läsningsskalning för bättre prestanda](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) i [!INCLUDE[prod_short](includes/prod_short.md)]-hjälp för utvecklare och administration.</span><span class="sxs-lookup"><span data-stu-id="b5450-113">In database terms, this feature is commonly known as *read scale-out*. For more information about read-scale out and data access intent in [!INCLUDE[prod_short](includes/prod_short.md)], see [Utilizing Read Scale-Out for Better Performance](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in the [!INCLUDE[prod_short](includes/prod_short.md)] Developer and Administration help.</span></span>

## <a name="to-change-the-database-access-intent"></a><span data-ttu-id="b5450-114">Så här ändrar du åtkomstmetod för databaser</span><span class="sxs-lookup"><span data-stu-id="b5450-114">To change the database access intent</span></span>

1. <span data-ttu-id="b5450-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Metodlista för databasåtkomst** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b5450-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Database Access Intent List**, and then choose the related link.</span></span>

    <span data-ttu-id="b5450-116">På sidan visas alla rapporter, sidor och frågor.</span><span class="sxs-lookup"><span data-stu-id="b5450-116">The page lists all reports, pages, and queries.</span></span> <span data-ttu-id="b5450-117">I kolumnen **Åtkomstmetod** finns ett av följande värden:</span><span class="sxs-lookup"><span data-stu-id="b5450-117">The **Access Intent** column includes one of the following values:</span></span>

    |<span data-ttu-id="b5450-118">**Inställning**</span><span class="sxs-lookup"><span data-stu-id="b5450-118">**Setting**</span></span>|<span data-ttu-id="b5450-119">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="b5450-119">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="b5450-120">**Standard**</span><span class="sxs-lookup"><span data-stu-id="b5450-120">**Default**</span></span>|<span data-ttu-id="b5450-121">Anger att objektet använder den fördefinierade metoden för databasåtkomst.</span><span class="sxs-lookup"><span data-stu-id="b5450-121">Indicates that the object uses the predefined database access intent.</span></span>|
    |<span data-ttu-id="b5450-122">**Ej skrivskydd**</span><span class="sxs-lookup"><span data-stu-id="b5450-122">**Allow Write**</span></span>|<span data-ttu-id="b5450-123">Anger att objektet ska använda den primära databasen så att användaren kan ändra data.</span><span class="sxs-lookup"><span data-stu-id="b5450-123">Sets the object to use the primary database, allowing the user to modify data.</span></span>|
    |<span data-ttu-id="b5450-124">**Skrivskyddad**</span><span class="sxs-lookup"><span data-stu-id="b5450-124">**Read Only**</span></span>|<span data-ttu-id="b5450-125">Anger att objektet ska använda databaskopian, vilket innebär att användaren endast kan visa men inte ändra data.</span><span class="sxs-lookup"><span data-stu-id="b5450-125">Sets the object to use the database replica, which means that the user can only view data, not change data.</span></span>|

2. <span data-ttu-id="b5450-126">Välj åtgärden **Redigera lista**.</span><span class="sxs-lookup"><span data-stu-id="b5450-126">Choose the **Edit List** action.</span></span>

3. <span data-ttu-id="b5450-127">På sidan **Redigera – Metodlista för databasåtkomst** kan du ändra fältet **Åtkomstmetod** för objekten.</span><span class="sxs-lookup"><span data-stu-id="b5450-127">On the **Edit - Database Access Intent List** page, change the **Access Intent** field for the objects.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b5450-128">Om ett objekt som är redigerbart, exepelvis kundkortet, är **Skrivskyddat**, kommer den primära databasen fortfarande att användas oavsett vilken behörighet som används, vilket gör att användarna kan göra ändringar som vanligt.</span><span class="sxs-lookup"><span data-stu-id="b5450-128">If an object that is editable, like the Customer Card, is set to **Read Only**, the primary database will still be used, regardless of the access intent, allowing users to make changes as normal.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="b5450-129">Se Relaterad utbildning på [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="b5450-129">See Related Training at [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="b5450-130">Se även</span><span class="sxs-lookup"><span data-stu-id="b5450-130">See Also</span></span>
[<span data-ttu-id="b5450-131">Affärsfunktion</span><span class="sxs-lookup"><span data-stu-id="b5450-131">Business Functionality</span></span>](across-business-functionality.md)  
[<span data-ttu-id="b5450-132">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="b5450-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="b5450-133">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b5450-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b5450-134">Gör dig redo att göra affärer</span><span class="sxs-lookup"><span data-stu-id="b5450-134">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]