---
title: Plocka för produktion, montering eller jobb i grundläggande distributionslager
description: När distributionslagrets lagerställe kräver att du behandlar plock, men inte utleveranser, använder du sidan Lagerplockning för att registrera plockning av komponenter.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/02/2022
ms.author: bholtorf
ms.openlocfilehash: 859c70ebc51f2649000d41817d173292ed5b0870
ms.sourcegitcommit: b4da421c19c3aa3031b0344ec2829d2038be6642
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617883"
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Plocka för produktion, montering eller jobb i grundläggande distributionslagerkonfigurationer

Hur du för in plockningskomponenter för produktions- eller monteringsorder beror på hur distributionslagret har ställts in som lagerställe. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Plocka komponenter för produktion i en grundläggande lagerkonfiguration.

Om ett lagerställe kräver plockningsbehandling men inte utleveransbehandling kan du använda sidan **Lagerplockning**. På sidan **Lagerplockning** kan du ordna och registrera plockningen av artiklar som har bokföringsmetoden inställd på **Manuell**. När du registrerar en lagerplockning bokförs förbrukningen av plockade komponenter. Du kan även använda **Lagerrrörelse** med hänvisning till ett källdokument för att tilldela komponenter med bokföringsmetod inställd på **Manuell**, **Plocka + Framåt**, **Plocka + Bakåt** till produktionsorder.

Om produktionen integreras med lagerprocesser, genom lagerplatser eller dirigerad artikelinförsel och plockning, förbrukas komponenterna från lagerplatsen på produktionsorderraden. Alla nödvändiga komponenter måste vara tillgänglig på lagerplatsen. Annars stoppas manuell eller spolad förbrukning som bokförs för den komponenten.

> [!NOTE]  
> Lagerplockningar, lagerförflyttningar och distributionslagerplockningar har följande viktiga skillnader:  
>
> - När du registrerar en lagerplockning för en intern operation, bokförs till exempel produktion, förbrukningen av markerade komponenterna samtidigt. När du registrerar en lagerförflyttning eller en distributionslagerplockning för en intern operation, registrerar du bara en fysisk transport av nödvändiga komponenter till en lagerplats i verksamhetsområdet utan att bokföra förbrukningen.  
> - Om du använder lagerplockningar definierar fältet **Lagerställeskod** på en produktionsorderkomponentrad lagerstället *ta* från vilken antalet komponenter minskas när konsumtionen bokförs. Om du använder lagerförflyttningar eller distributionslagerplockningar definierar fältet **Lagerställeskod** på en produktionsorderkomponentrad, lagerstället *plats* i verksamhetsområdet från vilken antalet lagerarbetare måste placera komponenter.  

För att plocka eller flytta komponenter för källdokument måste en utgående distributionslagerbegäran meddelande distributionslagret om behovet av komponenten. Den utgående distributionslagerbegäran skapas när du gör följande:

- Ändrar statusen på en produktionsorder till Släppt.
- Skapar en utsläppt produktionsorder.  

Bokföringsmetoder påverkar också flödet av komponenter i produktionen. Mer information finns i [Bokför komponenter enligt verksamhetens utflöde](production-how-to-flush-components-according-to-operation-output.md). **Lagerförflyttning** med referenser till källdokumentet och **Distributionslagerplockning** kan inte användas för att plocka komponenter med bokföringsmetoder *framåt* och *bakåt*. **Lagerplockning** kan inte användas för att plocka komponenter med någon annan bokföringsmetod än *Manuell* . Om du vill hantera återstående komponenter använder du **Lagerförflyttning** utan hänvisning till ett källdokument. Mer information finns i [Flytta komponenter till ett verksamhetsområde i grundläggande distributionslagerkonfiguration](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

I avancerade lagerkonfigurationer där platser kräver både val och leveranser måste du använda sidan **Dist.lager plockning** för att få komponenter med spolningsmetod inställd på *Manuell*, *Plocka + Framåt*, *Plocka + Bakåt* till produktionsorder. Mer information finns i [Plocka för produktion eller montering i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="to-pick-components-for-production-and-jobs-in-basic-warehouse-configurations"></a>Plocka komponenter för produktion och jobb i grundläggande lagerkonfigurationer

I grundläggande distributionslagerkonfigurationer, där det har angetts att lagerstället endast ska använda plockning, kan du välja plockkomponenter för produktionsaktiviteter och projektplaneringsrader på sidan **Lagerplockning**. För mer information, se [Plocka artiklar med lagerplockningar](warehouse-how-to-pick-items-with-inventory-picks.md).

> [!NOTE]
> Möjligheten att plocka komponenter för projektplaneringsrader har lagts till [!INCLUDE[d365fin](includes/d365fin_md.md)] i utgivningscykel 2 år 2022. Om du vill börja använda funktionen måste en administratör aktivera **Funktionsuppdatering: Aktivera lager- och distributionslagerplockning från Projekt** på sidan **Funktionshantering**.
>
>[!INCLUDE[prod_short](includes/prod_short.md)] använder värdet i fältet **Återstående antal** på projektplaneringsraden när lagerplockningar skapas. Om du vill använda lagerplockningar för projekt måste du aktivera **Tillämpa användningslänk** på sidan **Projektkort** för projektet. På så sätt kan du spåra användningen mot din plan. Om du inte aktiverar detta fortsätter det återstående antalet att vara **0** och lagerplockningen skapas inte. Mer information finns i [Konfigurera projaktanvändningsspårning](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **lagerplockning** och väljer sedan relaterad länk.  
2. Om du vill komma åt produktionsorderns komponenter väljer du åtgärden **Hämta källdokument** och väljer den släppta produktionsordern.  
3. Plocka komponenten och registrera plockningsinformationen i fältet **Ant. att hantera**.  
4. När raderna är färdiga att bokföras klickar du på **Bokför**. Bokföringen skapar de nödvändiga distributionslagertransaktionerna och bokför förbrukningen av artiklarna.  

Du kan också skapa en **lagerplockning** direkt från den släppta produktionsordern. Välj **Skapa lagerartikelinförsel/Plocka/Förflyttning**, välj **Skapa lagerplockning** och välj sedan **OK**-knappen.

Alternativt kan du använda **Lagerförflyttning** med referens till källdokumentet för att flytta artiklar mellan lagerplatser. Du måste registrera förbrukningen separat. Mer information finns i [Batch-bokföra produktionsförbrukning](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Plocka för montering i en grundläggande lagerkonfiguration.

Använd följande sidor för att plocka monteringsorder:

- Sidan **Lagerförflyttning**.
- Om lagerstället kräver plockning men inte leverans, använder du sidan **Lagerplockning** för att plocka, montera och leverera försäljningsorder där artiklar måste vara monterade innan de kan levereras. Mer information finns i [hantera artiklar för montering mot kundorder i lagerplockningar](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks) .  

I avancerad distributionslagerkonfiguration, där lagerställen kräver både plockning och utleveranser måste du använda sidan **dist.lager plockning** för att få komponenter till monteringsordern. Mer information finns i [Plocka för produktion eller montering i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Hantering av artikel för montering mot kundorder i lagerplockningar

Sidan **Lagerplockning** används också för att plocka och leverera för försäljning där artiklar måste vara församlade, innan de kan levereras. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).

Artiklar där montering mot kundorder krävs för leverans anses inte finns i en lagerplats förrän de är monterade och bokförda som utflöde på en lagerplats i monteringsområdet. Därför kommer du att plocka dessa artiklar för leverans efter ett visst flöde. Från en lagerplats tar lagerarbetare monteringsartiklarna till ett leveransdocka och bokför sedan lagerplockningen. Bokförda lagerplockningen bokför sedan monteringsutflödet, komponentförbrukningen och utleveransen.

Du kan lägga upp [!INCLUDE[prod_short](includes/prod_short.md)] för att automatiskt skapa en lagertransport, när monteringsartikeln för lagerplockningen skapas. Du skapar förflyttningar automatiskt genom att välja fältet **Skapa transporter automatiskt** på sidan **Monteringsinställningar**. Mer information finns i [Flytta komponenter till ett verksamhetsområde i grundläggande lagerstyrning](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

[!INCLUDE[prod_short](includes/prod_short.md)] skapar lagerplockningsrader för försäljningsartiklar på olika sätt beroende på om ingen, några eller alla försäljningsradantal monteras mot kundorder.

- I försäljning där du använder lagerplockningar för att bokföra lagerleveranser skapar [!INCLUDE[prod_short](includes/prod_short.md)] en lagerplockningsrad för varje försäljningsorderrad. Om artikeln placeras på olika lagerplatser skapas fler än en rad. Plockningsraderna baseras på antalet i fältet **Ant. att utleverera**.
- I försäljning där hela antalet på försäljningsorderraden är monterad till order, skapas en lagerplockningsrad för det antalet. Värdet i fältet Antal att montera är lika med värdet i fältet **Antal att leverera**. Fältet **montering mot kundorder** är markerat på raden.

Om ett monteringsutflöde har angetts för lagerstället, infogas värdet i fältet **Lagerpl.kod för mont. mot lev.** eller **Från monteringsplats – kod** i den ordern i fältet **Lagerställeskod** på lagerplockningsraden.

Om ingen lagerställeskod anges på försäljningsorderraden, och ingen monteringsutflöde har angetts för lagerstället, är **Lagerställeskod** på lagerplockningsraden tomt. Lagerarbetaren måste öppna sidan **Lagerställesinnehåll** och markera den lagerplats där monteringsartiklarna är församlade.

När en del av antalet måste monteras först och en annan del måste plockas från lagret skapar [!INCLUDE[prod_short](includes/prod_short.md)] minst två lagerplockningsrader. En plockningsrad är för antal för montering mot kundorder. Den andra plockningsraden beror på vilka lagerställen som kan uppfylla det återstående antalet från lagret. Lagerställeskoder på de två raderna är ifyllt olika sätt, som beskrivs för de två olika försäljningstyperna. Mer information finns i avsnittet Kombinationsscenarion i [Förstå montering mot order och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md).

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
