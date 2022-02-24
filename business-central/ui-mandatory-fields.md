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
ms.date: 10/01/2019
ms.author: solsen
ms.openlocfilehash: 6cab6247c8edb050a038ef7641b646f1a7412588
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310834"
---
# <a name="detecting-mandatory-fields"></a>Identifiera obligatoriska fält
När du anger data på sidor i [!INCLUDE[d365fin](includes/d365fin_md.md)], markeras vissa fält med en röd asterisk. Den röda asterisken betyder att fältet måste fyllas för att slutföra en viss process som använder fältet, till exempel bokföra en transaktion som använder värdet i fältet.

Även om fältet innehåller en asterisk tvingas du inte att fylla u fältet innan du fortsätter till andra fält eller avslutar sidan. Den röda asterisken fungerar endast som en påminnelse att du kommer att spärras från att slutföra en viss process.

## <a name="examples"></a>Exempel
På sidan **Kundkort** visas den röda asterisken i fältet **Namn** i fältet **Skatteområdeskod** och i fälten för bokföringsmallar för att visa att du inte kan bokföra en försäljningstransaktion för kunden om inte fälten fylls i.

På sidan **Artikelkort** visas den röda asterisken i fälten **Beskrivning** och Basenhet för att visa att du inte kan ange artikeln på en dokumentrad, t.ex försäljningsorder, om inte detta fält fylls i.

## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
