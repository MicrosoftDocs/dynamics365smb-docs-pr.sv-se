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
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: c185ab8fecc8f8d70dad7696a5fb5f67207717aa
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924609"
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
|**Ta bort koppling**|Tar bort kopplingen för posterna och synkroniserar dem inte längre. Om du vill starta om synkroniseringen måste du koppla dem igen. |
|**Försök igen** och **Försök alla igen**|För varje post där ett fel påträffas hoppas synkroniseringen över om du inte korrigerar ärendet. Om du försöker igen kommer den valda posten att inkluderas i nästa synkronisering och **Försök alla igen** inkluderar alla posterna.|
|**Synkronisera**|Programmet kommer att försöka lösa en konflikt där en post har ändrats i båda affärsprogramen. Du kan välja vilken version av posten som ska användas.|
|**Återställa poster** och **ta bort poster**|Dessa är användbara när en transaktion har tagits bort i en av företagsapparna. Ta bort poster tar bort posten i appen där den fortfarande finns. Återskapa återskapar transaktionen i den affärsapp där den togs bort.|

> [!NOTE]
> Om du vill minska antalet konflikter som du behöver lösa kan du ställa in mappningarna för integreringstabellen så att de här åtgärderna tillämpas automatiskt. Mer information finns i [Mappning för integreringstabeller](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Så här visar du synkroniseringsloggen för specifika (manuellt synkroniserade) poster
1. Öppna till exempel kund, artikel eller någon annan transaktion som synkroniserar data mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och Common Data Service eller [!INCLUDE[crm_md](includes/crm_md.md)].
2. Välj åtgärden **synkroniseringsloggen** om du vill visa synkroniseringsloggen för en vald post. Det kan till exempel vara en specifik kund som du har synkroniserat manuellt.

## <a name="see-also"></a>Se även  
[Ställa in konton för integrering med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Använda Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md)
