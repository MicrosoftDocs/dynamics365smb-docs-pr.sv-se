---
title: "Så här konfigurerar du nya företag som använder en Cmdlet | Microsoft Docs"
description: "I ett antal scenarier kanske du vill läsa in och importera ett konfigurationspaket utan att blanda in dina användare eller använda RapidStart Services-användargränssnittet. Du kan göra detta genom att använda en Windows PowerShell-cmdlet."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 9d248f2f8676c392451ae4a6f99932145f354f5b
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a><span data-ttu-id="aaa35-104">Så här konfigurerar du nya företag med Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aaa35-104">Configure New Companies using a Cmdlet</span></span>
<span data-ttu-id="aaa35-105">I ett antal scenarier kanske du vill läsa in och importera ett konfigurationspaket utan att blanda in dina användare eller använda RapidStart Services-användargränssnittet.</span><span class="sxs-lookup"><span data-stu-id="aaa35-105">In a number of scenarios, you may want to load and import a configuration package without involving your users or using the RapidStart Services user interface.</span></span> <span data-ttu-id="aaa35-106">Du kan göra detta genom att använda en Windows PowerShell-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaa35-106">You can do so by using a Windows PowerShell cmdlet.</span></span> <span data-ttu-id="aaa35-107">Scenarier där det kan vara användbart, inkluderar:</span><span class="sxs-lookup"><span data-stu-id="aaa35-107">Scenarios where this may be useful include:</span></span>  

- <span data-ttu-id="aaa35-108">Utföra dataimport på olika [!INCLUDE[d365fin](includes/d365fin_md.md)]-installationer.</span><span class="sxs-lookup"><span data-stu-id="aaa35-108">Performing data import across multiple [!INCLUDE[d365fin](includes/d365fin_md.md)] installations.</span></span>
- <span data-ttu-id="aaa35-109">Konfigurera ytterligare moduler för flera kunder.</span><span class="sxs-lookup"><span data-stu-id="aaa35-109">Configuring additional application areas for multiple customers.</span></span>  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a><span data-ttu-id="aaa35-110">Så här distribuerar du ett konfigurationspaket med hjälp av en cmdlet</span><span class="sxs-lookup"><span data-stu-id="aaa35-110">To deploy a configuration package using a cmdlet</span></span>  

1. <span data-ttu-id="aaa35-111">Förbereda ett RapidStart Services-paket.</span><span class="sxs-lookup"><span data-stu-id="aaa35-111">Prepare a RapidStart Services package.</span></span> <span data-ttu-id="aaa35-112">Du kan till exempel skapa ett paket för att importera vissa värden och namnen på tabellen och fälten att infoga dessa värden i.</span><span class="sxs-lookup"><span data-stu-id="aaa35-112">For example, you can create a package to import certain values and the names of the table and the fields to insert these values into.</span></span>  
2. <span data-ttu-id="aaa35-113">Markera paketet på en dator där du vill köra cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aaa35-113">Place the package on a computer where you will run the cmdlet.</span></span>  
3. <span data-ttu-id="aaa35-114">Öppna [!INCLUDE[d365fin](includes/d365fin_md.md)]-administrationsgränssnittet.</span><span class="sxs-lookup"><span data-stu-id="aaa35-114">Open the [!INCLUDE[d365fin](includes/d365fin_md.md)] administration shell.</span></span>  
4. <span data-ttu-id="aaa35-115">Ange **Anropa-NAVCodeUnit** och ange information som är liknande till följande exempel.</span><span class="sxs-lookup"><span data-stu-id="aaa35-115">Enter **Invoke-NAVCodeUnit**, and specify information similar to the following example.</span></span>  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
<span data-ttu-id="aaa35-116">Cmdleten importerar godset till varje företag.</span><span class="sxs-lookup"><span data-stu-id="aaa35-116">The cmdlet imports the package into each company.</span></span> <span data-ttu-id="aaa35-117">Användare kan börja använda den nya funktionen omedelbart.</span><span class="sxs-lookup"><span data-stu-id="aaa35-117">Users can start to use the new functionality immediately.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aaa35-118">Se även</span><span class="sxs-lookup"><span data-stu-id="aaa35-118">See Also</span></span>  
[<span data-ttu-id="aaa35-119">Konfigurera nya företag</span><span class="sxs-lookup"><span data-stu-id="aaa35-119">Configure New Companies</span></span>](admin-how-to-configure-new-companies.md)  
[<span data-ttu-id="aaa35-120">Koppla konfigurationen till nya företag</span><span class="sxs-lookup"><span data-stu-id="aaa35-120">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="aaa35-121">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="aaa35-121">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="aaa35-122">Administration</span><span class="sxs-lookup"><span data-stu-id="aaa35-122">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="aaa35-123">Microsoft Dynamics NAV Windows PowerShell-Cmdlet:ar</span><span class="sxs-lookup"><span data-stu-id="aaa35-123">Microsoft Dynamics NAV Windows PowerShell Cmdlets</span></span>](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

