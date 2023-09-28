---
title: Arbeta med Intrastat-rapporter
description: Lär dig hur du rapporterar handel med företag i andra EU-länder/regioner med hjälp av Intrastat-systemet.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
ms.date: 09/02/2022
ms.author: altotovi
---
# <a name="work-with-intrastat-reporting"></a>Arbeta med Intrastat-rapporter

Alla företag i Europeiska unionen (EU) måste rapportera sin handel med andra länder/regioner inom EU. I Sverige måste du rapportera transport av varor till de statistiska myndigheterna varje månad. Intrastat är det system som används för att samla in statistik över varor inom dessa länder/regioner. Du använder **Intrastat-rapport** för att slutföra periodisk rapportering för Intrastat (vanligen månadsvis), samla in, registrera och rapportera handel med varor enligt den lokala regeringens lagstiftning.

Intrastat-rapportering grundar sig på de grundläggande EU-bestämmelser som gäller för alla länder/regioner. I praktiken finns det emellertid vissa skillnader i de enskilda länderna/regionerna. Varje land/region har sina egna regler för exakt vad som ska rapporteras och på vilket sätt.

> [!IMPORTANT]
> I den här artikeln beskrivs den nya Intrastat-upplevelsen som finns tillgänglig i [!INCLUDE[prod_short](includes/prod_short.md)] från och med utgivningscykel 2 år 2022, som innehåller utökade funktioner och [måste vara aktiverad för befintliga företag](finance-how-setup-report-intrastat.md#enable-the-new-intrastat-experience). Kontakta administratören för att aktivera och konfigurera den nya funktionen.
>
> Läs den föregående versionens artikel för Intrastat-inställning och -användning på [Inställning och rapportering av Intrastat](finance-how-setup-report-intrastat-v20.md).

> [!NOTE]
> Intrastat-uppgifter gäller inte förflyttning av tjänster mellan länder/regioner, utan endast varor (artiklar och anläggningstillgångar). Om den lokala regeringen kräver registrering av transport av tjänster mellan länder/regioner kan du göra detta med hjälp av funktionen **Servicedeklaration**.
>
> Vi förväntar oss att funktionen ska vara tillgänglig från november 2022 som en app i [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). För att kunna använda den måste du först installera den på sidan **Tilläggshantering**.

## <a name="fill-in-the-intrastat-report"></a>Fyll i Intrastat-rapporten

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Intrastatlista** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny** för att skapa en ny **Intrastat-rapport**.
3. Om du behöver ange någon intern information om **Intrastat-rapporten** fyller du i denna information i fältet **Beskrivning**.
4. I fältet **Statistisk period** anger du månaden som data ska rapporteras för. Ange perioden som ett fyrsiffrigt tal utan blanksteg eller symboler. Beroende på vilket land/region du använder, anger du månadens namn och sedan året eller tvärtom. Skriv till exempel antingen *2206* eller *0622* för juni 2022.
5. Välj åtgärden **Föreslå rader**. Fälten **Startdatum** och **Slutdatum** innehåller redan de datum som angavs för statistikperioden i Intrastat-rapporthuvudet.
6. I fältet **Omkostnad reglering %** kan du ange ett värde i procent som täcker transport och försäkring. Om du gör detta är innehållet i fältet **Statistiskt värde** i journalen proportionellt sett högre. Men om du vill använda den här funktionen måste du växla fältet **Belopp inklusive artikelomkostnader** till **Ja**.
7. Du kan slutligen ställa in extra konfigurationer på snabbfliken **Ytterligare**:
   1. **Hoppa över omräkning av nollbelopp** för att ange att rader utan belopp inte ska räknas om under batch-jobbet.
   2. **Hoppa över nollbelopp** för att ange att artikeltransaktioner utan belopp inte ska inkluderas i batch-jobbet.
   3. **Visa artikelomkostnad** för att ange om du vill visa direkta kostnader som företaget har kopplat och bokfört som artikelomkostnader.
   4. **Hoppa över icke fakturerade transaktioner** för att ange om artikeltransaktioner som har utlevererats eller inlevererats men ännu inte fakturerats ska utelämnas från processen.
8. Välj **OK** när du vill starta batchjobbet.

När du kör batch-jobbet hämtas alla artikeltransaktioner inom statistikperioden och infogas som rader i **Intrastat-rapporten**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="modify-the-intrastat-report"></a>Ändra Intrastat-rapporten

Om det behövs kan du ändra raderna, men när du ändrar ett värde på Intrastat-rapportraden markeras fältet **Korrigering** automatiskt som **Ja**. Du kan lägga till en ny rad manuellt om det finns en anledning till det. Lägga till en ny rad manuellt:

1. På sidan **Intrastat-rapport** väljer du åtgärden **Ny rad** i snabbfliken **Rader**.
2. Välj **Inleverans** eller **Leverans** i fältet **Typ**.
3. I fältet **Källtyp** väljer du en av källorna: **Artikeltransaktion**, **Anl-transaktion** eller **Projekttransaktion**.
4. Baserat på **Källtyp** i fältet **Artikelnr** kan du välja **Artikel** (i båda fallen **Artikeltransaktion** eller **Projekttransaktion**) eller **Anläggningstillgångar**.
5. Fyll i övriga fält som du behöver för Intrastat-rapportering.

> [!NOTE]
> När du lägger till en ny rad manuellt i Intrastat-rapporten måste fältet **Datum** på raden ligga innanför den **statistiska period** som du har lagt till i huvudet.

## <a name="validate-intrastat-lines"></a>Validera Intrastat-raderna

När du har fyllt i **Intrastat-rapporten** kan du köra åtgärden **Checklisterapport** när du vill kontrollera att all information i **Intrastat-rapporten** är korrekt. Obligatoriska fält som du har angett på sidan **Checklista för Intrastat-rapport** som saknar värden visas i faktaboxen **Fel och varning** på sidan **Intrastat-rapport**.

Kör rapporten **Checklista för Intrastat-rapport** för att kontrollera Intrastat-rader innan de exporteras till det format som krävs. Checken körs inuti **Intrastat-rapporten**.

## <a name="recalculating-weight-or-supplementary-unit-of-measure"></a>Omberäkning av vikt eller extra måttenhet

Om du får felmeddelandet *Raden 'Total vikt' i Intrastat-rapporten får inte vara tom* beror det troligtvis på att du inte har ställt in fältet **Nettovikt** för den använda källan, artikeln eller anläggningstillgången. I det här fallet söker du efter artikel- eller anläggningstillgångskortet och lägger till det nödvändiga värdet. Sedan behöver du bara öppna **Intrastat-rapporten** på nytt och göra så här:

1. Välj åtgärden **Omberäkna vikt/kompletterande måttenhet** för att omberäkna **Total vikt** och/eller **Kompletterande antal**.
2. Välj något av följande alternativ:

    1. **Vikt** – om du endast vill beräkna om den **totala vikten**, utifrån aktuell information om **nettovikten** på artikeln och på anläggningstillgångskortet.
    2. **Kompletterande antalsenhet** – för att omberäkna endast **Kompletterande antal** på **Intrastat-rapport**raden om den finns, utifrån den aktuella informationen om **Kompletterande måttenhet** på artikel- och anläggningstillgångskorten.
    3. **Båda** – om du vill beräkna om både den **totala vikten** och **kompletterande antal** utifrån den aktuella informationen om på artikel- och anläggningstillgångskortet.
3. Välj **OK** när du vill starta batchjobbet.

## <a name="report-intrastat-in-a-file"></a>Rapportera intrastat i en fil

Du kan skicka Intrastat-rapporten som en fil baserad på olika lokala myndigheters behov. Innan du skapar filen bör du köra **Checklisterapport** för att kontrollera om alla rader innehåller all nödvändig och giltig information. Så här skapar du en fil:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Intrastatlista** och väljer sedan relaterad länk.
2. Välj den **Intrastat-rapport** som du vill rapportera som en fil.
3. Om du inte redan har gjort det fyller du i **Intrastat-rapporten** manuellt eller så väljer du åtgärden **Föreslå rader**.
4. Välj åtgärden **Skapa fil**.
5. Intrastat-filen sparas i det format som krävs.

När du skapat filen fyller [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt i följande information om rapportering:

* **Exportdatum** för att ange det datum då rapporten exporterades.
* **Exporttid** för att ange den tid då rapporten exporterades.

> [!NOTE]
> Nästa gång du skapar en fil kommer fälten **Exportdatum** och **Exporttid** endast att ha information om den senaste filen du skapade.

## <a name="intrastat-rules"></a>Intrastat-regler

### <a name="grouping-lines"></a>Gruppera rader

I **Intrastat-rapportens** rader finns det ingen gruppering efter fält. Alla transaktioner kopieras från ursprungskällan så att du snabbt kan hitta dem utifrån kombinationen av **Källtyp**och **Källtransaktionsnr**.

Gruppering som krävs av myndigheterna kommer att lämnas i den exporterade filen. Du måste konfigurera detta i **Datautbytesdefinitionen** som är helt konfigurerbar. Läs mer i [Så här skapar du datautbytesdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

### <a name="fixed-assets-reporting"></a>Anläggningstillgångsrapporter

Anläggningstillgångar visas endast i Intrastat-raderna om:

* **Anl.bokföringstypen** i fältet **Momstransaktion** är **Anskaffningskostnad** och om **Dokumenttyp** är **Faktura** i händelse av köp, och
* **Anl.bokföringstypen** i fältet **Momstransaktion** är **Avyttringsintäkt** och om **Dokumenttyp** är **Faktura** i händelse av försäljning.

### <a name="intrastat-report-statuses"></a>Intrastat-rapportstatus

När du arbetar med **Intrastat-rapporten** visas fältet **Status** i dokumenthuvudet. Du kan hitta följande status tillsammans med relaterade regler:

* *Öppen*: Den här statusen skapas automatiskt när du skapar en ny Intrastat-rapport och du kan göra alla operationer med denna status.
* *Släppt*: [!INCLUDE[prod_short](includes/prod_short.md)] ändrar automatiskt statusen till *Släppt* när du skapar en fil. Från det tillfället kan du inte ändra **Intrastat-rapporten**. Om du behöver ändra något och rapportera igen kan du använda åtgärden **Öppna igen** för att öppna Intrastat-rapporten på nytt. När dokumentet har öppnats igen kan du använda åtgärden **Släpp** för att frisläppa dokumentet igen.
* **Rapporterad**: Anger om transaktionen redan har rapporterats till skattemyndigheterna. Detta är inte en vanlig status, utan ett oberoende fält, och även om du öppnar Intrastat-rapporten igen, visas fortfarande att filen redan har skapats för rapporten.

### <a name="triangular-trade-in-intrastat"></a>Triangulär handel med Intrastat

Triangulär handel innebär handel mellan tre länder eller regioner där varor kringgår det rapporterande företagets land. I Business Central kan detta underlättas via funktionen [Direktleverans](sales-how-drop-shipment.md). Aktivera det här alternativet genom att aktivera fältet **Inkludera direktleverans** i **Konfiguration av Intrastat-rapporter**.  

När du aktiverar det här alternativet används följande regler i systemet, men bara om du har markerat **direktleverans** på **försäljningsordern**: 

| Inleverans från | Leverans till | Förväntat Intrastat-resultat |
|----------|------------|----------------------|
| Land som i  **Företagsinformation** | Land som i  **Företagsinformation** | Inga Intrastat-rader |  
| Land som i  **Företagsinformation** | EU-land som skiljer sig från landet i **företagsinformationen** | Intrastat-leveransrad | 
| Land som i  **Företagsinformation** | Land utanför EU | Inga Intrastat-rader |   
| EU-land som skiljer sig från landet i **företagsinformationen** | Land som i  **Företagsinformation** | Intrastat-inleveransrad | 
| EU-land som skiljer sig från landet i **företagsinformationen** | EU-land som skiljer sig från landet i **företagsinformationen** | Inga Intrastat-rader |
| EU-land som skiljer sig från landet i **företagsinformationen** | Land utanför EU | Inga Intrastat-rader | 
| Land utanför EU | Land som i  **Företagsinformation** | Inga Intrastat-rader |  
| Land utanför EU | EU-land som skiljer sig från landet i **företagsinformationen** | Inga Intrastat-rader |
| Land utanför EU | Land utanför EU | Inga Intrastat-rader |   

## <a name="see-also"></a>Se även

[Konfigurera Intrastat-rapportering](finance-how-setup-report-intrastat.md)  
[Ekonomihantering](finance.md)  
[Direktleverans](sales-how-drop-shipment.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
