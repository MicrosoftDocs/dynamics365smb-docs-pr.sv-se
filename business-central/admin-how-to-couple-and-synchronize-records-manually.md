---
title: Koppling och synkronisering | Microsoft-dokument
description: Genom att synkronisera en mappning av integreringstabellen möjliggörs datasynkronisering i alla poster i en tabell i Business Central eller Dynamics 365 Sales som är kopplade.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: fa4d6cfe13662613a73c14d68542f8319798ea80
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752681"
---
# <a name="coupling-and-synchronizing"></a><span data-ttu-id="d19c6-103">Koppling och synkronisering</span><span class="sxs-lookup"><span data-stu-id="d19c6-103">Coupling and Synchronizing</span></span>
<span data-ttu-id="d19c6-104">I det här avsnittet beskrivs hur du kopplar en eller flera transaktioner i [!INCLUDE[prod_short](includes/prod_short.md)] med transaktioner i Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d19c6-104">This topic describes how to couple one or more records in [!INCLUDE[prod_short](includes/prod_short.md)] with records in Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="d19c6-105">Koppling av poster låter dig visa Dataverse information från [!INCLUDE[prod_short](includes/prod_short.md)] och vice versa.</span><span class="sxs-lookup"><span data-stu-id="d19c6-105">Coupling records lets you view Dataverse information from [!INCLUDE[prod_short](includes/prod_short.md)], and vice versa.</span></span> <span data-ttu-id="d19c6-106">Kopplingen låter dig också synkronisera data mellan posterna.</span><span class="sxs-lookup"><span data-stu-id="d19c6-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="d19c6-107">Du kan koppla befintliga poster eller skapa och koppla nya poster.</span><span class="sxs-lookup"><span data-stu-id="d19c6-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="d19c6-108">Du kan bara koppla och synkronisera data om din systemadministratör har skapat en anslutning mellan [!INCLUDE[prod_short](includes/prod_short.md)] och Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d19c6-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[prod_short](includes/prod_short.md)] and Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="d19c6-109">Ett snabbt sätt att kontrollera är att öppna kortet **kund** och leta efter åtgärden **konfigurera koppling**.</span><span class="sxs-lookup"><span data-stu-id="d19c6-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="d19c6-110">Om åtgärden är tillgänglig är apparna sammankopplade.</span><span class="sxs-lookup"><span data-stu-id="d19c6-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="d19c6-111">Videoexempel</span><span class="sxs-lookup"><span data-stu-id="d19c6-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="d19c6-112">Om du vill koppla en post</span><span class="sxs-lookup"><span data-stu-id="d19c6-112">To couple a record</span></span>  
1.  <span data-ttu-id="d19c6-113">I [!INCLUDE[prod_short](includes/prod_short.md)] öppnar du kortet för den post du vill koppla.</span><span class="sxs-lookup"><span data-stu-id="d19c6-113">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="d19c6-114">Till exempel kund- eller kontaktkort.</span><span class="sxs-lookup"><span data-stu-id="d19c6-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="d19c6-115">Du kan också bara öppna listsidan och välja den post som du vill koppla.</span><span class="sxs-lookup"><span data-stu-id="d19c6-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="d19c6-116">Välj åtgärden **konfigurera koppling**.</span><span class="sxs-lookup"><span data-stu-id="d19c6-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="d19c6-117">Fyll i fälten och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="d19c6-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="d19c6-118">Om du vill synkronisera en enda post</span><span class="sxs-lookup"><span data-stu-id="d19c6-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="d19c6-119">I [!INCLUDE[prod_short](includes/prod_short.md)] öppnar du kortet för den post du vill koppla.</span><span class="sxs-lookup"><span data-stu-id="d19c6-119">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="d19c6-120">Till exempel kund- eller kontaktkort.</span><span class="sxs-lookup"><span data-stu-id="d19c6-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="d19c6-121">Välj åtgärden **synkronisera nu**.</span><span class="sxs-lookup"><span data-stu-id="d19c6-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="d19c6-122">Om en transaktion kan synkroniseras åt endast ett håll, välj då det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="d19c6-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="d19c6-123">Om du vill synkronisera en enda transaktion från [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="d19c6-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="d19c6-124">I [!INCLUDE[crm_md](includes/crm_md.md)] öppnar du formuläret för den transaktion du vill koppla.</span><span class="sxs-lookup"><span data-stu-id="d19c6-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="d19c6-125">Till exempel formuläret Kontokort eller Kontaktkort.</span><span class="sxs-lookup"><span data-stu-id="d19c6-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="d19c6-126">Välj åtgärden **[!INCLUDE[prod_short](includes/prod_short.md)]** i menyfliksområdet för att öppna och koppla transaktioner automatiskt.</span><span class="sxs-lookup"><span data-stu-id="d19c6-126">Choose the **[!INCLUDE[prod_short](includes/prod_short.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="d19c6-127">Du kan endast synkronisera en enskild transaktion automatiskt från [!INCLUDE[crm_md](includes/crm_md.md)] när **Synka endast kopplade transaktioner** är inaktiverat och synkroniseringen har angetts som dubbelriktad eller Från integreringstabell på sidan **Registermappning för integrering** för transaktionen.</span><span class="sxs-lookup"><span data-stu-id="d19c6-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="d19c6-128">Mer information finns i [Mappa de tabeller och fält som ska synkroniseras](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="d19c6-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="d19c6-129">Om du vill synkronisera flera poster</span><span class="sxs-lookup"><span data-stu-id="d19c6-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="d19c6-130">I [!INCLUDE[prod_short](includes/prod_short.md)] öppna listsidan för posten, till exempel listsidan kunder eller kontakter.</span><span class="sxs-lookup"><span data-stu-id="d19c6-130">In [!INCLUDE[prod_short](includes/prod_short.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="d19c6-131">Markera den post du vill synkronisera och välj sedan åtgärden **Synkronisera nu**.</span><span class="sxs-lookup"><span data-stu-id="d19c6-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="d19c6-132">Om transaktioner kan synkroniseras åt endast ett håll, välj då det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="d19c6-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="uncoupling-records"></a><span data-ttu-id="d19c6-133">Frånkopplingsposter</span><span class="sxs-lookup"><span data-stu-id="d19c6-133">Uncoupling Records</span></span>
<span data-ttu-id="d19c6-134">Du kan koppla bort en eller flera poster från listsidor eller sidan **Kopplade datasynkroniseringsfel** genom att välja en eller flera rader och välja **Radera koppling**.</span><span class="sxs-lookup"><span data-stu-id="d19c6-134">You can uncouple one or more records from list pages or the **Coupled Data Synchronization Errors** page by choosing one or more lines and choosing **Delete Coupling**.</span></span> <span data-ttu-id="d19c6-135">Du kan också ta bort alla kopplingar för en eller flera registermappningar på sidan **Mappningar för integrationstabeller**.</span><span class="sxs-lookup"><span data-stu-id="d19c6-135">You can also remove all couplings for one or more table mappings on the **Integration Table Mappings** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="d19c6-136">Se även</span><span class="sxs-lookup"><span data-stu-id="d19c6-136">See Also</span></span>  
[<span data-ttu-id="d19c6-137">Använda Dynamics 365 Sales från Business Central</span><span class="sxs-lookup"><span data-stu-id="d19c6-137">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
