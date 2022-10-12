---
title: Sälja en artikel som monterats mot kundorder
description: Om artikeln är inställd på montering mot kundorder förväntas inte artikeln finnas i lager, och den måste monteras särskilt mot en försäljningsorder.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting, substitute items
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 07/29/2021
ms.author: edupont
ms.openlocfilehash: 96186c821c7524b427ba8729e1d4f10c9db60c2b
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606998"
---
# <a name="sell-items-assembled-to-order"></a>Sälja en artikel som monterats mot kundorder

Om det i fältet **Monteringsmetod** på en monteringsartikels artikelkort står **Montering mot kundorder** förväntas inte artikeln finnas i lager, och den måste monteras särskilt mot en försäljningsorder. När du anger en artikel på en försäljningsorderrad skapas en monteringsorder automatiskt och länkas till försäljningsordern.  

> [!NOTE]  
>  Om några artiklar för montering mot kundorder redan finns i lager kan du dra av antalet från monteringsordern och reservera det från lagret. Mer information finns i [Så här säljer du lagerartiklar i flöde för montering mot kundorder](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

I den här proceduren du behandla försäljningen av en artikel som ska monteras enligt de specifikationer som begärts av kunden. Stegen består i att påbörja försäljningsorderraden; att anpassa monteringsartikeln genom att redigera komponenterna och resurserna; att kontrollera tillgängligheten så att ett leveransdatum kan upprättas; och att släppa försäljningsordern så att den kan monteras och levereras direkt.  

> [!NOTE]  
>  I följande procedur ingår inte standardstegen för försäljningsorder före det steg där du anger artikeln för montering mot kundorder på försäljningsorderraden.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Så här säljer du en artikel som monterats mot kundorder

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2.  Skapa en försäljningsorder. Mer information finns i [Sälja produkter](sales-how-sell-products.md).  
3.  I fältet **Nr.** anger du en artikel som lagts upp för montering mot kundorder.  
4.  I fältet **Lagerställekod** anger du från vilket lagerställe som artikeln ska säljas. Monteringsprocessen genomförs där.  
5.  I fältet **Antal** anger du hur många enheter som ska säljas.  

    > [!NOTE]  
    >  Om en eller flera komponenter av det begärda antalet av monteringsartiklar inte är tillgängliga öppnas en sida med en detaljerad tillgänglighetsvarning. För mer information, se Monteringsdisposition.  

    En monteringsorder skapas nu automatiskt och länkas till försäljningsorderraden. Förfallodatumet för monteringsordern synkroniseras med utleveransdatumet på försäljningsorderraden.  

    Antalet som ska säljas kopieras till fältet **Antal att montera mot kundorder**. Med denna artikelinställning förväntas hela antalet på försäljningsraden monteras mot kundorder. Du kan minska antalet för montering mot kundorder, t. ex. om du vet att vissa artiklar redan är tillgängliga. Mer information finns i [Så här säljer du lagerartiklar i flöde för montering mot kundorder](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6.  Om du vill återspegla att kunden vill ha ytterligare en artikel i en monterad artikel, väljer du på snabbfliken **Rader**, sedan åtgärden **Rad**, åtgärden **Montering mot kundorder** och väljer sdan åtgärden **Montering mot kundorderrader** om du vill visa och ändra standardkomponenterna för montering. Alternativt kan du välja fältet **Antal att montera mot kundorder**.  
7.  Skapa en ny rad av typen **Artikel** för det begärda ytterligare innehållet för den monterade artikeln på sidan **Montering mot kundorderrader**. Raden representerar en extra komponent för montering.  

    Du kan också anpassa ordern genom att öka antalet av en standardartikel i den monterade artikeln. Du kan göra det om du ökar värdet i fältet **Antal per** på den specifika monteringsorderraden.  

    > [!NOTE]  
    >  Sidan **Montering mot kundorderrader** innehåller bara de grundläggande fält som en säljare förväntas använda för att anpassa komponentlistan, lägga till artikelspårningsnummer eller lösa problem med komponenttillgänglighet. Om du vill se mer information om monteringsorder, t. ex. startdatum, ska du välja åtgärden **Visa dokument**. Då öppnas en fullständig vy av monteringsordern som är kopplad till försäljningsorderraden. Du kan inte ändra innehållet av de flesta fält på monteringsorderhuvudet, och du kan inte bokföra monteringsutflöde därifrån, eftersom du måste använda leveransbokföring av försäljningsorderraden.  
    >   
    >  På huvudet av de kopplade monteringsorderna kan bara fältet **Startdatum** ändras så att det snabbt gör det möjligt för monteringsarbetare att ange ett datum som är tidigare än förfallodatumet, när de ska påbörja processen. Alla fält på raderna i den kopplade monteringsordern kan ändras så att lagerarbetare kan ange förbrukningssiffror under processen.  

8.  Granska och svara på problem med komponenttillgänglighet. Du kan till exempel välja ett tillgängligt ersättningsobjekt.  
9. Stäng sidan **Montering mot kundorderrader**. Den kopplade monteringsordern är nu redo att börja montera de anpassade artiklarna efter förfallodatum.  
10. I försäljningsordern väljer du åtgärden **Släpp** om du vill meddela monteringsavdelningen att monteringsprocessen kan börja.  
11. I monteringsavdelningen ska du utföra de steg av montering av de artiklar som säljs i den här proceduren. Mer information finns i [Montera artiklar](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Kom ihåg att artikelersättningar inte automatiskt gör att en artikel ersätts av en annan artikel, till exempel när du skapar en försäljningsorder eller i en strukturlista. Istället kommer du att aviseras om att en ersättning är tillgänglig för dig.

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft-utbildning](/training/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md)  
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
