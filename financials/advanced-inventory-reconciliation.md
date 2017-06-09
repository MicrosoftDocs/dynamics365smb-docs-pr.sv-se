---
title: "Avancerad: Lageravstämning | Microsoft Docs"
description: "Beskriver hur ditt lagervärde stäms av med redovisningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: post inventory cost to G/L, reconcile inventory
ms.date: 02/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7eb07530fe80f871ef113c95e48bf89da6c29db0
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
## <a name="advanced-inventory-reconciliation"></a>Avancerad: Lageravstämning
När du bokför lagertransaktioner, till exempel försäljningsutleveranser, inköpsfakturor eller lagerjusteringar, registreras de ändrade artikelkostnaderna i artikelvärdesposter. För att återspegla denna förändring i lagervärde i din bokföring kommer lagerkostnaderna automatiskt att bokföras på relaterade lagerkonton i redovisningen. För varje lagertransaktion som bokförs, bokförs lämpliga värden på lagerkontot, justeringskontot och KSV-kontot i redovisningen.

Även om lagerkostnaderna automatiskt bokförs i redovisningen måste du fortsatt säkerställa att varukostnader skickas vidare till relaterade avgående försäljningstransaktioner, i synnerhet när varorna säljs innan du har fakturerat inköpet av varorna. I programmet kallas detta för Kostnadsjustering. Artikelkostnader justeras automatiskt när du bokför artikeltransaktioner, men du kan också justera projektartikelkostnader manuellt. Mer information finns i [Så här justerar du artikelkostnader](inventory-how-adjust-item-costs.md).

## <a name="see-also"></a>Se även
[Lager](inventory-manage-inventory.md)  
[Avancerad: Bästa prisberäkning](advanced-best-price-calculation.md)

