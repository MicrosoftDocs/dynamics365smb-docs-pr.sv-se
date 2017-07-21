---
title: "Financials revisormiljö | Microsoft Docs"
description: "Läs mer om revisorportalen för Dynamics 365 for Financials och rollcentret revisor som stöder revisorn i kundföretaget."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 06/20/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bef1e9097a958c2f447e64ff33c7081a1d305f38
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="accountant-experiences-in-included365finincludesd365finmdmd"></a>Revisorupplevelse i Financials [!INCLUDE[d365fin](includes/d365fin_md.md)]
Alla företag måste göra sin redovisning och godkänna redovisningen. Vissa företag använder en extern revisor och andra har en revisor bland personalen. Oavsett vilken typ av revisor som du är kan du använda rollcentret **revisor** som din startsida i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Härifrån kan du komma åt alla fönster som behövs i arbetet.  

## <a name="accountant-role-center"></a>Rollcentret Revisor
Rollcentret är en instrumentpanel med aktivitetpaneler sida som visar nyckeltal i realtid och ger dig snabb åtkomst till data. På menyn längst upp i fönstret har du tillgång till fler åtgärder. I navigeringsrutan till vänster, kan du snabbt växla mellan de listor som du använder oftast. Om du expanderar **Start**-menyn i navigeringsrutan, visas andra områden såsom **bokförda dokument** med olika typer av dokument som har bokförts i företaget.  

Om du har använt [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du starta en förteckning över videor direkt från din startsida. Du kan också starta en **komma igång** som pekar ut viktiga områden.  

> [!NOTE]  
>  Den här funktionen kräver att din upplevelse är inställd på **Paket**. Mer information finns i [anpassa din finansiella upplevelse](ui-experiences.md).  

### <a name="get-invited-to-a-clients-included365finincludesd365finmdmd"></a>Bli inbjuden till en klients [!INCLUDE[d365fin](includes/d365fin_md.md)]
Ett företag som använder [!INCLUDE[d365fin](includes/d365fin_md.md)]kan bjuda in dig till [!INCLUDE[d365fin](includes/d365fin_md.md)]som deras extern revisor. Detta kräver att en administratör lägger till din e-postadress för arbete i deras Active Directory-klientorganisation och vi rekommenderar att de kontaktar sin [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner för att få hjälp. Vi rekommenderar att du anger den e.post som du vill använda för redovisningsarbetet – på så sätt kan du kan också välja om du vill använda *me@accountant.com* eller *me@client.com*  

Därför få du två e-postmeddelanden:

-   Ett från Microsoft Invitations med en länk för att lägga till dig själv i klientens organisation  
-   En från en klient med en länk till deras [!INCLUDE[d365fin](includes/d365fin_md.md)]  

Du kan sedan nå sina ekonomiska data från rollcentret **revisor**. Om du använder tillägget **revisorportal** kan du också lägga till klienten i listan över klienter i revisorportalens instrumentpanel.  

## <a name="accountant-portal"></a>Revisorsportal
Om du är en revisor med flera klienter, använd revisorportalen som en instrumentpanel för en bättre överblick över dina kunder. Härifrån kan du komma åt varje klients klientorganisationen i [!INCLUDE[d365fin](includes/d365fin_md.md)]och använda den för tollcentret redovisare som beskrivs ovan.  

Revisorportalen är en särskild version av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan få tillgång till portalen om du registrerar dig från [Financials for Accountants på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants), och genom att lägga till [tillägget Revisorportal](ui-extensions-accountant-portal.md) till din [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>  När du registrerar dig för revisorportalen måste du ange din e-postadress för arbete som *me@accountant.com*. Vi rekommenderar att du använder samma e-postadress när du arbetar i klientens [!INCLUDE[d365fin](includes/d365fin_md.md)], så att du kan växla mellan klienter.  

När du först loggar in på revisorportalen visar instrumentpanelen en exempelklient för att du ska komma igång. När du är nöjd kan du ta bort exempelklienten.  

### <a name="working-with-individual-clients"></a>Arbeta med enskilda kunder
Instrumentpanelen visar den viktigaste informationen om varje klient.  
[![Revisorsportal](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)

Kolumnen **klientnamn** visar namnen på kunder och kolumnen **företagsnamn** visar alla företag om klienten har mer än ett företag i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan anpassa instrumentpanelen att visa de datapunkter som du vill ska visas genom att lägga till eller ta bort kolumner. Du kanske vill visa moms som har förfallit till betalning, hur många öppna försäljningsdokument varje klient har eller antalet inköpsfakturor som förfaller nästa vecka. Du kan konfigurera vyn så att den passar dina behov. Om du har många klienter kan använda du filter för att sortera vyn.  

Bredvid klienten visar tre punkter en kort meny:

-   Uppdatera det aktuella företaget och hämta nya data för klienten  
-   Gå till klientens [!INCLUDE[d365fin](includes/d365fin_md.md)]  
-   Välj fler klienter  

På samma sätt kan du använda listrutan **klientsammanfattning** för att uppdatera alla företag.  

Alla andra produkter som du använder för varje klient kan du göra i rollcentret revisor i deras [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>  För att få åtkomst till en klients [!INCLUDE[d365fin](includes/d365fin_md.md)], väljer du menyobjektet **gå till klient** - du loggas in automatiskt.

### <a name="adding-clients"></a>Lägga till klienter
Du kan lägga till en klient med hjälp av fönstret **klienter** som du öppnar genom att välja åtgärd **hantera klienter** i menyfliksområdet. Välj bara **Ny** och fyll sedan i relevanta fält.  

Datan i ett kort för varje klient som anges av dig och du kan ändra den efter behov. Men fältet **klient-URL** är kritiskt – detta är hur du får tillgång till varje klients [!INCLUDE[d365fin](includes/d365fin_md.md)]. Använd åtgärdem **Testa klient-URL** i menyfliksområdet för att kontrollera att du har angett rätt länk. URL:en som du måste ange pekar på klientens [!INCLUDE[d365fin](includes/d365fin_md.md)], såsom *https://mybusiness.financials.dynamics.com*. Denna URL används sedan när du väljer menyobjektet **gå till klient**.  

<!--If you have been invited to a client's [!INCLUDE[d365fin](includes/d365fin_md.md)] and signed in with your work account, then the client will be added to your dashboard in the accountant portal. -->

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Redovisningen och kontoplanen](finance-general-ledger.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Sortering](ui-sorting.md)  
[Ange villkor i filter](ui-enter-criteria-filters.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Bjud in din externa revisorn till [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-invite-external-accountant.md)  
[Financials for Accountants på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

