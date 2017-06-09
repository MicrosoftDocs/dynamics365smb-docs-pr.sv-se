---
title: "Så här överför du banktillgångar | Microsoft Docs"
description: "Så här överför du banktillgångar"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 03/32/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e2e3642d08428367fac1dd5845013e14627fe6ed
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-transfer-bank-funds"></a>Så här överför du banktillgångar
Ibland kan du behöva överföra ett belopp från ett bankkonto till ett annat. För att göra detta måste du bokföra en transaktion i redovisningsjournalen. Uppgiften varierar beroende på om bankkontona använder samma valuta eller olika valutor.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Så här bokför du en överföring mellan bankkonton med samma valutakod
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Redovisningsjournal**, och välj sedan relaterad länk.
2. Fyll i fälten **Bokföringsdatum** och **Verifikationsnr** på en . .
3. Ange **Bankkonto** i fältet **Kontotyp**.
4. I fältet **Bankkontonr.** väljer du den bank som du vill överföra pengarna från.
5. Ange det belopp som ska överföras i fältet **Belopp**.
6. I fältet **Motkontotyp** väljer du **Bankkonto**.
7. I fältet **Motkonto** väljer du det bankkonto som du vill överföra pengarna till.
8. Bokför journalen.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Så här bokför du överföringar mellan bankkonton med olika valutakoder
För att överföra pengar mellan bankkonton som använder olika valutor måste du bokföra två redovisningsjournalrader.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Redovisningsjournal**, och välj sedan relaterad länk.
2. Skapa två journalrader och fyll i fälten **Bokföringsdatum** och **Verifikationsnr**. .
3. På den första journalraden anger du **Bankkonto** i fältet **Typ**.
4. I fältet **Bankkontonr.** väljer du det bankkonto som du vill överföra pengarna från.
5. I fältet **Belopp** anger du beloppet i samma valuta som bankontot Ange kreditbelopp med ett minustecken. Ange debetbelopp utan ett minustecken.
6. I fältet **Motkontotyp** väljer du **Bankkonto**.
7. I fältet **Motkonto** väljer du det bankkonto som du vill överföra pengarna till.
8. På den andra journalraden anger du **Bankkonto** i fältet **Typ**.
9. I fältet **Bankkontonr.** väljer du det bankkonto som du vill överföra pengarna till.
10. I fältet **Belopp** anger du beloppet i samma valuta som bankontot Ange kreditbelopp med ett minustecken. Ange debetbelopp utan ett minustecken.
11. I fältet **Motkontotyp** väljer du **Bankkonto**.  
12. I fältet **Motkonto** väljer du det bankkonto som du vill överföra pengarna från.

    **Obs!** Om de valutakurser som används i journalen inte är samma som valutakurserna i fönstret **Valutakurser** skapar du en tredje rad för valutavinsten eller valutaförlusten. Ange **Redovisningskonto** i fältet **Kontotyp**. Ange numret för redovisningskontot för valutavinster och valutaförluster i fältet **Kontonr**. . Ange valutavinsten eller valutaförlusten i fältet **Belopp** med eller utan ett minustecken för respektive kredit och debet.
13. Bokför journalen.

## <a name="see-also"></a>Se även
[Hantera bankkonton](bank-manage-bank-accounts.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

