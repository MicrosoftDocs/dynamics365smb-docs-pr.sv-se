---
title: Lägg till ytterligare rader när du definierar utökade beskrivningar
description: Du kan lägga till ytterligare rader om du vill utöka standardtexten som beskriver en artikel, ett redovisningskonto och andra data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/08/2020
ms.author: sgroespe
ms.openlocfilehash: 0b611a4f2bcabec7cda408790ab659c6cf3f8e97
ms.sourcegitcommit: 8b2f02dd5189c46ecff33c07223ed62b36842d34
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2020
ms.locfileid: "3542573"
---
# <a name="add-extended-text"></a>Lägg till extratext

Du kan utöka beskrivningen av artiklar, lagerhållningsenheter, redovisningskonton och resurser genom att lägga till extra rader som extratext. Du kan också ange villkor för hur de extra raderna ska användas.  

I följande avsnitt beskrivs hur du lägger till extratext i en beskrivning av en artikel. Men samma steg gäller för lager enheter, redovisningskonton och resurser.  

## <a name="to-define-extended-text-for-an-description"></a>Om du vill definiera extratexten för en beskrivning

1. Öppna kortet för en artikel som du vill lägga till extratext på, och välj sedan åtgärden **Extratext**.
2. Fyll i fälten **Kod** och **Beskrivning**.
3. Välj **Ny**.
4. Fyll i fältet **Språkkod** eller markera kryssrutan **Alla språkkoder** om du vill använda språkkoder.
5. Fyll i fältet **Startdatum** och fältet **Slutdatum** om du vill begränsa den period under vilken extratexten ska användas.
6. I fältet **Text** anger du den extra texten.
7. Markera relevanta kryssrutor för dokumenttyperna där du vill att extratexten ska skrivas ut.
8. Stäng sidan.

Nu kan du lägga till den utökade texten i dokument. I proceduren nedan beskrivs hur du lägger till extratext på en försäljningsorder, men samma steg gäller för andra dokument som du har angett för den extratext.  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a>För att lägga till en utökad artikeltext på en försäljningsorderrad.

1. Öppna en försäljningsorder med en försäljningsrad för en artikel som har förlängd text som har definierats. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
2. Markera den aktuella raden och välj sedan åtgärden **Infoga förl. text**.

## <a name="see-also"></a>Se även

[Ställa in lager](inventory-setup-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
