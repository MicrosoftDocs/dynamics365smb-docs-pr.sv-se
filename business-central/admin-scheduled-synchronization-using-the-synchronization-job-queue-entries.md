---
title: Synkronisera Business Central och Dataverse | Microsoft Docs
description: Lär dig mer om att synkronisera data mellan Business Central och Dataverse.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 94f969f4d96f31b3b6843614e1bd99790a22307d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755198"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dataverse"></a>Schemalägga en synkronisering mellan Business Central och Dataverse
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Du kan synkronisera [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på schemalagda intervall, genom att ställa in projekt i jobbkön. Synkroniseringjobben synkroniserar data i [!INCLUDE[prod_short](includes/prod_short.md)]-poster och [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-poster som har kopplats ihop tidigare. Eller för poster som inte redan är kopplade, beroende på synkroniseringsriktningen och reglerna, kan synkroniseringjobben skapa och koppla nya poster i målsystemet. 

Det finns flera synkroniseringsprojekt som är tillgängliga förinstallerade. Jobben körs i följande ordning i syfte att undvika kopplingsberoenden mellan tabeller. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

1. VALUTA – Common Data Service-synkroniseringsjobb.
2. LEVERANTÖR – Common Data Service-synkroniseringsjobb.
3. KONTAKT – Common Data Service-synkroniseringsjobb.
4. KUND – Common Data Service-synkroniseringsjobb.
5. SÄLJARE – Common Data Service-synkroniseringsjobb.

Du kan visa jobb på sidan **jobbkötransaktioner**. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

## <a name="default-synchronization-job-queue-entries"></a>Poster för standardsynkroniseringjobbkön

I följande tabell beskrivs standardsynkroniseringjobben för [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

| Jobbkötransaktion | Beskrivning | Riktning | Registermappning för integrering | Standardfrekvens för synkronisering (minuter) | Standardväntetid för inaktivitet (minuter) |
|--|--|--|--|--|--|--|
| KONTAKT – Common Data Service synkroniseringsjobb | Synkroniserar [!INCLUDE[cds_long_md](includes/cds_long_md.md)] kontakter med [!INCLUDE[prod_short](includes/prod_short.md)] kontakter. | Dubbelriktad | KONTAKT | 30 | 720 <br>(12 timmar) |
| VALUTA – Common Data Service synkroniseringsjobb | Synkroniserar [!INCLUDE[cds_long_md](includes/cds_long_md.md)] transaktionsvalutor med [!INCLUDE[prod_short](includes/prod_short.md)]-valutor. | Från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[cds_long_md](includes/cds_long_md.md)] | VALUTA | 30 | 720 <br> (12 tim) |
| KUND – Common Data Service synkroniseringsjobb | Synkroniserar [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konton med [!INCLUDE[prod_short](includes/prod_short.md)]-kunder. | Dubbelriktad | KUND | 30 | 720<br> (12 tim) |
| LEVERANTÖR – Common Data Service-synkroniseringsjobb | Synkroniserar [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konton med [!INCLUDE[prod_short](includes/prod_short.md)]-kunder. | Dubbelriktad | LEVERANTÖR | 30 | 720<br> (12 tim) |
| SÄLJARE – Common Data Service synkroniseringsjobb | Synkroniserar [!INCLUDE[prod_short](includes/prod_short.md)]-säljare med [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-användare. | Från [!INCLUDE[cds_long_md](includes/cds_long_md.md)] till [!INCLUDE[prod_short](includes/prod_short.md)] | SÄLJARE | 30 | 1440<br> (24 tim) |

## <a name="synchronization-process"></a>Synkroniseringsprocess

Varje köpost för synkroniseringsjobb använder en specifik integreringsregistermappning som anger vilka [!INCLUDE[prod_short](includes/prod_short.md)]- och [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabeller som ska synkroniseras. Registermappningarna innehåller också vissa inställningar som styr vilka poster i [!INCLUDE[prod_short](includes/prod_short.md)]- och [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabellerna som ska synkroniseras.  

För att synkronisera data måste [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabellposter vara kopplade till [!INCLUDE[prod_short](includes/prod_short.md)]-poster. Till exempel måste en [!INCLUDE[prod_short](includes/prod_short.md)]-kund kopplas till ett [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konto. Du kan skapa kopplingar manuellt, innan du kör synkroniseringjobben, eller låta synkroniseringsjobben ställa in kopplingar automatiskt. Följande lista beskriver hur data synkroniseras mellan [!INCLUDE[cds_long_md](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)] när du vill använda synkroniseringsjobbköposterna. Mer information finns i [Koppla och synkronisera posterna manuellt](admin-how-to-couple-and-synchronize-records-manually.md).

- Kryssrutan **Synka endast kopplade poster** styr om nya poster skapas när du synkroniserar. Som standard är kryssrutan markerad, vilket innebär att endast de poster som är kopplade kommer att synkroniseras. I registermappningarna för integrering kan du ändra registermappningen mellan en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabell och en [!INCLUDE[prod_short](includes/prod_short.md)]-tabell, så att integreringssynkroniseringsjobben skapar nya poster i måldatabasen för varje rad i källdatabasen som inte är kopplad. Mer information finns i [Skapa nya poster](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).

    **Exempel** Om du avmarkerar kryssrutan **Synka endast kopplade poster** när du synkroniserar kunder i [!INCLUDE[prod_short](includes/prod_short.md)] med konton i [!INCLUDE[cds_long_md](includes/cds_long_md.md)], skapas ett nytt konto för varje kund i [!INCLUDE[prod_short](includes/prod_short.md)] och kopplas automatiskt. Dessutom, eftersom synkroniseringen är dubbelriktad skapas och kopplas en ny kund för varje [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konto som redan har kopplats.  

    > [!NOTE]  
    > Det finns regler och filter som bestämmer vilka data som synkroniseras. Mer information finns i [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md).

- När nya poster skapas i [!INCLUDE[prod_short](includes/prod_short.md)] använder posterna antingen den mall som har definierats för integreringsregistermappning eller standardmallen som finns för radtypen. Fälten fylls i med data från [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[cds_long_md](includes/cds_long_md.md)] beroende på riktningen för synkroniseringen. Mer information finns i [Ändra registermappningar för synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).  

- Med efterföljande synkroniseringar kommer endast poster som har ändrats eller lagts till efter det senast slutförda synkroniseringsjobbet för tabellen att uppdateras.  

     Nya poster i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] läggs till i [!INCLUDE[prod_short](includes/prod_short.md)]. Om data i fält i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-poster har ändrats, kopieras informationen till motsvarande fält i [!INCLUDE[prod_short](includes/prod_short.md)].  

- Med dubbelriktad synkronisering synkroniserar jobbet från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[cds_long_md](includes/cds_long_md.md)] och sedan från [!INCLUDE[cds_long_md](includes/cds_long_md.md)] till [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="about-inactivity-timeouts"></a>Om timeout för inaktivitet
Vissa jobbkötransaktioner, till exempel sådana som schemalägger synkronisering mellan [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[cds_long_md](includes/cds_long_md.md)], använder fältet **Timeout för inaktivitet** på SIDAN för jobbkötransaktion för att förhindra att jobbkötransaktionen körs i onödan.  

:::image type="content" source="media/on-hold-with-inactivity-timeout.png" alt-text="Flödesschema för när jobbkötransaktioner spärras på grund av inaktivitet.":::

När värdet i det här fältet inte är noll och jobbkön inte hittade några ändringar under den senaste körningen placerar [!INCLUDE[prod_short](includes/prod_short.md)] jobbkötransaktionen i jobbkön. När det inträffar visar fältet **Status för jobbkö** **Stoppad på grund av inaktivitet** och [!INCLUDE[prod_short](includes/prod_short.md)] kommer att vänta på den tidsperiod som angetts i **timeout för inaktivitet** innan jobbkötransaktionen körs igen.  

Till exempel letar jobbkötransaktionen VALUTA som standard synkroniserar valutor i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] med valutakurser i [!INCLUDE[prod_short](includes/prod_short.md)] efter förändringar i valutakurser var 30:e minut. Om inga ändringar hittas [!INCLUDE[prod_short](includes/prod_short.md)] spärras jobbkötransaktionen VALUTA i 720 minuter (sex timmar). Om en valutakurs ändras i [!INCLUDE[prod_short](includes/prod_short.md)] medan jobbkötransaktionen är spärrad kommer [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt att återaktivera jobbkötransaktionen och starta om jobbkön. 

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] aktiverar automatiskt jobbkötransaktioner som är spärrade när ändringar sker i [!INCLUDE[prod_short](includes/prod_short.md)]. Ändringar i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] kommer inte att aktivera jobbkötransaktioner.

## <a name="to-view-the-synchronization-job-log"></a>Så här visar du synkroniseringsjobbloggen

1. Välj ikonen :::image type="icon" source="media/ui-search/search_small.png" border="false":::, ange **Synkroniseringslogg för integrationen** och välj sedan relaterad länk.
2. Om ett eller flera fel inträffade för ett synkroniseringsjobb visas antalet fel i kolumnen **Misslyckades**. Välj antalet om du vill visa felen för jobbet.  

    > [!TIP]  
    > Du kan visa alla synkroniseringsjobbfel genom att öppna synkroniseringsjobbfelloggen direkt.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Om du vill visa synkroniseringsjobbloggen från registermappningarna

1. Välj ikonen :::image type="icon" source="media/ui-search/search_small.png" border="false":::, ange **Registermappning för integrationen** och välj sedan relaterad länk.
2. På sidan **Registermappningar för integrering** markerar du en post och väljer **Logg över synk.jobb för integrering**.  

## <a name="to-view-the-synchronization-error-log"></a>Så här visar du synkroniseringsfelloggen

- Välj ikonen :::image type="icon" source="media/ui-search/search_small.png" border="false":::, ange **Synkroniseringsfel i integrationen** och välj sedan relaterad länk.

## <a name="see-also"></a>Se även

[Synkroniserar data i Business Central och [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Synkronisera manuellt registermappning](admin-manual-synchronization-of-table-mappings.md)  
[Schemalägga en synkronisering mellan Business Central och [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Om integrering Dynamics 365 Business Central med [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
