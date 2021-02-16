---
title: Uppgradera en integrering med Dynamics 365 Sales
description: Lär dig hur du flyttar Dynamics 365 Business Central-integrationen med Dynamics 365 Sales till den senaste versionen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 6528a05d0d2b43d39f0f2fafa26d71b03d0d2511
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013723"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="38f52-103">Uppgradera en integrering med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="38f52-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="38f52-104">integreras också med [!INCLUDE[prod_short](includes/cds_long_md.md)], vilket gör det enkelt att ansluta och synkronisera data med andra Dynamics 365-program, till exempel [!INCLUDE[crm_md](includes/crm_md.md)] eller till och med appar som du själv skapar.</span><span class="sxs-lookup"><span data-stu-id="38f52-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="38f52-105">Om du integrerar för första gången rekommenderar vi att du gör det via [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="38f52-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="38f52-106">Mer information finns i [Integrera med Dataverse](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="38f52-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="38f52-107">Om du redan har integrerat [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)] kan du fortsätta att synkronisera data med hjälp av dina inställningar.</span><span class="sxs-lookup"><span data-stu-id="38f52-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="38f52-108">Om du uppgraderar [!INCLUDE[prod_short](includes/prod_short.md)] eller stänger av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen måste du emellertid ansluta dig via [!INCLUDE[prod_short](includes/cds_long_md.md)] för att aktivera den igen.</span><span class="sxs-lookup"><span data-stu-id="38f52-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="38f52-109">När du återansluter via [!INCLUDE[prod_short](includes/cds_long_md.md)] används standardinställningarna för synkroniseringen, och eventuella konfigurationsinställningar skrivs över.</span><span class="sxs-lookup"><span data-stu-id="38f52-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="38f52-110">Till exempel tillämpas standardmappningarna för tabeller.</span><span class="sxs-lookup"><span data-stu-id="38f52-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="38f52-111">Så här uppgraderar du anslutningen till att använda Dataverse</span><span class="sxs-lookup"><span data-stu-id="38f52-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="38f52-112">Öppna sidan **Anslutningskonfiguration för Microsoft Dynamics 365** och stäng av brytaren **Aktiverad** för att koppla ifrån [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="38f52-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="38f52-113">Öppna sidan **Anslutningskonfiguration för Dataverse** och välj brytaren **Aktiverad** för att aktivera anslutningen till [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="38f52-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   <span data-ttu-id="38f52-114">När du har aktiverat anslutningen distribueras integreringslösningen till Business Central till Dataverse.</span><span class="sxs-lookup"><span data-stu-id="38f52-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="38f52-115">Välj **Omdistribuera integreringslösning** för att ominstallera integreringslösningen för Business Central.</span><span class="sxs-lookup"><span data-stu-id="38f52-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="38f52-116">På sidan **Anslutningskonfiguration för Microsoft Dynamics 365** aktiverar du reglaget **Aktiverad** för att återansluta till [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="38f52-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   <span data-ttu-id="38f52-117">Detta möjliggör integrering med tabeller som är specifika för [!INCLUDE[crm_md](includes/crm_md.md)], t.ex. försäljningsorder, offerter och fakturor.</span><span class="sxs-lookup"><span data-stu-id="38f52-117">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="38f52-118">På sidan **Anslutningsinställningar för Sales** väljer du **Använd standardinställningar för synkronisering** om du vill initiera registermappningarna för [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="38f52-118">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="38f52-119">Se även</span><span class="sxs-lookup"><span data-stu-id="38f52-119">See Also</span></span>
[<span data-ttu-id="38f52-120">Integrering med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="38f52-120">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="38f52-121">Integrera med Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="38f52-121">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)
