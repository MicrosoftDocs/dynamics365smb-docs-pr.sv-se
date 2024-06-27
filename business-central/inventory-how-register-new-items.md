---
title: Skapa artikelkort för varor eller tjänster
description: Du skapar artikelkort för service som du säljer som timmar och för fysiska produkter. Exempel inkluderar monteringsartiklar och färdiga varor som du säljer från lagret.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="register-new-items"></a>Registrera nya artiklar

Artiklar är de varor eller tjänster som du köper, lagrar, säljer, levererar och står för. Använd sidan **Artikelkort** för att registrera information om följande typer av artiklar:

* **Lager** anger att artikeln är en fysisk enhet som du hanterar och spårar i lagret.
* **INte i lager** är fysiska enheter som du inte hanterar eller spårar i lagret.
* **Serviceartiklar** är en arbetstidsenhet som vanligtvis används i servicehantering.

Om du vill veta mer om dessa typer av artiklar som inte finns i lager går du till [Om artikeltyper](inventory-about-item-types.md).

> [!TIP]
> Det finns också katalogartiklar som liknar artiklar som inte finns i lager på så sätt att de är artiklar som du erbjuder till kunder men inte hanterar förrän du säljer dem. Om du vill lära dig mer går du till [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).  

## <a name="primary-and-alternate-vendors"></a>Primära och alternativa leverantörer

Om du köper samma artikel från flera olika leverantörer, kan du ansluta de leverantörerna till artikeln. Använd åtgärden **Leverantörer** på sidan **Artikelkort** för att öppna sidan **Artikelns leverantörskatalog**. På sidan visas de leverantörer som du köper artikeln från, så att du enkelt kan skapa eller välja en alternativ leverantör när du skapar en inköpsorder.

## <a name="use-item-templates"></a>Använd artikelmallar

Om du vill återanvända inställningar för olika typer av objekt när du skapar nya objekt kan du spara objekten som artikelmallar. Artikelmallar hjälper till att påskynda processen med att lägga till nya artiklar och ökar enhetligheten i dina artikeldata. När du registrerar ett nytt objekt visas en sida där du kan välja en mall. När du har valt en mall fylls dess inställningar i automatiskt för objektet du skapar. Om du bara har en artikelmall använder nya objekt alltid den mallen. Information om hur du skapar en artikelmall finns i [Spara ett artikelkort som en artikelmall](#save-an-item-card-as-an-item-template).

## <a name="include-items-in-bills-of-materials"></a>Ta med artiklar i strukturlistor

Du kan strukturera hierarkier som har en huvudartikel med underliggande komponentartiklar i monterings- och produktionsstrukturer. Om du vill lära dig mer om strukturer går du till [Arbeta med strukturer](inventory-how-work-BOMs.md).

## <a name="to-create-a-new-item-card"></a>Skapa ett nytt artikelkort

Följande video visar hur du ställer in ett objekt på sidan Artikelkort. Men du kan också ställa in nya objekt genom att kopiera befintliga. Mer information finns i [kopiera befintliga objekt om du vill skapa nya objekt](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> I fältet **värderingsprincip** anger du hur artikelns styckkostnad beräknas genom att anta hur flödet av fysiska artiklar sker i företaget. Fem metoder är tillgängliga, beroende på typen av objekt. Mer information om kostnad finns i [Designdetaljer: värderingsprinciper](design-details-costing-methods.md).
>
> Om du använder **Genomsnitt** beräknas en artikels styckkostnad som den genomsnittliga styckkostnaden vid respektive tidpunkt efter ett inköp. Lager värderas med förutsättningen att alla lagerartiklar säljs samtidigt. Med den här inställningen kan du välja fältet **Styckkostnad** för att på sidan **Översikt: Beräkning av genomsnittskostnad** för att se de transaktioner som användes för att beräkna den genomsnittliga kostnaden.

Du kan använda specialpriser eller rabatter som du eller leverantören beviljar för artikeln baserat på vissa kriterier. Kriterierna omfattar till exempel kund, minsta orderkvantitet eller slutdatum. Du ställer in specialpriser genom att välja åtgärderna **ange särskilda priser** eller **ange särskilda rabatter**. Varje rad på, t. ex. sidan **försäljningspriser**, representerar ett specialpris. Varje kolumn representerar ett kriterium som måste användas för att ge kunden det särskilda pris som du anger i fältet **enhetspris** på sidan **försäljningspriser**. För att lära dig mer om prissättning, gå till [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md) eller [Registrera särskilda inköpspriser och rabatter](purchasing-how-record-purchase-price-discount-payment-agreements.md).

### <a name="save-an-item-card-as-an-item-template"></a>Spara ett artikelkort som en artikelmall

1. På sidan **artikelkort** väljer du åtgärden **Spara som mall**. Sidan **artikelmall** visar artikelkortet som mall.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Du kan även återanvända dimensioner för artiklar. Om du vill återanvända dimensioner i mallar väljer du fönstret **Dimensioner**. Sidan **Dimensionsmallar** visar de mått som är inställda för artikeln. Redigera eller lägg till dimensioner som gäller för nya objekt som du skapar från mallen.

Artikelmallen läggs till listan över artikelmallar, så att du kan använda det för att skapa nya artikelkort.

### <a name="items-used-in-production-orders"></a>Artiklar som används i produktionsorder

Om du vill registrera artiklar som används i produktionsorder anger du återanskaffningssystemet som *Prod. order* på snabbfliken **Återanskaffning**. För mer information, se [Om produktionsorder](production-about-production-orders.md).  

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Så här lägger du upp flera leverantörer för artiklar

Om du köper samma artikel från flera olika leverantörer måste du ange information om varje leverantör, t. ex. priser, ledtid och rabatter.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2. Välj relevant artikel och välj sedan åtgärden **Artikel**.  
3. Välj åtgärden **Leverantörer**.  
4. Välj fältet **Leverantörsnr** och välj sedan leverantör som du vill lägga upp för artikeln.  
5. Det är frivilligt att fylla i övriga fält.  
6. Upprepa moment 2 till 5 för varje leverantör som du vill köpa artikeln från.

Leverantörer visas nu på sidan **Artikelleverantörskatalog** som du kan öppna från artikelkortet så att du enkelt kan välja en annan leverantör.

## <a name="set-up-item-substitutions"></a>Ställa in artikelersättningar

Du kan ställa in artiklar så att de har ersättningar, som andra artiklar som kan användas i stället för den ursprungliga artikeln.

### <a name="to-make-an-item-substitution"></a>Så här gör du en artikelersättning

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2. Hitta den aktuella artikeln och välj sedan **Artikelnr** för att öppna artikelkortet.  
3. Välj åtgärden **Relaterat**, välj sedan **Artikel** och sedan **Ersättningar** för att öppna sidan **Artikelersättningspost**.  
4. Välj **Ersättningsnr**. fältet och välj sedan ersättningsartikel i listan.
5. Fyll i eller ändra andra fält på sidan vid behov.

När antal artiklar som har begärts överstiger det tillgängliga antalet i lager visas ett meddelande som anger att ersättningsartiklar finns.

> [!NOTE]  
> Kom ihåg att artikelersättningar inte automatiskt gör att en artikel ersätts av en annan artikel, till exempel när du skapar en försäljningsorder eller i en strukturlista. Istället kommer du att aviseras om att en ersättning är tillgänglig för dig.

## <a name="categories-attributes-and-variants"></a>Kategorier, attribut och varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

Läs mer om varianter på [Hantera produktvarianter](inventory-item-variants.md).  

## <a name="delete-item-cards"></a>Ta bort artikelkort

Om du har bokfört en transaktion för en artikel kan du inte ta bort kortet eftersom transaktionerna kan behövas för lagervärdering eller revision. Om du vill ta bort artikelkort med transaktioner, kontaktar du Microsoft partner för att göra det via kod.  

## <a name="manage-inventory-in-warehouses"></a>Hantera lager i distributionslager

När du registrerar en ny artikel visas fält som är kopplade till hanteringen av distributionslager, särskilt på snabbfliken **Distributionslager**. Om organisationen inte använder funktionerna för hantering av distributionslager i [!INCLUDE [prod_short](includes/prod_short.md)] kan du ignorera dessa fält.  

Om företaget senare konfigurerar lagerhantering rekommenderar vi att du säkerställer att varje befintlig artikeln har rätt information i de olika fälten. På så sätt kan lagerprocesserna köras som förväntat. Informationen kan omfatta fält som **Indelningskod för distributionslager** eller **Mallkod för artikelinförsel**. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).  

## <a name="planning"></a>Planering

När ditt företag använder leveransplaneringsprocesserna i [!INCLUDE [prod_short](includes/prod_short.md)], måste du fylla i relevanta fält på snabbfliken **Planering**. En introduktion till planeringsområdet finns i [Designdetaljer: Centrala begrepp i planeringssystemet](design-details-central-concepts-of-the-planning-system.md).  

Exempel på hur du kan använda fälten på snabbfliken **Planering** finns i [Metodtips för installation: Planeringsparametrar](setup-best-practices-planning-parameters.md).  

## <a name="see-also"></a>Se även

[Lager](inventory-manage-inventory.md)  
[Konfigurera måttenheter](inventory-how-setup-units-of-measure.md)  
[Hantera produktvarianter](inventory-item-variants.md)  
[Ställa in Intrastat-rapporter](finance-how-setup-report-intrastat.md#other-intrastat-configurations)  
[Stämma av lagerkostnader med redovisningen](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Skapa nummerserier](ui-create-number-series.md)  
[Ställa in bokföringsmallar](finance-posting-groups.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Om planeringsfunktioner](production-about-planning-functionality.md)  
[Skapa metodtips: planeringsparametrar](setup-best-practices-planning-parameters.md)  
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)  
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
