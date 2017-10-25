---
title: "Planera plockningar i förslaget | Microsoft Docs"
description: "Om distributionslagret kräver både plocknings- och utleveransbearbetning kan du välja att raderna i utleveransdokument inte automatiskt ska omvandlas till plockningsinstruktioner, utan i stället göras tillgängliga i plockningsförslaget."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: cb9a8366dbce67f7fdf3f32d55d7c5a289b9db4e
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-plan-picks-in-worksheets"></a>Så här planerar du plockningar i förslaget
Om distributionslagret kräver både plocknings- och utleveransbearbetning kan du välja att raderna i utleveransdokument inte automatiskt ska omvandlas till plockningsinstruktioner, utan i stället göras tillgängliga i plockningsförslaget.  

> [!NOTE]  
>  Om plockningsinstruktioner för lagret redan har skapats och du vill kombinera dessa för att skapa en enda effektiv plockningsinstruktion, måste du ta bort de enskilda lagerplockningarna. Raderna som ska plockas kan nu visas i listan i förslaget.  

I plockningsförslaget kan du lägga upp plockningslistor för de anställda, vilket minimerar den tid det tar för de anställda att plocka artiklar i lagret. Det finns fält som innehåller information om antalet artiklar som är tillgängliga i lagerplatser för direktutleverans. Det är användbart i situationer med lagerplatser för direktutleverans, för planering av dina arbetsuppgifter, eftersom programmet ska alltid plocka från en annan lagerplats oavsett enhet. Raderna i förslaget kan komma från flera källdokument och kan sorteras efter artikel, hyllnummer, källdokument, förfallodatum eller leveransadress.  

Om du sorterar efter förfallodatum kan du välja att ta bort alla rader i förslaget utom de allra mest kritiska. Egentligen raderas inte de mindre kritiska raderna, utan skickas bara tillbaka till förslaget **Plockningsval**. När du skapar plockningen har raderna redan sorterats efter förfallodatum och du kan välja att tilldela en viss anställd plockningen.  

> [!NOTE]  
>  Plockning för distributionslagerutleverans av artiklar som är monterade till försäljningsorder som har levererats, följer samma steg för distributionslager som vanliga plockning för utleverans, enligt beskrivningen i det här avsnittet. Numret på plockningsrader per antal som ska levereras kan vara många-till-en, eftersom plockning för distributionslager är för monteringskomponenter och inte för monteringsartikeln.  
>   
>  Distributionslagerplockningsrader skapas för värdet i fältet **Återstående antal** på raderna i monteringsorder som är kopplad till försäljningsorderraden som levereras. Det gör att alla komponenter kan plockas i en åtgärd.  
>   
>  Mer information finns i ”Hantera artiklar för montering mot kundorder i distributionslagerutleveranser” i Dist.lager utleverans.  
>   
>  Information om hur du plockar komponenter för monteringsorder, inklusive lagerställen, där monteringsartikeln inte ska betalas på en utleverans, se [så här: Plocka för montering eller produktion i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="to-plan-picks-in-the-worksheet"></a>Så här planerar du plockningar i förslaget  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Plockningsförslag**, och välj sedan relaterad länk.  
2.  Välj åtgärden **Hämta dist.lager dokument**.  
3.  Välj de utleveranser som du vill förbereda en plockning för. Du kan nu sortera raderna i viss mån, men den sortering som du gör här överförs inte till plockningsinstruktionen. Du kan också ta bort en del rader för att skapa en effektivare plockning. Om det till exempel finns rader med artiklar på lagerplatser för direktutleveranser kanske du vill skapa en plockning för alla rader som är kopplade till dessa. Artiklarna för direktutleverans utlevereras, tillsammans med övriga artiklar i utleveransen, och lagerplatserna för direktutleveranser får därmed plats för fler inkommande artiklar.  
4.  Välj åtgärden **Skapa plockning** och fyll i fönstret för begäran om **Skapa plockning**. De plockningsrader som du skapar ordnas enligt den sortering som du väljer här. Du kan till exempel skapa en plockning för varje zon och sortera raderna efter lagerplatsordning i varje plockning.  
5.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Plockningar**, och välj sedan relaterad länk. Fönstret **Plockningar** öppnas.  
6.  Nu kan du visa den plockningstilldelning som du just skapade genom att välja plockningen med det högsta numret.  
7.  I plockningen kan du fortfarande modifiera det tilldelade användar-ID:t och hur raderna sorteras om det behövs.  
8.  Välj åtgärden **Skriv ut** när du vill skriva ut instruktioner.  
9. När du har utfört plockningen, väljer du åtgärden **Registrera**.  

Om lagerplatserna har numrerats på ett sätt som återspeglar lagrets fysiska struktur kan den lageranställda, för rader som sorterats efter lagerplatskod, enkelt plocka artiklar för flera olika utleveranser på en gång. Den anställda hämtar begärt antal artiklar för respektive utleveransrad från varje lagerplats och placerar dem tillsammans med övriga artiklar för aktuell utleverans. Den lageranställda kan spara mycket tid på att plocka artiklar på samma lagerplats för flera utleveranser samtidigt.  

En annan effektiv sorteringsmetod är lagerplatsordning, som lämpar sig då lagrets fysiska struktur bättre återspeglar lagerplatsernas ordning än lagerplatsernas koder.  

I plockningsförslaget kan du även sortera efter leveransadress, vilket ger dig möjlighet att sammanställa och leverera beställningar till avlägsna kunder först.  

## <a name="see-also"></a>Se även
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

