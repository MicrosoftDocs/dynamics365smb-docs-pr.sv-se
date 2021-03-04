---
title: Hantera momssatsändringar | Microsoft Docs
description: Lära dig hur du kan utfärda ändringsverktyget för momssats i Dynamics 365 Business Central.
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.workload: na
ms.search.keywords: VAT, VAT rate, posting, tax, value-added tax
ms.date: 10/01/2020
ms.author: andregu
ms.openlocfilehash: 9d01d332457d85c0450cdf98c79778b18eba304e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746797"
---
# <a name="managing-vat-rate-changes"></a>Hantera momssatsändringar

Momssatser kan ändras beroende på lokal lagstiftning. Alla ändringar av moms påverkar data i [!INCLUDE[prod_short](includes/prod_short.md)] oavsett om momssatsen sänks, höjs eller tas bort. Moms kopplas till många olika enheter i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel kunder, leverantörer, artiklar, resurser, artikelomkostnader och redovisningskonton. Ändringar i momssatser sker vanligtvis vid ett visst datum, från vilket ställe du måste ha ändrat momsinställningarna, bokföringsmallarna o.s.v. för att se till att nya försäljningsorder och inköpsorder skapas med den nya momssatsen.

## <a name="changing-vat-rates"></a>Ändra momssatser

Det bästa sättet att hantera en ändring av momssats är att bokföra och stänga öppna order och andra dokument innan momssatsen växlar datum för att säkerställa att dessa ändringar inte påverkas av ändringen. Det här är den enklaste metoden som gör det möjligt att starta nya order och dokument med den nya momssatsen.

Följande tillvägagångssätt föreslås för att hantera ändring av momssats

1. Bokföra och avsluta öppna order, journaler och andra dokument före växeldatumet. Du kan vänta efter växeldatumet så länge du inte lägger till några nya rader och se till att giltighetsdatumet infaller före växeldatumet.  
2. Skapa den nya momsinställningen.  
3. Gör momsväxeln för entiteter (relevanta kunder, leverantörer, artiklar och så vidare).  
4. På växlingsdatumet för momssatsen skapar du nya dokument som kommer att använda den nya kursen.  


> [!NOTE]  
> Vi uppdaterar för närvarande momssats ändringsverktyget. De funktioner som beskrivs nedan kanske inte stämmer överens med funktionaliteten i miljön. Uppdateringen utförs före den 1 juli 2020 och kommer inte att vara en vanlig månatlig uppdatering. I stället uppdateras alla miljöer automatiskt (snabb korrigering). När uppdateringen har slutförts visas inte längre meddelandet.  

## <a name="the-vat-rate-change-tool"></a>Ändringsverktyget för momssats

Ändringsverktyget för momssats kan hjälpa till med konvertering av momssatser på huvuddata, journaler och order. Detta är användbart om du vill omvandla moms på huvuddata enklare eller om du har order som du inte kan stänga före växeldatumet och som kommer att bearbetas under en längre tidsperiod och på så sätt korsa momssatsens växeldatum. Det finns vissa begränsningar i ändringsverktyget för momssats.

## <a name="understanding-the-vat-rate-conversion-process-and-limitations"></a>Förstå begränsningarna för konverteringen av momssatsen

Verktyget för momsändring utför momssatskonvertering för huvuddata, journaler och order på olika sätt. De valda huvuddata och journalerna uppdateras med den nya allmänna produktbokföringsmallen eller produktbokföringsmallen för moms. Om en order har levererats helt eller delvis, kommer de levererade artiklarna behålla den aktuella produktbokföringsmallen eller produktbokföringsmallen för moms. En ny orderrad skapas för de olevererade artiklarna och uppdateras för att stämma med den nuvarande och nya momsen eller allmänna produktbokföringsmallen. Dessutom ska artikelomkostnadsfördelningar, konfigurationsmallar för artiklar, reservationer och artikelspårningsinformation uppdateras. 

På orderrader uppdateras a-priset för alla rader av typen artikel och resurs om de använder priser inklusive moms för artikeln. För andra typer av rader kan det bestämmas om a-priset ska uppdateras eller inte.

Det finns några saker som verktyget inte konverterar:

* Försäljnings- eller inköpsorder och fakturor där leveranser har bokförts. Dessa dokumentet bokförs med hjälp av den aktuella momssatsen.  
* Dokument som har bokförda förskottsfakturor. Du har till exempel gjort eller tagit emot förskottsbetalningar för fakturor som inte har slutförts innan du använder ändringsverktyget för momssats. I det här fallet blir det en differens mellan momsen som har förfallit och momsen som har betalats i förskottsbetalningar när fakturan har slutförts. Ändringsverktyget för momssats hoppar över dessa dokument och du måste uppdatera dem manuellt.  
* Försäljnings- eller inköpsorder med lagerintegrering om de är delvis levererade eller mottagna.  
* Direktutleveranser.
* Specialorder. 
* Monteringsorder.
* Servicekontrakt  
* Kreditnotor.
* Returorder.
* Priser för artiklar (huvuddata)
* Priser på försäljningspriser (huvuddata)
* Rörelsebokföringsmallar för kunder och leverantörer.

### <a name="to-prepare-vat-rate-change-conversions"></a>Så här förbereder du konverteringar av momssatser

Innan du skapar ändringsverktyget för momssats, måste du göra följande förberedelser.

* Om du har transaktioner som används olika satser måste de delas upp i olika grupper, antingen genom att skapa nya redovisningskonton för varje sats eller genom att använda datafilter för att gruppera transaktioner efter sats.  
* Om du skapar nya redovisningskonton, måste du skapa nya generella bokföringsmallar.  
* Om du vill reducera antalet dokumentet som konverteras, bokför så många dokument som möjligt och minska ej bokförda dokument till en minimum.  
* Säkerhetskopiera data.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Så här ställer du in ändringsverktyget för momssats

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för ändring av momssats** och välj sedan relaterad länk.  
2. På snabbflikarna **Huvuddata**, **Journaler** och **Dokument**, välj en bokföringsmall i alternativlistan för nödvändiga fält. För varje grupp kan du välja om du vill konvertera produktbokföringsmallar för moms eller generella produktbokföringsmallar, eller konvertera båda värdena om de är tillgängliga i huvuddataartikeln. För vissa områden kan du också definiera ett filter för att endast konvertera en delmängd av värden, till exempel redovisningskonton. 
3. På snabbfliken **priser inklusive moms** väljer du vilka radtyper på order som du vill uppdatera a-priser för. A-priserna på rader av typen artikel och resurs kommer alltid att uppdateras.

### <a name="to-set-up-product-posting-group-conversion"></a>Så här skapar du konvertering av produktbokföringsmallar

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för ändring av momssats** och välj sedan relaterad länk.  
2. På sidan **Inställningar för ändring av momssats** väljer du åtgärden **Moms prod.bokf.mall, konv.** eller **Produktbokföringsmall, konv**.  
3. I fältet  **Från kod**, ange den aktuella bokföringsmallen.  
4. I fältet **Till kod** anger du den nya bokföringsgruppen.  

### <a name="to-perform-vat-rate-change-conversion"></a>Utföra konvertering för ändring av momssats

Du använder momssatsändringsverktyget till rätta ändringar i standardsatsen för moms. Du utför moms och generella bokföringsmallkonverteringar för att ändra momssatser och underhålla exakt momsrapportering. Beroende på inställningen görs följande ändringar:  

* Moms- och bokföringsmallar konverteras.  
* Ändringar genomförs i redovisningskonton, kunder, leverantörer, öppna dokument, journalrader, o.s.v.  

> [!IMPORTANT]  
> Innan du utför konverteringen av momssats, kan du testa konverteringen. Följ instruktionerna nedan för att göra det, men du måste avmarkera **utför konvertering** och **Ändringsverktyget för momssats har slutförts**. Under testkonverteringen avmarkerades fältet **konverterad** i tabellen **Ändringsloggtransaktion för momssats** och fältet **konverteras datum** i tabellen **Ändringsloggtransaktion för momssats** är tom. Välj **Ändringsloggtransaktion för momssats** för att visa resultatet av testkonverteringen. Kontrollera varje transaktion, innan du utför konverteringen. Kontrollera särskilt transaktioner som använder en gammal momssats.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Ändring av momssats** och väljer sedan länken **Inställningar för ändring av momssats**.  
2. Kontrollera att du har ställt in konverteringen för momsproduktbokföringsmall eller produktbokföringsmall.  
3. Markera kryssrutan **utför konvertering**.  

    > [!IMPORTANT]  
    >  Avmarkera kryssrutan **Ändringsverktyget för momssats har slutförts**. Kryssrutan markeras automatiskt, när konverteringen av momssats slutförs.  

4. Välj åtgärden **Konvertera**.  
5. Välj åtgärden **Ändringsloggtransaktion för momssats** för att visa resultatet av konverteringen.  

> [!IMPORTANT]  
> När konverteringen är klar markeras fältet **konverterad** i tabellen **Ändringsloggtransaktion för momssats** och **konverteras datum** i den **Ändringsloggtransaktion för momssats** fylls i med konverteringsdatumet.  

## <a name="see-also"></a>Se även

[Ställa in moms](finance-setup-vat.md)  
[Ställa in orealiserad mervärdesskatt](finance-setup-unrealized-vat.md)  
[Rapportera moms till skattemyndigheterna](finance-how-report-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Lokal funktionalitet i Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]