---
title: Visa status för en synkroniseringsjobb | Microsoft Docs
description: Lär dig mer om hur du visar statusen efter att ha synkroniserat kopplade poster.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: b87bd1061adbcaae3a5497fa1af020cfaa412593
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781267"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Visa status för en synkroniseringsjobb
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Anvönd sidan **Kopplade datasynkroniseringsfel** för att visa statusen för synkroniseringsjobb som körts för kopplade transaktioner i Dataverse- eller [!INCLUDE[crm_md](includes/crm_md.md)]-integreringar. Det innehåller synkroniseringjobb som har körts från jobbkön- och manuella synkroniseringsjobb som kördes på poster från [!INCLUDE[prod_short](includes/prod_short.md)]. Det kan till exempel vara bra att visa deras status vid felsökning eftersom det ger dig tillgång till information om fel som rör sammankopplade poster. Dessa typer av fel orsakas vanligen av användaråtgärder, till exempel när:  

* Två personer gjorde ändringar i samma data i båda affärsappar.
* Någon har tagit bort data i en av apparna, men inte båda.

> [!Note]
> På sidan **Kopplade synkroniseringsfel** visas information om projekt som hör samman med kopplade poster. Om du löser alla fel men posterna fortfarande inte synkroniseras, kan det vara något fel på inställning för integreringen. Normalt sett måste administratören lösa dessa typer av fel.   

<!--

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

-->

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Så här visar och löser du synkroniseringsfel för kopplade poster
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Synkroniseringsfel för kopplade data** och välj sedan tillhörande länk.
2. På sidan **sammankopplade datasynkroniseringar** visas problem som uppstod när du synkroniserade kopplade poster. Följande tabell innehåller åtgärder som du kan använda för att lösa ärenden en i taget:

|Åtgärd|Beskrivning|
|----|----|
|**Ta bort koppling**|Tar bort kopplingen för posterna och synkroniserar dem inte längre. Om du vill starta om synkroniseringen måste du koppla dem igen. |
|**Försök igen** och **Försök alla igen**|För varje post där ett fel påträffas hoppas synkroniseringen över om du inte korrigerar ärendet. Om du försöker igen kommer den valda posten att inkluderas i nästa synkronisering och **Försök alla igen** inkluderar alla posterna.|
|**Synkronisera**|Programmet kommer att försöka lösa en konflikt där data har ändrats i båda affärsapparna. Du kan välja vila data som ska användas.|
|**Återställa poster** och **ta bort poster**|Dessa är användbara när en transaktion har tagits bort i en av företagsapparna. "Ta bort poster" tar bort posten eller raden i appen där den fortfarande finns kvar. "Återskapa poster" återskapar posten eller raden i den affärsapp där den togs bort.|

> [!NOTE]
> Om du vill minska antalet konflikter som du behöver lösa kan du ställa in mappningarna för integreringstabellen så att de här åtgärderna tillämpas automatiskt. Mer information finns i [Mappning för integreringstabeller](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Så här visar du synkroniseringsloggen för specifika (manuellt synkroniserade) poster
1. Öppna till exempel kund, artikel eller någon annan transaktion som synkroniserar data mellan [!INCLUDE[prod_short](includes/prod_short.md)] och Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)].
2. Välj åtgärden **synkroniseringsloggen** om du vill visa synkroniseringsloggen för en vald post. Det kan till exempel vara en specifik kund som du har synkroniserat manuellt.

## <a name="see-also"></a>Se även  
[Ställa in konton för integrering med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Använda Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]