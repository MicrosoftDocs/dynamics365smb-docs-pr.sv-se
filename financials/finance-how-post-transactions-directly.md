---
title: "Registrera kostnader eller intäkter direkt i redovisningen | Microsoft Docs"
description: "Du kan skapa relaterade transaktioner genom att bokföra journalrader i fönstret redovisningsjournal för verksamhet som inte representeras av ett dokument, till exempel mindre utgifter eller inbetalningar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7fa0d6b604a60e000208287546d831690a914931
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-post-transactions-directly-to-the-general-ledger"></a>Så här bokför du transaktioner direkt i redovisningen
De flesta finansiella transaktioner bokförs i redovisningen genom särskilda dokument, till exempel inköpsfakturor och försäljningsorder. För verksamhet som inte representeras av ett dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], till exempel mindre utgifter eller inbetalningar kan du skapa relaterade transaktioner genom att bokföra journalrader i fönstret **redovisningsjournal**.

Redovisningsjournaler bokför ekonomiska transaktioner direkt till redovisningskonton och andra konton, till exempel bank-, kund-, leverantörskonton. När du bokför med en redovisningsjournal skapas alltid transaktioner på redovisningskonton. Så sker till exempel även när en journalrad bokförs på ett kundkonto, eftersom en transaktion bokförs på ett kundfordringskonto i redovisningen via en bokföringsmall. Du kan anpassa din version av en redovisningsjournal genom att ställ ain en journal eller mall. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).

Till skillnad från transaktioner som har bokförts med dokument som kräver en kreditnotaprocess, kan du korrekt återföra transaktioner som har bokförts med den allmänna journalen. Mer information finns i [Så hör: Återföra journalbokningar](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Bokföra transaktioner direkt i redovisningen
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler** och välj sedan relaterad länk.
2. Öppna relevant buntnamn för redovisningsjournalen. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).
3. Fyll i fälten på en ny journalrad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Upprepa steg 3 för alla enskilda transaktioner som du vill tilldela bokföra.

    > [!TIP]  
    > Om du vill ange flera transaktionsrader ovanför en rad i motkontot, till exempel för ett bankkonto markerar du kryssrutan **föreslå saldobelopp** på raden för journalen i fönstret **redovisningsjournaler**. Fältet **belopp** på motkontots rad är fördefinierade automatiskt med det värde som krävs för att balansera transaktionerna.
5. Välj åtgärden **Bokför** för att registrera transaktioner på de angivna redovisningskontona.

## <a name="see-also"></a>Se även
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Så här: Återföra en journalbokning](finance-how-reverse-journal-posting.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

