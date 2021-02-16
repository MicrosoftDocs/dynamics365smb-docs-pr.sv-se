---
title: Fält som krävs för att slutföra processer | Microsoft Docs
description: Få mer information om de fält som är markerade med en röd asterisk som anger att de är obligatoriska och måste fyllas i för att slutföra en process.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: f525077069107e1365728aaaaf1e4791a250c6ee
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760373"
---
# <a name="detecting-mandatory-fields"></a>Identifiera obligatoriska fält
När du anger data på sidor i [!INCLUDE[prod_short](includes/prod_short.md)], markeras vissa fält med en röd asterisk. Den röda asterisken betyder att fältet måste fyllas för att slutföra en viss process som använder fältet, till exempel bokföra en transaktion som använder värdet i fältet.

Även om fältet innehåller en asterisk tvingas du inte att fylla u fältet innan du fortsätter till andra fält eller avslutar sidan. Den röda asterisken fungerar endast som en påminnelse att du kommer att spärras från att slutföra en viss process.

## <a name="examples"></a>Exempel
På sidan **Kundkort** visas den röda asterisken i fältet **Namn** i fältet **Skatteområdeskod** och i fälten för bokföringsmallar för att visa att du inte kan bokföra en försäljningstransaktion för kunden om inte fälten fylls i.

På sidan **Artikelkort** visas den röda asterisken i fälten **Beskrivning** och Basenhet för att visa att du inte kan ange artikeln på en dokumentrad, t.ex försäljningsorder, om inte detta fält fylls i.

## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
