---
title: Designdetaljer - Maximalt antal | Microsoft Docs
description: Principen Maximalt antal är ett sätt att underhålla lagret med hjälp av en beställningspunkt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 857a01bac28d85a35668f3aa01e8807a6f6dc845
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239159"
---
# <a name="design-details-maximum-qty"></a>Designdetaljer: Maximalt antal
Principen Maximalt antal är ett sätt att underhålla lagret med hjälp av en beställningspunkt.  

 Allt som gäller metoden Fast orderkvantitet gäller även för den här metoden. Den enda skillnaden är antalet på i den föreslagna tillgången. När du använder principen för högsta antal definieras beställningsantalet dynamiskt baserat på den planerade lagernivån och kommer därför vanligtvis att skilja sig åt från order till order.  

## <a name="calculated-per-time-bucket"></a>Beräknat per tidsenhet  
 Orderkvantitet bestäms vid tidpunkten (slutet av en tidsenhet) när planeringssystemet identifierar att beställningspunkten har passerats. Vid den här tidpunkten mäter systemet luckan mellan den aktuella planerade lagernivån fram till den angivna beställningsgränsen. Det här fältet utgör antalet som ska beställas. Systemet kontrollerar sedan om tillgång redan har beställts någon annanstans för att tas emot under ledtiden och i så fall minskar antalet på den nya leveransorder genom redan beställda antal.  

 Systemet kontrollerar att det planerade lagret minst når beställningspunktnivån – i händelse användaren har glömt att ange en beställningsgränsnivå.  

## <a name="combines-with-order-modifiers"></a>Kombineras med ordermodifierare  
 Beroende på inställningarna kan det vara bra att kombinera principen Max. ant. med ordermodifierare för att säkerställa en minsta partistorlek eller för att avrunda den till ett heltalsnummer av inköpsenheter, eller dela den i flera partier enligt vad som anges av den maximala orderkvantiteten.  

## <a name="combines-with-calendars"></a>Kombineras med kalendrar  
 Innan du föreslår en ny leveransorder för att uppfylla en beställningspunkt, kontrollerar planeringssystemet om den schemaläggs för en ickearbetsdag enligt alla kalendrar som har definierats i fältet **Baskalenderkod** på sidorna **företagsinformation** och **lagerställekort**.  

 Om det planerade datumet är ett ickearbetsdag flyttar planeringssystemet ordern framåt till nästa arbetsdag. Detta kan leda till att en order som uppfyller en beställningspunkt, inte uppfyller vissa specifika behov. För sådan ej balanserad efterfrågan skapar planeringssystemet en extra leverans.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md)   
 [Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
 [Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
 [Designdetaljer: Leveransplanering](design-details-supply-planning.md)
