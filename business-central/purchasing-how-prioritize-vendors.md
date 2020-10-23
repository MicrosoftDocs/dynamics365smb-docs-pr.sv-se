---
title: Tilldela en leverantör till en prioritetsnivå | Microsoft Docs
description: Du kan tilldela nummer till dina leverantörer för att prioritera dessa och underlätta betalningsförslag i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 177fb324e39a59abbfc1b50e6ceaa34d4ae06f56
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926903"
---
# <a name="prioritize-vendors"></a>Prioritera leverantörer
[!INCLUDE[d365fin](includes/d365fin_md.md)] används för att ta fram olika betalningsförslag, t.ex. betalningar som snart förfaller eller betalningar för vilka en rabatt kan erhållas. Mer information finns i [Föreslå leverantörsbetalningar](payables-how-suggest-vendor-payments.md).

Först måste du prioritera leverantörerna genom att tilldela nummer till dem.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a>Så här prioriterar du leverantörer:
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Leverantör** och välj sedan relaterad länk.
2. Välj lämplig leverantör och sedan **Redigera**.
3. Ange ett nummer i fältet **Prioritet**.

I [!INCLUDE[d365fin](includes/d365fin_md.md)] räknas lägst nummer (förutom 0) som högst prioritet. Om du t.ex. använder 1, 2 och 3 har alltså 1 högst prioritet.

Om du inte vill prioritera en leverantör lämnar du fältet **Prioritet** tomt. Om du sedan använder funktionen för betalningsförslag visas den här leverantören sist i listan, efter de leverantörer som har tilldelats ett prioritetsnummer. Du kan ange valfritt antal prioritetsnivåer alltefter behov.

## <a name="see-also"></a>Se även
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
