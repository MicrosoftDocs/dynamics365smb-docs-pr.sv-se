---
title: Ångra monteringsboking
description: Lär dig korrigera misstag i en bokförd monteringsorder.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# Ångra monteringsboking

Ångra bokföringen av en monteringsorder för att korrigera ett misstag eller ta bort en oönskad bokföring.

När du återställer en bokförd monteringsorder, skapas korrigerande artikeltransaktioner för att återföra de ursprungliga transaktionerna. Varje positivt utflödestransaktion för monteringsartikeln återförs av en negativ utflödestransaktion. Varje negativ förbrukningstransaktion för en monteringskomponent återförs av en positiv förbrukningstransaktion. Fast kostnad-koppling skapas automatiskt mellan korrigerande och ursprungliga transaktionerna som visas för att garantera exakt kostnadsåterställning.  

När du återställer en helt bokförd monteringsorder kan du återskapa den ursprungliga ordern. Om du till exempel vill göra korrigeringar innan du bokför dem igen.  

När du återställer delvis bokförda monteringsorder, påverkas alla antalfält, till exempel **Monterad kvantitet**, **Förbrukat antal** och **Återstående antal**, som återställs till värdena de hade innan bokföringen.  

Om du skapar om eller återställer monteringsorder måste artikeln i den ursprungliga bokföringen uppfylla följande villkor:  

* Den finns fortfarande i lager. D.v.s. den har inte sålts eller förbrukats av utgående transaktioner.  
* Den är inte reserverad.  
* Den finns på lagerstället som den tillverkades till.  

Monteringsorder kan endast återställas om antalet rader och sekvensen av rader på den ursprungliga monteringsorder inte ändras.  

> [!TIP]  
> För att lösa konflikter som orsakats av ändringar i rader, kan du manuellt återföra ändringar på raderna i fråga, innan du återställer den bokförda monteringsorder. Du kan bokföra monteringsorder fullständigt och skapa den på nytt, när du ångrar bokföringen.  

Nedan beskrivs hur du återställer bokförda monteringsorder som innehåller artiklar som monterades mot lager. Om du vill ångra bokförda monteringsorder med artiklar som monterats mot kundorder använder du åtgärden **Återställ utleverans** för den tillhörande bokförda utleveransen. Om du vill veta mer om återställa utleveranser går du till [Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md). Återställa den bokförda monteringsordern sker på samma sätt som beskrivs i den här artikeln.  

## Om du vill ångra bokföring av en monteringsorder

Du kan ångra helt eller delvis bokförda monteringsorder.

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bokförda monteringsorder** och väljer sedan relaterad länk.  

   Varje delbokföringstyp skapar en separat bokförda monteringsorder.  
2. Öppna den bokförda monteringsordern som du vill ångra och välj sedan åtgärden **Ångra montering**.  

    Om den bokförda monteringsordern är kopplad till en helt bokförd monteringsorder som har tagits bort, kan du återskapa den borttagna ordern. Du kan till exempel skapa ordern på grund av att du vill omarbeta den.  
3. Välj **Ja** om du vill skapa monteringsorder igen. Välj **nej** om du vill ångra bokföringen, utan att skapa den kopplade monteringsordern på nytt.  

Fältet **Återförd** på monteringsordern ändras till **Ja**. Bokföringen av monteringsorder har nu återförts. Du kan hantera hela monteringsordern om du väljer att återskapa den, eller den öppna monteringsorder som du har återställt till det ursprungliga tillståndet.  

> [!NOTE]  
> Om du vill återställa antal från flera delbokföringar i en monteringsorder måste du ångra alla bokförda monteringsorder genom att följa steg 1 till 3.  

## Se även

[Monteringshantering](assembly-assemble-items.md)  
[Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md)  
[Behandla försäljningsreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md)  
[Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Warehouse Management – översikt](design-details-warehouse-management.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]