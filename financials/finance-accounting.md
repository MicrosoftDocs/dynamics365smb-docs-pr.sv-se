---
title: "Financials revisormiljö | Microsoft Docs"
description: "Läs mer om revisorportalen för Dynamics 365 for Financials och rollcentret revisor som stöder intern och extern revisor i kundföretaget."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b75c223b01690703b57c427ff00267ed5af7a13e
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="accountant-experiences-in-included365finlongincludesd365finlongmdmd"></a>Revisorupplevelse i Financials [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Alla företag måste göra sin redovisning och godkänna redovisningen. Vissa företag använder en extern revisor och andra har en revisor bland personalen. Oavsett vilken typ av revisor som du är kan du använda rollcentret **revisor** som din startsida i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Härifrån kan du komma åt alla fönster som behövs i arbetet.  

## <a name="accountant-role-center"></a>Rollcentret Revisor
Rollcentret är en instrumentpanel med aktivitetpaneler sida som visar nyckeltal i realtid och ger dig snabb åtkomst till data. På menyn längst upp i fönstret har du tillgång till fler åtgärder, t ex öppna mest vanliga ekonomiska rapporter och rapporter i Excel. I navigeringsrutan till vänster, kan du snabbt växla mellan de listor som du använder oftast. Om du expanderar **Start**-menyn i navigeringsrutan, visas andra områden såsom **bokförda dokument** med olika typer av dokument som har bokförts i företaget.  

Om du har använt [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du starta en förteckning över videor direkt från din startsida. Du kan också starta en **komma igång** som pekar ut viktiga områden.  

> [!NOTE]  
>  Den här funktionen kräver att din upplevelse är inställd på **Paket**. Mer information finns i [anpassa din Financials-upplevelse](ui-experiences.md).  

### <a name="get-invited-to-a-clients-included365finincludesd365finmdmd"></a>Bli inbjuden till en klients [!INCLUDE[d365fin](includes/d365fin_md.md)]
Ett företag som använder [!INCLUDE[d365fin](includes/d365fin_md.md)]kan bjuda in dig till [!INCLUDE[d365fin](includes/d365fin_md.md)]som deras extern revisor. Detta innebär att de har installerat SMTP-post, så de kan behöva kontakta sina [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner för att få hjälp. Mer information finns i [bjud in din externa revisor](finance-invite-external-accountant.md). Vi rekommenderar att du anger den e.post som du vill använda för redovisningsarbetet – på så sätt kan du kan också välja om du vill använda *me@accountant.com* eller *me@client.com*  

Därför får du e-post från en klient med en länk till deras[!INCLUDE[d365fin](includes/d365fin_md.md)]  

Du kan sedan nå sina ekonomiska data från rollcentret **revisor**. Om du använder tillägget revisorportal kan du också lägga till klienten i listan över klienter i revisorportalens instrumentpanel.  

## <a name="accountant-portal"></a>Revisorsportal
Om du är en revisor med flera klienter, använd revisorportalen som en instrumentpanel för en bättre överblick över dina kunder. Härifrån kan du komma åt varje klients klientorganisationen i [!INCLUDE[d365fin](includes/d365fin_md.md)]och använda den för tollcentret redovisare som beskrivs ovan.  

Revisorportalen är en särskild version av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan få tillgång till instrumentpanelen genom att logga från [Financials for Accountants på Microsoft.com ](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants).  

> [!TIP]  
>  När du registrerar dig för portalen beräkning måste du ange din e-postadress för arbete som *me@accountant.com*. Vi rekommenderar att du använder samma e-postadress när du arbetar i klientens [!INCLUDE[d365fin](includes/d365fin_md.md)], så att du kan växla mellan klienter.  

När du först loggar in på revisorportalen visar instrumentpanelen en exempelklient för att du ska komma igång. När du är nöjd kan du ta bort exempelklienten.  

### <a name="working-with-individual-clients"></a>Arbeta med enskilda kunder
Instrumentpanelen visar den viktigaste informationen om varje klient.  
[![Revisorsportal](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)

Kolumnlistan **Företagsnamn** visar namnen på alla företag som dina kunder har i [!INCLUDE[d365fin](includes/d365fin_md.md)], och kolumnen **Klientnamn** visar namnen på dina kunder. Du kan anpassa instrumentpanelen att visa de datapunkter som du vill ska visas genom att lägga till eller ta bort kolumner. Du kanske vill visa moms som har förfallit till betalning, hur många öppna försäljningsdokument varje klient har eller antalet inköpsfakturor som förfaller nästa vecka. Du kan konfigurera vyn så att den passar dina behov. Om du har många klienter kan använda du filter för att sortera vyn.  

Bredvid företagsnamnet visar tre punkter (...) en kort meny:

* Uppdatera det aktuella företaget och hämta nya data för klienten  
* Gå till klientens företag  
* Markerade fler företag:  

På samma sätt kan du använda listrutan **klientsammanfattning** för att uppdatera alla företag eller för att öppna valda företag.  

### <a name="company-details"></a>Företagsdetaljer
Mer information om klientens data ser du genom att välja namnet på det företag som du vill veta mer om. Då öppnar rutan **Företagsdetaljer** där du kan visa ytterligare information, till exempel följande:  

* Saldon på kassakonto  
* Kassaflödesprognos  
* Förfallna inköpsfakturor  
* Förfallna försäljningsfakturor  

![Klientens företagsinformation på Revisorportalen](./media/finance-accounting/accountant-company-details.png)

Tekniskt sett är du nu inloggad i kundens [!INCLUDE[d365fin](includes/d365fin_md.md)], och informationen du ser är aktuella data. Om du vill titta närmare på data, till exempel förfallna inköpsfakturor väljer du länken och tas till kundföretaget.  

> [!TIP]  
>  Du kan starta en fördefinierad Excel-arbetsbok från fliken **rapporter** i menyfliksområdet. Dessa arbetsböcker är utformade som viktiga ekonomiska rapporter som är klara att skrivas ut och du kan också ändra dem efter behov. Mer information finns i [analys av finansiella rapporter i Microsoft Excel](finance-analyze-excel.md).  

I annat fall stänger du av informationsfönstret och fortsätter till nästa klient.  

### <a name="working-in-the-client-company"></a>Arbeta i kundföretaget
Om du vill utföra mer arbete för en klient kan du göra det i Rollcentret Revisor i deras [!INCLUDE[d365fin](includes/d365fin_md.md)] - välj bara menyobjektet **gå till klient** och du har loggat in automatiskt.  

I kundföretaget, kan du visa och ändra de data som du behöver i ditt arbete. Mer information finns längst upp på sidan.

> [!NOTE]  
>  Om du inte vill gå tillbaka till den här klienten senare rekommenderas att du stänger fliken.  

### <a name="adding-clients"></a>Lägga till klienter
Du kan lägga till en klient med hjälp av fönstret **klienter** som du öppnar genom att välja åtgärd **hantera klienter** i menyfliksområdet. Välj bara **Ny** och fyll sedan i relevanta fält.  

Datan i ett kort för varje klient som anges av dig och du kan ändra den efter behov. Men fältet **klient-URL** är kritiskt – detta är hur du får tillgång till varje klients [!INCLUDE[d365fin](includes/d365fin_md.md)]. Använd åtgärdem **Testa klient-URL** i menyfliksområdet för att kontrollera att du har angett rätt länk. Den URL-adress du måste ange pekar på klientens [!INCLUDE[d365fin](includes/d365fin_md.md)], såsom *https://mybusiness.financials.dynamics.com*. Denna URL används sedan när du väljer menyobjektet **gå till företag**.  

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Redovisningen och kontoplanen](finance-general-ledger.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Analysera finansiella rapporter i Excel](finance-analyze-excel.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Bjud in din externa revisorn till [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-invite-external-accountant.md)  
[Financials for Accountants på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
[Ställa in analysvy för kassaflöde](finance-setup-cash-flow-analyses.md)  

