---
title: Koppla och synkronisera poster manuellt | Microsoft Docs
description: Synkronisera en mappning för integreringstabellen tillåter datasynkronisering data i alla poster i en tabell i Business Central och den Dynamics 365 Sales-enhet som används.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: fdc407ef26d238ba54a2566cdd9003c29da2eeb3
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196669"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="f0e18-103">Koppla och synkronisera poster manuellt</span><span class="sxs-lookup"><span data-stu-id="f0e18-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="f0e18-104">I det här avsnittet beskrivs hur du kopplar en eller flera transaktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] med transaktioner i Common Data Service eller [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f0e18-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="f0e18-105">Koppling av poster låter dig visa Common Data Service information från [!INCLUDE[d365fin](includes/d365fin_md.md)] och vice versa.</span><span class="sxs-lookup"><span data-stu-id="f0e18-105">Coupling records lets you view Common Data Service information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="f0e18-106">Kopplingen låter dig också synkronisera data mellan posterna.</span><span class="sxs-lookup"><span data-stu-id="f0e18-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="f0e18-107">Du kan koppla befintliga poster eller skapa och koppla nya poster.</span><span class="sxs-lookup"><span data-stu-id="f0e18-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="f0e18-108">Du kan bara koppla och synkronisera data om din systemadministratör har skapat en anslutning mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och Common Data Service eller [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f0e18-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="f0e18-109">Ett snabbt sätt att kontrollera är att öppna kortet **kund** och leta efter åtgärden **konfigurera koppling**.</span><span class="sxs-lookup"><span data-stu-id="f0e18-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="f0e18-110">Om åtgärden är tillgänglig är apparna sammankopplade.</span><span class="sxs-lookup"><span data-stu-id="f0e18-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="f0e18-111">Videoexempel</span><span class="sxs-lookup"><span data-stu-id="f0e18-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="f0e18-112">Om du vill koppla en post</span><span class="sxs-lookup"><span data-stu-id="f0e18-112">To couple a record</span></span>  
1.  <span data-ttu-id="f0e18-113">I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppnar du kortet för den post du vill koppla.</span><span class="sxs-lookup"><span data-stu-id="f0e18-113">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="f0e18-114">Till exempel kund- eller kontaktkort.</span><span class="sxs-lookup"><span data-stu-id="f0e18-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="f0e18-115">Du kan också bara öppna listsidan och välja den post som du vill koppla.</span><span class="sxs-lookup"><span data-stu-id="f0e18-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="f0e18-116">Välj åtgärden **konfigurera koppling**.</span><span class="sxs-lookup"><span data-stu-id="f0e18-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="f0e18-117">Fyll i fälten och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0e18-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="f0e18-118">Om du vill synkronisera en enda post</span><span class="sxs-lookup"><span data-stu-id="f0e18-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="f0e18-119">I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppnar du kortet för den post du vill koppla.</span><span class="sxs-lookup"><span data-stu-id="f0e18-119">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="f0e18-120">Till exempel kund- eller kontaktkort.</span><span class="sxs-lookup"><span data-stu-id="f0e18-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="f0e18-121">Välj åtgärden **synkronisera nu**.</span><span class="sxs-lookup"><span data-stu-id="f0e18-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="f0e18-122">Om en transaktion kan synkroniseras åt endast ett håll, välj då det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0e18-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="f0e18-123">Om du vill synkronisera en enda transaktion från [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0e18-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="f0e18-124">I [!INCLUDE[crm_md](includes/crm_md.md)] öppnar du formuläret för den transaktion du vill koppla.</span><span class="sxs-lookup"><span data-stu-id="f0e18-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="f0e18-125">Till exempel formuläret Kontokort eller Kontaktkort.</span><span class="sxs-lookup"><span data-stu-id="f0e18-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="f0e18-126">Välj åtgärden **[!INCLUDE[d365fin](includes/d365fin_md.md)]** i menyfliksområdet för att öppna och koppla transaktioner automatiskt.</span><span class="sxs-lookup"><span data-stu-id="f0e18-126">Choose the **[!INCLUDE[d365fin](includes/d365fin_md.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="f0e18-127">Du kan endast synkronisera en enskild transaktion automatiskt från [!INCLUDE[crm_md](includes/crm_md.md)] när **Synka endast kopplade transaktioner** är inaktiverat och synkroniseringen har angetts som dubbelriktad eller Från integreringstabell på sidan **Tabellmappning för integrering** för transaktionen.</span><span class="sxs-lookup"><span data-stu-id="f0e18-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="f0e18-128">Mer information finns i [Mappa de tabeller och fält som ska synkroniseras](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="f0e18-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="f0e18-129">Om du vill synkronisera flera poster</span><span class="sxs-lookup"><span data-stu-id="f0e18-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="f0e18-130">I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppna listsidan för posten, till exempel listsidan kunder eller kontakter.</span><span class="sxs-lookup"><span data-stu-id="f0e18-130">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="f0e18-131">Markera den post du vill synkronisera och välj sedan åtgärden **Synkronisera nu**.</span><span class="sxs-lookup"><span data-stu-id="f0e18-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="f0e18-132">Om transaktioner kan synkroniseras åt endast ett håll, välj då det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0e18-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f0e18-133">Se även</span><span class="sxs-lookup"><span data-stu-id="f0e18-133">See Also</span></span>  
[<span data-ttu-id="f0e18-134">Använda Dynamics 365 Sales från Business Central</span><span class="sxs-lookup"><span data-stu-id="f0e18-134">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
