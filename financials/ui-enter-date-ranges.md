---
title: "Ställa in datumintervall i Dynamics 365 Business edition | Microsoft Docs"
description: "Lära dig hur du får en rapport med data från specifika tidsperioder med datumintervall i Dynamics 365 Business edition."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: fee6a5d7ce6603829ed98913b7e370a53239ee3e
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---
# <a name="entering-date-ranges-in-dynamics-365-business-edition"></a>Mata in datumintervall i Dynamics 365 Business edition 
Du kan ange filter som innehåller ett startdatum och ett slutdatum om du vill visa enbart de data som finns i datumintervallet eller tidsintervallet. Speciella regler gäller för hur du kan ange datumintervall. Ta **10 högsta kund** som exempel:

![Ange ett datumintervall på sidan för begäran för listan över 10 högsta kund](./media/ui-enter-date-ranges/customer-top10-list.png)

Här kan du begränsa rapporten till ett datumintervall, till exempel de två senaste veckorna eller totalt 6 veckor eller det intervall du vill använda. Om du vill ange datumintervall, ange datum och använda någon **...** Eller **|** för att ange projektintervall. I vårt exempel, om du vill visa de 10 främsta kunderna för de första två veckorna ställer du in datumfiltret på *05 01 17..05 14 17*.
Här följer några andra exempel:

| Betydelse | Exempel | Inkluderade transaktioner |
|---|---|---|
|Lika med| 12 15 16 |Endast de som bokförts 15 december 2016.|
|Intervall| 12 15 16..01 15 17<br /><br />..12 15 16|De som bokförts på datum mellan och inklusive 15 december 2016 och 15 januari 2017.<br /><br />De som bokförts 02-12-15 eller tidigare.|
|Antingen eller|12 15 16&#124;12 16 16|Transaktioner registrerade antingen den 15 December eller 16 December 2016. Om det finns transaktioner som bokförs båda dagarna kommer alla att visas.|

Du kan också kombinera formattyperna.

| Exempel | Inkluderade transaktioner |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Transaktioner som bokförts antingen den 15 december 2016, eller på datum mellan och inklusive 01 december 2016 och 31 maj 2017. |
|..12 14 16&#124;12 30 16.. | Transaktioner bokförda 14 December eller tidigare, eller transaktioner bokförda 30 December eller senare – d.v.s. alla transaktioner utom de som bokförts på datum mellan och inklusive 15 December och 29. |

Observera att vi har använt Amerikanskt datumformat MMDDÅÅ här. När [!INCLUDE[d365fin](includes/d365fin_md.md)] blir tillgängliga för andra marknader, kommer du att kunna använda de format som används.

## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Ange villkor i filter](ui-enter-criteria-filters.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

