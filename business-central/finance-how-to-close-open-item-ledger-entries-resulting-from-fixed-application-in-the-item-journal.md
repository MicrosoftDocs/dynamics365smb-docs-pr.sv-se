---
title: Avsluta öppna artikeltransaktioner som skapas från en fast koppling i artikeljournalen | Microsoft Docs
description: Du kan använda fältet **Kopplas från löpnr** på sidan **Artikeljournal** för att skapa en fast koppling mellan en inkommande transaktion och den ursprungliga utgående transaktionen. Till exempel, för att korrigera utgående transaktion eller bearbeta dess retur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 7a7f31ea698a314d8a69c3bf9c2e7ab04ccd5f46
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783455"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Stäng öppna artikeltransaktioner som skapas från en fast koppling i artikeljournalen
Du kan använda fältet **Kopplas från löpnr** på sidan **Artikeljournal** för att skapa en fast koppling mellan en inkommande transaktion och den ursprungliga utgående transaktionen. Till exempel, för att korrigera utgående transaktion eller bearbeta dess retur. Mer information finns i Kopplas från löpnr.  

> [!IMPORTANT]  
>  Fast koppling som gjorts på det här sättet gäller endast kostnaden, inte antal. På så sätt kommer den bokförda positiv artikeltransaktion inte avsluta det kopplade avgående transaktion, och att stå öppen. Detta gäller också när du bokför en fast koppling för en positiv transaktion på en negativ transaktion som inte har avslutats av en vanlig positiva transaktion, kommer både negativ och de positiva transaktionerna finns kvar öppna.  
>   
>  Det innebär att du inte kan avsluta en lagerperiod, om sådan transaktion finns.  

I följande procedur beskrivs hur du avslutar sådana transaktioner genom att utföra två korrigerande bokföringar i artikeljournalen.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Om du vill avsluta öppna artikeltransaktioner som skapas från ett fast koppling i artikeljournalen  

1.  Använd fältet **Kopplas från löpnr** om du vill bokföra en positiv justering med motsvarande antal. Denna åtgärd stänger den ursprungliga negativ transaktion med en fast koppling.  
2.  Använd fältet **Kopplas till löpnr** om du vill bokföra en negativ justering. Denna åtgärd stänger den korrigerande positiva transaktionen med en fast koppling.  

## <a name="see-also"></a>Se även  
[ Ta bort och koppla om artikeltransaktioner](finance-how-to-remove-and-reapply-item-entries.md)  
 [Behandla försäljningsreturer och annulleringar](sales-how-process-sales-returns-cancellations.md)   
 [Ställa in lagervärdering och lagerkostnad](finance-set-up-inventory-valuation-and-costing.md)   
 [Hantera lagerkostnader](finance-manage-inventory-costs.md)   
 [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)
