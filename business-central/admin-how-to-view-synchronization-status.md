---
title: Visa status för en synkroniseringsjobb (innehåller video)
description: Använd sidan Kopplade datasynkroniseringsfel för att visa statusen för synkroniseringsjobb som har körts för kopplade poster i en -integration.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.search.form: 6250
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: a9f4f2442e9cb3f8efc46cc7c9fd1f92c002d0dd
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115318"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Visa status för en synkroniseringsjobb


Anvönd sidan **Kopplade datasynkroniseringsfel** för att visa statusen för synkroniseringsjobb som körts för kopplade transaktioner i Dataverse- eller [!INCLUDE[crm_md](includes/crm_md.md)]-integreringar. Det innehåller synkroniseringjobb som har körts från jobbkön- och manuella synkroniseringsjobb som kördes på poster från [!INCLUDE[prod_short](includes/prod_short.md)]. Det kan till exempel vara bra att visa deras status vid felsökning eftersom det ger dig tillgång till information om fel som rör sammankopplade poster. Dessa typer av fel orsakas vanligen av användaråtgärder, till exempel när:  

* Två personer gjorde ändringar i samma data i båda affärsappar.
* Någon har tagit bort data i en av apparna, men inte båda.

> [!Note]
> På sidan **Kopplade synkroniseringsfel** visas information om projekt som hör samman med kopplade poster. Om du löser alla fel men posterna fortfarande inte synkroniseras, kan det vara något fel på inställning för integreringen. Normalt sett måste administratören lösa dessa typer av fel.   

## <a name="example"></a>Exempel
I det här videoklippet visas ett exempel på hur du felsöker fel som har uppstått vid synkronisering med [!INCLUDE[prod_short](includes/cds_long_md.md)]. Samma procedur kommer att användas för alla integreringar. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]


## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Så här visar och löser du synkroniseringsfel för kopplade poster
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") Välj ikonen, ange **Kopplade synkroniseringsfel** och välj sedan relaterad länk.
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

## <a name="remove-couplings-between-records"></a>Ta bort kopplingar mellan poster
När något går fel i integrationen och du behöver ta bort kopplingen mellan poster för att sluta synkronisera dem, kan du göra det för en eller flera poster i taget. Du kan koppla bort en eller flera poster från listsidor eller sidan **Kopplade datasynkroniseringsfel** genom att välja en eller flera rader och välja **Radera koppling**. Du kan också ta bort alla kopplingar för en eller flera registermappningar på sidan **Mappningar för integrationstabeller**. 

Om en entitet med enkelriktad koppling tas bort i [!INCLUDE[prod_short](includes/prod_short.md)] måste du ta bort den brutna kopplingen manuellt. Det gör du genom att gå till sidan **Synkroniseringsfel av kopplade data** och välja åtgärden **Sök efter borttagna** och sedan at bort kopplingarna.

## <a name="see-also"></a>Se även  
[Ställa in konton för integrering med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Använda Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]