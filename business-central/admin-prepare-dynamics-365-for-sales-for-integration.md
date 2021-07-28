---
title: Integrering med Dynamics 365 Sales
description: Lär dig hur du gör Dynamics 365 Business Central redo att integrera med Dynamics 365 Sales för att se vad som händer på serverdelen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 437287401003cc008e3a998e7d28fb7862415abc
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6325474"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integrering med Dynamics 365 Sales
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Rollen säljare betraktas ofta som en de mest utåtriktade jobben i ett företag. Men kan det vara användbart för säljare att kunna se inuti verksamheten och se vad som händer på serverdelen. Genom att integrera [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] kan du ge säljare denna information genom att visa informationen i [!INCLUDE[prod_short](includes/prod_short.md)] medan de arbetar i [!INCLUDE[crm_md](includes/crm_md.md)]. Till exempel när du förbereder en försäljningsoffert kan det vara bra att veta om det finns tillräckligt mycket lager för att uppfylla ordern. Mer information finns i [Använd Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> I detta ämne beskrivs hur du integrerar onlineversioner av [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)] med hjälp av [!INCLUDE[prod_short](includes/cds_long_md.md)]. Information om lokal konfiguration finns i [förbereda Dynamics 365 Sales för integrering lokalt](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-dataverse"></a>Integrera via Dataverse
[!INCLUDE[prod_short](includes/prod_short.md)] integreras också med [!INCLUDE[prod_short](includes/cds_long_md.md)], vilket gör det enkelt att ansluta och synkronisera data med andra Dynamics 365-program, till exempel [!INCLUDE[crm_md](includes/crm_md.md)] eller till och med appar som du själv skapar. Om du integrerar för första gången rekommenderar vi att du gör det via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Mer information finns i [Integrera med Dataverse](admin-common-data-service.md).

Om du redan har integrerat [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)] kan du fortsätta att synkronisera data med hjälp av dina inställningar. Om du uppgraderar eller stänger av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen måste du emellertid ansluta dig via [!INCLUDE[prod_short](includes/cds_long_md.md)] för att aktivera den igen. Mer information finns i [Uppgradera en integrering med Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> När du återansluter via [!INCLUDE[prod_short](includes/cds_long_md.md)] används standardinställningarna för synkroniseringen, och eventuella konfigurationsinställningar skrivs över. Till exempel tillämpas standardmappningarna för tabeller.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Integreringsinställningar som är specifika för en [!INCLUDE[crm_md](includes/crm_md.md)]-integrering
Integreringen med [!INCLUDE[prod_short](includes/prod_short.md)] sker via [!INCLUDE[prod_short](includes/cds_long_md.md)], och det finns många standardinställningar och tabeller som tillhandahålls av integreringen. Utöver standardinställningarna finns det vissa som är specifika för [!INCLUDE[crm_md](includes/crm_md.md)]. Följande avsnitt visar dessa.

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
| **Publicera webbtjänsten för artikeldisposition** | Aktivera människor som använder [!INCLUDE[crm_md](includes/crm_md.md)] för att visa disponibla artiklar (produkter) i lagret i [!INCLUDE[prod_short](includes/prod_short.md)]. Detta kräver att ett [!INCLUDE[prod_short](includes/prod_short.md)]-användarkonto med en åtkomstnyckel för webbtjänsterna. Tilldela nyckeln är en tvåstegsprocess. För användarkontot i [!INCLUDE[prod_short](includes/prod_short.md)] måste du välja åtgärden **ändra webbtjänstnyckeln**. I guiden för assisterad konfiguration Dynamics 365 Sales-anslutning anger du Dynamics 365 Business Central OData webbtjänst-URL och ger [!INCLUDE[prod_short](includes/prod_short.md)] användarens autentiseringsuppgifter för att komma åt tjänsten. Mer information finns i [OData webbtjänst](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). |
|**Användarnamn för OData-webbtjänsten för Business Central** | Namnet på det [!INCLUDE[prod_short](includes/prod_short.md)]-användarkonto som [!INCLUDE[crm_md](includes/crm_md.md)] använder för att hämta information om artikeldisposition i [!INCLUDE[prod_short](includes/prod_short.md)] via OData-webbtjänsten. |
| **Åtkomstnyckel för OData-webbtjänsten för Business Central** | Åtkomstnyckeln för det användarkonto som [!INCLUDE[crm_md](includes/crm_md.md)] använder för att hämta information om artikeldisposition från [!INCLUDE[prod_short](includes/prod_short.md)] via OData-webbtjänsten. Nyckeln tilldelas den användare som valts i fältet **Användarnamn för OData-webbtjänsten för Business Central**. Om du vill hämta nyckeln väljer du knappen **sök efter värdet** bredvid användarnamnet, väljer användaren, väljer **hantera** och sedan **redigera**. På användarkortet väljer du **åtgärder**, **autentisering** och väljer sedan **ändra webbtjänstnyckeln**. |
| **Aktivera försäljningsorderintegrering** | När en användare skapar försäljningsorder i [!INCLUDE[crm_md](includes/crm_md.md)] och uppfyller order i [!INCLUDE[prod_short](includes/prod_short.md)] integreras processen i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Aktivera integrering av bearbetning av försäljningsorder](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Detta innebär att du anger autentiseringsuppgifter för en administratörs användarkonto i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i avsnittet [Hantera speciella försäljningsorderdata](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
|**Aktivera anslutning för Dynamics 365 Sales** | Aktivera anslutning till [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **SDK-version för Dynamics 365** | Detta gäller endast om du integrerar med en lokal version av [!INCLUDE[crm_md](includes/crm_md.md)]. Det här är den SDK-version för Dynamics 365 (även kallat Xrm) för att ansluta [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]. Versionen måste vara kompatibel med SDK-versionen som används av [!INCLUDE[crm_md](includes/crm_md.md)] och motsvarande eller senare än den version som används av [!INCLUDE[crm_md](includes/crm_md.md)]. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Anslutningsinställningar på inställningssidan för Microsoft Dynamics 365-anslutningar

Ange följande information om anslutningen från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[prod_short](includes/prod_short.md)].

| Fält | Beskrivning |
|--|--|
|**Dynamics 365 Sales-URL**|URL:en för din instans av [!INCLUDE[crm_md](includes/crm_md.md)]. Detta låter användare öppna motsvarande transaktioner i [!INCLUDE[prod_short](includes/prod_short.md)] från transaktioner i [!INCLUDE[crm_md](includes/crm_md.md)], exempelvis som konto eller produkt. [!INCLUDE[prod_short](includes/prod_short.md)]-poster är öppna i [!INCLUDE[prod_short](includes/prod_short.md)].|
|**Webbtjänsten Artikeldisposition har aktiverats**|Aktivera människor som använder [!INCLUDE[crm_md](includes/crm_md.md)] för att visa disponibla artiklar (produkter) i lagret i [!INCLUDE[prod_short](includes/prod_short.md)]. Om detta aktiveras måste du också ange ett namn och en snabbtangent för [!INCLUDE[crm_md](includes/crm_md.md)] för att fråga OData-webbtjänsten om disponibla artiklar (produkter). Mer information finns i [OData webbtjänst](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**Dynamics 365 Business Central OData webbtjänst-URL**|Om du aktiverar webbtjänsten för artikeldisposition anges URL för OData webbadressen för dig. Ange detta fält till url-adressen för den [!INCLUDE[prod_short](includes/prod_short.md)]-instans att använda.<br /><br /> Om du vill återställa fältet till standard-URL för [!INCLUDE[prod_short](includes/prod_short.md)], på Åtgärd-fliken, välj **Återställ webbklient-URL**.<br /><br /> Detta fält gäller endast om integreringslösningen för [!INCLUDE[prod_short](includes/prod_short.md)] har installerats i [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Dynamics 365 Business Central Användarnamn för OData-webbtjänsten**|Namnet på det användarkonto som [!INCLUDE[crm_md](includes/crm_md.md)] använder för att hämta information om artikeldisposition i [!INCLUDE[prod_short](includes/prod_short.md)] via webbtjänsten för OData.|
|**Dynamics 365 Business Central Åtkomstnyckel för OData-webbtjänsten**|Åtkomstnyckeln för det användarkonto som [!INCLUDE[crm_md](includes/crm_md.md)] använder för att hämta information om artikeldisposition från [!INCLUDE[prod_short](includes/prod_short.md)] via webbtjänsten för OData. Nyckeln tilldelas användaren i fältet **Dynamics 365 Business Central Användarnamn för OData-webbtjänsten**. Om du vill hämta nyckeln väljer du knappen **sök efter värdet** bredvid användarnamnet, väljer användaren, väljer **hantera** och sedan **redigera**. På användarkortet väljer du **åtgärder**, **autentisering** och väljer sedan **ändra webbtjänstnyckeln**.|
|**SDK-version för Dynamics 365**|Om du integrerar med en lokal version av [!INCLUDE[crm_md](includes/crm_md.md)] är det denna SDK-versionen för Dynamics 365 (även kallad Xrm) som du använder för att ansluta [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]. Den version som du väljer måste vara kompatibel med SDK-versionen som används av [!INCLUDE[crm_md](includes/crm_md.md)]. Den här versionen motsvarar eller är senare än den version som används av [!INCLUDE[crm_md](includes/crm_md.md)].|

Förutom inställningarna ovan anger du följande inställningar för [!INCLUDE[crm_md](includes/crm_md.md)].

| Fält | Beskrivning |
|--|--|
| **Försäljningsorderintegrering är aktiverad** | Användaren ska kunna skicka försäljningsorder och aktiverade offerter i [!INCLUDE[crm_md](includes/crm_md.md)] och sedan granska och bearbeta dem i [!INCLUDE[prod_short](includes/prod_short.md)]. Det här integrerar den här processen i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Aktivera integrering av bearbetning av försäljningsorder](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Skapa försäljningsorder automatiskt** | Skapa en försäljningsorder i [!INCLUDE[prod_short](includes/prod_short.md)] när en användare skapar och skickar en i [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Bearbeta försäljningsofferter automatiskt** | Bearbeta en försäljningsoffert i [!INCLUDE[prod_short](includes/prod_short.md)] när en användare skapar och aktiverar en i [!INCLUDE[crm_md](includes/crm_md.md)]. |

<!--
### User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Standardinställd försäljningsenhetsmappningar för synkronisering

Enheter i [!INCLUDE[crm_md](includes/crm_md.md)], till exempel order, är integrerade med motsvarande tabelltyper i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel försäljningsorder. För att arbeta med [!INCLUDE[crm_md](includes/crm_md.md)]-data anger du länkar kallade "kopplingar" mellan tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[crm_md](includes/crm_md.md)].

I följande tabell visas standardmappningen mellan tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] som [!INCLUDE[prod_short](includes/prod_short.md)] tillhandahåller.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synkroniseringsriktning | Standardfilter |
|--|--|--|--|
| Enhet | Enhetsgrupp | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Artikel | Produkt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-kontaktfilter: **produkttyp** är **Sales-lager** |
| Resurs | Produkt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-kontaktfilter: **produkttyp** är **Tjänster** |
| Kund prisgrupp | Prislista | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Förs.pris | Produktprislista | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] kontaktfilter: **försäljningskod** är inte tom, **förs.typ** är **kundprisgrupp** |
| Affärsmöjlighet | Affärsmöjlighet | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Försäljningsfakturahuvud | Fakturera | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Försäljningsfakturarad | Fakturaprodukt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Rubrik för försäljningsorder | Reservationstransaktion | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] Försäljningsrubrikfilter: **Dokumenttyp** är Order, **Status** är Frisläppt |
| Försäljningsordermeddelanden | Försäljningsordermeddelanden | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

### <a name="synchronization-rules"></a>Synkroniseringsregler

Följande tabell anger regler som kontrollerar synkroniseringen mellan [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)]. Dessa gäller utöver de regler som angetts för Dataverse, vilka också gäller. För mer information, se [Standardenhetsmappningar](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

> [!NOTE]  
> Ändrar data i  som genomfördes av användarkontot för integrering synkroniseras inte. Därför rekommenderar vi att du inte ändrar data när du använder kontot. Mer information finns i [Ställa in konton för att integrera med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Bord|Regel|
|-----|----|
|Enheter|Måttenheter synkroniseras med enhetsgrupper i [!INCLUDE[crm_md](includes/crm_md.md)]. Det kan finnas endast en måttenhet som definieras i enhetsgruppen.|
|Artiklar|När artiklar synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter skapar [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt en prislista i [!INCLUDE[crm_md](includes/crm_md.md)]. För att undvika synkroniseringsfel bör du inte ändra denna prislista manuellt.|
|Resurser|Resurser som ska synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter som har produktypen tjänster.|
|Kundprisgrupper|Kundprisgrupper synkroniseras med Sales-prislistor.|
|Förs.priser|Sales-priser som har försäljning skriver kundprisgrupp och har definierats försäljningskod synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-prislistrader|
|Affärsmöjligheter|Affärsmöjligheter som ska synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-affärsmöjligheter. Värdet för säljarkod definierar ägare till den kopplade tabellen i [!INCLUDE[crm_md](includes/crm_md.md)].|
|Bokförda försäljningsfakturor|Bokförda försäljningsfakturor som är synkroniserade med försäljningsfakturor. Innan du kan synkronisera en faktura är det bättre att synkronisera alla andra tabeller som kan delta i fakturan, från säljare till prislistor. Värdet för säljarkod i fakturarubriken definierar ägaren till den kopplade tabellen i Sales.|
|Försäljningsorder|När integrering av försäljningsorder har aktiverats synkroniseras försäljningsorder i [!INCLUDE[prod_short](includes/prod_short.md)] som har skapats från skickade försäljningsorder i [!INCLUDE[crm_md](includes/crm_md.md)] med försäljningsorder i INCLUDE SALES när de släpps. Innan du synkroniserar order bör du först synkronisera alla tabeller som ingår i ordern, till exempel säljare och prislistor. Fältet Säljarkod i orderrubriken definierar ägaren till den kopplade tabellen i [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Synkroniseringsjobb för Sales-integrering

Projekten körs i följande ordning i syfte att undvika kopplingsberoenden mellan tabeller. Det finns ytterligare jobb tillgängliga från Dataverse. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](./admin-job-queues-schedule-tasks.md).

1. MÅTTENHET – Dynamics 365 Sales synkroniseringsjobb  
2. RESURS-PRODUKTER – Dynamics 365 Sales synkroniseringsjobb  
3. ARTKEL-PRODUKTER – Dynamics 365 Sales synkroniseringsjobb  
4. ANPASSADPRISGRUPP – Dynamics 365 Sales-synkroniseringsjobb.
5. FÖRSÄLJNPRIS – PROUDUKTPRIS – Dynamics 365 Sales synkroniseringsjobb.
6. BOKFÖRD FÖRSÄLJNINGSFAKTURA-FAKT – Dynamics 365 Sales-synkroniseringsjobb.

### <a name="default-synchronization-job-queue-entries"></a>Poster för standardsynkroniseringjobbkön

I följande tabell beskrivs standardsynkroniseringjobben för Sales.  

|Projektkötransaktion|Beskrivning|Riktning|Registermappning för integrering|Standardfrekvens för synkronisering (minuter)|Standardväntetid för inaktivitet (minuter)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|MÅTTENHET – Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-enhetsgrupper med [!INCLUDE[prod_short](includes/prod_short.md)]-måttenheter.|Från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|MÅTTENHET|30|720<br> (12 tim)|
|RESURS-PRODUKTER – Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[prod_short](includes/prod_short.md)]-resurser.|Från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|RESURS-PRODUKT|30|720<br> (12 tim)|
|ARTIKEL – PRODUKT – Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[prod_short](includes/prod_short.md)]-artiklar.|Från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL-PRODUKT|30|1440<br> (24 tim)|
|ANPASSADPRISGRUPP – PRIS – Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] försäljningsprislistor med [!INCLUDE[prod_short](includes/prod_short.md)] kundprisgrupper.| |KUNDPRISGRUPPER – FÖRSÄLJNINGSPRISLISTOR|30|1440<br> (24 tim)|
|FÖRSÄLJNPRIS – PROUDUKTPRIS – Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] produktpriser med [!INCLUDE[prod_short](includes/prod_short.md)] försäljningspriser.||PRODUKTPRIS-FÖRSÄLJNINGSPRIS|30|1440<br> (24 tim)|
|BOKFÖRD FÖRSÄLJNINGSFAKTURA-FAKT – Dynamics 365 Sales synkroniseringsjobb|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-fakturor med [!INCLUDE[prod_short](includes/prod_short.md)] bokförda försäljningsfakturor.|Från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|FAKTUROR-BOKFÖRDA FÖRSÄLJNINGSFAKTUROR|30|1440<br> (24 tim)|
|Kundstatistik – Dynamics 365 Sales-synkronisering.|Uppdaterar [!INCLUDE[crm_md](includes/crm_md.md)]-konton med senaste [!INCLUDE[prod_short](includes/prod_short.md)] kundinformation. I [!INCLUDE[crm_md](includes/crm_md.md)] visas den här informationen i snabbformuläret **Business Central bankkontostatistik** som är kopplat till [!INCLUDE[prod_short](includes/prod_short.md)] kunder.<br /><br /> Informationen kan även uppdateras manuellt från varje kundpost. Mer information finns i [Koppla och synkronisera posterna manuellt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Obs:** denna jobbkötransaktion är endast relevant om [!INCLUDE[prod_short](includes/prod_short.md)] integreringslösning är installerad i [!INCLUDE[crm_md](includes/crm_md.md)]. |Ej tillämpbart|Ej tillämpbart|30|Ej tillämpbart| 

## <a name="connecting-to-on-premises-versions-of-business-central-2019-release-wave-1-and-microsoft-dynamics-nav-2018"></a>Ansluter till lokala versioner av Business Central 2019 utgivningscykel 1 och Microsoft Dynamics NAV 2018
Microsoft Power Platform-teamet har [meddelat](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse) att man kommer att fasa ut autentiseringstypen Office365. Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt som är äldre än Business Central 2019 utgivningscykel 1 måste du använda OAuth-autentiseringstypen för att ansluta till [!INCLUDE[crm_md](includes/crm_md.md)] online. Instruktionerna i det här avsnittet beskriver hur du ansluter följande produktversioner:

* Business Central 2019 utgivningscykel 1
* Microsoft Dynamics NAV 2018

### <a name="prerequisites"></a>Förutsättningar

- Du måste ha en Microsoft Azure-prenumeration. Ett provkonto kommer att fungera för programregistrering.
- [!INCLUDE[crm_md](includes/crm_md.md)] är konfigurerad för att använda någon av följande autentiseringstyper:

   - Office 365 (äldre)

     > [!IMPORTANT]
     > Från och med april 2022 kommer Office 365 (äldre) inte längre att stödjas. Mer information finns i [Viktiga ändringar (utfasningar) som kommer i Power Apps, Power Automate och kundengagemangsappar](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   - OAuth

### <a name="to-connect-business-central-2019-release-wave-1-and-dynamics-nav-2018"></a>Så här ansluter du Business Central 2019 utgivningscykel 1 och Dynamics NAV 2018

1. Importera integreringslösningen Microsoft Dynamics 365 Business Central i din [!INCLUDE[crm_md](includes/crm_md.md)]-miljö. Integreringslösningen finns i mappen CrmCustomization på [!INCLUDE[prod_short](includes/prod_short.md)] eller Dynamics NAV 2018 installation DVD. Beroende på produktversionen importerar du något av följande:

   * För [!INCLUDE[prod_short](includes/prod_short.md)] innehåller mappen DynamicsNAVIntegrationSolution_v9 och DynamicsNAVIntegrationSolution_v91. lösningar. Vilken lösning du bör importera beror på vilken version av [!INCLUDE[crm_md](includes/crm_md.md)] du ansluter till. [!INCLUDE[crm_md](includes/crm_md.md)] online kräver integreringslösningen DynamicsNAVIntegrationSolution_v91.
   * För Dynamics NAV 2018, installera lösningen DynamicsNAVIntegrationSolution.

2. Skapa en icke-interaktiv integrationsanvändare i din [!INCLUDE[crm_md](includes/crm_md.md)]-miljö och tilldela användaren följande säkerhetsroller. Mer information finns i [skapa ett icke-interaktivt användarkonto](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Dynamics 365 Business Central-integreringsadministratör
   * Dynamics 365 Business Central-integreringsanvändare

   > [!Important]
   > Den här användaren får inte ha säkerhetsrollen Systemadministratör. Du kan heller inte använda systemadministratörskontot som integrationsanvändare.

3.  Skapa en programregistrering för [!INCLUDE[prod_short](includes/prod_short.md)] i Azure-portalen. Mer information finns i [Registrera ett program i Azure Active Directory](/powerapps/developer/data-platform/walkthrough-register-app-azure-active-directory). 
  
   > [!NOTE]
   > Vi rekommenderar att du registrerar appen i samma klientorganisation som din Dataverse-miljö så att du inte behöver ge appen åtkomst till miljön. Om du registrerar appen i en annan miljö måste du logga in på Azure AD med administratörskontot för din Dataverse-miljö och ge tillstånd.
   >
   > Dessutom måste appen du registrerar inte ha någon hemlighet. Det går bara att ansluta en app med hemlighet till Dataverse i Business Central 2020 utgivningscykel 1 och senare.
  
4. Beroende på produktversionen importerar du något av följande:

    * I [!INCLUDE[prod_short](includes/prod_short.md)] söker du efter **Konfiguration av anslutning till Microsoft Dynamics 365** och väljer sedan relaterad länk. 
    * I Dynamics NAV 2018 söker du efter **Konfiguration av anslutning till Microsoft Dynamics 365 for Sales** och väljer sedan relaterad länk.

5. I fältet **Autentiseringstyp**, välj alternativet för OAuth. 
6. Välj den CRM SDK-version som matchar den lösningsversion som du importerade i steg 1.

   > [!NOTE]
   > Det här steget är bara relevant för [!INCLUDE[prod_short](includes/prod_short.md)].

7. Ange URL för din [!INCLUDE[crm_md](includes/crm_md.md)]-miljö och anger sedan användarnamn och lösenord för integrationsanvändaren. 

   * I [!INCLUDE[prod_short](includes/prod_short.md)] använd fältet **Serveradress**.
   * I Dynamics NAV 2018, använd fältet **Dynamics 365 Sales URL**.

8. I fältet **Anslutningssträng** anger du ID för programregistreringen. Detta fält har två token i vilka ID:t för ditt program ska anges.

   |Token           |Beskrivning  |
   |----------------|-------------|
   |**AppId**       |Ange program-ID.      |
   |**RedirectUri** |Ange program-ID, men Lägg till prefixet **app://**.         |

    **Exempel** Följande exempel visar en anslutningssträng.

    ```
    AuthType=OAuth;Username=jsmith@contoso.onmicrosoft.com;Password=****;Url=https://contosotest.crm.dynamics.com;AppId=<your AppId>;RedirectUri=app://<your AppId>;TokenCacheStorePath=;LoginPrompt=Auto
    ```
9. Aktivera anslutningen.

> [!Note]
> Om du vill konfigurera en anslutning till en [!INCLUDE[crm_md](includes/crm_md.md)]-instans med en specifik autentiseringstyp fyller du i fälten i snabbfliken **Information om autentiseringstyp**. Mer information finns i [Autentisering med Microsoft Dataverse webbtjänster](/powerapps/developer/data-platform/authentication). Detta steg är inte nödvändigt när du ansluter en onlineversion av [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Se även

[Ställa in konton för integrering med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Ställ in en anslutning till [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Synkroniserar Business Central och [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Förbereder Dynamics 365 Sales för integrering lokalt](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]
