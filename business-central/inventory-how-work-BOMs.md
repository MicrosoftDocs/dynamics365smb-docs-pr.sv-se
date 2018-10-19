---
title: "Så här arbetar du med strukturer för att hantera komponenter | Microsoft Docs"
description: "Du kan skapa en monteringsstruktur eller produktionsstruktur för att ange vilka komponenter eller resurser som krävs för att sätta ihop artiklarna som strukturen representerar."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 44648f9d9cfd9ad2e1ea3589031b6560f4a4dcfb
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="work-with-bills-of-material"></a>Arbeta med strukturer
Du använder strukturlistor (stycklistor) till strukturens överordnade artiklar som monteras eller tillverkas av resurser eller maskin resurserna från komponenter. En monteringsstruktur kan också användas för att sälja en överordnad artikel som byggsatser bestående av dess komponenter.

## <a name="assembly-boms-or-production-boms"></a>Monteringsstrukturer eller produktionsstrukturer
Du använder monteringsorder för att slutboka artiklar från komponenter i en enkel sätt, som kan utföras av en eller flera grundläggande resurser, som inte är maskin- eller produktionsgrupper, eller utan något resurser. Det kan exempelvis vara en monteringsprocess att välja två som vinflaska och en kaffesäck och sedan packa dem som presentartiklar.  

En monteringsstruktur är mycket viktigt som definierar vilka komponentartiklarna ingår i en slutartikelmontering mot kundorder, och vilka resurser som används för att monterar monteringsartikeln. När du anger monteringsartikeln och ett antal i huvudet för en ny monteringsorder, fylls monteringsorderraderna i automatiskt enligt monteringsstrukturen med en monteringsorderrad per komponent eller resurs. Mer information finns i [Monteringshantering](assembly-assemble-items.md).

I det här avsnittet beskrivs monteringsstrukturer.

Du använder produktionsorder för att slutboka artiklar från komponenter i en komplex behandling som kräver en verksamhetsföljd och en produktions- eller maskingrupper, som representerar produktionskapaciteterna. Det kan till exempel vara att en produktionsprocess klippa ut stålplattor i en operation, svetsar dem i nästa operation och färga slutartikeln i den senaste operationen. Mer information finns i [Tillverkning](production-manage-manufacturing.md).  

En produktionsstruktur är huvuddata som definierar en produktionsartikel och komponenter som ingår i den. För monteringsartiklar måste produktionsstrukturen godkännas och tilldelas produktionsartikeln innan den kan användas i en produktionsorder. När du anger produktionsartikeln på en produktionsorderrad, antingen manuellt eller genom att uppdatera order, då blir produktionsstrukturinnehållet produktionsorderkomponenterna. För mer information, se [Skapa produktionsstrukturer](production-how-to-create-production-boms.md).  

Begreppet av resurser i produktionen är mycket mer avancerad än i monteringshantering. Produktionsgrupper och maskingrupper fungerar som resurser, och produktionssteg representeras av operationer som tilldelas resurser i produktionsstrukturer. Mer information finns i [Skapa verksamhetsföljder](production-how-to-create-routings.md).

Både monteringsorder och produktionsorder kan kopplas direkt till försäljningsorder. Du kan dock endast använda monteringsorder att anpassa slutartikeln direkt för en kundförfråga med försäljningsordern.

## <a name="to-create-an-assembly-bom"></a>Skapa en monteringsstruktur
Om du vill definiera en överordnad artikel som består av andra artiklar eller resurser som krävs för att montera den överordnade, måste du skapa en monteringsstruktur.  

Monteringsstrukturer innehåller vanligtvis artiklar men kan också innehålla en eller flera resurser som krävs för att utföra monteringsarbetet.

Monteringsstrukturer kan ha flera nivåer, vilket innebär att en komponent på monteringsstruktur kan vara en monteringsartikel själv. I så fall innehåller fältet **Monteringsstruktur** på monteringsstrukturraden **Ja**.

Särskilda krav gäller artiklarna på moneringsstrukturer med avseende på tillgängligheten. Mer information finns i avsnittet "För att visa tillgängligheten för en artikel efter dess användning i monteringsstrukturer" i [Visa artikeldisposition](inventory-how-availability-overview.md).

Det finns två delar för att skapa en monteringsstruktur:
- Skapa en ny artikel
- Ange strukturem för monteringsartikeln.

1. Skapa en ny artikel. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

    Fortsätt med att ange komponenter eller resurser i monteringsstrukturen.  
2. I fönstret **artikelkort** för en monteringsartikel väljer du åtgärden **montering** och väljer sedan åtgärden **Monteringsstruktur**.
3. I fönstret **Monteringsstruktur** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Att visa komponenter i en monteringsartikel som dras in enligt strukturen
Från fönstret **Monteringsstruktur** kan du öppna ett separat fönster som visar komponenterna och resurserna med indrag enligt deras strukturplats under monteringsartikeln.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.
2. Öppna kortet för monteringsartikeln. (Fältet **Monteringsstruktur** i fönstret **artiklar** innehåller **Ja**.)
3. I fönstret **artikelkort** väljer du åtgärden **montering** och väljer sedan åtgärden **Monteringsstruktur**.
4. I fönstret **Monteringsstruktur** väljer du åtgärden **visa struktur**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Ersätta monteringsartikeln med de komponenter som ingår i rader
Du kan använda en särskild funktion för att ersätta raden för monteringsartikeln med nya rader för dess komponenter från alla försäljnings- och inköpsdokument som innehåller en monteringsartikel. Den här funktionen används, till exempel för att sälja komponenter som en sats som motsvarar monteringsartikeln.

**Varning**: när du har använt funktionen **Expandera struktur**, kan du inte enkelt ångra det. Om du vill ångra åtgärden måste du ta bort försäljningsorderraderna som representerar komponenterna och sedan skriva en försäljningsorderrad för monteringsartikeln på nytt.

Följande procedur är baserad på en försäljningsfaktura. Samma steg gäller för andra försäljningsdokument och alla inköpsdokument.

1. Välj ikonen **Söka efter sida eller rapport** i det övre högra hörnet, gå till **Försäljningsfakturor** och välj sedan relaterad länk.
2. Öppna en försäljningsfaktura som innehåller en rad för en monteringsartikel.
3. Välj rad för en monteringsartikel och radåtgärden **Expandera struktur**.

Alla fält på försäljningsfakturaraden för den monterade artikeln avmarkeras utom fälten **artikel** och **beskrivning**. Ifyllda försäljningsfakturarader infogas för komponenter och eventuella resurser som utgör grunden för monteringsartikeln.

**Observera**: funktionen Expandera struktur finns också i fönstret **Monteringsstruktur**.

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Beräkna standardkostnaden för monteringsartikel
Du beräknar styckkostnaden för en monteringsartikel genom att summera styckkostnaden för varje komponent och resurs i artikelns monteringsstruktur.

Du kan även beräkna och uppdatera standardkostnaden för en eller flera artiklar i fönstret **Standardkostnadsformulär**. För mer information, se [Uppdateras standardkostnader](finance-how-to-update-standard-costs.md).  

Styckkostnaden för en monteringsstruktur är alltid lika med de sammanlagda styckkostnaderna för komponenterna, inklusive andra monterinhsstrukturer och resurser.

1. Välj ikonen **Söka efter sida eller rapport** i det övre högra hörnet, gå till **Artiklar** och välj sedan relaterad länk.
2. Öppna kortet för monteringsartikeln. (Fältet **Monteringsstruktur** i fönstret **artiklar** innehåller **Ja**.)
3. I fönstret **artikelkort** väljer du åtgärden **montering** och väljer sedan åtgärden **Monteringsstruktur**.
4. I fönstret **Monteringsstruktur** kan du välja åtgärden **beräkna standardkostnad**.
5. Markera ett av alternativen och klicka på **OK**.

|Alternativ |Description |
|-------|------------|
|**Högsta nivå**|Beräknar monteringsartikelens standardkostnad som den totala kostnaden för alla inköpta eller monterade artiklar på den monteringsstrukturen oberoende av alla underliggande monteringsstrukturer.|
|**Alla nivåer**|Beräknar monteringsartikelns standardkostnad som summan av: 1) den beräknade kostnaden för alla underliggande monteringsstrukturer på monteringsstrukturen. 2) Kostnaden för alla inköpta artiklar i monteringsstrukturen.|



Kostnaderna för de artiklar som utgör monteringsstrukturen kopieras från komponentens artikelkort. Kostnaden för varje artikel multipliceras med det aktuella antalet, och totalkostnaden visas i fältet **Styckkostnad** på artikelkortet för monteringsartikeln.

## <a name="see-also"></a>Se även
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Visa artikeldisposition](inventory-how-availability-overview.md)     
[Lagersaldo](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

