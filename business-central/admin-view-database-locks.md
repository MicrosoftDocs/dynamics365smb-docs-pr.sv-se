---
title: Visa databaslås
description: Lär dig mer om hur du kan visa information om databaslås direkt från klientgränssnittet i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6880ffa9a2ab42c1af7c22f9cace64697c9f905b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922323"
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