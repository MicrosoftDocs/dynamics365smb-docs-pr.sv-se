---
title: "Så här: Plocka för produktion i grundläggande distributionslagerkonfiguration | Microsoft Docs"
description: "När distributionslagrets lagerställe kräver plockningsbearbetning, men inte utleveransbearbetning, använder du fönstret **Lagerplockning** för att ordna och registrera plockning av komponenter."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 68702e384ea750535a8d7e5b83ee619856b6a34b
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="pick-for-production-or-assembly"></a>Plocka för produktion eller montering
Hur du för in plockningskomponenter för produktions- eller monteringsorder beror på hur distributionslagret har ställts in som lagerställe. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

Igrundläggande lagerkonfigurationer där lagerställe kräver plockningsbearbetning, men inte utleveransbearbetning, använder du fönstret **Lagerplockning** för att ordna och registrera plockning av komponenter.  

I grundläggande distributionslagerkonfiguration måste du plocka för monteringsorder med fönstret **Lagertransport**. Mer information finns i avsnittet ”Hantera artiklar för montering mot kundorder med lagerplockning” i [Plocka artiklar med Lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md).  

I avancerad distributionslagerkonfiguration, där lagerställen kräver både plockning och utleveranser, använder du **dist.lager plockning** för att få komponenter till produktions- eller monteringsordern.

> [!NOTE]  
>  Lagerplockningar och lagerförflyttningar har följande viktiga skillnader:  
>   
>  -   När du registrerar en lagerplockning för en intern operation, bokförs till exempel produktion, förbrukningen av markerade komponenterna samtidigt. När du registrerar en lagerförflyttning för en intern operation, registrerar du bara en fysisk transport av nödvändiga komponenter till en lagerplats i verksamhetsområdet utan att bokföra förbrukningen.  
> -   Om du använder lagerplockningar definierar fältet **Lagerplatskod** på en produktionsorderkomponentrad lagerplatsen *ta* från vilken antalet komponenter minskas när konsumtionen bokförs. Om du använder lagerförflyttningar definierar fältet **Lagerplatskod** på en produktionsorderkomponentrad, lagerplatsen *plats* i verksamhetsområdet från vilken antalet lagerarbetare måste placera komponenter.  

En systemvillkor för plockning eller flyttning av komponenter för källdokument, är att en avgående distributionslagerkrav finns för att meddela lagerområdet i komponentbehovet. Den avgående distributionslagerförfrågan skapas när produktionsorderns status ändras till Släppt eller när en släppt produktionsordern skapas.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Plocka komponenter i en grundläggande lagerkonfiguration.
I grundläggande distributionslagerkonfiguration, där det har angetts att lagerstället ska endast använda plockning samt leverans, kan du välja plockkomponenter i fönstret **Lagerplockning**. För mer information, se [Plocka artiklar med lagerplockningar](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lagerplockningar** och välj sedan relaterad länk.  
2.  Om du vill komma åt produktionsorderns komponenter väljer du åtgärden **Hämta källdokument** och väljer den släppta produktionsordern.  
3.  Utför plockningen och registrera den verkliga plockningsinformationen i fältet **Plockat antal**.  
4.  När raderna är färdiga att bokföras klickar du på **Bokför**. Bokföringen skapar de nödvändiga distributionslagertransaktionerna och bokför förbrukningen av artiklarna.  

Du kan också skapa en **lagerplockning** direkt från den släppta produktionsordern. Välj **Skapa lagerartikelinförsel/Plocka**, välj **Skapa lagerplockning** och välj sedan **OK**-knappen.

Du kan också använda **Lagertransport**-fönstret för att flytta artiklar mellan lagerplatser ad hoc-, d.v.s till utan att referera till ett ursprungsdokument.
Mer information finns i [Flytta komponenter till ett verksamhetsområde i grundläggande distributionslagerkonfiguration](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Hantering av artikel för montering mot kundorder i lagerplockningar
Fönstret **Lagerplockning** används också för att plocka och leverera för försäljning där artiklar måste vara församlade, innan de kan levereras. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).

Artiklar som ska levereras, inte fysiskt finns i en lagerplats, förrän de är bokförda och församlade som utflöde på en lagerplats i monteringsområdet. Det innebär att plocka artiklar för montering mot kundorder för utleverans följer ett speciellt flöde. Från en lagerplats tar lagerarbetare monteringsartiklarna till ett leveransdocka och bokför sedan lagerplockningen. Bokförda lagerplockningen bokför sedan monteringsutflödet, komponentförbrukningen och utleveransen.

Du kan lägga upp [!INCLUDE[d365fin](includes/d365fin_md.md)] för att automatiskt skapa en lagertransport, när monteringsartikeln för lagerplockningen skapas. Du anger dessa inställningar genom att välja fältet **skapa transporter automatiskt** i fönstret **Monteringsinställningar** Mer information finns i [Flytta komponenter till ett verksamhetsområde i grundläggande lagerstyrning](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Lagerplockningsrader för försäljningsartiklar skapas på olika sätt beroende på om ingen, några eller alla försäljningsradantal monteras mot kundorder.

I vanliga lagerförsäljningar, när du använder lagerplockningar för att bokföra utleveransen av lagerantal, skapas en lagerplockrad eller flera om artikeln ligger i olika lagerplatser för varje försäljningsorderrad. Denna plockningsrad baseras på antalet i **Ant. att utleverera**.

I montering mot kundorder försäljning, där hela antalet på försäljningsorderraden är monterad till order, skapas en lagerplockningsrad för det antal. Detta innebär att värdet i fältet Antal att montera är lika med värdet i fältet **Antal att leverera**. Fältet **montering mot kundorder** är markerat på raden.

Om ett monteringsutflöde har angetts för lagerstället, när värdet i fältet **Lagerpl.kod för mont. mot lev.** eller värdet i **Från monteringsplats - kod** i den ordern infogas i fältet **Lagerplatskod** på lagerplockningsraden.

Om ingen lagerplatskod anges på försäljningsorderraden, och ingen monteringsutflöde har angetts för lagerstället, är **Lagerplatskod** på lagerplockningsraden tomt. Lagerarbetaren måste öppna **Lagerplatsinnehåll**och markera den lagerplats där monteringsartiklarna är församlade.

I alla scenarier där en del av antalet måste först vara församlad och ett annat ska plockas från lagret, skapas ett minimum på två lagerplockningsrader. En plockningsrad är för antal för montering mot kundorder. Den andra plockningsraden beror på vilka lagerplatser som kan uppfylla det återstående antalet från lagret. Lagerplatskoder på de två raderna är ifyllt olika sätt, som beskrivs för de två olika försäljningstyperna. Mer information finns i avsnittet Kombinationsscenarion i [Förstå montering mot order och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="to-pick-components-in-advanced-warehouse-configurations"></a>Plocka komponenter i en avancerad lagerkonfiguration.
I avancerad distributionslagerkonfigurationer, där det har angetts att lagerstället ska använda plockning samt leverans, kan du välja plockkomponenter för produktion- och monteringsaktiviteter via fönstret **Dist.lagerplockning**. För mer information, se [Plocka artiklar med lagerplockningar](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Du kan också använda fönstret **Transportkalkylark** för att flytta artiklar mellan lagerplatser ad hoc, d.v.s utan att referera till ett källdokument. Mer information finns i [Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Du kan inte skapa ett dokument för dist.lager plockning från grunden, eftersom en plockningsaktivitet alltid ingår i ett arbetsflöde, i ett pull-/pushscenario.  

Du kan skapa dokumentet för dist.lager plockning med en pushmetod genom att välja **Skapa dist.lagerplockning** i källdokumentet, till exempel en släppt monteringsorder eller lagerutleverans. För mer information, se [Plocka artiklar med lagerplockningar](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Du kan också skapa dokumentet för dist.lager plockning med en pullmetod med hjälp av **Plockningskalkylark** fönstret för att undersöka plockningsförfrågningar, både för leverans och intern operation, och sedan skapa de nödvändiga dokumentet för dist.lager plockning.  

Nedan förklaras ett pull-scenario där du plockar komponenter för en släppt produktionsorder via **Plockningskalkylark** fönstret. Följande procedur gäller även för en monteringsorder.  

För att skapa plockning för både pull- och pushscenarier, måste källdokumenten släppas. Släppa källdokumenten för intern operation på följande sätt.  

 |Källdokument|Släppningsmetod|  
 |---------------------|--------------------|  
 |Produktionsorder|Ändra ordertyp till släppta produktionsorder.|  
 |Monteringsorder|Ändra status till släppt.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Så här plockar du komponenter med hjälp av plockningskalkylarket  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Plockningskalkylark**, och välj sedan relaterad länk.  
2.  Välj åtgärden **Hämta dist.lager dokument** och välj sedan de komponentrader från den släppta produktionsordern.  
3.  Analysera raderna, sortera dem för att garantera en effektiv plockningsrunda och kombinera dem med andra kalkylarksrader, om så behövs, för att minimera plockningstiden för den anställda.  
4.  Välj åtgärden **Skapa plockning**.  
5.  Definiera hur du skapar dokument för dist.lager plockning och hur här fältet sorterar plockningsrader genom att fylla i **Skapa plockning** fönstret.  
6.  Välj knappen **OK**.

Dokumenten för dist.lager plockning skapas med plockningsrader för varje komponent som krävs i den intern operation.

Om internt verksamhetsområde, till exempel ett produktionslagerplats, har upprättats med en standardlagerplats för placering av komponenter som ska användas i operationen, infogas den lagerplatskoden i placeringsraderna på dokumentet för dist.lager plockning för att visa lagerarbetare var artiklarna ska placeras. Mer information finns i [Ställa in grundläggande dist.lager med verksamhetsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

## <a name="filling-the-consumption-bin"></a>Fylla förbrukningslagerplatsen
Diagrammet visar hur **Lagerplatskod** på produktionsorderkomponentraderna fylls enligt platsinställningen.

![Flödesschema för lagerplats](media/binflow.png "BinFlow")

## <a name="see-also"></a>Se även
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

