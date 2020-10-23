---
title: Skapa artikelkort för varor eller tjänster | Microsoft Docs
description: Du skapar artikelkort för tjänster som du säljer som timmar och för fysiska produkter, till exempel monteringsartiklar, färdiga produkter, komponenter eller råmaterial som säljs från lagret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 74eb66c4303acb452972f9ac3c7dda008e3c6502
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923826"
---
# <a name="register-new-items"></a>Registrera nya artiklar

Artiklar, bland andra produkter, utgör basen för ditt arbete, varorna eller tjänster som du handlar med. Varje artiklar måste registreras som ett artikelkort.

Artikelkort innehåller den information som behövs för att köpa, lagra, sälja, leverera och informera om artiklar.

Artikelkortet kan vara av typen **Lager**, **Service**, eller **Inte i lager** för att ange om artikeln är en fysisk inventeringsenhet, en arbetstidsenhet eller en fysisk enhet som inte spåras i inventeringen. Mer information om typerna finns i [Om artikeltyper](inventory-about-item-types.md).

En artikel kan struktureras som en överordnad artikel med underliggande underordnade objekt i en struktur. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan en strukturlista vara antingen en monteringsstruktur eller en produktionsstruktur, beroende på dess användning. Mer information finns i [Arbeta med strukturer](inventory-how-work-BOMs.md).

Om du köper samma artikel från flera olika leverantörer, kan du ansluta de leverantörerna till artikelkortet. Leverantörer visas sedan på sidan **Artikelleverantörskatalog** så att du enkelt kan välja en annan leverantör.

Artiklar som du erbjuder dina kunder men som du inte vill hantera i ditt system, tills du börjar sälja dem kan ställas in som katalogartiklar. Katalogartiklar ska inte förväxlas med vanliga artiklar av typen **Inte i lager**. Mer information finns i [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Om artikelmallar finns för olika artikeltyper, visas en sida när du skapar ett nytt artikelkort där du kan välja en lämplig mall. Om endast en artikelmall finns, då använder nya artikelkort alltid den mallen.

I proceduren nedan beskrivs hur du skapar ett artikelkort från grunden. Du kan också skapa nya artikelkort genom att kopiera befintliga artiklar. Mer information finns i [kopiera befintliga objekt om du vill skapa nya objekt](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card"></a>Skapa ett nytt artikelkort

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.  
2. På sidan **Artiklar** väljer du åtgärden **Ny**.

    Om endast en artikelmall finns, då öppnas ett nytt artikelkort med fält ifyllda med information från mallen.
3. Välj den mall som du vill använda för den nya artikelkortet på sidan **Välj en mall för en ny artikel**.
4. Välj **OK**. Ett nytt artikelkort öppnas med ifyllda fält med information från mallen.
5. Fortsätt att fylla i eller ändra fält på artikelkortet vid behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> I fältet **värderingsprincip** anger du hur artikelns styckkostnad beräknas genom att anta hur flödet av fysiska artiklar sker i företaget. Fem metoder är tillgängliga, beroende på typen av objekt. Mer information finns i [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md).
>
> Om du använder **Genomsnitt** beräknas en artikels enhetskostnad som den genomsnittliga styckkostnaden vid respektive tidpunkt efter ett inköp. Lager värderas med förutsättningen att alla lagerartiklar säljs samtidigt. Med den här inställningen kan du välja fältet **Styckkostnad** för att på sidan **Översikt: Beräkning av genomsnittskostnad** visa tidigare transaktioner som genomsnittskostnaden beräknas från.

Du kan visa eller redigera specialpriser eller rabatter som du beviljar eller som säljaren ger dig för artikeln om vissa kriterier uppfylls, till exempel kund, lägsta partistorlek eller slutdatum Det gör du genom att välja åtgärderna **ange särskilda priser** eller **ange särskilda rabatter**. Varje rad på, t.ex. sidan **försäljningspriser**, representerar ett specialpris. Varje kolumn representerar ett kriterium som måste användas för att ge kunden det särskilda pris som du anger i fältet **enhetspris** på sidan **försäljningspriser**. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md) eller [Registrera särskilda inköpspriser och rabatter](purchasing-how-record-purchase-price-discount-payment-agreements.md).

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

Om du vill registrera artiklar som sedan används i produktionsorder anger du återanskaffningssystemet som *Prod. order* på snabbfliken **återanskaffning**. För mer information, se [Om produktionsorder](production-about-production-orders.md).  

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Så här lägger du upp flera leverantörer för artiklar

Om du köper samma artikel från flera olika leverantörer måste du ange information om varje leverantör, t.ex. priser, ledtid och rabatter.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.  
2. Välj relevant artikel och välj sedan åtgärden **Artikel**.  
3. Välj åtgärden **Leverantörer**.  
4. Välj fältet **Leverantörsnr** och välj sedan leverantör som du vill lägga upp för artikeln.  
5. Det är frivilligt att fylla i övriga fält.  
6. Upprepa moment 2 till 5 för varje leverantör som du vill köpa artikeln från.

Leverantörer visas nu på sidan **Artikelleverantörskatalog** som du kan öppna från artikelkortet så att du enkelt kan välja en annan leverantör.

## <a name="categories-attributes-and-variants"></a>Kategorier, attribut och varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="deleting-item-cards"></a>Ta bort artikelkort

Om du har bokfört en transaktion för en artikel kan du inte ta bort kortet eftersom transaktionerna kan behövas för lagervärdering eller revision. Om du vill ta bort artikelkort med transaktioner, kontaktar du Microsoft partner för att göra det via kod.  

## <a name="manage-inventory-in-warehouses"></a>Hantera lager i distributionslager

När du registrerar en ny artikel visas fält som är kopplade till hanteringen av distributionslager, särskilt på snabbfliken **Distributionslager**. Om organisationen inte använder funktionerna för hantering av distributionslager i [!INCLUDE [prodshort](includes/prodshort.md)] kan du ignorera dessa fält.  

Om företaget senare konfigurerar hantering av distributionslager, måste du i de flesta fall gå tillbaka till varje befintlig artikel för att försäkra dig om att de har rätt information i de olika fälten så att lagerprocesserna kan köras som förväntat. Informationen kan omfatta fält som **Indelningskod för distributionslager** eller **Mallkod för artikelinförsel**. Mer information finns i [Designdetaljer: Lagerstyrningsinställningar](design-details-warehouse-setup.md).  

## <a name="see-also"></a>Se även

[Lager](inventory-manage-inventory.md)  
[Ställa in måttenheter](inventory-how-setup-units-of-measure.md)  
[EU tull statistiknr](finance-how-setup-report-intrastat.md#tariff-numbers)  
[Stämma av lagerkostnader med redovisningen](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Skapa nummerserier](ui-create-number-series.md)  
[Ställa in bokföringsmallar](finance-posting-groups.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
