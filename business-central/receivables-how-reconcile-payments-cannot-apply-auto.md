---
title: Använda funktionen Överför differens till konto för att stämma av betalningar | Microsoft Docs
description: Beskriver hur du kan bearbeta betalningar som inte kan kopplas till ett dokument, till exempel när en valutakurs orsakar att belopp skiljer sig åt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 03/05/2019
ms.author: sgroespe
ms.openlocfilehash: 7d952f46d5e688fe1b86077723a0482c91995661
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807901"
---
# <a name="reconcile-payments-that-cannot-be-applied-automatically"></a>Så här stämmer du av betalningar som inte kan kopplas automatiskt
Du måste ibland hantera betalningar till ditt bankkonto som inte kan kopplas till en relaterad öppen kund, leverantör eller bankkontotransaktion. Anledningar kan vara att det inte finns något dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)] som betalningen kan kopplas till, eller det relaterade dokumentet i [!INCLUDE[d365fin](includes/d365fin_md.md)] har ett annat belopp än transaktionbeloppet, tex på grund av valutakursen. På sidan **Betalningavstämningjournal** visas inte alla transaktionsbelopp för betalningar som inte kopplats ännu i fältet **Skillnad** inklusive belopp, som inte kan användas på grund av anledningarna ovan.

Betalningar som inte kan kopplas kan visas på betalningavstämningjournalrader på följande sätt:

* Värdet i fältet **skillnad** är lika med värdet i fältet **transaktionbelopp** vilket betyder att ingen del av betalningen kan kopplas till en relaterad öppen kund, leverantör eller bankkontotransaktion.
* Värdet i fältet **skillnad** är lägre än värdet i fältet **transaktionbelopp** vilket betyder att ingen del av betalningen kan kopplas till en relaterad öppen kund, leverantör eller bankkontotransaktion. Återstående del av betalningen kan inte kopplas och måste avstämmas manuellt eller genom att bokföra den direkt till ett konto.

Om du vill avstämma sådana betalningar kan du välja knappen **Överför differens till konto** och sedan ange på vilket konto som beloppet i fältet **Skillnad** ska bokföras på när du bokför.

> [!TIP]  
>   Liknande funktioner finns för att definiera automatisk avstämning återkommande betalningar som inte kan användas till relaterade öppna kund-, leverantörs- eller bankkontotransaktioner. Mer information finns i [Mappa text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## <a name="to-reconcile-payments-that-cannot-be-applied-automatically"></a>Så här stämmer du av betalningar som inte kan kopplas automatiskt
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Betalningsavstämningsjournaler** och välj sedan relaterad länk.
2. Öppna en betalningsavstämningsjournal. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).
3. Välj **Överför differens till konto**. Sidan **Överför differens till konto** öppnas.
4. I fältet **Kontotyp** anger du typen av konto som betalningsbeloppet bokförs på.
5. I fältet **Kontotnr** anger du typen av konto som betalningsbeloppet bokförs på.
6. I fältet **Beskrivning** anger du den text som beskriver denna direktbetalningsbokföring.  Som standard infogas texten i fältet **transaktionstext** på betalningavstämningjournalraden.
7. Välj **OK**.

Om värdet i fältet **skillnad** var lika med värdet i fältet **transaktionbelopp** när du bokförde betalningavstämningjournalen, kommer hela betalningen på journalraden bokföras direkt på angivet motkonto.

Om värdet i fältet **skillnad**var mindre än värdet i fältet **transaktionsbelopp** kommer en ytterligare journalrad skapas med samma text och datum och med skillnaden som infogas i fältet **transaktionbelopp**. På den ursprungliga journalraden kommer skillnaden dras av från värdet i fältet **transaktionbelopp** och betalningen kommer att fortsätta vara kopplad till kund-, leverantörs- eller bankkontotransaktionen. När du bokför betalningsavstämningsjournalen kommer en del av betalningen att bokföras som en kopplad betalning. Den andra delen av betalningen ska bokföras direkt till det angivna kontot.

## <a name="see-also"></a>Se även
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
