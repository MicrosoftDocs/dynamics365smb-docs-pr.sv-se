---
title: Kassaflöde, översikt
description: En översikt över kassainflöden och kassautflöden för att hjälpa till att beräkna pengar som ska tas emot och betalas ut.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash flow, money flow, expense and income, liquidity, cash receipts minus cash payments
ms.date: 06/08/2021
ms.author: a-jillk
ms.reviewer: edupont
ms.openlocfilehash: 8359d95b36d6c16b179de2fce400c44fd93ec0f1
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216408"
---
# <a name="cash-flow-overview"></a>Kassaflöde, översikt

Att förstå kassainflöde och kassautflöde är nyckeln till att driva en framgångsrik verksamhet. Du kan använda kassaflöde för att enkelt skapa en kortfristig prognos som förutsäger hur och när du kan förvänta dig pengar in i och ut ur verksamheten. Det är viktigt att du vet att ditt företag har tillräckligt mycket kontanter för att betala fordringsägare och kostnader när de förfaller.

## <a name="definition-of-cash-flow"></a>Definition av kassaflöde

Termen *kassaflöde* används för att visa inbetalningar minus utbetalningar under en vald period. Det är en uppskattning av den mängd pengar du kan förvänta dig in i och ut ur din verksamhet, och innefattar alla förväntade intäkter och kostnader.

## <a name="cash-flow-overview"></a>Kassaflöde, översikt

Illustrationen visar en översikt över hur du kan arbeta med kassaflöde.

![Kassaflöde, översikt](media/finance_cash_flow_overview.png "Kassaflöde, översikt")

- Du gör en kassaflödesprognos.  

- Du får kassaflödesprognoskällor från följande områden:  

  - Redovisningen – information om likvida medel och de budgeterade intäkterna och kostnaderna för ditt företag.  
  - Inköp – information om aktuella utbetalningar och eventuella förutsedda skulder från öppna inköpsorder.  
  - Sälj – information om aktuella inbetalningar och eventuella förutsedda intäkter från öppna säljorder.  
  - Service – information om öppna serviceorder.  
  - Anläggningstillgångar – information om planerade avyttringar och budgeterade inköp av anläggningstillgångar.  
  - Manuella intäkter och kostnader – hantera manuella intäkter och kostnader och inkludera dem i kassaflödesprognosen.  
- Du kan använda ett batchjobb för att överföra information från områden i redovisningen, försäljning, inköp, service och anläggningstillgångar till förslaget. Sedan registrerar du förslagsrader för att göra en kassaflödesprognos.  
- Du använder olika fönster, rapporter och diagram för att analysera och skriva ut en kassaflödesprognos som avser tillgänglighets- och tidslinjeöversikter.  

## <a name="making-a-cash-flow-forecast"></a>Göra en prognos för kassaflöde

Baserat på registrerade förslagsrader kan du regelbundet göra en kassaflödesprognos. Följande layout är en vanligen använd layout för en kassaflödesprognos. Layouten har tre avsnitt:

  - Inbetalning  
  - Kontantutbetalning  
  - Nettokassaflöde eller kontanter i handen  

Inbetalningar ger detaljerad information om inkomsten som rörelsen tar emot.

*totala inbetalningar* = *kundreskontra* + *öppna säljorder* + *öppna serviceorder* + *avyttring av anläggningstillgångar* + *manuella intäkter* + *budgeterade intäkter*

> [!NOTE]
> Manuella intäkter kan vara hyresinkomster, ränta från finansiella tillgångar eller nytt privat kapital. Du kan planera manuella intäkter för en tidsperiod och använda dem i beräkningen av kassaflödesprognosen.

Kontantutbetalningar ger detaljerad information om betalningar som görs av verksamheten.

*totala kontantutbetalningar* = *leverantörsreskontra* + *öppna inköptsorder* + *investering i anläggningstillgångar* + *manuella kostnader* + *budgeterade kostnader*

> [!NOTE]
> Manuella kostnader kan vara löner, ränta på krediter eller privata förbrukningskostnader. Du kan planera manuella kostnader för en tidsperiod och använda dem i beräkningen av kassaflödesprognosen.

Nettokassaflöde eller kontanter i handen beräknas som totala inbetalningar minus totala utbetalningar i slutet av varje period.

*nettokassaflöde* = *totala inbetalningar* – *totala kontantutbetalningar* + *likvida medel*

Prognosen kan sedan användas som ett internt beslutsverktyg som hjälper dig att planera framåt och göra viktiga strategiska beslut i verksamheten.

## <a name="see-also"></a>Se även
[Ställa in analys för kassaflöde](finance-setup-cash-flow-analyses.md)  
[Analysera kassaflöde](finance-analyze-cash-flow.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
