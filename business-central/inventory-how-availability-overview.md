---
title: Skapa en tillgänglighetsöversikt | Microsoft Docs
description: Du kan få information om dispositionen av artiklar eller lager mellan lagerställen per försäljning eller inköphändelser efter en viss tidsperiod eller efter artikelns placering på en monterings- eller produktionsstruktur.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.date: 06/03/2019
ms.author: SorenGP
ms.openlocfilehash: f1c7fbe75dfa9767e5a5dfbfbe354fbd3f9448b5
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621005"
---
# <a name="view-the-availability-of-items"></a>Visa artikeldisposition
Utifrån en verksamhetsuppgift kan du få avancerad information om när och var en artikel är disponibel, exempelvis när du talar med en kund om ett leveransdatum.

Du kan visa dispositionen för alla artiklar per lagerställe, och du kan visa varje artikels disposition per händelse, tid eller lagerställe. En händelse är alla planerade artikeltransaktioner, till exempel en utleverans eller en inleverans av ankommande överföring.

> [!NOTE]  
>   Tillgänglighetsvyer per lagerställe kräver att du för lager på flera lägerställen. Mer information finns i [Ange platser](inventory-how-setup-locations.md).

Om du nvänder lagerfunktionerna varierar tillgängligheten beroende på fördelningar på lagerplatsnivån när distributionslageraktiviteter, till exempel plockning och transport, inträffar och när lagerreservationssystemet har begränsningar som ska uppfyllas. En ganska komplex algoritm kontrollerar att alla villkor är uppfyllda innan antal tilldelas till plockningar för utgående flöden. Mer information finns i [Designdetaljer: disposition i distributionslagret](design-details-availability-in-the-warehouse.md).

I [!INCLUDE[d365fin](includes/d365fin_md.md)], visas dispositionssiffror i två olika fält, var och en med en annan definition:

* Fältet **Lagersaldo**, på vissa platser med namnet **Lager**, visar den faktiska kvantiteten enligt bokförda artikeltransaktioner.
* Fältet **Lagerutveckling över tid** beräknas och visar antalet i lager samt planenliga inleveranser minus bruttobehov. (I [!INCLUDE[d365fin](includes/d365fin_md.md)], kan planenliga inleveranser inkludera antal på inköpsorder och inkommande överföringsorder. Bruttobehov omfattar kvantiteter i försäljningsorder och avgående överföringsorder.)

> [!TIP]  
>   Lagerutvecklingen över tid är särskilt relevant att visa på sidorna **Artikeldisp. per perioder** och **Artikeldisposition per händelse** eftersom dessa innehåller datumdimensionen.  

> [!NOTE]  
>   I följande procedurer beskrivs hur du visar avancerad tillgänglighetsinformation från artikellistan och artikelkortet. Du kan också visa information för artikeln på raden via försäljningsdokumentraderna. Mer information finns i [Sälja produkter](sales-how-sell-products.md).

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Visa tillgängligheten för en artikel efter in- eller utlevereranstidpunkt
Du kan visa tillgängligheten för en artikel enligt planerade artikeltransaktioner på sidan **Artikeldisposition per händelse**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.
2. Öppna kortet för en artikel som du vill visa dispositionen för.
3. Välj åtgärden **Artikeldisposition per**, och välj sedan åtgärden **Händelse**.

    På sidan **Artikeldisposition per händelse** visas hur lagerkvantiteten utvecklas över tid enligt schemalagda händelser för ut- och inleverans. Sidan har en komprimerad vy som visar en rad med ackumulerad information per tidsintervall då lagerkvantiteterna ändras. Tidsintervall där inga händelser inträffat visas inte. Du kan expandera varje rad för att visa information om händelsen eller händelserna som orsakade det ackumulerade antalet på raden.
4. Välj värdet i fältet **Lagerutveckling över tid** för att visa artikeltransaktionerna och öppna dokument som utgör värdet.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>Visa dispositionen för en artikel under olika perioder
Du visar en artikels disposition över tid för angivna tidsperioder på sidan **Artikeldisp. per perioder**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.
2. Öppna kortet för en artikel som du vill visa dispositionen för.
3. Välj åtgärden **Artikeldisposition per** och välj sedan åtgärden **Period**.

    Sidan **Artikeldisp. per perioder** visar hur artikelns lagerkvantitet utvecklas över tid under en period som du själv väljer, till exempel dag, vecka eller kvartal.
4. Välj värdet i fältet **Lagerutveckling över tid** för att visa artikeltransaktionerna och öppna dokument som utgör värdet.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>Visa tillgängligheten för en artikel på de lägerställen där den lagras
Du kan visa dispositionen av en artikel på de olika lägerställen där den lagras på sidan **Artikeldisp. per lagerställe**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.
2. Öppna kortet för en artikel som du vill visa dispositionen för.
3. Välj åtgärden **Artikeldisposition per** och välj sedan åtgärden **Lagerställe**.

    Sidan **Artikeldisp. per lagerställe** visar hur artikelns lagerkvantitet utvecklas i framtiden och för varje lagerställe där den lagras.
4. Välj värdet i fältet **Lagersaldo** för att visa de artikeltransaktioner som utgör värdet.
5. Välj värdet i fältet **Lagerutveckling över tid** för att visa artikeltransaktionerna och öppna dokument som utgör värdet.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>Visa tillgängligheten för alla artiklar per det lagerställe där de lagras
Du kan visa disposition för alla artiklar på alla lägerställen på sidan **Artiklar per lagerställe**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.
2. Välj åtgärden **Artiklar per lagerställe**.

    Sidan **Artiklar per lagerställe** visar, för alla artiklar, hur många som är tillgängliga på respektive lagerställe.
3. Välj värdet i fältet **Lagersaldo** för att visa de artikeltransaktioner som utgör värdet.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms"></a>För att visa tillgängligheten för en artikel med dess användning i monterings- eller produktionsstrukturer
Om en artikel finns i monterings- eller produktionsstrukturer, antingen som en överordnad artikel eller en komponent kan du se hur många enheter av den som krävs på sidan **Artikeldisposition per strukturnivå**. Sidan visar hur många av en överordnad det går att producera baserat på dispositionen av underordnade artiklar på underliggande rader. Ett objekt som har en monterings- eller produktionsstruktur visas på sidan som en komprimerbar rad. Du kan expandera raden för att visa underliggande komponenter och underenheter på låg-nivå med egna strukturer.

Du kan använda sidan för att se om du kan uppfylla en försäljningsorder för en artikel på ett angivet datum genom att se den aktuella tillgängligheten och antal av komponenterna. Du kan också använda sidan för att identifiera flaskhalsar i relaterade strukturer.

På varje rad på sidan för både den överordnade artikeln och underartiklar visas tillgänglighetssiffror i följande nyckelfält. Du kan använda dessa siffror som löfte om hur många enheter av en överordnad artikel du kan tillhandahålla om du startar den relaterade monteringen.

|Fält|Beskrivning|
|------|-----------|
|**Kan skapa överordnad**|Visar hur många enheter du kan tillverka av monteringsartiklarna till toppartikeln. Fältet anger hur många enheter av omedelbart överordnade artiklar som kan monteras. Värdet baseras på tillgänglighet till artikeln som finns specificerad på raden.|
|**Kan skapa toppartikel**|Visar hur många enheter du kan tillverka av toppartikeln. Fältet anger hur många enheter av strukturartikeln på den översta raden som kan monteras. Värdet baseras på tillgänglighet till artikeln som finns specificerad på raden.|

### <a name="item-availability-by-bom-level-page"></a>Sidan Artikeldisposition per strukturnivå
Sidan **Artikeldisposition per strukturnivå** visar information för artikeln på kortet eller dokumentraden som sidan har öppnats för. Artikeln visas alltid på den översta raden. Du kan visa information för andra artiklar eller alla artiklar genom att ändra värdet i fältet **Artikelfilter**.

> [!NOTE]  
>   Som standard visar tillgänglighetssiffror på raderna en total disposition för alla artiklar under toppartikeln. Dessa siffror visas i fältet **Disponibelt antal** och är fokuserade på toppartikeln. Informationen om hur delmonteringar du kan göra kan emellertid snedfördelas. Om du vill få en indikation på exakt hur många överordnade artiklar du kan producera måste du rensa kryssrutan **Visa total disposition** och sedan visa siffran i fältet **Kan skapa överordnad**.

Fältet **Flaskhals** anger vilken artikel i strukturen som begränsar dig från att kunna producera ett större antal än antalet som visas i fältet **Kan skapa toppartikel**. En flaskhalsartikel kan till exempel vara en inköpt komponent med ett förväntat inleveransdatum som är för sent för att skapa fler enheter av toppartikeln per datumet i fältet **Behövs den**.

## <a name="assembly-availability-page"></a>Sidan Monteringsdisposition
Fönstret **Monteringsdisposition** visar detaljerade dispositionsinformation för monteringsartikeln. Den öppnar:

- Automatiskt från en försäljningsorderrad i montering mot kundorder-scenario, när du anger ett antal som orsakar en komponentdispositionsproblem.
- Automatiskt från en monteringsorderhuvud när du anger ett värde i fältet Antal som orsakar en komponentdispositionsproblem.
- Manuellt, när du öppnar fönstret från en monteringsorder. På Åtgärder fliken i Funktioner gruppen, klicka på Visa disposition.

Snabbfliken **Detaljer** visar de detaljerade dispositionsinformationen för monteringsartikeln, inkl. hur många av antalet monteringsorder som kan monteras efter förfallodatum utifrån tillgänglighet av nödvändiga komponenter. Det visas i Möjlig att montera på Detaljer Snabbfliken.

Värdet i **Möjlig att montera** fältet visas i den röda teckensnittet, om kvantiteten är lägre än antal i **återstående antal** fältet, som betyder att det inte finns tillräckligt med tillgängliga komponenter att sammanställa hela kvantitet.

Snabbfliken **Rader** visar de detaljerade dispositionsinformationen för monteringskomponenterna.

Om en eller flera monteringskomponenter inte är tillgänglig, visas det i **Möjlig att montera** fältet på den aktuella raden som ett antal mindre än antalet i **återstående antal** på **Detaljer** Snabbfliken.

## <a name="see-also"></a>Se även
[Hantera lager](inventory-manage-inventory.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med strukturer](inventory-how-work-BOMs.md)    
[Konfigurera platser](inventory-how-setup-locations.md)  
[Överföra lager mellan olika lagerställen](inventory-how-transfer-between-locations.md)  
[Sälja produkter](sales-how-sell-products.md)      
[Arbeta med Business Central](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)
