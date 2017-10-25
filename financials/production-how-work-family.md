---
title: "SÅ här använder du objektfamiljer i produktion | Microsoft Docs"
description: "Huvuduppgiften när du anpassar en baskalender för företaget, eller någon av dess affärspartner, är att ange eventuella ändringar av status som arbetsdag eller ledig dag."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 060c58991ae48ba768f5c1c0bd7442228e6bc976
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-production-families"></a>Så här: arbeta med produktionsfamiljer
En produktionsfamilj är en grupp enskilda artiklar med liknande tillverkningsprocesser. Om du utformar produktionsfamiljer kan vissa artiklar tillverkas två eller flera gånger i en produktion, vilket optimerar materialförbrukningen.

I fältet **Antal** i fönstret **Familj** anger du den kvantitet som ska produceras när hela familjen har tillverkats en gång.

## <a name="example"></a>Exempel
I stansningsprocesser kan fyra enheter av en artikel produceras av ett ark och tio enheter av en annan artikel av samma ark. Stansningsmaskinen stansar alla 14 enheterna i ett steg.

Genom att skapa produktionsfamiljer minskas spillet eftersom materialet som vanligtvis blir över när stora enheter produceras kan användas till produktionen av små enheter.

## <a name="to-set-up-a-production-family"></a>Så här skapar du produktionfamilj
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Familjer** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-familily"></a>Om du vill skapa baserat på en produktionsfamilj
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Fasta planerade prod.order** och välj sedan relaterad länk.
2. Skapa en nu produktionsorder. Mer information finnsi [Så här skapar du ett produktionsorder](production-how-to-create-production-orders.md).
3. I fältet **Ursprungstyp** väljer du **Familj**.  
4. I fältet **Ursprungsnr.** väljer du relevant produktionsfamilj.

## <a name="see-also"></a>Se även
[Så här skapar du nya produktionsstrukturer](production-how-to-create-production-boms.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planerad](production-planning.md)   
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

