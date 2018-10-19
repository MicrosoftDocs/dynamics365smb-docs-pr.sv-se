---
title: "Så här: Tilldela standardlagerplatser till artiklar | Microsoft Docs"
description: "Om du använder lagerplatser för ett lagerställe blir det mycket enklare för dig att leverera, inleverera och flytta artiklar om du tilldelar dem standardlagerplatser. När en artikel tilldelas en standardlagerplats kommer denna lagerplats att föreslås varje gång du påbörjar en transaktion för artikeln."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e6c6c8a54ae638fa90bca94e43a38d120b5fd3f6
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="assign-default-bins-to-items"></a>Tilldela standardlagerplatser till artiklar
Om du använder lagerplatser för ett lagerställe blir det mycket enklare för dig att leverera, inleverera och flytta artiklar om du tilldelar dem standardlagerplatser. När en artikel tilldelas en standardlagerplats kommer denna lagerplats att föreslås varje gång du påbörjar en transaktion för artikeln. Standardlagerplatser definieras i fönstret **Lagerplatsinnehåll**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Så här tilldelar du en standardlagerplats till en artikel
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lagerplatsinnehålluppl förslag** och välj sedan relaterad länk.  
2.  Fyll i lagerplatskoden och information om artiklar för respektive lagerplats som du vill ange som standard för en artikel. Se till att välja **Standard** här fältet.  
3.  Välj åtgärden **Skapa lagerplatsinnehåll**. Din artikel tilldelas nu standardlagerplatser.  

> [!NOTE]  
>  Vid införsel av artiklar som inte har tilldelats någon standardlagerplats, kommer den lagerplats där artikeln införs att anges som standardlagerplats.  

## <a name="to-change-the-default-bin-for-an-item"></a>Så här ändrar du standardlagerplatser en artikel  
Ibland kan det bli nödvändigt att ändra fördelningen av standardlagerplats för en viss artikel, eller tilldela en ny artikel en standardlagerplats.    
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lagerplatsinnehåll** och välj sedan relaterad länk.  
2.  Välj tillämplig lagerställekod i fältet **Lagerställefilter**.  
3.  Sök efter aktuell post för standardlagerplatsinnehåll för artikeln och avmarkera kryssrutan **Standardlagerplats**.  
4.  Sök efter raden för lagerplatsinnehåll för den lagerplats som du vill använda som ny standardlagerplats. Markera kryssrutan **Standardlagerplats**.  

> [!NOTE]  
>  När en artikel införs för första gången och den inte har tilldelats någon standardlagerplats, kommer den lagerplats där artikeln införs att anges som standardlagerplats.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

