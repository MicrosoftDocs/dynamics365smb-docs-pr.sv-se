---
title: "Så här - Ta bort kostnadsbudgettransaktioner | Microsoft Docs"
description: "Du använder batch-jobbet **Ta bort kostnadsbudgettransaktioner** för att rätta kostnadsbudgettransaktioner i kostnadsbudgetjournalen."
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
ms.openlocfilehash: cdd7f7cfb2645d780df47bfb75ec7392c1739843
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="delete-cost-budget-entries"></a>Ta bort kostnadsbudgettransaktioner
Du använder batch-jobbet **Ta bort kostnadsbudgettransaktioner** för att rätta kostnadsbudgettransaktioner i kostnadsbudgetjournalen.  

För att förhindra luckor i kostnadsbudgettransaktionerna och kostnadsjournalstransaktionerna kan du inte ta bort en enstaka post eller en gruppera poster i mitten av listan över registerposter.  

### <a name="to-delete-a-cost-budget-entry"></a>Ta bort kostnadsbudgettransaktioner  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Ta bort kostnadsbudgettransaktioner** och välj sedan relaterad länk.  

    **Till journalnr** -fältet innehåller det sista registerpostnumret och kan inte ändras.  

    Använd fältet **från att registrera nr** för att välja ett registerpostnummer från vilket borttagningen ska börja.  
2.  Välj **OK** för att ta bort de valda kostnadsbudgettransaktionerna.  

> [!NOTE]  
>  För att undvika ofrivillig borttagning av kostnadsbudgettransaktioner kan du stänga registerposter genom att markera raderna som **Avslutade** i fältet **Avslutat**  i fönstret **Kostnadsbudgetregister**.  

## <a name="see-also"></a>Se även  
[Redovisa kostnader](finance-manage-cost-accounting.md)
[Skapa kostnadsbudgetar](finance-create-cost-budgets.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

