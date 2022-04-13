---
title: Granska och koppla betalningar manuellt efter automatisk koppling
description: När betalningen kopplas automatiskt, kan du granska alla poster för en betalning och manuellt återställa dem som använts felaktigt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.search.form: 1290, 1294, 1287
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f1d14532095fd2d34f1dbdf57a3916dbd1c561a3
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8513711"
---
# <a name="review-and-apply-payments-manually-after-automatic-application"></a>Granska och koppla betalningar manuellt efter automatisk koppling
För varje journalrad som representerar en betalning på sidan **Betalningsavstämningsjournal** kan du öppna sidan **Betalningskoppling** för att visa alla öppna kandidattransaktioner för betalningen och för att visa detaljerad information för varje transaktion om datamatchningen som en betalningskoppling baseras på. Här kan du koppla manuellt betalningar eller koppla om betalningar som kopplades automatiskt till fel transaktion. Mer information om automatisk koppling finns i [Så här stämmer du av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]  
>   När bankkontot som du stämmer av betalningar för ställs in för lokal valuta kommer sidan **Betalningskoppling** att visa alla öppna transaktioner i lokal valuta, inklusive öppna transaktioner för dokument som fakturerats ursprungligen i utländsk valuta. Betalningar som kopplas till transaktioner med konverterade valutor kan därför bokföras med olika belopp än på originaldokumentet på grund av de eventuellt olika valutakurserna som används av banken och [!INCLUDE[prod_short](includes/prod_short.md)].

Därför bör du söka efter utländska valutakoder i fältet **Valutakod** på sidan **Betalningskoppling** för att kontrollera om kopplingar baseras på konverterade valutor. Om du vill förhandsgranska belopp i det ursprungliga dokumentet i utländsk valuta och för att se den valutakursen som används, välj fältet **Kopplas till löpnr.** och sedan, på snabbmenyn, väljer du knappen för att öppna sidan **Kundreskontratransaktioner** eller **Lev.reskontratransaktioner**.

Vinst-och-förlustjusteringar som krävs på grund av valutakonverteringar hanteras inte automatiskt i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]  
>   Du kan inte koppla transaktioner till ett annat tecken än tecknet på betalningen. Om du till exempel vill stänga både en kreditnota med negativt tecken och dess relaterade faktura med positivt tecken måste du först koppla kreditnotan till fakturan och sedan koppla betalningen till fakturan med det reducerade återstående beloppet.

> [!WARNING]  
>   Om du använder kassarabatter och om betalningsdatumet infaller före betalningens förfallodatum kommer fältet **Återstående belopp inkl. rabatt** på sidan **Betalningskoppling** att användas för matchning. Annars kommer värdet i fältet **Återstående belopp** att användas. Om betalningen skickades med ett rabatterat belopp efter betalningens förfallodatum eller om hela beloppet betalades men en kassarabatt har lämnats kommer beloppet inte att matchas.

> [!NOTE]  
>   Du kan bara koppla en betalning till ett konto. Om du vill dela kopplingen på flera öppna transaktioner, till exempel för att koppla en klumpsummabetalning måste de öppna transaktionerna vara för samma konto. Mer information finns i moment 7 och 8 i proceduren i det här avsnittet.

## <a name="to-review-or-apply-payments-after-automatic-application"></a>Så här granskar och kopplar du betalningar efter automatisk koppling
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **betalningsavstämningsjournal** och väljer sedan relaterad länk.
2. Öppna betalningsavstämningsjournalen för ett bankkonto som du vill stämma av betalningar för. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).
3. På sidan **Betalningsavstämningsjournal** väljer du en betalning som du vill granska eller manuellt koppla till en eller flera öppna transaktioner, och väljer sedan åtgärden **Koppla manuellt**.
4. Välj kryssrutan **Kopplat** på raden för den öppna transaktion som du vill koppla betalningen till.
5. Betalningsbeloppet, som visas även i fältet **Transaktionsbelopp** på sidan **Betalningskoppling** infogas i fältet **Kopplade belopp** men du kan ändra fältet, t. ex. om du vill koppla beloppet till flera öppna transaktioner.
6. Om du vill koppla en del av det betalda beloppet till en annan öppen transaktion för kontot, till exempel för att koppla klumpsummabetalning, markera kryssrutan **Kopplad** för raden. Det kopplade beloppet dras automatiskt av från transaktionsbeloppet för att motsvara distributionen på de två öppna transaktionerna.
7. Skapa en ny rad under raden för samma konto för att koppla en del av en betalning till en eller flera öppna transaktioner som inte finns i databasen. I fältet **Kopplat belopp** anger du beloppet som ska kopplas på nya raden och justerar sedan fältet **Kopplat belopp** på den befintliga raden.
8. Upprepa moment 5, 6 eller 7 för andra öppna transaktioner som du vill koppla en del av eller hela betalningsbeloppet till.
9. När du har granskat en betalningskoppling eller manuellt har kopplat till en eller flera öppna transaktioner väljer du åtgärden **Acceptera koppling**.

Sidan **Betalningskoppling** stängs och på sidan **Betalningsavstämningsjournal** ändras värdet i fältet **Matchningssäkerhet** till **Accepterat** för att ange att du har granskat eller manuellt kopplat betalningen.

## <a name="see-also"></a>Se även
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]