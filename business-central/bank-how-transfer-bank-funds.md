---
title: Överföra banktillgångar | Microsoft Docs
description: Du kan överföra belopp från ett bankkonto, till exempel olika valutor genom att bokföra transaktionen i redovisningsjournalen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 934124d419e19c1dc8180f11fcae748cd2afd15d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752361"
---
# <a name="transfer-bank-funds"></a>Överföra banktillgångar
Du kan ibland komma att behöva överföra ett belopp från ett bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] till ett annat. För att göra detta måste du bokföra en transaktion på sidan **Redovisningsjournal**. Uppgiften varierar beroende på om bankkontona använder samma valuta eller olika valutor.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Så här bokför du en överföring mellan bankkonton med samma valutakod
1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournal** och välj sedan relaterad länk.
2. Fyll i fälten **Bokföringsdatum** och **Verifikationsnr** på en .
3. Ange **Bankkonto** i fältet **Kontotyp**.
4. I fältet **Kontonr** väljer du det bankkonto som du vill överföra pengarna från.
5. Ange det belopp som ska överföras i fältet **Belopp**.
6. Välj åtgärden **visa fler kolumner** för att se alla tillgängliga fält.
7. I fältet **Motkontotyp** väljer du **Bankkonto**.
8. I fältet **Balanskontonr** väljer du det bankkonto som du vill överföra pengarna till.
9. Bokför journalen.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Så här bokför du överföringar mellan bankkonton med olika valutakoder
För att överföra pengar mellan bankkonton som använder olika valutor måste du bokföra två redovisningsjournalrader.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournal** och välj sedan relaterad länk.
2. Skapa två journalrader och fyll i fälten **Bokföringsdatum** och **Verifikationsnr**.
3. På den första journalraden anger du **Bankkonto** i fältet **Typ**.
4. I fältet **Kontonr** väljer du det bankkonto som du vill överföra pengarna från.
5. I fältet **Belopp** anger du beloppet i samma valuta som bankontot. Ange kreditbelopp med ett minustecken. Ange debetbelopp utan ett minustecken.
6. I fältet **Motkontotyp** väljer du **Bankkonto**.
7. I fältet **Balanskontonr** väljer du det bankkonto som du vill överföra pengarna till.
8. På den andra journalraden anger du **Bankkonto** i fältet **Typ**.
9. I fältet **Kontonr** väljer du det bankkonto som du vill överföra pengarna till.
10. I fältet **Belopp** anger du beloppet i samma valuta som bankontot. Ange kreditbelopp med ett minustecken. Ange debetbelopp utan ett minustecken.
11. I fältet **Motkontotyp** väljer du **Bankkonto**.  
12. I fältet **Balanskontonr** väljer du det bankkonto som du vill överföra pengarna från.

    > [!NOTE]  
    > Om de valutakurser som används i journalen inte är samma som valutakurserna på sidan **Valutakurser** skapar du en tredje rad för valutavinsten eller valutaförlusten. Ange **Redovisningskonto** i fältet **Kontotyp**. Ange numret för redovisningskontot för valutavinster och valutaförluster i fältet **Kontonr**. Ange valutavinsten eller valutaförlusten i fältet **Belopp** med eller utan ett minustecken för respektive kredit och debet.
13. Bokför journalen.

## <a name="see-also"></a>Se även
[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
