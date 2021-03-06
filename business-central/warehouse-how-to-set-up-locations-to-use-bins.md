---
title: Så här ställer du in lagerställen att använda lagerställen | Microsoft Docs
description: Lagerställen representerar den grundläggande lagerstrukturen och används för att lägga förslag om artiklarnas specifika placering av artiklar. När du har skapat lagerställena kan du definiera det innehåll som du vill placera på respektive lagerplats, eller så kan lagerstället fungera som en flytande lagerplats utan att något särskilt innehåll har angetts.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e04ec3be3385b86cfdfb42bffadcdd9730244efc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771632"
---
# <a name="set-up-locations-to-use-bins"></a>Registrera lagerställen för att använda lagerställen
Lagerställen representerar den grundläggande lagerstrukturen och används för att lägga förslag om artiklarnas specifika placering av artiklar. När du har skapat lagerställena kan du definiera det innehåll som du vill placera på respektive lagerplats, eller så kan lagerstället fungera som en flytande lagerplats utan att något särskilt innehåll har angetts.  

Om du vill använda lagerplatsfunktionerna på ett lagerställe måste du först aktivera dessa på kortet **Lagerställe**. Sedan designar du artikelflödet på lagerstället, genom att ange inställningar för lagerställeskoder i fältet som representerar de olika flödena.  

> [!NOTE]  
>  Innan du kan ange lagerställeskoder på lagerställekortet, måste lagerställeskoderna skapas. Mer information finns i [Skapa lagerställen](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a>Så här lägger du upp ett lagerställe för att använda lagerställen  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Platser** och välj sedan relaterad länk.  
2.  Välj lagerstället där du vill använda lagerställen.  
3.  Välj åtgärden **Redigera**.  
4.  Markera fältet **Lagerplats ska finnas** på kryssrutan **Dist.lager**.  
5.  Om du inte använder dirigerad artikelinförsel och plockning för ett lagerställe fyller du i fältet **Standard lagerplatsval** med den metod som ska användas för att tilldela en standardlagerplats till en artikel.  
6.  Öppna kortet för den plats som du vill ställa in lagerställen för.
7.  På snabbfliken **Lagerställen** väljer du de lagerställen som du vill använda som standard för inleveranser, utleveranser samt inkommande, utgående och öppna produktionslagerställen.  
8.  De lagerställeskoder som du fyller i här visas automatiskt i huvudena och på raderna för olika distributionslagerdokument. Standardlagerställena definierar alla start- och slutplaceringar av artiklar i distributionslagret.  
9.  Om du använder dirigerad artikelinförsel och plockning väljer du en lagerplats för distributionslagerjusteringarna. Lagerställeskoden i **Justering lagerställeskod** fältet anger den virtuella lagerplats där avvikelser i lagret registreras, när du registrerar antingen observerade avvikelser som har registrerats i dist.lagerartikeljournalen, eller avvikelser beräknade när du registrerar en fysiskt dist.lager.  
10. Fyll i fälten på snabbfliken **Lagerplatsprinciper** om de är relevanta för distributionslagret. De viktigaste fälten är **Lagerplats kapacitetsprincip**, **Tillåt brytenhet** och **Artikelinförsel mallkod**.  
11. På snabbfliken **Dist.lager** fyller du i fälten **utgående lagerhanteringstid**, **inkommande lagerhanteringstid** och **Baskalenderkod**. Mer information finns i [Så här skapar du baskalendrar](across-how-to-assign-base-calendars.md).

## <a name="filling-the-consumption-bin"></a>Fylla förbrukningslagerstället
Diagrammet visar hur **Lagerställeskod** på produktionsorderkomponentraderna fylls enligt platsinställningen.

![Flödesschema för lagerplats](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Se även
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]