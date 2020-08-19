---
title: Förstå montering mot kundorder och montering mot lager | Microsoft Docs
description: Monteringsartiklar kan anges genom att sammanföra dem när de beställs eller genom att montering att finnas i lagret tills de behov från en försäljningsorder.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 07/23/2020
ms.author: bholtorf
ms.openlocfilehash: a5fc9b13e28b51d776fad6d02feae4624b756c4c
ms.sourcegitcommit: 7b5c927ea9a59329daf1b60633b8290b552d6531
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617942"
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock"></a>Förstå montering mot kundorder och montering mot lager
Monteringsartiklar kan levereras i följande två processerna:  

-   Montering mot order.  
-   Montering mot lager.  

## <a name="assemble-to-order"></a>Montering mot kundorder  
Du använder vanligtvis *montering mot kundorder* för de artiklar som du inte vill att tillverka, eftersom du förväntar dig att anpassa dem till kundförfrågningar, eller eftersom du vill att minska den bärande kostnaden för lagret. Den andra funktionen är:  

-   Kapacitet för att anpassa monteringsartiklar, när ta en försäljningsorder.  
-   Översikt över tillgänglighet för monteringsartikeln och dess komponenter.  
-   Möjligheter att reservera monteringskomponenter direkt för att garantera uppfyllning av order.  
-   Arbeta för att bestämma vinst av anpassad order efter att summera priser och kostnad.  
-   Integrering till distributionslagret som gör det enklare att montering och leverans.  
-   Kapacitet till montering mot kundorder i fönstret för att skapa en förs.offert eller avropsorder, försäljning.  
-   Möjligheter att kombinera lagerkvantiteten med antalet för montering mot kundorder.  

I montering mot kundorderprocessen är artikel satt samman som svar på en försäljningsorder och med ett ett-till-ett-länk mellan monteringsorder och försäljningsorder.  

När du anger en artikel för montering mot kundorder på en försäljningsrad, skapas en monteringsorder automatiskt med ett huvud baserat på försäljningsraden och med rader som baseras på artikelns monteringsstruktur multiplicerat med partistorlek. Du kan använda sidan **Montering mot kundorderrader** för att visa kopplad monteringsorderraderna för att stödja anpassning av monteringsartikeln och i ett leveransdatum som baseras på tillgänglighetsinformation för komponent. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
>  Även om detta inte är en del av standard processen, kan du sälja lagerkvantiteten med antalet för montering mot kundorder. Mer information finns i [Så här säljer du lagerartiklar i flöde för montering mot kundorder](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

 Om du vill aktivera den här processen, måste fältet **Monteringsmetod** på artikelkortet vara **Montering mot kundorder**.  

## <a name="assemble-to-stock"></a>Montering mot lager  
 Du kan använda den för *montering mot lager* för de artiklar som du vill att sammanställa framåt av försäljning, till exempel att förbereda för en satskampanj och hålla lagret tills de beställs. Dessa artiklar är vanligtvis standardobjekt som emballerade satser, som du inte erbjuder för att anpassa till kundförfrågningar.  

 I montering mot lager monteras artiklar utan direkt försäljningsbehov och i lagras som en lagerartikel i distributionslagret för senare försäljning eller förbrukning som ett detaljmontage. Mer information finns i [Montera artiklar](assembly-how-to-assemble-items.md). I det här läget plockas artikel och bearbetas som ett enstaka artikel och är hanterade som en avslutad produktionsartikel.  

 När du anger ett montering mot lager artikel på en försäljningsrad, den är som alla andra sålda artiklar från lagret. Till exempel kontrolleras tillgänglighet för monteringsartikeln endast.  

> [!NOTE]  
>  Även om detta inte är en del av processen standard, kan du sammanställa en artikel för order, även om det har konfigurerats till att monteras mot lager. Mer information finns i [Så här säljer du artiklar för montering mot kundorder och lagerartiklar ihop](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

 Om du vill aktivera den här processen, måste fältet **Monteringsmetod** på artikelkortet vara **Montering mot lager**.  

## <a name="combination-scenarios"></a>Kombinationsscenarion  
 En allmän princip i monteringshantering är att montering mot kundorder, när de kombineras på en försäljningsorderrad, måste levereras innan och lagerkvantiteten.  

 Om en monteringsorder är kopplad till en försäljningsorderrad, uppdateras värdet i fältet i **Antal att montera mot kundorder** på försäljningsorderraden, **Antal att montera** via **Antal** på monteringsorderhuvudet. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).  

 Dessutom värdet i fältet fält **Antal att montera** är relaterat till fältet **Ant. att utleverera** på försäljningsorderraden och kopplingen hanterar utleveransbokning för montering mot kundorder mängder, både delvis och helt. Detta gäller både när hela antalet på försäljningsraden monteras mot kundorder, och i kombinationsscenarion där en del av försäljningsradantalet monteras mot kundorder och en annan del skickas från lagret. Men i kombinationsscenariot har du ytterligare möjligheter vid delleverans, då du kan ändra fältet **Antal att montera** inom fördefinierade regler, och anger hur många enheter som ska levereras delvis från lagret, samt hur många som ska levereras delvis genom att montera till order.  

 Om hela antalet på försäljningsraden måste monteras enligt order och levereras kopieras värdet i fältet **Ant. att utleverera** kopieras **Antal att montera** i den kopplade monteringsordern när du ändrar antal som ska levereras. Detta försäkrar att det antalet som ska levereras uppfyller antalet i montering mot kundorder.  

 Dock i kombinationsscenarion, hela värdet i **Ant. att utleverera** kopieras inte till **Antal att montera** på monteringsorderhuvudet. I stället detta standardvärde infogas i fältet **Antal att montera** och beräknas från fältet **Ant. att utleverera** enligt en fördefinierad regel som garanterar leverans av montering mot kundorderantalet först.  

 Om du vill att avvika från det här standardvärdet, eftersom till exempel du bara vill sammanställa mer eller mindre av antalet i fältet **Ant. att utleverera** kan du ändra **Antal att montera** men endast enligt fördefinierade regler, som illustreras under.  

 Ett exempel på varför du vill ändra kvantiteten så att montera, är att du ska delvis bokföra utleveransen av lagersaldot, innan monteringsutflöde kan levereras.  

 Följande tabell förklarar regler som definierar den minimala och maximala värde som du kan ange manuellt i **Antal att montera** för att avvika från standardvärdet i en kombinationsscenario. Tabellen visar en kombinationsscenario där **Ant. att utleverera** på den kopplade försäljningsordern ändras från 7 till 4, och standard för **Antal att montera** är därför 4.  

|-|Försäljningsorderrad|Monteringsorderhuvud|  
|-|----------------------|---------------------------|  
||**Antal**|**Ant. att utleverera**|**Antal att montera mot kundorder**|**Utlevererat antal**|**Antal**|**Antal att montera**|**Monterad kvantitet**|**Återstående antal**|  
|Initial|10|7|7|0|7|7|0|7|  
|Ändra||4||||4 (infoga som standard)|||  

 Utifrån det ovan, kan du endast ändra **Antal att montera** enligt nedan:  

-   Den lägsta kvantitet som du kan ange är 1. Det är eftersom du måste åtminstone sammanställa en enhet för att kunna sälja de fyra enheter, antaget att de återstående tre finns i lager.  
-   Den höga kvantitet som du kan ange är 4. Detta görs för att se till att du inte monterar flera av denna monteringmotkundorderartikel än vad som behövs på försäljningen.  

## <a name="see-also"></a>Se även  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med strukturer](inventory-how-work-BOMs.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
