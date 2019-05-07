---
title: Så här granskar och anpassar du befintliga databasdata | Microsoft Docs
description: När du skapar ett konfigurationspaket för en lösning kan du visa och anpassa tillgängliga databasdata så att dessa stämmer överens med dina kundbehov. Databastabellen måste vara kopplad till en sida.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: admin-how-to-create-custom-company-configuration-packages
ms.openlocfilehash: 95b16dc77bcdb0051447a4f153dd720661c52cf9
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "917942"
---
# <a name="review-and-customize-existing-database-data"></a><span data-ttu-id="6458a-104">Så här granskar och anpassar du befintliga databasdata</span><span class="sxs-lookup"><span data-stu-id="6458a-104">Review and Customize Existing Database Data</span></span>
<span data-ttu-id="6458a-105">När du skapar ett konfigurationspaket för en lösning kan du visa och anpassa tillgängliga databasdata så att dessa stämmer överens med dina kundbehov.</span><span class="sxs-lookup"><span data-stu-id="6458a-105">As you create a configuration package for a solution, you can view and customize the available database data to suit your customer needs.</span></span> <span data-ttu-id="6458a-106">Databastabellen måste vara kopplad till en sida.</span><span class="sxs-lookup"><span data-stu-id="6458a-106">The database table has to have an associated page.</span></span>  

### <a name="to-customize-data-in-the-database"></a><span data-ttu-id="6458a-107">Så här kan du anpassa data i databasen</span><span class="sxs-lookup"><span data-stu-id="6458a-107">To customize data in the database</span></span>  

1.  <span data-ttu-id="6458a-108">Identifiera tabellerna med data som du vill visa eller anpassa i konfigurationskalkylarket.</span><span class="sxs-lookup"><span data-stu-id="6458a-108">In the configuration worksheet, identify the tables whose data that you want to view or customize.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6458a-109">Se till att varje tabell tilldelats ett sid-ID.</span><span class="sxs-lookup"><span data-stu-id="6458a-109">Make sure that each table has a page ID assigned to it.</span></span> <span data-ttu-id="6458a-110">Som standarden [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell fylls detta värdet i automatiskt.</span><span class="sxs-lookup"><span data-stu-id="6458a-110">For standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables, this value is automatically filled in.</span></span> <span data-ttu-id="6458a-111">För anpassade tabeller måste du ange ID.</span><span class="sxs-lookup"><span data-stu-id="6458a-111">For custom tables, you have to provide the ID.</span></span>  

2.  <span data-ttu-id="6458a-112">Välj **Databasdata** på fliken **Åtgärder** i gruppen **Visa**.</span><span class="sxs-lookup"><span data-stu-id="6458a-112">On the **Actions** tab, in the **Show** group, choose **Database Data**.</span></span>  

     <span data-ttu-id="6458a-113">Sidan [!INCLUDE[d365fin](includes/d365fin_md.md)] för sidan öppnas.</span><span class="sxs-lookup"><span data-stu-id="6458a-113">The [!INCLUDE[d365fin](includes/d365fin_md.md)] page for the page opens.</span></span>  

3.  <span data-ttu-id="6458a-114">Granska den tillgängliga informationen.</span><span class="sxs-lookup"><span data-stu-id="6458a-114">Review the available information.</span></span> <span data-ttu-id="6458a-115">Ändra den efter behov genom att ta bort transaktioner som inte är relevanta eller lägga till nya.</span><span class="sxs-lookup"><span data-stu-id="6458a-115">Modify it as necessary by deleting records that are not relevant or by adding new ones.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6458a-116">Se även</span><span class="sxs-lookup"><span data-stu-id="6458a-116">See Also</span></span>  
 [<span data-ttu-id="6458a-117">Så här hanterar du företagskonfigurationen i ett kalkylark</span><span class="sxs-lookup"><span data-stu-id="6458a-117">Manage Company Configuration in a Worksheet</span></span>](admin-how-to-manage-company-configuration-in-a-worksheet.md)
