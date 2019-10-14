---
title: Om kostnader för färdiga produktionsorder | Microsoft Docs
description: Att färdigställa produktionsordern är en viktig uppgift när det gäller att slutföra livscykeln för kostnadsberäkning för artikeln som tillverkas. Slutkostnader (inklusive avvikelser i standardkostnad, faktiska värden i en FIFO, genomsnittskostnader eller LIFO-kostnader) beräknas med hjälp av batch-jobbet Justera kostnad - Artikeltrans.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 509ee1cdbcf9c0ddd362435ed4d2319561a9e731
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302650"
---
# <a name="about-finished-production-order-costs"></a><span data-ttu-id="9b070-104">Om kostnader för färdiga produktionsorder</span><span class="sxs-lookup"><span data-stu-id="9b070-104">About Finished Production Order Costs</span></span>
<span data-ttu-id="9b070-105">Att färdigställa produktionsordern är en viktig uppgift när det gäller att slutföra livscykeln för kostnadsberäkning för artikeln som tillverkas.</span><span class="sxs-lookup"><span data-stu-id="9b070-105">Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced.</span></span> <span data-ttu-id="9b070-106">Slutkostnader, inklusive avvikelser i standardkostnad, faktiska värden i en FIFO, genomsnittlig eller LIFO-kostnad, beräknas med hjälp av batch-jobbet **Justera kostnad - artikeltransaktioner** som används för avstämning av kostnaderna för produktionsartiklar.</span><span class="sxs-lookup"><span data-stu-id="9b070-106">Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the **Adjust Cost - Item Entries** batch job, which allows for financial reconciliation of the costs of item production.</span></span> <span data-ttu-id="9b070-107">Om kostnadsjustering ska genomföras för en produktionsorder måste statusen vara **Färdig**.</span><span class="sxs-lookup"><span data-stu-id="9b070-107">For a production order to be considered for cost adjustment, the status must be **Finished**.</span></span> <span data-ttu-id="9b070-108">Det är därför viktigt att vid slutförande ändra statusen för en produktionsorder till **Färdig**.</span><span class="sxs-lookup"><span data-stu-id="9b070-108">It is therefore critical that upon completion, the status of a production order is changed to **Finished**.</span></span>  

## <a name="example"></a><span data-ttu-id="9b070-109">Exempel</span><span class="sxs-lookup"><span data-stu-id="9b070-109">Example</span></span>  
 <span data-ttu-id="9b070-110">Vid standardkostnad, när du t.ex. förbrukar material för att producera en artikel, överförs förenklat kostnaden för artikeln plus arbets- och overheadkostnader till PIA.</span><span class="sxs-lookup"><span data-stu-id="9b070-110">In a standard cost environment, when you consume material to produce an item, stated simply, the cost of the item plus labor and overhead go into WIP.</span></span> <span data-ttu-id="9b070-111">När artikeln tillverkas minskar PIA med beloppet för standardkostnaden för artikeln.</span><span class="sxs-lookup"><span data-stu-id="9b070-111">When the item is produced, WIP is reduced by the amount of the standard cost of the item.</span></span> <span data-ttu-id="9b070-112">De här kostnaderna får vanligtvis inte nollnetto.</span><span class="sxs-lookup"><span data-stu-id="9b070-112">Typically, these costs do not net to zero.</span></span> <span data-ttu-id="9b070-113">För att dessa kostnader inte ska få nollnetto måste du köra batchjobbet **Justera kostnad - artikeltransaktiner** och notera att endast produktionsorder med statusen **Färdig** ska beaktas för justering.</span><span class="sxs-lookup"><span data-stu-id="9b070-113">So that these costs can net to zero, you must run the **Adjust Cost - Item Entries** batch job, noting that only production orders with the status of **Finished** will be considered for adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9b070-114">Se även</span><span class="sxs-lookup"><span data-stu-id="9b070-114">See Also</span></span>  
[<span data-ttu-id="9b070-115">Hantera lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="9b070-115">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="9b070-116">Produktion</span><span class="sxs-lookup"><span data-stu-id="9b070-116">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="9b070-117">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9b070-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
