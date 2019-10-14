---
title: Ange layouten för en kontroll | Microsoft Docs
description: Du kan skapa och skriva ut dina checkar i flera olika format i överensstämmelse med standarder.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: fea52bfa75d953b96aecc0f3e354806324f77d83
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306322"
---
# <a name="select-a-check-layout"></a>Välj en checklayout
Du kan designa dina checkar så att de uppfyller de normer som fastställts av de lokala myndigheterna. Checkbilder kan vara skrivna ut på engelska, franska, eller spanska.

Checkar har utformats för att skrivas ut i både amerikanska och kanadensiska checkbildformat i antingen check-checktalong-check-format eller checktalong-checktalong-check-format.

## <a name="to-select-a-check-layout"></a>Välj en checklayout genom att
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Rapportval - bankkonto** och välj sedan relaterad länk.
2. På sidan **Rapportval - bankkonto** i fältet **Användning** väljer du **Check**.
3. Välj något av följande rapport-ID:

| Rapport-ID | Rapportnamn | Beskrivning |
| --- | --- | --- |
| 1401 |Check |Detta är standardrapporten. |
| 10411 |Check (checktalong/checktalong/check) |Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/checktalong/check. |
| 10412 |Check (checktalong/check/checktalong) |Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/check/checktalong. |
| 10413 |Tre checkar per sida |Den här rapporten är utformad för att skriva ut tre checkar på varje sida. |

När du har upprättat checklayouter, kan du skriva ut checkar från sidan **utbetalningsjournal**. Mer information finns i [Arbeta med checkar](payables-how-work-checks.md).

Om du vill ändra en av dessa standardlayouter använder du antingen Word- eller RDLC-integration. Mer information finns i [så här skapar du och ändrar en anpassad rapport eller dokumentlayout](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se även
[Så här skapar och ändrar du en anpassad rapport eller dokumentlayout](ui-how-create-custom-report-layout.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Hantera bankkonton](bank-manage-bank-accounts.md)   
[Slutföra periodslutsprocesser](year-how-complete-period-end-processes.md)  
[Arbeta med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)
