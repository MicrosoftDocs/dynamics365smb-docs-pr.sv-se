---
title: Organisera i kategorier | Microsoft Docs
description: "För att söka efter och hitta objekt ska du tilldela artikelattribut och ordna objekt i kategorier."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5b684df40599a730054e333f1bdf2e526c840e0b
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="categorize-items"></a>Kategorisera artiklar
För att underhålla en översikt över dina artiklar och för att sortera och söka artiklar är det praktiskt att ordna artiklarna i artikelkategorier.

Om du vill söka artiklar efter egenskaper kan du tilldela objektattribut till artiklar och även till artikelkategorier. Mer information finns i [Så här arbetar du med attribut](inventory-how-work-item-attributes.md).

## <a name="to-create-an-item-category"></a>Så här skapar du ett artikelkategori
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artikelkategorier** och välj sedan relaterad länk.
2. På sidan **Artikelkategorier** väljer du åtgärden **Ny**.
3. På sidan**Artikelkategori** på snabbfliken **Allmänt** fyller du sedan de fält som behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. På snabbfliken **Attribut** anger du ett artikelattribut för artikelkategorin. För mer information, se avsnittet "Tilldela artikelattribut till en artikelkategori" i [Så här arbetar du med artikelattribut](inventory-how-work-item-attributes.md).

> [!NOTE]  
>   Om artikelkategorin har en överordnad artikelkategori som indikeras i fältet **Överordnad kategori** kommer alla artikelattribut, som har tilldelats den överordnade artikelkategorin att förifyllas på snabbfliken **Attribut**.

> [!NOTE]  
>   Artikelattribut som du tilldelar en artikelkategori, kommer automatiskt att gälla för den artikel som artikelkategorin tilldelats.

## <a name="to-assign-an-item-category-to-an-item"></a>Så här tilldelar du en artikelkategori till en artikel
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.
2. Öppna kortet för den artikel som du vill tilldela en en artikelkategori.
3. Välj sökknappen i fältet **Artikelkategorikod** och välj en befintlig artikelkategori. Välj alternativt åtgärden **Ny** för att först skapa en ny artikelkategori som förklaras i avsnittet "Att skapa en artikelkategori".

## <a name="see-also"></a>Se även
[Arbeta med artikelattribut](inventory-how-work-item-attributes.md)  
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

