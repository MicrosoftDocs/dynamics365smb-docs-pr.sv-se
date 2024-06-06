---
title: Monteringshantering
description: Lär dig stödja produkter till kunderna genom att kombinera komponenter i enkla processer utan att använda produktionsfunktioner.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/26/2024
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.service: dynamics-365-business-central
---
# <a name="assembly-management"></a>Monteringshantering

Företag kan stödja produkter till kunderna genom att kombinera komponenter utan att använda produktionsfunktioner. Funktioner för att montera artiklar integreras med relaterade funktioner som försäljning, planering, reservationer och lagerstyrning.  

En monteringsartikel är en säljbar artiklar som innehåller en monteringsstruktur. Om du vill lära dig mer om monteringsstrukturer går du till [Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md).

Monteringsorder är interna order, precis som produktionsorder. Använd monteringsorder för att hantera monteringsprocesser och för att koppla försäljningsbehov med lageraktiviteter. Monteringsorder avser både produktion och förbrukning vid bokföring. Monteringsorderhuvud påminner om utflödesjournalrader. Monteringsorderrader påminner om förbrukningsjournalrader.  

Du kan använda en just-in-time inventeringsstrategi och anpassa produkter för att uppfylla kundernas önskemål. Monteringsorder kan skapas automatiskt och länkas när du skapar en försäljningsorderrad. Länken mellan försäljningsbehov och monteringsleverans öppnar upp flera affärsmöjligheter när du behandlar försäljningsorder:

* Anpassade monteringsartiklar i farten.
* Utlova leveransdatum efter komponent tillgänglighet.
* Bokför produktion och leverans av den sammansatta artikeln direkt från deras försäljningsorder.

Om du vill veta mer om att sälja monteringsartiklar går du till [Sälja artiklar monterade på order](assembly-how-to-sell-items-assembled-to-order.md).  

Rader på försäljningsorder kan innehålla artiklar som ska plockas från lager och artiklar som ska monteras för ordern. Antalet för montering mot kundorder har företräde framför lagerkvantiteter i delleveranser. För att lära dig mer om att sälja lager och monteringsartiklar, gå till [Kombinationsscenarier](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

När antalet för montering mot kundorder är redo att utlevereras kan en lageranställd bokföra en lagerplockning för försäljningsorderraderna. När du bokför en lagerplockning utförs några saker:

* Skapa en lagerförflyttning för komponenterna
* Bokför monteringsutflödet och försäljningsorder utleveransen.

Om du vill lära dig mer om montering mot kundorder och lagerplockning gå till [Hantering av montering mot kundorder med lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

I följande tabell beskrivs en serie uppgifter, med länkar till de artiklar där de beskrivs.

|**Om du vill**|**Se**|  
|------------|-------------|  
|Mer information om montering av artiklar för försäljningsorder och lagring.|[Förstå montering mot kundorder och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Använd lagerställekort och i lagerinställningar för att definiera hur artiklar överförs till och från montering.|[Ställa in grundläggande dist.lager med verksamhetsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Gör offert för anpassad monteringsartikel och konvertera sedan offerten till en försäljning när kunden accepterar den.|[Skapa en försäljning för montering mot kundorder](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Kombinera komponenter för att skapa en artikel till order eller lager.|[Montera Artiklar](assembly-how-to-assemble-items.md)|  
|Du kan sälja monteringsartiklar som inte är tillgängliga genom att skapa en länkad monteringsorder för att tillhandahålla hela eller delvisa försäljningsorderantal.|[Sälja en artikel som monterats mot kundorder](assembly-how-to-sell-items-assembled-to-order.md)|
|Om några artiklar för montering mot kundorder redan finns i lager kan du dra av antalet från monteringsordern och reservera det från lagret.|[Sälja lagerartiklar i flöden för montering mot kundorder](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|När monteringsartiklar inte finns i lager använder du en monteringsorder för att ange en del av eller hela antalet.|[Artiklar för montering mot kundorder och lagerartiklar ihop](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Skapa anpassade monteringsartiklar för avropsorder för försäljning innan du skapar försäljningsorder.|[Skapa monteringsorder för avrop](assembly-how-to-create-blanket-assembly-orders.md)|
|Ångra en bokförd monteringsorder, till exempel för att ordern har bokförts med misstag.|[Ångra monteringsboking](assembly-how-to-undo-assembly-posting.md)|
|Lära dig att arbeta med monteringsstrukturer och hur de skiljer sig från produktionsstrukturer.|[Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md)|
|Lära dig mer om bokföring av monteringsförbrukning och utflöde och hur [!INCLUDE [prod_short](includes/prod_short.md)] fördelar artikel- och resurskostnader i redovisningen.|[Designdetaljer: Bokföring av monteringsorder](design-details-assembly-order-posting.md)|  

## <a name="see-also"></a>Se även

[Arbeta med strukturlistor](inventory-how-work-BOMs.md)  
[Lager](inventory-manage-inventory.md)  
[Översikt över Warehouse Management](design-details-warehouse-management.md)
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)  
<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
<!-- [Walkthrough: Selling, Assembling, and Shipping Kits](walkthrough-selling-assembling-and-shipping-kits.md)   -->
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
