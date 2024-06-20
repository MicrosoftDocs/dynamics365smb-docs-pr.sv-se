---
title: Ta bort kostnadsbudgettransaktioner
description: Du använder batch-jobbet Ta bort kostnadsbudgettransaktioner för att rätta kostnadsbudgettransaktioner i kostnadsbudgetjournalen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 1115
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="delete-cost-budget-entries"></a>Ta bort kostnadsbudgettransaktioner

Du använder batch-jobbet **Ta bort kostnadsbudgettransaktioner** för att rätta kostnadsbudgettransaktioner i kostnadsbudgetjournalen.  

För att förhindra luckor i kostnadsbudgettransaktionerna och kostnadsjournalstransaktionerna kan du inte ta bort en enstaka post eller en gruppera poster i mitten av listan över registerposter.  

## <a name="to-delete-a-cost-budget-entry"></a>Ta bort kostnadsbudgettransaktioner

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Ta bort användaranpassning** och väljer sedan relaterad länk.  

    **Till journalnr** -fältet innehåller det sista registerpostnumret och kan inte ändras.  

    Använd fältet **från att registrera nr** för att välja ett registerpostnummer från vilket borttagningen ska börja.  
2. Välj **OK** för att ta bort de valda kostnadsbudgettransaktionerna.  

> [!NOTE]  
> För att undvika ofrivillig borttagning av kostnadsbudgettransaktioner kan du stänga registerposter genom att markera raderna som **Avslutade** i fältet **Avslutat** på sidan **Kostnadsbudgetregister**.  

## <a name="see-also"></a>Se även

[Redovisa kostnader](finance-manage-cost-accounting.md)
[Skapa kostnadsbudgetar](finance-create-cost-budgets.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
