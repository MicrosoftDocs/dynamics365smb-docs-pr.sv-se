---
title: Visa databaslås
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1153ffc97d0f22c889ff23c5a27a8c0446b17018
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196392"
---
# <a name="viewing-database-locks"></a>Visa databaslås

## <a name="about-locks"></a>Om lås

Databaslåsning styr åtkomsten för flera användare till samma data samtidigt. Om du vill skydda en transaktion mot att andra transaktioner ändrar samma data kommer den första transaktionen att låsa datan. Låset förblir aktiverat tills transaktionen är klar.

Användare kan hindras från att slutföra transaktioner på den låsta datan. Oftast visas ett meddelande som anger låsstatusen.

## <a name="to-view-database-locks"></a>För att visa databaslås

Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **Databaslås** och välj sedan relaterad länk.

Sidan **Databaslås** ger en översiktsbild av alla aktuella databaslås.

Mer information om hur du låser databasen finns i [Övervaka databaslås](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) i hjälpavsnittet för Business Central-utvecklare och IT-proffs.

## <a name="see-also"></a>Se även

[Övervaka databaslås](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) 
