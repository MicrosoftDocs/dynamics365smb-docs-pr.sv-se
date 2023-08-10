---
title: Så här skapar du lagerställeenheter
description: Använd lagerställeenheter för att registrera artikelinformation som rör ett visst lagerställe eller en viss variant.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/19/2023
ms.custom: bap-template
ms.search.forms: '5704, 5700, 5702, 5701'
---

# <a name="set-up-stockkeeping-units"></a>Konfigurera lagerställeenheter

Använd lagerställeenheter (SKU) för att registrera artikelinformation som rör ett visst lagerställe eller en viss variant. De ger dig möjlighet att lägga till olika typer av information om en artikel på en viss plats, t.ex.:

* Ett lagerställe eller distributionscenter
* Varianter, t.ex. olika hyllnummer och olika återanskaffnings information, för samma artikel  

## <a name="to-set-up-a-stockkeeping-unit"></a>Så här skapar du lagerställeenheter

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **lagerställeenheter** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Fyll i fälten om det behövs. Följande fält är obligatoriska: **Artikelnr**, **Lagerställekod**och/eller **Variantkod**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

När du har skapat den första lagerställeenheten för en artikel, markeras kryssrutan **Lagerställeenhet finns** på **artikelkortet**.  

Om du vill skapa flera lagerställeenheter för en artikel, kan du använda batch-jobbet **Skapa lagerställeenhet**. Lär dig mer om batchjobb i [Använd jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).  

> [!NOTE]  
> Informationen på **lagerställeenhetskortet** har högre prioritet än informationen på **artikelkortet**.

> [!Warning]
> Om LAGERSTÄLLEENHETEN levereras via produktion, kommer inte fältet **Standardkostnad** användas för fakturering, och justera den faktiska kostnaden för den producerade artikeln. I stället använder [!INCLUDE [prod_short](includes/prod_short.md)] värdet i fältet **Standardkostnad** på den underliggande artikelkortet, och eventuella avvikelser beräknas mot kostnadsandelar för artikeln.<br><br>
> Även om du kan tilldela produktionsstrukturer och operationsföljden inte kan tilldelas Lagerställekonfiguration, är styckkostnaden summerad och den relaterade beräkningen av kostnad delar inte heller tillgängliga på Lagerställeenheter. Om du vill veta mer om standardkostnader går du till [Beräkna standardkostnad](finance-about-calculating-standard-cost.md)

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/control-inventory-multiple-locations/)

## <a name="see-also"></a>Se även

[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Monteringshantering](assembly-assemble-items.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
