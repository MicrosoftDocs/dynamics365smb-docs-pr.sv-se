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
ms.lasthandoff: 07/07/2017


---
# <a name="entering-criteria-in-filters"></a>Ange villkor i filter
När du vill söka efter data, till exempel kundnamn, adresser eller produktgrupper, anger du kriterier. I sökkriterier kan du använda alla siffror och bokstäver som du normalt kan använda i det specifika fältet. Dessutom kan du använda specialtecken som du vill filtrera resultatet ytterligare.

## <a name="searching-using-the-quick-filter"></a>Sök genom att använda snabbfiltret
Du kan lägga till filter för alla sidor genom att använda snabbfiltret. Snabbfiltret aktiveras genom att välja ikonen med förstoringsglas i det övre högra hörnet av en sida. Filtrering av den här typen används för att snabbt ange kriterier.

> [!IMPORTANT]  
>   Snabbfiltret ger enkelt tillgång till filterdata genom att ange vanlig text, men ger även många alternativet för sökningkriterier. Beroende på om du anger vanlig text, eller text inklusive symboler, uppför sig snabbfiltret på olika sätt.  

* Om du anger vanlig text i sökkriterierna tolkas sökkriterierna som en skiftlägesokänslig sökning som innehåller viss text.  
* Om du anger en text inklusive symboler i sökkriterierna tolkas sökkriterierna exakt som du har angett den, och sökningen är skiftlägeskänslig.

### <a name="quick-filter-criteria"></a>Snabbfilterkriterium
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Sökkriterier</TH>
    <TH>Tolkat som…</TH>
    <TH>Returer...</TH>
  </TR>
  <TR>
    <TD>tillverk</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Alla transaktioner som innehåller texten <b>man</b> och är skiftlägesokänsliga.</TD>
  </TR>
  <TR>
    <TD>sö</TD>
    <TD>@&#42;se&#42;</TD>
    <TD>Alla transaktioner som innehåller texten <b>se</b> och är skiftlägesokänsliga.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Börjar med <b>Man</b> och är skiftlägeskänsligt.</TD>
    <TD>Alla poster som börjar med texten <b>Man</b>.</TD>
  </TR>
  <TR>
    <TD>'tillverk'</TD>
    <TD>En exakt text och är skiftlägeskänsligt.</TD>
    <TD>Alla poster som matchar <b>man</b> exakt.</TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Börjar med och skiftlägesokänsligt.</TD>
    <TD>Alla poster som börjar med <b>man</b>.</TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Slutar på och är skiftlägesokänsligt.</TD>
    <TD>Alla poster som slutar på <b>man</b>.</TD>
  </TR>
</TABLE>

> [!NOTE]  
>   Du kan inte använda ett jokertecken när du filtrerar på uppräkningsfält, t.ex fältet **Status** på försäljningsorder. För att ange ett filter för den här typen av fält kan du ange det numeriska värdet som en filtreringsparameter. Använd till exempel värdena **0**, **1**, **2** och **3** för att filtrera för dessa alternativ i fältet **Status** på en försäljningsorder, som har värdena **Öppna**, **Släppt**, **Väntar på godkännande** och **Väntar på förskottsbetalning**.  

## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

