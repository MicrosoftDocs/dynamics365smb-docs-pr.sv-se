---
title: Så här flyttar du artiklar ad hoc i grundläggande lagerkonfiguration | Microsoft Docs
description: Ibland kan du behöva flytta artiklar mellan interna lagerställen, inte inleverans eller utleveranslagerställen, utan en viss efterfrågan från ett källdokument. Du kan utföra dessa ad hoc-transporter, till exempel, kan du ordna om distributionslagret, för att få artiklarna till område, eller flytta ytterligare artiklar till och från en produktionsområde utan ett systemsamband med produktionsorderkälldokumentet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 926d7076ba8b9ae78f718afcab434d012d885233
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756223"
---
# <a name="move-items-ad-hoc-in-basic-warehouse-configurations"></a>Flytta artiklar ad hoc i grundläggande lagerkonfigurationer
Ibland kan du behöva flytta artiklar mellan interna lagerställen, inte inleverans eller utleveranslagerställen, utan en viss efterfrågan från ett källdokument. Du kan utföra dessa ad hoc-transporter, till exempel, kan du ordna om distributionslagret, för att få artiklarna till område, eller flytta ytterligare artiklar till och från en produktionsområde utan ett systemsamband med produktionsorderkälldokumentet.  

I grundläggande distributionslagerkonfiguration, dvs lagerställen som använder **Lagerplats ska finnas** inställningsfältet, och möjligen **Begär plockning** och den **Begär artikelinförsel** inställningarna, kan du registrera ad hoc-transporter utan källdokument på följande sätt:  

- Med sidan **Intern förflyttning**.  
- Med sidan **Artikelgrupperingsjournal**.  

> [!NOTE]  
>  I avancerad lagerkonfiguration, dvs lagerställen som använder **Dirigerad art.inf. och plock.** inställningsfältet använder du **Transportkalkylark** sidan eller **Intern Dist.lager plockning** eller **Intern Dist.lager art.införsel** för flytta artiklar som är ad hoc mellan lagerställen.  

## <a name="to-move-items-as-an-internal-movement"></a>Så här flyttar du artiklar som en internförflyttning  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Internförflyttning** och välj sedan tillhörande länk.  
2.  Fyll i fältet **Nr** på snabbfliken **Allmänt** . Fyll Nr fälten, antingen genom att lämna fältet eller genom att välja **AssistEdit** för att välja nummer i nummerserien.  
3.  I **Lagerställekod** fältet, ange det lagerställe där transporten ska utföras.  

    Om lagerstället lagts upp som din standardplats som distributionslageranvändare, infogas lagerställekod i automatiskt.  
4.  I **Till lagerställeskod** fältet, ange en kod för den lagerplats som du vill flytta artikeln till. För produktionen kan detta vara till exempel en öppen produktionslagerställeskod som har angetts på lagerställekortet eller i produktionsgruppen.  
5.  I **Förfallodatum** fältet, ange det datum då transporten måste ha slutförts.  
6.  På snabbfliken **Rader** väljer du fältet **Artikelnr** för att öppna sidan **Lagerställesinnehåll lista** och välj sedan artikeln som ska flyttas baserat på dess tillgänglighet i lagerställena. Det går också att välja **Hämta lagerställesinnehåll** för att fylla i interförflyttningsrader baserat på dina filter. Mer information finns i beskrivningen för åtgärden **Hämta lagerställesinnehåll**.   

    När du har valt artikel innehåller fältet **Från lagerställeskod** automatiskt enligt valt lagerplats, men du kan ändra den till en annan lagerplats där artikeln är tillgänglig.  

    > [!NOTE]  
    >  Eftersom **Artikelnr** fältet, och **Från lagerställeskod** fältet är kopplade, deras värden kan ändras oberoende av varandra, när du redigerar endera fältet.  

    Fältet **Till lagerställeskod** fylls i med värdet som du har angett i huvudet, men du kan ändra koden på raden till en annan lagerställeskod som är inte spärrad, eller hängivet till särskilt ändamål. Se Dedikerad för mer information om batch-jobb avseende att skapa lagerställen.  
7.  Ange det antal som ska flyttas i **Antal** fältet, när du har definierat lagerställen som du vill flytta artikeln till och från.  

    > [!NOTE]  
    >  Antalet måste vara tillgängligt i fältet Från lagerställeskod.  

8.  Är du klar att bearbeta internförflyttningen, välj åtgärden **Skapa lagerförflyttning**.  

    > [!NOTE]  
    >  När du har skapat lagerförflyttningen, tas rad för interntransport bort.  

    Du utför resten av ad hoc-flyttningen på sidan **Lagertransport**, på samma sätt som du skulle för en transport baserat på källdokument. För mer information, se [Flytta komponenter till ett verksamhetsområde i grundläggande distributionslagerkonfiguration](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Så här flyttar du artiklar med artikelgrupperingsjournalen
Du kan registrera flyttning av objekt genom att gruppera de lagerställeskoder som finns i stället för att använda dokument för distributionslagertransport. Mer information finns i [Inventera, justera och gruppera om lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md).   
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artikelgrupperingsjnl** och välj sedan tillhörande länk.  
2.  Definiera vilka lagerställen som du vill flytta artiklar till och från på varje journalrad, genom att fylla i **Lagerställeskod** och **Ny lagerställeskod** fältet.  

    1.  Om du vill flytta hela innehållet från en lagerplats till en annan lagerplats väljer du åtgärden **Hämta lagerställesinnehåll**.  
    2.  Fyll i filter för att hitta den lagerplats vars innehåll du vill flytta och klicka på **OK**. Journalraderna fylls i med innehållet av lagerstället.  
3.  Fyll i de återstående fälten på varje journalrad.   
4.  Bokför Grupperingsjournalen  

    > [!NOTE]  
    >  Till skillnad från transportdokument skapar en transportinstruktion som bokförs med grupperingsjournalen, inte ett distributionslagerkrav att utföra den fysiska aktiviteten.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
