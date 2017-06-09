---
title: "Så här registrerar du nya kunder | Microsoft Docs"
description: "Så här registrerar du nya kunder"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6789e6a4129789e950c7f71ff86e62263ae9c087
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-register-new-customers"></a>Så här registrerar du nya kunder
Kunderna är källan till din inkomst. Du måste registrera varje kund som du säljer till som ett kundkort. Kundkort innehåller den information som behövs för att sälja produkter till kunden. Mer information finns i [Så här fakturerar du försäljning](sales-how-invoice-sales.md), [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).  

Innan du kan registrera nya kunder, måste du lägga upp olika försäljningskoder som du kan välja mellan, när du fyller i kundkort. Mer information finns i [Konfigurera försäljning](sales-setup-sales.md).

**Obs!** Om kundmallar finns för olika kundtyper, visas ett fönster när du skapar ett nytt kundkort där du kan välja en lämplig mall. Om endast en kundmall finns, då använder nya kundkort alltid den mallen.

## <a name="to-create-a-new-customer-card"></a>SÅ här skapar du ett nytt kundkort
1. På startsidan väljer du åtgärden **Kunder** för att öppna listan över befintliga kunder.  
2. I fönstret **Kunder** väljer du åtgärden **Ny**.

    Om endast en kundmall finns, då öppnas ett nytt kundkort med fält ifyllda med information från mallen.

    Om fler än en kundmall finns, öppnas ett fönster där du kan välja kundmall. I detta fall, följ nästa två steg.
3. Välj den mall som du vill använda för det nya kundkortet i fönstret **Välj en mall för en ny kund**.
4. Välj **OK**. Ett nytt kundkort öppnas med ifyllda fält med information från mallen.  
5. Fortsätt att fylla i eller ändra fält på kundkortet vid behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

På snabbfliken **Försäljningspriser** ser du specialpriser eller rabatter som du beviljar för kunden om vissa kriterier uppfylls, till exempel artikel, lägsta partistorlek eller slutdatum Varje rad representerar ett speciellt pris eller radrabatt. Varje kolumn representerar ett kriterium som måste gälla för att garantera specialpriset som du anger i fältet **Enhetspris** eller radrabatten som du anger i fältet **Radrabatt %**. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).

Kunden är nu registrerad, och kundkortet är klart att användas i försäljningsdokument.

Om du vill använda detta kundkort som en mall när du skapar nya kundkort, så fortsätt med att spara den som en mall. Mer information finns i följande avsnitt:

## <a name="to-save-the-customer-card-as-a-template"></a>Om du vill spara kundkortet som en mall
1. I fönstret **kundkort** väljer du åtgärden **Spara som mall**. Fönstret **Kundmall** öppnas och visar kundkortet som mall.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om du vill återanvända dimensioner i mallar väljer du fönstret **Dimensioner**. Fönstret **Dimensionsmallar** öppnas och visar de dimensionskoder som ställts in för kunden.
4. Ändra eller ange dimensionskoder som ska kopplas till nya kundkort som skapas med hjälp av mallen.  
5. Välj **OK** när du har slutfört den nya kundmallen.

Kundmallen läggs till listan över kundmallar, så att du kan använda det för att skapa nya kundkort.

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)    
[Konfigurera försäljning](sales-setup-sales.md)    
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

