---
title: Plocka produktion eller montering i en grundläggande lager
description: När distributionslagrets lagerställe kräver plockningsbearbetning, men inte utleveransbearbetning, använder du sidan Lagerplockning för att ordna och registrera plockning av komponenter.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 80a34d18c94038ded7bcf405cabd1c67ddf82539
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078420"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Plocka för produktion eller montering i grundläggande distributionslagerkonfiguration

Hur du för in plockningskomponenter för produktions- eller monteringsorder beror på hur distributionslagret har ställts in som lagerställe. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Plocka komponenter för produktion i en grundläggande lagerkonfiguration.

Bokföringsmetoder påverkar också flödet av komponenter i produktionen. Mer information finns i [Bokför komponenter enligt verksamhetens utflöde](production-how-to-flush-components-according-to-operation-output.md).

I avancerade lagerkonfigurationer där platser kräver både val och leveranser måste du använda sidan **Dist.lager plockning** för att få komponenter med spolningsmetod inställd på *Manuell*, *Plocka + Framåt*, *Plocka + Bakåt* till produktionsorder. Mer information finns i [Plocka för produktion eller montering i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

I grundläggande lagerkonfigurationer där lagerställe kräver plockningsbearbetning, men inte utleveransbearbetning, använder du sidan **Lagerplockning** för att organisera och registrera plockning av komponenter med bokföringsmetod inställd på *Manuell*. När du registrerar en lagerplockning för en intern operation, bokförs till exempel produktion, förbrukningen av markerade komponenterna samtidigt. Alternativt kan du använda **Lagerrrörelse** med hänvisning till ett källdokument för att föra komponenter med bokföringsmetod inställd på *Manuell*, *Plocka + Framåt*, *Plocka + Bakåt* till produktionsorder.

När produktionsoperationer som integreras med lagerprocesser, antingen per lagerplatser eller av dirigerad artikelinförsel och plockning, används lagerplatsen som komponenterna förbrukas från som den lagerplats som har definierats på varje produktionsorderkomponentrad. Alla nödvändiga komponenter måste vara tillgänglig på lagerplatsen. Annars stoppas manuell eller spolad förbrukning som bokförs för den komponenten.

**Lagerförflyttning** med referenser till källdokumentet och **Dist.lager plockning** kan inte användas för att plocka komponenter med bokföringsmetoder *framåt* och *bakåt*. **Lagerplockning** kan inte användas för att plocka komponenter med någon spolningsmetod än *Manuell* . Om du vill hantera återstående komponenter använder du **Lagerförflyttning** utan hänvisning till ett källdokument. Mer information finns i [Flytta komponenter till ett verksamhetsområde i grundläggande distributionslagerkonfiguration](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

> [!NOTE]  
>  Lagerplockningar, lagerförflyttningar och distributionslagerplockningar har följande viktiga skillnader:  
>   
>  -   När du registrerar en lagerplockning för en intern operation, bokförs till exempel produktion, förbrukningen av markerade komponenterna samtidigt. När du registrerar en lagerförflyttning eller en distributionslagerplockning för en intern operation, registrerar du bara en fysisk transport av nödvändiga komponenter till en lagerplats i verksamhetsområdet utan att bokföra förbrukningen.  
> -   Om du använder lagerplockningar definierar fältet **Lagerställeskod** på en produktionsorderkomponentrad lagerstället *ta* från vilken antalet komponenter minskas när konsumtionen bokförs. Om du använder lagerförflyttningar eller distributionslagerplockningar definierar fältet **Lagerställeskod** på en produktionsorderkomponentrad, lagerstället *plats* i verksamhetsområdet från vilken antalet lagerarbetare måste placera komponenter.  

En systemvillkor för plockning eller flyttning av komponenter för källdokument, är att en utgående distributionslagerkrav finns för att meddela lagerområdet i komponentbehovet. Den utgående distributionslagerförfrågan skapas när produktionsorderns status ändras till Släppt eller när en släppt produktionsordern skapas.  

## <a name="to-pick-production-components-in-basic-warehouse-configurations-using-inventory-pick"></a>Så här plockar du produktionskomponenter i grundläggande distributionslagerkonfiguration med lagerplockning

I grundläggande distributionslagerkonfiguration, där det har angetts att lagerstället ska endast använda plockning samt leverans, kan du välja plockkomponenter på sidan **Lagerplockning**. För mer information, se [Plocka artiklar med lagerplockningar](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **lagerplockning** och väljer sedan relaterad länk.  
2.  Om du vill komma åt produktionsorderns komponenter väljer du åtgärden **Hämta källdokument** och väljer den släppta produktionsordern.  
3.  Utför plockningen och registrera den verkliga plockningsinformationen i fältet **Ant. att hantera**.  
4.  När raderna är färdiga att bokföras klickar du på **Bokför**. Bokföringen skapar de nödvändiga distributionslagertransaktionerna och bokför förbrukningen av artiklarna.  

Du kan också skapa en **lagerplockning** direkt från den släppta produktionsordern. Välj **Skapa lagerartikelinförsel/Plocka/Förflyttning**, välj **Skapa lagerplockning** och välj sedan **OK**-knappen.

Alternativt kan du använda **Lagerförflyttningen** med referens till källdokumentet för att flytta artiklar mellan lagerplatser. Du måste registrera förbrukningen separat. Mer information finns i [Batch-bokföra produktionsförbrukning](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Plocka för montering i en grundläggande lagerkonfiguration.

I avancerad distributionslagerkonfiguration, där lagerställen kräver både plockning och utleveranser måste du använda sidan **dist.lager plockning** för att få komponenter till monteringsordern. Mer information finns i [Plocka för produktion eller montering i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

I grundläggande distributionslagerkonfiguration kan du också plocka för monteringsorder med sidan **Lagertransport**. 

I grundläggande lagerkonfigurationer där lagerstället kräver plockbearbetning men inte leveransbearbetning används sidan **Lagerplockning** också för att plocka, montera och leverera för försäljningsorder där artiklar måste monteras innan de kan levereras. Mer information finns i [hantera artiklar för montering mot kundorder i lagerplockningar](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks) .  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Hantering av artikel för montering mot kundorder i lagerplockningar

Sidan **Lagerplockning** används också för att plocka och leverera för försäljning där artiklar måste vara församlade, innan de kan levereras. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).

Artiklar som ska levereras, inte fysiskt finns i en lagerplats, förrän de är bokförda och församlade som utflöde på en lagerplats i monteringsområdet. Det innebär att plocka artiklar för montering mot kundorder för utleverans följer ett speciellt flöde. Från en lagerplats tar lagerarbetare monteringsartiklarna till ett leveransdocka och bokför sedan lagerplockningen. Bokförda lagerplockningen bokför sedan monteringsutflödet, komponentförbrukningen och utleveransen.

Du kan lägga upp [!INCLUDE[prod_short](includes/prod_short.md)] för att automatiskt skapa en lagertransport, när monteringsartikeln för lagerplockningen skapas. Du anger dessa inställningar genom att välja fältet **skapa transporter automatiskt** på sidan **Monteringsinställningar** Mer information finns i [Flytta komponenter till ett verksamhetsområde i grundläggande lagerstyrning](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Lagerplockningsrader för försäljningsartiklar skapas på olika sätt beroende på om ingen, några eller alla försäljningsradantal monteras mot kundorder.

I vanliga lagerförsäljningar, när du använder lagerplockningar för att bokföra utleveransen av lagerantal, skapas en lagerplockrad eller flera om artikeln ligger i olika lagerställen för varje försäljningsorderrad. Denna plockningsrad baseras på antalet i **Ant. att utleverera**.

I montering mot kundorder försäljning, där hela antalet på försäljningsorderraden är monterad till order, skapas en lagerplockningsrad för det antal. Detta innebär att värdet i fältet Antal att montera är lika med värdet i fältet **Antal att leverera**. Fältet **montering mot kundorder** är markerat på raden.

Om ett monteringsutflöde har angetts för lagerstället, när värdet i fältet **Lagerpl.kod för mont. mot lev.** eller värdet i **Från monteringsplats – kod** i den ordern infogas i fältet **Lagerställeskod** på lagerplockningsraden.

Om ingen lagerställeskod anges på försäljningsorderraden, och ingen monteringsutflöde har angetts för lagerstället, är **Lagerställeskod** på lagerplockningsraden tomt. Lagerarbetaren måste öppna sidan **Lagerställesinnehåll** och markera den lagerplats där monteringsartiklarna är församlade.

I alla scenarier där en del av antalet måste först vara församlad och ett annat ska plockas från lagret, skapas ett minimum på två lagerplockningsrader. En plockningsrad är för antal för montering mot kundorder. Den andra plockningsraden beror på vilka lagerställen som kan uppfylla det återstående antalet från lagret. Lagerställeskoder på de två raderna är ifyllt olika sätt, som beskrivs för de två olika försäljningstyperna. Mer information finns i avsnittet Kombinationsscenarion i [Förstå montering mot order och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Fylla förbrukningslagerstället

Diagrammet visar hur **Lagerställeskod** på produktionsorderkomponentraderna fylls enligt platsinställningen.

![Flödesschema för lagerplats.](media/binflow.png "BinFlow")

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
