---
title: Hantera kunder som använder Dynamics 365 Sales | Microsoft Docs
description: Du kan använda Dynamics 365 Sales uniti Business Central för att mappa data och ha sömlös integrering och synkronisering i processen från kundämne till betalning.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 37e94bcc276ee8526a336e13eabe81c694130196
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923701"
---
# <a name="using-dynamics-365-sales-from-business-central"></a>Använda Dynamics 365 Sales från Business Central
Om du använder Dynamics 365 Sales for Customer Engagement kan du utnyttja sömlös integrering i processen från kundämne till betalning genom att använda [!INCLUDE[d365fin](includes/d365fin_md.md)] för underliggande verksamhet som bearbeta order, hantering av lager och hantera de ekonomiska transaktionerna.

Innan du kan använda integreringsfunktionerna måste din systemadministratör ställa in anslutningen och definiera användarna i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Integrera med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Här beskrivs hur du integrerar onlineversioner av [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)]. Information om lokal konfiguration finns i [förbereda Dynamics 365 Sales för integrering lokalt](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Integrera program låter dig komma åt data i Sales från [!INCLUDE[d365fin](includes/d365fin_md.md)] och i vissa fall vice versa. Du kan arbeta med och synkronisera data som är gemensamma för båda tjänsterna, till exempel kunder, kontakter och försäljningsinformation och hålla informationen uppdaterad i båda programmen.  

Exempelvis kan en säljare i [!INCLUDE[crm_md](includes/crm_md.md)] använda prislistorna från [!INCLUDE[d365fin](includes/d365fin_md.md)] när de skapar en säljorder. När de lägger till artikeln till försäljningsorderraden i [!INCLUDE[crm_md](includes/crm_md.md)] kan de se lagernivån (tillgängligheten) för artikeln från [!INCLUDE[d365fin](includes/d365fin_md.md)].

På samma sätt kan orderhandläggare i [!INCLUDE[d365fin](includes/d365fin_md.md)] hantera försäljningsorder som överförs automatiskt eller manuellt från [!INCLUDE[crm_md](includes/crm_md.md)]. De kan till exempel skapa och bokföra försäljningsorderrader för artiklar eller resurser som förts in i [!INCLUDE[crm_md](includes/crm_md.md)] som produkter som ej är i register. Mer information finns i avsnittet [Hantera speciella försäljningsorderdata](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] integreras endast med [!INCLUDE[crm_md](includes/crm_md.md)]. Andra Dynamics 365-program som ändrar den standardinställda arbetsflödes- eller datamodellen i [!INCLUDE[crm_md](includes/crm_md.md)], till exempel Project Service Automation, kan avbryta integreringen mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="coupling-records"></a>Kopplingsposter
Guiden för assisterad konfiguration låter dig välja de data som ska överföras. Senare kan du också ange inställningar för synkronisering av vissa poster. Det kallas för *koppling*. Du kan till exempel koppla ett visst konto i [!INCLUDE[crm_md](includes/crm_md.md)] med en viss kund i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det här avsnittet beskriver vad du ska ta hänsyn till när du kopplar poster.

Om du till exempel vill visa konton i [!INCLUDE[crm_md](includes/crm_md.md)] som kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)] måste du koppla dessa båda posttyper. Gör detta listsidan **kunder** i [!INCLUDE[d365fin](includes/d365fin_md.md)], använd åtgärden **konfigurera koppling**. Därefter anger du vilka [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder som matchar vilka konton i [!INCLUDE[crm_md](includes/crm_md.md)].

Du kan också skapa (och koppla) ett konto i [!INCLUDE[crm_md](includes/crm_md.md)] baserat på exempelvis en pundpost i [!INCLUDE[d365fin](includes/d365fin_md.md)] med hjälp av **Skapa konto i Dynamics 365 Sales** - eller vice versa - med hjälp av **Skapa kund i [!INCLUDE[d365fin](includes/d365fin_md.md)]**.

När du har skapat kopplingen mellan två poster kan du manuellt kan begära aktuell post, till exempel en kund, att skriva över omedelbart av kontodata från Sales (eller från [!INCLUDE[d365fin](includes/d365fin_md.md)]) med hjälp av åtgärden **synkronisera**. Åtgärden **Synkronisera nu** som frågar om du vill skriva över Sales eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-postdata.

I vissa fall måste du koppla vissa uppsättningar data innan andra uppsättningar data, vilket visas i följande tabell.

|Data|Vad du kan koppla först|
|-----|----|
|Kunder och konton.|Koppla säljare med [!INCLUDE[crm_md](includes/crm_md.md)]-användare|
|Artiklar och resurser|Koppla måttenheter med [!INCLUDE[crm_md](includes/crm_md.md)]-enhetsgrupper|
|Artiklar och resurspriser|Koppla kundprisgrupper med [!INCLUDE[crm_md](includes/crm_md.md)]-priser|

> [!NOTE]  
> Om du använder priser eller om kunder använder utländska valutor, se till att du kopplar valutor till Sales-transaktionsvalutor.

Försäljningsorder i [!INCLUDE[crm_md](includes/crm_md.md)] beror på information som till exempel kunder, måttenheter, valutor, kundprisgrupper, artiklar och/eller resurser. För att integrera med försäljningsorder måste du koppla kunder, enheter, valutor, kundprisgrupper, artiklar och/eller resurser först.

## <a name="fully-synchronizing-records"></a>Synkronisera poster helt
I slutet av den assisterade konfigurationsguiden kan du välja åtgärden **Kör fullständig synkronisering** för att börja synkronisera alla [!INCLUDE[d365fin](includes/d365fin_md.md)]-transaktioner med alla relaterade transaktioner i [!INCLUDE[crm_md](includes/crm_md.md)]. På sidan **Dynamics 365 Sales fullständig synk.granskning** kan du välja åtgärden **Starta**. En full synkronisering kan ta en stund, men du kan fortsätta arbeta i [!INCLUDE[d365fin](includes/d365fin_md.md)] medan synkroniseringen körs i bakgrunden.

Så här kontrollerar du status på enskilda projekt i en fullständig synkronisering på sidan **Dynamics 365 Sales fullständig synk.granskning** väljer du en post om du vill visa information. Uppdatera sidan om du vill uppdatera status under synkroniseringen.

Från sidan Konfigurera anslutning till **Microsoft Dynamics 365** kan du få information om fullständig synkronisering när som helst. Här kan du också öppna sidan **Tabellmappningar för integrering** för att visa detaljerad information om tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] och i Sales som måste synkroniseras.

## <a name="handling-sales-order-data"></a>Hantering av försäljningsorderdata
Försäljningsorder som människor skickar i [!INCLUDE[crm_md](includes/crm_md.md)] överförs automatiskt till [!INCLUDE[d365fin](includes/d365fin_md.md)] om du väljer kryssrutan **Automatiskt skapa försäljningsorder** på sidan **Microsoft Dynamics 365 konfigurera anslutning**.
Alternativt kan du manuellt konvertera skickade försäljningsorder från [!INCLUDE[crm_md](includes/crm_md.md)] med hjälp av åtgärden **skapa i [!INCLUDE[d365fin](includes/d365fin_md.md)]** på sidan **försäljningsorder - Dynamics 365 for Sales**.
På sådana försäljningsorder överförs fältet **Namn** på den ursprungliga ordern och mappas till fältet **Externa verifikationsnummer** på försäljningsordern i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Detta fungerar även om den ursprungliga försäljningsordern innehåller produkter som ej är i register vilket avser artiklar eller resurser som inte är registrerade hos någon app. I så fall måste du fylla i fälten **Produkttyp ej i register** och **Produktnr ej i register** fält på sidan **Försäljningsinställningar** så att försäljning av oregistrerade produkter mappas till ett angivet artikel- eller resursnummer.

> [!NOTE]
> Du kan inte mappa produkter som ej är i register till en artikel eller resurs i [!INCLUDE[d365fin](includes/d365fin_md.md)] som är kopplad till en produkt i [!INCLUDE[crm_md](includes/crm_md.md)]. För att tillåta produkter som ej är i register rekommenderar vi att du skapar en artikel eller resurs speciellt för det syftet och inte kopplar den till någon produkt i [!INCLUDE[crm_md](includes/crm_md.md)]. 

Om artikelbeskrivningen på den ursprungliga försäljningsordern är mycket omfattande, skapas en ytterligare försäljningsorderrad av typen **Kommentar** för att hålla hela texten på försäljningsordern i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Uppdateringar av fält i försäljningsorderhuvud, till exempel fälten Senaste utleveransdatum eller Begärt leveransdatum, som har mappats i integreringstabellmappningen **FÖRSÄLJNINGSORDER-ORDER** synkroniseras med jämna mellanrum till [!INCLUDE[crm_md](includes/crm_md.md)]. Processer som att släppa en försäljningsorder och leverans och fakturering av en försäljningsorder bokförs på försäljningsorderns tidslinje i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [introduktion till aktivitetsfeeder](/dynamics365/sales-enterprise/manage-activities). <!--The /dynamics365/sales-enterprise/developer/introduction-activity-feeds link was broken. Should this actually point to /dynamics365/sales-enterprise/manage-activities-->

> [!NOTE]  
> Periodisk synkronisering som baseras på integreringstabellmappningen **FÖRSÄLJNINGSORDER-ORDER** fungerar bara när integrering av försäljningsorder har aktiverats. Mer information finns i [Anslutningsinställningar på sidan Sales anslutningsinställningar](admin-prepare-dynamics-365-for-sales-for-integration.md). Enbart försäljningsorder som skapats från försäljningsorder som har skickats i [!INCLUDE[crm_md](includes/crm_md.md)] synkroniseras. Mer information finns i [Aktivera integrering av bearbetning av försäljningsorder](/dynamics365/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Hantering av försäljningsoffertdata
Försäljningsofferter som aktiveras i [!INCLUDE[crm_md](includes/crm_md.md)] överförs till [!INCLUDE[d365fin](includes/d365fin_md.md)] om du väljer kryssrutan **Automatiskt bearbeta offerter** på sidan **Microsoft Dynamics 365 konfigurera anslutning**.
Alternativt kan du manuellt konvertera aktivera försäljningsofferter från [!INCLUDE[crm_md](includes/crm_md.md)] med hjälp av åtgärden **Bearbeta i [!INCLUDE[d365fin](includes/d365fin_md.md)]** på sidan **försäljningsofferter - Dynamics 365 Sales**.
På sådana försäljningsofferter överförs fältet **Namn** på den ursprungliga offerten och mappas till fältet **Externa verifikationsnummer** på försäljningsordern i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Även fältet **gäller till** på offerten har överförts och mappats till fältet **offertens giltighetsdatum** på försäljningsoffert i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Försäljningsofferter gå igenom ändringar medan de är färdigställs. Både manuell och automatisk behandlingen av försäljningsofferter i [!INCLUDE[d365fin](includes/d365fin_md.md)] ser du till att tidigare versioner av försäljningsofferterna arkiveras innan nya versioner av försäljningsofferter från [!INCLUDE[crm_md](includes/crm_md.md)].

När du väljer **Process** i [!INCLUDE[d365fin](includes/d365fin_md.md)] för en offert som har tillståndet **Vunnen**, skapas en försäljningsorder i [!INCLUDE[d365fin](includes/d365fin_md.md)] endast om en motsvarande försäljningsorder skickas in i [!INCLUDE[crm_md](includes/crm_md.md)]. Annars släpps offerten endast i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om en motsvarande försäljningsorder skickas in i [!INCLUDE[crm_md](includes/crm_md.md)] senare och en försäljningsorder skapas från den, uppdateras **Offertnr** på försäljningsordern och offerten arkiveras.

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Hantera bokförda försäljningsfakturor, kundbetalningar och statistik
När försäljningsordern har uppfyllts skapas fakturor för den. När du fakturerar försäljningsorder kan du överföra bokförda försäljningsfakturor till [!INCLUDE[crm_md](includes/crm_md.md)] om du väljer kryssrutan **Skapa faktura i [!INCLUDE[crm_md](includes/crm_md.md)]** på sidan **bokförd försäljningsfaktura**. Bokförda fakturor överförs till [!INCLUDE[crm_md](includes/crm_md.md)] med statusen **fakturerade**.

När kundbetalning har inlevererats förförsäljnngsfakturan i [!INCLUDE[d365fin](includes/d365fin_md.md)], kommer status för försäljningsfakturor ändras till **Betald** ed fältet **Statusorsak** inställt på **Delvis**, om den är delvis eller **fullständig** om den är helt betald, när du kör åtgärden **Uppdatera kontostatistik** på kundsidan i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Funktionen **Uppdatera kontostatistiken** uppdaterar också värden som saldo och total försäljning i fälten **Saldo** och **Total försäljning** på faktaboxen **[!INCLUDE[d365fin](includes/d365fin_md.md)] Kontostatistik** i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan också låta schemalagda projekt (kundstatistik och POSTEDSALESINV-INV) köra båda dessa processer automatiskt i bakgrunden.

## <a name="see-also"></a>Se även
[Integrering med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Kundhantering](marketing-relationship-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)    
[Översikt över försäljnings- och försäljningsnav](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
