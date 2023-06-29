---
title: Registrera kostnader eller intäkter direkt i redovisningen
description: Du kan skapa relaterade transaktioner genom att bokföra journalrader på sidan redovisningsjournal för verksamhet som inte representeras av ett dokument.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'direct posting, general ledger'
ms.search.form: '39, 251'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="post-transactions-directly-to-the-general-ledger"></a><a name="post-transactions-directly-to-the-general-ledger"></a>Så här bokför du transaktioner direkt i redovisningen

Du använder Redovisningsjournaler för att bokföra ekonomiska transaktioner direkt på redovisningskonton och andra konton, till exempel bank-, leverantörs- och personalkonton.  

En vanlig användning av redovisningsjournalen är att publicera anställdas utgifter med egna pengar under affärsaktiviteter för senare återbetalning. Mer information finns i [Så här registrerar du och återbetalar personalens utgifter](finance-how-record-reimburse-employee-expenses.md).

Redovisningsjournaler bokför ekonomiska transaktioner direkt till redovisningskonton och andra konton, till exempel bank-, leverantörs- och anställdas konton. När du bokför med en redovisningsjournal skapas alltid transaktioner på redovisningskonton. Så sker till exempel även när en journalrad bokförs på ett kundkonto, eftersom en transaktion bokförs på ett kundfordringskonto i redovisningen via en bokföringsmall. Du kan anpassa din version av en redovisningsjournal genom att ställ ain en journal eller mall. Mer information finns i [Arbeta med redovisningsjournaler](ui-work-general-journals.md).

Till skillnad från transaktioner som har bokförts med dokument som kräver en kreditnotaprocess, kan du korrekt återföra transaktioner som har bokförts med den allmänna journalen. Mer information finns i [återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Bokföra transaktioner direkt i redovisningen

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **redovisningsjournaler** och väljer sedan relaterad länk.
2. Öppna relevant redovisningsjournal. Mer information finns i [Arbeta med redovisningsjournaler](ui-work-general-journals.md).
3. Fyll i fälten på en ny journalrad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Upprepa steg 3 för alla enskilda transaktioner som du vill tilldela bokföra.

    > [!TIP]  
    > Om du vill ange flera transaktionsrader ovanför en rad i motkontot, till exempel för ett bankkonto markerar du kryssrutan **föreslå saldobelopp** på raden för journalen på sidan **redovisningsjournaler**. Fältet **belopp** på motkontots rad är fördefinierade automatiskt med det värde som krävs för att balansera transaktionerna.
5. Välj åtgärden **Bokför** för att registrera transaktioner på de angivna redovisningskontona.

## <a name="see-also"></a><a name="see-also"></a>Se även

[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Skapa och återbetala de anställdas utgifter](finance-how-record-reimburse-employee-expenses.md)  
[Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
