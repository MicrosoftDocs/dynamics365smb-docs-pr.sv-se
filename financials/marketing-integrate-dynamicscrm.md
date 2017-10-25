---
title: "Hantera kunder som använder Dynamics 365 for Sales| Microsoft Docs"
description: "Du kan använda Dynamics 365 for Sales inne i Dynamics 365 for Financials för att mappa data och ha sömlös integration och synkronisering i processen från kundämne till betalning."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bc0b9c8141c6c2eac78abc9cd3f5c89af3c89fbb
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="managing-your-customer-relationships-using-dynamics-365-for-sales-from-inside-dynamics-365-for-financials"></a>Hantera kundrelationer med Dynamics 365 for Sales från insidan av Dynamics 365 for Financials
Om du använder Dynamics 365 for Sales för kundengagemang kan du använda [!INCLUDE[d365fin](includes/d365fin_md.md)] för orderbehandling och ekonomi och har sömlös integrering i processen från kundämne till betalning.

Om programmet har konfigurerats för integration med Dynamics 365 for Sales, har du åtkomst tillförsäljningsdata från [!INCLUDE[d365fin](includes/d365fin_md.md)]och tvärtom i vissa fall. Integrationen låter dig arbeta med och synkronisera datatyper som är gemensamma för båda tjänsterna, till exempel kunder, kontakter och försäljningsinformation och hålla informationen uppdaterad på båda platserna.  

Säljare i Dynamics 365 for Sales kan till exempel använda prislistor från [!INCLUDE[d365fin](includes/d365fin_md.md)] när de skapar en försäljningsorder. När de lägger till artikeln till försäljningsorderraden i Dynamics 365 for Sales kan de också visa lagernivån (tillgänglighet) av artikeln från [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dessa data har publicerats som en del av de assisterade konfigurationsguiden **anslutningsinställningar för Dynamics 365**.  

> [!NOTE]  
>   Den här funktionen kräver att din upplevelse är inställd på **Paket**. Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).  

## <a name="setting-up-the-connection"></a>Ställer in anslutning
Hemifrån kan du öppna den assisterade konfigurationsguiden **anslutningsinställningar för Dynamics 365** som hjälper dig att konfigurera anslutningen. När detta är klart får du en sömlös koppling av Dynamics 365 for Sales-poster med [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster.  

> [!NOTE]  
>   Förklarar de assisterade inställningarna, men du kan utföra samma aktiviteter manuellt i fönstret **installation av Dynamics 365-anslutning**.

I assisterade konfigurationsguiden, kan du välja vilka data som ska synkroniseras mellan två tjänster. Du kan också ange att du vill importera dina befintliga Dynamics 365 for Sales-lösning. I detta fall måste du ange behörigheter för ett användarkonto.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Konfigurera användarkontot för att importera lösningen
Om du vill importera en befintlig Dynamics 365 for Sales-lösning, använder guiden ett administratörskonto. Kontot måste vara en giltig användare i Dynamics 365 for Sales med följande säkerhetsrollerna:

* Systemadministratör  
* Lösningsanpassare  

Mer information finns i [skapa användare och tilldela säkerhetsroller i Microsoft Dynamics 365 (online)](https://technet.microsoft.com/library/jj191623.aspx) på techNet och [så här hanterar du användare och behörigheter ](ui-how-users-permissions.md).  

Det här kontot används bara vid installationen. När lösningen har importerats till [!INCLUDE[d365fin](includes/d365fin_md.md)], behövs inte längre kontot.

### <a name="setting-up-the-user-account-for-synchronization"></a>Konfigurera användarkontot för synkronisering
Integrering med hjälp av ett delat användarkonto används. Därför måste du i din Office 365-prenumeration skapa en särskild användare som ska användas för synkroniseringen mellan två tjänster. Kontot måste redan vara en giltig användare i Dynamics 365 for Sales, men du behöver inte tilldela säkerhetsroller till kontot eftersom guiden gör detta åt dig. Du måste ange det här kontot en eller flera gånger i inställningsguiden, beroende på hur mycket synkronisering du vill aktivera. Mer information finns i [skapa användare och tilldela säkerhetsroller i Microsoft Dynamics 365 (online)](https://technet.microsoft.com/library/jj191623.aspx) på techNet.

Om du vill aktivera *artikeldisposition*, måste integreringsanvändarkontot ha en snabbtangent för webbplatstjänster. Detta är eni två stegssak på sidan [!INCLUDE[d365fin](includes/d365fin_md.md)]för det användarkontot och du måste du välja knappen **ändra webbtjänstnyckeln** och i konfigurationsguiden för Dynamics 365 for Sales-anslutning måste du ange användaren som OData webbtjänstanvändare.

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

Försäljningsorder för Dynamics 365 for Sales beror på ytterligare information, till exempel kunder, enheter, valutor, kundprisgrupper, artiklar och/eller resurser. För att Dynamics 365 for Sales försäljningsorder ska fungera utan problem, måste du koppla kunder, enheter, valutor, kundprisgrupper, artiklar och/eller resurser först.

### <a name="synchronizing-records-fully"></a>Synkronisera poster helt
I slutet av den assisterade konfigurationsguiden kan du välja åtgärden **kör fullständig synkronisering** för att starta synkronisering av alla [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster med alla relaterade poster i den kopplade Dynamics 365 for Sales-lösningen. I fönstret **CRM fullständig synk.granskning** kan du välja åtgärden **starta**. Sedan börjar synkroniseringen köra projekt efter beroenden. Exempelvis synkroniseras valutaposter innan kundposter. Fullständig synkronisering kan ta lång tid och kommer att köras i bakgrunden så att du kan fortsätta att arbeta i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Om du vill kontrollera förloppet för enskilda projekt i en fullständig synkronisering, öka detaljnivån i fältet **Transaktionsstatus för jobbkö**, eller **Från projektstatus för int. tabell**, eller **CRM fullständig synk.granskning** i fönstret **CRM fullständig synk.granskning**.

Från fönstret **Konfigurera anslutning till Dynamics 365** kan du få information om fullständig synkronisering när som helst. Här kan du också öppna fönstret **Tabellmappningar för integrering** för att visa detaljerad information om tabeller i Financials och i Dynamics 365 for Sales-lösningen som måste synkroniseras.

## <a name="see-also"></a>Se även
[Kundhantering](marketing-relationship-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)]-upplevelse](ui-experiences.md)  
[Så här hanterar du användare och behörigheter](ui-how-users-permissions.md)    
[Integrera organisationen och användare till Dynamics 365 (online)](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

