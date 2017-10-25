---
title: "Så här flyttar du artiklar ad hoc i grundläggande lagerkonfiguration | Microsoft Docs"
description: "Ibland kan du behöva flytta artiklar mellan interna lagerplatser, inte inleverans eller utleveranslagerplatser, utan en viss efterfrågan från ett källdokument. Du kan utföra dessa ad hoc-transporter, till exempel, kan du ordna om distributionslagret, för att få artiklarna till område, eller flytta ytterligare artiklar till och från en produktionsområde utan ett systemsamband med produktionsorderkälldokumentet."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 38361c04f4ede35afd20e1fe84128fcdbfe104d0
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-move-items-ad-hoc-in-basic-warehouse-configurations"></a>Så här flyttar du artiklar ad hoc i grundläggande lagerkonfiguration
Ibland kan du behöva flytta artiklar mellan interna lagerplatser, inte inleverans eller utleveranslagerplatser, utan en viss efterfrågan från ett källdokument. Du kan utföra dessa ad hoc-transporter, till exempel, kan du ordna om distributionslagret, för att få artiklarna till område, eller flytta ytterligare artiklar till och från en produktionsområde utan ett systemsamband med produktionsorderkälldokumentet.  

I grundläggande distributionslagerkonfiguration, dvs lagerställen som använder **Lagerplats ska finnas** inställningsfältet, och möjligen **Begär plockning** och den **Begär artikelinförsel** inställningarna, kan du registrera ad hoc-transporter utan källdokument på följande sätt:  

    - Med **Internförflyttning** fönstret.  
    - Med fönstret **Artikelgrupperingsjournal**.  

> [!NOTE]  
>  I avancerad lagerkonfiguration, dvs lagerställen som använder **Dirigerad art.inf. och plock.** inställningsfältet använder du **Transportförslag** fönstret eller **Intern Dist.lager plockning** eller **Intern Dist.lager art.införsel** fönstren för flytta artiklar som är ad hoc mellan lagerplatser.  

## <a name="to-move-items-as-an-internal-movement"></a>Så här flyttar du artiklar som en internförflyttning  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Interntransport** och välj sedan relaterad länk.  
2.  Fyll i fältet **Nr** på snabbfliken **Allmänt** . Fyll Nr fälten, antingen genom att lämna fältet eller genom att välja **AssistEdit** för att välja nummer i nummerserien.  
3.  I **Lagerställekod** fältet, ange det lagerställe där transporten ska utföras.  

    Om lagerstället lagts upp som din standardplats som distributionslageranvändare, infogas lagerställekod i automatiskt.  
4.  I **Till lagerplatskod** fältet, ange en kod för den lagerplats som du vill flytta artikeln till. För produktionen kan detta vara till exempel en öppen produktionslagerplatskod som har angetts på lagerställekortet eller i produktionsgruppen.  
5.  I **Förfallodatum** fältet, ange det datum då transporten måste ha slutförts.  
6.  På snabbfliken **Rader** väljer du fältet **Artikelnr** för att öppna fönstret **Lagerplatsinnehåll lista** och välj sedan artikeln som ska flyttas baserat på dess tillgänglighet i lagerplatserna. Det går också att välja **Hämta lagerplatsinnehåll** för att fylla i interförflyttningsrader baserat på dina filter. Mer information finns i beskrivningen för åtgärden **Hämta lagerplatsinnehåll**.   

    När du har valt artikel innehåller fältet **Från lagerplatskod** automatiskt enligt valt lagerplats, men du kan ändra den till en annan lagerplats där artikeln är tillgänglig.  

    > [!NOTE]  
    >  Eftersom **Artikelnr** fältet, och **Från lagerplatskod** fältet är kopplade, deras värden kan ändras oberoende av varandra, när du redigerar endera fältet.  

    Fältet **Till lagerplatskod** fylls i med värdet som du har angett i huvudet, men du kan ändra koden på raden till en annan lagerplatskod som är inte spärrad, eller hängivet till särskilt ändamål. Se Dedikerad för mer information om batch-jobb avseende att skapa lagerplatser.  
7.  Ange det antal som ska flyttas i **Antal** fältet, när du har definierat lagerplatser som du vill flytta artikeln till och från.  

    > [!NOTE]  
    >  Antalet måste vara tillgängligt i fältet Från lagerplatskod.  

8.  Är du klar att bearbeta internförflyttningen, välj åtgärden **Skapa lagerförflyttning**.  

    > [!NOTE]  
    >  När du har skapat lagerförflyttningen, tas rad för interntransport bort.  

    Du utför resten av ad hoc-flyttningen i **Lagertransport** fönstret, på samma sätt som du skulle för en transport baserat på källdokument. För mer informatio, se [Så här: Flytta komponenter till ett operationsområde i grundläggande distributionslagerkonfiguration](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Så här flyttar du artiklar med artikelgrupperingsjournalen
Du kan registrera flyttning av objekt genom att gruppera de lagerplatskoder som finns i stället för att använda dokument för distributionslagertransport. Mer information finns i [så här: Inventera, justera och gruppera lager](inventory-how-count-adjust-reclassify.md).   
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artikelgrupperingsjournal** och välj sedan relaterad länk.  
2.  Definiera vilka lagerplatser som du vill flytta artiklar till och från på varje journalrad, genom att fylla i **Lagerplatskod** och **Ny lagerplatskod** fältet.  

    1.  Om du vill flytta hela innehållet från en lagerplats till en annan lagerplats väljer du åtgärden **Hämta lagerplatsinnehåll**.  
    2.  Fyll i filter för att hitta den lagerplats vars innehåll du vill flytta och klicka på **OK**. Journalraderna fylls i med innehållet av lagerplatsen.  
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
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

