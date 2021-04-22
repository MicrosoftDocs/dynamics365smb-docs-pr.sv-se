---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 95121642b62f33ea1fc160c103ee845816706530
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778653"
---
När alla artiklar har angetts på raderna kan du beräkna fakturarabatten för hela försäljningsdokumentet genom att välja åtgärden **Beräkna fakturarabatt**.

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
