---
title: "Kontrollera automatiskt tillämpade betalningar och koppla betalningar manuellt | Microsoft Docs"
description: "När betalningen kopplas automatiskt, kan du granska alla poster för en betalning och manuellt återställa dem som använts felaktigt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 745766657fe7e993aaa689f0074c4f4a41e0090c
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="review-or-apply-payments-manually-after-automatic-application"></a>Så här granskar och kopplar du betalningar manuellt efter automatisk koppling
För varje journalrad som representerar en betalning i fönstret **Betalningsavstämningsjournal** kan du öppna fönstret **Betalningskoppling** för att visa alla öppna kandidattransaktioner för betalningen och för att visa detaljerad information för varje transaktion om datamatchningen som en betalningskoppling baseras på. Här kan du koppla manuellt betalningar eller koppla om betalningar som kopplades automatiskt till fel transaktion. Mer information om automatisk koppling finns i [Så här stämmer du av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]  
>   När bankkontot som du stämmer av betalningar för ställs in för lokal valuta kommer fönstret **Betalningskoppling** att visa alla öppna transaktioner i lokal valuta, inklusive öppna transaktioner för dokument som fakturerats ursprungligen i utländsk valuta. Betalningar som kopplas till transaktioner med konverterade valutor kan därför bokföras med olika belopp än på originaldokumentet på grund av de eventuellt olika valutakurserna som används av banken och [!INCLUDE[d365fin](includes/d365fin_md.md)].

Därför bör du söka efter utländska valutakoder i fältet **Valutakod**i fönstret **Betalningskoppling** för att kontrollera om kopplingar baseras på konverterade valutor. Om du vill förhandsgranska belopp i det ursprungliga dokumentet i utländsk valuta och för att se den valutakursen som används, välj fältet **Kopplas till löpnr.** och sedan, på snabbmenyn, väljer du knappen för att öppna fönstren **Kundreskontratransaktioner** eller **Lev.reskontratransaktioner**.

Vinst-och-förlustjusteringar som krävs på grund av valutakonverteringar hanteras inte automatiskt i [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]  
>   Du kan inte koppla transaktioner till ett annat tecken än tecknet på betalningen. Om du till exempel vill stänga både en kreditnota med negativt tecken och dess relaterade faktura med positivt tecken måste du först koppla kreditnotan till fakturan och sedan koppla betalningen till fakturan med det reducerade återstående beloppet.

> [!WARNING]  
>   Om du använder kassarabatter och om betalningsdatumet infaller före betalningens förfallodatum kommer fältet **Återstående belopp inkl. rabatt** i fönstret **Betalningskoppling** att användas för matchning. Annars kommer värdet i fältet **Återstående belopp** att användas. Om betalningen skickades med ett rabatterat belopp efter betalningens förfallodatum eller om hela beloppet betalades men en kassarabatt har lämnats kommer beloppet inte att matchas.

> [!NOTE]  
>   Du kan bara koppla en betalning till ett konto. Om du vill dela kopplingen på flera öppna transaktioner, till exempel för att koppla en klumpsummabetalning måste de öppna transaktionerna vara för samma konto. Mer information finns i moment 7 och 8 i proceduren i det här avsnittet.

## <a name="to-review-or-apply-payments-after-automatic-application"></a>Så här granskar och kopplar du betalningar efter automatisk koppling
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Betalningsavstämningsjournaler** och välj sedan relaterad länk.
2. Öppna betalningsavstämningsjournalen för ett bankkonto som du vill stämma av betalningar för. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).
3. I fönstret **Betalningsavstämningsjournal** väljer du en betalning som du vill granska eller manuellt koppla till en eller flera öppna transaktioner, och väljer sedan åtgärden**Koppla manuellt**.
4. Välj kryssrutan **Kopplat** på raden för den öppna transaktion som du vill koppla betalningen till.
5. Betalningsbeloppet, som visas även i fältet **Transaktionsbelopp** i fönstret **Betalningskoppling** infogas i fältet **Kopplade belopp** men du kan ändra fältet, t.ex. om du vill koppla beloppet till flera öppna transaktioner.
6. Om du vill koppla en del av det betalda beloppet till en annan öppen transaktion för kontot, till exempel för att koppla klumpsummabetalning, markera kryssrutan **Kopplad** för raden. Det kopplade beloppet dras automatiskt av från transaktionsbeloppet för att motsvara distributionen på de två öppna transaktionerna.
7. Skapa en ny rad under raden för samma konto för att koppla en del av en betalning till en eller flera öppna transaktioner som inte finns i databasen. I fältet **Kopplat belopp** anger du beloppet som ska kopplas på nya raden och justerar sedan fältet **Kopplat belopp** på den befintliga raden.
8. Upprepa moment 5, 6 eller 7 för andra öppna transaktioner som du vill koppla en del av eller hela betalningsbeloppet till.
9. När du har granskat en betalningskoppling eller manuellt har kopplat till en eller flera öppna transaktioner väljer du åtgärden **Acceptera koppling**.

Fönstret **Betalningskoppling** stängs och i fönstret **Betalningsavstämningsjournal** ändras värdet i fältet **Matchningssäkerhet** till **Accepterat** för att ange att du har granskat eller manuellt kopplat betalningen.

## <a name="see-also"></a>Se även
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

