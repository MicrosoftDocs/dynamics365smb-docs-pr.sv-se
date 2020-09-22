---
title: Ställ in och hantera en budget för ett projekt | Microsoft Docs
description: Beskriver hur du planerar resurser och prognos och styr kostnader för ett projekt genom att skapa en budget för varje projekt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: a395ba9feee028db02b4fb7786e77afafdeaea0a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783864"
---
# <a name="manage-job-budgets"></a><span data-ttu-id="d3144-103">Hantera projektbudgetar</span><span class="sxs-lookup"><span data-stu-id="d3144-103">Manage Job Budgets</span></span>
<span data-ttu-id="d3144-104">Du kan lägga upp en budget för varje projekt.</span><span class="sxs-lookup"><span data-stu-id="d3144-104">You can set up a budget for each job.</span></span> <span data-ttu-id="d3144-105">Budgeten används för att planera de resurser du tilldelar ett projekt.</span><span class="sxs-lookup"><span data-stu-id="d3144-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="d3144-106">Budgeten kan antingen vara allmän med få poster eller innehålla fler poster som är indelade i aktivitetsnivåer.</span><span class="sxs-lookup"><span data-stu-id="d3144-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="d3144-107">Du kan sedan jämföra budgeterade belopp med den faktiska förbrukningen enligt registreringen i projektjournalen.</span><span class="sxs-lookup"><span data-stu-id="d3144-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="d3144-108">Genom att övervaka skillnader mellan faktisk förbrukning och budgeterad användning kan du kontrollera pågående projekt och förbättra kvaliteten hos framtida projekt genom att minska risken för att kostnader underskattas.</span><span class="sxs-lookup"><span data-stu-id="d3144-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="d3144-109">Efterföljande procedur beskriver hur du beräknar budgeterade kostnader under planering.</span><span class="sxs-lookup"><span data-stu-id="d3144-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="d3144-110">Mer information om registrering av budgeterade jämfört med faktiska projektpriser och -kostnader finns i [Så här registrerar du förbrukning för projekt](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="d3144-110">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <a name="to-estimate-the-budgeted-costs-for-a-job"></a><a name="JobBudgetCosts"></a> <span data-ttu-id="d3144-111">Att ange budgeterade kostnader för ett projekt</span><span class="sxs-lookup"><span data-stu-id="d3144-111">To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="d3144-112">När en kund vill veta priset på ett projekt som kommer att faktureras baserat på förbrukning, måste du fastställa de budgeterade kostnaderna för projektet.</span><span class="sxs-lookup"><span data-stu-id="d3144-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="d3144-113">Du använder sidan **Projektaktivitetsrader** om du vill göra detta.</span><span class="sxs-lookup"><span data-stu-id="d3144-113">You use the **Job Task Lines** page to do this.</span></span>

1. <span data-ttu-id="d3144-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projekt** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="d3144-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d3144-115">Öppna ett relevant projekt.</span><span class="sxs-lookup"><span data-stu-id="d3144-115">Open a relevant job.</span></span>
3. <span data-ttu-id="d3144-116">Markera en projektrad av typen Bokföring och välj sedan åtgärden **Projektplaneringsrader**.</span><span class="sxs-lookup"><span data-stu-id="d3144-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="d3144-117">Fyll i fälten på en ny rad efter behov.</span><span class="sxs-lookup"><span data-stu-id="d3144-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="d3144-118">Se följande information för fältet **Radtyp**.</span><span class="sxs-lookup"><span data-stu-id="d3144-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="d3144-119">Typ av rad</span><span class="sxs-lookup"><span data-stu-id="d3144-119">Line Type</span></span> | <span data-ttu-id="d3144-120">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d3144-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="d3144-121">**Både Budget och Fakturerbart**</span><span class="sxs-lookup"><span data-stu-id="d3144-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="d3144-122">Kostnads- och prisbelopp som har angetts på planeringsraderna är de budgeterade kostnaderna för denna specifika planeringsrad.</span><span class="sxs-lookup"><span data-stu-id="d3144-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="d3144-123">Prisbeloppet faktureras.</span><span class="sxs-lookup"><span data-stu-id="d3144-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="d3144-124">**Budget**</span><span class="sxs-lookup"><span data-stu-id="d3144-124">**Budget**</span></span> |<span data-ttu-id="d3144-125">Kunden debiteras inte för användning.</span><span class="sxs-lookup"><span data-stu-id="d3144-125">The customer is not charged for usage.</span></span> <span data-ttu-id="d3144-126">Förbrukningen överförs inte till en faktura, men den kommer fortfarande att användas i PIA-beräkningen.</span><span class="sxs-lookup"><span data-stu-id="d3144-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="d3144-127">**Fakturerbart**</span><span class="sxs-lookup"><span data-stu-id="d3144-127">**Billable**</span></span> |<span data-ttu-id="d3144-128">Kunden debiteras för användning.</span><span class="sxs-lookup"><span data-stu-id="d3144-128">The customer is charged for usage.</span></span> <span data-ttu-id="d3144-129">Förbrukningen överförs till fakturan baserat på det antal som finns angivet i fältet Antal att överföra till faktura.</span><span class="sxs-lookup"><span data-stu-id="d3144-129">Usage is transferred to the invoice, based on the quantity specified in the Qty. to Transfer to Invoice field.</span></span> |

> [!NOTE]  
> <span data-ttu-id="d3144-130">Fältet **Planerat leveransdatum** för planeringsraden innehåller datumet då förbrukning som relateras till planeringsraden förväntas slutföras.</span><span class="sxs-lookup"><span data-stu-id="d3144-130">The **Planned Delivery Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="d3144-131">Det är också datumet då planeringsraden kan överföras till en försäljningsfaktura och bokföras.</span><span class="sxs-lookup"><span data-stu-id="d3144-131">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span> <br /><br /> <span data-ttu-id="d3144-132">I underliggande projektaktiviteten på sidan **projektkortet** innehåller **startdatum** och **slutdatum** värdet för fältet **planerat leveransdatum** på tidigaste och senaste projektets planeringsrader på relaterad sida för **projektplaneringsrader**.</span><span class="sxs-lookup"><span data-stu-id="d3144-132">On the underlying job task on the **Job Card** page, the **Start Date** and **End Date** fields respectively contain the value of the **Planned Delivery Date** field on the earliest and latest job planning lines in the related **Job Planning Lines** page.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d3144-133">När du fyller i fältet **Antal** kommer all information om totalt pris och total kostnad att beräknas och fyllas i för planeringsraden.</span><span class="sxs-lookup"><span data-stu-id="d3144-133">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="d3144-134">De kan redigeras när det passar dig.</span><span class="sxs-lookup"><span data-stu-id="d3144-134">You can edit them at any time.</span></span>

<span data-ttu-id="d3144-135">På sidan **Projektkort** kan du nu se en översikt över de totala budgeterade kostnaderna, budgeterat pris, fakturerbar kostnad och fakturerbart pris för varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="d3144-135">On the **Job Card** page, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="d3144-136">Mer information om registrering av budgeterade jämfört med faktiska projektpriser och -kostnader finns i [Så här registrerar du förbrukning för projekt](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="d3144-136">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d3144-137">Se även</span><span class="sxs-lookup"><span data-stu-id="d3144-137">See Also</span></span>
[<span data-ttu-id="d3144-138">Projekthantering</span><span class="sxs-lookup"><span data-stu-id="d3144-138">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="d3144-139">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="d3144-139">Finance</span></span>](finance.md)  
<span data-ttu-id="d3144-140">[Inköp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="d3144-140">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="d3144-141">[Försäljning](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="d3144-141">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="d3144-142">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d3144-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
