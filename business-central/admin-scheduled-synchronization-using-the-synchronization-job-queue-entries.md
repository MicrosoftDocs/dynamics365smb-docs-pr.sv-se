---
title: Synkroniserar i Business Central och Dynamics 365 Sales | Microsoft Docs
description: Lär dig mer om att synkronisera data mellan Business Central och Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 4b6137f6d5fa057d801a1afe30480017ceadd1c8
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879088"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-sales"></a>Schemalägga en synkronisering mellan Business Central och Dynamics 365 Sales
Du kan synkronisera [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] på schemalagda intervall, genom att ställa in projekt i jobbkön. Synkroniseringjobben synkroniserar data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster och [!INCLUDE[crm_md](includes/crm_md.md)]-poster som har kopplats ihop tidigare. Eller för poster som inte redan är kopplade, beroende på synkroniseringsriktningen och reglerna, kan synkroniseringjobben skapa och koppla nya poster i målsystemet. Det finns flera synkroniseringsprojekt som är tillgängliga förinstallerade. Du kan visa dem på sidan **jobbkötransaktioner**. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.-->

## <a name="synchronization-process"></a>Synkroniseringsprocess  
Varje synkroniseringjobbköpost använder en viss integrationstabellmappning som anger vilken [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell och [!INCLUDE[crm_md](includes/crm_md.md)]-enhet som ska synkroniseras. Tabellmappningarna innehåller också en del inställningar som styr vilka poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen och [!INCLUDE[crm_md](includes/crm_md.md)]-entiteten som synkroniseras.  

För att synkronisera data måste [!INCLUDE[crm_md](includes/crm_md.md)]-enhetsposter vara kopplade till [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster. Till exempel måste en [!INCLUDE[d365fin](includes/d365fin_md.md)]-kund kopplas till ett [!INCLUDE[crm_md](includes/crm_md.md)]-konto. Du kan skapa kopplingar manuellt, innan du kör synkroniseringjobben, eller låta synkroniseringsjobben ställa in kopplingar automatiskt. Följande lista beskriver hur data synkroniseras mellan [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)] när du vill använda synkroniseringsjobbköposterna. Mer information finns i [Koppla och synkronisera posterna manuellt](admin-how-to-couple-and-synchronize-records-manually.md).

-   Kryssrutan **Synka endast kopplade poster** styr om nya poster skapas när du synkroniserar. Som standard är kryssrutan markerad, vilket innebär att endast de poster som är kopplade kommer att synkroniseras. I tabellmappningar för integrering kan du ändra tabellmappningen mellan en [!INCLUDE[crm_md](includes/crm_md.md)]-enhet och en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell, så att integrationssynkroniseringsjobben ska skapa nya poster i måldatabasen för varje post i källdatabasen som inte är kopplad. (Mer information finns i [Skapa nya poster](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).) 
    
    **Exempel** Om du avmarkerar kryssrutan **Synka endast kopplade poster** när du synkroniserar kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)] med konton i [!INCLUDE[crm_md](includes/crm_md.md)], skapas ett nytt konto för varje kund i [!INCLUDE[d365fin](includes/d365fin_md.md)] och kopplas automatiskt. Dessutom, eftersom synkroniseringen är dubbelriktad skapas och kopplas en ny kund för varje [!INCLUDE[crm_md](includes/crm_md.md)]-konto som redan har kopplats.  

    > [!NOTE]  
    > Det finns regler och filter som bestämmer vilka data som synkroniseras. Mer information finns i [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   När nya poster skapas i [!INCLUDE[d365fin](includes/d365fin_md.md)] använder posterna antingen mallen som har definierats för integrationstabellmappning eller standardmallen som finns för posttypen. Fälten fylls i med data från [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)] beroende på riktningen för synkroniseringen. Mer information finns i [Ändra tabellmappningar för synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Med efterföljande synkroniseringar kommer endast poster som har ändrats eller har lagts till efter det senast slutförda synkroniseringjobbbet för enheten att uppdateras.  

     Nya poster i [!INCLUDE[crm_md](includes/crm_md.md)] läggs till i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om data i fält i [!INCLUDE[crm_md](includes/crm_md.md)]-poster har ändrats, kopieras informationen till motsvarande fält i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Med dubbelriktad synkronisering synkroniserar jobbet från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)] och sedan från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Poster för standardsynkroniseringjobbkön  
I följande tabellen beskrivs standardsynkroniseringjobben.  

|Jobbkötransaktion|Beskrivning|Riktning|Tabellmappning för integrering|Standardfrekvens för synkronisering (minuter)|Standardväntetid för inaktivitet (minuter)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|KONTAKT - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] kontakter med [!INCLUDE[d365fin](includes/d365fin_md.md)] kontakter.|Dubbelriktad|KONTAKT|30|720 <br>(12 timmar)| 
|VALUTA - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] transaktionsvalutor med [!INCLUDE[d365fin](includes/d365fin_md.md)]-valutor.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|VALUTA|30|720 <br> (12 tim)| 
|KUND - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-konton med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder.|Dubbelriktad|KUND|30|720<br> (12 tim)|
|ANPASSADPRISGRUPP - PRIS - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] försäljningsprislistor med [!INCLUDE[d365fin](includes/d365fin_md.md)] kundprisgrupper.| |KUNDPRISGRUPPER - FÖRSÄLJNINGSPRISLISTOR|30|1440<br> (24 tim)|
|ARTIKEL - PRODUKT - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-artiklar.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL-PRODUKT|30|1440<br> (24 tim)|
|BOKFÖRD FÖRSÄLJNINGSFAKTURA-FAKT - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-fakturor med [!INCLUDE[d365fin](includes/d365fin_md.md)] bokförda försäljningsfakturor.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|FAKTUROR-BOKFÖRDA FÖRSÄLJNINGSFAKTUROR|30|1440<br> (24 tim)|
|RESURS-PRODUKTER - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-resurser.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|RESURS-PRODUKT|30|720<br> (12 tim)|  
|SÄLJARE - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[d365fin](includes/d365fin_md.md)]-säljare med [!INCLUDE[crm_md](includes/crm_md.md)]-användare.|Från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)]|SÄLJARE|30|1440<br> (24 tim)|
|FÖRSÄLJNPRIS - PROUDUKTPRIS - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] produktpriser med [!INCLUDE[d365fin](includes/d365fin_md.md)] försäljningspriser.||PRODUKTPRIS-FÖRSÄLJNINGSPRIS|30|1440<br> (24 tim)|
|MÅTTENHET - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-enhetsgrupper med [!INCLUDE[d365fin](includes/d365fin_md.md)]-måttenheter.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|MÅTTENHET|30|720<br> (12 tim)|  
|Kundstatistik – Dynamics 365 Sales-synkronisering.|Uppdaterar [!INCLUDE[crm_md](includes/crm_md.md)]-konton med senaste [!INCLUDE[d365fin](includes/d365fin_md.md)] kundinformation. I [!INCLUDE[crm_md](includes/crm_md.md)] visas den här informationen i snabbformuläret **Business Central bankkontostatistik** som är kopplat till [!INCLUDE[d365fin](includes/d365fin_md.md)] kunder.<br /><br /> Informationen kan även uppdateras manuellt från varje kundpost. Mer information finns i [Koppla och synkronisera posterna manuellt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Obs:** denna jobbkötransaktion är endast relevant om [!INCLUDE[d365fin](includes/d365fin_md.md)] integrationslösning är installerad i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [om Business Central integrationslösning](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Ej tillämpbart|Ej tillämpbart|30|Ej tillämpbart|   

## <a name="about-inactivity-timeouts"></a>Om timeout för inaktivitet
Vissa jobbkötransaktioner, till exempel sådana som schemalägger synkronisering mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] använder fältet **timeout för inaktivitet** på transaktionskort för jobbkö för att förhindra att jobbkötransaktionen körs i onödan.  
<br><br>

> ![Flödesschema för när jobbkötransaktioner spärras på grund av inaktivitet.](media/on-hold-with-inactivity-timeout.png)

När värdet i det här fältet inte är noll och jobbkön inte hittade några ändringar under den senaste körningen placerar [!INCLUDE[d365fin](includes/d365fin_md.md)] jobbkötransaktionen i jobbkön. När det inträffar visar fältet **Status för jobbkö** **Stoppad på grund av inaktivitet** och [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer att vänta på den tidsperiod som angetts i **timeout för inaktivitet** innan jobbkötransaktionen körs igen. 

Till exempel letar jobbkötransaktionen VALUTA som standard synkroniserar valutor i [!INCLUDE[crm_md](includes/crm_md.md)] med valutakurser i [!INCLUDE[d365fin](includes/d365fin_md.md)] efter förändringar i valutakurser var 30:e minut. Om inga ändringar hittas [!INCLUDE[d365fin](includes/d365fin_md.md)] spärras jobbkötransaktionen VALUTA i 720 minuter (sex timmar). Om en valutakurs ändras i [!INCLUDE[d365fin](includes/d365fin_md.md)] medan jobbkötransaktionen är spärrad kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] automatiskt att återaktivera jobbkötransaktionen och starta om jobbkön. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] aktiverar automatiskt jobbkötransaktioner som är spärrade när ändringar sker i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ändringar i [!INCLUDE[crm_md](includes/crm_md.md)] kommer inte att aktivera jobbkötransaktioner.

## <a name="to-view-the-synchronization-job-log"></a>Så här visar du synkroniseringsjobbloggen  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **synkroniseringslogg för integrering** och välj sedan relaterad länk.
2.  Om ett eller flera fel inträffade för ett synkroniseringsjobb visas antalet fel i kolumnen **Misslyckades**. Välj antalet om du vill visa felen för jobbet.  

    > [!TIP]  
    > Du kan visa alla synkroniseringsjobbfel genom att öppna synkroniseringsjobbfelloggen direkt.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Om du vill visa synkroniseringsjobbloggen från tabellmappningarna  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Tabellmappningar för integrering** och välj sedan relaterad länk.
2.  På sidan **Tabellmappningar för integrering** markerar du en post och väljer **Logg över synk.jobb för integrering**.  

## <a name="to-view-the-synchronization-error-log"></a>Så här visar du synkroniseringsfelloggen  
* Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **synkroniseringsfel för integrering** och välj sedan relaterad länk.

## <a name="see-also"></a>Se även  
[Synkroniserar data i Business Central och Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)  
[Synkronisera manuellt tabellmappning](admin-manual-synchronization-of-table-mappings.md)  
[Schemalägga en synkronisering mellan Business Central och Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Om integration av Dynamics 365 Business Central med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
