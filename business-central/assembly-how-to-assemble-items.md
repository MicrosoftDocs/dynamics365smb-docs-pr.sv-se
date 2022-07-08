---
title: Montera Artiklar
description: Om fältet Återanskaffningssystem på artikelkortet innehåller Montering, när standard metoden för att tillhandahålla artikeln är att sammanställa från definierade komponenter.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 13f1a68ebb3c9a16c06cdc0cf9382867403ba5ca
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079252"
---
# <a name="assemble-items"></a>Montera Artiklar

Om fältet **Återanskaffningssystem** på artikelkortet innehåller **Montering**, när standard metoden för att tillhandahålla artikeln är att sammanställa från definierade komponenter och eventuellt med en viss resurs.  

Komponenterna och resurser, som ingår i den här typen av en monteringsartikel, måste definieras i en monteringsstruktur. Mer information finns i [Arbeta med strukturer](inventory-how-work-BOMs.md).  

Monteringsartiklar kan indelas för två olika monteringsprocesser:  

-   Montering mot lager.  
-   Montering mot order.  

Du kan använda **montering mot lager** för de artiklar som du vill att sammanställa framåt av försäljning, till exempel att förbereda för en satskampanj och hålla lagret tills de beställs. Dessa artiklar är vanligtvis standardobjekt som emballerade satser, som du inte erbjuder för att anpassa till kundförfrågningar.  

Du använder vanligtvis **montering mot kundorder** för de artiklar som du inte vill att tillverka, eftersom du förväntar dig att anpassa dem till kundförfrågningar, eller eftersom du vill att minska den bärande kostnaden för lagret, genom att tillhandahålla dem precis i tid. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).  

Mer information om hur du ställer in en monteringsartikel finns i [Förstå montering mot order och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

Dessa inställningsalternativ är standardinställningar som hantera hur försäljning och monteringsorderrader behandlas först. Du kan avgå från dessa standardinställningar och leverera monteringsartikeln på det mest optimal sätt, när du bearbetar en försäljning. Mer information finns i [Så här säljer du lagerartiklar i flöde för montering mot kundorder](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) och [Så här säljer du artiklar för montering mot kundorder och lagerartiklar ihop](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Monteringskomponenterna hanteras på ett speciellt sätt i grundläggande distributionslagerkonfiguration. Mer information finns i avsnittet ”Hantera artiklar för montering mot kundorder i lagerplockningar” i [Plocka artiklar med Lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md).   

I den här proceduren skapar och behandlar du och en monteringsorder för artiklar som monteras mot lager, som innebär utan ett kopplat försäljningsorder. Steget innehåller initialisera monteringsorder, hantera potentiella komponenttillgänglighetsproblem och delvis att bokföra monteringsartikel utflöde.

## <a name="to-assemble-an-item"></a>Om du vill att sammanställa en artikel

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **monteringsorder** och väljer sedan relaterad länk.  
2.  Välj åtgärden **Ny**. Sidan **Ny monteringsorder** öppnas.  
3.  Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  I fältet **Artikelnr** anger du monteringsartikeln du vill beställa. Fältet visar artiklar som har upprättats för montering, vilket innebär att de har monteringsstrukturer tilldelade.  
5.  I **Antal** fältet, ange hur många enheter av artikeln som du vill monteras.  

    > [!NOTE]  
    >  Om en eller flera komponenter inte är tillgängliga för att uppfylla den angivna monteringsartikelantalet på angivna förfallodatum, så öppnas sidan **Monteringsdisposition** fönstret automatiskt för att ange utförlig information om, hur många monteringsartiklar kan monteras baserat på komponenttillgänglighet. Mer information finns i [Visa tillgängliga objekt](inventory-how-availability-overview.md). När du stänger sidan, monteringsorder skapas med disponibla aviseringar på de berörda komponentraderna  

    Monteringsorderrader fylls automatiskt med innehållet av monteringsstrukturen och med rad antal enligt monteringsorderhuvudet.  

    > [!NOTE]  
    >  Om du öppnade sidan **Monteringsdisposition** , när du fyller i monteringsorderhuvudet, varje berörd monteringsorderrad innehåller en **ja** i **Disp.-varning** fältet med en länk till detaljerad dispositionsinformationen. För mer information, se Kontrollera disponibelt. Du kan lösa en komponentdispositionsproblem, genom att skapa startdatum, ersätta komponenten med en annan artikel eller välja en tillgänglig ersättning, om den har definierats.  

6.  I **Antal att montera** fältet, ange hur många enheter för monteringsartikeln som ska bokföras som utflöde nästa gång som du bokför monteringsorder. Antalet, kan vara lägre än värdet i **Antal** fältet för att visa en delleverans utflödesbokföring.  

    > [!NOTE]  
    >  För att se till att komponentförbrukningsbokföring matchar monteringsartikel utflödesbokföringen, innehåller fältet antalet i monteringsorderrader, automatiskt justerade till värde du anger i **Antal att montera** fältet.  
7.  På monteringsorderrader av typen **Artikel** eller **Resurs** i **Antal att förbruka** fältet, ange hur många enheter för monteringsartikeln som ska bokföras som utflöde nästa gång som du bokför monteringsorder.
8.  När du är klar att helt eller delvis bokföra väljer du åtgärden **Bokföra**.  

    > [!NOTE]  
    >  Om varningar fortfarande presenteras i något av monteringsorderrader, bokföringen är spärrad. Ett meddelande om komponenten eller komponenter om inte finns i lager, visas.  

När du bokför har lyckas, monteringsartikeln bokförs som utflöde på den potentiella lagerställekod och lagerställeskod som definieras på monteringsorder. För manuellt skapade monteringsorder kan lagerstället kopieras från fältet **Standardplacering av order** inställningsfältet. För flöde för montering mot kundorder kan lagerställekoden kopieras från försäljningsorderraden.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med strukturer](inventory-how-work-BOMs.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]