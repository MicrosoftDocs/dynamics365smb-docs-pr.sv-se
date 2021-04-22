---
title: Så här registrerar du distributionslagerpersonal | Microsoft Docs
description: Alla användare som utför distributionslageraktiviteter måste registreras som distributionslageranställda som är tilldelade ett standardlagerställe och eventuellt andra lagerställen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4a2ebf2d28833b9cb79c5711fd0314134dfc0915
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784173"
---
# <a name="set-up-warehouse-employees"></a>Registrera distributionslagerpersonal
Alla användare som utför distributionslageraktiviteter måste registreras som distributionslageranställda som är tilldelade ett standardlagerställe och eventuellt andra lagerställen. Denna användarinställning filtrerar alla distributionslageraktiviteter i hela databasen till den anställdes lagerställe, så att han eller hon bara kan utföra distributionslageraktiviteter vid standardlagerstället. En användare kan tilldelas andra lagerställen som han eller hon kan visa aktivitetsrader för, men inte utföra aktiviteterna.

## <a name="to-set-up-warehouse-employees"></a>Så här registrerar du distributionslagerpersonal  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Distributionslagerpersonal** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Välj **Användar-ID** fältet och markera användaren som ska läggas till som distributionslageranvändare. Välj **OK**.  
6.  Gå till fältet **Lagerställekod** och ange koden för lagerstället där användaren ska arbeta.  
7.  Markera kryssrutan **Standard** för att ange att detta är det enda lagerställe som den anställda kan utföra aktiviteter på.  
8.  Upprepa de här stegen om du vill tilldela andra anställda till lagerställen, eller tilldela lagerställen som inte är standard till befintliga anställda.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]