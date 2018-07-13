---
title: "Utfärda, Skriv ut, Avbryt och Makulera checkar | Microsoft Docs"
description: "Beskriver hur du utfärdar checkar med utbetalningsjournalen, skriver ut checkar och annullerar checkar eller granskar checktransaktioner i Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: bcd0e21bc40b63c99f37618ae3406395b3c31b10
ms.contentlocale: sv-se
ms.lasthandoff: 06/11/2018

---
# <a name="make-check-payments"></a>Gör checkbetalningar
Du kan skicka elektroniska och manuella checkar i [!INCLUDE[d365fin](includes/d365fin_md.md)]. För båda metoder används utbetalningsjournalen för att utfärda checkar till leverantörer. Du kan även makulera checkar och granska checktransaktioner.

I följande procedur beskrivs hur du betalar en leverantör med en datorcheck som kontrolleras genom att koppla betalningen till relevant faktura, skriver ut checken och sedan bokför betalningen som betald. Detta ger positiva leverantörsreskontratransaktioner, som gäller för negativa banktransaktioner och fysiska kontroller för bearbetning i banken.

Du kan betala med två typer av checkar. För båda typerna måste fälten **motkontotyp** eller **kontotyp** innehålla **bankkonto**.

- **Datorcheck** Välj alternativet om du vill att programmet ska upprätta, och senare skriva ut, en check på beloppet på utbetalningsjournalens rad. Du måste skriva ut checkarna, innan du kan bokföra journalraderna. Du kan bara välja **Datorcheck** om
- **Manuell check** Välj alternativet om du vill skriva en check för hand och vill att programmet ska upprätta en motsvarande checktransaktion för beloppet. Med det här alternativen kan du inte skriva ut checkar.

> [!NOTE]  
> Om du vill vara säker på att banken bara godkänner validerade checkar och belopp kan du skicka en fil som innehåller information om leverantör, check ch betalning. Mer information finns i [Exportera en Positive Pay-fil](finance-how-positive-pay.md).

Skrivaren måste vara korrekt inställd med checkformulären, och du måste definiera vilken checklayout som ska användas. Mer information finns i [Definiera checklayouter](finance-how-define-check-layouts.md)

Du kan skriva ut upp till 10 fakturor på en sida för en checktalong. Om en check är kopplad till fler än 10 fakturor, när du skriver ut en checktalong annullerar vi checken på den första sidan och skriver ut order ANNULLERAD på checken. Sedan skriver vi ut en påminnelse på fakturorna och det totala checkbeloppet på andra sidan. 

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Betala en leverantörsfaktura med datorcheck
Nedan beskrivs hur du betalar en leverantör med check. Stegen liknar återbetalning till en kund med check.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Utbetalningsjournal** och välj sedan relaterad länk.
2. Fyll i utbetalningsjournalraderna. Mer information finns i [Registrera betalningar och återbetalningar](payables-how-post-payments-refunds.md).
3. I fältet **Kod för betalningssätt** väljer du **Check.**
4. I fältet **Bankbetalningstyp** väljer du **Datorcheck.**
5. Välj åtgärden **Skriv ut check**.
6. I fönstret **Check** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Välj knappen **skicka till**, välj alternativet **PDF-dokument**, och välj sedan **OK**-knappen.

    Numera du kan föra fysiska checkar till banken för bearbetning. Fortsätt att bokföra betalningen som tillämpas för leverantören och därmed betald i systemet.
8. Välj åtgärden **Bokföra**.

Fullständigt kopplade leverantörsreskontratransaktioner och bankkontotransaktioner skapas.

> [!NOTE]  
> Om du vill skriva ut och betala checkar i flera olika valutor från olika bankkonton måste du köra batch-jobbet **Skriv ut check** separat för varje valuta och ange bankkontot.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Att skriva ut checkar som inte har bokförts
Du kan makulera checkar som inte har bokförts när de har skrivits ut, genom att använda åtgärden **Makulera check** i fönstret **Betalningsjournal**.

1. I fönstret **Betalningsjournal** väljer du **Makulera check** och sedan väljer du checken som ska annulleras.

## <a name="to-void-checks"></a>Så här makulerar du checkar:
När checkbetalning har bokförts, kan du bara ångra (makulera) checkar från de resulterande banktransaktionerna.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.
2. Välj det relevanta bankkontot och välj åtgärden **Redigerat** och välj sedan åtgärden **checktransaktioner**.
3. I fönstret **checktransaktioner** väljer du åtgärden **Makuler check**.
4. Markera kryssrutan **Makulera endast check**.
5. Välj knappen **OK**.

## <a name="to-view-a-summary-of-posted-checks"></a>Om du vill visa en sammanfattning av bokförda checkar
Om du vill granska bokförda checkar, till exempel för att kontrollera flera kontroller som betalas till en leverantör, kan du använda rapporten **bankkonto - checkinformation**.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkontoavstämningar - Checkinformation** och välj sedan relaterad länk.
2. Ställa in filter som relevanta och välj sedan knappen **förhandsgranskning**.

## <a name="see-also"></a>Se även
[Göra betalningar](payables-make-payments.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Exportera en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

