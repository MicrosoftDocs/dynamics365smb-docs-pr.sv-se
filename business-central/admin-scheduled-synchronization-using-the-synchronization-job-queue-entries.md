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
ms.openlocfilehash: 8b1fd4a676d1efe508e6fd2dcb37a67b3c24cdb1
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304354"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-sales"></a>Schemalägga en synkronisering mellan Business Central och Dynamics 365 Sales
Du kan synkronisera [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] på schemalagda intervall, genom att ställa in projekt i jobbkön. Synkroniseringjobben synkroniserar data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster och [!INCLUDE[crm_md](includes/crm_md.md)]-poster som har kopplats ihop tidigare. Eller för poster som inte redan är kopplade, beroende på synkroniseringsriktningen och reglerna, kan synkroniseringjobben skapa och koppla nya poster i målsystemet. Det finns flera synkroniseringsprojekt som är tillgängliga förinstallerade. Du kan visa dem på sidan **jobbkötransaktioner**. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.--> 

## <a name="synchronization-process"></a>Synkroniseringsprocess  
Varje synkroniseringjobbköpost använder en viss integrationstabellmappning som anger vilken [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell och [!INCLUDE[crm_md](includes/crm_md.md)]-enhet som ska synkroniseras. Tabellmappningarna innehåller också en del inställningar som styr vilka poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen och [!INCLUDE[crm_md](includes/crm_md.md)]-entiteten som synkroniseras.  

För att synkronisera data måste [!INCLUDE[crm_md](includes/crm_md.md)]-enhetsposter vara kopplade till [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster. Till exempel måste en [!INCLUDE[d365fin](includes/d365fin_md.md)]-kund kopplas till ett [!INCLUDE[crm_md](includes/crm_md.md)]-konto. Du kan skapa kopplingar manuellt, innan du kör synkroniseringjobben, eller låta synkroniseringsjobben ställa in kopplingar automatiskt. Följande lista beskriver hur data synkroniseras mellan [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)] när du vill använda synkroniseringsjobbköposterna. Mer information finns i [Koppla och synkronisera posterna manuellt](admin-how-to-couple-and-synchronize-records-manually.md). 

-   Som standard synkroniseras endast poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] som är kopplade till poster i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan ändra tabellmappningen mellan en [!INCLUDE[crm_md](includes/crm_md.md)]-enhet och en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell, så att integrationssynkroniseringsjobben ska skapa nya poster i måldatabasen för varje post i källdatabasen som inte är kopplad. De nya posterna används också till motsvarande poster i källan. När du exempelvis synkroniserar kunder med [!INCLUDE[crm_md](includes/crm_md.md)]-konton skapas en kontopost för varje kund i [!INCLUDE[d365fin](includes/d365fin_md.md)]. De nya kontona kopplas automatiskt till kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Eftersom synkroniseringen i det här fallet är dubbelriktad skapas och kopplas en ny kund för varje [!INCLUDE[crm_md](includes/crm_md.md)]-konto som redan har kopplats.  

    > [!NOTE]  
    > Det finns regler och filter som bestämmer vilka data som synkroniseras. Mer information finns i [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   När nya poster skapas i [!INCLUDE[d365fin](includes/d365fin_md.md)] använder posterna antingen mallen som har definierats för integrationstabellmappning eller standardmallen som finns för posttypen. Fälten fylls i med data från [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)] beroende på riktningen för synkroniseringen. Mer information finns i [Så här ändrar du tabellmappningar för synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Med efterföljande synkroniseringar kommer endast poster som har ändrats eller har lagts till efter det senast slutförda synkroniseringjobbbet för enheten att uppdateras.  

     Nya poster i [!INCLUDE[crm_md](includes/crm_md.md)] läggs till i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om data i fält i [!INCLUDE[crm_md](includes/crm_md.md)]-poster har ändrats, kopieras informationen till motsvarande fält i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Med dubbelriktad synkronisering synkroniserar jobbet från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)] och sedan från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Poster för standardsynkroniseringjobbkön  
I följande tabellen beskrivs standardsynkroniseringjobben.  

|Jobbkötransaktion|Beskrivning|Riktning|Tabellmappning för integrering|  
|---------------------|---------------------------------------|---------------|-------------------------------|  
|KONTAKT - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] kontakter med [!INCLUDE[d365fin](includes/d365fin_md.md)] kontakter.|Dubbelriktad|KONTAKT|  
|VALUTA - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] transaktionsvalutor med [!INCLUDE[d365fin](includes/d365fin_md.md)]-valutor.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|VALUTA|  
|KUND - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-konton med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder.|Dubbelriktad|KUND|  
|ANPASSADPRISGRUPP - PRIS - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] försäljningsprislistor med [!INCLUDE[d365fin](includes/d365fin_md.md)] kundprisgrupper.| |KUNDPRISGRUPPER - FÖRSÄLJNINGSPRISLISTOR|
|ARTIKEL - PRODUKT - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-artiklar.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL-PRODUKT|
|BOKFÖRD FÖRSÄLJNINGSFAKTURA-FAKT - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-fakturor med [!INCLUDE[d365fin](includes/d365fin_md.md)] bokförda försäljningsfakturor.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|FAKTUROR-BOKFÖRDA FÖRSÄLJNINGSFAKTUROR|
|RESURS-PRODUKTER - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-resurser.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|RESURS-PRODUKT|  
|SÄLJARE - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[d365fin](includes/d365fin_md.md)]-säljare med [!INCLUDE[crm_md](includes/crm_md.md)]-användare.|Från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)]|SÄLJARE|
|FÖRSÄLJNPRIS - PROUDUKTPRIS - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] produktpriser med [!INCLUDE[d365fin](includes/d365fin_md.md)] försäljningspriser.||PRODUKTPRIS-FÖRSÄLJNINGSPRIS|
|MÅTTENHET - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-enhetsgrupper med [!INCLUDE[d365fin](includes/d365fin_md.md)]-måttenheter.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|MÅTTENHET|  
|Kundstatistik – Dynamics 365 Sales-synkronisering.|Uppdaterar [!INCLUDE[crm_md](includes/crm_md.md)]-konton med senaste [!INCLUDE[d365fin](includes/d365fin_md.md)] kundinformation. I [!INCLUDE[crm_md](includes/crm_md.md)] visas den här informationen i snabbformuläret **Business Central bankkontostatistik** som är kopplat till [!INCLUDE[d365fin](includes/d365fin_md.md)] kunder.<br /><br /> Informationen kan även uppdateras manuellt från varje kundpost. Mer information finns i [Så här kopplar du och synkroniserar posterna manuellt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Obs:** denna jobbkötransaktion är endast relevant om [!INCLUDE[d365fin](includes/d365fin_md.md)] integrationslösning är installerad i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [om Business Central integrationslösning](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Ej tillämpbart.|Ej tillämpbart.|   

## <a name="to-view-the-synchronization-job-log"></a>Så här visar du synkroniseringsjobbloggen  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **synkroniseringslogg för integrering** och välj sedan relaterad länk.
2.  Om ett eller flera fel inträffade för ett synkroniseringsjobb visas antalet fel i kolumnen **Misslyckades**. Välj antalet om du vill visa felen för jobbet.  

    > [!TIP]  
    > Du kan visa alla synkroniseringsjobbfel genom att öppna synkroniseringsjobbfelloggen direkt.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Om du vill visa synkroniseringsjobbloggen från tabellmappningarna  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Tabellmappningar för integrering** och välj sedan relaterad länk.
2.  På sidan **Tabellmappningar för integrering** markerar du en post och väljer **Logg över synk.jobb för integrering**.  

## <a name="to-view-the-synchronization-error-log"></a>Så här visar du synkroniseringsfelloggen  
* Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **synkroniseringsfel för integrering** och välj sedan relaterad länk.

## <a name="see-also"></a>Se även  
[Synkroniserar data i Business Central och Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)  
[Synkronisera manuellt tabellmappning](admin-manual-synchronization-of-table-mappings.md)  
[Schemalägga en synkronisering mellan Business Central och Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Om integration av Dynamics 365 Business Central med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  



