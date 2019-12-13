---
title: Hantera kunder som använder Dynamics 365 Sales | Microsoft Docs
description: Du kan använda Dynamics 365 Sales uniti Business Central för att mappa data och ha sömlös integration och synkronisering i processen från kundämne till betalning.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 33b2931e14cb7e41cc3e71c327d2237cd8308466
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878203"
---
# <a name="using-dynamics-365-sales-from-business-central"></a>Använda Dynamics 365 Sales från Business Central
Om du använder Dynamics 365 Sales for Customer Engagement kan du utnyttja sömlös integrering i processen från kundämne till betalning genom att använda [!INCLUDE[d365fin](includes/d365fin_md.md)] för underliggande verksamhet som bearbeta order, hantering av lager och hantera de ekonomiska transaktionerna.

Innan du kan använda integrationsfunktionerna måste du ställa in anslutningen och definiera användarna i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Integrera med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Här beskrivs hur du integrerar onlineversioner av [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)]. Information om lokal konfiguration finns i [förbereda Dynamics 365 Sales för integrering lokalt](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Integrera program låter dig komma åt data i Sales från [!INCLUDE[d365fin](includes/d365fin_md.md)] och i vissa fall vice versa. Du kan arbeta med och synkronisera data som är gemensamma för båda tjänsterna, till exempel kunder, kontakter och försäljningsinformation och hålla informationen uppdaterad i båda programmen.  

Säljare i Sales kan till exempel använda prislistor från [!INCLUDE[d365fin](includes/d365fin_md.md)] när de skapar en försäljningsorder. När de lägger till artikeln till försäljningsorderraden i Sales kan de visa lagernivån (tillgänglighet) av artikeln från [!INCLUDE[d365fin](includes/d365fin_md.md)].

På samma sätt kan orderhandläggare i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan hantera försäljningsorder som är automatiskt eller manuellt överförda från försäljning. De kan till exempel skapa och bokföra försäljningsorderrader för artiklar eller resurser som förts in i Sales som produkter som ej är i register. Mer information finns i avsnittet [Hantera speciella försäljningsorderdata](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] integreras endast med Dynamics 365 Sales. Andra program i Dynamics 365 som ändrar den standardinställda arbetsflödes- eller datamodellen i Sales, till exempel Project Service Automation, kan avbryta integreringen mellan [!INCLUDE[d365fin](includes/d365fin_md.md)]och Sales.

### <a name="coupling-records"></a>Kopplingsposter
Guiden för assisterad konfiguration låter dig välja de data som ska överföras. Senare kan du också ange inställningar för synkronisering av vissa poster. Det kallas för *koppling*. Du kan till exempel koppla ett visst konto i Sales med en viss kund i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det här avsnittet beskriver vad du ska ta hänsyn till när du kopplar poster.

Om du till exempel om du vill visa Sales-konton som kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du koppla de två typerna av poster. Gör detta listsidan **kunder** i [!INCLUDE[d365fin](includes/d365fin_md.md)], använd åtgärden **konfigurera koppling**. Därefter anger du vilka [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder som matchar vilka konton i Sales.

Du kan också skapa (och koppla) ett konto i Sales baserat på till exempel kundposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] med **skapa konto i Dynamics 365 Sales**, eller vice versa med hjälp av **skapa kund i [!INCLUDE[d365fin](includes/d365fin_md.md)]**.

När du har skapat kopplingen mellan två poster kan du manuellt kan begära aktuell post, till exempel en kund, att skriva över omedelbart av kontodata från Sales (eller från [!INCLUDE[d365fin](includes/d365fin_md.md)]) med hjälp av åtgärden **synkronisera**. Åtgärden **Synkronisera nu** som frågar om du vill skriva över Sales eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-postdata.

I vissa fall måste du koppla vissa uppsättningar data innan andra uppsättningar data, vilket visas i följande tabell.

|Data|Vad du kan koppla först|
|-----|----|
|Kunder och konton.|Koppla säljare med Sales-användare|
|Artiklar och resurser|Koppla måttenheter med Sales enhetsgrupper|
|Artiklar och resurspriser|Koppla kundprisgrupper med Sales-priser|

> [!NOTE]  
> Om du använder priser eller om kunder använder utländska valutor, se till att du kopplar valutor till Sales-transaktionsvalutor.

Försäljningsorder för Sales beror på information, till exempel kunder, enheter, valutor, kundprisgrupper, artiklar och/eller resurser. För att integrera med försäljningsorder måste du koppla kunder, enheter, valutor, kundprisgrupper, artiklar och/eller resurser först.

### <a name="fully-synchronizing-records"></a>Synkronisera poster helt
I slutet av den assisterade konfigurationsguiden kan du välja åtgärden **kör fullständig synkronisering** för att starta synkronisering av alla [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster med alla relaterade poster i Sales. På sidan **Dynamics 365 Sales fullständig synk.granskning** kan du välja åtgärden **Starta**. Fyll synkronisering kan ta en stund, men du kan fortsätta att arbeta i [!INCLUDE[d365fin](includes/d365fin_md.md)] när det körs i bakgrunden.

Så här kontrollerar du status på enskilda projekt i en fullständig synkronisering på sidan **Dynamics 365 Sales fullständig synk.granskning** väljer du en post om du vill visa information. Uppdatera sidan om du vill uppdatera status under synkroniseringen.

Från sidan Konfigurera anslutning till **Microsoft Dynamics 365** kan du få information om fullständig synkronisering när som helst. Här kan du också öppna sidan **Tabellmappningar för integrering** för att visa detaljerad information om tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] och i Sales som måste synkroniseras.

## <a name="handling-sales-order-data"></a>Hantering av försäljningsorderdata
Försäljningsorder som människor skickar i [!INCLUDE[crm_md](includes/crm_md.md)] överförs automatiskt till [!INCLUDE[d365fin](includes/d365fin_md.md)] om du väljer kryssrutan **Automatiskt skapa försäljningsorder** på sidan **Microsoft Dynamics 365 konfigurera anslutning**.
Alternativt kan du manuellt konvertera skickade försäljningsorder från [!INCLUDE[crm_md](includes/crm_md.md)] med hjälp av åtgärden **skapa i [!INCLUDE[d365fin](includes/d365fin_md.md)]** på sidan **försäljningsorder - Dynamics 365 for Sales**.
På sådana försäljningsorder överförs fältet **Namn** på den ursprungliga ordern och mappas till fältet **Externa verifikationsnummer** på försäljningsordern i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Detta fungerar även om den ursprungliga försäljningsordern innehåller produkter som ej är i register vilket avser artiklar eller resurser som inte är registrerade hos någon app. I så fall måste du fylla i fälten **Produkttyp ej i register** och **Produktnr ej i register** på sidan **Försäljningsinställningar** så att denna oregistrerade produktförsäljning mappas till ett angivet artikel-/resursnummer för ekonomisk analys.

Om artikelbeskrivningen på den ursprungliga försäljningsordern är mycket omfattande, skapas en ytterligare försäljningsorderrad av typen **Kommentar** för att hålla hela texten på försäljningsordern i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Uppdateringar av fält för försäljningsorderhuvud, till exempel senaste utleveransdatum eller begärt leveransdatum som har mappats i FÖRSÄLJNINGSORDER-ORDER **Tabellmappningar för integrering** synkroniseras med jämna mellanrum till [!INCLUDE[crm_md](includes/crm_md.md)]. Processer som att släppa en försäljningsorder och leverans och fakturering av en försäljningsorder bokförs på försäljningsorderns tidslinje i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [introduktion till aktivitetsfeeder](/dynamics365/customer-engagement/developer/introduction-activity-feeds).

> [!NOTE]  
> Periodisk synkronisering som baseras på FÖRSÄLJNINGSORDERORDER i **Tabellmappningar för integrering** fungerar bara när integration av försäljningsorder har aktiverats. Mer information finns i [Ansluten till Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md). Enbart försäljningsorder som skapats från försäljningsorder som har skickats i [!INCLUDE[crm_md](includes/crm_md.md)] synkroniseras. Mer information finns i [Aktivera integrering av bearbetning av försäljningsorder](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Hantering av försäljningsoffertdata
Försäljningsofferter som aktiveras i [!INCLUDE[crm_md](includes/crm_md.md)] överförs till [!INCLUDE[d365fin](includes/d365fin_md.md)] om du väljer kryssrutan **Automatiskt bearbeta offerter** på sidan **Microsoft Dynamics 365 konfigurera anslutning**.
Alternativt kan du manuellt konvertera aktivera försäljningsofferter från [!INCLUDE[crm_md](includes/crm_md.md)] med hjälp av åtgärden **Bearbeta i [!INCLUDE[d365fin](includes/d365fin_md.md)]** på sidan **försäljningsofferter - Dynamics 365 Sales**.
På sådana försäljningsofferter överförs fältet **Namn** på den ursprungliga offerten och mappas till fältet **Externa verifikationsnummer** på försäljningsordern i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Även fältet **gäller till** på offerten har överförts och mappats till fältet **offertens giltighetsdatum** på försäljningsoffert i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Försäljningsofferter gå igenom ändringar medan de är färdigställs. Både manuell och automatisk behandlingen av försäljningsofferter i [!INCLUDE[d365fin](includes/d365fin_md.md)] ser du till att tidigare versioner av försäljningsofferterna arkiveras innan nya versioner av försäljningsofferter från [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Hantera bokförda försäljningsfakturor, kundbetalningar och statistik
När försäljningsordern har uppfyllts skapas fakturor för den. När du fakturerar försäljningsorder kan du överföra bokförda försäljningsfakturor till [!INCLUDE[crm_md](includes/crm_md.md)] om du väljer kryssrutan **Skapa faktura i [!INCLUDE[crm_md](includes/crm_md.md)]** på sidan **bokförd försäljningsfaktura**. Bokförda fakturor överförs till [!INCLUDE[crm_md](includes/crm_md.md)] med statusen **fakturerade**.

När kundbetalning har inlevererats förförsäljnngsfakturan i [!INCLUDE[d365fin](includes/d365fin_md.md)], kommer status för försäljningsfakturor ändras till **Betald** ed fältet **Statusorsak** inställt på **Delvis**, om den är delvis eller **fullständig** om den är helt betald, när du kör åtgärden **Uppdatera kontostatistik** på kundsidan i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Funktionen **Uppdatera kontostatistiken** uppdaterar också värden som saldo och total försäljning i fälten **Saldo** och **Total försäljning** på faktaboxen **[!INCLUDE[d365fin](includes/d365fin_md.md)] Kontostatistik** i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan också låta schemalagda projekt (kundstatistik och POSTEDSALESINV-INV) köra båda dessa processer automatiskt i bakgrunden.

## <a name="see-also"></a>Se även
[Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Kundhantering](marketing-relationship-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)    
[Översikt över försäljnings- och försäljningsnav](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
