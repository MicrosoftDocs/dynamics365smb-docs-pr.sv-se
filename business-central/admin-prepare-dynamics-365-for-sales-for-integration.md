---
title: Integrera med Dynamics 365 Sales | Microsoft Docs
description: Lär dig hur du hämtar Dynamics 365 Business Central redo att integreras med Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 07/23/2020
ms.author: bholtorf
ms.openlocfilehash: 7132a32a37844078b696af5e8d19bf951460a2e2
ms.sourcegitcommit: 7b5c927ea9a59329daf1b60633b8290b552d6531
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617660"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integrering med Dynamics 365 Sales

Rollen säljare betraktas ofta som en de mest utåtriktade jobben i ett företag. Men kan det vara användbart för säljare att kunna se inuti verksamheten och se vad som händer på serverdelen. Genom att integrera [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] kan du ge säljare denna information genom att visa informationen i [!INCLUDE[d365fin](includes/d365fin_md.md)] medan de arbetar i [!INCLUDE[crm_md](includes/crm_md.md)]. Till exempel när du förbereder en försäljningsoffert kan det vara bra att veta om det finns tillräckligt mycket lager för att uppfylla ordern. Mer information finns i [Använd Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> I detta ämne beskrivs hur du integrerar onlineversioner av [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)] med hjälp av [!INCLUDE[d365fin](includes/cds_long_md.md)]. Information om lokal konfiguration finns i [förbereda Dynamics 365 Sales för integrering lokalt](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-common-data-service"></a>Integrera via Common Data Service
[!INCLUDE[d365fin](includes/d365fin_md.md)] integreras också med [!INCLUDE[d365fin](includes/cds_long_md.md)], vilket gör det enkelt att ansluta och synkronisera data med andra Dynamics 365-program, till exempel [!INCLUDE[crm_md](includes/crm_md.md)] eller till och med appar som du själv skapar. Om du integrerar för första gången rekommenderar vi att du gör det via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Mer information finns i [Integrera med Common Data Service](admin-common-data-service.md).

Om du redan har integrerat [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du fortsätta att synkronisera data med hjälp av dina inställningar. Om du uppgraderar eller stänger av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen måste du emellertid ansluta dig via [!INCLUDE[d365fin](includes/cds_long_md.md)] för att aktivera den igen. Mer information finns i [Uppgradera en integrering med Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> När du återansluter via [!INCLUDE[d365fin](includes/cds_long_md.md)] används standardinställningarna för synkroniseringen, och eventuella konfigurationsinställningar skrivs över. Till exempel tillämpas standardmappningarna för tabeller.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Integreringsinställningar som är specifika för en [!INCLUDE[crm_md](includes/crm_md.md)]-integrering
Integreringen med [!INCLUDE[d365fin](includes/d365fin_md.md)] sker via [!INCLUDE[d365fin](includes/cds_long_md.md)], och det finns många standardinställningar och enheter som tillhandahålls av integreringen. Utöver standardinställningarna finns det vissa som är specifika för [!INCLUDE[crm_md](includes/crm_md.md)]. Följande avsnitt visar dessa.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Behörigheter och säkerhetsroller för användarkonton i Sales
När du installerar integreringslösningen konfigureras behörigheter för användarkontot för integrering. Om behörigheterna ändras kan du behöva återställa dem. Detta kan du göra genom att ominstallera integreringslösningen genom att välja **Omdistribuera integreringslösning** på sidan **Anslutningsinställningar för Dynamics 365**. Följande säkerhetsroller har distribuerats:

* Dynamics 365 Business Central-integreringsadministratör
* Dynamics 365 Business Central-integreringsanvändare
* Dynamics 365 Business Central-produktartikelanvändare

### <a name="connection-settings-in-the-setup-guide"></a>Anslutningsinställningar i installationsguiden

Du kan använda en assisterad konfigurationsguide för att snabbt ställa in anslutningen och ange avancerade funktioner, till exempel att koppla mellan transaktioner.

1. Välj **inställningar och tillägg**, och välj **assisterad konfiguration**.
2. Välj **Ställ in Dynamics 365 Sales-anslutning** för att starta guiden för assisterad konfiguration.
3. Fyll i fälten om det behövs.
4. Alternativt finns avancerade inställningar som kan förbättra säkerheten och aktivera ytterligare funktioner, till exempel behandling av försäljningsorder och visa lagernivåer. Avancerade inställningarna beskrivs i tabellen nedan.  

| Fält | Beskrivning |
|--|--|
| **Importera Dynamics 365 Sales-lösning** | Aktivera det här alternativet om du vill installera och konfigurera lösningen för integrering i [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
| **Publicera webbtjänsten för artikeldisposition** | Aktivera människor som använder [!INCLUDE[crm_md](includes/crm_md.md)] för att visa disponibla artiklar (produkter) i lagret i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Detta kräver att ett [!INCLUDE[d365fin](includes/d365fin_md.md)]-användarkonto med en åtkomstnyckel för webbtjänsterna. Tilldela nyckeln är en tvåstegsprocess. För användarkontot i [!INCLUDE[d365fin](includes/d365fin_md.md)] måste du välja åtgärden **ändra webbtjänstnyckeln**. I guiden för assisterad konfiguration Dynamics 365 Sales-anslutning anger du Dynamics 365 Business Central OData webbtjänst-URL och ger [!INCLUDE[d365fin](includes/d365fin_md.md)] användarens autentiseringsuppgifter för att komma åt tjänsten. Mer information finns i [OData webbtjänst](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). |
| **URL för OData-webbtjänsten för Business Central** | Om du aktiverar webbtjänsten för att se artikeldispositionen anges webbadressen (URL) för webbtjänsten OData för dig. |
| **Användarnamn för OData-webbtjänsten för Business Central** | Namnet på det [!INCLUDE[d365fin](includes/d365fin_md.md)]-användarkonto som [!INCLUDE[crm_md](includes/crm_md.md)] använder för att hämta information om artikeldisposition i [!INCLUDE[d365fin](includes/d365fin_md.md)] via OData-webbtjänsten. |
| **Åtkomstnyckel för OData-webbtjänsten för Business Central** | Åtkomstnyckeln för det användarkonto som [!INCLUDE[crm_md](includes/crm_md.md)] använder för att hämta information om artikeldisposition från [!INCLUDE[d365fin](includes/d365fin_md.md)] via OData-webbtjänsten. Nyckeln tilldelas den användare som valts i fältet **Användarnamn för OData-webbtjänsten för Business Central**. Om du vill hämta nyckeln väljer du knappen **sök efter värdet** bredvid användarnamnet, väljer användaren, väljer **hantera** och sedan **redigera**. På användarkortet väljer du **åtgärder**, **autentisering** och väljer sedan **ändra webbtjänstnyckeln**. |
| **Aktivera försäljningsorderintegrering** | När en användare skapar försäljningsorder i [!INCLUDE[crm_md](includes/crm_md.md)] och uppfyller order i [!INCLUDE[d365fin](includes/d365fin_md.md)] integreras processen i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Aktivera integrering av bearbetning av försäljningsorder](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Detta innebär att du anger autentiseringsuppgifter för en administratörs användarkonto i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i avsnittet [Hantera speciella försäljningsorderdata](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
| **Aktivera CDS-anslutning** | Aktivera anslutning till [!INCLUDE[d365fin](includes/cds_long_md.md)]. |
| **SDK-version för Dynamics 365** | Detta gäller endast om du integrerar med en lokal version av [!INCLUDE[crm_md](includes/crm_md.md)]. Det här är den SDK-version för Dynamics 365 (även kallat Xrm) för att ansluta [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]. Versionen måste vara kompatibel med SDK-versionen som används av [!INCLUDE[crm_md](includes/crm_md.md)] och motsvarande eller senare än den version som används av [!INCLUDE[crm_md](includes/crm_md.md)]. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Anslutningsinställningar på inställningssidan för Microsoft Dynamics 365-anslutningar

Ange följande information om anslutningen från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)].

| Fält | Beskrivning |
|--|--|
| **Dynamics 365 Sales-URL** | URL:en för din instans av [!INCLUDE[crm_md](includes/crm_md.md)]. Detta låter användare öppna motsvarande transaktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] från transaktioner i [!INCLUDE[crm_md](includes/crm_md.md)], exempelvis som konto eller produkt. [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster är öppna i [!INCLUDE[d365fin](includes/d365fin_md.md)]. |
|**Dynamics 365 Sales-URL**|URL:en för din instans av [!INCLUDE[crm_md](includes/crm_md.md)]. Detta låter användare öppna motsvarande transaktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] från transaktioner i [!INCLUDE[crm_md](includes/crm_md.md)], exempelvis som konto eller produkt. [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster är öppna i [!INCLUDE[d365fin](includes/d365fin_md.md)].|
|**Webbtjänsten Artikeldisposition har aktiverats**|Aktivera människor som använder [!INCLUDE[crm_md](includes/crm_md.md)] för att visa disponibla artiklar (produkter) i lagret i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om detta aktiveras måste du också ange ett namn och en snabbtangent för [!INCLUDE[crm_md](includes/crm_md.md)] för att fråga OData-webbtjänsten om disponibla artiklar (produkter). Mer information finns i [OData webbtjänst](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**Dynamics 365 Business Central OData webbtjänst-URL**|Om du aktiverar webbtjänsten för artikeldisposition anges URL för OData webbadressen för dig. Ange detta fält till url-adressen för den [!INCLUDE[d365fin](includes/d365fin_md.md)]-instans att använda.<br /><br /> Om du vill återställa fältet till standard-URL för [!INCLUDE[d365fin](includes/d365fin_md.md)], på Åtgärd-fliken, välj **Återställ webbklient-URL**.<br /><br /> Detta fält gäller endast om integreringslösningen för [!INCLUDE[d365fin](includes/d365fin_md.md)] har installerats i [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Dynamics 365 Business Central Användarnamn för OData-webbtjänsten**|Namnet på det användarkonto som [!INCLUDE[crm_md](includes/crm_md.md)] använder för att hämta information om artikeldisposition i [!INCLUDE[d365fin](includes/d365fin_md.md)] via webbtjänsten för OData.|
|**Dynamics 365 Business Central Åtkomstnyckel för OData-webbtjänsten**|Åtkomstnyckeln för det användarkonto som [!INCLUDE[crm_md](includes/crm_md.md)] använder för att hämta information om artikeldisposition från [!INCLUDE[d365fin](includes/d365fin_md.md)] via webbtjänsten för OData. Nyckeln tilldelas användaren i fältet **Dynamics 365 Business Central Användarnamn för OData-webbtjänsten**. Om du vill hämta nyckeln väljer du knappen **sök efter värdet** bredvid användarnamnet, väljer användaren, väljer **hantera** och sedan **redigera**. På användarkortet väljer du **åtgärder**, **autentisering** och väljer sedan **ändra webbtjänstnyckeln**.|
|**SDK-version för Dynamics 365**|Om du integrerar med en lokal version av [!INCLUDE[crm_md](includes/crm_md.md)] är det denna SDK-versionen för Dynamics 365 (även kallad Xrm) som du använder för att ansluta [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]. Den version som du väljer måste vara kompatibel med SDK-versionen som används av [!INCLUDE[crm_md](includes/crm_md.md)]. Den här versionen motsvarar eller är senare än den version som används av [!INCLUDE[crm_md](includes/crm_md.md)].|-->

Förutom inställningarna ovan anger du följande inställningar för [!INCLUDE[crm_md](includes/crm_md.md)].

| Fält | Beskrivning |
|--|--|
| **Försäljningsorderintegrering är aktiverad** | Användaren ska kunna skicka försäljningsorder och aktiverade offerter i [!INCLUDE[crm_md](includes/crm_md.md)] och sedan granska och bearbeta dem i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det här integrerar den här processen i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Aktivera integrering av bearbetning av försäljningsorder](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Skapa försäljningsorder automatiskt** | Skapa en försäljningsorder i [!INCLUDE[d365fin](includes/d365fin_md.md)] när en användare skapar och skickar en i [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Bearbeta försäljningsofferter automatiskt** | Bearbeta en försäljningsoffert i [!INCLUDE[d365fin](includes/d365fin_md.md)] när en användare skapar och aktiverar en i [!INCLUDE[crm_md](includes/crm_md.md)]. |

<!--
### User Account Settings
Integrate with Business Central through Common Data Service requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Standardinställd försäljningsenhetsmappningar för synkronisering

Enheter i [!INCLUDE[crm_md](includes/crm_md.md)], till exempel order, är integrerade med motsvarande enhetstyper i [!INCLUDE[d365fin](includes/d365fin_md.md)], till exempel försäljningsorder. För att arbeta med [!INCLUDE[crm_md](includes/crm_md.md)] data anger du länkar som kallas kopplingar mellan enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)].

I följande tabell visas standardmappningen mellan enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] som [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller.

| [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synkroniseringsriktning | Standardfilter |
|--|--|--|--|
| Enhet | Enhetsgrupp | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Artikel | Produkt | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Sales-kontaktfilter: **produkttyp** är **Sales-lager** |
| Resurs | Produkt | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Sales-kontaktfilter: **produkttyp** är **Tjänster** |
| Kund prisgrupp | Prislista | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Förs.pris | Produktprislista | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)] kontaktfilter: **försäljningskod** är inte tom, **förs.typ** är **kundprisgrupp** |
| Affärsmöjlighet | Affärsmöjlighet | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] |  |
| Försäljningsfakturahuvud | Fakturera | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Försäljningsfakturarad | Fakturaprodukt | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Rubrik för försäljningsorder | Reservationstransaktion | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)] Försäljningsrubrikfilter: **Dokumenttyp** är Order, **Status** är Frisläppt |
| Försäljningsordermeddelanden | Försäljningsordermeddelanden | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] |  |

### <a name="synchronization-rules"></a>Synkroniseringsregler

Följande tabell anger regler som kontrollerar synkroniseringen mellan [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dessa gäller utöver de regler som angetts för Common Data Service, vilka också gäller. För mer information, se [Standardenhetsmappningar](/dynamics365/business-central/admin-synchronizing-business-central-and-sales?branch=master-cds-crm#standard-entity-mapping-for-synchronization).

> [!NOTE]  
> Ändrar data i  som genomfördes av användarkontot för integrering synkroniseras inte. Därför rekommenderar vi att du inte ändrar data när du använder kontot. Mer information finns i [Ställa in konton för att integrera med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Bord|Regel|
|-----|----|
|Enheter|Måttenheter synkroniseras med enhetsgrupper i [!INCLUDE[crm_md](includes/crm_md.md)]. Det kan finnas endast en måttenhet som definieras i enhetsgruppen.|
|Artiklar|När artiklar synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter skapar [!INCLUDE[d365fin](includes/d365fin_md.md)] automatiskt en prislista i [!INCLUDE[crm_md](includes/crm_md.md)]. För att undvika synkroniseringsfel bör du inte ändra denna prislista manuellt.|
|Resurser|Resurser som ska synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter som har produktypen tjänster.|
|Kundprisgrupper|Kundprisgrupper synkroniseras med Sales-prislistor.|
|Förs.priser|Sales-priser som har försäljning skriver kundprisgrupp och har definierats försäljningskod synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-prislistrader|
|Affärsmöjligheter|Affärsmöjligheter som ska synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-affärsmöjligheter. Säljarkod värdet definierar ägare till den kopplade enheten i [!INCLUDE[crm_md](includes/crm_md.md)].|
|Bokförda försäljningsfakturor|Bokförda försäljningsfakturor som är synkroniserade med försäljningsfakturor. Innan du kan synkronisera en faktura, är det bättre att synkronisera alla andra enheter som kan delta i fakturan från säljare till prislistor. Säljarkodvärdet i fakturarubriken definierar ägare till den kopplade enheten i Sales.|
|Försäljningsorder|När integrering av försäljningsorder har aktiverats synkroniseras försäljningsorder i [!INCLUDE[d365fin](includes/d365fin_md.md)] som har skapats från skickade försäljningsorder i [!INCLUDE[crm_md](includes/crm_md.md)] med försäljningsorder i INCLUDE SALES när de släpps. Innan du synkroniserar order bör du först synkronisera alla enheter som ingår i ordern, till exempel säljare och prislistor. Fältet Säljarkod i orderrubriken definierar ägare till den kopplade enheten i [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Synkroniseringsjobb för Sales-integrering

Jobben körs i följande ordning för att undvika kopplingsberoenden mellan posterna. Det finns ytterligare jobb tillgängliga från Common Data Service. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](/dynamics365/business-central/admin-job-queues-schedule-tasks).

1. MÅTTENHET - Dynamics 365 Sales synkroniseringsjobb  
2. RESURS-PRODUKTER - Dynamics 365 Sales synkroniseringsjobb  
3. ARTKEL-PRODUKTER - Dynamics 365 Sales synkroniseringsjobb  
4. ANPASSADPRISGRUPP - Dynamics 365 Sales-synkroniseringsjobb.
5. FÖRSÄLJNPRIS - PROUDUKTPRIS - Dynamics 365 Sales synkroniseringsjobb.
6. BOKFÖRD FÖRSÄLJNINGSFAKTURA-FAKT - Dynamics 365 Sales-synkroniseringsjobb.

### <a name="default-synchronization-job-queue-entries"></a>Poster för standardsynkroniseringjobbkön

I följande tabell beskrivs standardsynkroniseringjobben för Sales.  

|Jobbkötransaktion|Beskrivning|Riktning|Tabellmappning för integrering|Standardfrekvens för synkronisering (minuter)|Standardväntetid för inaktivitet (minuter)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|MÅTTENHET - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-enhetsgrupper med [!INCLUDE[d365fin](includes/d365fin_md.md)]-måttenheter.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|MÅTTENHET|30|720<br> (12 tim)|
|RESURS-PRODUKTER - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-resurser.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|RESURS-PRODUKT|30|720<br> (12 tim)|
|ARTIKEL - PRODUKT - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-artiklar.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL-PRODUKT|30|1440<br> (24 tim)|
|ANPASSADPRISGRUPP - PRIS - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] försäljningsprislistor med [!INCLUDE[d365fin](includes/d365fin_md.md)] kundprisgrupper.| |KUNDPRISGRUPPER - FÖRSÄLJNINGSPRISLISTOR|30|1440<br> (24 tim)|
|FÖRSÄLJNPRIS - PROUDUKTPRIS - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] produktpriser med [!INCLUDE[d365fin](includes/d365fin_md.md)] försäljningspriser.||PRODUKTPRIS-FÖRSÄLJNINGSPRIS|30|1440<br> (24 tim)|
|BOKFÖRD FÖRSÄLJNINGSFAKTURA-FAKT - Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-fakturor med [!INCLUDE[d365fin](includes/d365fin_md.md)] bokförda försäljningsfakturor.|Från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|FAKTUROR-BOKFÖRDA FÖRSÄLJNINGSFAKTUROR|30|1440<br> (24 tim)|
|Kundstatistik – Dynamics 365 Sales-synkronisering.|Uppdaterar [!INCLUDE[crm_md](includes/crm_md.md)]-konton med senaste [!INCLUDE[d365fin](includes/d365fin_md.md)] kundinformation. I [!INCLUDE[crm_md](includes/crm_md.md)] visas den här informationen i snabbformuläret **Business Central bankkontostatistik** som är kopplat till [!INCLUDE[d365fin](includes/d365fin_md.md)] kunder.<br /><br /> Informationen kan även uppdateras manuellt från varje kundpost. Mer information finns i [Koppla och synkronisera posterna manuellt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Obs:** denna jobbkötransaktion är endast relevant om [!INCLUDE[d365fin](includes/d365fin_md.md)] integreringslösning är installerad i [!INCLUDE[crm_md](includes/crm_md.md)]. |Ej tillämpbart|Ej tillämpbart|30|Ej tillämpbart| 

### <a name="note-for-on-premises-versions"></a>Anmärkning för lokala versioner

> [!Note]
> Om du ansluter en lokal version av [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)] och du vill konfigurera en anslutning till en [!INCLUDE[crm_md](includes/crm_md.md)]-instans med en specifik autentiseringsmetod fyller du i fälten på snabbfliken **Information om autentiseringstyp**. Mer information finns i [använd anslutningssträngar i XRM verktygsuppsättning för att ansluta till Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Detta steg är inte nödvändigt när du ansluter en onlineversion av [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se även

[Ställa in konton för integrering med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Ställ in en anslutning till [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Synkroniserar Business Central och [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Förbereder Dynamics 365 Sales för integrering lokalt](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)
