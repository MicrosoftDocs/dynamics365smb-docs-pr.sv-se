---
title: Tips och råd - RapidStart Services | Microsoft Docs
description: När du konfigurerar företag som använder RapidStart Services finns några tips och trick som du kan använda för att implementeringen ska gå smidigt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: e1c3dfe37e6288934d05c4e2d9294cf87da49537
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786127"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="a5a88-103">Tips och råd: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="a5a88-103">Tips and Tricks: RapidStart Services</span></span>

<span data-ttu-id="a5a88-104">När du konfigurerar företag som använder RapidStart Services finns några tips och trick som du kan använda för att implementeringen ska gå smidigt.</span><span class="sxs-lookup"><span data-stu-id="a5a88-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="a5a88-105">Utnyttja fördelarna med konfigurationsmallar</span><span class="sxs-lookup"><span data-stu-id="a5a88-105">Take advantage of configuration templates</span></span>

<span data-ttu-id="a5a88-106">Konfigurationsmallar kan hjälpa dig att rationalisera din implementering.</span><span class="sxs-lookup"><span data-stu-id="a5a88-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="a5a88-107">Genom att använda dem kan du ta med liknande kunder i segment och sedan utveckla ett implementeringsprotokoll som behandlar alla kunder i ett segment på ungefär samma sätt.</span><span class="sxs-lookup"><span data-stu-id="a5a88-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="a5a88-108">På så sätt kan du tillämpa en nivå av förkonfiguration på varje segment och fortsätta med en snabb implementering.</span><span class="sxs-lookup"><span data-stu-id="a5a88-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="a5a88-109">Konfigurationsfrågeformulär</span><span class="sxs-lookup"><span data-stu-id="a5a88-109">Configuration questionnaires</span></span>

<span data-ttu-id="a5a88-110">Som hjälp vid processen att fylla i ett konfigurationsfrågeformulär bör du överväga att definiera standardsvar för att ange metodtips.</span><span class="sxs-lookup"><span data-stu-id="a5a88-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="a5a88-111">Batchskapande av journalrader</span><span class="sxs-lookup"><span data-stu-id="a5a88-111">Batch creation of journal lines</span></span>

<span data-ttu-id="a5a88-112">Vi rekommenderar att du använder datamigreringsverktygen som tillhandahålls för att migrera journaltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a5a88-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="a5a88-113">Annars, om du använder batch-jobbet för att skapa journalrader, har det en begränsad omfattning och skapar endast pre-standardfält i en journal.</span><span class="sxs-lookup"><span data-stu-id="a5a88-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="a5a88-114">Resten av journalen måste sedan avslutas manuellt.</span><span class="sxs-lookup"><span data-stu-id="a5a88-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="a5a88-115">Migrera transaktioner</span><span class="sxs-lookup"><span data-stu-id="a5a88-115">Migrating transactions</span></span>

<span data-ttu-id="a5a88-116">Vi rekommenderar att du migrerar ingående balanser i följande ordning.</span><span class="sxs-lookup"><span data-stu-id="a5a88-116">We recommend that you migrate opening balances in the following order.</span></span> <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. <span data-ttu-id="a5a88-117">Migrera redovisningen av ingående balanser utan att använda underredovisningarna för redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="a5a88-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="a5a88-118">Använd specifika motkonton för ingående balanser, en inställning för varje underredovisning.</span><span class="sxs-lookup"><span data-stu-id="a5a88-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="a5a88-119">Skapa motkonteringskontona för att aktivera direkt bokföring.</span><span class="sxs-lookup"><span data-stu-id="a5a88-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2. <span data-ttu-id="a5a88-120">Migrera öppna kundreskontratransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a5a88-120">Migrate open customer ledger entries.</span></span>  <!--work on these-->
3. <span data-ttu-id="a5a88-121">Migrera öppna artikeltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a5a88-121">Migrate open item ledger entries.</span></span>  
4. <span data-ttu-id="a5a88-122">Migrera öppna anläggningstillgångstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a5a88-122">Migrate open fixed asset entries.</span></span>  

## <a name="make-each-package-manageable"></a><span data-ttu-id="a5a88-123">Gör respektive paket hanterbart</span><span class="sxs-lookup"><span data-stu-id="a5a88-123">Make each package manageable</span></span>

<span data-ttu-id="a5a88-124">När du använder konfigurationspaket för att migrera data separerar du datan i separata paket för en enklare överföring.</span><span class="sxs-lookup"><span data-stu-id="a5a88-124">When you use configuration packages to migrate data, separate the data into separate packages for easier portability.</span></span> <span data-ttu-id="a5a88-125">Om du till exempel vill migrera 20 års poster i transaktionsregister kan importen ta många timmar och dagar i anspråk.</span><span class="sxs-lookup"><span data-stu-id="a5a88-125">For example, if you want to migrate 20 years of ledger entries, the import might take many hours and days.</span></span> <span data-ttu-id="a5a88-126">Se istället till att dela upp datan så att respektive paket blir mer hanterbart.</span><span class="sxs-lookup"><span data-stu-id="a5a88-126">Instead, split the data up so that each package becomes more manageable.</span></span> <span data-ttu-id="a5a88-127">Det finns för tillfället inga fasta regler för vad som gör ett paket effektivt, men om du upplever problem med att importera eller exportera ett paket, försök då göra det mindre och se om det hjälper.</span><span class="sxs-lookup"><span data-stu-id="a5a88-127">Currently, there are no firm rules for what makes a package performant, but if you see problems importing or exporting a package, try making it smaller and see if that helps.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a5a88-128">Se även</span><span class="sxs-lookup"><span data-stu-id="a5a88-128">See Also</span></span>

[<span data-ttu-id="a5a88-129">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="a5a88-129">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="a5a88-130">Administration</span><span class="sxs-lookup"><span data-stu-id="a5a88-130">Administration</span></span>](admin-setup-and-administration.md)  
