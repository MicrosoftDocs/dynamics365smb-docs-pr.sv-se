---
title: Välj för intern verksamhet i avancerade konfigurationer för distributionslager
description: Om lagerstället använder plockning och leverans väljer du komponenter för produktions-, och monterings- och projektaktiviteter på sidan Distributionslagerplockning.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/02/2022
ms.author: bholtorf
ms.openlocfilehash: 2ef879e5dbabb9281114d62a956ad4b10113c199
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607560"
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Plocka för produktion, montering eller jobb i avancerade distributionslagerkonfigurationer

I avancerade distributionslagerkonfigurationer, där det har angetts att lagerstället ska använda plockning samt leverans, kan du välja plockkomponenter för produktions- och monteringsaktiviteter på sidan **Dist.lager plockning**.  

Du kan också använda sidan **Transportkalkylark** för att flytta artiklar spontant mellan lagerställen, utan att referera till ett ursprungsdokument. Mer information finns i [Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Information om hur du plockar artiklar på grundläggande lagerställen som endast definierats för plockning, se [Flytta komponenter till ett verksamhetsområde i grundläggande distributionslagerkonfigurationer](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

> [!NOTE]
> Du kan inte skapa ett dokument för distributionslagerplockdokument från grunden, eftersom en plockningsaktivitet alltid ingår i ett arbetsflöde, i ett pull-/pushscenario.  

Du kan skapa dokumentet för dist.lager plockning med en pushmetod genom att välja **Skapa dist.lagerplockning** i källdokumentet, till exempel en släppt monteringsorder eller lagerutleverans. För mer information, se [Plocka artiklar med lagerplockningar](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Du kan också skapa ett distributionslagerplockdokument i ett pull-scenario med hjälp av sidan **Plockkalkylark** för att identifiera plockförfrågningar. Den här metoden är användbar för utleveranser och interna operationer. Du kan sedan skapa de distributionslagerplockdokument som krävs.  

Nedan förklaras ett pull-scenario där du plockar komponenter för en släppt produktionsorder via sidan **Plockningskalkylark**. Följande procedur gäller även för en monteringsorder.  

För att skapa plockning för både pull- och pushscenarier, måste källdokumenten släppas. Släppa källdokumenten för intern operation på följande sätt.  

|Källdokument|Släppningsmetod|  
|---------------------|--------------------|  
|Produktionsorder|Ändra ordertyp till släppta produktionsorder.|  
|Monteringsorder|Ändra status till släppt.|
|Projekt | Ändra status till Öppen.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Så här plockar du komponenter med hjälp av plockningskalkylarket

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Plockningskalkylark** och väljer sedan relaterad länk.  
2. Välj åtgärden **Hämta dist.lager dokument** och välj sedan de komponentrader från den släppta produktionsordern.  
3. Sortera raderna för att säkerställa effektiv plockning. Du kanske vill kombinera rader för att spara medarbetartid.  
4. Välj åtgärden **Skapa plockning**.  
5. Definiera hur du skapar dokument för dist.lager plockning och hur här fältet sorterar plockningsrader genom att fylla i sidan **Skapa plockning**.  
6. Välj knappen **OK**. Dokumenten för dist.lager plockning skapas med plockningsrader för varje komponent som krävs i den intern operation.  

Operationsområden som t.ex. produktionsgolv kan ha en standardlagerplats för komponenterna som behövs. Om så är fallet läggs standardlagerplatskoden till i distributionslagerplockdokumentet för att ange var artiklarna ska placeras. Mer information finns i verktygstipsen för **Till prod.-lagerplats – kod** eller fältet **Till monteringsplats – kod**.

## <a name="filling-the-consumption-bin"></a>Fylla förbrukningslagerstället

Diagrammet visar hur **Lagerställeskod** på produktionsorderkomponentraderna fylls enligt platsinställningen.

![Flödesschema för lagerplats.](media/binflow.png "BinFlow")  

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
