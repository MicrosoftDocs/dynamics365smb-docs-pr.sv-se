---
title: Exportera du Positive Pay-filer | Microsoft Docs
description: "Du kan se till att banken bara godkänner validerade checkar och belopp genom att exportera Positive Pay-fil som innehåller information om leverantör betalning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 57580354c2ea5b63162e1539cf2f97eb9770c50b
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="export-a-positive-pay-file"></a>Exportera en Positive Pay-fil
För att se till att banken bara godkänner validerade checkar och belopp kan du exportera en Positive Pay-fil med relevant leverantörsinformation, checknummer och betalningsbelopp som du sedan skickar till banken som referens när du behandlar betalningar.

[!INCLUDE[d365fin](includes/d365fin_md.md)]  är förkonfigurerat för att stödja Positive Pay-filer för Bank of America och City Bank.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Så här skapar du ett bankkonto för Positive Pay
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.
2. Öppna kortet för den bank du vill använda Positive Pay för.
3. I fältet **Positive Pay exportkod** anger du POSPAYBANK.
4. Stäng fönstret.

## <a name="to-export-a-positive-pay-file"></a>För att exportera en Positive Pay-fil
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.
2. Välj det bankkonto som du vill exportera en Positive Pay-fil till.
3. Välj åtgärden **Positive Pay-export**.

    Fönstret **Positive Pay-export** öppnas och visar betalningar som har gjorts för bankkontot efter det sista överföringsdatumet, enligt fälten **senaste överföringsdatum** och **senaste överföringstid**.
4. I fältet **Brytdatum för uppladdning** anger ett datum före vilket betalningar inte inkluderas i den exporterade filen.
5. Välj åtgärden **Exportera**.
6. Klicka på **Spara** i fönstret **Exportera fil** och spara sedan filen till lämplig plats.
7. Överför filen till din elektroniska bank.
8. Skriv ner eller kopiera bekräftelsenumret som du får när filuppladdningen till banken lyckas.

Så här visar du exporterade Positive Pay-poster

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.
2. Välj det bankkonto som du vill visa Positive Pay-exportposter för.
3. Välj åtgärden **Positive Pay-transaktioner**.

    I fönstret **Positive Pay-transaktioner** kan du se alla Positive Pay-exportposter för bankkontot.
4. I fältet **bekräftelsenummer** anger du bekräftelsenummer för varje exportpost som du får vid filöverföring till banken.
5. Om du vill visa de relaterade betalningsraderna väljer du åtgärden **Positive Pay-transaktionsinformation**.

Att återexportera Positive Pay-filer

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.
2. Välj det bankkonto som du vill återexportera en Positive Pay-fil till.
3. Välj åtgärden **Positive Pay-transaktioner**.
4. Välj den rad för Positive Pay-exportfilen som du vill återexportera.
5. I fönstret **Positive Pay-transaktioner** väljer du åtgärden **Återexportera Positive Pay till fil**.

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

