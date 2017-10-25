---
title: "Tilldela en leverantör till en prioritetsnivå | Microsoft Docs"
description: "Du kan tilldela nummer till leverantörer eller för att prioritera dem och underlätta betalningsförslag i Financials."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2c91b28daf27ddd2b698ffe4338bbf92fd1f9adf
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-prioritize-vendors"></a>Så här prioriterar du leverantörer
[!INCLUDE[d365fin](includes/d365fin_md.md)] används för att ta fram olika betalningsförslag, t.ex. betalningar som snart förfaller eller betalningar för vilka en rabatt kan erhållas. Mer information finns i [Så här föreslår du leverantörsbetalningar](payables-how-suggest-vendor-payments.md).

Först måste du prioritera leverantörerna genom att tilldela nummer till dem.

## <a name="to-prioritize-vendors"></a>Så här prioriterar du leverantörer:
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Leverantör** och välj sedan relaterad länk.
2. Välj lämplig leverantör och sedan **Redigera**.
3. Ange ett nummer i fältet **Prioritet**.

I [!INCLUDE[d365fin](includes/d365fin_md.md)] räknas lägst nummer (förutom 0) som högst prioritet. Om du t.ex. använder 1, 2 och 3 har alltså 1 högst prioritet.

Om du inte vill prioritera en leverantör lämnar du fältet **Prioritet** tomt. Om du sedan använder funktionen för betalningsförslag visas den här leverantören sist i listan, efter de leverantörer som har tilldelats ett prioritetsnummer. Du kan ange valfritt antal prioritetsnivåer alltefter behov.

## <a name="see-also"></a>Se även
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

