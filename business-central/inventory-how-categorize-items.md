---
title: Organisera i kategorier | Microsoft Docs
description: För att söka efter och hitta objekt ska du tilldela artikelattribut och ordna objekt i kategorier.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 55196b8026e5efc5a79ce1a547e2ff594fae231c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786029"
---
# <a name="categorize-items"></a>Kategorisera artiklar

För att underhålla en översikt över dina artiklar och för att sortera och söka artiklar är det praktiskt att ordna artiklarna i artikelkategorier.

Om du vill söka artiklar efter egenskaper kan du tilldela objektattribut till artiklar och även till artikelkategorier. Mer information finns i [Så här arbetar du med attribut](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a>Så här skapar du ett artikelkategori
1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artikelkategorier** och välj sedan relaterad länk.
2. På sidan **Artikelkategorier** väljer du åtgärden **Ny**.
3. På sidan **Artikelkategori** på snabbfliken **Allmänt** fyller du sedan de fält som behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. På snabbfliken **Attribut** anger du ett artikelattribut för artikelkategorin. Mer information finns i avsnittet [Att tilldela attribut till artikelattribut](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
> Om artikelkategorin har en överordnad artikelkategori som indikeras i fältet **Överordnad kategori** kommer alla artikelattribut, som har tilldelats den överordnade artikelkategorin att förifyllas på snabbfliken **Attribut**.

> [!NOTE]  
> Artikelattribut som du tilldelar en artikelkategori, kommer automatiskt att gälla för den artikel som artikelkategorin tilldelats.

Om du ändrar dig om en artikelkategori kan du ta bort den. Om en artikel redan har tilldelats måste du dock ta bort tilldelningen innan du kan ta bort artikelkategorin.

## <a name="to-assign-an-item-category-to-an-item"></a>Så här tilldelar du en artikelkategori till en artikel

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.
2. Öppna kortet för den artikel som du vill tilldela en en artikelkategori.
3. Välj sökknappen i fältet **Artikelkategorikod** och välj en befintlig artikelkategori. Välj alternativt åtgärden **Ny** för att först skapa en ny artikelkategori som förklaras i [Att skapa en artikelkategori](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="categories-attributes-and-variants"></a>Kategorier, attribut och varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Se även

[Arbeta med artikelattribut](inventory-how-work-item-attributes.md)  
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]