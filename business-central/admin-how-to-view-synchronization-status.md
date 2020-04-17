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
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 2371c61c36a17df93ccc1a24c588b12613f5c380
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196621"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Visa status för en synkroniseringsjobb
Anvönd sidan **Kopplade datasynkroniseringsfel** för att visa statusen för synkroniseringsjobb som körts för kopplade transaktioner i Common Data Service- eller [!INCLUDE[crm_md](includes/crm_md.md)]-integreringar. Det innehåller synkroniseringjobb som har körts från jobbkön- och manuella synkroniseringsjobb som kördes på poster från [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det kan till exempel vara bra att visa deras status vid felsökning eftersom det ger dig tillgång till information om fel som rör sammankopplade poster. Dessa typer av fel orsakas vanligen av användaråtgärder, till exempel när:  

* Två personer gjorde ändringar i samma post i båda affärsapparna.
* Någon har tagit bort en post i en av apparna, men inte båda.

> [!Note]
> På sidan **Kopplade synkroniseringsfel** visas information om projekt som hör samman med kopplade poster. Om du löser alla fel men posterna fortfarande inte synkroniseras, kan det vara något fel på inställning för integreringen. Normalt sett måste administratören lösa dessa typer av fel.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Så här visar och löser du synkroniseringsfel för kopplade poster
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Synkroniseringsfel för kopplade data** och välj sedan tillhörande länk.
2. På sidan **sammankopplade datasynkroniseringar** visas problem som uppstod när du synkroniserade kopplade poster. Följande tabell innehåller åtgärder som du kan använda för att lösa ärenden en i taget:

|Åtgärd|Beskrivning|
|----|----|
|**Ta bort koppling**|Tar bort kopplingen för posterna och synkroniserar dem inte längre. Om du vill fortsätta synkronisera posterna måste du koppla dem igen.|
|**Försök igen**|För varje post där ett fel påträffas hoppas synkroniseringen över om du inte korrigerar ärendet manuellt. Ett nytt försök kommer att inkludera posten vid nästa synkronisering.|
|**Synkronisera**|Programmet kommer att försöka lösa en konflikt där en post har ändrats i båda affärsprogramen. Du kan välja vilken version av posten som ska användas i båda apparna.|
|**Återställa poster** och **ta bort poster**|Dessa är användbara när en transaktion har tagits bort i en av företagsapparna. Ta bort poster tar bort posten i appen där den fortfarande finns. Återskapa återskapar transaktionen i den affärsapp där den togs bort.|

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Så här visar du synkroniseringsloggen för specifika (manuellt synkroniserade) poster
1. Öppna till exempel kund, artikel eller någon annan transaktion som synkroniserar data mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och Common Data Service eller [!INCLUDE[crm_md](includes/crm_md.md)].
2. Välj åtgärden **synkroniseringsloggen** om du vill visa synkroniseringsloggen för en vald post. Det kan till exempel vara en specifik kund som du har synkroniserat manuellt.

## <a name="see-also"></a>Se även  
[Ställa in konton för integrering med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Använda Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md)
