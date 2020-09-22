---
title: Uppgradera en integrering med Dynamics 365 Sales | Microsoft-dokument
description: Lär dig hur du hämtar Dynamics 365 Business Central redo att integreras med Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 57bb8d6ee48b608074a669109bdd99abf8c452c2
ms.sourcegitcommit: 351eb465e6dfb3d01c0f3ea406db340f393f47fc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3742841"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="7cce1-103">Uppgradera en integrering med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="7cce1-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="7cce1-104">integreras också med [!INCLUDE[d365fin](includes/cds_long_md.md)], vilket gör det enkelt att ansluta och synkronisera data med andra Dynamics 365-program, till exempel [!INCLUDE[crm_md](includes/crm_md.md)] eller till och med appar som du själv skapar.</span><span class="sxs-lookup"><span data-stu-id="7cce1-104">integrates with [!INCLUDE[d365fin](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="7cce1-105">Om du integrerar för första gången rekommenderar vi att du gör det via [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7cce1-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <span data-ttu-id="7cce1-106">Mer information finns i [Integrera med Common Data Service](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="7cce1-106">For more information, see [Integration with Common Data Service](admin-common-data-service.md).</span></span>

<span data-ttu-id="7cce1-107">Om du redan har integrerat [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du fortsätta att synkronisera data med hjälp av dina inställningar.</span><span class="sxs-lookup"><span data-stu-id="7cce1-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="7cce1-108">Om du uppgraderar [!INCLUDE[d365fin](includes/d365fin_md.md)] eller stänger av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen måste du emellertid ansluta dig via [!INCLUDE[d365fin](includes/cds_long_md.md)] för att aktivera den igen.</span><span class="sxs-lookup"><span data-stu-id="7cce1-108">However, if you upgrade [!INCLUDE[d365fin](includes/d365fin_md.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="7cce1-109">När du återansluter via [!INCLUDE[d365fin](includes/cds_long_md.md)] används standardinställningarna för synkroniseringen, och eventuella konfigurationsinställningar skrivs över.</span><span class="sxs-lookup"><span data-stu-id="7cce1-109">Reconnecting through [!INCLUDE[d365fin](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="7cce1-110">Till exempel tillämpas standardmappningarna för tabeller.</span><span class="sxs-lookup"><span data-stu-id="7cce1-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a><span data-ttu-id="7cce1-111">Så här uppgraderar du anslutningen till att använda Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7cce1-111">To upgrade your connection to use Common Data Service</span></span>
1. <span data-ttu-id="7cce1-112">Öppna sidan **Konfigurera anslutning för Microsoft Dynamics 365**, välj brytaren **Aktivera** för att stänga av den befintliga anslutningen till [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7cce1-112">Open the **Microsoft Dynamics 365 Connection Setup** page, choose the **Enable** toggle to turn off your existing connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="7cce1-113">Öppna sidan **Konfiguration av anslutning till Common Data Service** och välj brytaren **Aktivera** för att slå på anslutningen.</span><span class="sxs-lookup"><span data-stu-id="7cce1-113">Open the **Common Data Service Connection Setup** page, and choose the **Enable** toggle to turn on the connection.</span></span>
  
   <span data-ttu-id="7cce1-114">När du har aktiverat CDS-anslutningen distribueras anslutningen till basintegrering med CDS för Business Central till Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7cce1-114">After you enable the CDS connection, the Business Central CDS Base Integration Solution is deployed to Common Data Service.</span></span>
3. <span data-ttu-id="7cce1-115">Avinstallera Microsoft Dynamics 365 Business Central-integreringslösningen från Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="7cce1-115">Uninstall the Microsoft Dynamics 365 Business Central Integration solution from your Dynamics 365 Sales.</span></span> <span data-ttu-id="7cce1-116">Mer information finns i avsnittet [Avinstallera eller ta bort ett lösningsämne](/powerapps/developer/common-data-service/uninstall-delete-solution).</span><span class="sxs-lookup"><span data-stu-id="7cce1-116">For more information, see [Uninstall or delete a solution topic](/powerapps/developer/common-data-service/uninstall-delete-solution).</span></span> 

4. <span data-ttu-id="7cce1-117">På sidan **Anslutningskonfiguration för Microsoft Dynamics 365** aktiverar du reglaget **Aktivera** för att ansluta till [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7cce1-117">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enable** toggle to connect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   <span data-ttu-id="7cce1-118">När du har aktiverat Sales-anslutningen distribueras anslutningen till basintegrering med CDS för Business Central till Sales.</span><span class="sxs-lookup"><span data-stu-id="7cce1-118">After you enable the Sales connection, the Business Central Integration Solution is deployed to Sales.</span></span> <span data-ttu-id="7cce1-119">Detta möjliggör integrering med enheter som är specifika för [!INCLUDE[crm_md](includes/crm_md.md)], t.ex. försäljningsorder, offerter och fakturor.</span><span class="sxs-lookup"><span data-stu-id="7cce1-119">This enables integration with entities that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="7cce1-120">På sidan **Anslutningsinställningar för Sales** väljer du **Använd standardinställningar för synkronisering** om du vill initiera tabellmappningarna för [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7cce1-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="7cce1-121">Se även</span><span class="sxs-lookup"><span data-stu-id="7cce1-121">See Also</span></span>
[<span data-ttu-id="7cce1-122">Integrering med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="7cce1-122">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="7cce1-123">Integrera med Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7cce1-123">Integrating with Common Data Service</span></span>](admin-common-data-service.md)