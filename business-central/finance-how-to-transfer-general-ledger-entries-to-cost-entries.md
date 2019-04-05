---
title: 'Så här: Överföra redovisningstransaktioner till kostnadstransaktioner | Microsoft Docs'
description: Du kan överföra redovisningstransaktioner till kostnadstransaktioner.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 273a8c4341f621710819fd5fbc5cb8ce579c86f5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "808033"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="b40d6-103">Överföra redovisningstransaktioner till kostnadstransaktioner</span><span class="sxs-lookup"><span data-stu-id="b40d6-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="b40d6-104">Du kan överföra redovisningstransaktioner till kostnadstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="b40d6-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="b40d6-105">Innan du kör processen för att överföra redovisningstransaktioner till kostnadstransaktioner, måste du förbereda överföringen för att undvika manuella rättningsbokföringar.</span><span class="sxs-lookup"><span data-stu-id="b40d6-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="b40d6-106">Så här förbereder du överföringen</span><span class="sxs-lookup"><span data-stu-id="b40d6-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="b40d6-107">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inställningar för kostnadsredovisning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b40d6-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b40d6-108">På sidan **Inställningar för kostnadsredovisning** kontrollerar du att fältet **startdatum för överföring till redovisning** anges till rätt värde.</span><span class="sxs-lookup"><span data-stu-id="b40d6-108">On the **Cost Accounting Setup** page, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="b40d6-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lista över kostnadstyper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b40d6-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="b40d6-110">På sidan **Kostnadstypkort** kontrollerar du att fältet **Redovisningskontointervall** är korrekt länkat för alla kostnadstyper som tar transaktioner från redovisningen.</span><span class="sxs-lookup"><span data-stu-id="b40d6-110">On the **Cost Type Card** page, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="b40d6-111">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontoplan** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b40d6-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="b40d6-112">För varje relevant redovisningskonto på sidan **Redovisningskontokort** kontrollerar du att fältet **Kostnadstypsnr.**</span><span class="sxs-lookup"><span data-stu-id="b40d6-112">For each relevant general ledger account, on the **G/L Account Card** page, verify that the **Cost Type No.**</span></span> <span data-ttu-id="b40d6-113">är korrekt länkat till en kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="b40d6-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="b40d6-114">Mer information finns i [Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="b40d6-114">For more information, see [Setting Up Cost Accounting](finance-set-up-cost-accounting.md).</span></span>  
7.  <span data-ttu-id="b40d6-115">Kontrollera att alla relevanta redovisningstransaktioner har dimensionsvärden som motsvarar ett kostnadsställe och en kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="b40d6-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="b40d6-116">Så här överför du redovisningstransaktioner till kostnadstransaktioner</span><span class="sxs-lookup"><span data-stu-id="b40d6-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="b40d6-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Överför redovisningstransaktioner till kostnadsredovisning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b40d6-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b40d6-118">Välj **Ja** för att starta överföringen.</span><span class="sxs-lookup"><span data-stu-id="b40d6-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="b40d6-119">Processen överför alla redovisningstransaktioner som inte redan har överförts.</span><span class="sxs-lookup"><span data-stu-id="b40d6-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="b40d6-120">Under överföringen skapar processen anslutningar i transaktionerna i tabellerna **Kostnadstransaktion** och **Bokförd journal för kostnad**.</span><span class="sxs-lookup"><span data-stu-id="b40d6-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="b40d6-121">Det gör det möjligt att spåra ursprunget till kostnadstransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="b40d6-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b40d6-122">Se även</span><span class="sxs-lookup"><span data-stu-id="b40d6-122">See Also</span></span>  
<span data-ttu-id="b40d6-123">[Överföra och bokföra kostnadstransaktioner](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="b40d6-123">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
[<span data-ttu-id="b40d6-124">Ställa in kostnadsredovisning</span><span class="sxs-lookup"><span data-stu-id="b40d6-124">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)   
