---
title: "Ställa in anläggningstillgångar | Microsoft Docs"
description: "Få information om de åtgärder som du måste göra om du vill ställa in anläggningstillgångar, till exempel maskiner eller byggnader."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: fac857ae94152104ea6640782a5f315424b739e7
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="ba965-103">Ställa in anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="ba965-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="ba965-104">Innan du kan arbeta med anläggningstillgångar, måste du definiera ett par saker:</span><span class="sxs-lookup"><span data-stu-id="ba965-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="ba965-105">Hur du försäkrar, underhåller och skriver av anläggningstillgångar.</span><span class="sxs-lookup"><span data-stu-id="ba965-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="ba965-106">Hur du registrerar kostnader och andra värden i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="ba965-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="ba965-107">I tabellen nedan finns länkar till mer information.</span><span class="sxs-lookup"><span data-stu-id="ba965-107">The table below has links to more information.</span></span> <span data-ttu-id="ba965-108">När du har skapat detta kan du starta olika aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="ba965-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="ba965-109">Mer information finns i [Anläggningstillgångar](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="ba965-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="ba965-110">Du kan bokföra anläggningstillgångstransaktioner i fönstret **Anl.tillg. redovisningsjournal** eller **Anlägg.tillg.journal** beroende på om transaktionerna är för finansiell rapportering eller för intern hantering.</span><span class="sxs-lookup"><span data-stu-id="ba965-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="ba965-111">Hjälp för anläggningstillgångar beskriver endast hur du använder fönstret **Anl.tillg. redovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="ba965-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="ba965-112">När du aktiverar en anläggningstillgångsaktivitet i avsnittet **Redov.integration** i fönstret **Avskrivningsregelkort**, sedan kommer fönstret **Anl.tillg. redovisningsjournal** att användas till att bokföra transaktionerna för aktiviteten i fråga.</span><span class="sxs-lookup"><span data-stu-id="ba965-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

<span data-ttu-id="ba965-113">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="ba965-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="ba965-114">Om du vill</span><span class="sxs-lookup"><span data-stu-id="ba965-114">To</span></span> | <span data-ttu-id="ba965-115">Gå till</span><span class="sxs-lookup"><span data-stu-id="ba965-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="ba965-116">Skapa standardredovisningskonton, fördelningsnycklar, journalmallar och batcher för fasta anläggningstillgångar och ställ in indelningar och underklasser för fasta anläggningstillgångar som till exempel Materiella och Immateriella.</span><span class="sxs-lookup"><span data-stu-id="ba965-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="ba965-117">Skapa allmän information om anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="ba965-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="ba965-118">Skapa avskrivningsregler, definiera avskrivningsmetoder, integrera med redovisningen och tillåta att transaktioner kan kopieras till flera avskrivningsregler.</span><span class="sxs-lookup"><span data-stu-id="ba965-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="ba965-119">Skapa avskrivning för anläggningstillgång</span><span class="sxs-lookup"><span data-stu-id="ba965-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="ba965-120">Aktivera försäkringsskydd för anläggningstillgångar, ange allmän försäkringsinformation, ett försäkringskort per brev och förbered journaler för att bokföra försäkringkostnader.</span><span class="sxs-lookup"><span data-stu-id="ba965-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="ba965-121">Skapa försäkring för anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="ba965-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="ba965-122">Aktivera underhåll av anläggningstillgångar, ange allmän underhållsinformation, skapa konton för bokföring av underhåll och definiera typer av underhållsarbete.</span><span class="sxs-lookup"><span data-stu-id="ba965-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="ba965-123">Skapa underhåll för anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="ba965-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="ba965-124">Lär dig mer om olika avskrivningsmetoder för anläggningstillgångarna.</span><span class="sxs-lookup"><span data-stu-id="ba965-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="ba965-125">Avskrivningsmetoder</span><span class="sxs-lookup"><span data-stu-id="ba965-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="ba965-126">Se även</span><span class="sxs-lookup"><span data-stu-id="ba965-126">See Also</span></span>
[<span data-ttu-id="ba965-127">Anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="ba965-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="ba965-128">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="ba965-128">Finance</span></span>](finance.md)  
[<span data-ttu-id="ba965-129">Komma igång</span><span class="sxs-lookup"><span data-stu-id="ba965-129">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="ba965-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ba965-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
