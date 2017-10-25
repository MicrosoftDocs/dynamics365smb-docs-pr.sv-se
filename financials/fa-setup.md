---
title: "Ställa in anläggningstillgångar | Microsoft Docs"
description: "Få information om de åtgärder som du måste göra om du vill ställa in anläggningstillgångar, till exempel maskiner eller byggnader."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9dea8be0f5b0200f97082dc25dbaa2483ad6c735
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="cb3aa-103">Ställa in anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="cb3aa-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="cb3aa-104">Innan du kan arbeta med anläggningstillgångar, måste du definiera ett par saker:</span><span class="sxs-lookup"><span data-stu-id="cb3aa-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="cb3aa-105">Hur du försäkrar, underhåller och skriver av anläggningstillgångar.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="cb3aa-106">Hur du registrerar kostnader och andra värden i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="cb3aa-107">I tabellen nedan finns länkar till mer information.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-107">The table below has links to more information.</span></span> <span data-ttu-id="cb3aa-108">När du har skapat detta kan du starta olika aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="cb3aa-109">Mer information finns i [Anläggningstillgångar](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="cb3aa-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="cb3aa-110">Du kan bokföra anläggningstillgångstransaktioner i fönstret **Anl.tillg. redovisningsjournal** eller **Anlägg.tillg.journal** beroende på om transaktionerna är för finansiell rapportering eller för intern hantering.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="cb3aa-111">Hjälp för anläggningstillgångar beskriver endast hur du använder fönstret **Anl.tillg. redovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="cb3aa-112">När du aktiverar en anläggningstillgångsaktivitet i avsnittet **Redov.integration** i fönstret **Avskrivningsregelkort**, sedan kommer fönstret **Anl.tillg. redovisningsjournal** att användas till att bokföra transaktionerna för aktiviteten i fråga.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

> [!NOTE]  
>  <span data-ttu-id="cb3aa-113">Den här funktionen kräver att din upplevelse är inställd på **Paket**.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-113">This functionality requires that the experience is set to **Suite**.</span></span> <span data-ttu-id="cb3aa-114">Mer information finns i [anpassa din Financials-upplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="cb3aa-114">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>  

<span data-ttu-id="cb3aa-115">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-115">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="cb3aa-116">Om du vill</span><span class="sxs-lookup"><span data-stu-id="cb3aa-116">To</span></span> | <span data-ttu-id="cb3aa-117">Gå till</span><span class="sxs-lookup"><span data-stu-id="cb3aa-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="cb3aa-118">Skapa standardredovisningskonton, fördelningsnycklar, journalmallar och batcher för fasta anläggningstillgångar och ställ in indelningar och underklasser för fasta anläggningstillgångar som till exempel Materiella och Immateriella.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-118">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="cb3aa-119">Så här skapar du allmän information för anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="cb3aa-119">How to: Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="cb3aa-120">Skapa avskrivningsregler, definiera avskrivningsmetoder, integrera med redovisningen och tillåta att transaktioner kan kopieras till flera avskrivningsregler.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-120">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="cb3aa-121">Så här skapar du avskrivning av anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="cb3aa-121">How to: Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="cb3aa-122">Aktivera försäkringsskydd för anläggningstillgångar, ange allmän försäkringsinformation, ett försäkringskort per brev och förbered journaler för att bokföra försäkringkostnader.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-122">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="cb3aa-123">Så här skapar du försäkring för anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="cb3aa-123">How to: Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="cb3aa-124">Aktivera underhåll av anläggningstillgångar, ange allmän underhållsinformation, skapa konton för bokföring av underhåll och definiera typer av underhållsarbete.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-124">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="cb3aa-125">Så här skapar du underhåll av anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="cb3aa-125">How to: Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="cb3aa-126">Lär dig mer om olika avskrivningsmetoder för anläggningstillgångarna.</span><span class="sxs-lookup"><span data-stu-id="cb3aa-126">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="cb3aa-127">Avskrivningsmetoder</span><span class="sxs-lookup"><span data-stu-id="cb3aa-127">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="cb3aa-128">Se även</span><span class="sxs-lookup"><span data-stu-id="cb3aa-128">See Also</span></span>
[<span data-ttu-id="cb3aa-129">Anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="cb3aa-129">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="cb3aa-130">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="cb3aa-130">Finance</span></span>](finance.md)  
<span data-ttu-id="cb3aa-131">[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="cb3aa-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="cb3aa-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cb3aa-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

