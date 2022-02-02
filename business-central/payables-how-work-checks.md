---
title: Utfärda, Skriv ut, Avbryt och Makulera checkar
description: Beskriver hur du utfärdar checkar med utbetalningsjournalen, skriver ut checkar och annullerar checkar eller granskar checktransaktioner i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.search.form: 256, 404,
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 24e12472ea02f91ff3a0a8d23295865ca2855ca5
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953009"
---
# <a name="make-check-payments"></a>Gör checkbetalningar

Du kan skicka elektroniska och manuella checkar i [!INCLUDE[prod_short](includes/prod_short.md)]. För båda metoder används utbetalningsjournalen för att utfärda checkar till leverantörer. Du kan även makulera checkar och granska checktransaktioner.

I följande procedur beskrivs hur du betalar en leverantör med en datorcheck som kontrolleras genom att koppla betalningen till relevant faktura, skriver ut checken och sedan bokför betalningen som betald. Detta ger positiva leverantörsreskontratransaktioner, som gäller för negativa banktransaktioner och fysiska kontroller för bearbetning i banken.

Du kan betala med två typer av checkar. För båda typerna måste fälten **motkontotyp** eller **kontotyp** innehålla **bankkonto**.

- **Datorcheck** Välj alternativet om du vill att programmet ska upprätta, och senare skriva ut, en check på beloppet på utbetalningsjournalens rad. Du måste skriva ut checkarna, innan du kan bokföra journalraderna.
- **Manuell check** Välj alternativet om du vill skriva en check för hand och vill att programmet ska upprätta en motsvarande checktransaktion för beloppet. Med det här alternativen kan du inte skriva ut checkar.

> [!NOTE]  
> Om du vill vara säker på att banken bara godkänner validerade checkar och belopp kan du skicka en fil som innehåller information om leverantör, check ch betalning. Mer information finns i [Exportera en Positive Pay-fil](finance-how-positive-pay.md).

> [!IMPORTANT]
> Skrivaren måste vara korrekt inställd med checkformulären, och du måste definiera vilken checklayout som ska användas. Mer information finns i [Välj en checklayout](finance-how-define-check-layouts.md). Du kan också skicka checken som en PDF-fil, t. ex.  

Du kan skriva ut upp till 10 fakturor på en sida för en checktalong. Om en check är kopplad till fler än 10 fakturor, när du skriver ut en checktalong annullerar vi checken på den första sidan och skriver ut order ANNULLERAD på checken. Sedan skriver vi ut en påminnelse på fakturorna och det totala checkbeloppet på andra sidan.

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Betala en leverantörsfaktura med datorcheck
Nedan beskrivs hur du betalar en leverantör med check. Stegen liknar återbetalning till en kund med check.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Betalningsjournaler** och väljer sedan relaterad länk.
2. Fyll i utbetalningsjournalraderna. Mer information finns i [Registrera betalningar och återbetalningar](payables-how-post-payments-refunds.md).
3. I fältet **Kod för betalningssätt** väljer du **Check.**
4. I fältet **Bankbetalningstyp** väljer du **Datorcheck.**
5. Välj åtgärden **Skriv ut check**.
6. På sidan **Kontrollera** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Om skrivaren är konfigurerad för utskrift av checkar klickar du på knappen **Skriv ut**. Välj annars knappen **skicka till**, välj alternativet **PDF-dokument**, och välj sedan **OK**-knappen och skriv sedan ut PDF-dokumentet.

    De fysiska checkerna kan numera skickas vidare till leverantörerna för bearbetning. Fortsätt att bokföra betalningen som tillämpas för leverantören och därmed betald i systemet.
8. Välj åtgärden **Bokföra**.

Fullständigt kopplade leverantörsreskontratransaktioner och bankkontotransaktioner skapas.

> [!NOTE]  
> Om du vill skriva ut och betala checkar i flera olika valutor från olika bankkonton måste du köra batch-jobbet **Skriv ut check** separat för varje valuta och ange bankkontot.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Att skriva ut checkar som inte har bokförts
Du kan makulera checkar som inte har bokförts när de har skrivits ut, genom att använda åtgärden **Makulera check** på sidan **Betalningsjournal**.

1. På sidan **Betalningsjournal** väljer du **Makulera check** och sedan väljer du checken som ska annulleras.

## <a name="to-void-checks"></a>Så här makulerar du checkar:

När checkbetalning har bokförts, kan du bara ångra (makulera) checkar från de resulterande banktransaktionerna.

> [!IMPORTANT]
> Om checken tillämpas på en faktura, se då till att först avlägsna tillämpningen av checken så att fakturan kan återbetalas, och gör sedan checken ogiltig. Om checken skrivits ut men inte betalat någon faktura väljer du **Ogiltigförklara endast check** enligt beskrivet i detta avsnitt.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bankkonton** och väljer sedan relaterad länk.
2. Välj det relevanta bankkontot och välj åtgärden **Redigerat** och välj sedan åtgärden **checktransaktioner**.
3. På sidan **checktransaktioner** väljer du åtgärden **Makuler check**.
4. Markera kryssrutan **Makulera endast check**.
5. Välj knappen **OK**.

## <a name="to-view-a-summary-of-posted-checks"></a>Om du vill visa en sammanfattning av bokförda checkar
Om du vill granska bokförda checkar, till exempel för att kontrollera flera kontroller som betalas till en leverantör, kan du använda rapporten **bankkonto – checkinformation**.
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bankkonto - kontrollera detaljer** och väljer sedan relaterad länk.
2. Ställa in filter som relevanta och välj sedan knappen **förhandsgranskning**.

## <a name="see-also"></a>Se även
[Göra betalningar](payables-make-payments.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Exportera en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]