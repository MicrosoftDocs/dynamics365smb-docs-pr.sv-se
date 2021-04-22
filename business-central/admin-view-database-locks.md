---
title: Visa databaslås
description: Lär dig mer om hur du kan visa information om databaslås direkt från klientgränssnittet i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: b53677ab57d6c48b015bb0dd47ea6e315f8e80c3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776922"
---
# <a name="viewing-database-locks"></a>Visa databaslås

Databaslåsning styr åtkomsten för flera användare till samma data samtidigt. Om du vill skydda en transaktion mot att andra transaktioner ändrar samma data kommer den första transaktionen att låsa datan. Låset förblir aktiverat tills transaktionen är klar.

Användare kan hindras från att slutföra transaktioner på den låsta datan. Oftast visas ett meddelande som anger låsstatusen.

## <a name="to-view-database-locks"></a>För att visa databaslås

Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **Databaslås** och välj sedan relaterad länk.

Sidan **Databaslås** ger en översiktsbild av alla aktuella databaslås.

Mer information om hur du låser databasen finns i [Övervaka databaslås](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) i hjälpavsnittet för Business Central-utvecklare och IT-proffs.

## <a name="see-also"></a>Se även

[Övervaka databaslås](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]