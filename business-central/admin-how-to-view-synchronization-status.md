---
title: Visa status för en synkronisering | Microsoft Docs
description: Så här visar du status för ett enskilt synkroniseringsjobb.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620890"
---
# <a name="view-the-status-of-a-synchronization"></a>Visa status för en synkronisering
Du kan visa statusen för de individuella synkroniseringsjobben som har körts för [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen. Det innehåller synkroniseringjobb som har körts från jobbkön- och manuella synkroniseringsjobb som utfördes på poster från [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det är användbart när du felsöker synkroniseringsproblem eftersom det låter dig komma åt detaljer om specifika fel.

### <a name="to-view-synchronization-issues-for-coupled-records"></a>Så här visar du synkroniseringsproblem för sammanfogade poster
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kopplade datasynkroniseringsfel** och välj sedan relaterad länk.
2. På sidan **sammankopplade datasynkroniseringar** visas problem som uppstod när du synkroniserade kopplade poster. Du kan filtrera och sortera poster och utföra åtgärder såsom **Återställ** eller **Ta bort poster** för att lösa ärenden en och en.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Så här visar du synkroniseringsloggen för specifika (manuellt synkroniserade) poster
1. Öppna till exempel kund, artikel eller någon annan post som synkroniserar data mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och försäljning
2. Välj åtgärden **synkroniseringsloggen** om du vill visa synkroniseringsloggen för en vald post. Det kan till exempel vara en specifik kund som du har synkroniserat manuellt.

## <a name="see-also"></a>Se även  
[Ställa in Dynamics 365 for Sales integrering i Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Med hjälp av Dynamics 365 for Sales från Business Central](marketing-integrate-dynamicscrm.md)
