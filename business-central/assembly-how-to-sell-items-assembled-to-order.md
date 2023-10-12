---
title: Sälja en artikel som monterats mot kundorder
description: Så här säljer du en artikel som monterats mot kundorder.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting, substitute items'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# Sälja en artikel som monterats mot kundorder

Artiklar som är inställda för montering enligt beställning förväntas inte finnas i lager och kommer att monteras när det ingår i en försäljningsorder. En artikel ställs in för montering mot kundorder när **monteringsmetod** på artikelkortet innehåller **montering mot kundorder**. När du anger en artikel på en försäljningsorderrad skapas en monteringsorder automatiskt och länkas till försäljningsordern.  

> [!NOTE]  
> Om artiklar för montering mot kundorder redan finns i lager kan du dra av antalet från monteringsordern och reservera det från lagret. Läs mer på [Sälja lagerartiklar i flöden för montering mot kundorder](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

I den här proceduren du behandla försäljningen av en artikel som ska monteras enligt de specifikationer som begärts av kunden. Stegen är följande: 

* Skapar försäljningsorderrad.
* Anpassa monteringsartikeln genom att redigera dess komponenter och resurser.
* Kontrollerar tillgänglighet för att upprätta ett leveransdatum.
* Släpper upp försäljningsordern som ska monteras och levereras omedelbart.  

> [!NOTE]  
> I följande procedur ingår inte stegen för att skapa en standard försäljningsorder som sker före det steg där du anger artikeln för montering mot kundorder på försäljningsorderraden. Mer information om hur du skapar försäljningsorder finns på [Sälja produkter med en kundförsäljning](sales-how-sell-products.md).  

## Så här säljer du en artikel som monterats mot kundorder

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Skapa en försäljningsorder. 
3. I fältet **Nr.** anger du en artikel som lagts upp för montering mot kundorder.  
4. I fältet **Lagerställekod** anger du från vilket lagerställe som artikeln ska säljas. Monteringsprocessen genomförs där.  
5. I fältet **Antal** anger du hur många enheter som ska säljas.  

    > [!NOTE]  
    >  Om en eller flera komponenter av det begärda antalet av monteringsartiklar inte är tillgängliga öppnas en sida med tillgänglighetsvarning. <!-- Check whether the field help would be useful. For more information, see Assembly Availability.  -->

    En monteringsorder skapas och länkas till försäljningsorderraden. Förfallodatumet för monteringsordern med utleveransdatumet på försäljningsorderraden.  

    Antalet som ska säljas kopieras till fältet **Antal att montera mot kundorder**. Med denna artikelinställning förväntas hela antalet på försäljningsraden monteras mot kundorder. Du kan minska antalet för montering mot kundorder, t. ex. om du vet att vissa artiklar redan är tillgängliga. Läs mer på [Sälja lagerartiklar i flöden för montering mot kundorder](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6. Om kunden vill ha ytterligare en artikel i en monterad artikel, väljer du på snabbfliken **Rader**, sedan åtgärden **Rad**, åtgärden **Montering mot kundorder** och väljer sdan åtgärden **Montering mot kundorderrader** om du vill visa och ändra standardkomponenterna för montering. Alternativt kan du välja fältet **Antal att montera mot kundorder**.  
7. Skapa en ny rad av typen **Artikel** för den ytterligare monteringskomponenten på sidan **Montering mot kundorderrader**.  

    Du kan också anpassa ordern genom att öka antalet av en standardartikel i den monterade artikeln. Du kan göra det om du ökar värdet i fältet **Antal per** på den specifika monteringsorderraden.  

    > [!NOTE]  
    >  Sidan **Montering mot kundorderrader** innehåller bara de grundläggande fält för att anpassa komponentlistan, lägga till artikelspårningsnummer eller lösa problem med komponenttillgänglighet. Om du vill se mer information om monteringsorder, t. ex. startdatum, ska du välja åtgärden **Visa dokument**. Då öppnas en fullständig vy av monteringsordern som är kopplad till försäljningsorderraden. Du kan inte ändra innehållet i de flesta fält i monteringsorder huvudet, och du kan inte bokföra monteringsutflöde från det. Du måste bokföra utleveransen av försäljningsorderraden.  
    >
    >  I kopplade monterings order kan endast fältet **startdatum** ändras. Om du ändrar startdatum kan monteringsarbetare ange att de påbörjar montering som är tidigare än förfallodatumet. Alla fält på raderna i den kopplade monteringsordern kan ändras så att lagerarbetare kan ange förbrukningssiffror under processen.  

8. Granska och svara på problem med komponenttillgänglighet. Du kan till exempel välja ett ersättningsobjekt.  
9. Stäng sidan **Montering mot kundorderrader**. Den kopplade monteringsordern är nu redo och alla arbetare kan börja montera de anpassade artiklarna.  
10. I försäljningsordern väljer du åtgärden **Släpp** om du vill meddela monteringsavdelningen att monteringsprocessen kan börja. Läs mer på [Montera artiklar](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> artikelersättningar gör inte automatiskt att en artikel ersätts av en annan artikel, till exempel när du skapar en försäljningsorder eller i en strukturlista. Istället kommer du att aviseras om att en ersättning är tillgänglig.

## Se även

[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med monteringsstrukturlistor](assembly-how-work-assembly-boms.md)  
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Warehouse Management – översikt](design-details-warehouse-management.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]