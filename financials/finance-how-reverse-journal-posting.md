---
title: "Ångra en redovisningsjournal genom att bokföra en mottransaktion | Microsoft Docs"
description: "Om du har bokfört en felaktig bokföring i den allmänna journalen, kan du använda funktionen Återför transaktion för att ångra bokföringen med ett korrekt redovisningsspårning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-reverse-journal-posting"></a>Så här: Återföra en journalbokning
För att kunna återföra (ångra) en felaktig bokföring markerar du posten och skapar en korrigeringspost (transaktioner som är identiska med den ursprungliga transaktionen, men har ett motsatt tecken i beloppsfältet) med samma dokumentnummer och bokföringsdatum som den ursprungliga posten automatiskt. När du har återfört en post måste du skapa en korrekt post.

Du kan endast återföra poster som har bokförts från en redovisningsjournalrad. En transaktion kan endast återföras en gång.

Läs mer om hur du bokför från en redovisningsjournal, [så här: bokföra transaktioner direkt till redovisningsmodulen ](finance-how-post-transactions-directly.md).

Du kan återföra poster från alla fönster **Transaktioner**. Följande procedur baseras fönstret **redovisningstransaktioner**.

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Att återföra bokföringen av en redovisningstransaktion journal
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningstransaktioner** och välj sedan relaterad länk.
2. Markera den transaktion som du vill återföra och välj sedan åtgärden **återföringstransaktion**. Observera att det måste komma från en journalbokföring.
3. I fönstret **Återför transaktionsposter** väljer du önskad post och klickar på åtgärden **Återför**.
4. Välj knappen **Ja** på bekräftelsemeddelandet.

## <a name="see-also"></a>Se även
[Så här bokför du transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

