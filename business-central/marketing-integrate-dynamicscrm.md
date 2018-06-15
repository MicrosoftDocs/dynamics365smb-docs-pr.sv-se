---
title: "Hantera kunder som använder Dynamics 365 for Sales| Microsoft Docs"
description: "Du kan använda Dynamics 365 for Sales uniti Business Central för att mappa data och ha sömlös integration och synkronisering i processen från kundämne till betalning."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 05/24/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: f9ac1c1e1a9f4ca043ddd87c98c8014ca96d8c87
ms.contentlocale: sv-se
ms.lasthandoff: 05/28/2018

---
# <a name="managing-customers-and-sales-created-in-dynamics-365-for-sales"></a>Hantera kunder och försäljningsorder som har skapats i Dynamics 365 for Sales
Om du använder Dynamics 365 for Sales för kundengagemang kan du använda [!INCLUDE[d365fin](includes/d365fin_md.md)] för orderbehandling och ekonomi och har sömlös integrering i processen från kundämne till betalning.

Om programmet har konfigurerats för integration med Dynamics 365 for Sales, har du åtkomst tillförsäljningsdata från [!INCLUDE[d365fin](includes/d365fin_md.md)] och tvärtom i vissa fall. Integrationen låter dig arbeta med och synkronisera datatyper som är gemensamma för båda tjänsterna, till exempel kunder, kontakter och försäljningsinformation och hålla informationen uppdaterad på båda platserna.  

Säljare i Dynamics 365 for Sales kan till exempel använda prislistor från [!INCLUDE[d365fin](includes/d365fin_md.md)] när de skapar en försäljningsorder. När de lägger till artikeln till försäljningsorderraden i Dynamics 365 for Sales kan de också visa lagernivån (tillgänglighet) av artikeln från [!INCLUDE[d365fin](includes/d365fin_md.md)].

På samma sätt kan orderprocessorer i [!INCLUDE[d365fin](includes/d365fin_md.md)] hantera speciella särdrag hos försäljningsorder som överförs automatiskt eller manuellt från Dynamics 365 for Sales, som t.ex. att automatiskt skapa och bokföra giltiga försäljningorderrader för artiklar eller resurser som har angetts i Sales som produkter ej i register. Mer information finns i avsnittet ”Hantera speciella försäljningsorderdata”.  

## <a name="setting-up-the-connection"></a>Ställer in anslutning
Från Start kan du öppna den assisterade konfigurationsguiden **anslutningsinställningar för Microsoft Dynamics 365** som hjälper dig att konfigurera anslutningen. När detta är klart får du en sömlös koppling av Dynamics 365 for Sales-poster med [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster.  

> [!NOTE]  
>   Förklarar de assisterade inställningarna, men du kan utföra samma aktiviteter manuellt i fönstret **installation av Dynamics 365 for Sales-anslutning**.

I assisterade konfigurationsguiden, kan du välja vilka data som ska synkroniseras mellan två tjänster. Du kan också ange att du vill importera dina befintliga Dynamics 365 for Sales-lösning. I detta fall måste du ange behörigheter för ett användarkonto.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Konfigurera användarkontot för att importera lösningen
Om du vill importera en befintlig Dynamics 365 for Sales-lösning, använder guiden ett administratörskonto. Kontot måste vara en giltig användare i Dynamics 365 for Sales med följande säkerhetsrollerna:

* Systemadministratör  
* Lösningsanpassare  

Mer information finns i [skapa användare och tilldela säkerhetsroller i Microsoft Dynamics 365 (online)](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) och [så här hanterar du användare och behörigheter](ui-how-users-permissions.md).  

Det här kontot används bara vid installationen. När lösningen har importerats till [!INCLUDE[d365fin](includes/d365fin_md.md)], behövs inte längre kontot.

### <a name="setting-up-the-user-account-for-synchronization"></a>Konfigurera användarkontot för synkronisering
Integrering med hjälp av ett delat användarkonto används. Därför måste du i din Office 365-prenumeration skapa en särskild användare som ska användas för synkroniseringen mellan två tjänster. Kontot måste redan vara en giltig användare i Dynamics 365 for Sales, men du behöver inte tilldela säkerhetsroller till kontot eftersom guiden gör detta åt dig. Du måste ange det här kontot en eller flera gånger i inställningsguiden, beroende på hur mycket synkronisering du vill aktivera. Mer information finns i [skapa användare och tilldela säkerhetsroller i Microsoft Dynamics 365 (online)](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Om du vill aktivera *artikeldisposition*, måste integreringsanvändarkontot ha en snabbtangent för webbplatstjänster. Detta är en tvåstegsåtgärd på sidan [!INCLUDE[d365fin](includes/d365fin_md.md)] för användarkontot; du måste du välja knappen **Ändra webbtjänstnyckel**, och i konfigurationsguiden för Dynamics 365 for Sales-anslutning måste du ange användaren som OData-webbtjänstanvändare.

Om du vill aktivera *integrering av försäljningsorder*, måste du ange en användare som kan hantera synkroniseringen - Integrationsanvändare eller ett annat konto.

### <a name="coupling-records"></a>Kopplingspost
I assisterade konfigurationsguiden, kan du välja vilka data som ska synkroniseras mellan två tjänster. Men du kan också ange inställningar för synkronisering av vissa typer av data. Detta kallas *koppling*, och det här avsnittet innehåller rekommendationer som du måste ta hänsyn till.

Till exempel om du vill visa Dynamics 365 for Sales-konton som kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du koppla de två typerna av poster. Det är inte mycket komplicerat, öppna fönstret **Kundlista** i [!INCLUDE[d365fin](includes/d365fin_md.md)], och det finns en åtgärd i menyfliksområdet för att koppla dessa data med Dynamics 365 for Sales. Därefter anger du vilka [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder som matchar vilka konton i Dynamics 365 for Sales.

I vissa områden måste funktionen koppla vissa uppsättningar data innan andra uppsättningar data visas i följande lista:

* Kunder och konton.  
  * Koppla säljare först med Dynamics 365 for Sales-användare  
* Artiklar och resurser  
  * Koppla först måttenheter med Dynamics 365 for Sales enhetsgrupper  
* Artiklar och resurspriser  
  * Koppla kundprisgrupper med Dynamics 365 for Sales priser först  

> [!NOTE]  
>   Obs! Om du använder priser i utländska valutor, se till att du kopplar valutor till Dynamics 365 for Sales transaktionsvalutor.

Försäljningsorder för Dynamics 365 for Sales beror på ytterligare information, till exempel kunder, enheter, valutor, kundprisgrupper, artiklar och/eller resurser. För att integrera med försäljningsorder utan problem, måste du koppla kunder, enheter, valutor, kundprisgrupper, artiklar och/eller resurser först.

### <a name="synchronizing-records-fully"></a>Synkronisera poster helt
I slutet av den assisterade konfigurationsguiden kan du välja åtgärden **kör fullständig synkronisering** för att starta synkronisering av alla [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster med alla relaterade poster i den kopplade Dynamics 365 for Sales-lösningen. I fönstret **CRM fullständig synk.granskning** kan du välja åtgärden **starta**. Sedan börjar synkroniseringen köra projekt efter beroenden. Exempelvis synkroniseras valutaposter innan kundposter. Fullständig synkronisering kan ta lång tid och kommer att köras i bakgrunden så att du kan fortsätta att arbeta i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Om du vill kontrollera förloppet för enskilda projekt i en fullständig synkronisering, öka detaljnivån i fältet **Transaktionsstatus för jobbkö**, eller **Från projektstatus för int. tabell**, eller **CRM fullständig synk.granskning** i fönstret **CRM fullständig synk.granskning**.

Via fönstret **Konfigurera anslutning till Microsoft Dynamics 365** kan du när som helst få information om fullständig synkronisering. Här kan du också öppna fönstret **Tabellmappningar för integrering** för att visa detaljerad information om tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] och i Dynamics 365 for Sales-lösningen som måste synkroniseras.  

## <a name="handling-special-sales-order-data"></a>Hantering av speciella försäljningsorderdata
Försäljningsorder i Dynamics 365 for Sales kommer att överföras till [!INCLUDE[d365fin](includes/d365fin_md.md)] automatiskt om du markerar kryssrutan **Automatiskt skapa försäljningsorder** i fönstret **Konfigurera anslutning till Microsoft Dynamics 365**. På sådana försäljningsorder överförs fältet **Namn** på den ursprungliga ordern och mappas till fältet **Externa verifikationsnummer** på försäljningsordern i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Detta fungerar även om den ursprungliga försäljningsordern innehåller produkter som ej är i register vilket avser artiklar eller resurser som inte är registrerade hos någon produkt. I så fall måste du fylla i fälten **Produkttyp ej i register** och **Produktnr ej i register** i fönstret **Försäljningsinställningar** så att denna oregistrerade produktförsäljning mappas till ett angivet artikel-/resursnummer för ekonomisk analys.

Om artikelbeskrivningen på den ursprungliga försäljningsordern är mycket omfattande, skapas en ytterligare försäljningsorderrad av typen Kommentar för att hålla hela texten på försäljningsordern i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se även
[Kundhantering](marketing-relationship-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Hantera användare och behörigheter](ui-how-users-permissions.md)    
[Integrera organisationen och användare till Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

