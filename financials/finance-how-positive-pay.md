---
title: "Så här exporterar du Positive Pay-filer | Microsoft Docs"
description: "Beskriver hur du ser till att banken bara godkänner validerade checkar och belopp genom att exportera Positive Pay-fil som innehåller information om leverantör betalning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 03/24/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ee93f8eb889ae1d635bca22ff133e1523fd1b825
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-export-a-positive-pay-file"></a>Så här exporterar du en Positive Pay-fil
För att se till att banken bara godkänner validerade checkar och belopp kan du exportera en Positive Pay-fil med relevant leverantörsinformation, checknummer och betalningsbelopp som du sedan skickar till banken som referens när du behandlar betalningar.

[!INCLUDE[d365fin](includes/d365fin_md.md)] är förkonfigurerat för att stödja Positive Pay-filer för Bank of America och City Bank.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Så här skapar du ett bankkonto för Positive Pay
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Bankkonton**, och välj sedan relaterad länk.
2. Öppna kortet för den bank du vill använda Positive Pay för.
3. I fältet **Positive Pay exportkod** anger du POSPAYBANK.
4. Stäng fönstret.

## <a name="to-export-a-positive-pay-file"></a>För att exportera en Positive Pay-fil
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Bankkonton**, och välj sedan relaterad länk.
2. Välj det bankkonto som du vill exportera en Positive Pay-fil till.
3. Välj åtgärden **Positive Pay-export**.

    Fönstret **Positive Pay-export** öppnas och visar betalningar som har gjorts för bankkontot efter det sista överföringsdatumet, enligt fälten **senaste överföringsdatum** och **senaste överföringstid**.
4. I fältet **Brytdatum för uppladdning** anger ett datum före vilket betalningar inte inkluderas i den exporterade filen.
5. Välj åtgärden **Exportera**.
6. Klicka på **Spara** i fönstret **Exportera fil** och spara sedan filen till lämplig plats.
7. Överför filen till din elektroniska bank.
8. Skriv ner eller kopiera bekräftelsenumret som du får när filuppladdningen till banken lyckas.

Så här visar du exporterade Positive Pay-poster

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Bankkonton**, och välj sedan relaterad länk.
2. Välj det bankkonto som du vill visa Positive Pay-exportposter för.
3. Välj åtgärden **Positive Pay-transaktioner**.

    I fönstret **Positive Pay-transaktioner** kan du se alla Positive Pay-exportposter för bankkontot.
4. I fältet **bekräftelsenummer** anger du bekräftelsenummer för varje exportpost som du får vid filöverföring till banken.
5. Om du vill visa de relaterade betalningsraderna väljer du åtgärden **Positive Pay-transaktionsinformation**.

Att återexportera Positive Pay-filer

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Bankkonton**, och välj sedan relaterad länk.
2. Välj det bankkonto som du vill återexportera en Positive Pay-fil till.
3. Välj åtgärden **Positive Pay-transaktioner**.
4. Välj den rad för Positive Pay-exportfilen som du vill återexportera.
5. I fönstret **Positive Pay-transaktioner** väljer du åtgärden **Återexportera Positive Pay till fil**.

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Så här arbetar du med redovisningsjournaler](ui-work-general-journals.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

