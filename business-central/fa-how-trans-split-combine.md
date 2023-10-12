---
title: Omklassificera anläggningstillgångar
description: Du grupperar om en anläggningstillgång till en annan avdelning om du vill dela och kombinera den med andra anläggningstillgångar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5638, 5636, 5640, 5637'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Överföra, dela eller kombinera anläggningstillgångar

Du kan använda grupperingsjournalen för anläggningstillgångar när du överför, delar upp och slår ihop anläggningstillgångar. Du visar eller skriver ut resultatet av grupperingen av anläggningstillgångar med rapporten **Anl. – bokföringsvärde 02**.

## Om du vill överföra en anläggningstillgång till en annan avdelning

Du kan behöva överföra en anläggningstillgång till en annan avdelning, du till exempel placerar en tillgång i produktionsavdelningen när den är under utveckling och sedan flyttar den till administrationsavdelningen när den är färdig.  

1. Skapa en ny anläggningstillgång. Ange den nya avdelningen som en dimension.  
2. Tilldela en avskrivningsregel för anläggningstillgång till den nya anläggningstillgången. Mer information finns i [Så här anskaffar du anläggningstillgångar](fa-how-acquire.md).
3. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Omklassificeringsjournaler för anläggningstillgång** och väljer sedan relaterad länk.
4. Skapa en journalrad där fältet **Anl.nr.** innehåller den ursprungliga anläggningstillgången och fältet **Nytt anl.nr** innehåller den nya anläggningstillgången som ska flyttas. Fyll i resterande fält om det behövs.  
5. Välj åtgärden **Gruppera**.

    Två rader skapas nu i redovisningsjournalen för anläggningstillgångar med mallen och journalen som du har angett på sidan **Anl. journalinställningar** för den angivna avskrivningsregeln. Mer information finns i [Ställa in avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md).
6. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Redovisningsjournaler för anl.tillg.** och väljer sedan relaterad länk.    
7. På sidan **Anl.tillg. redovisningsjournal** väljer du åtgärden **Bokför** för att bokföra grupperingen som du utförde i steg 4 och 5.

Om du har bokfört en anskaffningskostnad för en tillgång kan du använda grupperingsjournalen för anläggningstillgångar när du vill dela upp anskaffningskostnaden på flera tillgångar.  

## Om du vill dela en anläggningstillgång i tre anläggningstillgångar
Du kan dela upp en anläggningstillgång till åtskilliga anläggningstillgångar, till exempel när du vill fördela en anläggningstillgång till tre olika avdelningar. Du kan till exempel flytta 25 % av anskaffningskostnaden och avskrivningskostnaden för den ursprungliga anläggningstillgången till en andra anläggningstillgång och 45 % till en tredje tillgång. De återstående 30 % kvarstår på den ursprungliga anläggningstillgången.

1. Skapa två nya anläggningstillgången. Ange relevanta avdelningar som dimensioner.  
2. Tilldela en avskrivningsregel för anläggningstillgång till den nya anläggningstillgången. Mer information finns i [Så här anskaffar du anläggningstillgångar](fa-how-acquire.md).
3. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Omklassificeringsjournaler för anläggningstillgång** och väljer sedan relaterad länk.
4. Skapa två grupperingsjournalrader, en för varje ny anläggningstillgång.
5. På den första raden anger du den andra anläggningstillgången i fältet **Nytt anl.nr** och 25 i fältet **Gruppera anskaff.kost. %**.
6. På den andra raden anger du den tredje anläggningstillgången i fältet **Nytt anl.nr** och 40 i fältet **Gruppera anskaff.kost. %**.
7. På båda rader markerar du kryssrutorna **Gruppera anskaff.kost.** och **Gruppera avskrivning**.  
8. Välj åtgärden **Gruppera**.  

    Två rader skapas nu i redovisningsjournalen för anläggningstillgångar med mallen och journalen som du har angett på sidan **Anl. journalinställningar** för den angivna avskrivningsregeln. Mer information finns i [Ställa in avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md).    
9. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Redovisningsjournaler för anl.tillg.** och väljer sedan relaterad länk.
10. På sidan **Anl.tillg. redovisningsjournal** väljer du åtgärden **Bokför** för att bokföra grupperingen som du utförde i steg 4 och 8.

## Om du vill kombinera flera anläggningstillgångar till en

Du kan kombinera flera anläggningstillgångar till en anläggningstillgång, till exempel när du vill flytta distribuerade anläggningstillgångar till en avdelning. Om du har bokfört anskaffningskostnader och avskrivning anläggningstillgång som ska flyttas, kombineras dessa värden i en enda anläggningstillgång.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Omklassificeringsjournaler för anläggningstillgång** och väljer sedan relaterad länk.
2. Skapa en grupperingsjournal där fältet **Anl.nr.** innehåller den anläggningstillgången som ska flyttas/kombineras och fältet **Nytt anl.nr** innehåller den nya anläggningstillgången som ska kombineras med.
3. Lämna fältet **Gruppera anskaff.kost. %** tomt om du vill flytta/kombinera den totala anskaffningskostnaden.  
4. Välj kryssrutorna **Gruppera anskaff.kost.** och **Gruppera avskrivning**.
5. Välj åtgärden **Gruppera**.

    Två rader skapas nu i redovisningsjournalen för anläggningstillgångar med mallen och batchen som du har angett på sidan **Journalinställningar för anläggningstillgångar** för den angivna avskrivningsregeln. Mer information finns i [Ställa in avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md).   
6. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anl.tillg. redovisningsjournaler** och väljer sedan relaterad länk.
7. På sidan **Anl.tillg. redovisningsjournal** väljer du åtgärden **Bokför** för att bokföra grupperingen som du utförde i steg 2 och 5.

## Så här visar du ändrade avskrivningsregelvärden som beror på gruppering av anläggningstillgångar

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokföringsvärde 02 för anläggningstillgång** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs.
3. Välj knappen **Skriv ut** eller **Förhandsgranska**.  

## Se även

[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
