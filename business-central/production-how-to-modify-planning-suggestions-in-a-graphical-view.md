---
title: Så här kan du ändra planeringsförslag i en grafisk översikt över serviceverksamheten | Microsoft Docs
description: En vanlig planeringsaktivitet är att ändra eller lägga till planeringsförslagsrader för att ändra de föreslagna leveransordrarna innan du utför dem genom att köra funktionen **Verkställ åtgärdsmeddelande**. Ett alternativ för att göra det i planeringsförslaget är att använda en grafisk översikt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 30de3d3243b0b6babff94efc33d87e7494d2e2bd
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2019
ms.locfileid: "939253"
---
# <a name="modify-planning-suggestions-in-a-graphical-view"></a>Ändra planeringsförslag i en grafisk vy
En vanlig planeringsaktivitet är att ändra eller lägga till planeringsförslagsrader för att ändra de föreslagna leveransordrarna innan du utför dem genom att köra funktionen **Verkställ åtgärdsmeddelande**. Ett alternativ för att göra det i planeringsförslaget är att använda en grafisk översikt.

På sidan **Artikeldisposition per tidslinje** kan du ändra vissa leveransorder och förslag genom att dra element längs x-axeln för att ändra antalet eller längs y-axeln för att ändra förfallodatumet.  

 På sidan **Artikeldisposition per tidslinje** och den **planeringsförslag** kan du göra följande ändringar:  

-   Ändra en de föreslagna leveransordrarna som endast finns som en planeringsrad.  
-   Ändra en befintlig leveransorder som planeringssystemet föreslår ska ändras.  
-   Skapa en ny föreslagen leveransorder och ändra den.  

För mer information om de olika typerna av planeringsrader som visas, se fältet Beskrivning på snabbfliken **Händelseändringar**.  

När du väljer **Spara ändringar** på sidan **Artikeldisposition per tidslinje** kopieras ändringarna som du har gjort till planering eller inköpskalkylarket. Nu kan du använda dem med hjälp av funktionen **Skapa order från planering**.  

I följande procedur beskrivs hur du ändrar leveransförslag genom att dra och släppa. Som alternativ kan du ändra fälten **Förfallodatum** och **Antal** på snabbfliken **Händelseändringar** och se mötesändringarna grafiskt direkt på snabbfliken **Tidslinje** på sidan **Planeringsförslag**.  

## <a name="to-modify-suggested-supply-orders-in-the-graphical-view"></a>Om du vill ändra de föreslagna leveransordrarna i den grafiska översikten  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artikeldisposition per tidslinje** och välj sedan relaterad länk.  

    Sidan **Artikeldisposition per tidslinje** öppnas med artikelnummer, lagerstället och varianten av artikeln på den aktuella planeringsraden förifyllda i fälten på snabbfliken **Alternativ**. Snabbfliken **Tidslinje** visar en grafisk återgivning av artikelns planerade lager, inklusive planeringsförslag.  

2.  Se till att fältet **Ta med planeringsförslag** är markerat.  
3.  Hitta leveransorderkalkylarket som du vill ändra. Du kan identifiera modifierbara element med den gröna cirkeln och diskikonen. Mer information om de olika symbolerna finns i [Symboler och ikoner på snabbfliken Tidslinje](production-how-to-modify-planning-suggestions-in-a-graphical-view.md#symbols-and-icons-on-the-timeline-fasttab).  
4.  Markera pekaren över den gröna cirkeln tills den förstoras och pekaren ändras till flyttform (fyra pilar).  
5.  Tryck på och håll ned musknappen samtidigt som du drar du pekaren uppåt eller nedåt för att ändra antal. Tryck på och håll ned musknappen samtidigt som du drar du pekaren till vänster eller höger för att ändra förfallodatum.  
6.  Förutom att flytta element genom att dra och släppa kan du ändra planeringsförslag genom att använda funktionerna i den nedrullningsbara menyn. Gå till den nedrullningsbara menyn på den gröna cirkeln i ett föreslaget leveranselement och välja en av följande funktioner  

    |Funktion|Beskrivning|  
    |--------------|---------------------------------------|  
    |**Skapa ny leverans**|Skapa ett nytt element på punkten där du går till nedrullningsbara menyn som representerar en ny föreslagen leveransorder. Det blir en ny rad i planeringsförslaget, när du väljer **Spara ändringar**.<br /><br /> **OBS!** Om fälten **Lagerställefilter** eller **Variantfilter** på snabbfliken **Alternativ** är tomma, eller har fler än en filtervärde, skapas den nya tillgången, och senare sparas till planering eller inköpskalkylarket med följande koder:<br /><br /> * Om fältet är tomt kommer den nya tillgången skapas utan lagerställe eller en variantkod.<br /><br /> * Om fler än en filtervärde definieras, skapas den nya tillgången för den första filtervärdet enligt sorteringsmetoden.<br /><br /> Om du vill ha en annan variant eller lagerställekod, måste du ändra numret manuellt på den nya planeringsraden.|  
    |**Autojustera tillgång**|Optimerar en ny efterfrågan som du har skapat i diagrammet genom att kontrollera att den resulterar i noll i lagret före nästa leverans.|  
    |**Ta bort tillgång**|Ta bort element i Snabbfliken **Tidslinje** och tar bort planeringsraden, när du väljer **Spara ändringar**. Ikonen ändras till en diskenhet med ett rött kors när leveransen har tagits bort.<br /><br /> **OBS!:** Du kan endast ta bort en leverans av åtgärdsmeddelandetypen **Ny**. När du har valt **Spara ändringar** måste du manuellt ta bort den aktuella planeringsraden i planeringen eller inköpskalkylarket.|  

7.  Välj åtgärden **Läs in på nytt** om du vill återställa alla ändringar som du har gjort, när du öppnade den sista sidan **Artikeldisposition per tidslinje** eller **Läs in på nytt**.  
8. Välj **Spara ändringar** för att kopiera ändrat antal och datumändringar i planeringen eller rekvisitionsraderna när elementen placeras där du vill ha dem i diagrammet, som motsvarar de grafiska elementen.  

För att verkställa planändringar för leverans måste du följa de resulterande åtgärdsmeddelandena från planering eller inköpskalkylarket. Mer information finns i Skapa order från planering.

## <a name="symbols-and-icons-on-the-timeline-fasttab"></a>Symboler och ikoner på snabbfliken Tidslinje
 |Symbol/ikon|Beskrivning|  
 |------------------|---------------------------------------|  
 |Svart kors|Order (både efterfrågan och tillgång).<br /><br /> -   Kan inte ändras.<br />-   Visas när fältet **Visa planerat lagersaldo** markerats (orange diagram).|  
 |Röd cirkel|Befintliga leveransordrar som inte finns i planeringsförslag.<br /><br /> -   Kan inte ändras.<br />-   Visas när fältet **Visa planerat lagersaldo** markerats (orange diagram).|  
 |Gul stjärna|Prognostiserat behov.<br /><br /> -   Kan inte ändras.<br />-   Visas när fältet **Prognosnamn** har ett värde.<br /><br /> När både fältet **Visa planerat lagersaldo** och **Ta med planeringsförslag** markeras får varje gul stjärna en länkad motsvarighet i motsatt diagram. Detta visar hur en föreslagen leverans uppfyller prognostiserat behov.|  
 |Grön cirkel med en ikon formad som en skiva som har ett rött kors|Föreslagen leveransorder med åtgärdsmeddelandet *Avbryt*.<br /><br /> -   Kan inte ändras.<br />-   Visas när fältet **Ta med planeringsförslag** markeras (grönt diagram).|  
 |Grön cirkel med en ikon formad som en skiva med en stjärna|Föreslagna leveransordrar med åtgärdsmeddelandet *Nytt*.<br /><br /> -   Kan ändras.<br />-   Visas när fältet **Ta med planeringsförslag** markeras (grönt diagram).|  
 |Grön cirkel med en ikon formad som en skiva med en eller två pilar|De föreslagna leveransorderna med åtgärdsmeddelandet *Omplanera*, *Ändra antal* eller *Planera & ändra antal*<br /><br /> -   Kan ändras.<br />-   Visas när fältet **Ta med planeringsförslag** markeras (grönt diagram).<br /><br /> Pilarna återspeglar riktningen i planeringsförslaget. Till exempel återspeglar en vänsterpil med en uppåtpil ett åtgärdsmeddelande *Planera & ändra antal* som består av en bakåtomplanering och en ökning av antalet.|  

När du öppnar listrutan för snabbfliken **tidslinje** visas följande funktioner beroende på vad du väljer  

 |Funktion|Beskrivning|  
 |--------------|---------------------------------------|  
 |**Skapa ny leverans**|Skapa ett nytt element på punkten där du går till nedrullningsbara menyn som representerar en ny föreslagen leveransorder. Det blir en ny rad i planeringsförslaget när du väljer **Spara ändringar** på fliken **Process**.<br /><br /> Eventuella filtervärden, som definieras i fälten **Lagerställefilter** eller **Variantfilter** på Snabbfliken **Alternativ**, ska kopplas till den nya leveransordern. **Obs!** Om fältet är tomt eller har fler än ett filtervärde skapas den nya leveransordern med hjälp av följande koder: <ul><li>Om fältet är tomt kommer den nya tillgången skapas utan lagerställe eller en variantkod.</li><li>Om fler än en filtervärde definieras skapas den nya tillgången genom att den första filtervärdet enligt sorteringsordningen används.</li></ul> Om du vill ha en annan variant eller lagerställekod i den nya leveransordern måste du ändra numret manuellt på den nya planeringsraden.|  
 |**Autojustera tillgång**|Optimerar en ny efterfrågan som du har skapat i diagrammet genom att kontrollera att den resulterar i noll i lagret före nästa leverans.|  
 |**Ta bort tillgång**|Tar bort element på snabbfliken **Tidslinje**  och tar bort planeringsraden när du väljer **Spara ändringar** på fliken **Process**. Ikonen ändras till en diskenhet med ett rött kryss när leveransen har tagits bort. **OBS!:** Du kan endast ta bort en leverans av åtgärdsmeddelandetypen *Ny*. När du har valt **Spara ändringar** på fliken **Process** måste du manuellt ta bort den aktuella planeringsraden i planeringen eller inköpskalkylarket.|  
 |**Visa dokument**|Öppnar ordern, planeringsraden eller prognosen som elementet representerar.|  
 |**Zooma ut (Ctrl++)**|Gör skalan på x-axeln större, så att färre dagar visas. **Obs!**  Du kan också göra detta genom att trycka på Ctrl + rulla med mushjulet.|  
 |**Zooma in (Ctrl+-)**|Gör skalan på x-axeln mindre, så att fler dagar visas. **Obs!**  Du kan också göra detta genom att trycka på Ctrl + rulla med mushjulet.|  
 |**Återställ zoom (Ctrl+0)**|Återställer skalan på x-axeln till det som användes tidigare, innan du zoomade.|  

Förutom de kortkommmandon som nämndes tidigare kan du också använda följande kortkommmandon på snabbfliken **Tidslinje** .  

 |Kortkommmando|Beskrivning|  
 |---------------------|---------------------------------------|  
 |Ctrl + rulla med mushjulet|Ändrar skala på x-axeln.|  
 |Markera ett element och tryck sedan på Skift+pil|Flyttar elementet i pilens riktning.|  
 |Tabb|Flyttar till nästa element.|  
 |Skift+Tabb|Flyttar till föregående element.|  
 |Flytta ett element och tryck samtidigt på Esc.|Avbryter flyttningen. **Obs!** Detta fungerar inte om du har släppt musknappen.|

## <a name="see-also"></a>Se även  
[Planerad](production-planning.md)   
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
