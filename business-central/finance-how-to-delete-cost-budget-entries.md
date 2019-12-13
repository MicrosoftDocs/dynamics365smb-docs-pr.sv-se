---
title: Så här - Ta bort kostnadsbudgettransaktioner | Microsoft Docs
description: Du använder batch-jobbet Ta bort kostnadsbudgettransaktioner för att rätta kostnadsbudgettransaktioner i kostnadsbudgetjournalen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 04510e87789e6d69b33009be7ebbaf7a405d0dff
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882706"
---
# <a name="delete-cost-budget-entries"></a>Ta bort kostnadsbudgettransaktioner
Du använder batch-jobbet **Ta bort kostnadsbudgettransaktioner** för att rätta kostnadsbudgettransaktioner i kostnadsbudgetjournalen.  

För att förhindra luckor i kostnadsbudgettransaktionerna och kostnadsjournalstransaktionerna kan du inte ta bort en enstaka post eller en gruppera poster i mitten av listan över registerposter.  

### <a name="to-delete-a-cost-budget-entry"></a>Ta bort kostnadsbudgettransaktioner  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Ta bort kostnadsbudgettransaktioner** och välj sedan relaterad länk.  

    **Till journalnr** -fältet innehåller det sista registerpostnumret och kan inte ändras.  

    Använd fältet **från att registrera nr** för att välja ett registerpostnummer från vilket borttagningen ska börja.  
2.  Välj **OK** för att ta bort de valda kostnadsbudgettransaktionerna.  

> [!NOTE]  
>  För att undvika ofrivillig borttagning av kostnadsbudgettransaktioner kan du stänga registerposter genom att markera raderna som **Avslutade** i fältet **Avslutat** på sidan **Kostnadsbudgetregister**.  

## <a name="see-also"></a>Se även  
[Redovisa kostnader](finance-manage-cost-accounting.md)
[Skapa kostnadsbudgetar](finance-create-cost-budgets.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
