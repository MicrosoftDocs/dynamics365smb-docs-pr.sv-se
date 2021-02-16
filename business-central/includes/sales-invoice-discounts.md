---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035797"
---
När alla artiklar har angetts på försäljningsorderraderna kan du beräkna försäljningsdokuments totala fakturarabatt genom att välja åtgärden **Beräkna fakturarabatt**.

Om fältet **Berk. fakturarabatt** väljs i fönstret **Försäljningsinställningar** kommer fakturarabatten att beräknas automatiskt när du gör något av följande i ett säljdokument:

* Visa statistik
* Visa en testrapport
* Skriv ut
* Post

Rabatten fördelas på alla försäljningsdokumentets rader för artiklar där fältet **Tillåt fakturarabatt** på försäljningsorderraden innehåller **Ja**. Detta är den förvalda inställningen för artiklar.

Villkoren för fakturarabatt definieras på sidan **Anp. fakturarabatter** för att beräkna fakturarabatten. Valutakoden i försäljningsdokumentet används för att hitta villkoren för fakturarabatt i motsvarande valuta.

Om inga fakturarabatter har definierats för utländska valutor används villkoren för fakturarabatt som definieras på sidan **Anp. fakturarabatter** med belopp i din lokala valuta, och valutakursen på bokföringsdatumet i säljdokumentet används för att beräkna fakturarabatten i den utländska valutan.
