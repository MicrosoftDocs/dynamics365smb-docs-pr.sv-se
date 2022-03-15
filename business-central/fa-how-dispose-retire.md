---
title: Avyttra eller ställa av anläggningstillgångar
description: När du säljer eller på annat sätt avyttrar en anläggningstillgång, måste avyttringsvärdet bokföras för att beräkna och registrera vinst eller förlust.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.search.form: 5628, 5610, 5611, 5629, 5633
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: a24e9ae44f2e342301600ebd5b66d28f66b4d50a
ms.sourcegitcommit: 6d48c1f601ed22b6b0358311baf63c073ab75e64
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/01/2022
ms.locfileid: "8367020"
---
# <a name="dispose-of-or-retire-fixed-assets"></a>Avyttra eller ställa av anläggningstillgångar

När du säljer eller på annat sätt avyttrar en anläggningstillgång, måste avyttringsvärdet bokföras för att beräkna och registrera vinst eller förlust. En avyttringstransaktion måste vara den sista bokförda transaktionen för en anläggningstillgång. För delvis avyttrade anläggningstillgångar kan du bokföra fler än en avyttringstransaktion. Summan av alla bokförda avyttringsbelopp måste vara ett kreditbelopp.  

> [!NOTE]  
> Om du byter en anläggningstillgång mot en annan måste du registrera både försäljningen av den gamla tillgången (avyttring) och inköpet av den nya (anskaffning). Mer information finns i [Så här anskaffar du anläggningstillgångar](fa-how-acquire.md).  

Följande åtgärder förutsätter att du redan har skapat relevanta bokföringsmallar på sidan **Anl.bokföringsmallar**. Mer information finns i [Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Bokföra en avyttringstransaktion i redovisningsjournalen för anläggningstillgångar.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Anl.tillg. redovisningsjournaler** och väljer sedan relaterad länk.  
2. Skapa en första journalrad och fyll i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Välj **Anskaffningskostnad** i fältet **Avyttring**.  
4. Välj åtgärden **Infoga anl. motkonto**. En andra journalrad skapas för motkontot som ställs in för bokföring av avyttring.  

    > [!NOTE]  
    >  Steg 4 fungerar bara om du har ställt in följande: På sidan **Anl.bokföringsmallkort** för den fasta anläggningstillgångens bokföringsmall, innehåller fältet **Avyttringskonto** redovisningsdebitkontot och fältet **Avuttringskontosaldo** innehåller det redovisningskonto där du vill bokföra mottransaktioner för uppskrivning. Mer information finns i [Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Välj åtgärden **Bokföra**.  

Om du säljer eller på annat sätt avyttrar en del av en anläggningstillgång måste du dela upp tillgången innan du kan registrera avyttringstransaktionen. För mer information, se [Så här överför, delar eller kombinerar du anläggningstillgångar](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Så här visar du avyttringstransaktioner
När du säljer eller avyttrar en anläggningstillgång måste avyttringsvärdet bokföras på redovisningskonton där du kan se resultatet.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.  
2. Markera den fasta anläggningstillgång som du vill visa poster för välj sedan åtgärden **Avskrivningsregler**.  
3. Markera den avskrivningsregel som du vill visa poster för välj sedan åtgärden **Transaktionsposter**.  
4. Markera en rad med **Avyttring** i fältet **Anl.bokföringskategori** och klicka sedan på åtgärden **Hitta transaktioner**.  
5. På sidan **Hitta transaktioner** väljer du redovisningstransaktionen och väljer sedan åtgärden **Visa relaterade transaktioner**.  

Sidan **Redovisningstransaktioner** öppnas där du kan visa de transaktioner som förfogandeinlägget ledde till.  

## <a name="see-also"></a>Se även

[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Hitta transaktioner](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]