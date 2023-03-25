---
title: Så här skapar du lagerställeenheter
description: Du kan använda lagerställeenheter för att registrera artikelinformation som rör ett visst lagerställe eller en viss variantkod.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '5704, 5700, 5702, 5701'
ms.date: 04/01/2021
ms.author: edupont
---
# Ställa in lagerställeenheter

Du kan använda lagerställeenheter för att registrera artikelinformation som rör ett visst lagerställe eller en viss variantkod.  

lagerställetheter fungerar som komplement till artikelkort. De ersätter dem inte även om de är relaterade till dem. Med lagerställeenheter kan du ha olika information om en artikel på ett visst lagerställe (t. ex. ett distributionslager eller ett distributionscenter) eller om en särskild variant, (t. ex. olika hyllnummer och olika återanskaffningsinformation) av samma artikel.  

## Så här skapar du lagerställeenheter  

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **lagerställeenheter** och väljer sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3.  Fyll i fälten på kortet. Följande fält är obligatoriska: **Artikelnr**, **Lagerställekod**och/eller **Variantkod**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

När du har skapat den första lagerställeenheten för en artikel, markeras kryssrutan **Lagerställeenhet finns** på **artikelkortet**.  

Om du vill skapa flera lagerställeenheter för en artikel, kan du använda batch-jobbet **Skapa lagerställeenhet**.  

> [!NOTE]  
>  Informationen på **lagerställeenhetskortet** har högre prioritet än informationen på **artikelkortet**.

> [!Warning]
> Om LAGERSTÄLLEENHETEN levereras via produktion, kommer inte fältet **Standardkostnad** användas för fakturering, och justera den faktiska kostnaden för den producerade artikeln. I stället används fältet **Standardkostnad** på den underliggande artikelkortet, och eventuella avvikelser beräknas mot kostnadsandelar för artikeln.<br /><br />
> Eftersom produktionsstrukturer och operationsföljden inte kan tilldelas Lagerställekonfiguration, är styckkostnaden summerad och den relaterade beräkningen av kostnad delar inte heller tillgängliga på Lagerställeenheter. Mer information finns i [Om att beräkna standardkostnad](finance-about-calculating-standard-cost.md).

## Se relaterad [Microsoft utbildning](/training/modules/control-inventory-multiple-locations/)

## Se även

[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Monteringshantering](assembly-assemble-items.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
