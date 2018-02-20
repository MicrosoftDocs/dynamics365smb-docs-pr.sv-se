---
title: "Skapa artikelkort för varor eller tjänster | Microsoft Docs"
description: "Du skapar artikelkort för tjänster som du säljer som timmar och för fysiska produkter, till exempel monteringsartiklar, färdiga produkter, komponenter eller råmaterial som säljs från lagret."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 39a701fb0ff705508fdc4ddcec0af661d234e8c8
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="register-new-items"></a>Registrera nya artiklar
Artiklar, bland andra produkter, utgör basen för ditt arbete, varorna eller tjänster som du handlar med. Varje artiklar måste registreras som ett artikelkort.

Artikelkort innehåller den information som behövs för att köpa, lagra, sälja, leverera och informera om artiklar.

Artikelkortet kan vara av typen **Lager** eller **Service** för att ange om artikeln är en fysisk enhet eller en arbetstidsenhet. Förutom vissa fält som är knutna till de fysiska aspekterna av en artikel, fungerar alla fält på ett artikelkort på samma sätt för lagerartiklar och tjänster. Mer information om att sälja en artikel finns i [Så här säljer du produkter](sales-how-sell-products.md) eller [Så här fakturerar du försäljning](sales-how-invoice-sales.md).

En artikel kan struktureras som en överordnad artikel med underliggande underordnade objekt i en struktur. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan en strukturlista vara antingen en monteringsstruktur eller en produktionsstruktur, beroende på dess användning. Mer information finns i [Arbeta med strukturer](inventory-how-work-BOMs.md).

> [!NOTE]  
>   Om artikelmallar finns för olika artikeltyper, visas ett fönster när du skapar ett nytt artikelkort där du kan välja en lämplig mall. Om endast en artikelmall finns, då använder nya artikelkort alltid den mallen.

Om du köper samma artikel från flera olika leverantörer, kan du ansluta de leverantörerna till artikelkortet. Leverantörer visas sedan i fönstret **Artikelleverantörskatalog** så att du enkelt kan välja en annan leverantör.

## <a name="to-create-a-new-item-card"></a>Skapa ett nytt artikelkort
1. På startsidan väljer du åtgärden **Artiklar** för att öppna listan över befintliga artiklar.  
2. I fönstret **Artiklar** väljer du åtgärden **Ny**.

    Om endast en artikelmall finns, då öppnas ett nytt artikelkort med fält ifyllda med information från mallen.
3. Välj den mall som du vill använda för den nya artikelkortet i fönstret **Välj en mall för en ny artikel**.
4. Välj **OK**. Ett nytt artikelkort öppnas med ifyllda fält med information från mallen.
5. Fortsätt att fylla i eller ändra fält på artikelkortet vid behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> I fältet **värderingsprincip** anger du hur artikelns styckkostnad beräknas genom att anta hur flödet av fysiska artiklar sker i företaget. Fem metoder är tillgängliga, beroende på typen av objekt. Mer information finns i [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md).
>
> Om du använder **Genomsnitt** beräknas en artikels enhetskostnad som den genomsnittliga styckkostnaden vid varje tidpunkt efter ett inköp. Lager värderas med förutsättningen att alla lagerartiklar säljs samtidigt. Med den här inställningen kan du välja fältet **Styckkostnad** för att i fönstret **Översikt: Beräkning av genomsnittskostnad** visa tidigare transaktioner som genomsnittskostnaden beräknas från.

På snabbfliken **Pris och bokföring** ser du specialpriser eller rabatter som du beviljar för artikeln om vissa kriterier uppfylls, till exempel kund, lägsta partistorlek eller slutdatum. Varje rad representerar ett speciellt pris eller radrabatt. Varje kolumn representerar ett kriterium som måste gälla för att garantera specialpriset som du anger i fältet **Enhetspris** eller radrabatten som du anger i fältet **Radrabatt %**. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).

Artikeln är nu registrerad, och artikelkortet är klart att användas i försäljningsdokument.

Om du vill använda detta artikelkort som en mall när du skapar nya artikelkort, så fortsätt med att spara den som en mall. Mer information finns i följande avsnitt:

## <a name="to-save-the-item-card-as-a-template"></a>Om du vill spara artikelkortet som en mall
1. I fönstret **artikelkort** väljer du åtgärden **Spara som mall**. Det **artikelmall** fönstret öppnas uppvisar artikelkortet som mall.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om du vill återanvända dimensioner i mallar väljer du fönstret **Dimensioner**. Fönstret **Dimensionsmallar** öppnas och visar de dimensionskoder som ställts in för artikeln.
4. Ändra eller ange dimensionskoder som ska kopplas till nya artikelkort som skapas med hjälp av mallen.
5. Välj **OK** när du har slutfört den nya artikelmallen.

Artikelmallen läggs till listan över artikelmallar, så att du kan använda det för att skapa nya artikelkort.

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Så här lägger du upp flera leverantörer för artiklar  
Om du köper samma artikel från flera olika leverantörer måste du ange information om varje leverantör, t.ex. priser, ledtid och rabatter.  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Artiklar** och välj sedan relaterad länk.  
2.  Välj relevant artikel och välj sedan åtgärden **Artikel**.  
3.  Välj åtgärden **Leverantörer**.  
4.  Välj fältet **Leverantörsnr** och välj sedan leverantör som du vill lägga upp för artikeln.  
5.  Det är frivilligt att fylla i övriga fält.  
6.  Upprepa moment 2 till 5 för varje leverantör som du vill köpa artikeln från.

Leverantörer visas nu i fönstret **Artikelleverantörskatalog** som du kan öppna från artikelkortet så att du enkelt kan välja en annan leverantör.

## <a name="see-also"></a>Se även
  [Lagersaldo](inventory-manage-inventory.md)  
  [Inköp](purchasing-manage-purchasing.md)  
  [Försäljning](sales-manage-sales.md)  
  [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

