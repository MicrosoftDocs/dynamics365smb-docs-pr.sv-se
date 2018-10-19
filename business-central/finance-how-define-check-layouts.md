---
title: "Ange layouten för en kontroll | Microsoft Docs"
description: "Du kan skapa och skriva ut dina checkar i flera olika format i överensstämmelse med standarder."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d8546cd2f713416e50474848e783d61b4b1dc810
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="define-check-layouts"></a>Definiera checklayouter
Du kan designa dina checkar så att de uppfyller de normer som fastställts av de lokala myndigheterna. Checkbilder kan vara skrivna ut på engelska, franska, eller spanska.

Checkar har utformats för att skrivas ut i både amerikanska och kanadensiska checkbildformat i antingen check-checktalong-check-format eller checktalong-checktalong-check-format.

## <a name="to-define-check-layouts"></a>Om du vill definiera checklayouter
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Rapportval - bankkonto** och välj sedan relaterad länk.
2. I fönstret **Rapportval - bankkonto** i fältet **Användning** väljer du **Check**.
3. Välj något av följande rapport-ID:

| Rapport-ID | Rapportnamn | Beskrivning |
| --- | --- | --- |
| 1401 |Check |Detta är standardrapporten. |
| 10401 |Check (checktalong/checktalong/check) |Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/checktalong/check. |
| 10411 |Check (checktalong/check/checktalong) |Den här rapporten är utformad för att skriva ut checkar i formatet check/checktalong/check. |

När du har upprättat checklayouter, kan du skriva ut checkar från fönstret **utbetalningsjournal**. Mer information finns i [Arbeta med checkar](payables-how-work-checks.md).

## <a name="see-also"></a>Se även
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Hantera bankkonton](bank-manage-bank-accounts.md)   
[Slutföra periodslutsprocesser](year-how-complete-period-end-processes.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

