---
title: "Bästa metoder för global planeringsinstallation | Microsoft Docs"
description: "Snabbfliken **Planering** i fönstret **Produktionsinställningar** innehåller flera fält som definierar globala regler för leveransplanering."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f1a4e3a30d4d665a83ab599ad19dfd3760d744b2
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="setup-best-practices-global-planning-setup"></a><span data-ttu-id="a9011-103">Skapa metodtips: konfiguration av global planering</span><span class="sxs-lookup"><span data-stu-id="a9011-103">Setup Best Practices: Global Planning Setup</span></span>
<span data-ttu-id="a9011-104">Snabbfliken **Planering** i fönstret **Produktionsinställningar** innehåller flera fält som definierar globala regler för leveransplanering.</span><span class="sxs-lookup"><span data-stu-id="a9011-104">The **Planning** FastTab in the **Manufacturing Setup** window contains several fields that define global rules for supply planning.</span></span>  

 <span data-ttu-id="a9011-105">I tabellen nedan finns best practice för hur du lägger upp valda globala planeringsparameterfält.</span><span class="sxs-lookup"><span data-stu-id="a9011-105">The following table provides best practices on how to set up selected global planning parameter fields.</span></span> <span data-ttu-id="a9011-106">Välj länken i kolumnen **Inställningsfält** om du vill ha mer information om ett fält.</span><span class="sxs-lookup"><span data-stu-id="a9011-106">For more information about a field, choose the link in the **Setup field** column.</span></span>  

|<span data-ttu-id="a9011-107">Inställningsfält</span><span class="sxs-lookup"><span data-stu-id="a9011-107">Setup field</span></span>|<span data-ttu-id="a9011-108">Best practice</span><span class="sxs-lookup"><span data-stu-id="a9011-108">Best practice</span></span>|<span data-ttu-id="a9011-109">Kommentar</span><span class="sxs-lookup"><span data-stu-id="a9011-109">Comment</span></span>|  
|-----------------|-------------------|-------------|  
|<span data-ttu-id="a9011-110">Prognos på lagerställen</span><span class="sxs-lookup"><span data-stu-id="a9011-110">Use Forecast on Locations</span></span>|<span data-ttu-id="a9011-111">Markera om du har prognoser för särskilda platser.</span><span class="sxs-lookup"><span data-stu-id="a9011-111">Select if you have forecasts for specific locations.</span></span>||  
|<span data-ttu-id="a9011-112">Komponenter vid lagerställe</span><span class="sxs-lookup"><span data-stu-id="a9011-112">Components at Location</span></span>|<span data-ttu-id="a9011-113">Om artiklar inte definieras som lagerställeenheter, välj lagerställekoden för huvudlager.</span><span class="sxs-lookup"><span data-stu-id="a9011-113">If items are not defined as SKUs, select the location code of your main warehouse.</span></span>|<span data-ttu-id="a9011-114">Detta gäller också om du bara använder inköpsförslaget.</span><span class="sxs-lookup"><span data-stu-id="a9011-114">This also applies if you only use the requisition worksheet.</span></span>|  
|<span data-ttu-id="a9011-115">Tom överflödesnivå</span><span class="sxs-lookup"><span data-stu-id="a9011-115">Blank Overflow Level</span></span>|<span data-ttu-id="a9011-116">Välj **Tillåt standardberäkningen** om du flyttar från Microsoft Dynamics NAV 5.0 eller tidigare.</span><span class="sxs-lookup"><span data-stu-id="a9011-116">Select **Allow Default Calculation** if you are migrating from Microsoft Dynamics NAV 5.0 or earlier.</span></span>|<span data-ttu-id="a9011-117">Använd endast om du vill tillåta några eller alla artiklarna att gå över beställningspunkten.</span><span class="sxs-lookup"><span data-stu-id="a9011-117">Use only if you want to allow all or some of your items to overflow the reorder point.</span></span>|  
|<span data-ttu-id="a9011-118">Standard för utjämningsperiod</span><span class="sxs-lookup"><span data-stu-id="a9011-118">Default Dampener Period</span></span>|<span data-ttu-id="a9011-119">Ställ in mellan 1D och 5D.</span><span class="sxs-lookup"><span data-stu-id="a9011-119">Set between 1D and 5D.</span></span><br /><br /> <span data-ttu-id="a9011-120">Ange en längre peridod i [!INCLUDE[d365fin](includes/d365fin_md.md)] om du är ny i planering.</span><span class="sxs-lookup"><span data-stu-id="a9011-120">If new to planning in [!INCLUDE[d365fin](includes/d365fin_md.md)], then set a longer period.</span></span>|<span data-ttu-id="a9011-121">När användare är mer förtrogna med de olika orsakerna till åtgärdsmeddelanden, förkorta dämpningsperioden om du vill tillåta fler ändringsförslag.</span><span class="sxs-lookup"><span data-stu-id="a9011-121">When users are more familiar with the different reasons for action messages, then shorten the dampener period to allow more change suggestions.</span></span>|  
|<span data-ttu-id="a9011-122">Max. avvikelsekvantitet</span><span class="sxs-lookup"><span data-stu-id="a9011-122">Default Dampener Quantity</span></span>|<span data-ttu-id="a9011-123">Ange mellan 5 och 20 procent av artikelns partistorlek.</span><span class="sxs-lookup"><span data-stu-id="a9011-123">Set between 5 and 20 percent of the item’s lot size.</span></span>||  

## <a name="see-also"></a><span data-ttu-id="a9011-124">Se även</span><span class="sxs-lookup"><span data-stu-id="a9011-124">See Also</span></span>  
 <span data-ttu-id="a9011-125">[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="a9011-125">[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md) </span></span>  
 <span data-ttu-id="a9011-126">[Designdetaljer: Leveransplanering](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="a9011-126">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="a9011-127">Skapa komplexa moduler med hjälp av bästa metoder</span><span class="sxs-lookup"><span data-stu-id="a9011-127">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="a9011-128">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a9011-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
