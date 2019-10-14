---
title: Tips och råd - RapidStart Services | Microsoft Docs
description: När du konfigurerar företag som använder RapidStart Services finns några tips och trick som du kan använda för att implementeringen ska gå smidigt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d77aefd006031dde120851fe69c5abae9d46e49e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307807"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="43960-103">Tips och råd: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="43960-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="43960-104">När du konfigurerar företag som använder RapidStart Services finns några tips och trick som du kan använda för att implementeringen ska gå smidigt.</span><span class="sxs-lookup"><span data-stu-id="43960-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="43960-105">Utnyttja fördelarna med konfigurationsmallar</span><span class="sxs-lookup"><span data-stu-id="43960-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="43960-106">Konfigurationsmallar kan hjälpa dig att rationalisera din implementering.</span><span class="sxs-lookup"><span data-stu-id="43960-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="43960-107">Genom att använda dem kan du ta med liknande kunder i segment och sedan utveckla ett implementeringsprotokoll som behandlar alla kunder i ett segment på ungefär samma sätt.</span><span class="sxs-lookup"><span data-stu-id="43960-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="43960-108">På så sätt kan du tillämpa en nivå av förkonfiguration på varje segment och fortsätta med en snabb implementering.</span><span class="sxs-lookup"><span data-stu-id="43960-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="43960-109">Konfigurationsfrågeformulär</span><span class="sxs-lookup"><span data-stu-id="43960-109">Configuration questionnaires</span></span>  
<span data-ttu-id="43960-110">Som hjälp vid processen att fylla i ett konfigurationsfrågeformulär bör du överväga att definiera standardsvar för att ange metodtips.</span><span class="sxs-lookup"><span data-stu-id="43960-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="43960-111">Batchskapande av journalrader</span><span class="sxs-lookup"><span data-stu-id="43960-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="43960-112">Vi rekommenderar att du använder datamigreringsverktygen som tillhandahålls för att migrera journaltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="43960-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="43960-113">Annars, om du använder batch-jobbet för att skapa journalrader, har det en begränsad omfattning och skapar endast pre-standardfält i en journal.</span><span class="sxs-lookup"><span data-stu-id="43960-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="43960-114">Resten av journalen måste sedan avslutas manuellt.</span><span class="sxs-lookup"><span data-stu-id="43960-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="43960-115">Migrera transaktioner</span><span class="sxs-lookup"><span data-stu-id="43960-115">Migrating transactions</span></span>  
<span data-ttu-id="43960-116">Vi rekommenderar att du migrerar ingående balanser i följande ordning.</span><span class="sxs-lookup"><span data-stu-id="43960-116">We recommend that you migrate opening balances in the following order.</span></span>  

1.  <span data-ttu-id="43960-117">Migrera redovisningen av ingående balanser utan att använda underredovisningarna för redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="43960-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="43960-118">Använd specifika motkonton för ingående balanser, en inställning för varje underredovisning.</span><span class="sxs-lookup"><span data-stu-id="43960-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="43960-119">Skapa motkonteringskontona för att aktivera direkt bokföring.</span><span class="sxs-lookup"><span data-stu-id="43960-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="43960-120">Migrera öppna kundreskontratransaktioner.</span><span class="sxs-lookup"><span data-stu-id="43960-120">Migrate open customer ledger entries.</span></span>  
3.  <span data-ttu-id="43960-121">Migrera öppna artikeltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="43960-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="43960-122">Migrera öppna anläggningstillgångstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="43960-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="43960-123">Se även</span><span class="sxs-lookup"><span data-stu-id="43960-123">See Also</span></span>  
[<span data-ttu-id="43960-124">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="43960-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="43960-125">Administration</span><span class="sxs-lookup"><span data-stu-id="43960-125">Administration</span></span>](admin-setup-and-administration.md)
