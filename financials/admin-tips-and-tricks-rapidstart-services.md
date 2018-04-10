---
title: Tips och tricks - RapidStart Services | Microsoft Docs
description: "När du konfigurerar företag med hjälp av RapidStart Services finns några tips och tricks som du kan använda för att få implementeringen att förlöpa smidigt."
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
ms.openlocfilehash: e43859a6095f0087c12d0f9c071c0504d3781ad2
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="fd4f9-103">Tips och tricks: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="fd4f9-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="fd4f9-104">När du konfigurerar företag med hjälp av RapidStart Services finns några tips och tricks som du kan använda för att få implementeringen att förlöpa smidigt.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="fd4f9-105">Utnyttja fördelarna med konfigurationsmallar</span><span class="sxs-lookup"><span data-stu-id="fd4f9-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="fd4f9-106">Konfigurationsmallar kan hjälpa dig att rationalisera din implementering.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="fd4f9-107">Genom att använda dem kan du ta med liknande kunder i segment och sedan utveckla ett implementeringsprotokoll som behandlar alla kunder i ett segment på ungefär samma sätt.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="fd4f9-108">På så sätt kan du tillämpa en nivå av förkonfiguration på varje segment och fortsätta med en snabb implementering.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="fd4f9-109">Konfigurationsfrågeformulär</span><span class="sxs-lookup"><span data-stu-id="fd4f9-109">Configuration questionnaires</span></span>  
<span data-ttu-id="fd4f9-110">Som hjälp vid processen att fylla i ett konfigurationsfrågeformulär bör du överväga att definiera standardsvar för att ange metodtips.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="fd4f9-111">Batchskapande av journalrader</span><span class="sxs-lookup"><span data-stu-id="fd4f9-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="fd4f9-112">Vi rekommenderar att du använder datamigreringsverktygen som tillhandahålls för att migrera journaltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="fd4f9-113">Annars, om du använder batch-jobbet för att skapa journalrader, har det en begränsad omfattning och skapar endast pre-standardfält i en journal.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="fd4f9-114">Resten av journalen måste sedan avslutas manuellt.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="fd4f9-115">Migrera transaktioner</span><span class="sxs-lookup"><span data-stu-id="fd4f9-115">Migrating transactions</span></span>  
<span data-ttu-id="fd4f9-116">Vi rekommenderar att du migrerar ingående balanser i följande ordning.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-116">We recommend that you migrate opening balances in the following order.</span></span>  

1.  <span data-ttu-id="fd4f9-117">Migrera redovisningen av ingående balanser utan att använda underredovisningarna för redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="fd4f9-118">Använd specifika motkonton för ingående balanser, en inställning för varje underredovisning.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="fd4f9-119">Skapa motkonteringskontona för att aktivera direkt bokföring.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="fd4f9-120">Migrera öppna kundreskontratransaktioner.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-120">Migrate open customer ledger entries.</span></span>  
3.  <span data-ttu-id="fd4f9-121">Migrera öppna artikeltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="fd4f9-122">Migrera öppna anläggningstillgångstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="fd4f9-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fd4f9-123">Se även</span><span class="sxs-lookup"><span data-stu-id="fd4f9-123">See Also</span></span>  
[<span data-ttu-id="fd4f9-124">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="fd4f9-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="fd4f9-125">Administration</span><span class="sxs-lookup"><span data-stu-id="fd4f9-125">Administration</span></span>](admin-setup-and-administration.md)
