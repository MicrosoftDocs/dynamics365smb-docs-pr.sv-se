---
title: Hantera partistorlekar
description: Det här avsnittet beskriver olika sätt att hantera partistorlekar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: f5af806ee6f8345932e13139de5f5d70700aed1e
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381861"
---
# <a name="handling-lot-sizes-in-production"></a>Hantera partistorlekar i produktion
När det gäller kvantitet kanske antalet artiklar som du producerar i en produktionsåtgärd inte korrelerar med hur du säljer dem. Du kan till exempel producera hundratals artiklar i ett enda parti, men sälja varje artikel för sig. När du konfigurerar dina produktionsflöden och strukturlistor (BOMs) finns det ett antal nyanser du bör tänka på när det gäller partistorlekar. Detta avsnitt beskriver hur partistorlekar påverkar kostnadsberäkningar och resursplanering.

## <a name="units-of-measure-in-production-bill-of-materials"></a>Måttenheter i produktionsstrukturlistor
Även om du anger basenheten (UOM) för en artikel kanske din struktur använder en annan UOM för den färdiga produkten. Bas-UOM för en artikel kan exempelvis vara PCS, men din struktur kan kräva lastpall eller ton. Detta kommer väl till pass när dina maskiner eller råa komponenter dikterar volymen. Du skulle förmodligen inte skulle vilja baka en enda muffin eftersom det är svårt att använda en del av ett ägg. Istället bakar du ett parti muffins för att minska spillmängden. För mer information, se [Skapa produktionsstrukturer](production-how-to-create-production-boms.md).

## <a name="lot-size-on-routing-lines"></a>Partistorlek på operationsföljdsrader
Ur ett operationsföljdsperspektiv kan du ange en partistorlek på operationsföljdsrader som anpassas till kapaciteten hos de maskiner som framställer artiklarna. Körningstiden på operationsföljdrader minskas proportionellt till partistorleken. 

Detta fungerar bra när kvantiteten på en produktionsorder är en faktor beroende av flödets partistorlek. Om din plåt exempelvis rymmer 10 muffins bör du baka 10, 20, 30 och så vidare, inte 5 eller 15.  Detta är ett mycket mindre problem om du har att göra med stora mängder.

Partistorlek är också populärt i tillverkningsmiljöer där utdata mäts som kvantitet som kan framställas under en fastställd tidsrymd. Om exempelvis volym per 9 timmars skift är 25 000 kubikfot kan du ange bearbetningstid som 9 timmar och partistorlek som 25 000.
Produktionsorderns kvantitet blir mindre viktigt eftersom bearbetningstiden på produktionsordern beräknas som körtid / partistorlek för att räkna ut körtiden per styck.
 
> [!NOTE]
> Värdet som definieras i partistorlek har ingen inverkan på den tid som anges i fältet **Konfigurationstid** för operationsföljdsraden. Konfigurationen sker endast en gång, även om det finns flera partier. Till exempel så att du inte behöver värma ugnen för den andra omgången muffins. Mer information finns i [Skapa verksamhetsföljder](production-how-to-create-routings.md).

## <a name="lot-sizes-for-items-and-stockkeeping-units"></a>Partistorlekar för artiklar och lagerhållningsenheter
Partistorlekar som definierats för operationsföljder är inte samma sak som partistorlekar för artiklar eller lagerhållningsenheter. Dessa värden används för ett annat ändamål och påverkar inte produktionskapaciteten. 

## <a name="lot-size-on-item-and-stockkeeping-units"></a>Partistorlekar för artiklar och lagerhållningsenheter
För artiklar och lagerhållningsenheter har partistorlekar följande effekter på kostnadsberäkning och försörjningsplanering:

* För standardkostnadsberäkning: Om du aktiverar **Kostnadsinkl. inställningar** på sidan **Tillverkningsinställningar** läggs kostnaden för inställningen till i standardkostnaden. Om du anger en partistorlek kommer inställningskostnaden för operationsföljdåtgärden att minskas enligt en partistorlek. Om din partistorlek som definieras på artikelkort exempelvis är 10, och det tar 15 minuter att värma ugnen, kommer kostnaden för bränslet att fördelas på de 10 muffins som ungefär 1,5 minuter per styck. 

> [!NOTE]
> Inställningskostnaderna hanteras annorlunda än ett standardkostnads- eller kapacitetsallokeringsperspektiv. Om producerad kvantitet inte matchar den partistorlek som definierats på artikelkortet som kommer att leda till variation. Mer information finns i [Administrera lagerkostnader](finance-manage-inventory-costs.md). <!--not sure that I got this part right seems to repeat the first example.-->

För leveransplanering fungerar partistorleksinställningen på artiklar med **Standarddämpare %** på sidan **Tillverkningsinställning**. [!INCLUDE[prod_short](includes/prod_short.md)] kommer att ignorera förändringar i efterfrågan som understiger dämparprocenten och inte kommer att skapa planeringsförslag. Till exempel anges 15 i fältet Standarddämpare % och vi har en produktionsorder för 20 muffins för att mätta 20 gäster, men en gäst kan inte delta. [!INCLUDE[prod_short](includes/prod_short.md)] kommer att ignorera den enda saknade gästen eftersom det endast utgör 10 % av den partistorlek om 10 som definieras på objektet. Om två gäster emellertid inte kan delta kommer [!INCLUDE[prod_short](includes/prod_short.md)] att föreslå att vi minskar orderkvantiteten eftersom två utgör 20 % av partistorleken. Mer information om planering finns i [Planering](production-planning.md).

## <a name="see-also"></a>Se även
[Skapa produktionsstrukturer](production-how-to-create-production-boms.md)  
[Arbeta med måttenheter för produktionsbatch](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)
[Skapa flöden](production-how-to-create-routings.md)  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]