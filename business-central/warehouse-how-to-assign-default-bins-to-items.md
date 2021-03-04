---
title: 'Så här: Tilldela standardlagerställen till artiklar | Microsoft Docs'
description: Om du använder lagerställen för ett lagerställe blir det mycket enklare för dig att leverera, inleverera och flytta artiklar om du tilldelar dem standardlagerställen. När en artikel tilldelas en standardlagerplats kommer denna lagerplats att föreslås varje gång du påbörjar en transaktion för artikeln.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f3374929434876cee088f046efc6d5f950671cc8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756323"
---
# <a name="assign-default-bins-to-items"></a>Tilldela standardlagerställen till artiklar
Om du använder lagerställen för ett lagerställe blir det mycket enklare för dig att leverera, inleverera och flytta artiklar om du tilldelar dem standardlagerställen. När en artikel tilldelas en standardlagerplats kommer denna lagerplats att föreslås varje gång du påbörjar en transaktion för artikeln. Standardlagerställen definieras på sidan **Lagerställesinnehåll**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Så här tilldelar du en standardlagerplats till en artikel
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Lagerställesinnehålluppl förslag** och välj sedan relaterad länk.  
2.  Fyll i lagerställeskoden och information om artiklar för respektive lagerplats som du vill ange som standard för en artikel. Se till att välja **Standard** här fältet.  
3.  Välj åtgärden **Skapa lagerställesinnehåll**. Din artikel tilldelas nu standardlagerställen.  

> [!NOTE]  
>  Vid införsel av artiklar som inte har tilldelats någon standardlagerplats, kommer den lagerplats där artikeln införs att anges som standardlagerplats.  

## <a name="to-change-the-default-bin-for-an-item"></a>Så här ändrar du standardlagerställen en artikel  
Ibland kan det bli nödvändigt att ändra fördelningen av standardlagerplats för en viss artikel, eller tilldela en ny artikel en standardlagerplats.    
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **lagerställesinnehåll** och välj sedan relaterad länk.  
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