---
title: Så här beräknar du lagerplatsåteranskaffning | Microsoft Docs
description: Om lagerstället är inställt på dirigerad artikelinförsel och plockning, beaktas artikelinförsel prioriteter av mallen för lagerstället när införsel av inleveranser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 626e023d97c869d9d0fe63346053ecb42120a0ee
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782740"
---
# <a name="calculate-bin-replenishment"></a>Beräkna lagerplatsåteranskaffning
Om lagerstället är inställt på dirigerad artikelinförsel och plockning, beaktas artikelinförsel prioriteter av mallen för lagerstället när införsel av inleveranser. Prioriteter innehåller minimal och maximal kvantitet av lagerställesinnehåll, som har kopplats till en viss lagerplats, och lagerplatsordningarna. Om artiklar anländer i fast takt fylls därför de plocklagerställen på som används mest allt eftersom de töms.  

Inleveranser anländer dock inte alltid i en stadig takt. Ibland köps artiklar in i större kvantiteter så att företaget kan få rabatt, eller så att produktionsenheten kan producera mycket av en artikel för att få en låg styckkostnad. Då kan det ta ett tag innan artiklarna inlevereras på nytt i distributionslagret, och distributionslagret behöver regelbundet transportera artiklar till plocklagerställen från volymlagret.  

Det kan även vara så att ett nytt parti förväntas inom kort och därför behöver volymlagret tömmas på artiklar innan de nya varorna anländer.  

Slutligen gäller att om du har definierat volymlagerställen med enbart lagerplatstypåtgärden **Artikelinförsel**, d.v.s. åtgärden **Plocka** inte är markerad, måste du alltid fylla på plocklagerställena eftersom lagerställen av artikelinförseltyp inte föreslås för en plockning från lager.  

## <a name="to-replenish-pick-bins"></a>Så här fyller du på plocklagerställen  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Transportkalkylark** och välj sedan relaterad länk.  
2.  Välj åtgärden **Beräkna lagerplatsåteranskaffning** för att öppna sidan för rapportbegäran.  
3.  Fyll i sidan för begäran om batch-jobb för att begränsa omfattningen av de påfyllningsförslag som kommer beräknas. Du kanske är mest intresserad av särskilda artiklar, zoner eller lagerställen.  
4.  Välj **OK**. Rader skapas för de påfyllningstransporter som måste utföras enligt de regler som har angetts för lagerställena och lagerställesinnehållet, d.v.s. artiklar på lagerställen.  
5.  Om du vill utföra alla påfyllningsförslag klickar du på åtgärden **Skapa transport**. Lagerpersonalen kan nu hitta instruktionerna under menyobjektet **Transport**, utföra dem och registrera dem.  
6.  Om du endast vill utföra vissa förslag tar du bort de rader som är mindre viktiga och skapar sedan en transport.  

Nästa gång som du beräknar lagerplatspåfyllning återskapas de förslag som du har tagit bort, om de fortfarande är aktuella.  

> [!NOTE]  
>  Om följande villkor är uppfyllda för en artikel:  
>   
>  -   artikeln har ett utgångsdatum,  
> -   Fältet **Plocka enligt FEFO** på lagerställekortet är markerat och  
> -   Du använder funktionen **Beräkna lagerplatsåteranskaffning**  
>   
>  då innehåller fälten **Från zon** och **Från lagerplats** inga värden. Detta beror på att algoritmen som används för att beräkna varifrån artiklarna ska transporteras endast utlöses när du aktiverar funktionen **Skapa transport**.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Plockning med FEFO](warehouse-picking-by-fefo.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]