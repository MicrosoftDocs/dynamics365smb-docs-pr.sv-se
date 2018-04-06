---
title: "Designdetaljer - Parti-för-parti | Microsoft Docs"
description: "Lär dig att använda de parti-för-parti som ska kvitta orderkvantiteten baserat på behov."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 712068b5fafb8c5334bf48ddfc9242d21c0995e9
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-lot-for-lot"></a>Designdetaljer: Parti-för-parti
Parti-för-parti-policyn är den mest flexibla eftersom systemet bara reagerar på faktisk efterfrågan, plus att den agerar på förutsedd efterfrågan från prognos och avropsorder, och sedan avräknar orderantalet baserat på efterfrågan. Parti-för-parti-principen gäller A-och B-artiklar där lager kan accepteras men ska undvikas.  
  
På vissa sätt liknar parti-för-parti-principen som orderprincipen, men den har en generisk inställning till artiklar: den kan ta emot antal i lager, och den samlar ihop efterfrågan och motsvarande tillgång i tidsenheter som definieras av användaren.  
  
Tidsenheten definieras i fältet **Tidsenhet**. Systemet arbetar med en lägsta tidsenhet av en dag, eftersom det är den minsta tidsenheten för efterfrågan- och tillgångshändelser i systemet (fast i praktiken kan tidsenheten för produktionsorder och komponentbehov vara sekunder).  
  
Tidsenheten anger också gränser för när en befintlig leveransorder ska omplaneras för att uppfylla en viss efterfrågan. Om tillgången ligger inom tidsenheten kommer den att planeras om framåt eller bakåt för att uppfylla efterfrågan. Annars, om det ligger tidigare, kommer det att orsaka onödig uppbyggnad av lagersaldot och ska avbrytas. Om det ligger senare, kommer en ny leveransorder att skapas i stället.  
  
Med den här metoden det är också möjligt att definiera ett säkerhetslager för att kompensera för möjliga variationer i tillgången, eller för att uppfylla plötslig efterfrågan.  
  
Eftersom leveranspartistorleken baseras på faktiskt behov, kan det vara praktiskt att använda ordermodifierare: avrunda partistorleken uppåt för att uppfylla en viss partistorleksmultipel (eller inköpsenhet), öka beställningen till en viss lägsta partistorlek eller minska partistorleken till det angivna högsta antalet (och skapa därmed två eller flera leveranser för att erhålla den totala behovskvantiteten).  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md)   
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)
