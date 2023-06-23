---
title: Montera Artiklar
description: Lära dig mer om montering mot kundorder och montering mot lager-processer i Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="assemble-items" />Montera Artiklar

Om fältet **Återanskaffningssystem** på artikelkortet innehåller **Montering**, när standard metoden för att tillhandahålla montera den enligt en monteringsstruktur och eventuellt av en specifik resurs. Mer information: [Arbeta med monteringsstruktur](assembly-how-work-assembly-boms.md). Mer information om hur du ställer in en monteringsartikel finns i [Förstå montering mot order och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md).

Monteringsartiklar kan indelas för två olika monteringsprocesser.

|Behandla  |Description  |
|---------|---------|
|Montering mot lager     | Artiklar som du sätter samman och lagrar för framtida försäljning. Till exempel satser för en kommande försäljningskampanj. Artiklarna är inte relaterade till en försäljnings order, inte heller ännu. Dessa artiklar anpassas vanligen inte för kundförfrågningar.        |
|Montering mot kundorder     | Artiklar som du inte vill lagerför. Eftersom de anpassas till exempel efter kundorder eller för att minska lagerbehållningens kostnad. |
  
I den här artikeln beskrivs standardinställningarna för montering mot lager. Det kan finnas andra sätt som passar ditt företag. Mer information finns i [Så här säljer du lagerartiklar i flöde för montering mot kundorder](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) och [Så här säljer du artiklar för montering mot kundorder och lagerartiklar ihop](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Monteringskomponenterna hanteras på ett speciellt sätt i grundläggande distributionslagerkonfiguration. Mer information finns på [Hantering av artikel för montering mot kundorder i lagerplockningar](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

## <a name="to-assemble-an-item-to-stock" />Om du vill att sammanställa en artikel till lager

Följ stegen i proceduren för att montera en artikel på lager. Om du vill veta mer om montering mot kundorder går du till [Sälja artiklar monterade på order](assembly-how-to-sell-items-assembled-to-order.md).

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **monteringsorder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. Sidan **Ny monteringsorder** öppnas.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I fältet **Artikelnr** anger du artikeln du vill montera. Du kan välja artiklar som är inställda för montering och har en monteringsstruktur, eller artiklar utan monteringsstruktur. De senare är användbara för oplanerade monteringar eller scenarier när du vill använda artikel omklassificering och spåra kostnader.  
5. I **Antal** fältet, ange hur många enheter av artikeln som du vill monteras.  

    > [!NOTE]  
    >  Om en eller flera komponenter inte är tillgängliga för att uppfylla kvantiteten på förfallodagen, **Monteringsdisposition** öppnas. På sidan visas hur många monteringsartiklar som kan monteras baserat på komponenttillgänglighet. Läs mer på [Visa artikeldisposition](inventory-how-availability-overview.md). När du stänger sidan, monteringsorder skapas med disponibla aviseringar på raderna för de påverkade komponenterna.  

    Raderna innehåller innehållet i monteringsstrukturen och angivna kvantiteter.  

    > [!NOTE]  
    >  Om du öppnade sidan **Monteringsdisposition** , när du fyller i monteringsorderhuvudet, varje berörd monteringsorderrad innehåller en **ja** i **Disp.-varning** fältet med en länk till detaljerad dispositionsinformationen. <!--check whether this field help is useful For more information, see Check Availability.--> Du kan lösa en komponent tillgänglighetsproblem per:

    > * Senarelägga startdatum.
    > * Ersätta komponenten med ett annat objekt.
    > * Väljer en tillgänglig ersättning om en sådan har definierats.  

6. I **Antal att montera** fältet, ange hur många enheter för monteringsartikeln som ska bokföras som utflöde nästa gång som du bokför monteringsorder. Antalet, kan vara lägre än värdet i **Antal** fältet för att visa en delleverans utflödesbokföring.  

    > [!NOTE]  
    >  För att se till att komponentförbrukningsbokföring matchar monteringsartikel utflödesbokföringen, innehåller fältet antalet i monteringsorderrader, automatiskt justerade till värde du anger i **Antal att montera** fältet.  
7. På monteringsorderrader av typen **Artikel** eller **Resurs** i **Antal att förbruka** fältet, ange hur många enheter för monteringsartikeln som ska bokföras som utflöde nästa gång som du bokför monteringsorder.
8. När du är klar att helt eller delvis bokföra väljer du åtgärden **Bokföra**.  

    > [!NOTE]  
    >  Om varningar fortfarande presenteras i monteringsorderraderna kan du inte bokföra ordern. Ett meddelande om komponenten eller komponenter om inte finns i lager, visas.  

När du bokför har lyckas, monteringsartikeln bokförs som utflöde på den potentiella lagerställekod och lagerställeskod som definieras på monteringsorder. För manuellt skapade monteringsorder kan lagerstället kopieras från fältet **Standardplacering av order** inställningsfältet. För flöde för montering mot kundorder kan lagerställekoden kopieras från försäljningsorderraden.  

## <a name="see-related-microsoft-trainingtrainingpathsassemble-items-dynamics-365-business-central" />Se relaterad [Microsoft-utbildning](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also" />Se även

[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Warehouse Management – översikt](design-details-warehouse-management.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
