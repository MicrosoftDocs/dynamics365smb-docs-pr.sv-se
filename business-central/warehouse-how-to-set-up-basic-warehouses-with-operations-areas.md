---
title: Ställa in grundläggande dist.lager med verksamhetsområden
description: 'Ställ in åtgärder för distributionslager och använd lagerförflyttningar, plockningar och införslar för att flytta varor mellan dem.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '6774, 6775, 6776'
ms.date: 06/25/2021
ms.author: bholtorf
---
# Ställa in grundläggande dist.lager med verksamhetsområden

Om internt verksamhetsområde till exempel produktion eller tillverkning finns i grundläggande distributionslagerkonfiguration, där lagerställen använder **Lagerplats ska finnas** inställningar, och eventuellt fälten **Begär plockning** och **Begär artikelinförsel**, kan du använda följande grundläggande dokument för att registrera lageraktiviteter för internt verksamhetsområde:  

- Sidan **Lagerförflyttning**.  
- Sidan **Lagerplockning**.  
- Sidan **Lagerinförsel**.

> [!NOTE]
> Även om inställningarna kallas **Begär plockning** och **Begär artikelinförsel**, kan du fortfarande bokföra inleveranser och utleveranser direkt från affärskälldokument på platser där du markerar dessa kryssrutor.  

Att använda dessa sidor med intern operation t.ex för att plocka komponenter och flytta till produktionen, måste du följa några eller alla följande steg, beroende på hur mycket kontrollerar du behöver:  

- Aktivera lagerplockningen, flytta och artikelinför dokumenten.  
- Definiera standardlagerplatsstrukturer för komponenter och artiklar, flöde till och från åtgärdsresurser.  
- Göra till- och frånlagerställen som är avsedda för åtgärdsresurser för att förhindra att artiklarna plockas för utgående dokument.

Lagerställeskoder som definierats på lagerställekort anger ett standardlagerflöde för vissa aktiviteter, till exempel komponenter i en monteringsavdelning. Ytterligare funktioner finns för att se till att artiklar inte kan plockas eller flyttas till andra aktiviteter när de placerats på en viss lagerplats. Mer information finns i [Så här skapar du särskilda komponentlagerställen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md#to-create-dedicated-component-bins).

Procedurerna baseras på att ställa in grundläggande av lageraktiviteter kring en produktionsområde. Momentet är liknande för andra verksamhetsområden, t.ex montering, tjänstehantering och projekt.  

> [!NOTE]  
>  I följande procedur här fältet **Lagerplats ska finnas** på lagerställekort markeras som ett villkor, eftersom det betraktas som grund för en nivå i lagerstyrningen.  

## Om du vill aktivera lagerdokument för intern operation aktiviteter

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.
2. Öppna lagerställekortet som du vill ställa in.  
3.  Välj kryssrutan **Dist.lager**, fältet **Begär artikelinförsel** för att visa att när ett inkommande eller en internt källdokument med en lagerställeskod släpps, en lagerartikelinförsel eller en lagertransportdokument kan skapas.  
4.  Välj **Begär plockning** för att visa att när ett utgående eller en internt källdokument med en lagerställeskod skapas, en lagerplockning eller en lagertransportdokument måste skapas.  

## Så här definierar du en standardlagerplatsstruktur i produktionsområdet

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.
2. Öppna lagerstället som du vill ställa in.  
3.  På Snabbfliken **Lagerställen** , i **Öppen prod.lagerplats kod** fältet, ange koden för lagerstället i produktionsområdet med överflöd av komponenter som maskinoperatören kan använda utan att begära en lageraktivitet om att ta dem till lagerstället. Artiklar som placeras på denna lagerplats, används vanligtvis för automatisk bokföring. Det innebär att **Bokföringsmetod** fältet, innehåller **Framåt** eller **Bakåt**.  
4. I fältet **Till prod.-lagerplats – kod** anger du koden för lagerstället i produktionen där komponenter, som plockas för produktion i denna plats, placeras som standard, innan de kan förbrukas. Artiklar som placeras på denna lagerplats, används vanligtvis för förbrukningsbokföring. Det innebär att **Bokföringsmetod** fältet innehåller **Manuell** eller **Plocka + framåt** eller **Plocka + bakåt** för dist.lager plockning och lagerförflyttningar.  

    > [!NOTE]  
    > Om du använder lagerplockningar definierar fältet **Lagerställeskod** på en produktionsorderkomponentrad lagerstället *ta* från vilken antalet komponenter minskas när konsumtionen bokförs. Om du använder lagerförflyttningar definierar fältet **Lagerställeskod** på en produktionsorderkomponentrad, lagerstället *plats* i verksamhetsområdet från vilken antalet lagerarbetare måste placera komponenter.  

5. På Snabbfliken **Lagerställen** , i **Från prod.lagerplats – kod** fältet, ange koden för lagerstället i produktionsområdet där färdiga slutartiklar tas från som standard, när processen omfattar lageraktiviteter. I grundläggande lagerkonfigurationer registreras aktiviteten som en lagerartikelinförsel eller en lagerförflyttning.  

Nu kräver produktionsorderkomponentrader med standardlagerställeskoden att framåtriktade komponenter placeras där. Dock tills komponenterna förbrukas från den lagerplats kan andra komponentbehov väljas eller förbrukas från den lagerstället eftersom de är fortfarande tillgängligt lagerställesinnehåll. Se till att lagerställesinnehållet är bara tillgänglig för det komponentbehov som använder den till produktion-lagerplats genom att välja sidan **Dedikerad** på raden för den lagerställeskoden i **Lagerställen**-fönstret som du öppnar från lagerställekortet.

Diagrammet visar hur **Lagerställeskod** på produktionsorderkomponentraderna fylls enligt inställningen.  

![Flödesschema för lagerplats.](media/binflow.png "BinFlow")

## Så här definierar du en standardlagerplatsstruktur i monteringsområdet

Komponenter för monteringsorder kan inte plockas eller bokföras med lagerplockningar. Använd istället sidan **lagerförflyttning**. Mer information finns i [Plocka för produktion, montering eller projekt i grundläggande distributionslager](warehouse-how-to-pick-for-production.md).

Om plockning- och leveransförsäljningsradantal läggs till i order ska du följa vissa regler när du skapar lagerplockningsraderna. Mer information finns i avsnittet ”Hantera artiklar för montering mot kundorder i lagerplockningar” i [Plocka artiklar med Lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md).

Mer information finns i [Monteringshantering](assembly-assemble-items.md).

### För att ställa in automatiskt skapa en lagertransport, när monteringsartikeln för lagerplockningen skapas.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Monteringsinställningar** och väljer sedan relaterad länk.
2. Markera kryssrutan **Skapa transporter automatiskt**.

### Anger lagerstället i monteringsområdet där komponenter placeras som standard innan de kan förbrukas vid montering.

Värdet i det här fältet infogas automatiskt i fältet **Lagerställeskod** på monteringsorderrader när lagerstället anges i fältet **Platskod** på monteringsorderraden.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.
2. Öppna lagerstället som du vill ställa in.
3. Fyll i fältet **Till monteringsplats – kod**.

### Anger lagerstället i monteringsområdet där slutförda monteringsartiklar bokförs när de monteras mot lager.

Värdet i det här fältet infogas automatiskt i fältet **Lagerställeskod** på monteringsorderhuvuden när platskod anges i fältet **Platskod** på monteringsorderhuvudet.

Lagerställeskoder som definierats på lagerställekort anger ett standardlagerflöde för vissa lageraktiviteter, till exempel konsumtion i en monteringsavdelning. Ytterligare funktioner finns för att se till att artiklar inte kan plockas eller flyttas till andra aktiviteter när de placerats på en standardlagerplats.

> [!NOTE]
> Den här konfigurationen är endast möjlig för lagerställen där fältet Lagerplats ska finnas är markerat.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.
2. Öppna lagerstället som du vill ställa in.
3. Fyll i fältet **Från monteringsplats – kod**.

### Anger lagerstället där slutförda monteringsartiklar bokförs när de monteras mot en kopplad försäljningsorder.

Från den här lagerstället levereras monteringsartiklarna omedelbart, via en lagerplockning, för att uppfylla försäljningsordern.

> [!NOTE]
> Fältet kan inte användas om dirigerad artikelinförsel och plockning används på lagerstället.

Lagerställeskoden kopieras från försäljningsorderraden till monteringsorderhuvudet för att meddela monteringsarbetarna om var utflödet ska placeras inför leveransen. Den kopieras även till lagerplockningsraden för att ange för lagerarbetarna var det ska tas från för leverans.

> [!NOTE]
> Utleveranslagerstället för montering mot kundorder är alltid tom. När du bokför en försäljningsrad för montering mot kundorder justeras lagerställesinnehållet först positivt med monteringsutflödet. Direkt efter justeras det negativt med det levererade antalet.

Värdet i fältet infogas automatiskt i fältet Lagerställeskod på försäljningsorderrader som innehåller ett antal i fältet **Antal att montera mot kundorder** eller om den artikel som ska säljas har **Montering mot kundorder** i fältet **Återanskaffningssystem**.

Om **Lagerpl.kod för mont. mot lev.** är tomt, används fältet **från monteringsplats-kod** i stället. Om båda konfigurationsfälten är tomma används den sista använda lagerstället med innehåll i fältet **Lagerställeskod** på försäljningsorderrader.

Samma lagerställeskod kopieras i sin tur till fältet **Lagerställeskod** på lagerplockningsraden som hanterar utleveransen av antalet för montering mot kundorder. Mer information finns i avsnittet ”Hantera artiklar för montering mot kundorder i lagerplockningar” i [Plocka artiklar med Lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.
2. Öppna lagerstället som du vill ställa in.
3. Fyll i fältet **Lagerpl.kod för mont. mot lev.**.

## För att du ska kunna göra dedikerade komponentlagerställen

Du kan ange att kvantiteter på lagerställen skyddas från plockning för andra krav än krav från det aktuella syftet.

Antalet i lagerställena kan fortfarande reserveras. Därmed ingår antalet i dedikerade lagerställen i fältet **Totalt disponibelt antal** på sidan **Reservation**.

Till exempel skapas en produktionsgrupp med en lagerställeskod i fältet **Till prod.-lagerplats – kod**. Produktionsorderkomponentrader med den här lagerställeskoden kräver att framåtriktade komponenter placeras där. Dock tills komponenterna förbrukas från den lagerplats kan andra komponentbehov väljas eller förbrukas från den lagerstället eftersom de är fortfarande tillgängligt lagerställesinnehåll. Se till att lagerställesinnehållet är bara tillgänglig för det komponentbehov som använder den till produktion-lagerplats genom att välja sidan **Dedikerad** på raden för den lagerställeskoden i **Lagerställen**-fönstret som du öppnar från lagerställekortet.

Att dedikera en lagerplats påminner om funktionen att använda lagerplatstyper, som endast finns i avancerade distributionslager. Mer information finns i [Skapa lagerställen](warehouse-how-to-set-up-bin-types.md).

> [!Caution]
> Artiklar på dedikerade lagerställen skyddas inte när de plockas och förbrukas som produktionskomponenter med sidan Lagerplockning.

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk. Välj lagerstället som du vill uppdatera.  
2.  Välj åtgärden **Lagerställen**.  
3.  Välj **Dedikerad**-fältet för varje Lagerplats som du vill använda exklusivt för vissa interna operationer och där kvantiteten på lagerstället ska reserveras för den interna åtgärd som placerats där.  

> [!NOTE]  
>  lagerstället måste vara tom, innan du kan välja eller ta bort **Dedikerad** fältet.

## Se relaterad [Microsoft utbildning](/training/modules/get-started-warehouse-management/)

## Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
