---
title: Skapa ett lagerställekort och definiera överföringsflöden (innehåller video)
description: Om du köper, lagrar eller säljer artiklar på mer än en plats eller ett lager, måste du ställa in varje plats med ett lagerställeskort och definiera överföringsflöden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 1d65213d81c2a615481e753adb380675ff2ee691
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940732"
---
# <a name="set-up-locations"></a>Konfigurera platser

Om du köper, lagrar eller säljer artiklar på mer än en plats eller ett lager, måste du ställa in varje plats med ett lagerställeskort och definiera överföringsflöden. [!INCLUDE [prod_short](includes/prod_short.md)] använder platser för att hålla ordning på lagret i både enklare ärenden och i mer komplicerade lagerprocesser.

Du kan sedan skapa dokumentrader för ett visst lagerställe, visa disposition per lagerställe och överföra lager mellan olika lagerställen. Mer information finns i [Administrera projekt](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Lagerställekort

Lagerställekortet anger information om ett lagerställe, till exempel ett distributionslager eller distributionscenter. Du tilldelar varje lagerställe ett namn och en kod som representerar lagerstället. Du kan sedan ange lagerställekoden i andra delar av programmet när du vill registrera transaktioner för ett visst lagerställe.  

Du kan ange information om lagerplatser och lagerprinciper för varje lagerställe. Utifrån de lagerprinciper du väljer kan du välja alternativ på snabbfliken **Lagerplatser** för att definiera vilka lagerplatser som ska användas som standard vid transaktioner. Om du använder riktad artikelinförsel och plockning, kan du använda de flesta alternativen på snabbfliken **Lagerplatsprinciper** för att definiera hur du vill använda de olika avancerade lagerfunktionerna.  

Vissa alternativfält tonas ned och inaktiveras av andra inställningar på sidan **Lagerställekort** för att begränsa konfigurationskombinationer som inte stöds.  

Välj åtgärden **Zoner** eller **Lagerplatser** om du vill visa information om zoner och lagerplatser som har definierats för lagerstället.

### <a name="to-create-a-location-card"></a>Skapa ett nytt lagerställeskort

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. På sidan **Lagerställekort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Upprepa steg 2 och 3 för varje lagerställe där du vill bedriva lagerhållning.

> [!NOTE]  
> Många fält på lagerställekortet hänvisar till hanteringen av artiklar i ingående och utgående lagerprocesser. Fälten är inte relevanta för företag som inte behöver den mer komplicerade distributionslagerfunktionen. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

Du kan ändra konfigurationen av en plats senare, men du kan inte redigera inställningen av lagerställen som har artikeltransaktioner.  

Sedan kan du definiera överföringsflöden mellan lagerställen, om du har flera lagerställen.  

### <a name="to-create-a-transfer-route"></a>Så här skapar du ett överföringsflöde

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **överföringsflöden** och väljer sedan relaterad länk.
2. Alternativt kan du på sidan **Lagerställekort** välja åtgärden **Överföringsflöden**.
3. Välj åtgärden **Ny**.
4. På sidan **Lagerställekort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Du kan nu överföra lagerartiklar mellan två lagerställen. Mer information finns i [Så här överför du lager mellan olika lagerställen](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Lagerställen

Lagerställen representerar den grundläggande lagerstrukturen och används för att lägga förslag om artiklarnas specifika placering av artiklar. När du har skapat lagerplatser kan du definiera det innehåll som du vill placera på respektive lagerplats, eller så kan lagerplatsen fungera som en flytande lagerplats utan att något särskilt innehåll har angetts. Om du hanterar lager i en enklare konfiguration behöver du troligtvis inte lagerplatser.Lagerplatser används främst i grundläggande och förebyggande åtgärder för distributionslager. Om du hanterar lagret i en mer enkel inställning behöver du troligen inte ha några lagerplatser.

Om du vill använda lagerplatsfunktionen på ett lagerställe måste du först aktivera funktionen på kortet **Lagerställe** genom att markera fältet **Lagerplatser obligatoriskt** på snabbfliken **Distributionslager**. Sedan designar du artikelflödet på lagerstället, genom att ange inställningar för lagerställeskoder i fältet som representerar de olika flödena.

> [!NOTE]
> Innan du kan ange lagerställeskoder på lagerställekortet, måste lagerställeskoderna skapas.

Mer information finns i [Skapa lagerställen](warehouse-how-to-create-individual-bins.md) och [Skapa lagerplatstyper](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zoner

Om du vill strukturera lagerplatser under zoner kan du göra det på sidan **Zoner**.

[!INCLUDE [prod_short](includes/prod_short.md)] kopierar de fält som du har skapat för en viss zon till lagerplatserna i zonen. På så sätt kan du fördela en zon till en lagerplats eller en lagerplatsmall (lagerplatsuppläggningsfilter) så fylls flera andra fält i automatiskt.

Du kan dock välja att bara skapa en zon och strukturera distributionslagret enbart med hjälp av lagerplatser. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).  

## <a name="see-also"></a>Se även

[Hantera lager](inventory-manage-inventory.md)  
[Överföra lager mellan olika lagerställen](inventory-how-transfer-between-locations.md)  
[Skapa lagerställen](warehouse-how-to-create-individual-bins.md)  
[Skapa lagerplatstyper](warehouse-how-to-set-up-bin-types.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]