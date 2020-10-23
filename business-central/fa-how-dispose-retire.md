---
title: Avyttra eller ställa av anläggningstillgångar | Microsoft Docs
description: Vid kassation, försäljning eller avställning av en anläggningstillgång måste du bokföra ett avyttringsvärde.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9a155c5b2f616963da34c4d512bcc0f52623f58b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920728"
---
# <a name="dispose-of-or-retire-fixed-assets"></a>Avyttra eller ställa av anläggningstillgångar

När du säljer eller på annat sätt avyttrar en anläggningstillgång, måste avyttringsvärdet bokföras för att beräkna och registrera vinst eller förlust. En avyttringstransaktion måste vara den sista bokförda transaktionen för en anläggningstillgång. För delvis avyttrade anläggningstillgångar kan du bokföra fler än en avyttringstransaktion. Summan av alla bokförda avyttringsbelopp måste vara ett kreditbelopp.  

> [!NOTE]  
> Om du byter en anläggningstillgång mot en annan måste du registrera både försäljningen av den gamla tillgången (avyttring) och inköpet av den nya (anskaffning). Mer information finns i [Så här anskaffar du anläggningstillgångar](fa-how-acquire.md).  

Följande åtgärder förutsätter att du redan har skapat relevanta bokföringsmallar på sidan **Anl. bokföringsmallar**. Mer information finns i [Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Bokföra en avyttringstransaktion i redovisningsjournalen för anläggningstillgångar.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Redovisningsjournaler för anläggningstillgång** och välj sedan relaterad länk.  
2. Skapa en första journalrad och fyll i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Välj **Anskaffningskostnad** i fältet **Avyttring**.  
4. Välj åtgärden **Infoga anl. motkonto**. En andra journalrad skapas för motkontot som ställs in för bokföring av avyttring.  

    > [!NOTE]  
    >  Steg 4 fungerar bara om du har ställt in följande: På sidan **Anl. bokföringsmallkort** för den fasta anläggningstillgångens bokföringsmall, innehåller fältet **Avyttringskonto** redovisningsdebitkontot och fältet **Avuttringskontosaldo** innehåller det redovisningskonto där du vill bokföra mottransaktioner för uppskrivning. Mer information finns i [Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Välj åtgärden **Bokföra**.  

Om du säljer eller på annat sätt avyttrar en del av en anläggningstillgång måste du dela upp tillgången innan du kan registrera avyttringstransaktionen. För mer information, se [Så här överför, delar eller kombinerar du anläggningstillgångar](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Så här visar du avyttringstransaktioner
När du säljer eller avyttrar en anläggningstillgång måste avyttringsvärdet bokföras på redovisningskonton där du kan se resultatet.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Anläggningstillgångar** och välj sedan relaterad länk.  
2. Markera den fasta anläggningstillgång som du vill visa poster för välj sedan åtgärden **Avskrivningsregler**.  
3. Markera den avskrivningsregel som du vill visa poster för välj sedan åtgärden **Transaktionsposter**.  
4. Markera en rad med **Avyttring** i fältet **Anl. bokföringskategori** och klicka sedan på åtgärden **Hitta transaktioner**.  
5. På sidan **Hitta transaktioner** väljer du redovisningstransaktionen och väljer sedan åtgärden **Visa relaterade transaktioner**.  

Sidan **Redovisningstransaktioner** öppnas där du kan visa de transaktioner som förfogandeinlägget ledde till.  

## <a name="see-also"></a>Se även

[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Ekonomi](finance.md)  
[Komma igång](product-get-started.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Hitta transaktioner](ui-find-entries.md)  
