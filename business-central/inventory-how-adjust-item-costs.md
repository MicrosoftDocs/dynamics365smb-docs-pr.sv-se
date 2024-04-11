---
title: Så här justerar du kostnader för artiklar manuellt
description: Du kan justera lagervärderingen för en artikel med hjälp av FIFO-eller genomsnittskostnadsmetoderna när kostnaderna för produkter ändras.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'cost adjustment, cost forwarding, costing method, inventory valuation, costing'
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="adjust-item-costs"></a>Justera artikelkostnader

Kostnaden för en artikel (lagervärde) som du köper och senare säljer kan ändras under dess livstid, eftersom till exempel en fraktkostnad läggs till dess inköpkostnad när du har sålt artikeln. Kostnadsjustering är speciellt relevant i situationer där du säljer varor, innan du fakturerar inköpet av dessa varor. För att alltid ha rätt lagervärde måste bör regelbundet justera artikelkostnaderna. Korrekta kostnader bidrar till att säkerställa att försäljnings- och vinststatistiken är aktuell och ekonomiska KPI-er är korrekta. Mer information finns i [Designdetaljer: kostnadsjustering](design-details-cost-adjustment.md).

Värdet i fältet **Styckkostnad** på artikelkortet enligt standardkostnaden för artiklar där värderingsprincipen Standard används. För artiklar där någon annan värderingsprincip används, beräknas värdet baserat på beräkningen av lagersaldot (fakturerade kostnader och förväntade kostnader) dividerat med lagersaldot. Mer information finns i avsnittet [Förstå Styckkost. beräkningstyp](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

I [!INCLUDE[prod_short](includes/prod_short.md)] justera artikelkostnaderna automatiskt varje gång en lagertransaktion uppstår till exempel när bokföring av en faktura för en artikel.

Du kan också manuellt justera kostnaderna för en eller flera artiklar. Till exempel är manuella justeringar användbara när du vet att artikelkostnaderna ändras av andra skäl än artikeltransaktioner.

Artikelkostnaderna justeras av FIFO eller metoden Genomsnittskostnad beroende på ditt val i assisterad inställningsguide för **Konfigurera mitt företag** på fältet **Värderingsprincip** på artikelkortet. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).  

För FIFO-kostnadsmetoden är en artikels enhetskostnad det faktiska värdet av varje mottagande av varan. Lager värderas genom att anta att de första artiklarna in i lagret säljs först.

Om du använder metoden Genomsnittskostnad beräknas en artikels styckkostnad som den genomsnittliga styckkostnaden vid varje tidpunkt efter ett inköp. Lager värderas med förutsättningen att alla lagerartiklar säljs samtidigt. För artiklar som avänder den här värderingsprincipen kan du välja fältet **Styckkostnad** på artikelkortet för att visa tidigare transaktioner som genomsnittskostnaden beräknas från.

Kostnadsjustering bearbetar endast värdetransaktioner som inte är justerade. I en situation där ändrade inkommande kostnader måste vidarebefordras till relaterade avgående transaktioner skapas nya justeringsvärdetransaktioner. Justeringsvärdetransaktionerna baseras på informationen i de ursprungliga värdetransaktionerna, men innehåller justeringsbeloppet. Funktionen Kostnadsjustering använder bokföringsdatumet för den ursprungliga värdetransaktionen om inte det datumet infaller i en avslutad lagerperiod. Om så är fallet används startdatumet för nästa öppna lagerperiod. Om lagerperioder inte används definieras datumet i fältet **Tillåt bokföring fr.o.m.** på sidan **Redovisningsinställningar** när justeringstransaktionerna bokförs.

## <a name="to-adjust-item-costs-manually"></a>Så här justerar du artikelkostnader manuellt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Justera kostn. – artikeltrans.** och välj sedan relaterad länk.
2. På sidan **Justera kost. – artikeltrans** kan du ange vilka artiklar som du vill justera kostnader för.
3. Välj knappen **OK**.

## <a name="to-make-general-changes-in-the-direct-unit-cost"></a>Så här gör du generella ändringar i inköpspris

Om du vill ändra inköpspriset för flera olika artiklar kan du använda batchjobbet **Justera artikelkost./priser**.  

När batch-jobbet körs ändras innehållet i fältet **Inköpspris** på artikelkortet. Innehållet i fältet ändras på samma sätt för alla artiklar eller för de artiklar du valt. Värdet i fältet multipliceras med en justeringsfaktor som du anger.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Justera artikelkostnad/pris** och väljer sedan relaterad länk.  
2. I fältet **Justeringsfält** anger du vilket artikelfält eller lagerställeskortfält du vill justera.  
3. I fältet **Justeringsfaktor** anger du den faktor som ska justera värdet. Ange t. ex. **1,5** för att minska värdet med 50 %.  
4. På snabbfliken **Artikel** ställer du in filter för att ange till exempel vilka artiklar som ska hanteras med batch-jobbet.  
5. Välj **OK**.  

## <a name="understanding-unit-cost-calculation"></a>Förstå beräkning av styckkostnad

Värdet i fältet **Styckkostnad** på artikelkortet enligt standardkostnaden för artiklar där värderingsprincipen Standard används. För artiklar där någon annan värderingsprincip används, beräknas värdet baserat på beräkningen av lagersaldot (fakturerade kostnader och förväntade kostnader) dividerat med lagersaldot.  

I de avsnitt som följer beskrivs hur innehållet i fältet **Värderingsprincip** påverkar beräkningen av styckkostnaden vid inköp och försäljningar.  

## <a name="unit-cost-calculation-for-purchases"></a>Beräkna styckkostnad vid inköp

När du köper in artiklar kopieras alltid värdet i fältet **Senaste direkt kostnad** på artikelkortet till fältet **Inköpspris** på en inköpsrad eller till raden **A-pris** på en artikeljournalrad.  

Ditt val i fältet **Värderingsprincip** påverkar hur [!INCLUDE[prod_short](includes/prod_short.md)] beräknar innehållet i fältet **Styckkostnad** på raderna.  

### <a name="fifo-lifo-specific-or-average-costing-methods"></a>FIFO-, LIFO-, Specifika eller Genomsnittliga kostnadsmetoder

[!INCLUDE[prod_short](includes/prod_short.md)] använder följande formel för att beräkna innehållet i fältet **Styckkostnad (BVA)** på inköpsraden eller innehållet i fältet **Styckkostnad**:  

Styckkostnad (BVA) = (Inköpspris – (Rabattbelopp/Antal)) x (1 + Indirekt kostnad %/100) + Overheadkostnad  

### <a name="standard-costing-method"></a>Standardkalkyleringsmetod

Fältet **Styckkostnad (BVA)** på inköpsraden, eller fältet **Styckkostnad** på artikeljournalraden, fylls i med värdet i fältet **Styckkostnad** på artikelkortet. Om du använder standardkostnadsmetoden baseras värdet alltid på standardkostnaden.  

När du bokför inköpet använder styckkostnaden från inköpsraden eller artikeljournalraden till transaktionsrad för den inköpta artikeln. Det visar i artikelns transaktionslista.  

### <a name="all-costing-methods"></a>Samtliga värderingsprinciper

Enhetskostnaden från källdokumentraden används för att beräkna värdet i fältet **Kostnadsbelopp (faktiskt)** om tillämpligt, den **Kost.belopp (faktiskt)** oavsett vilken värderingsprincip som används för artikeln. Kostnaden inkluderas i beräkningen oavsett artikelns värderingsprincip.  

## <a name="unit-cost-calculation-for-sales"></a>Beräkning av styckkostnad vid försäljning

När du säljer artiklar, kopieras styckkostnaden från fältet **Styckkostnad** på artikelkortet till försäljnings- eller artikeljournalraden.  

När du bokför, kopieras styckkostnaden till en rad på försäljningsfakturan. Styckkostnaden visas på artikelns transaktionslista. [!INCLUDE[prod_short](includes/prod_short.md)] använder styckkostnaden från källdokumentraden för att beräkna innehållet i **Kost.belopp (aktuellt)** eller, om tillämpligt, fältet **Kost.belopp(förväntat)** oavsett vilken värderingsprincip som används för artikeln.  

## <a name="track-item-cost-adjustments"></a>Spåra artikelkostnadsjusteringar

Artikelkostnader kan ändras av många anledningar, så det är viktigt att du kan hålla reda på kostnadsjusteringar. Använd sidan **Kostnadsjustering av lager** för att hantera och övervaka kostnadsjusteringsprocessen. På den här sidan visas artiklarna tillsammans med deras kostnadsparametrar och kostnadsjusteringsstatus. Du kan filtrera listan så att den fokuserar på artiklar som behöver justeras eller som är undantagna från kostnadsjusteringsprocessen. Mer information om hur du spårar kostnadsjusteringar finns i [Spåra justeringar av artikelkostnader](finance-track-inventory-costs.md).

## <a name="see-also"></a>Se även

[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Lager](inventory-manage-inventory.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
