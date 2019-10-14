---
title: Visa status för en synkroniseringsjobb | Microsoft Docs
description: Lär dig mer om hur du visar statusen efter att ha synkroniserat kopplade poster.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 022e364b6a40fe8df1f9c4e3425030d35f729e6a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304498"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Visa status för en synkroniseringsjobb
Använd sidan **Kopplade datasynkroniseringsfel** för att visa statusen för synkroniseringsjobb som har körts för kopplade poster i en [!INCLUDE[crm_md](includes/crm_md.md)]-integration. Det innehåller synkroniseringjobb som har körts från jobbkön- och manuella synkroniseringsjobb som kördes på poster från [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det kan till exempel vara bra att visa deras status vid felsökning eftersom det ger dig tillgång till information om fel som rör sammankopplade poster. Dessa typer av fel orsakas vanligen av användaråtgärder, till exempel när:  

* Två personer gjorde ändringar i samma post i båda affärsapparna.
* Någon har tagit bort en post i en av apparna, men inte båda.

> [!Note]
> På sidan **Kopplade synkroniseringsfel** visas information om projekt som hör samman med kopplade poster. Om du löser alla fel men posterna fortfarande inte synkroniseras, kan det vara något fel på inställning för integreringen. Normalt sett måste administratören lösa dessa typer av fel.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Så här visar och löser du synkroniseringsfel för kopplade poster
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kopplade datasynkroniseringsfel** och välj sedan relaterad länk.
2. På sidan **sammankopplade datasynkroniseringar** visas problem som uppstod när du synkroniserade kopplade poster. Följande tabell innehåller åtgärder som du kan använda för att lösa ärenden en i taget:

|Åtgärd|Beskrivning|
|----|----|
|**Ta bort koppling**|Tar bort kopplingen för posterna och synkroniserar dem inte längre. Om du vill fortsätta synkronisera posterna måste du koppla dem igen.|
|**Försök igen**|För varje post där ett fel påträffas hoppas synkroniseringen över om du inte korrigerar ärendet manuellt. Ett nytt försök kommer att inkludera posten vid nästa synkronisering.|
|**Synkronisera**|Programmet kommer att försöka lösa en konflikt där en post har ändrats i båda affärsprogramen. Du kan välja vilken version av posten som ska användas i båda apparna.|
|**Återställa poster** och **ta bort poster**|Dessa är användbara när en post har tagits bort i ett av programmen. Ta bort poster tar bort posten i appen där den fortfarande finns. Återskapar posten i programmet där den togs bort.|

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Så här visar du synkroniseringsloggen för specifika (manuellt synkroniserade) poster
1. Öppna till exempel kund, artikel eller någon annan post som synkroniserar data mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)]
2. Välj åtgärden **synkroniseringsloggen** om du vill visa synkroniseringsloggen för en vald post. Det kan till exempel vara en specifik kund som du har synkroniserat manuellt.

## <a name="see-also"></a>Se även  
[Ställa in konton för integrering med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Använda Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md)
