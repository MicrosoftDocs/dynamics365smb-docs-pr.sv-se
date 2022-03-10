---
title: Visa databaslås
description: Lär dig mer om hur du kan visa information om kunddatabaslås direkt från klientgränssnittet i Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9511
ms.date: 06/14/2021
ms.author: jswymer
ms.openlocfilehash: 0a2561eea331ffbaeb058dee2ee13caf0a82d18c
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143692"
---
# <a name="viewing-database-locks"></a>Visa databaslås

Databaslåsning styr åtkomsten för flera användare till samma data samtidigt. Om du vill skydda en transaktion mot att andra transaktioner ändrar samma data kommer den första transaktionen att låsa datan. Låset förblir aktiverat tills transaktionen är klar.

Användare kan hindras från att slutföra transaktioner på den låsta datan. Oftast visas ett meddelande som anger låsstatusen.

## <a name="to-view-database-locks"></a>För att visa databaslås

Välj ![Sök efter sida eller rapport.](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport") anger du **Databaslås** och väljer sedan relaterad länk.

Sidan **Databaslås** ger en översiktsbild av alla aktuella databaslås.

Mer information om hur du låser databasen finns i [Övervaka databaslås](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) i hjälpavsnittet för Business Central-utvecklare och IT-proffs.

## <a name="see-also"></a>Se även

[Övervaka databaslås](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]