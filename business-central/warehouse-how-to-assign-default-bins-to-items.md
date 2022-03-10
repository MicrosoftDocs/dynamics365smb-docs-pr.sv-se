---
title: 'Så här: Tilldela standardlagerplatser till artiklar'
description: Om du använder lagerställen för ett lagerställe blir det mycket enklare för dig att leverera, inleverera och flytta artiklar om du tilldelar dem standardlagerställen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: e4f3d103c5bfdcedfef6fa3571f4ca56aa2ccb9a
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134671"
---
# <a name="assign-default-bins-to-items"></a>Tilldela standardlagerställen till artiklar
Om du använder lagerställen för ett lagerställe blir det mycket enklare för dig att leverera, inleverera och flytta artiklar om du tilldelar dem standardlagerställen. När en artikel tilldelas en standardlagerplats kommer denna lagerplats att föreslås varje gång du påbörjar en transaktion för artikeln. Standardlagerställen definieras på sidan **Lagerställesinnehåll**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Så här tilldelar du en standardlagerplats till en artikel
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Lagerställesinnehålluppl kalkylark** och väljer sedan relaterad länk.  
2.  Fyll i lagerställeskoden och information om artiklar för respektive lagerplats som du vill ange som standard för en artikel. Se till att välja **Standard** här fältet.  
3.  Välj åtgärden **Skapa lagerställesinnehåll**. Din artikel tilldelas nu standardlagerställen.  

> [!NOTE]  
>  Vid införsel av artiklar som inte har tilldelats någon standardlagerplats, kommer den lagerplats där artikeln införs att anges som standardlagerplats.  

## <a name="to-change-the-default-bin-for-an-item"></a>Så här ändrar du standardlagerställen en artikel  
Ibland kan det bli nödvändigt att ändra fördelningen av standardlagerplats för en viss artikel, eller tilldela en ny artikel en standardlagerplats.    
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **lagerplatsinnehåll** och väljer sedan relaterad länk.  
2.  Välj tillämplig lagerställekod i fältet **Lagerställefilter**.  
3.  Sök efter aktuell post för standardlagerställesinnehåll för artikeln och avmarkera kryssrutan **Standardlagerplats**.  
4.  Sök efter raden för lagerställesinnehåll för den lagerplats som du vill använda som ny standardlagerplats. Markera kryssrutan **Standardlagerplats**.  

> [!NOTE]  
>  När en artikel införs för första gången och den inte har tilldelats någon standardlagerplats, kommer den lagerplats där artikeln införs att anges som standardlagerplats.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]