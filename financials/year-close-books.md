---
title: "Avsluta böckerna | Microsoft Docs"
description: "Beskriver de processer som är involverade när du vill avsluta böckerna för ett räkenskapsår eller en period."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a8d379c971d9b21b0eac552f8c7f68926090f037
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="closing-books"></a>Avsluta böcker
När du försäkrat dig om att alla dina räkenskaper är uppdaterade och du fördelat kostnader och intäkter, kan du avsluta böckerna för ett räkenskapsår eller en period.

Du måste inte avsluta ett år, men när du gör det blir det enklare att arbeta i systemet eftersom du kommer att kunna utnyttja de praktiska filtreringsalternativ som finns tillgängliga. Du behöver inte heller oroa dig för att förlora detaljer om transaktioner när du avslutar eftersom alla detaljer behålls även när du har avslutat ett år.

## <a name="closing-book-process"></a>Avsluta bokbearbetning
Processen för att avsluta boken innehåller dessa huvuduppgifter:

1. avsluta bokföringsperioden

    Ett räkenskapsår defineras som en eller flera öppna perioder som definieras i fönstret **Bokföringsperioder**. Ett typiskt räkenskapsår består av 12 perioder på vardera en månad, men du kan välja att definiera det enligt någon annan metod.

    Mer information finns [Så här avslutar du bokföringsperioder](year-close-account-periods.md).
2. registrera transaktioner från föregående år

    När du avslutar ett räkenskapsår måste du ange ett antal administrativa transaktioner (till exempel förutbetalda och upplupna poster). Dessa transaktioner kallas justeringstransaktioner. Det finns inga särskilda regler för bokföring av dessa transaktioner och de (liksom andra transaktioner) har en markering i fältet **Föregående års transaktion** om de bokförs på ett datum i ett avslutat räkenskapsår. Även om ett räkenskapsår har avslutats kan du fortfarande bokföra redovisningstransaktioner på året.
3. föra över saldon från resultaträkningskontona till balansräkningen

    När ett räkenskapsår har avslutats och alla transaktioner från föregående år har bokförts, måste resultaträkningskontona avslutas och nettoresultatet föras över till ett konto under eget kapital i balansräkningen. Använd batch-jobbet Avslut av resultaträkningar för detta ändamål. Batch-jobbet bearbetar alla redovisningskonton av typen Resultaträkning och skapar transaktioner som återför deras saldon. Dessa transaktioner placeras i en journal från vilken de kan bokföras. De bokförs inte automatiskt med batch-jobbet utom när en alternativ rapporteringsvaluta används. När en alternativ rapporteringsvaluta används bokförs de direkt i redovisningen.

    Mer information finns i [Avslut av resultatkonton](year-close-income-statement.md).
4. Bokföra årsslutstransaktionen tillsammans med motkontering av konton för eget kapital.

    När batch-jobbet Avslut av resultatkonton är klart bokför du transaktionerna som skapas av jobbet. Om du inte angett ett konto för balanserad vinst eller förlust i batch-jobbet bör du ange en rad med en mottransaktion som bokför nettoresultatet på rätt redovisningskonto under eget kapital i balansräkningen. Bokför slutligen journalen.

    Mer information finns i [Så här bokför du årsslutstransaktionen](year-how-post-year-end-close-entry.md).

## <a name="what-happens-when-you-close"></a>Vad som händer när du avslutar
När du avslutar i slutet av året flyttas intäkterna från beräknade intäkter till kontot Balanserad vinst eller förlust. Räkenskapsåret markeras också som "avslutat", och alla efterföljande transaktioner för det avslutade året markeras som "föregående års transaktioner".

Sedan genereras en årsavslutstransaktion, men transaktionen bokförs inte automatiskt. Du har möjlighet att göra motkonteringar på kontot för eget kapital, vilket innebär att du kan bestämma hur du ska allokera bokföringsposten. Om företaget t.ex. har flera divisioner kan du låta en enskild årsavslutstransaktion genereras för alla divisionerna och du kan sedan göra en motkontering för varje divisions konto för eget kapital.

Du kan bokföra i ett föregående räkenskapsår även efter att resultatkontona har avslutats om du kör batch-jobbet Avslut av resultatkonton igen efteråt.

## <a name="see-also"></a>Se även
[Så här öppnar du ett nytt räkenskapsår](finance-how-open-new-fiscal-year.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

