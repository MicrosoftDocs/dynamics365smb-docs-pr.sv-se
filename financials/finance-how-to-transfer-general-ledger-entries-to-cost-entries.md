---
title: "Så här: Överföra redovisningstransaktioner till kostnadstransaktioner | Microsoft Docs"
description: "Du kan överföra redovisningstransaktioner till kostnadstransaktioner."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4e68378d7acc789a70caf9c5b0590a81bf874337
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="1cf8a-103">Så här: Överföra redovisningstransaktioner till kostnadstransaktioner</span><span class="sxs-lookup"><span data-stu-id="1cf8a-103">How to: Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="1cf8a-104">Du kan överföra redovisningstransaktioner till kostnadstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="1cf8a-105">Innan du kör processen för att överföra redovisningstransaktioner till kostnadstransaktioner, måste du förbereda överföringen för att undvika manuella rättningsbokföringar.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="1cf8a-106">Så här förbereder du överföringen</span><span class="sxs-lookup"><span data-stu-id="1cf8a-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="1cf8a-107">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inställningar för kostnadsredovisning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1cf8a-108">I fönstret **Inställningar för kostnadsredovisning** kontrollerar du att fältet **startdatum för överföring till redovisning** anges till rätt värde.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-108">In the **Cost Accounting Setup** window, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="1cf8a-109">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lista över kostnadstyper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="1cf8a-110">I fönstret **Kostnadstypkort** kontrollerar du att fältet **Redovisningskontointervall** är korrekt länkat för alla kostnadstyper som tar transaktioner från redovisningen.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-110">In the **Cost Type Card** window, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="1cf8a-111">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kontoplan** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="1cf8a-112">För varje relevant redovisningskonto i fönstret **Redovisningskontokort** kontrollerar du att fältet **Kostnadstypsnr.**</span><span class="sxs-lookup"><span data-stu-id="1cf8a-112">For each relevant general ledger account, in the **G/L Account Card** window, verify that the **Cost Type No.**</span></span> <span data-ttu-id="1cf8a-113">är korrekt länkat till en kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="1cf8a-114">För mer information, se [Definiera relationen mellan kostnadstyper och redovisningskonton](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="1cf8a-114">For more information, see [Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span></span>  
7.  <span data-ttu-id="1cf8a-115">Kontrollera att alla relevanta redovisningstransaktioner har dimensionsvärden som motsvarar ett kostnadsställe och en kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="1cf8a-116">Så här överför du redovisningstransaktioner till kostnadstransaktioner</span><span class="sxs-lookup"><span data-stu-id="1cf8a-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="1cf8a-117">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Överför redovisningstransaktioner till kostnadsredovisning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1cf8a-118">Välj **Ja** för att starta överföringen.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="1cf8a-119">Processen överför alla redovisningstransaktioner som inte redan har överförts.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="1cf8a-120">Under överföringen skapar processen anslutningar i transaktionerna i tabellerna **Kostnadstransaktion** och **Bokförd journal för kostnad**.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="1cf8a-121">Det gör det möjligt att spåra ursprunget till kostnadstransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1cf8a-122">Se även</span><span class="sxs-lookup"><span data-stu-id="1cf8a-122">See Also</span></span>  
 <span data-ttu-id="1cf8a-123">[Villkor för överföring av redovisningstransaktioner till kostnadstransaktioner](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="1cf8a-123">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="1cf8a-124">[Automatisk överföring och kombinerade transaktioner](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="1cf8a-124">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
 <span data-ttu-id="1cf8a-125">[Resultat av överföringen](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="1cf8a-125">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 <span data-ttu-id="1cf8a-126">[Överföra och bokföra kostnadstransaktioner](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="1cf8a-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="1cf8a-127">Definiera relationen mellan kostnadstyper och redovisningskonton</span><span class="sxs-lookup"><span data-stu-id="1cf8a-127">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   
