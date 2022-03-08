---
title: 'Så här: Flytta komponenter till ett verksamhetsområde i grundläggande lagerkonfiguration | Microsoft Docs'
description: Om artikeln som behandlar operationer utförs i din distributionslagerplats, kan du behöva flytta artiklar mellan lagerplatser så att det stämmer överens med interna källdokument, till exempel produktion, monterings eller serviceorder på lagerstället.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: fc3211ef873e3cf31768210e9659ae54dd59d10d
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882884"
---
# <a name="move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Flytta komponenter till ett verksamhetsområde i grundläggande lagerkonfigurationer
Om artikeln som behandlar operationer utförs i din distributionslagerplats, kan du behöva flytta artiklar mellan lagerplatser så att det stämmer överens med interna källdokument, till exempel produktion, monterings eller serviceorder på lagerstället.  

> [!NOTE]  
>  Visa Interntransport för information om att flytta artiklar mellan lagerplatser utan källdokument.  

I avancerade distributionslagerkonfigurationer, som är lagerställen som använder inställningsfältet **Dirigerad art.inf. och plock**, kan du använda sidan **Transportkalkylark** och flytta artiklar mellan lagerplatserna. Mer information finns i [Så här flyttar du artiklar i avancerad distributionslagerkonfiguration](warehouse-how-to-move-items-in-advanced-warehousing.md).  

I grundläggande distributionslagerkonfiguration, dvs lagerställen som använder **Lagerplats ska finnas** inställningsfältet, och **Begär plockning** inställningsfältet, kan du registrera transport av artiklar till interna verksamhetsområden baserade på interna källdokument på följande sätt:  

-   Med sidan **lagerförflyttning**.  
-   Med sidan **Lagerplockning**.  

> [!NOTE]  
>  Lagerplockningar bokför även negativa artikeltransaktionsposter som förbrukning och stöder bara för produktionskomponenter. Mer information finns på sidan lagerplockningar.  

För detaljerad information om lagerförflyttningar se sidan lagerförflyttningar.  

Två olika roller kan skapa den ursprungliga lagerförflyttningen. En monteringsarbetar, till exempel, kan skapa den från en släppt monteringsorder, så att den visar upp i lagerarbetare lista över arbete för att göra. Att skapa en lagerförflyttning för monteringsorderrader, som är klar att ha komponenter transporterade till den angivna lagerplatser, monteringsarbetaren använder **Skapa lagerförflyttning** funktionen.  

En lagerarbetare kan också skapa den, genom att peka på den släppta monteringsorder, i fråga. Beskriv i följande procedur.  

> [!NOTE]  
>  Om transporten är för en monteringsorder där artikeln är satt samman till en försäljningsorder, kan du ange att lagertransportdokumentet skapas automatiskt, när du skapar lagerplockningsdokument som tar den färdiga monteringsartikeln och bokför leveransen. Du anger dessa inställningar genom att välja fältet **skapa transporter automatiskt** på sidan **Monteringsinställningar**  
>   
>  Mer information om monteringsorder och grundläggande konfiguration av lagerstyrning finns [Hantering av artikel för montering mot kundorder i lagerplockningar](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Nedan beskrivs proceduren för att skapa en lagerförflyttning från sidan **Lagertransport** genom att referera en släppt monteringsorder som ett källdokument. Proceduren är samma när du vill flytta komponenter för produktionsorder och serviceordern.  

## <a name="to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Så här: Flytta komponenter till ett verksamhetsområde i grundläggande lagerkonfiguration  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **lagerförflyttning** och välj sedan relevant länk.  
2.  Fyll i fältet **Nr** på snabbfliken **Allmänt** . . Du kan trycka på RETUR för att välja mellan nummerserier.  
3.  I **Lagerställekod** fältet, ange det lagerställe där transporten utförs.  
4.  Välj åtgärden **Hämta källdokument**. Eller Fyll **Källdokument** fältet och välj sedan **AssistEdit** sökknappen i **Ursprungsnr** fältet.  
5.  På sidan **Ursprungsdokument** väljer du monteringsorder som du vill flytta komponenter för och väljer sedan knappen **OK**.  

    För varje nödvändig komponent, som kan flyttas, skapas en rad Ta och en Placera rad på sidan **lagerförflyttning** fönstret. Alla fält utom **Ant. att hantera** fältet är förfyllda enligt källdokumentrader. **Ant. att hantera** fältet är nollställt, tills du anger det antal du faktiskt har flyttats.  

    Du kan ändra lagerplatskoden på en Ta rad men endast utifrån tillgänglighet. Om du väljer den **AssistEdit** knappen i **Lagerplatskod** fältet på en Ta rad, sidan **Lagerplatsinnehåll** öppnas och endast visar den lagerplats där komponenten är tillgänglig.  

    Du kan inte ändra lagerplatskoden på ett ställe rad. Endast lagerplatskod som definieras på komponentraden i källdokumentet accepteras. Det principer som stöder rollen som begär en komponent, som är en monteringsarbetare i den här proceduren, vet var en komponent måste placeras. Om du vill placera komponenter i en annan lagerplats, måste du först ändra lagerplatskoden på komponentraden och sedan skapa lagerförflyttning raderna på nytt.  
6.  I **Ant. att hantera** fältet ange hela eller delkvantiteten du faktiskt har flyttats. Värdet för Ta och Placera raderna måste vara samma. Annars kan du inte registrera transporten.  

    > [!NOTE]  
    >  Som i andra lageraktiviteter, kan du dela upp raden plats, genom att välja åtgärden **Åtgärder** och sedan välja åtgärden **Dela rad**. I så fall måste summan av de två kluvna placeringsraderna vara samma antal som på Ta raden.  

7.  När du är Klar att registrera omplaceringar, som du har utfört, välj åtgärden **Registrera lagertransport**.  

    Dist.lager transaktioner är skapat att visa att komponenterna finns nu på lagerplatser som har angetts på monteringsorderrader.  

    > [!NOTE]  
    >  Till skillnad från när du vill flytta komponenter med en lagerplockning, förbrukning inte bokförs när du registrerar en lagerförflyttning. Det steg, måste utföras separat genom att bokföra monteringsorderns utflödet och förbrukning. För mer information, se montera order.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
