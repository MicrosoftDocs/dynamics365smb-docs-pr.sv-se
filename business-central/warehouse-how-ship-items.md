---
title: Så här utlevereras artiklar | Microsoft Docs
description: Beroende på konfigurationen av lagret, kan du antingen registrera utleverans på relaterade avgående affärsdokumentet, till exempel försäljningsorder, direkt eller använda distributionslagerutleveransdokument som följer ett arbetsflöde och integreras i olika lageraktiviteter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/03/2020
ms.author: sgroespe
ms.openlocfilehash: 65ae47563a55e94a726a2608c71718beedba2ceb
ms.sourcegitcommit: ca5bf1d934997ef8c0bc9f8ab0e5568f0ed42fa4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/06/2020
ms.locfileid: "3535371"
---
# <a name="ship-items"></a>Leverera artiklar

När artiklarna utlevereras från ett distributionslager som har ställts in för utleveransbearbetning kan du bara registrera utleveransen med relaterade dokument, till exempel en försäljningsorder, en serviceorder, inköpsreturorder eller en order för avgående överföringar.

När du utlevererar artiklar från ett distributionslagret som har ställt in utleveransbearbetning kan du bara leverera artiklar baserat på källdokument som andra företagsenheter har släppt till distributionslagret för åtgärder.

> [!NOTE]
> Om distributionslagret använder direktutleveranser och lagerplatser, kan du för varje rad visa hur många artiklar som har placerats i direktutleveranslagerplatserna. Programmet beräknar antalet automatiskt när fälten i utleveransen uppdateras. Om det rör sig om de artiklar som ingår i den utleverans du förbereder, kan du skapa en plockning för alla raderna och därefter färdigställa utleveransen. Mer information finns i [Artiklar för direktutleverans](warehouse-how-to-cross-dock-items.md).

## <a name="to-ship-items-with-a-sales-order"></a>För att utleverera artiklar med en försäljningsorder.

Nedan beskrivs hur du levererar artiklar från en försäljningsorder. Stegen är liknande för inköpsreturorder, serviceorder och utgående överföringsorder.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.
2. Öppna en befintlig försäljningsorder eller skapa en ny. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
3. Ange hur många enheter som har levererats i fältet **Ant. att utleverera**.

    Värdet i fältet **Utlevererat antal** uppdateras i enlighet därmed. Om detta är en delutleverans och värdet är lägre än värdet i fältet **antal**.
4. Välj åtgärden **Bokföra**.

> [!NOTE]
> Om organisationen inte använder försäljningsorder antar den att när du bokför försäljningsfakturan [!INCLUDE [prodshort](includes/prodshort.md)] att du har levererat hela antalet. Om det strider mot hur organisationen fungerar rekommenderar vi att du använder försäljningsorder och registrerar leveranser enligt vad som beskrivs i den här artikeln.

## <a name="to-ship-items-with-a-warehouse-shipment"></a>För att utleverera artiklar med en lagerutleverans.

Först kan du skapa ett utleveransdokument från ett källdokument för företag. Sedan kan du välja de angivna artiklarna för utleverans.

### <a name="to-create-a-warehouse-shipment"></a>Skapa en distributionslagerutleverans.

Medarbetare som är ansvarig för utleveransen skapar en distributionslagerutleverans. I följande procedur beskrivs hur du skapar utleverans manuellt i standardversionen av [!INCLUDE[prodshort](includes/prodshort.md)], men organisationen kanske har automatiserat en del av processen, till exempel med hjälp av handburna eller monterade skannrar som stöds av externa leverantörer.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Distributionslagerutleveranser** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  

    Fyll i fälten på snabbfliken **Allmänt**. När du hämtar källdokumentrader, kopieras delar av informationen i huvudet till varje rad.  

    För dirigerad artikelinförsel och plockning: om lagerstället har en standardzon och standardlagerplats för utleveranser fylls fälten **Zonkod** och **Lagerplatskod** i automatiskt. Du kan dock ändra fälten vid behov.  

    > [!NOTE]  
    > Om du vill utleverera artiklar med klasskoder för distributionslager som skiljer sig från klasskoderna för lagerplatsen i fältet **Lagerplatskod** i dokumenthuvudet, måste du ta bort innehållet i fältet **Lagerplatskod** i huvudet innan du hämtar källdokumentets rader för artiklarna.  
3. Välj åtgärden **Hämta källdokument**. Sidan **Källdokument** öppnas.

    Från en ny eller öppen lagerutleverans kan du använda sidan **Filter att hämta ursprungsdok.** för att hämta de släppta källdokumentraderna som anger vilka artiklar som ska utlevereras.

    1. Välj åtgärden **Filter för att hämta urspr.dok.**.  
    2. Du skapar ett nytt filter genom att ange en beskrivande kod i fältet **Kod** och väljer sedan åtgärden **Ändra**.  
    3. Definiera vilken typ av källdokumentrader som du vill hämta genom att fylla i relevanta filterfält.  
    4. Välj åtgärden **Kör**.  

    Alla relaterat källdokumentrader, som uppfyller filtervillkorna, infogas nu på sidan **Dist.lager utleverans** som du aktiverade från filterfunktionen.  

    Filterkombinationerna, vilka du definierar, sparas på sidan **Filter att hämta ursprungsdok.** tills nästa gång du behöver den. Du kan skapa ett obegränsat antal filterkombinationer. Du kan ändra villkor när som helst, genom att välja åtgärden **Ändra**.

4. Välj det källdokument som du vill utleverera artiklar för och klicka på knappen **OK**.  

Raderna i källdokumentet visas på sidan **Dist.lager utleverans**. **Ant. att utlevereras** är ifyllt med utestående antal på respektive rad, men du kan ändra antalet som behövs. Om du tar bort innehållet i fältet **Lagerplatskod** på snabbfliken **Allmänt** innan du hämtar raderna måste du fylla i en lämplig lagerplatskod på varje utleveransrad.  

> [!NOTE]  
> Det går inte att utleverera fler artiklar än antalet, i **Utestående ant.** på källdokumentraden. Om du vill utleverera fler artiklar, hämtar du ett annat källdokument som innehåller en rad för artikeln, genom att använda filterfunktionen för att hämta källdokument med aktuell artikel.  

När du har alla rader som ska utlevereras kan du skicka raderna som lagerpersonalen ska plocka.

### <a name="to-pick-and-ship"></a>Så här plockar och utlevererar du artiklar

Vanligtvis skapar en lagerarbetare ansvarig för plockning ett plockningsdokument eller öppnar ett redan skapat plockningsdokument.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Distributionslagerutleveranser** och välj sedan relaterad länk.
2. Välj dist.lager utleverans som du vill plocka för och välj sedan åtgärden **Skapa plockning**.
3. Fyll i fälten på sidan och sedan välj **OK** knappen. De angivna dokumenten för distributionslagertransport har skapats.

    Du kan också öppna en befintlig dist.lager plockning.
4. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Plockningar** och välj sedan relaterad länk. Välj Dist.lager plockning som du vill arbeta med.

    Om distributionslagret är konfigurerat att använda lagerplatser har plockningsraderna omvandlats till åtgärdsrader för Ta och Placera.

    Du kan sortera raderna, tilldela en anställd plockningen, använda ett brytenhetsfilter, om du använder dirigerad artikelinförsel och plockning, samt skriva ut plockningsinstruktionerna.

5. Utför den faktiska plockningen av artiklarna och placera dem på angiven utleveranslagerplats, eller i utleveransområdet, om du inte använder lagerplatser.
6. Välj **Registrera plockning**.

    Fälten **Ant. att utleverera** och **Dokumentstatus** i leveransdokumentets huvud uppdateras. De artiklar som du har plockat är inte längre tillgängliga för plockning för andra utleveranser eller för interna operationer.
7. Skriv ut leveransdokumenten, förbered godspaketen och bokför utleveransen.

Mer information om hur du plockar för utleveranser finns i [Plocka artiklar för Dist.lager utleverans](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Du kan också använda plockningskalkylarket för att kombinera flera plockningsinstruktioner till en enda instruktion (för flera utleveranser) och på så sätt optimera plockningen i distributionslagret. Mer information finns i [Planera plockning i kalkylark](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Om du väntar på att vissa artiklar ska anlända till distributionslagret, och du använder funktionerna för direktutleverans, beräknar [!INCLUDE[d365fin](includes/d365fin_md.md)] det antal artiklar som finns på lagerplatsen för direktutleverans för varje utleverans- eller plockningsförslagsrad. Det här fältet uppdateras varje gång du lämnar och öppnar utleveransdokumentet eller kalkylarket. Mer information finns i [Artiklar för direktutleverans](warehouse-how-to-cross-dock-items.md).

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
