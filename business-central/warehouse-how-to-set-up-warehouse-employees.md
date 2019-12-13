---
title: Så här registrerar du distributionslagerpersonal | Microsoft Docs
description: Alla användare som utför distributionslageraktiviteter måste registreras som distributionslageranställda som är tilldelade ett standardlagerställe och eventuellt andra lagerställen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 624603a2610ca07388c0b84d13b0707e06e92a18
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881546"
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
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
