---
title: Konfigurera räntevillkor
description: Läs om hur du konfigurerar Business Central så att du kan informera kunder om extra avgifter genom att skicka räntefakturor.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge
ms.date: 12/03/2020
ms.author: edupont
ms.openlocfilehash: dad02adfb6cc0a0ebb6d950b67f2e092b3313c59
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377093"
---
# <a name="set-up-finance-charge-terms"></a><span data-ttu-id="5033a-103">Konfigurera räntevillkor</span><span class="sxs-lookup"><span data-stu-id="5033a-103">Set Up Finance Charge Terms</span></span>

<span data-ttu-id="5033a-104">Om en kund inte har betalat på förfallodatumet kan du låta beräkna dröjsmålsränta automatiskt och lägga på den på de förfallna beloppen på kundens konto.</span><span class="sxs-lookup"><span data-stu-id="5033a-104">When a customer does not pay by the due date, you can have finance charges calculated automatically and add them to the overdue amounts on the customer's account.</span></span> <span data-ttu-id="5033a-105">Du kan informera kunder om debiterade dröjsmålsräntor genom att skicka räntefakturor.</span><span class="sxs-lookup"><span data-stu-id="5033a-105">You can inform customers of the added charges by sending finance charge memos.</span></span> <span data-ttu-id="5033a-106">Först måste du emellertid upprätta en kod som representerar respektive ränteberäkning.</span><span class="sxs-lookup"><span data-stu-id="5033a-106">But first, you must set up a code that represents each finance charge calculation.</span></span> <span data-ttu-id="5033a-107">Du kan sedan ange denna kod i fältet Räntevillkorskod på kundkorten.</span><span class="sxs-lookup"><span data-stu-id="5033a-107">Then you can enter this code in the Fin. Charge Terms Code field on customer cards.</span></span>  

## <a name="finance-charge-terms"></a><span data-ttu-id="5033a-108">Räntevillkor</span><span class="sxs-lookup"><span data-stu-id="5033a-108">Finance charge terms</span></span>

<span data-ttu-id="5033a-109">Du måste ange räntevillkor för respektive ränteberäkning och sedan tilldela villkoren till kunden i fältet **Räntevillkorskod** på sidan **Kund**.</span><span class="sxs-lookup"><span data-stu-id="5033a-109">You must set up finance charge terms for each finance charge calculation, and then assign the terms to the customer in the **Fin. Charge Terms Code** field on the **Customer** page.</span></span>

<span data-ttu-id="5033a-110">Räntor kan antingen beräknas med metoden genomsnittligt saldo per dag eller metoden förfallet saldo.</span><span class="sxs-lookup"><span data-stu-id="5033a-110">Finance charges can be calculated using either the average daily balance or the balance due methods.</span></span>

* <span data-ttu-id="5033a-111">Genomsnittligt saldo per dag</span><span class="sxs-lookup"><span data-stu-id="5033a-111">Average daily balance</span></span>  
  
  <span data-ttu-id="5033a-112">Hur många dagar som har passerat sedan betalningen förföll beaktas:</span><span class="sxs-lookup"><span data-stu-id="5033a-112">The number of days the payment is overdue is taken into account:</span></span>  
  <span data-ttu-id="5033a-113">*Metod för genomsnittligt saldo per dag* - *Räntefaktura* = *Förfallet belopp* x *(antal dagar försenat / ränteperiod)* x *(ränta/100)*</span><span class="sxs-lookup"><span data-stu-id="5033a-113">*Average Daily Balance method* - *Finance Charge* = *Overdue Amount* x *(Days Overdue / Interest Period)* x *(Interest Rate/100)*</span></span>

* <span data-ttu-id="5033a-114">Förfallet saldo</span><span class="sxs-lookup"><span data-stu-id="5033a-114">Balance due</span></span>  
  
  <span data-ttu-id="5033a-115">Räntan innebär helt enkelt en procentandel av det förfallna beloppet:</span><span class="sxs-lookup"><span data-stu-id="5033a-115">The finance charge is a percentage of the overdue amount:</span></span>  
  <span data-ttu-id="5033a-116">*Metod för förfallet saldo* - *Räntefaktura* = *Förfallet belopp* x *(ränta / 100)*</span><span class="sxs-lookup"><span data-stu-id="5033a-116">*Balance Due method* - *Finance Charge* = *Overdue Amount* x *(Interest Rate / 100)*</span></span>

<span data-ttu-id="5033a-117">Dessutom är varje villkor i tabellen Räntevillkor kopplad till en undertabell, nämligen Räntetext.</span><span class="sxs-lookup"><span data-stu-id="5033a-117">Additionally, each term in the Finance Charge Terms table is linked to a subtable, the Finance Charge Text table.</span></span> <span data-ttu-id="5033a-118">För respektive uppsättning av räntevillkor kan du definiera en inledande och/eller avslutande text som kan inkluderas på räntefakturan.</span><span class="sxs-lookup"><span data-stu-id="5033a-118">For each set of finance charge terms, you can define a beginning and/or an ending text to include on the finance charge memo.</span></span>

### <a name="to-set-up-finance-charge-terms"></a><span data-ttu-id="5033a-119">Ange räntevillkoren</span><span class="sxs-lookup"><span data-stu-id="5033a-119">To set up finance charge terms</span></span>

1. <span data-ttu-id="5033a-120">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Räntevillkor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5033a-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5033a-121">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="5033a-121">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="5033a-122">Om du vill använda fler än en uppsättning räntevillkor, anger du en kod för varje kombination.</span><span class="sxs-lookup"><span data-stu-id="5033a-122">To use more than one combination of finance charge terms, set up a code for each one.</span></span>

    <span data-ttu-id="5033a-123">För varje räntevillkor kan du ange särskilda villkor, som kan inkludera ytterligare avgifter i både BVA och i utländsk valuta.</span><span class="sxs-lookup"><span data-stu-id="5033a-123">For each finance charge term, you can specify individual conditions that can include additional fees in both LCY and in foreign currency.</span></span> <span data-ttu-id="5033a-124">Du kan definiera ytterliga avgifter i utländsk valuta för respektive villkor på sidan **Räntevillkor**.</span><span class="sxs-lookup"><span data-stu-id="5033a-124">You can define additional fees in foreign currencies for each term on the **Finance Charge Terms** page.</span></span>
4. <span data-ttu-id="5033a-125">Välj åtgärden **Valutor**.</span><span class="sxs-lookup"><span data-stu-id="5033a-125">Choose the **Currencies** action.</span></span>
5. <span data-ttu-id="5033a-126">På sidan **Valutor för räntevillkor** ange för varje villkor en valutakod och en tilläggsavgift.</span><span class="sxs-lookup"><span data-stu-id="5033a-126">On the **Currencies for Fin. Chrg. Terms** page, define for each term a currency code and an additional fee.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="5033a-127">När du skapar dröjsmålsränta i utländsk valuta används de villkor som angett här för att skapa räntefakturor.</span><span class="sxs-lookup"><span data-stu-id="5033a-127">When you create finance charges in a foreign currency, the foreign currency conditions that you set up here will be used to create finance charge memos.</span></span> <span data-ttu-id="5033a-128">Om det inte finns några räntevillkor definierade för utländsk valuta används de dröjsmålsräntevillkor för BVA som angetts på sidan **Räntevillkor** och omvandlas till relevant valuta.</span><span class="sxs-lookup"><span data-stu-id="5033a-128">If there are no foreign currency finance charge conditions set up, the LCY finance charge conditions specified on the **Finance Charge Terms** page will be used and then converted to the relevant currency.</span></span>

    <span data-ttu-id="5033a-129">För varje räntevillkor kan du ange text som ska infogas före (**Inledande text**) eller efter (**Avslutande text**) transaktionerna i räntefakturan.</span><span class="sxs-lookup"><span data-stu-id="5033a-129">For each finance charge term, you can specify text that will be printed before (**Beginning Text**) or after (**Ending Text**) on the entries on the finance charge memo.</span></span>  
6. <span data-ttu-id="5033a-130">Välj åtgärden **inledande text** eller **avslutande text** och fyll i på sidan **Räntetext**.</span><span class="sxs-lookup"><span data-stu-id="5033a-130">Choose the **Beginning Text** or **Ending Text** actions respectively, and fill on the **Finance Charge Text** page.</span></span>
7. <span data-ttu-id="5033a-131">Om du vill infoga relaterade värden i den resulterande Räntetext, anger du följande platshållare i **Text**-fältet.</span><span class="sxs-lookup"><span data-stu-id="5033a-131">To automatically insert related values in the resulting finance charge text, enter the following placeholders in the **Text** field.</span></span>

|<span data-ttu-id="5033a-132">Platshållare</span><span class="sxs-lookup"><span data-stu-id="5033a-132">Placeholder</span></span>|<span data-ttu-id="5033a-133">Värde</span><span class="sxs-lookup"><span data-stu-id="5033a-133">Value</span></span>|  
|-----------------|-----------|  
|<span data-ttu-id="5033a-134">%1</span><span class="sxs-lookup"><span data-stu-id="5033a-134">%1</span></span>|<span data-ttu-id="5033a-135">Innehållet i fältet **Dokumentdatum** i räntefakturans huvud</span><span class="sxs-lookup"><span data-stu-id="5033a-135">Content of the **Document Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="5033a-136">%2</span><span class="sxs-lookup"><span data-stu-id="5033a-136">%2</span></span>|<span data-ttu-id="5033a-137">Innehållet i fältet **Förfallodatum** i räntefakturans huvud</span><span class="sxs-lookup"><span data-stu-id="5033a-137">Content of the **Due Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="5033a-138">%3</span><span class="sxs-lookup"><span data-stu-id="5033a-138">%3</span></span>|<span data-ttu-id="5033a-139">Innehållet i fältet **Räntesats** på de relaterade räntevillkor</span><span class="sxs-lookup"><span data-stu-id="5033a-139">Content of the **Interest Rate** field on the related finance charge terms</span></span>|  
|<span data-ttu-id="5033a-140">%4</span><span class="sxs-lookup"><span data-stu-id="5033a-140">%4</span></span>|<span data-ttu-id="5033a-141">Innehållet i fältet **Återstående belopp** i räntefakturans huvud</span><span class="sxs-lookup"><span data-stu-id="5033a-141">Content of the **Remaining Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="5033a-142">%5</span><span class="sxs-lookup"><span data-stu-id="5033a-142">%5</span></span>|<span data-ttu-id="5033a-143">Innehållet i fältet **Räntebelopp** i räntefakturans huvud</span><span class="sxs-lookup"><span data-stu-id="5033a-143">Content of the **Interest Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="5033a-144">%6</span><span class="sxs-lookup"><span data-stu-id="5033a-144">%6</span></span>|<span data-ttu-id="5033a-145">Innehållet i fältet **Avgift** i räntefakturans huvud</span><span class="sxs-lookup"><span data-stu-id="5033a-145">Content of the **Additional Fee** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="5033a-146">%7</span><span class="sxs-lookup"><span data-stu-id="5033a-146">%7</span></span>|<span data-ttu-id="5033a-147">Påminnelsens totalbelopp.</span><span class="sxs-lookup"><span data-stu-id="5033a-147">The total amount of the reminder</span></span>|  
|<span data-ttu-id="5033a-148">%8</span><span class="sxs-lookup"><span data-stu-id="5033a-148">%8</span></span>|<span data-ttu-id="5033a-149">Innehållet i fältet **Valutakod** i räntefakturans huvud</span><span class="sxs-lookup"><span data-stu-id="5033a-149">Content of the **Currency Code** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="5033a-150">%9</span><span class="sxs-lookup"><span data-stu-id="5033a-150">%9</span></span>|<span data-ttu-id="5033a-151">Innehållet i fältet **Bokföringsdatum** i räntefakturans huvud</span><span class="sxs-lookup"><span data-stu-id="5033a-151">Content of the **Posting Date** field on the finance charge memo header</span></span>|  

## <a name="see-also"></a><span data-ttu-id="5033a-152">Se även</span><span class="sxs-lookup"><span data-stu-id="5033a-152">See also</span></span>

[<span data-ttu-id="5033a-153">Kräva in utestående saldon</span><span class="sxs-lookup"><span data-stu-id="5033a-153">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="5033a-154">Konfigurera påminnelsevillkor och nivåer</span><span class="sxs-lookup"><span data-stu-id="5033a-154">Set Up Reminder Terms and Levels</span></span>](finance-setup-reminders.md)  
[<span data-ttu-id="5033a-155">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="5033a-155">Setting Up Finance</span></span>](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]