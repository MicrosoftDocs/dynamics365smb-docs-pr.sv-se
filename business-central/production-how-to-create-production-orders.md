---
title: Så här skapar du ett produktionsorderhuvud | Microsoft Docs
description: Du kan skapa en produktionsorder manuellt och första steget är då att skapa ett produktionsorderhuvud.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 76d4b69de41343815175a7acd4329bb47b889f5a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759374"
---
# <a name="create-production-order-headers"></a>Så här skapar du produktionsorderhuvud
Du kan skapa en produktionsorder manuellt och första steget är då att skapa ett produktionsorderhuvud.

Produktionsorder skapas vanligtvis automatiskt av en planeringsfunktion för att uppfylla ett behov som är känt. Mer information finns i [Planering](production-planning.md).   

I det följande procedur skapas en fast planerad produktionsorder. Du kan också skapa produktionsorder med annan status.  

## <a name="to-create-a-production-order-header"></a>Så här skapar du ett produktionsorderhuvud  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Fast planerad prod.order** och välj sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3.  I fältet **Nr.** skriver du numret på den artikel som har beställts.  
4.  Välj produktionsorderns ursprung i fältet **Ursprungstyp**.

    Här kan du välja att skapa en familj av artiklar. Mer information finns i [Så här arbetar du med produktionsfamiljer](production-how-work-family.md).
5.  Välj artikelnummer, familj eller försäljningshuvud som produktionsordern ska skapas för i fältet **Ursprungsnr** .  
6.  Fyll i fälten **Antal** och **Förfallodatum** enligt aktuella specifikationer.  

När produktionsbehov ändras, till exempel komponenter och operationer, kan du snabbt omplanera produktionsordern. Mer information finns i [Omplanera eller uppdatera produktionsorder direkt](production-how-to-replan-refresh-production-orders.md). 

## <a name="see-also"></a>Se även  
[Produktion](production-manage-manufacturing.md)    
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]