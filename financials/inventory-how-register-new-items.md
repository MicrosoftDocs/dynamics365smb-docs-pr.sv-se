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
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 719e11f2c8fee3d7e5dd3736754700b68f57379c
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-register-new-items"></a>Så här registrerar du nya objekt
Artiklar, bland andra produkter, utgör basen för ditt arbete, varorna eller tjänster som du handlar med. Varje artiklar måste registreras som ett artikelkort.

Artikelkort innehåller den information som behövs för att köpa, lagra, sälja, leverera och informera om artiklar.

Artikelkortet kan vara av typen **Lager** eller **Service** för att ange om artikeln är en fysisk enhet eller en arbetstidsenhet. Förutom vissa fält som är knutna till de fysiska aspekterna av en artikel, fungerar alla fält på ett artikelkort på samma sätt för lagerartiklar och tjänster. Mer information om att sälja en artikel finns i [Så här säljer du produkter](sales-how-sell-products.md) eller [Så här fakturerar du försäljning](sales-how-invoice-sales.md).

En artikel kan struktureras som en överordnad artikel med underliggande underordnade objekt i en struktur. I [!INCLUDE[d365fin](includes/d365fin_md.md)],  är en struktur en monteringsstruktur. Använd monteringsstrukturer för att strukturera de överordnade artiklar som du säljer som satser som består av komponenter som du monterar till order eller lager. Mer information finns i [Så här arbetar du med strukturer](inventory-how-work-BOMs.md).

> [!NOTE]  
>   Om artikelmallar finns för olika artikeltyper, visas ett fönster när du skapar ett nytt artikelkort där du kan välja en lämplig mall. Om endast en artikelmall finns, då använder nya artikelkort alltid den mallen.

## <a name="to-create-a-new-item-card"></a>Skapa ett nytt artikelkort
1. På startsidan väljer du åtgärden **Artiklar** för att öppna listan över befintliga artiklar.  
2. I fönstret **Artiklar** väljer du åtgärden **Ny**.

    Om endast en artikelmall finns, då öppnas ett nytt artikelkort med fält ifyllda med information från mallen.
3. Välj den mall som du vill använda för den nya artikelkortet i fönstret **Välj en mall för en ny artikel**.
4. Välj **OK**. Ett nytt artikelkort öppnas med ifyllda fält med information från mallen.
5. Fortsätt att fylla i eller ändra fält på artikelkortet vid behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

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

## <a name="see-also"></a>Se även
  [Lagersaldo](inventory-manage-inventory.md)  
  [Inköp](purchasing-manage-purchasing.md)  
  [Försäljning](sales-manage-sales.md)  
  [Arbeta med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
