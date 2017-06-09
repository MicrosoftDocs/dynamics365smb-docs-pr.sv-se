---
title: "Så här definierar du checklayouter | Microsoft Docs"
description: "Mer information om de layouter som är tillgängliga i ekonomin."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6081b6d09fa75b868138817442d6df4d9a8d0d7f
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-define-check-layouts"></a>Så här definierar du checklayouter
Du kan designa dina checkar så att de uppfyller de normer som fastställts av de lokala myndigheterna. Checkbilder kan vara skrivna ut på engelska, franska, eller spanska.

Checkar har utformats för att skrivas ut i både amerikanska och kanadensiska checkbildformat i antingen check-checktalong-check-format eller checktalong-checktalong-check-format.

## <a name="to-define-check-layouts"></a>Om du vill definiera checklayouter
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger du **Rapportval, bankkonto** och väljer sedan relaterad länk.
2. I fönstret **Rapportval - bankkonto.** i fältet **Användning** markerar du **Check**.
3. Välj något av följande rapport-ID:

| Rapport-ID | Rapportnamn | Beskrivning |
| --- | --- | --- |
| 1401 |Check |Detta är standardrapporten. |
| 10401 |Check (checktalong/checktalong/check) |Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/checktalong/check |
| 10411 |Check (checktalong/check/checktalong) |Den här rapporten är utformad för att skriva ut checkar i formatet check/checktalong/check |

När du har upprättat checklayouter, kan du skriva ut checkar från fönstret **utbetalningsjournal**. (Mer information finns i [Arbeta med checkar](payables-how-work-checks.md).

## <a name="see-also"></a>Se även
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Hantera bankkonton](bank-manage-bank-accounts.md)   
[Slutföra periodslutsprocesser](year-how-complete-period-end-processes.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

