---
title: "Så här avyttrar du och ställer av anläggningstillgångar | Microsoft Docs"
description: "Beskriver hur du säljer och ställer av anläggningstillgångar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 28e4a67ae3df82a2860ced1b971ee41975c8d578
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-dispose-of-or-retire-fixed-assets"></a>Så här avyttrar och ställer av anläggningstillgångar.
När du säljer eller på annat sätt avyttrar en anläggningstillgång, måste avyttringsvärdet bokföras för att beräkna och registrera vinst eller förlust. En avyttringstransaktion måste vara den sista bokförda transaktionen för en anläggningstillgång. För delvis avyttrade anläggningstillgångar kan du bokföra fler än en avyttringstransaktion. Summan av alla bokförda avyttringsbelopp måste vara ett kreditbelopp.  

**Obs!** Om du byter en anläggningstillgång mot en annan måste du registrera både försäljningen av den gamla tillgången (avyttring) och inköpet av den nya (anskaffning). Mer information finns i [Så här skaffar du anläggningstillgångar](fa-how-acquire.md).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Bokföra en avyttringstransaktion i redovisningsjournalen för anläggningstillgångar.
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Redovisningsjournaler för anl.tillg.**, och välj sedan relaterad länk.  
2. Skapa en första journalrad och fyll i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Välj **Anskaffningskostnad** i fältet **Avyttring**.  
4. Välj åtgärden **Infoga anl. motkonto**. En andra journalrad skapas för motkontot som ställs in för bokföring av avyttring.  

    **Obs**: Steg 4 fungerar bara om du har ställt in följande: I fönstret **Anl. bokföringsmallkort** för den fasta anläggningstillgångens bokföringsmall, innehåller fältet **Avyttringskonto** redovisningsdebitkontot och fältet **Avuttringskontosaldo** innehåller det redovisningskonto där du vill bokföra mottransaktioner för uppskrivning. För mer information, se avsnittet "Att ställa in bokföringsmallar för anläggningstillgångar" i [Så här ställer du in allmän information för anläggningstillgångar](fa-how-setup-general.md).  
5. Välj åtgärden **Bokföra**.  

    Om du säljer eller på annat sätt avyttrar en del av en anläggningstillgång måste du dela upp tillgången innan du kan registrera avyttringstransaktionen. För mer information, se [Så här överför, delar eller kombinerar du Anläggningstillgångar](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Så här visar du avyttringstransaktioner
När du säljer eller avyttrar en anläggningstillgång måste avyttringsvärdet bokföras på redovisningskonton där du kan se resultatet.  

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Anläggningstillgångar**, och välj sedan relaterad länk.  
2. Markera den fasta anläggningstillgång som du vill visa poster för välj sedan åtgärden **Avskrivningsregler**.  
3. Markera den avskrivningsregel som du vill visa poster för välj sedan åtgärden **Transaktionsposter**.  
4. Markera en rad med **Avyttring** i fältet **Anl. bokföringskategori** och klicka sedan på åtgärden **Analysera**, .  
5. I fönstret **Analysera** väljer du redovisningstransaktionen och väljer sedan åtgärden **Visa**.  

Fönstret **Redovisningstransaktioner** öppnas där du kan visa de transaktioner som förfogandeinlägget ledde till.  

## <a name="see-also"></a>Se även
[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]] (index.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

