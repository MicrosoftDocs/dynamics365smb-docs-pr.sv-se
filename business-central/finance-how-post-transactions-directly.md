---
title: Registrera kostnader eller intäkter direkt i redovisningen
description: Du kan skapa transaktioner på sidan Redovisningsjournal för affärsaktiviteter som inte omfattar ett dokument.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'direct posting, general ledger'
ms.search.form: '39, 251'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Bokföra transaktioner direkt i redovisningen

Du använder Redovisningsjournaler för att bokföra ekonomiska transaktioner direkt på redovisningskonton och andra konton, till exempel bank-, leverantörs- och personalkonton.  

En typisk användning av den redovisningsjournal är att bokföra anställdas utgifter under affärsverksamhet för ersättning. Mer information finns i [Så här registrerar du och återbetalar personalens utgifter](finance-how-record-reimburse-employee-expenses.md).

Redovisningsjournaler bokför ekonomiska transaktioner direkt till redovisningskonton och andra konton, till exempel bank-, leverantörs- och anställdas konton. När du bokför med en redovisningsjournal skapas transaktioner på redovisningskonton. Transaktioner skapas även när en journalrad bokförs på ett kundkonto, eftersom en transaktion bokförs på ett kundfordringskonto i redovisningen via en bokföringsmall. Du kan anpassa din version av en redovisningsjournal genom att ställ ain en journal eller mall. Mer information finns i [Arbeta med Skapa redovisningsjournaler](ui-work-general-journals.md).

Transaktioner som du bokför med dokument kräver en kreditnotaprocess. Du kan emellertid återföra transaktioner som du bokför med redovisningsjournalen. Mer information finns i [Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md).

## Bokföra transaktioner direkt i redovisningen

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **redovisningsjournaler** och väljer sedan relaterad länk.
2. Öppna redovisningsjournalen. Mer information finns i [Arbeta med Skapa redovisningsjournaler](ui-work-general-journals.md).
3. Fyll i fälten på en ny journalrad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Upprepa steg 3 för alla transaktioner som du vill tilldela bokföra.

    > [!TIP]  
    > Om du vill ange flera transaktionsrader ovanför en rad i motkontot, till exempel för ett bankkonto markerar du kryssrutan **föreslå saldobelopp** på raden för journalen på sidan **redovisningsjournaler**. Fältet **belopp** på motkontots rad är fördefinierade automatiskt med det värde som krävs för att balansera transaktionerna.
5. Välj åtgärden **Bokför** för att registrera transaktioner på de angivna redovisningskontona.

## Se även

[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Skapa och återbetala de anställdas utgifter](finance-how-record-reimburse-employee-expenses.md)  
[Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]