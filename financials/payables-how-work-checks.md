---
title: "Utfärda, Skriv ut, Avbryt och Makulera checkar | Microsoft Docs"
description: "Beskriver hur du utfärdar checkar med utbetalningsjournalen, skriver ut checkar och annullerar checkar eller granskar checktransaktioner i Finance and Operations, Business edition."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b3f8bece0d0d1de9a6fd17b84df73d466ccdf403
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="work-with-checks"></a>Arbeta med checkar
Du kan skicka elektroniska och manuella checkar i [!INCLUDE[d365fin](includes/d365fin_md.md)]. För båda metoder används utbetalningsjournalen för att utfärda checkar till leverantörer. Du kan även makulera checkar och granska checktransaktioner.

I processen för att utfärda checkar får du förslag på betalningar, transaktioner skapas och datorcheckar skrivs ut.

> [!NOTE]  
>   Om du vill vara säker på att banken bara godkänner validerade checkar och belopp kan du skicka en fil som innehåller information om leverantör, check ch betalning. Mer information finns i [Exportera en Positive Pay-fil](finance-how-positive-pay.md).

Skrivaren måste vara korrekt inställd med checkformulären, och du måste definiera vilken checklayout som ska användas. Mer information finns i [Definiera checklayouter](finance-how-define-check-layouts.md)

## <a name="to-issue-checks"></a>Så här kan du utfärda checkar
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Utbetalningsjournal** och välj sedan relaterad länk.
2. Fyll i journalen med relevanta utbetalningar, till exempel genom att använda funktionen Betalningsförslag för lev. Mer information finns i [Föreslå leverantörsbetalningar](payables-how-suggest-vendor-payments.md).
3. I fältet **bankbetalningstyp** på journalrader för betalning, som du vill att göra med checkar väljer du ett av följande alternativ:

   * **Datorcheck** Välj alternativet om du vill att programmet ska upprätta, och senare skriva ut, en check på beloppet på utbetalningsjournalens rad. Du måste skriva ut checkarna, innan du kan bokföra journalraderna. Du kan bara välja **Datorcheck** eller **Handskriven check** om **Motkontotyp** eller **Kontotyp** är Bankkonto.
   * **Manuell check** Välj alternativet om du vill skriva en check för hand och vill att programmet ska upprätta en motsvarande checktransaktion för beloppet. Med det här alternativen kan du inte skriva ut checkar från [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan bara välja **Manuell check** eller **Handskriven check** om **Motkontotyp** eller **Kontotyp** är Bankkonto.

     > [!NOTE]  
>   Du måste skriva ut datorcheckarna, innan du kan bokföra de relaterade journalraderna.
4. Vid datorcheckar väljer du **Skriv ut check**.
5. I fönstret **Check** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Välj knappen **Skriv ut**.

> [!NOTE]  
>   Om du vill skriva ut checkar i flera olika valutor från olika bankkonton måste du köra batch-jobbet **Skriv ut check** separat för varje valuta och ange bankkontot.

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

## <a name="see-also"></a>Se även
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Exportera en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

