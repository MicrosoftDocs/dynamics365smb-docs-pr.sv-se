---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470293"
---
När alla artiklar har angetts på försäljningsraderna kan du beräkna fakturarabatten för hela dokumentet genom att välja åtgärden **Beräkna fakturarabatt**.

Rabatten beräknas baserat på alla försäljningsdokumentets rader för artiklar där fältet **Tillåt fakturarabatt** på försäljningsorderraden innehåller **Ja**. Detta är den förvalda inställningen för artiklar. Rader med artikelomkostnader ingår till exempel inte i beräkningen av fakturarabatten. Om du vill tillämpa en rabatt på sådana rader måste du ange fältet **Radrabatt %** på de relevanta raderna.  

> [!TIP]
> Om fältet **Beräkn. fakturarabatt** väljs på sidan **Försäljningsinställningar** kommer fakturarabatten att beräknas automatiskt när du gör något av följande i ett säljdokument:
>
> * Visa statistik
> * Visa en testrapport
> * Skriv ut
> * Post

Villkoren för fakturarabatt för en kund definieras på sidan **Kundfakturarabatter** för kunden. Valutakoden i försäljningsdokumentet används för att hitta villkoren för fakturarabatt i motsvarande valuta.

Om inga fakturarabatter har definierats för utländska valutor används villkoren för fakturarabatt som definieras på sidan **Anp. fakturarabatter** med belopp i din lokala valuta, och valutakursen på bokföringsdatumet i säljdokumentet används för att beräkna fakturarabatten i den utländska valutan.
