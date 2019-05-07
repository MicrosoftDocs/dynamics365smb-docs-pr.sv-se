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
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "940373"
---
# <a name="view-the-status-of-a-synchronization"></a>Visa status för en synkronisering
Du kan visa statusen för de individuella synkroniseringsjobben som har körts för [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen. Det innehåller synkroniseringjobb som har körts från jobbkön- och manuella synkroniseringsjobb som utfördes på poster från [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det är användbart när du felsöker synkroniseringsproblem eftersom det låter dig komma åt detaljer om specifika fel.

### <a name="to-view-all-synchronization-issues"></a>Så här visar du alla synkroniseringsproblem
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kopplade datasynkroniseringsfel** och välj sedan relaterad länk.
2. På sidan **Kopplade datasynkroniseringsfel** kan du visa alla problem som inträffade i synkroniseringen mellan [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)], filtrera och sortera poster på sidan per tabell, felmeddelande och utföra åtgärder som **Försök igen** eller **Ta bort koppling** för att lösa ett problem i taget eller samtidigt.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Så här visar du synkroniseringsloggen för specifika (manuellt synkroniserade) poster
1. Öppna till exempel kund, artikel eller någon annan post som synkroniserar data mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och försäljning
2. Välj åtgärder **synkroniseringsloggen** för att visa synkroniseringsloggen för den valda posten, till exempel specifik kund som synkroniserade manuellt

## <a name="see-also"></a>Se även  
[Ställa in Dynamics 365 for Sales integrering i Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Med hjälp av Dynamics 365 for Sales från Business Central](marketing-integrate-dynamicscrm.md)
