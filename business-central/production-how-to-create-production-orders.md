---
title: "Så här skapar du ett produktionsorderhuvud | Microsoft Docs"
description: "Du kan skapa en produktionsorder manuellt och första steget är då att skapa ett produktionsorderhuvud."
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
ms.openlocfilehash: 13d699dbeb8fe2c3979a7b6bd330b14f077d2d3c
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="create-production-order-headers"></a>Så här skapar du produktionsorderhuvud
Du kan skapa en produktionsorder manuellt och första steget är då att skapa ett produktionsorderhuvud.

Produktionsorder skapas vanligtvis automatiskt av en planeringsfunktion för att uppfylla ett behov som är känt. Mer information finns i [Planering](production-planning.md).   

I det följande procedur skapas en fast planerad produktionsorder. Du kan också skapa produktionsorder med annan status.  

## <a name="to-create-a-production-order-header"></a>Så här skapar du ett produktionsorderhuvud  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Fasta planerade prod.order** och välj sedan relaterad länk.  
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
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

