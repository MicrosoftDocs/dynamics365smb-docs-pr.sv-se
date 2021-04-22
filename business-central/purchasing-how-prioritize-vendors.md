---
title: Tilldela en leverantör till en prioritetsnivå | Microsoft Docs
description: Du kan tilldela nummer till dina leverantörer för att prioritera dessa och underlätta betalningsförslag i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1604113b255a585532677ccb47d7e68d1cc64059
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772785"
---
# <a name="prioritize-vendors"></a>Prioritera leverantörer
[!INCLUDE[prod_short](includes/prod_short.md)] används för att ta fram olika betalningsförslag, t. ex. betalningar som snart förfaller eller betalningar för vilka en rabatt kan erhållas. Mer information finns i [Föreslå leverantörsbetalningar](payables-how-suggest-vendor-payments.md).

Först måste du prioritera leverantörerna genom att tilldela nummer till dem.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a>Så här prioriterar du leverantörer:
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Leverantör** och välj sedan relaterad länk.
2. Välj lämplig leverantör och sedan **Redigera**.
3. Ange ett nummer i fältet **Prioritet**.

I [!INCLUDE[prod_short](includes/prod_short.md)] räknas lägst nummer (förutom 0) som högst prioritet. Om du t. ex. använder 1, 2 och 3 har alltså 1 högst prioritet.

Om du inte vill prioritera en leverantör lämnar du fältet **Prioritet** tomt. Om du sedan använder funktionen för betalningsförslag visas den här leverantören sist i listan, efter de leverantörer som har tilldelats ett prioritetsnummer. Du kan ange valfritt antal prioritetsnivåer alltefter behov.

## <a name="see-also"></a>Se även
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]