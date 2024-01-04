---
title: Så här skapar du produktionsorderhuvud
description: Du kan skapa en produktionsorder manuellt och första steget är då att skapa ett produktionsorderhuvud.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9325, 99000815, 99000829, 9900083'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Så här skapar du produktionsorderhuvud

Du kan skapa en produktionsorder manuellt och första steget är då att skapa ett produktionsorderhuvud.

Produktionsorder skapas vanligtvis automatiskt av en planeringsfunktion för att uppfylla ett behov som är känt. Mer information finns i [Planering](production-planning.md).  

I det följande procedur skapas en fast planerad produktionsorder. Du kan också skapa produktionsorder med annan status.  

## Så här skapar du ett produktionsorderhuvud

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Fast planerad prod.order** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I fältet **Nr.** skriver du numret på den artikel som har beställts.  
4. Välj produktionsorderns ursprung i fältet **Ursprungstyp**.

    Här kan du välja att skapa en familj av artiklar. Mer information finns i [Så här arbetar du med produktionsfamiljer](production-how-work-family.md).
5. Välj artikelnummer, familj eller försäljningshuvud som produktionsordern ska skapas för i fältet **Ursprungsnr** .  
6. Fyll i fälten **Antal** och **Förfallodatum** enligt aktuella specifikationer.  

När produktionsbehov ändras, till exempel komponenter och operationer, kan du snabbt omplanera produktionsordern. Mer information finns i [Omplanera eller uppdatera produktionsorder direkt](production-how-to-replan-refresh-production-orders.md).  

## Se även

[Produktion](production-manage-manufacturing.md)
[Konfigurera produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]