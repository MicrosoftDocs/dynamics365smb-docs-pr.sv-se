---
title: Hantera kunder som använder Dynamics 365 for Sales| Microsoft Docs
description: Du kan använda Dynamics 365 for Sales inne i Business Central för att mappa data och ha sömlös integration och synkronisering i processen från kundämne till betalning.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 01/24/2019
ms.author: edupont
ms.openlocfilehash: bba9fb9a83856cea43e4f4215e7c148b713252a9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "808212"
---
# <a name="integrating-with-dynamics-365-for-sales"></a>Integrera med Dynamics 365 for Sales
Om du använder Dynamics 365 for Sales for Customer Engagement kan du använda [!INCLUDE[d365fin](includes/d365fin_md.md)] för orderbehandling och ekonomi och har sömlös integrering i processen från kundämne till betalning.

> [!NOTE]
> Det här avsnittet antar att både [!INCLUDE[d365fin](includes/d365fin_md.md)] och integrerade Sales-lösningen distribueras i en SaaS-miljö. Det går att blanda online och lokalt, men det kräver speciell konfiguration. Mer information finns i [Förbereder integration till Dynamics 365 for Sales lokalt](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Om programmet har konfigurerats för integration med Sales, har du åtkomst till försäljningsdata från [!INCLUDE[d365fin](includes/d365fin_md.md)] och tvärtom i vissa fall. Integrationen låter dig arbeta med och synkronisera datatyper som är gemensamma för båda tjänsterna, till exempel kunder, kontakter och försäljningsinformation och hålla informationen uppdaterad på båda platserna.  

Säljare i Sales kan till exempel använda prislistor från [!INCLUDE[d365fin](includes/d365fin_md.md)] när de skapar en försäljningsorder. När de lägger till artikeln till försäljningsorderraden i Sales kan de också visa lagernivån (tillgänglighet) av artikeln från [!INCLUDE[d365fin](includes/d365fin_md.md)].

På samma sätt kan orderprocessorer i [!INCLUDE[d365fin](includes/d365fin_md.md)] hantera speciella särdrag hos försäljningsorder som överförs automatiskt eller manuellt från Dynamics 365 for Sales, som t.ex. att automatiskt skapa och bokföra giltiga försäljningorderrader för artiklar eller resurser som har angetts i Dynamics 365 for Sales som produkter ej i register. Mer information finns i avsnittet ”Hantera speciella försäljningsorderdata”.

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] integreras endast med Dynamics 365 for Sales. Andra program och lösningar med Dynamics 365 som ändrar den standardinställda arbetsflödes- eller datamodellen i Sales, till exempel Project Service Automation, kan avbryta integreringen mellan [!INCLUDE[d365fin](includes/d365fin_md.md)]och Sales.

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Standardinställd försäljningsenhetsmappningar för synkronisering
Sales-enheter, till exempel konton, är integrerade med likvärdiga [!INCLUDE[d365fin](includes/d365fin_md.md)]-posttyper, till exempel kunder. Om du vill arbeta med försäljningsdata installerar du kopplingar mellan [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster och Sales-enhetsposter  Till exempel skapar du en koppling mellan en specifik kund i [!INCLUDE[d365fin](includes/d365fin_md.md)] och motsvarande konto i Sales.

Efterföljande tabell listar [!INCLUDE[d365fin](includes/d365fin_md.md)]-posttyperna (tabeller) och motsvarande Sales-enheter som kan synkroniserades direkt.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|FÖRS|Synkroniseringsriktning|Standardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Säljare/Inköpare|Användare|Sales -> Business Central|Sales-kontaktfilter: **Status** är **Nej**, **licensierad användare** är **Ja**, integrationsanvändarläge är **Nej**|
|Kund|Konto|Business Central -> Sales och Sales -> Business Central|Sales-kontofilter: **Relationstyp** är **Kund** och **Status** är **Aktiv**.|
|Kontakt|Kontakt|Business Central -> Sales och Sales -> Business Central|Business Central-kontaktfilter: **Typ** är **Person** och kontakten har tilldelats till ett företag. Sales-kontaktfilter: Kontakten har tilldelats till ett företag och överordnad kundtyp är **Konto**|
|Valuta|Transaktionsvaluta|Business Central -> Sales| |
|Måttenhet|Enhetsgrupp|Business Central -> Sales| |
|Artikel|Produkt|Business Central -> Sales och Sales -> Business Central|Sales-kontaktfilter: **produkttyp** är **Sales-lager**|
|Resurs|Produkt|Business Central -> Sales och Sales -> Business Central|Sales-kontaktfilter: **produkttyp** är **Tjänster**|
|Kund prisgrupp|Prislista|Business Central -> Sales| |
|Förs.pris|Produktprislista|Business Central -> Sales|Business Central kontaktfilter: **Sales-kod** är inte tom, **förs.typ** är **kundprisgrupp**|
|Affärsmöjlighet|Affärsmöjlighet|Business Central -> Sales och Sales -> Business Central| |
|Försäljningsfakturahuvud|Fakturera|Business Central -> Sales| |
|Försäljningsfakturarad|Fakturaprodukt|Business Central -> Sales| |

Sales-enheter och [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller som ska synkroniseras definieras genom tabellmappningsposter i tabell 5335 med **Tabellmappning för integrering**. Du kan visa mappningarna och skapa filter från sidan 5335, **Tabellmappningar för integrering**. Mappningen mellan fälten i [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster och fälten i Sales-enheter definieras av fältmappningsposter i tabellen 5336 **Fältmappning för integrering** och med ytterligare mappningslogik.

### <a name="field-mapping-for-the-sales-account-option"></a>Fältmappning för alternativet Sales-konto
Tre tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] mappas till alternativfältet o enheten **konto**.   

Posterna i tabellen, som inte är kopplade till de alternativ som finns i Sales hoppas över under synkroniseringen. Det innebär att fälten **alternativet** kommer att vara tomt i Sales.

Följande tabell visar mappningar från Business Central-tabeller för fältet **alternativ** i enheten **konto**.

|Bord|Alternativfältet i kontoentiteten i Sales|
|----------------------|-------------------------------------------|
|Betalningsvillkor|Betalningsvillkor|
|Utleveransvillkor|Adress 1: Leveransvillkor|
|Speditör|Adress 1: Leveransmetod|

### <a name="synchronization-rules"></a>Synkroniseringsregler
Följande tabell beskriver regler som kontrollerar synkroniseringen mellan Business Central-tabeller och Sales-tabeller.

> [!NOTE]  
> Ändringar av data i Sales, som utförs av Sales-anslutningskontot, ignoreras. Ändringarna synkroniseras inte. Därför rekommenderas det att du inte gör ändringar av data med hjälp av Sales-anslutningskontot.

|Bord|Regel|
|-----|----|
|Kunder|Innan en kund kan synkroniseras till ett konto måste försäljningpersonen, som tilldelats kunden, kopplas till en Sales-användare. Därför när du vill köra synkroniseringsjobbet KUNDER – Dynamics 365 for Sales och du ställer in det till att skapa nya poster, säkerställ att du synkroniserar säljare med Sales innan du synkroniserar kunder med Sales-konton. <br /> <br />Synkroniseringsjobbet KUNDER – Dynamics 365 for Sales synkroniserar endast Sales-konton som har relationstypen Kund.|
|Kontakter|Endast kontakter i Sales som associeras med ett konto skapas i Business Central. Säljarkod värdet definierar ägare till den kopplade enheten i Sales..|
|Valutor|Valutor kopplas till transaktionvalutor i Sales baserat på iso-koder. Endast valutor, som har en standard-ISO-kod, kopplas och synkroniseras med transaktionsvalutor.|
|Enheter|Måttenheter synkroniseras med enhetsgrupper i Sales. Det kan finnas endast en måttenhet som definieras i enhetsgruppen.|
|Artiklar|När artiklar synkroniseras med Sales-produkter skapar Business Central automatiskt en prislista i Sales. För att undvika synkroniseringsfel bör du inte ändra denna prislista manuellt.|
|Säljare|Säljare är kopplat till systemanvändare i Sales. Användaren måste vara aktiverad och licens och vara integrationsanvändaren. Observera att detta är den första tabellen som måste synkroniseras eftersom den används i kunder, kontaktpersoner, affärsmöjligheter och fakturor.|
|Resurser|Resurser som ska synkroniseras med Sales-produkter som har produktypen tjänster.|
|Kundprisgrupper|Kundprisgrupper synkroniseras med Sales-prislistor.|
|Förs.priser|Sales-priser som har försäljning skriver kundprisgrupp och har definierats försäljningskod synkroniseras med förs.prislistrader|
|Affärsmöjligheter|Affärsmöjligheter som ska synkroniseras med Sales-affärsmöjligheter. Säljarkod värdet definierar ägare till den kopplade enheten i Sales..|
|Bokförda försäljningsfakturor|Bokförda försäljningsfakturor som är synkroniserade med försäljningsfakturor. Innan du kan synkronisera en faktura, är det bättre att synkronisera alla andra enheter som kan delta i fakturan från säljare till prislistor. Säljarkodvärdet i fakturarubriken definierar ägare till den kopplade enheten i Sales.|

## <a name="setting-up-the-connection"></a>Ställer in anslutningen
Hemifrån kan du öppna den assisterade **Microsoft Dynamics 365 konfigurationsguiden** anslutningsinställningar som hjälper dig att konfigurera anslutningen. När detta är klart får du en sömlös koppling av Sales-poster med [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster.  

> [!NOTE]  
>   Förklarar de assisterade inställningarna, men du kan utföra samma aktiviteter manuellt på sidan **installation av Sales-anslutning**.

I assisterade konfigurationsguiden, kan du välja vilka data som ska synkroniseras mellan två tjänster. Du kan också ange att du vill importera dina befintliga Sales-lösning. I detta fall måste du ange behörigheter för ett användarkonto.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Konfigurera användarkontot för att importera lösningen
Om du vill importera en befintlig Sales-lösning, använder guiden ett administratörskonto. Kontot måste vara en giltig användare i Sales med följande säkerhetsrollerna:

* Systemadministratör  
* Lösningsanpassare  

Mer information finns i [Skapa användare i Microsoft Dynamics 365 (online) och tilldela säkerhetsroller i ](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) och [Hantera användare och behörigheter](ui-how-users-permissions.md).  

Det här kontot används bara vid installationen. När lösningen har importerats till [!INCLUDE[d365fin](includes/d365fin_md.md)], behövs inte längre kontot.

### <a name="setting-up-the-user-account-for-synchronization"></a>Konfigurera användarkontot för synkronisering
Integrering med hjälp av ett delat användarkonto används. Därför måste du i din Office 365-prenumeration skapa en särskild användare som ska användas för synkroniseringen mellan två tjänster. Kontot måste redan vara en giltig användare i Sales, men du behöver inte tilldela säkerhetsroller till kontot eftersom guiden gör detta åt dig. Du måste ange det här kontot en eller flera gånger i inställningsguiden, beroende på hur mycket synkronisering du vill aktivera. Mer information finns i [Skapa användare i Microsoft Dynamics 365 (online) och tilldela säkerhetsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Om du vill aktivera *artikeldisposition*, måste integreringsanvändarkontot ha en snabbtangent för webbplatstjänster. Detta är eni två stegssak på sidan [!INCLUDE[d365fin](includes/d365fin_md.md)]för det användarkontot och du måste du välja knappen **ändra webbtjänstnyckeln** och i konfigurationsguiden för Sales-anslutning måste du ange användaren som OData webbtjänstanvändare.

Om du vill aktivera *integrering av försäljningsorder*, måste du ange en användare som kan hantera synkroniseringen - Integrationsanvändare eller ett annat konto.

### <a name="coupling-records"></a>Kopplingsposter
I assisterade konfigurationsguiden, kan du välja vilka data som ska synkroniseras mellan två tjänster. Men du kan också ange inställningar för synkronisering av vissa typer av data. Detta kallas *koppling*, och det här avsnittet innehåller rekommendationer som du måste ta hänsyn till.

Till exempel om du vill visa Sales-konton som kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du koppla de två typerna av poster. Det är inte mycket komplicerat, öppna sidan **Kundlista** i [!INCLUDE[d365fin](includes/d365fin_md.md)], och det finns en åtgärd i menyfliksområdet för att koppla dessa data med Sales. Därefter anger du vilka [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder som matchar vilka konton i Sales.

I vissa områden måste funktionen koppla vissa uppsättningar data innan andra uppsättningar data visas i följande lista:

* Kunder och konton.  
  * Koppla säljare först med Sales-användare  
* Artiklar och resurser  
  * Koppla först måttenheter med Sales enhetsgrupper  
* Artiklar och resurspriser  
  * Koppla kundprisgrupper med Sales-priser först  

> [!NOTE]  
>   Om du använder priser i utländska valutor, se till att du kopplar valutor till Sales-transaktionsvalutor.

Försäljningsorder för Sales beror på ytterligare information, till exempel kunder, enheter, valutor, kundprisgrupper, artiklar och/eller resurser. För att integrera med försäljningsorder utan problem, måste du koppla kunder, enheter, valutor, kundprisgrupper, artiklar och/eller resurser först.

### <a name="synchronizing-records-fully"></a>Synkronisera poster helt
I slutet av den assisterade konfigurationsguiden kan du välja åtgärden **kör fullständig synkronisering** för att starta synkronisering av alla [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster med alla relaterade poster i den kopplade Sales-lösningen. På sidan **CRM fullständig synk.granskning** kan du välja åtgärden **starta**. Sedan börjar synkroniseringen köra projekt efter beroenden. Exempelvis synkroniseras valutaposter innan kundposter. Fullständig synkronisering kan ta lång tid och kommer att köras i bakgrunden så att du kan fortsätta att arbeta i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Om du vill kontrollera förloppet för enskilda projekt i en fullständig synkronisering, öka detaljnivån i fältet **Transaktionsstatus för jobbkö**, eller **Från projektstatus för int. tabell**, eller **CRM fullständig synk.granskning** på sidan **CRM fullständig synk.granskning**.

Från sidan Konfigurera anslutning till **Microsoft Dynamics 365** kan du få information om fullständig synkronisering när som helst. Här kan du också öppna sidan **Tabellmappningar för integrering** för att visa detaljerad information om tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] och i Sales-lösningen som måste synkroniseras.

## <a name="handling-special-sales-order-data"></a>Hantering av speciella försäljningsorderdata
Försäljningsorder i Sales kommer att överföras till [!INCLUDE[d365fin](includes/d365fin_md.md)] automatiskt om du markerar kryssrutan **Automatiskt skapa försäljningsorder** på sidan **Microsoft Dynamics 365, konfigurera anslutning**. På sådana försäljningsorder överförs fältet **Namn** på den ursprungliga ordern och mappas till fältet **Externa verifikationsnummer** på försäljningsordern i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Detta fungerar även om den ursprungliga försäljningsordern innehåller produkter som ej är i register vilket avser artiklar eller resurser som inte är registrerade hos någon produkt. I så fall måste du fylla i fälten **Produkttyp ej i register** och **Produktnr ej i register** på sidan **Försäljningsinställningar** så att denna oregistrerade produktförsäljning mappas till ett angivet artikel-/resursnummer för ekonomisk analys.

Om artikelbeskrivningen på den ursprungliga försäljningsordern är mycket omfattande, skapas en ytterligare försäljningsorderrad av typen Kommentar för att hålla hela texten på försäljningsordern i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se även
[Förbereda för integrering till Dynamics 365 for Sales lokalt](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)  
[Kundhantering](marketing-relationship-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Hantera användare och behörigheter](ui-how-users-permissions.md)    
[Integrera organisationen och användare till Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
