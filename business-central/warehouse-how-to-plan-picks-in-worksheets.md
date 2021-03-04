---
title: Planera plockningar i kalkylarket | Microsoft Docs
description: Om distributionslagret kräver både plocknings- och utleveransbearbetning kan du välja att raderna i utleveransdokument inte automatiskt ska omvandlas till plockningsinstruktioner, utan i stället göras tillgängliga i plockningskalkylarket.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 250d85308e60f93ccba28e2354e47be185918d52
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756148"
---
# <a name="plan-picks-in-worksheets"></a>Planera plockningar i kalkylark

Om distributionslagret kräver både plocknings- och utleveransbearbetning kan du välja att raderna i utleveransdokument inte automatiskt ska omvandlas till plockningsinstruktioner, utan i stället göras tillgängliga i plockningskalkylarket.  

> [!NOTE]  
> Om plockningsinstruktioner för lagret redan har skapats och du vill kombinera dessa för att skapa en enda effektiv plockningsinstruktion, måste du ta bort de enskilda lagerplockningarna. Raderna som ska plockas kan nu visas i listan i kalkylarket.  

I plockningskalkylarket kan du lägga upp plockningslistor för de anställda, vilket minimerar den tid det tar för de anställda att plocka artiklar i lagret. Det finns fält som innehåller information om antalet artiklar som är tillgängliga i lagerställen för direktutleverans. Det är användbart i situationer med lagerställen för direktutleverans, för planering av dina arbetsuppgifter, eftersom programmet ska alltid plocka från en annan lagerplats oavsett enhet. Raderna i kalkylarket kan komma från flera källdokument och kan sorteras efter artikel, hyllnummer, källdokument, förfallodatum eller leveransadress.  

Om du sorterar efter förfallodatum kan du välja att ta bort alla rader i kalkylarket utom de allra mest kritiska. Egentligen raderas inte de mindre kritiska raderna, utan skickas bara tillbaka till kalkylarket **Plockningsval**. När du skapar plockningen har raderna redan sorterats efter förfallodatum och du kan välja att tilldela en viss anställd plockningen.  

> [!NOTE]  
> Plockning för distributionslagerutleverans av artiklar som är monterade till försäljningsorder som har levererats, följer samma steg för distributionslager som vanliga plockning för utleverans, enligt beskrivningen i det här avsnittet. Numret på plockningsrader per antal som ska levereras kan vara många-till-en, eftersom plockning för distributionslager är för monteringskomponenter och inte för monteringsartikeln.  
>
> Distributionslagerplockningsrader skapas för värdet i fältet **Återstående antal** på raderna i monteringsorder som är kopplad till försäljningsorderraden som levereras. Det gör att alla komponenter kan plockas i en åtgärd.  
>
> Mer information finns i ”Hantera artiklar för montering mot kundorder i distributionslagerutleveranser” i Dist.lager utleverans.  
>
> Information om hur du plockar komponenter för monteringsorder i allmänhet, inklusive situationer där monteringsartikeln inte ska betalas på en utleverans, se [Plocka för montering eller produktion i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="to-plan-picks-in-the-worksheet"></a>Så här planerar du plockningar i kalkylarket

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Hämta kalkylark** och välj sedan relaterad länk.  
2. Välj åtgärden **Hämta dist.lager dokument**.  
3. Välj de utleveranser som du vill förbereda en plockning för. Du kan nu sortera raderna i viss mån, men den sortering som du gör här överförs inte till plockningsinstruktionen. Du kan också ta bort en del rader för att skapa en effektivare plockning. Om det till exempel finns rader med artiklar på lagerställen för direktutleveranser kanske du vill skapa en plockning för alla rader som är kopplade till dessa. Artiklarna för direktutleverans utlevereras, tillsammans med övriga artiklar i utleveransen, och lagerställena för direktutleveranser får därmed plats för fler inkommande artiklar.  
4. Välj åtgärden **Skapa plockning** och fyll i sidan för begäran om **Skapa plockning**. De plockningsrader som du skapar ordnas enligt den sortering som du väljer här. Du kan till exempel skapa en plockning för varje zon och sortera raderna efter lagerplatsordning i varje plockning.  
5. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Distributionslagerplockningar** och välj sedan relaterad länk. Fönstret **Distributionslagerplockningar** öppnas.  
6. Nu kan du visa den plockningsfördelning som du just skapade genom att välja plockningen med det högsta numret.  
7. I plockningen kan du fortfarande modifiera det tilldelade användar-ID:t och hur raderna sorteras om det behövs.  
8. Välj åtgärden **Skriv ut** när du vill skriva ut instruktioner.  
9. När du har utfört plockningen, väljer du åtgärden **Registrera**.  

Om lagerställena har numrerats på ett sätt som återspeglar lagrets fysiska struktur kan den lageranställda, för rader som sorterats efter lagerställeskod, enkelt plocka artiklar för flera olika utleveranser på en gång. Den anställda hämtar begärt antal artiklar för respektive utleveransrad från varje lagerplats och placerar dem tillsammans med övriga artiklar för aktuell utleverans. Den lageranställda kan spara mycket tid på att plocka artiklar på samma lagerplats för flera utleveranser samtidigt.  

En annan effektiv sorteringsmetod är lagerplatsordning, som lämpar sig då lagrets fysiska struktur bättre återspeglar lagerställenas ordning än lagerställenas koder.  

I plockningskalkylarket kan du även sortera efter leveransadress, vilket ger dig möjlighet att sammanställa och leverera beställningar till avlägsna kunder först.  

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]