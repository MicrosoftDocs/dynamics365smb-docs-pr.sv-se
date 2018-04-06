---
title: "Ställa in företagskonfiguration | Microsoft Docs"
description: "Implementeringsprocessen börjar med det Business Central-lösningen kräver. Samla sedan ihop all denna information i konfigurationspaket."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: eeca45a36e38ab80a63156995a2f11466262d512
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-company-configuration"></a><span data-ttu-id="b88ce-104">Ställa in företagskonfiguration</span><span class="sxs-lookup"><span data-stu-id="b88ce-104">Set Up Company Configuration</span></span>
<span data-ttu-id="b88ce-105">Implementeringsprocessen börjar med Microsoft-partnern.</span><span class="sxs-lookup"><span data-stu-id="b88ce-105">The implementation process begins with the Microsoft partner.</span></span> <span data-ttu-id="b88ce-106">Partnern är ansvarig för att tänka igenom konfigurationdetaljerna och för att skapa ett paket som en kund enkelt kan använda.</span><span class="sxs-lookup"><span data-stu-id="b88ce-106">The partner is responsible for thinking through the configuration details and creating a package that a customer can easily apply.</span></span> <span data-ttu-id="b88ce-107">Innan du skapar ett nytt företag bör du planera hur det ska konfigureras.</span><span class="sxs-lookup"><span data-stu-id="b88ce-107">Before you create a new company, you should plan how it will be configured.</span></span> <span data-ttu-id="b88ce-108">Du måste beakta grundläggande inställningsdata och vilka slags data din [!INCLUDE[d365fin](includes/d365fin_md.md)]-lösning kräver.</span><span class="sxs-lookup"><span data-stu-id="b88ce-108">You must consider basic setup data and the types of data that your [!INCLUDE[d365fin](includes/d365fin_md.md)] solution will require.</span></span> <span data-ttu-id="b88ce-109">Samla sedan ihop all denna information i konfigurationspaket.</span><span class="sxs-lookup"><span data-stu-id="b88ce-109">You bundle all of this information in configuration packages.</span></span>

<span data-ttu-id="b88ce-110">RapidStart Services ger dig också de verktyg som du använder för att migrera bakåtkompatibla data, t.ex. kunder och leverantörer.</span><span class="sxs-lookup"><span data-stu-id="b88ce-110">RapidStart Services also provides you with the tools that you will use to migrate your legacy data, such as customers and vendors.</span></span>  

<span data-ttu-id="b88ce-111">Vi rekommenderar att du skapar konfigurationspaket där de flesta inställningstabellerna redan är ifyllda så att kunder bara behöver ändra några få inställningar när paketet används.</span><span class="sxs-lookup"><span data-stu-id="b88ce-111">We recommend that you create configuration packages with most of the setup tables already filled in, so that customers only have to change a few settings after the package is applied.</span></span> <span data-ttu-id="b88ce-112">När du till exempel skapar ett nytt företag kommer tabellerna **Nr-serier** och **Nr-serierad** att fyllas i med en uppsättning nummerserier och startnummer.</span><span class="sxs-lookup"><span data-stu-id="b88ce-112">For example, when you create a new company, the **No. Series** and the **No. Series Line** tables are filled in with a set of number series and starting numbers.</span></span> <span data-ttu-id="b88ce-113">Motsvarande **Nr-serie** i inställningstabellerna fylls också i automatiskt.</span><span class="sxs-lookup"><span data-stu-id="b88ce-113">The corresponding **No. Series** fields in the setup tables are also filled in automatically.</span></span> <span data-ttu-id="b88ce-114">Du måste inte att göra arbetet med att specificera nummerserier och andra grundläggande inställningsdata.</span><span class="sxs-lookup"><span data-stu-id="b88ce-114">You do not have to do the work of entering number series and other basic setup data.</span></span> <span data-ttu-id="b88ce-115">Du kan också ändra alla standarddata manuellt för RapidStart Services genom att använda konfigurationskalkylarket.</span><span class="sxs-lookup"><span data-stu-id="b88ce-115">You can also manually change all default data that is used with RapidStart Services by using the configuration worksheet.</span></span>  

<span data-ttu-id="b88ce-116">Konfigurationspaketen skapas utifrån ett förkonfigurerat företag.</span><span class="sxs-lookup"><span data-stu-id="b88ce-116">The configuration packages are built on a preconfigured company.</span></span> <span data-ttu-id="b88ce-117">När du har skapat ett företag som uppfyller dina behov kan du skapa ett konfigurationspaket som innehåller viktig information från det här företaget.</span><span class="sxs-lookup"><span data-stu-id="b88ce-117">After you have set up a company that meets your needs, you can create a configuration package that contains relevant data from this company.</span></span> <span data-ttu-id="b88ce-118">Då kan du använda den när du skapar ett nytt företag som ska konfigureras på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="b88ce-118">You can then use it when you create a new company that is to be configured in the same way.</span></span>  

<span data-ttu-id="b88ce-119">Om du vill underlätta importen av huvuddata, som kund- och leverantörsinformation, kan du använda konfigurationsmallar.</span><span class="sxs-lookup"><span data-stu-id="b88ce-119">To facilitate the import of master data, such as customer and vendor information, you can use configuration templates.</span></span> <span data-ttu-id="b88ce-120">Konfigurationsmallar innehåller en uppsättning standardinställningar som automatiskt tilldelas de transaktioner som importeras till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b88ce-120">Configuration templates contain a set of default settings that are automatically assigned to the records imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="b88ce-121">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="b88ce-121">The following table describes a sequence of tasks with links to topics that describe them.</span></span>

|<span data-ttu-id="b88ce-122">**För att**</span><span class="sxs-lookup"><span data-stu-id="b88ce-122">**To**</span></span>|<span data-ttu-id="b88ce-123">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="b88ce-123">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="b88ce-124">Planera en företagskonfiguration genom att fylla i konfigurationskalkylarket.</span><span class="sxs-lookup"><span data-stu-id="b88ce-124">Plan a company configuration by filling in the configuration worksheet.</span></span>|[<span data-ttu-id="b88ce-125">Så här hanterar du företagskonfigurationen i ett kalkylark</span><span class="sxs-lookup"><span data-stu-id="b88ce-125">Manage Company Configuration in a Worksheet</span></span>](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|<span data-ttu-id="b88ce-126">Skapa ett konfigurationspaket, anpassa ett paket, tilldela tabeller till ett paket, granska eller ändra kunddata, skapa det nya företaget och flytta testdata till produktionsmiljön.</span><span class="sxs-lookup"><span data-stu-id="b88ce-126">Create a configuration package, customize a package, assign tables to a package, review or edit existing customer data, create the new company and then move test data to the production environment.</span></span>|[<span data-ttu-id="b88ce-127">Förbered ett konfigurationspaket</span><span class="sxs-lookup"><span data-stu-id="b88ce-127">Prepare a Configuration Package</span></span>](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a><span data-ttu-id="b88ce-128">Se även</span><span class="sxs-lookup"><span data-stu-id="b88ce-128">See Also</span></span>  
[<span data-ttu-id="b88ce-129">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="b88ce-129">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="b88ce-130">Administration</span><span class="sxs-lookup"><span data-stu-id="b88ce-130">Administration</span></span>](admin-setup-and-administration.md)

