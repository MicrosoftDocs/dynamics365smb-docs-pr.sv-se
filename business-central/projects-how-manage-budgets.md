---
title: "Ställ in och hantera en budget för ett projekt | Microsoft Docs"
description: "Beskriver hur du planerar resurser och prognos och styr kostnader för ett projekt genom att skapa en budget för varje projekt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1dbca885e47b19c9ce1b78d092d1dc15dc23449e
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="manage-job-budgets"></a><span data-ttu-id="80ce6-103">Hantera projektbudgetar</span><span class="sxs-lookup"><span data-stu-id="80ce6-103">Manage Job Budgets</span></span>
<span data-ttu-id="80ce6-104">Du kan lägga upp en budget för varje projekt.</span><span class="sxs-lookup"><span data-stu-id="80ce6-104">You can set up a budget for each job.</span></span> <span data-ttu-id="80ce6-105">Budgeten används för att planera de resurser du tilldelar ett projekt.</span><span class="sxs-lookup"><span data-stu-id="80ce6-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="80ce6-106">Budgeten kan antingen vara allmän med få poster eller innehålla fler poster som är indelade i aktivitetsnivåer.</span><span class="sxs-lookup"><span data-stu-id="80ce6-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="80ce6-107">Du kan sedan jämföra budgeterade belopp med den faktiska förbrukningen enligt registreringen i projektjournalen.</span><span class="sxs-lookup"><span data-stu-id="80ce6-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="80ce6-108">Genom att övervaka skillnader mellan faktisk förbrukning och budgeterad användning kan du kontrollera pågående projekt och förbättra kvaliteten hos framtida projekt genom att minska risken för att kostnader underskattas.</span><span class="sxs-lookup"><span data-stu-id="80ce6-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="80ce6-109">Efterföljande procedur beskriver hur du beräknar budgeterade kostnader under planering.</span><span class="sxs-lookup"><span data-stu-id="80ce6-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="80ce6-110">Mer information om registrering av budgeterade jämfört med faktiska projektpriser och -kostnader finns i [Så här registrerar du förbrukning för projekt](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="80ce6-110">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <a name="JobBudgetCosts"></a> <span data-ttu-id="80ce6-111">Att ange budgeterade kostnader för ett projekt</span><span class="sxs-lookup"><span data-stu-id="80ce6-111">To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="80ce6-112">När en kund vill veta priset på ett projekt som kommer att faktureras baserat på förbrukning, måste du fastställa de budgeterade kostnaderna för projektet.</span><span class="sxs-lookup"><span data-stu-id="80ce6-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="80ce6-113">Du använder fönstret **Projektaktivitetsrader** om du vill göra detta.</span><span class="sxs-lookup"><span data-stu-id="80ce6-113">You use the **Job Task Lines** window to do this.</span></span>

1. <span data-ttu-id="80ce6-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Projekt** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="80ce6-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="80ce6-115">Öppna ett relevant projekt.</span><span class="sxs-lookup"><span data-stu-id="80ce6-115">Open a relevant job.</span></span>
3. <span data-ttu-id="80ce6-116">Markera en projektrad av typen Bokföring och välj sedan åtgärden **Projektplaneringsrader**.</span><span class="sxs-lookup"><span data-stu-id="80ce6-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="80ce6-117">Fyll i fälten på en ny rad efter behov.</span><span class="sxs-lookup"><span data-stu-id="80ce6-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="80ce6-118">Se följande information för fältet **Radtyp**.</span><span class="sxs-lookup"><span data-stu-id="80ce6-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="80ce6-119">Typ av rad</span><span class="sxs-lookup"><span data-stu-id="80ce6-119">Line Type</span></span> | <span data-ttu-id="80ce6-120">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="80ce6-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="80ce6-121">**Både Budget och Fakturerbart**</span><span class="sxs-lookup"><span data-stu-id="80ce6-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="80ce6-122">Kostnads- och prisbelopp som har angetts på planeringsraderna är de budgeterade kostnaderna för denna specifika planeringsrad.</span><span class="sxs-lookup"><span data-stu-id="80ce6-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="80ce6-123">Prisbeloppet faktureras.</span><span class="sxs-lookup"><span data-stu-id="80ce6-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="80ce6-124">**Budget**</span><span class="sxs-lookup"><span data-stu-id="80ce6-124">**Budget**</span></span> |<span data-ttu-id="80ce6-125">Kunden debiteras inte för användning.</span><span class="sxs-lookup"><span data-stu-id="80ce6-125">The customer is not charged for usage.</span></span> <span data-ttu-id="80ce6-126">Förbrukningen överförs inte till en faktura, men den kommer fortfarande att användas i PIA-beräkningen.</span><span class="sxs-lookup"><span data-stu-id="80ce6-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="80ce6-127">**Fakturerbart**</span><span class="sxs-lookup"><span data-stu-id="80ce6-127">**Billable**</span></span> |<span data-ttu-id="80ce6-128">Kunden debiteras för användning.</span><span class="sxs-lookup"><span data-stu-id="80ce6-128">The customer is charged for usage.</span></span> <span data-ttu-id="80ce6-129">Förbrukningen överförs till fakturan baserat på det antal som finns angivet i fältet Antal att överföra till faktura.</span><span class="sxs-lookup"><span data-stu-id="80ce6-129">Usage is transferred to the invoice, based on the quantity specified in the Qty. to Transfer to Invoice field.</span></span> |

> [!NOTE]  
>   <span data-ttu-id="80ce6-130">Fältet **Planeringsdatum** för planeringsraden innehåller datumet då förbrukning som relateras till planeringsraden förväntas slutföras.</span><span class="sxs-lookup"><span data-stu-id="80ce6-130">The **Planning Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="80ce6-131">Det är också datumet då planeringsraden kan överföras till en försäljningsfaktura och bokföras.</span><span class="sxs-lookup"><span data-stu-id="80ce6-131">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="80ce6-132">När du fyller i fältet **Antal** kommer all information om totalt pris och total kostnad att beräknas och fyllas i för planeringsraden.</span><span class="sxs-lookup"><span data-stu-id="80ce6-132">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="80ce6-133">De kan redigeras när det passar dig.</span><span class="sxs-lookup"><span data-stu-id="80ce6-133">You can edit them at any time.</span></span>

<span data-ttu-id="80ce6-134">I fönstret **Projektkort** kan du nu se en översikt över de totala budgeterade kostnaderna, budgeterat pris, fakturerbar kostnad och fakturerbart pris för varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="80ce6-134">In the **Job Card** window, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="80ce6-135">Mer information om registrering av budgeterade jämfört med faktiska projektpriser och -kostnader finns i [Så här registrerar du förbrukning för projekt](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="80ce6-135">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="80ce6-136">Se även</span><span class="sxs-lookup"><span data-stu-id="80ce6-136">See Also</span></span>
[<span data-ttu-id="80ce6-137">Projekthantering</span><span class="sxs-lookup"><span data-stu-id="80ce6-137">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="80ce6-138">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="80ce6-138">Finance</span></span>](finance.md)  
<span data-ttu-id="80ce6-139">[Inköp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="80ce6-139">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="80ce6-140">[Försäljning](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="80ce6-140">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="80ce6-141">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="80ce6-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
