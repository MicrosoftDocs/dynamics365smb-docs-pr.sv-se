---
title: Fält som krävs för att slutföra processer | Microsoft Docs
description: Få mer information om de fält som är markerade med en röd asterisk som anger att de är obligatoriska och måste fyllas i för att slutföra en process.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 8c631dcbb2c6afa6abec9ace86df0f0babb23b2d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385505"
---
# <a name="detecting-mandatory-fields"></a>Identifiera obligatoriska fält
När du anger data på sidor i [!INCLUDE[prod_short](includes/prod_short.md)], markeras vissa fält med en röd asterisk. Den röda asterisken betyder att fältet måste fyllas för att slutföra en viss process som använder fältet, till exempel bokföra en transaktion som använder värdet i fältet.

Även om fältet innehåller en asterisk tvingas du inte att fylla u fältet innan du fortsätter till andra fält eller avslutar sidan. Den röda asterisken fungerar endast som en påminnelse att du kommer att spärras från att slutföra en viss process.

## <a name="examples"></a>Exempel
På sidan **Kundkort** visas den röda asterisken i fältet **Namn** i fältet **Skatteområdeskod** och i fälten för bokföringsmallar för att visa att du inte kan bokföra en försäljningstransaktion för kunden om inte fälten fylls i.

På sidan **Artikelkort** visas den röda asterisken i fälten **Beskrivning** och Basenhet för att visa att du inte kan ange artikeln på en dokumentrad, t.ex försäljningsorder, om inte detta fält fylls i.

## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]