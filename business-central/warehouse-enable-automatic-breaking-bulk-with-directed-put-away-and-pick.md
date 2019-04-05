---
title: Aktivera Automatisk bryta ned volym med dirigerad artikelinförsel och plockning | Microsoft Docs
description: För lagerställen, som använder artikelinförsel och plockning, kan du dela upp en större enhet till mindre enheter, när du skapar lagerinstruktioner som uppfyller behoven hos källdokument, produktionsorder eller intern plockning och artikelinförsel.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: c328df334d1bb1be33ced814677c3ef3ea634799
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807667"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><span data-ttu-id="f24b9-103">Aktivera automatisk volymnedbrytning med dirigerad artikelinförsel och plockning</span><span class="sxs-lookup"><span data-stu-id="f24b9-103">Enable Automatic Breaking Bulk with Directed Put-away and Pick</span></span>
<span data-ttu-id="f24b9-104">För lagerställen, som använder artikelinförsel och plockning, kan [!INCLUDE[d365fin](includes/d365fin_md.md)] i olika situationer, automatiskt använda brytenhet, d.v.s. dela upp en större enhet till mindre enheter, när du skapar lagerinstruktioner som uppfyller behoven hos källdokument, produktionsorder eller intern plockning och artikelinförsel.</span><span class="sxs-lookup"><span data-stu-id="f24b9-104">For locations that use directed put-away and pick, [!INCLUDE[d365fin](includes/d365fin_md.md)] can, in various situations, automatically breakbulk, that is, break a larger unit of measure into smaller units of measure, when it creates warehouse instructions that fulfill the needs of source documents, production orders, or internal picks and put-aways.</span></span> <span data-ttu-id="f24b9-105">Med brytenhet menas ibland också samling av mindre måttenheter, om det behövs, för att uppfylla utgående förfrågningar, genom att analysera den större måttenheten i ursprungsdokumentet eller produktionsorder till de mindre enheter som är tillgängliga i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="f24b9-105">To breakbulk sometimes also means gathering smaller units of measure, if necessary, to meet outbound requests by breaking the larger unit of measure on the source document or production order into the smaller units of measure that are available in the warehouse.</span></span>   

## <a name="breakbulking-in-picks"></a><span data-ttu-id="f24b9-106">Enhetsbrytning vid plockning</span><span class="sxs-lookup"><span data-stu-id="f24b9-106">Breakbulking in Picks</span></span>  
<span data-ttu-id="f24b9-107">Om du vill lagra artiklar i flera olika måttenheter och tillåta dem att kombineras automatiskt efter behov vid plockning väljer du fältet **Tillåt brytenhet** på lagerställekortet.</span><span class="sxs-lookup"><span data-stu-id="f24b9-107">If you want to store items in several different units of measure and allow them to be automatically combined as needed in the picking process, select the **Allow Breakbulk** field on the location card.</span></span>  

<span data-ttu-id="f24b9-108">När en aktivitet ska utföras söker programmet automatiskt efter en artikel i den begärda måttenheten.</span><span class="sxs-lookup"><span data-stu-id="f24b9-108">To fulfill a task, the program automatically looks for an item in the same unit of measure.</span></span> <span data-ttu-id="f24b9-109">Om artikeln inte finns i denna enhet och du har valt fältet, föreslår programmet att du bryter ned en större måttenhet till den mindre måttenhet som behövs.</span><span class="sxs-lookup"><span data-stu-id="f24b9-109">But if it cannot find this form of the item, and this field is selected, the program will suggest that you break a larger unit of measure into the unit of measure that is needed.</span></span>  

<span data-ttu-id="f24b9-110">Om systemet bara hittar mindre måttenheter, föreslår programmet att du samlar ihop flera artiklar för att komma upp i den kvantitet som begärs på utleverans- eller produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="f24b9-110">If the system can only find smaller units of measure, it will suggest that you gather items to fulfill the quantity on the shipment or production order.</span></span> <span data-ttu-id="f24b9-111">Det som sedan sker är att den större måttenheten i ursprungsdokumentet bryts ned i mindre enheter för plockning.</span><span class="sxs-lookup"><span data-stu-id="f24b9-111">In effect, it breaks the larger unit of measure on the source document into smaller units for picking.</span></span>  

## <a name="breakbulking-in-put-aways"></a><span data-ttu-id="f24b9-112">Enhetsbrytning vid artikelinförsel</span><span class="sxs-lookup"><span data-stu-id="f24b9-112">Breakbulking in Put-aways</span></span>  
<span data-ttu-id="f24b9-113">Vid en artikelinförsel i distributionslagret föreslås automatiskt åtgärdsrader för Placera i den måttenhet som används i artikelinförseln, till exempel enheter, även om artiklarna inlevereras i en annan måttenhet.</span><span class="sxs-lookup"><span data-stu-id="f24b9-113">In the warehouse put-away, the program automatically suggests Place action lines in the put-away unit of measure, for example, pieces, even though the items arrive in a different unit of measure.</span></span>  

## <a name="breakbulking-in-movements"></a><span data-ttu-id="f24b9-114">Enhetsbrytning vid transport</span><span class="sxs-lookup"><span data-stu-id="f24b9-114">Breakbulking in Movements</span></span>  
<span data-ttu-id="f24b9-115">Enhetsbrytning sker också automatiskt vid påfyllningstransporter om fältet **Tillåt brytenhet** är valt på snabbfliken **Alternativ** på sidan **Beräkna lagerplatsåteranskaffning**.</span><span class="sxs-lookup"><span data-stu-id="f24b9-115">The program also breakbulks automatically in replenishment movements, if the **Allow Breakbulk** field is selected on the **Option** FastTab on the **Calculate Bin Replenishment** page.</span></span>  

<span data-ttu-id="f24b9-116">Du kan granska resultaten av enhetskonverteringsprocessen som övergångsrader för enhetsbrytning i instruktionerna för artikelinförsel, plockning eller transport.</span><span class="sxs-lookup"><span data-stu-id="f24b9-116">You can view the results of the conversion process from one unit of measure to another as intermediate breakbulk lines in the put-away, pick, or movement instructions.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f24b9-117">Om du väljer fältet **Sätt brytenhetsfilter** i huvudet för instruktionerna för distributionslagret, döljs enhetsbrytningsraderna om det uteslutande är den större måttenheten som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f24b9-117">If you select the **Set Breakbulk Filter** field on the warehouse instruction header, the program will hide the breakbulk lines whenever the larger unit of measure is going to be completely used.</span></span> <span data-ttu-id="f24b9-118">Exempel: Om en lastpall består av 12 enheter och samtliga enheter kommer att användas, dirigeras du under plockningen att ta en lastpall och placera 12 enheter.</span><span class="sxs-lookup"><span data-stu-id="f24b9-118">For example, if a pallet is 12 pieces and you are going to use all 12 pieces, the pick will then direct you to take 1 pallet and place 12 pieces.</span></span> <span data-ttu-id="f24b9-119">Om du bara ska plocka nio enheter döljs inte enhetsbrytningsraderna, även om du markerar fältet **Brytenhetsfilter**, eftersom du måste placera de återstående tre enheterna någonstans i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="f24b9-119">However, if you have to pick only 9 pieces, then the breakbulk lines will not be hidden, even if you have selected the **Breakbulk Filter** field, because you have to place the remaining three pieces somewhere in the warehouse.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f24b9-120">Om du vill att måttenheterna ska fungera så bra som möjligt i distributionslagret, också när du använder enhetsbrytning, ska du alltid försöka göra följande:</span><span class="sxs-lookup"><span data-stu-id="f24b9-120">If you want your units of measure to perform optimally in the warehouse, also in connection with the breakbulk functionality, you should wherever possible try to:</span></span>  
>   
> - <span data-ttu-id="f24b9-121">Ange den minsta måttenhet som du tror kommer att användas i distributionslagret som basmåttenhet för artiklar.</span><span class="sxs-lookup"><span data-stu-id="f24b9-121">Set up the base unit of measure for an item as the smallest unit of measure that you expect to handle in your warehouse processes.</span></span>  
> - <span data-ttu-id="f24b9-122">Ange alternativa måttenheter för artiklar som multiplar av basmåttenheten.</span><span class="sxs-lookup"><span data-stu-id="f24b9-122">Set up your alternative units of measure for the item as multiples of the base unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f24b9-123">Se även</span><span class="sxs-lookup"><span data-stu-id="f24b9-123">See Also</span></span>  
[<span data-ttu-id="f24b9-124">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="f24b9-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="f24b9-125">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="f24b9-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f24b9-126">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="f24b9-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="f24b9-127">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="f24b9-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="f24b9-128">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="f24b9-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="f24b9-129">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f24b9-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
