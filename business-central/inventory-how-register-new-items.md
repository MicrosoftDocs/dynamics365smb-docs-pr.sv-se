---
title: Skapa artikelkort för varor eller tjänster (innehåller video)
description: Du skapar artikelkort för service som du säljer som timmar och för fysiska produkter. Exempel inkluderar monteringsartiklar och färdiga varor som du säljer från lagret.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item, item substitution
ms.search.form: 30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719
ms.date: 09/26/2022
ms.author: edupont
ms.openlocfilehash: 945197681e32f6d77ede2f1b0e727892a64d8277
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9604955"
---
# <a name="register-new-items"></a>Registrera nya artiklar

Artiklar, bland andra produkter, utgör basen för ditt arbete, varorna eller tjänster som du handlar med. Varje artiklar måste registreras som ett artikelkort.

Artikelkort innehåller den information som behövs för att köpa, lagra, sälja, leverera och informera om artiklar.

Artikelkortet kan vara av typen **Lager**, **Service** eller **Inte i lager** för att ange om artikeln är en fysisk lagerenhet, en arbetstidsenhet eller en fysisk enhet som inte spåras i inventeringen. Mer information om typerna finns i [Om artikeltyper](inventory-about-item-types.md).

En artikel kan struktureras som en överordnad artikel med underliggande underordnade objekt i en struktur. Läs mer om monteringsstrukturer och produktionsstrukturer på [Arbeta med strukturer](inventory-how-work-BOMs.md).

Om du köper samma artikel från flera olika leverantörer, kan du ansluta de leverantörerna till artikelkortet. Leverantörer visas sedan på sidan **Artikelleverantörskatalog** så att du enkelt kan välja en annan leverantör.

*Katalogartiklar* är artiklar du erbjuder dina kunder men som du inte vill hantera i ditt system, tills du börjar sälja dem. Katalogartiklar är inte vanliga artiklar av typen **Inte i lager**. Mer information: [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Om artikelmallar finns för olika artikeltyper, visas en sida när du skapar ett nytt artikelkort där du kan välja en lämplig mall. Om endast en artikelmall finns, då använder nya artikelkort alltid den mallen.

I proceduren nedan beskrivs hur du skapar ett artikelkort från grunden. Du kan också skapa nya artikelkort genom att kopiera befintliga artiklar. Mer information finns i [kopiera befintliga objekt om du vill skapa nya objekt](inventory-how-copy-items.md).  

<br />
> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card"></a>Skapa ett nytt artikelkort

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> I fältet **värderingsprincip** anger du hur artikelns styckkostnad beräknas genom att anta hur flödet av fysiska artiklar sker i företaget. Fem metoder är tillgängliga, beroende på typen av objekt. Mer information finns i [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md).
>
> Om du använder **Genomsnitt** beräknas en artikels styckkostnad som den genomsnittliga styckkostnaden vid respektive tidpunkt efter ett inköp. Lager värderas med förutsättningen att alla lagerartiklar säljs samtidigt. Med den här inställningen kan du välja fältet **Styckkostnad** för att på sidan **Översikt: Beräkning av genomsnittskostnad** visa tidigare transaktioner som genomsnittskostnaden beräknas från.

Du kan visa eller redigera specialpriser eller rabatter som du beviljar eller som säljaren ger dig för artikeln om vissa kriterier uppfylls, till exempel kund, lägsta partistorlek eller slutdatum Det gör du genom att välja åtgärderna **ange särskilda priser** eller **ange särskilda rabatter**. Varje rad på, t. ex. sidan **försäljningspriser**, representerar ett specialpris. Varje kolumn representerar ett kriterium som måste användas för att ge kunden det särskilda pris som du anger i fältet **enhetspris** på sidan **försäljningspriser**. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md) eller [Registrera särskilda inköpspriser och rabatter](purchasing-how-record-purchase-price-discount-payment-agreements.md).

Artikeln är nu registrerad, och artikelkortet är klart att användas i försäljningsdokument.

Om du vill använda detta artikelkort som en mall när du skapar nya artikelkort, så fortsätt med att spara den som en mall. Mer information finns i följande avsnitt:  

### <a name="to-save-the-item-card-as-a-template"></a>Om du vill spara artikelkortet som en mall

1. På sidan **artikelkort** väljer du åtgärden **Spara som mall**. Sidan **artikelmall** öppnas och uppvisar artikelkortet som mall.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om du vill återanvända dimensioner i mallar väljer du fönstret **Dimensioner**. Sidan **Dimensionsmallar** öppnas och visar de dimensionskoder som ställts in för artikeln.
4. Ändra eller ange dimensionskoder som ska kopplas till nya artikelkort som skapas med hjälp av mallen.
5. Välj **OK** när du har slutfört den nya artikelmallen.

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

## <a name="deleting-item-cards"></a>Ta bort artikelkort

Om du har bokfört en transaktion för en artikel kan du inte ta bort kortet eftersom transaktionerna kan behövas för lagervärdering eller revision. Om du vill ta bort artikelkort med transaktioner, kontaktar du Microsoft partner för att göra det via kod.  

## <a name="manage-inventory-in-warehouses"></a>Hantera lager i distributionslager

När du registrerar en ny artikel visas fält som är kopplade till hanteringen av distributionslager, särskilt på snabbfliken **Distributionslager**. Om organisationen inte använder funktionerna för hantering av distributionslager i [!INCLUDE [prod_short](includes/prod_short.md)] kan du ignorera dessa fält.  

Om företaget senare konfigurerar lagerhantering rekommenderar vi att du säkerställer att varje befintlig artikeln har rätt information i de olika fälten. På så sätt kan lagerprocesserna köras som förväntat. Informationen kan omfatta fält som **Indelningskod för distributionslager** eller **Mallkod för artikelinförsel**. Mer information finns i [Designdetaljer: Lagerstyrningsinställningar](design-details-warehouse-setup.md).  

## <a name="planning"></a>Planering

När ditt företag använder leveransplaneringsprocesserna i [!INCLUDE [prod_short](includes/prod_short.md)], måste du fylla i relevanta fält på snabbfliken **Planering**. En introduktion till planeringsområdet finns i [Designdetaljer: Centrala begrepp i planeringssystemet](design-details-central-concepts-of-the-planning-system.md).  

Exempel på hur du kan använda fälten på snabbfliken **Planering** finns i [Metodtips för installation: Planeringsparametrar](setup-best-practices-planning-parameters.md).  

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/create-items/)

## <a name="see-also"></a>Se även

[Lager](inventory-manage-inventory.md)  
[Ställa in måttenheter](inventory-how-setup-units-of-measure.md)  
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
