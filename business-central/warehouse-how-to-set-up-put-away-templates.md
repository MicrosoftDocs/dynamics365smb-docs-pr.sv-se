---
title: Så här skapar du artikelinförselmallar | Microsoft Docs
description: Med dirigerad artikelinförsel och plockning går det alltid att hitta den lämpligaste lagerstället för artiklarna enligt den artikelinförselmall som du har skapat för distributionslagret, de lagerplatsordningar som du har angett för lagerställena samt de lägsta och högsta antal som du har definierat för de fasta lagerställena.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 336a9aa748d997d2cf4c5ae9a93cab6f96495fd6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784198"
---
# <a name="set-up-put-away-templates"></a>Skapa artikelinförselmallar

Med dirigerad artikelinförsel och plockning går det alltid att hitta den lämpligaste lagerstället för artiklarna enligt den artikelinförselmall som du har skapat för distributionslagret, de lagerplatsordningar som du har angett för lagerställena samt de lägsta och högsta antal som du har definierat för de fasta lagerställena.  

Du kan skapa flera artikelinförselmallar och välja en av dem för att styra allmänna artikelinförslar i distributionslagret. Du kan även välja en artikelinförselmall för valfri artikel eller lagerställeenhet som kan ha specialkrav beträffande artikelinförsel.  

## <a name="to-set-up-put-away-templates"></a>Så här skapar du artikelinförselmallar:

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **artikelinförselmallar** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Ange en kod som är unik för den mall som du ska skapa.  
4. Ange vid behov en kort beskrivning.  
5. Fyll i den första raden med de lagerplatskrav som du vill ska uppfyllas först och främst när en artikelinförsel föreslås.

    Om du till exempel vill att standard artikelinförselmetoden ska baseras på fasta lagerställen väljer du fältet **Sök fast lagerplats**. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. Fyll i den andra raden med de lagerplatskrav som ska gälla i andra hand vid artikelinförsel till en lagerplats. Den andra raden används endast om det inte går att hitta en lagerplats som uppfyller kraven på den första raden.  
7. Fortsätt att fylla i raderna tills du har beskrivit alla godtagbara lagerplatsplaceringar som du vill använda vid artikelinförsel.  
8. På den sista raden i artikelinförselmallen markerar du kryssrutan **Sök flytande lagerplats**.  

Du kan skapa olika artikelinförselmallar och sedan använda dem som du vill. Den artikelinförselmall som du har valt för artikeln eller lagerställeenheten om det finns någon. Om de här fälten inte fylls i används den artikelinförselmall som du har valt för distributionslagret på snabbfliken **Lagerplatsprinciper** på lagerställekortet.  

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]