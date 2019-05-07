---
title: Lägg till ytterligare rader när du definierar utökade artikelbeskrivningar | Microsoft Docs
description: Du kan lägga till ytterligare rader om du vill utöka standardtexten som beskriver en artikel.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a43cca28bb24c5723d81ca28a3d1f86a38f5ad7c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "941663"
---
# <a name="add-extended-item-text"></a>Lägg till utökad artikeltext
Du kan utöka en standardtext för artiklar genom att lägga till extrarader och du kan ange villkor för användningen av extraraderna. Detta kan du göra från artikelkort.

## <a name="to-define-extended-text-for-an-item-description"></a>Om du vill definiera extratexten för en objektbeskrivning
1. Öppna kortet för en artikel som du vill lägga till extratext på, och välj sedan åtgärden **Extratext**.
2. Fyll i fälten **Kod** och **Beskrivning**.
3. Välj **Ny**.
4. Fyll i fältet **Språkkod** eller markera kryssrutan **Alla språkkoder** om du vill använda språkkoder.
5. Fyll i fältet **Startdatum** och fältet **Slutdatum** om du vill begränsa den period under vilken extratexten ska användas.
6. I fältet **Text** anger du den extra texten.
7. Markera relevanta kryssrutor för dokumenttyperna där du vill att extratexten ska skrivas ut.
8. Stäng sidan.

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a>För att lägga till en utökad artikeltext på en försäljningsorderrad.
1. Öppna en försäljningsorder med en försäljningsrad för en artikel som har förlängd text som har definierats. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
2. Markera den aktuella raden och välj sedan åtgärden **Infoga förl. text**.

## <a name="see-also"></a>Se även
[Ställa in lager](inventory-setup-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
