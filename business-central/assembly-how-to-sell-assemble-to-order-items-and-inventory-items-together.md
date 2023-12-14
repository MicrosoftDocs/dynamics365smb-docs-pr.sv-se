---
title: Artiklar för montering mot kundorder och lagerartiklar ihop
description: Om en del av artikel för montering mot lager inte är tillgänglig kan du skapa en monteringsorder för återstående antal.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Artiklar för montering mot kundorder och lagerartiklar ihop

Om fältet **Monteringsmetod** på en monteringsartikels artikelkort innehåller **Montering mot lager** förutsätter processen för försäljningsorder att artikeln redan monterats och kan plockas från lagret, om den är tillgänglig. Därför skapas inte monteringsorder automatiskt och länkas till försäljningsorderraden. Men om en del eller hela antalet inte är tillgängligt kan du skapa en monteringsorder för återstående antal. För att göra det fyller du i fältet **Antal att montera mot kundorder** försäljningsorderraden. Denna inställning gör att du kan montera artikeln mot ordern även om det har lagts upp för montering mot lager.  

Du har liknande flexibilitet när du säljer artiklar med montering mot kundorder och en del av antalet redan finns i lager. Du ska dra av kvantiteten från monteringsordern. Mer information om att sälja lagerartiklar finns i [Sälja lagerartiklar i flöden för montering mot kundorder](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
> Vissa regler gäller för fältet **Ant. att utleverera** på försäljningsorderrader som innehåller en kombination av antal i montering mot kundorder och antal i lager. Om du vill veta mer om reglerna går du till [kombinationsscenarier](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

> [!NOTE]  
> I följande procedur ingår inte de steg för försäljningsorder som du bör följa innan du skapar en monteringsorder för antal som inte är tillgängliga.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Så här säljer du artiklar för montering mot kundorder och lagerartiklar ihop

1. På en försäljningsorderrad för en montering mot lagerartikel, ange antal i fältet **Antal** som överstiger lagret. Sidan **Kontrollera disponibelt** visas. Om du vill veta mer om artikeldisposition kan du gå till [Visa artikeldisposition](inventory-how-availability-overview.md).
2. I fältet **Antal att montera mot kundorder** anger du värdet från fältet **Totalt antal**.  
3. Utför eventuella ändringar i monteringskomponenterna. Läs mer på [Sälja artiklar som monterats mot kundorder](assembly-how-to-sell-items-assembled-to-order.md).  
4. Släpp försäljningsordern för att göra artiklarna tillgängliga för plockning och för montering av de artiklar som inte är tillgängliga. Mer information om dessa standardsteg för montering finns i [Montera artiklar](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Fältet **Lagerställeskod** på försäljningsordern kan innehålla värdet från fältet **Lagerpl.kod för mont. mot lev.** eller fältet **Från monteringsplats – kod** på lagerställekortet. I så fall här kan fältet **Lagerställeskod** på försäljningsorderraden vara felaktigt i den här kombinationen av antal av montering mot kundorder och antal av montering mot lager. Det kan vara bra att titta i fältet **Lagerställeskod** och se till att det fungerar för alla antal. Alternativt kan du ange de två olika antalen på separata försäljningsorderrader.  

## <a name="see-also"></a>Se även

[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Warehouse Management – översikt](design-details-warehouse-management.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
