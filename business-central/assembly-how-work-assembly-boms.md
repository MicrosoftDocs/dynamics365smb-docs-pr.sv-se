---
title: Arbeta med monteringsstrukturlistor
description: Du kan skapa en monteringsstruktur för att ange vilka komponenter som krävs för att sätta ihop artiklarna som strukturen representerar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'assembly bom, bills of material,'
ms.search.form: '36, 5870, 5872, 5874'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# <a name="work-with-assembly-boms"></a>Arbeta med monteringsstrukturlistor

Du använder strukturlistor (stycklistor) till strukturens överordnade artiklar som monteras från komponenter med liten eller ingen resursanvändning. En monteringsstruktur kan användas till exempel för att sälja en överordnad artikel som ett paket bestående av komponentartiklar.

Använd monteringsorder för att göra färdiga artiklar från komponenter i en process som kan utföras av en eller flera grundläggande resurser, som inte är maskin- eller produktionsgrupper, eller utan något resurser. Det kan exempelvis vara en monteringsprocess att välja två som vinflaska och en kaffesäck och sedan packa dem som presentartiklar.  

En monteringsstruktur är mycket viktigt som definierar vilka komponentartiklarna ingår i en slutartikelmontering mot kundorder, och vilka resurser som används för att monterar monteringsartikeln. När du anger en monteringsartikel och en kvantitet på en monteringsorder fylls monteringsorderraderna i enligt monteringsstrukturen. Ordern har en monteringsorderrad per komponent eller resurs. Läs mer på [Monteringshantering](assembly-assemble-items.md).

[!INCLUDE[prod_short](includes/prod_short.md)] stödjer även produktionsstrukturer. Produktionsstrukturer skiljer sig från monteringsstrukturer genom att använda mer komplexa procedurer, bland annat resursanvändning, produktions-operationsföljd och produktions- eller maskingrupper. Läs mer om skillnaderna i [Arbeta med strukturer](inventory-how-work-BOMs.md) och [Skapa produktionsstrukturer](production-how-to-create-production-boms.md).

## <a name="to-create-an-assembly-bom"></a>Skapa en monteringsstruktur

För att definiera en artikel som består av andra artiklar och kanske resurserna som sammanställer artikeln, måste du skapa en monteringsstruktur.  

Monteringsstrukturer kan ha flera nivåer, vilket innebär att en komponent på monteringsstruktur kan vara en monteringsartikel själv. I så fall innehåller fältet **Monteringsstruktur** på monteringsstrukturraden **Ja**.

Särskilda krav gäller artiklarna på moneringsstrukturer med avseende på tillgängligheten. Läs mer i [För att visa tillgängligheten för en artikel efter dess användning i monteringsstrukturer](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Det finns två delar för att skapa en monteringsstruktur:

- Skapa en ny artikel.
- Ange strukturem för monteringsartikeln.

1. Skapa en ny artikel. Lär dig mer om att [Registrera nya artiklar](inventory-how-register-new-items.md).

   Fortsätt med att ange komponenter eller resurser i monteringsstrukturen.  
2. På sidan **Artikelkort** för en monteringsartikel väljer du åtgärden **Montering** och väljer sedan åtgärden **Monteringsstruktur**.
3. På sidan **Monteringsstruktur** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Monteringsartiklar kan ha varianter, precis som andra artiklar, vilket hjälper dig att hålla listan över tillgängliga produkter kortare. Läs mer om funktioner på [Hantera produktvarianter](inventory-item-variants.md).

## <a name="to-edit-assembly-boms"></a>Så här redigerar du monteringsstrukturer

Du kan när som helst redigera raderna i en monteringsstruktur. Strukturen kan emellertid användas av löpande försäljning eller sammanställningar av det överordnade företaget. Dessa aktiviteter kan påverkas om du ändrar strukturen. Välj åtgärden **Används i** för att se i vilka artiklar den används och sedan om försäljnings- eller monteringsorder kan påverkas.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. Välj värdet **Ja** i kolumnen **Monteringsstruktur**.
3. På sidan **Monteringsstruktur**, välj åtgärden **Redigera lista** och ändra sedan fältet efter behov.

## <a name="to-view-components-and-resources-indented-according-to-the-bom-structure"></a>Visa komponenter och resurser indragna enligt strukturen

Från sidan **Monteringsstruktur** kan du öppna en separat sida som visar komponenterna och resurserna med indrag enligt deras strukturplats under monteringsartikeln.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. Öppna kortet för monteringsartikeln. (Sidan **Monteringsstruktur** på sidan **Artiklar** innehåller **Ja**.)
3. På sidan **Artikelkort** väljer du åtgärden **Montering** och väljer sedan åtgärden **Monteringsstruktur**.
4. På sidan **Monteringsstruktur** väljer du åtgärden **visa struktur**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Ersätta monteringsartikeln med de komponenter som ingår i rader

Du kan använda en särskild åtgärd för att ersätta raden för monteringsartikeln med nya rader för dess komponenter från alla försäljnings- och inköpsdokument som innehåller en monteringsartikel. Den här åtgärden används, till exempel för att sälja komponenter som en sats som motsvarar monteringsartikeln.

Åtgärden **Expandera struktur** finns också på sidan **Monteringsstruktur** som en metod för att visa underordnade artiklar på en monteringsstruktur.

> [!CAUTION]  
> När du har använt åtgärden **Expandera struktur**, kan du inte enkelt ångra det. Om du vill ångra åtgärden måste du ta bort försäljningsorderraderna för komponenterna och sedan skriva en försäljningsorderrad för monteringsartikeln på nytt.

Följande procedur är baserad på en försäljningsfaktura. Samma steg gäller för andra försäljningsdokument och alla inköpsdokument.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsfakturor** och väljer sedan relaterad länk.
2. Öppna en försäljningsfaktura som innehåller en rad för en monteringsartikel.
3. Välj rad för en monteringsartikel och radåtgärden **Expandera struktur**.

Alla fält på försäljningsfakturaraden för den monterade artikeln avmarkeras utom fälten **artikel** och **beskrivning**. Ifyllda försäljningsfakturarader infogas för komponenter och eventuella resurser som utgör grunden för monteringsartikeln.

> [!NOTE]
> Rapporten **Plockningslista efter order** ändras också till att endast visa komponenter. Det innebär att lagerarbetaren kan plocka den överordnade artikeln, monteringsartikeln, inte kommer att se den i plockningslistan. Mer information finns i [Skriv ut plocklistan](sales-how-print-picking-list.md).

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Beräkna standardkostnaden för monteringsartikel

Du beräknar styckkostnaden för en monteringsartikel genom att summera styckkostnaden för respektive komponent och resurs i artikelns monteringsstruktur.

Du kan även beräkna och uppdatera standardkostnaden för en eller flera artiklar på sidan **Standardkostnadsformulär**. Mer information finns i [Uppdatera standardkostnader](finance-how-to-update-standard-costs.md).  

Styckkostnaden för en monteringsstruktur är alltid lika med de sammanlagda styckkostnaderna för komponenterna, inklusive andra monterinhsstrukturer och resurser.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. Öppna kortet för monteringsartikeln. (Sidan **Monteringsstruktur** på sidan **Artiklar** innehåller **Ja**.)
3. På sidan **Artikelkort** väljer du åtgärden **Monteringsstruktur**.
4. På sidan **Monteringsstruktur** kan du välja åtgärden **beräkna standardkostnad**.
5. Markera ett av alternativen och klicka på **OK**.

|Alternativ |Description |
|-------|------------|
|**Högsta nivå**|Beräknar monteringsartikelens standardkostnad som den totala kostnaden för alla inköpta eller monterade artiklar på den monteringsstrukturen oberoende av alla underliggande monteringsstrukturer.|
|**Alla nivåer**|Beräknar monteringsartikelns standardkostnad som summan av:</br></br>* Den beräknade kostnaden för alla underliggande monteringsstrukturer på monteringsstrukturen.</br>* Kostnaden för alla inköpta artiklar i monteringsstrukturen.|

Kostnaderna för de artiklar som utgör monteringsstrukturen kopieras från komponentens artikelkort. Kostnaden för varje artikel multipliceras med det aktuella antalet, och totalkostnaden visas i fältet **Styckkostnad** på artikelkortet för monteringsartikeln.

## <a name="see-also"></a>Se även

[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Hantera produktvarianter](inventory-item-variants.md)  
[Visa artikeldisposition](inventory-how-availability-overview.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med strukturer](inventory-how-work-BOMs.md)  
[Skapa produktionsstrukturer](production-how-to-create-production-boms.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
