---
title: "Ange sökkriterier i filer | Microsoft Docs"
description: "Beskriver hur du arbetar med filter, till exempel snabbfiltret för att förfina resultaten när du söker efter data."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="entering-criteria-in-filters"></a><span data-ttu-id="22f1b-103">Ange villkor i filter</span><span class="sxs-lookup"><span data-stu-id="22f1b-103">Entering Criteria in Filters</span></span>
<span data-ttu-id="22f1b-104">När du vill söka efter data, till exempel kundnamn, adresser eller produktgrupper, anger du kriterier.</span><span class="sxs-lookup"><span data-stu-id="22f1b-104">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="22f1b-105">I sökkriterier kan du använda alla siffror och bokstäver som du normalt kan använda i det specifika fältet.</span><span class="sxs-lookup"><span data-stu-id="22f1b-105">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="22f1b-106">Dessutom kan du använda specialtecken som du vill filtrera resultatet ytterligare.</span><span class="sxs-lookup"><span data-stu-id="22f1b-106">In addition, you can use special symbols to further filter the results.</span></span>

## <a name="searching-using-the-quick-filter"></a><span data-ttu-id="22f1b-107">Sök genom att använda snabbfiltret</span><span class="sxs-lookup"><span data-stu-id="22f1b-107">Searching using the Quick Filter</span></span>
<span data-ttu-id="22f1b-108">Du kan lägga till filter för alla sidor genom att använda snabbfiltret.</span><span class="sxs-lookup"><span data-stu-id="22f1b-108">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="22f1b-109">Snabbfiltret aktiveras genom att välja ikonen med förstoringsglas i det övre högra hörnet av en sida.</span><span class="sxs-lookup"><span data-stu-id="22f1b-109">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="22f1b-110">Filtrering av den här typen används för att snabbt ange kriterier.</span><span class="sxs-lookup"><span data-stu-id="22f1b-110">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="22f1b-111">Snabbfiltret ger enkelt tillgång till filterdata genom att ange vanlig text, men ger även många alternativet för sökningkriterier.</span><span class="sxs-lookup"><span data-stu-id="22f1b-111">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="22f1b-112">Beroende på om du anger vanlig text, eller text inklusive symboler, uppför sig snabbfiltret på olika sätt.</span><span class="sxs-lookup"><span data-stu-id="22f1b-112">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="22f1b-113">Om du anger vanlig text i sökkriterierna tolkas sökkriterierna som en skiftlägesokänslig sökning som innehåller viss text.</span><span class="sxs-lookup"><span data-stu-id="22f1b-113">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="22f1b-114">Om du anger en text inklusive symboler i sökkriterierna tolkas sökkriterierna exakt som du har angett den, och sökningen är skiftlägeskänslig.</span><span class="sxs-lookup"><span data-stu-id="22f1b-114">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="22f1b-115">Snabbfilterkriterium</span><span class="sxs-lookup"><span data-stu-id="22f1b-115">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="22f1b-116">Sökkriterier</span><span class="sxs-lookup"><span data-stu-id="22f1b-116">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="22f1b-117">Tolkat som…</span><span class="sxs-lookup"><span data-stu-id="22f1b-117">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="22f1b-118">Returer...</span><span class="sxs-lookup"><span data-stu-id="22f1b-118">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="22f1b-119">tillverk</span><span class="sxs-lookup"><span data-stu-id="22f1b-119">man</span></span></TD>
    <TD><span data-ttu-id="22f1b-120">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="22f1b-120">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="22f1b-121">Alla transaktioner som innehåller texten <b>man</b> och är skiftlägesokänsliga.</span><span class="sxs-lookup"><span data-stu-id="22f1b-121">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="22f1b-122">sö</span><span class="sxs-lookup"><span data-stu-id="22f1b-122">se</span></span></TD>
    <TD><span data-ttu-id="22f1b-123">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="22f1b-123">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="22f1b-124">Alla transaktioner som innehåller texten <b>se</b> och är skiftlägesokänsliga.</span><span class="sxs-lookup"><span data-stu-id="22f1b-124">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="22f1b-125">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="22f1b-125">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="22f1b-126">Börjar med <b>Man</b> och är skiftlägeskänsligt.</span><span class="sxs-lookup"><span data-stu-id="22f1b-126">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="22f1b-127">Alla poster som börjar med texten <b>Man</b>.</span><span class="sxs-lookup"><span data-stu-id="22f1b-127">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="22f1b-128">'tillverk'</span><span class="sxs-lookup"><span data-stu-id="22f1b-128">'man'</span></span></TD>
    <TD><span data-ttu-id="22f1b-129">En exakt text och är skiftlägeskänsligt.</span><span class="sxs-lookup"><span data-stu-id="22f1b-129">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="22f1b-130">Alla poster som matchar <b>man</b> exakt.</span><span class="sxs-lookup"><span data-stu-id="22f1b-130">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="22f1b-131">@man*</span><span class="sxs-lookup"><span data-stu-id="22f1b-131">@man*</span></span> </TD>
    <TD><span data-ttu-id="22f1b-132">Börjar med och skiftlägesokänsligt.</span><span class="sxs-lookup"><span data-stu-id="22f1b-132">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="22f1b-133">Alla poster som börjar med <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="22f1b-133">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="22f1b-134">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="22f1b-134">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="22f1b-135">Slutar på och är skiftlägesokänsligt.</span><span class="sxs-lookup"><span data-stu-id="22f1b-135">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="22f1b-136">Alla poster som slutar på <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="22f1b-136">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="22f1b-137">Du kan inte använda ett jokertecken när du filtrerar på uppräkningsfält, t.ex fältet **Status** på försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="22f1b-137">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="22f1b-138">För att ange ett filter för den här typen av fält kan du ange det numeriska värdet som en filtreringsparameter.</span><span class="sxs-lookup"><span data-stu-id="22f1b-138">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="22f1b-139">Använd till exempel värdena **0**, **1**, **2** och **3** för att filtrera för dessa alternativ i fältet **Status** på en försäljningsorder, som har värdena **Öppna**, **Släppt**, **Väntar på godkännande** och **Väntar på förskottsbetalning**.</span><span class="sxs-lookup"><span data-stu-id="22f1b-139">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span>  

## <a name="see-also"></a><span data-ttu-id="22f1b-140">Se även</span><span class="sxs-lookup"><span data-stu-id="22f1b-140">See Also</span></span>
<span data-ttu-id="22f1b-141">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="22f1b-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

