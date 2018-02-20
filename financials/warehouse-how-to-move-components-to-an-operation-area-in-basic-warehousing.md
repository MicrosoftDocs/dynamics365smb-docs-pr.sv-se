---
title: "Så här: Flytta komponenter till ett verksamhetsområde i grundläggande lagerkonfiguration | Microsoft Docs"
description: "Om artikeln som behandlar operationer utförs i din distributionslagerplats, kan du behöva flytta artiklar mellan lagerplatser så att det stämmer överens med interna källdokument, till exempel produktion, monterings eller serviceorder på lagerstället."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 111d79755a3141bf4e562de3e99ffc2117d12d16
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Flytta komponenter till ett verksamhetsområde i grundläggande lagerkonfigurationer
Om artikeln som behandlar operationer utförs i din distributionslagerplats, kan du behöva flytta artiklar mellan lagerplatser så att det stämmer överens med interna källdokument, till exempel produktion, monterings eller serviceorder på lagerstället.  

> [!NOTE]  
>  Visa Interntransport för information om att flytta artiklar mellan lagerplatser utan källdokument.  

I avancerade distributionslagerkonfigurationer, som är lagerställen som använder inställningsfältet **Dirigerad art.inf. och plock**, kan du använda fönstret **Transportförslag** och flytta artiklar mellan lagerplatserna. Mer information finns i [Så här flyttar du artiklar i avancerad distributionslagerkonfiguration](warehouse-how-to-move-items-in-advanced-warehousing.md).  

I grundläggande distributionslagerkonfiguration, dvs lagerställen som använder **Lagerplats ska finnas** inställningsfältet, och **Begär plockning** inställningsfältet, kan du registrera transport av artiklar till interna verksamhetsområden baserade på interna källdokument på följande sätt:  

-   Med **lagerförflyttning** fönstret.  
-   med fönstret **Lagerplockning**.  

> [!NOTE]  
>  Lagerplockningar bokför även negativa artikeltransaktionsposter som förbrukning och stöder bara för produktionskomponenter. Mer information finns i lagerplockningar.  

För detaljerad information om lagerförflyttningar se lagerförflyttningar.  

Två olika roller kan skapa den ursprungliga lagerförflyttningen. En monteringsarbetar, till exempel, kan skapa den från en släppt monteringsorder, så att den visar upp i lagerarbetare lista över arbete för att göra. Att skapa en lagerförflyttning för monteringsorderrader, som är klar att ha komponenter transporterade till den angivna lagerplatser, monteringsarbetaren använder **Skapa lagerförflyttning** funktionen.  

En lagerarbetare kan också skapa den, genom att peka på den släppta monteringsorder, i fråga. Beskriv i följande procedur.  

> [!NOTE]  
>  Om transporten är för en monteringsorder där artikeln är satt samman till en försäljningsorder, kan du ange att lagertransportdokumentet skapas automatiskt, när du skapar lagerplockningsdokument som tar den färdiga monteringsartikeln och bokför leveransen. Du anger dessa inställningar genom att välja fältet **skapa transporter automatiskt** i fönstret **Monteringsinställningar**  
>   
>  Mer information om monteringsorder och grundläggande konfigurationer för distributionslager finns i avsnittet ”Hantera artiklar för montering mot kundorderartiklar med lagerplockning” i [Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md).  

Nedan beskrivs proceduren för att skapa en lagerförflyttning från det **Lagertransport** fönstret, genom att referera en släppt monteringsorder som ett källdokument. Proceduren är samma när du vill flytta komponenter för produktionsorder och serviceordern.  

## <a name="to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Så här: Flytta komponenter till ett verksamhetsområde i grundläggande lagerkonfiguration  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lagerförflyttning** och välj sedan relevant länk.  
2.  Fyll i fältet **Nr** på snabbfliken **Allmänt** . . Du kan trycka på RETUR för att välja mellan nummerserier.  
3.  I **Lagerställekod** fältet, ange det lagerställe där transporten utförs.  
4.  Välj åtgärden **Hämta källdokument**. Eller Fyll **Källdokument** fältet och välj sedan **AssistEdit** sökknappen i **Ursprungsnr** fältet.  
5.  Välj monteringsorder, som du vill flytta komponenter för i fönstret **Ursprungsdokument**, och välj sedan **OK** knappen.  

    För varje nödvändig komponent, som kan flyttas, skapas en rad Ta och en Placera rad i fönstret **lagerförflyttning** fönstret. Alla fält utom **Ant. att hantera** fältet är förfyllda enligt källdokumentrader. **Ant. att hantera** fältet är nollställt, tills du anger det antal du faktiskt har flyttats.  

    Du kan ändra lagerplatskoden på en Ta rad men endast utifrån tillgänglighet. Om du väljer den **AssistEdit** knappen i **Lagerplatskod** fältet på en Ta rad, **Lagerplatsinnehåll** fönstret öppnas och endast visar den lagerplats där komponenten är tillgänglig.  

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

