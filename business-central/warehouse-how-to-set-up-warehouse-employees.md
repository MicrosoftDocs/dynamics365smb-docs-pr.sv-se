---
title: Registrera distributionslagerpersonal
description: Alla användare som utför distributionslageraktiviteter måste registreras som distributionslageranställda som är tilldelade ett standardlagerställe och eventuellt andra lagerställen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7328, 7348
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7c04e2e81876628a8b6fe9534bb7ecdbb960bcc8
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511323"
---
# <a name="set-up-warehouse-employees"></a>Registrera distributionslagerpersonal

Alla användare som utför distributionslageraktiviteter måste registreras som distributionslageranställda som är tilldelade ett standardlagerställe och eventuellt andra lagerställen. Denna användarinställning filtrerar alla distributionslageraktiviteter i hela databasen till den anställdes lagerställe, så att han eller hon bara kan utföra distributionslageraktiviteter vid standardlagerstället. En användare kan tilldelas andra lagerställen som han eller hon kan visa aktivitetsrader för, men inte utföra aktiviteterna.

## <a name="to-set-up-warehouse-employees"></a>Så här registrerar du distributionslagerpersonal  

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **distributionslagerpersonal** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Välj **Användar-ID** fältet och markera användaren som ska läggas till som distributionslageranvändare. Välj **OK**.  
4. Gå till fältet **Lagerställekod** och ange koden för lagerstället där användaren ska arbeta.  
5. Markera kryssrutan **Standard** för att ange att detta är det enda lagerställe som den anställda kan utföra aktiviteter på.  
6. Upprepa de här stegen om du vill tilldela andra anställda till lagerställen, eller tilldela lagerställen som inte är standard till befintliga anställda.  

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md) 
[Monteringshantering](assembly-assemble-items.md)
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]