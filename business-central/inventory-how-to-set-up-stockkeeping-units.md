---
title: Så här konfigurerar du lagerställeenheter | Microsoft Docs
description: Du kan använda lagerställeenheter för att registrera artikelinformation som rör ett visst lagerställe eller en viss variantkod.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 50bf3695a135652ec422bb187f1ff2fef06f3a35
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "934218"
---
# <a name="set-up-stockkeeping-units"></a>Ställa in lagerställeenheter
Du kan använda lagerställeenheter för att registrera artikelinformation som rör ett visst lagerställe eller en viss variantkod.  

 Lagerplatsenheter fungerar som komplement till artikelkort. De ersätter dem inte även om de är relaterade till dem. Med lagerställeenheter kan du ha olika information om en artikel på ett visst lagerställe (t.ex. ett distributionslager eller ett distributionscenter) eller om en särskild variant, (t.ex. olika hyllnummer och olika återanskaffningsinformation) av samma artikel.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Så här skapar du lagerställeenheter  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lagerställeenheter** och välj sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3.  Fyll i fälten på kortet. Följande fält är obligatoriska: **Artikelnr**, **Lagerställekod**och/eller **Variantkod**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

När du har skapat den första lagerställeenheten för en artikel, markeras kryssrutan **Lagerställeenhet finns** på **artikelkortet**.  

Om du vill skapa flera lagerställeenheter för en artikel, kan du använda batch-jobbet **Skapa lagerställeenhet**.  

> [!NOTE]  
>  Informationen på **lagerställeenhetskortet** har högre prioritet än informationen på **artikelkortet**.

> [!Warning]
> Om LAGERSTÄLLEENHETEN levereras via produktion, kommer inte fältet **Standardkostnad** användas för fakturering, och justera den faktiska kostnaden för den producerade artikeln. I stället används fältet **Standardkostnad** på den underliggande artikelkortet, och eventuella avvikelser beräknas mot kostnadsandelar för artikeln.<br /><br />
> Eftersom produktionsstrukturer och operationsföljden inte kan tilldelas Lagerställekonfiguration, är styckkostnaden summerad och den relaterade beräkningen av kostnad delar inte heller tillgängliga på Lagerställeenheter. Mer information finns i [Om att beräkna standardkostnad](finance-about-calculating-standard-cost.md).

## <a name="see-also"></a>Se även  
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
