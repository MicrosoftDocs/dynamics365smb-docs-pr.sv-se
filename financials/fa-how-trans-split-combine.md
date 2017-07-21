---
title: "Gruppera anläggningstillgångar | Microsoft Docs"
description: "Du grupperar om en anläggningstillgång till en annan avdelning om du vill dela och kombinera den med andra anläggningstillgångar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 4e29a08e9b0fd9c20dac12bb32dd1be604ff2dcf
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-transfer-split-or-combine-fixed-assets"></a>SÅ här överför, delar eller kombinerar du anläggningstillgångar.
Du kan använda grupperingsjournalen för anläggningstillgångar när du överför, delar upp och slår ihop anläggningstillgångar. Du visar eller skriver ut resultatet av grupperingen av anläggningstillgångar med rapporten **Anl. - bokföringsvärde 02**.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>Om du vill överföra en anläggningstillgång till en annan avdelning
Du kan behöva överföra en anläggningstillgång till en annan avdelning, du till exempel placerar en tillgång i produktionsavdelningen när den är under utveckling och sedan flyttar den till administrationsavdelningen när den är färdig.  

1. Skapa en ny anläggningstillgång. Ange den nya avdelningen i fältet **Avdelningskod**.
2. Tilldela en avskrivningsregel för anläggningstillgång till den nya anläggningstillgången. Mer information finns i [Så här skaffar du anläggningstillgångar](fa-how-acquire.md).
3. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anl. grupperingsjournaler** och välj sedan relaterad länk.
4. Skapa en grupperingsjournal där fältet **Anl.nr.** innehåller den ursprungliga anläggningstillgången och fältet **Nytt anl.nr.** innehåller den nya anläggningstillgången som ska flyttas.  
5. Välj åtgärden **Gruppera**.

    Två rader skapas nu i redovisningsjournalen för anläggningstillgångar med mallen och journalen som du har angett i fönstret **Anl. journalinställningar** för den angivna avskrivningsregeln. Mer information finns i [Så här ställer du in avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md).
6. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.    
7. I fönstret **Anl.tillg. redovisningsjournal** väljer du åtgärden **Bokför** för att bokföra grupperingen som du utförde i steg 4 och 5.

Om du har bokfört en anskaffningskostnad för en tillgång kan du använda grupperingsjournalen för anläggningstillgångar när du vill dela upp anskaffningskostnaden på flera tillgångar.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>Om du vill dela en anläggningstillgång i tre anläggningstillgångar
Du kan dela upp en anläggningstillgång till åtskilliga anläggningstillgångar, till exempel när du vill fördela en anläggningstillgång till tre olika avdelningar. Du kan till exempel flytta 25 % av anskaffningskostnaden och avskrivningskostnaden för den ursprungliga anläggningstillgången till en andra anläggningstillgång och 45 % till en tredje tillgång. De återstående 30 % kvarstår på den ursprungliga anläggningstillgången.

1. Skapa två nya anläggningstillgången. Ange den nya avdelningen i fältet **Avdelningskod**.
2. Tilldela en avskrivningsregel för anläggningstillgång till den nya anläggningstillgången. Mer information finns i [Så här skaffar du anläggningstillgångar](fa-how-acquire.md).
3. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anl. grupperingsjournaler** och välj sedan relaterad länk.
4. Skapa två grupperingsjournalrader, en för varje ny anläggningstillgång.
5. På den första raden anger du den andra anläggningstillgången i fältet **Nytt anl.nr.** 25 i fältet **Gruppera anskaff.kost. %**.
6. På den andra raden anger du den tredje anläggningstillgången i fältet **Nytt anl.nr.** 40 i fältet **Gruppera anskaff.kost. %**.
7. På båda rader markerar du kryssrutorna **Gruppera anskaff.kost.** och **Gruppera avskrivning**.   
8. Välj åtgärden **Gruppera**.

    Två rader skapas nu i redovisningsjournalen för anläggningstillgångar med mallen och journalen som du har angett i fönstret **Anl. journalinställningar** för den angivna avskrivningsregeln. Mer information finns i [Så här ställer du in avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md).    
9. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.
10. I fönstret **Anl.tillg. redovisningsjournal** väljer du åtgärden **Bokför** för att bokföra grupperingen som du utförde i steg 4 till 8.

## <a name="to-combine-two-fixed-assets-into-one"></a>Om du vill kombinera flera anläggningstillgångar till en
Du kan kombinera flera anläggningstillgångar till en anläggningstillgång, till exempel när du vill flytta distribuerade anläggningstillgångar till en avdelning. Om du har bokfört anskaffningskostnader och avskrivning anläggningstillgång som ska flyttas, kombineras dessa värden i en enda anläggningstillgång.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anl. grupperingsjournaler** och välj sedan relaterad länk.
2. Skapa en grupperingsjournal där fältet **Anl.nr.** innehåller den ursprungliga anläggningstillgången som ska flyttas/kombineras och fältet **Nytt anl.nr.** innehåller den anläggningstillgång som den ska kombineras med.
3. Lämna fältet **Gruppera anskaff.kost. %** tomt om du vill flytta/kombinera den totala anskaffningskostnaden.    
4. Välj kryssrutorna **Gruppera anskaff.kost.** och **Gruppera avskrivning**.
5. Välj **Gruppering**på fliken **Åtgärder**.

    Två rader skapas nu i redovisningsjournalen för anläggningstillgångar med mallen och journalen som du har angett i fönstret **Anl. journalinställningar** för den angivna avskrivningsregeln. Mer information finns i [Så här ställer du in avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md).   
6. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.
7. I fönstret **Anl.tillg. redovisningsjournal** väljer du åtgärden **Bokför** för att bokföra grupperingen som du utförde i steg 2 till 5.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>Så här visar du ändrade avskrivningsregelvärden som beror på gruppering av anläggningstillgångar
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anl.bokföringsvärde 02** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs.
3. Välj knappen **Skriv ut** eller **Förhandsgranska**.  

## <a name="see-also"></a>Se även
[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

