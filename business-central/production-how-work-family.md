---
title: Arbeta med produktionsfamiljer inom produktion
description: Huvuduppgiften när du anpassar en baskalender för företaget, eller någon av dess affärspartner, är att ange eventuella ändringar av status som arbetsdag eller ledig dag.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000790, 99000791, 99000792, 99000793
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9732817de350d4fe709802b9726a3ad8d364ec5e
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521916"
---
# <a name="work-with-production-families"></a>Arbeta med produktionsfamiljer

En produktionsfamilj är en grupp enskilda artiklar med liknande tillverkningsprocesser. Om du utformar produktionsfamiljer kan vissa artiklar tillverkas två eller flera gånger i en produktion, vilket optimerar materialförbrukningen.

I fältet **Antal** på sidan **Familj** anger du den kvantitet som ska produceras när hela familjen har tillverkats en gång.

## <a name="example"></a>Exempel

I stansningsprocesser kan fyra enheter av en artikel produceras av ett ark och tio enheter av en annan artikel av samma ark. Stansningsmaskinen stansar alla 14 enheterna i ett steg.

Genom att skapa produktionsfamiljer minskas spillet eftersom materialet som vanligtvis blir över när stora enheter produceras kan användas till produktionen av små enheter.

## <a name="to-set-up-a-production-family"></a>Så här skapar du produktionfamilj

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **familjer** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a>Om du vill skapa baserat på en produktionsfamilj

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Fast planerad prod.order** och väljer sedan relaterad länk.
2. Skapa en nu produktionsorder. För mer information, se [Skapa produktionsorder](production-how-to-create-production-orders.md).
3. I fältet **Ursprungstyp** väljer du **Familj**.  
4. I fältet **Ursprungsnr.** väljer du relevant produktionsfamilj.

## <a name="see-also"></a>Se även

[Skapa produktionsstrukturer](production-how-to-create-production-boms.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)
[Planering](production-planning.md)   
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]