---
title: Så här planerar du plockningar i förslaget
description: Lär dig hur rader på leveransdokument kan göras tillgängliga på plockförslag för lagerarbetare.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/13/2021
ms.author: edupont
ms.openlocfilehash: fbb85d69cdd7844bbc63e6367ea962897ab30478
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144313"
---
# <a name="plan-picks-in-worksheets"></a>Planera plockningar i kalkylark

Om distributionslagret kräver både plocknings- och utleveransbearbetning kan du välja att skapa rader i leveransdokument som är tillgängliga på plockningsförslag i stället för plockningsinstruktioner.  

> [!NOTE]  
> Om plockningsinstruktioner för lagret redan har skapats och du vill kombinera dessa för att skapa en enda effektiv plockningsinstruktion, måste du ta bort de enskilda lagerplockningarna. Raderna som ska plockas kan nu visas i listan i plockförslaget.  

På sidan **plockningsförslag** kan du skapa plocklistor som hjälper anställda att samla artiklar i distributionslagret. På sidan visas de tillgängliga kvantiteterna för lagerplatser för direktutleverans, vilket är användbart när du planerar arbetstilldelningar i direktutleveranser. [!INCLUDE[prod_short](includes/prod_short.md)] föreslår alltid en plockning från en lagerplats för direktutleverans först. Raderna i förslaget kan komma från flera källdokument. De kan till exempel komma från fler än en försäljningsorder. 

> [!NOTE]  
> Plockningsartiklar som är monterade för försäljningsorder som levereras, följer samma steg för distributionslager för utleverans. Numret på plockningsrader per antal som ska levereras kan vara många-till-en, eftersom plockning för distributionslager är för monteringskomponenter och inte för monteringsartikeln.  
>
> Distributionslagerplockningsrader skapas för värdet i fältet **Återstående antal** på raderna i monteringsorder som är kopplad till försäljningsorderraden som levereras. Det gör att alla komponenter kan plockas i en åtgärd. Mer information finns i [Så här säljer du lagerartiklar i flöde för montering mot kundorder](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  
>
> Information om hur du plockar komponenter för monteringsorder i allmänhet, inklusive situationer där monteringsartikeln inte ska betalas på en utleverans, se [Plocka för montering eller produktion i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="sorting-lines-on-a-pick-worksheet"></a>Sortera rader på ett plockningsförslag
Du kan sortera rader efter artikel, hyllnummer, källdokument, förfallodatum eller destination. Här följer några exempel på hur sortering kan användas.

* Om du sorterar efter förfallodatum kan du välja att ta bort alla rader utom de allra mest kritiska. Egentligen raderas inte de mindre kritiska raderna, utan skickas bara tillbaka till kalkylarket **Plockningsval**. När du skapar plockningen har raderna redan sorterats efter förfallodatum och du kan välja att tilldela en anställd plockningen.
* Om lagerplatserna är numrerade så att de överensstämmer med distributionslagrets fysiska struktur kan det vara enklare att plocka flera olika leveranser samtidigt när du sorterar rader per lagerplatsnummer. 
* Om du använder lagerplatsordning kan sortering efter rangordning spara tid. 
* Du kan sortera efter mål, så att du kan sätta samman och leverera order per kund.

## <a name="to-plan-picks-in-the-worksheet"></a>Så här planerar du plockningar i kalkylarket

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Plockningskalkylark** och väljer sedan relaterad länk.  
2. Välj åtgärden **Hämta dist.lager dokument**.  
3. Välj de utleveranser som du vill förbereda en plockning för. Du kan sortera raderna, men sorteringen tillämpas inte på plockningsinstruktionen. Du kan också ta bort en del rader för att skapa en effektivare plockning. Om det till exempel finns rader med artiklar på lagerställen för direktutleveranser kanske du vill skapa en plockning för alla rader. Artiklarna för direktutleverans utlevereras, tillsammans med övriga artiklar i utleveransen, och lagerställena för direktutleveranser får därmed plats för fler inkommande artiklar.  
4. Välj åtgärden **Skapa plockning** och fyll i sidan för **Skapa plockning**. De plockningsrader som du skapar ordnas enligt den sortering som du väljer här. Du kan till exempel skapa en plockning för varje zon och sortera raderna efter lagerplatsordning i varje plockning.  
5. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Distributionslagerplockningar** och väljer sedan relaterad länk. Fönstret **Distributionslagerplockningar** öppnas.  
6. Nu kan du visa den plockningsfördelning genom att välja plockningen med det högsta numret.  
7. Om det behövs kan du tilldela en annan användare eller sortera raderna på olika sätt.  
8. Välj åtgärden **Skriv ut** när du vill skriva ut instruktioner.  
9. När du har utfört plockningen, väljer du åtgärden **Registrera**.  

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]