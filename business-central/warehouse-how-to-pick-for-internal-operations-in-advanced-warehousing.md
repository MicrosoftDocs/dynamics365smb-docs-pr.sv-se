---
title: 'Så här: välj för Intern operation i avancerad distributionslagerkonfiguration | Microsoft Docs'
description: I avancerad distributionslagerkonfiguration, där det har angetts att lagerstället ska använda plockning samt leverans, kan du välja plockkomponenter för produktion- och monteringsaktiviteter med sidan **Dist.lager plockning**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 4272512046a3951eb933fb25c869d5e9d7a3b416
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876613"
---
# <a name="pick-for-production-or-assembly-in-advanced-warehouse-configurations"></a>Plocka för produktion eller montering i avancerad distributionslagerkonfiguration
I avancerad distributionslagerkonfiguration, där det har angetts att lagerstället ska använda plockning samt leverans, kan du välja plockkomponenter för produktion- och monteringsaktiviteter med sidan **Dist.lager plockning**.  

Du kan också använda sidan **Transportkalkylark** för att flytta artiklar mellan lagerplatser ad hoc-, d.v.s till utan att referera till ett ursprungsdokument. Mer information finns i [Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Information om hur du plockar artiklar för intern verksamhet på grundläggande lagerställen som endast definierats för plockning, se [Flytta komponenter till ett verksamhetsområde i grundläggande distributionslagerkonfiguration](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

Du kan inte skapa ett dokument för dist.lager plockning från grunden, eftersom en plockningsaktivitet alltid ingår i ett arbetsflöde, i ett pull-/pushscenario.  

Du kan skapa dokumentet för dist.lager plockning med en pushmetod genom att välja **Skapa dist.lagerplockning** i källdokumentet, till exempel en släppt monteringsorder eller lagerutleverans. För mer information, se [Plocka artiklar med lagerplockningar](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Du kan också skapa dokumentet för dist.lager plockning med en pullmetod med hjälp av sidan **Plockningskalkylark** för att undersöka plockningsförfrågningar, både för leverans och intern operation, och sedan skapa de nödvändiga dokumentet för dist.lager plockning.  

Nedan förklaras ett pull-scenario där du plockar komponenter för en släppt produktionsorder via sidan **Plockningskalkylark**. Följande procedur gäller även för en monteringsorder.  

För att skapa plockning för både pull- och pushscenarier, måste källdokumenten släppas. Släppa källdokumenten för intern operation på följande sätt.  

|Källdokument|Släppningsmetod|  
|---------------------|--------------------|  
|Produktionsorder|Ändra ordertyp till släppta produktionsorder.|  
|Monteringsorder|Ändra status till släppt.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Så här plockar du komponenter med hjälp av plockningskalkylarket  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Hämta kalkylark** och välj sedan relaterad länk.  
2.  Välj åtgärden **Hämta dist.lager dokument** och välj sedan de komponentrader från den släppta produktionsordern.  
3.  Analysera raderna, sortera dem för att garantera en effektiv plockningsrunda och kombinera dem med andra kalkylarksrader, om så behövs, för att minimera plockningstiden för den anställda.  
4.  Välj åtgärden **Skapa plockning**.  
5.  Definiera hur du skapar dokument för dist.lager plockning och hur här fältet sorterar plockningsrader genom att fylla i sidan **Skapa plockning**.  
6.  Välj knappen **OK**. Dokumenten för dist.lager plockning skapas med plockningsrader för varje komponent som krävs i den intern operation.  

Om internt verksamhetsområde, till exempel ett produktionslagerplats, har upprättats med en standardlagerplats för placering av komponenter som ska användas i operationen, infogas den lagerplatskoden i placeringsraderna på dokumentet för dist.lager plockning för att visa lagerarbetare var artiklarna ska placeras. Mer information finns på **Till prod.-lagerplats - kod** eller fältet **Till monteringsplats - kod**.

## <a name="filling-the-consumption-bin"></a>Fylla förbrukningslagerplatsen
Diagrammet visar hur **Lagerplatskod** på produktionsorderkomponentraderna fylls enligt platsinställningen.

![Flödesschema för lagerplats](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Se även
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
