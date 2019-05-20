---
title: Koppla och synkronisera poster manuellt | Microsoft Docs
description: Synkronisera en mappning för integrationstabellen tillåter datasynkronisering data i alla poster i en tabell i Business Central och den Dynamics 365 for Sales enhet som används.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 36f1a0fe8c50744d9ce13d1e6c3c899f4ceaf5e4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245411"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="31a5d-103">Koppla och synkronisera poster manuellt</span><span class="sxs-lookup"><span data-stu-id="31a5d-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="31a5d-104">I det här avsnittet beskrivs hur du kopplar en eller flera poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] med poster i [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="31a5d-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="31a5d-105">Koppling av poster låter dig visa [!INCLUDE[crm_md](includes/crm_md.md)] information från [!INCLUDE[d365fin](includes/d365fin_md.md)] och vice versa.</span><span class="sxs-lookup"><span data-stu-id="31a5d-105">Coupling records lets you view [!INCLUDE[crm_md](includes/crm_md.md)] information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="31a5d-106">Kopplingen låter dig också synkronisera data mellan posterna.</span><span class="sxs-lookup"><span data-stu-id="31a5d-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="31a5d-107">Du kan koppla befintliga poster eller skapa och koppla nya poster.</span><span class="sxs-lookup"><span data-stu-id="31a5d-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="31a5d-108">Koppla och synkronisera data med [!INCLUDE[crm_md](includes/crm_md.md)] är endast tillgängligt om administratören har skapat en anslutning mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="31a5d-108">Coupling and synchronizing data with [!INCLUDE[crm_md](includes/crm_md.md)] is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="31a5d-109">Ett snabbt sätt att kontrollera är att öppna kortet **kund** och leta efter åtgärden **konfigurera koppling**.</span><span class="sxs-lookup"><span data-stu-id="31a5d-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="31a5d-110">Om åtgärden är tillgänglig är apparna sammankopplade.</span><span class="sxs-lookup"><span data-stu-id="31a5d-110">If the action is available, the apps are connected.</span></span>   

## <a name="to-couple-a-record"></a><span data-ttu-id="31a5d-111">Om du vill koppla en post</span><span class="sxs-lookup"><span data-stu-id="31a5d-111">To couple a record</span></span>  
1.  <span data-ttu-id="31a5d-112">I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppnar du kortet för den post du vill koppla.</span><span class="sxs-lookup"><span data-stu-id="31a5d-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="31a5d-113">Till exempel kund- eller kontaktkort.</span><span class="sxs-lookup"><span data-stu-id="31a5d-113">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="31a5d-114">Du kan också bara öppna listsidan och välja den post som du vill koppla.</span><span class="sxs-lookup"><span data-stu-id="31a5d-114">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="31a5d-115">Välj åtgärden **konfigurera koppling**.</span><span class="sxs-lookup"><span data-stu-id="31a5d-115">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="31a5d-116">Fyll i fälten och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="31a5d-116">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="31a5d-117">Om du vill synkronisera en enda post</span><span class="sxs-lookup"><span data-stu-id="31a5d-117">To synchronize a single record</span></span>  
1.  <span data-ttu-id="31a5d-118">I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppnar du kortet för den post du vill koppla.</span><span class="sxs-lookup"><span data-stu-id="31a5d-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="31a5d-119">Till exempel kund- eller kontaktkort.</span><span class="sxs-lookup"><span data-stu-id="31a5d-119">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="31a5d-120">Välj åtgärden **synkronisera nu**.</span><span class="sxs-lookup"><span data-stu-id="31a5d-120">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="31a5d-121">Om en post kan synkroniseras antingen från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)] eller från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)] välj det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="31a5d-121">If a record can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="31a5d-122">Om du vill synkronisera flera poster</span><span class="sxs-lookup"><span data-stu-id="31a5d-122">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="31a5d-123">I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppna listsidan för posten, till exempel listsidan kunder eller kontakter.</span><span class="sxs-lookup"><span data-stu-id="31a5d-123">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="31a5d-124">Markera den post du vill synkronisera och välj sedan åtgärden **Synkronisera nu**.</span><span class="sxs-lookup"><span data-stu-id="31a5d-124">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="31a5d-125">Om poster kan synkroniseras antingen från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)] eller från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)] välj det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="31a5d-125">If records can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="31a5d-126">Se även</span><span class="sxs-lookup"><span data-stu-id="31a5d-126">See Also</span></span>  
[<span data-ttu-id="31a5d-127">Med hjälp av Dynamics 365 for Sales från Business Central</span><span class="sxs-lookup"><span data-stu-id="31a5d-127">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
