---
title: Så här ställer du in flera räntesatser
description: Du kan beräkna dröjsmålsränta med flera räntesatser för en särskild period. Ränteberäkningen görs på samma sätt för alla dröjsmålsräntor, men räntan kan variera under en viss period.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1a38e286dab02dcb23acaba39a0d61b0b939bb20
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775431"
---
# <a name="set-up-multiple-interest-rates"></a><span data-ttu-id="aa4df-104">Ställ in flera räntesatser</span><span class="sxs-lookup"><span data-stu-id="aa4df-104">Set Up Multiple Interest Rates</span></span>
<span data-ttu-id="aa4df-105">Flera räntesatser används för olika perioder för försenade betalningar i handelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="aa4df-105">Multiple interest rates are used for different periods for delayed payments in trade transactions.</span></span> <span data-ttu-id="aa4df-106">En myndighet anger till exempel den högsta räntan som kan tas ut för en kund.</span><span class="sxs-lookup"><span data-stu-id="aa4df-106">For example, a government specifies the maximum interest to be levied for a consumer.</span></span> <span data-ttu-id="aa4df-107">Den räntan kan ändras två gånger per år, den 1 januari och den 1 juli.</span><span class="sxs-lookup"><span data-stu-id="aa4df-107">This interest rate can be changed twice a year on 01 January and 01 July.</span></span> <span data-ttu-id="aa4df-108">Räntesatsen mellan företag avtalas av parterna och det finns ingen gräns för den kundgruppen.</span><span class="sxs-lookup"><span data-stu-id="aa4df-108">The interest rate between businesses (B2B) is agreed by the parties and there is no limit to that customer group.</span></span> <span data-ttu-id="aa4df-109">Den räntesatsen ligger vanligtvis 4 procent över den normala bankräntan.</span><span class="sxs-lookup"><span data-stu-id="aa4df-109">The announced rate is usually four percent more than the normal bank interest.</span></span>

<span data-ttu-id="aa4df-110">När du skapar villkor och betalningspåminnelsevillkor för räntefakturor, så kan du för avgiften för försenad betalning ange flera räntesatser så att avgiften beräknas utifrån olika räntesatser under olika perioder.</span><span class="sxs-lookup"><span data-stu-id="aa4df-110">When you create finance charge terms and reminder terms, for delayed payment penalty, you can specify multiple interest rates so that the penalty fee is calculated from different interest rates in different periods.</span></span> <span data-ttu-id="aa4df-111">Mer information finns i [Så här kräver du in utestående saldon](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="aa4df-111">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>

## <a name="to-set-up-multiple-interest-rates"></a><span data-ttu-id="aa4df-112">Så här ställer du in flera räntesatser</span><span class="sxs-lookup"><span data-stu-id="aa4df-112">To set up multiple interest rates</span></span>  
1.  <span data-ttu-id="aa4df-113">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Räntevillkor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="aa4df-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="aa4df-114">Gå till sidan **Räntevillkor** välj räntevillkoret och välj sedan åtgärden **Räntesatser**.</span><span class="sxs-lookup"><span data-stu-id="aa4df-114">On the **Finance Charge Terms** page, select the required finance term, and then choose the **Interest Rates** action.</span></span>  
3.  <span data-ttu-id="aa4df-115">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="aa4df-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="aa4df-116">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa4df-116">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="aa4df-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Betalningspåminnelsevillkor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="aa4df-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="aa4df-118">Gå till sidan **Betalningspåminnelsevillkor** välj villkoret och välj sedan åtgärden **Nivåer**.</span><span class="sxs-lookup"><span data-stu-id="aa4df-118">On the **Reminder Terms** page, select the required reminder term, and then choose the **Levels** action.</span></span>  
7.  <span data-ttu-id="aa4df-119">Markera fältet **Beräkna ränta** på sidan **Betalningspåminnelsenivåer**.</span><span class="sxs-lookup"><span data-stu-id="aa4df-119">On the **Reminder Levels** page, select the **Calculate Interest** field.</span></span>  

<span data-ttu-id="aa4df-120">När du skickar ut en räntefaktura, visar fakturan dröjsmålsräntan med flera räntesatser för en viss tidsperiod.</span><span class="sxs-lookup"><span data-stu-id="aa4df-120">When you issue a finance charge memo, the memo shows the finance charges with multiple interest rates for a specific time period.</span></span> <span data-ttu-id="aa4df-121">Räntefakturan innehåller även kontaktinformation för kunden, företaget som skickar räntefakturan, det ytterligare beloppet och totalt belopp.</span><span class="sxs-lookup"><span data-stu-id="aa4df-121">The memo also contains the contact details of the customer, the company issuing the memo, the additional amount, and the total amount.</span></span> <span data-ttu-id="aa4df-122">Den ingående transaktionen på räntefakturan visas i fet stil.</span><span class="sxs-lookup"><span data-stu-id="aa4df-122">The opening entry on the memo is displayed in bold.</span></span> <span data-ttu-id="aa4df-123">Dröjsmålsräntan beräknas med flera räntesatser för en viss tidsperiod och skrivs ut efter den ingående transaktionen på räntefakturan.</span><span class="sxs-lookup"><span data-stu-id="aa4df-123">The finance charges are calculated with multiple interest rates for a specific time period and are printed after the opening entry of the memo.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aa4df-124">Se även</span><span class="sxs-lookup"><span data-stu-id="aa4df-124">See Also</span></span>  
[<span data-ttu-id="aa4df-125">Kräva in utestående saldon</span><span class="sxs-lookup"><span data-stu-id="aa4df-125">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="aa4df-126">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="aa4df-126">Setting Up Finance</span></span>](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]