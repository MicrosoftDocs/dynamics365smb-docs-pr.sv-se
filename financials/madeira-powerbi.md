---
title: "Dynamics 365 for Financials och Power BI innehållspaket | Microsoft Docs"
description: "Det är enkelt att få insikter, affärsstöd och KPI:er från dina Financials-data med Power BI och innehållspaketet för Financials ."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 537effab2f406d619c5000efad12754db678e8b8
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivera affärsdata för Power BI
Det är enkelt att få insikter om [!INCLUDE[d365fin](includes/d365fin_md.md)]-data med Power BI och innehållspaketet för  [!INCLUDE[d365fin](includes/d365fin_md.md)]. Power BI hämtar dina data och bygger en förinstallerad instrumentbräda och rapporter baserade på den data.  

Innehållspaketet är förkonfigurerat för att arbeta med försäljningsdata och ekonomiska data från demonstrationsföretaget som du får när du registrerar dig på förhandsgranskningen av [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].  

* Välj något visuellt på instrumentbrädan för att få upp en av sju underliggande rapporter.  
* Filtrera rapporten eller lägg till fält som du vill övervaka.  
* Sätt fast den här vyn på instrumentbrädan om du vill fortsätta spårningen.  
  Instrumentbrädan och underliggande rapporter uppdateras dagligen. Du kan kontrollera uppdateringsschemat och ändra frekvens på datauppsättningen.  

> [!NOTE]  
>   Du kan också skapa egna rapporter och instrumentpaneler i Power BI utifrån dina [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Mer information finns i [ansluta din affärsdata till Power BI ](across-how-use-financials-data-source-powerbi.md).  

## <a name="accessing-included365finincludesd365finmdmd-in-power-bi"></a>Öppna [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI
Om du vill se [!INCLUDE[d365fin](includes/d365fin_md.md)]-data in Power BI måste du ha följande:  

* Åtkomst till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Financials](http://go.microsoft.com/fwlink/?LinkID=759714).  
* Åtkomst till Power BI. Mer information finns i [Power BI](https://powerbi.microsoft.com).

Du hittar ytterligare information på webbplatsen för Power BI om [ansluta till tjänster med innehållspaket för Power BI](http://go.microsoft.com/fwlink/?LinkID=760850).  

För att komma åt dina [!INCLUDE[d365fin](includes/d365fin_md.md)]-data i Power BI, måste du på anslutningssidan ange följande information:

| Fält | Beskrivning |
| --- | --- |
| **OData feed URL** |OData-URL så att Power BI kan få åtkomst till data från ditt företag som t.ex. https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('My%2Business'). |
| **Autentiseringsmetod** |Välj **grundläggande**. |
| **Användarnamn** |Ditt namn som det visas för ditt konto i [!INCLUDE[d365fin](includes/d365fin_md.md)], såsom *John Smith*. |
| **Lösenord** |Detta är webbtjänståtkomstnyckel för ditt användarkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)]. |

Detta innebär dock att du måste ha 3 enheter av information från Financials : OData-URL och webbtjänståtkomstnyckel för ditt användarkonto.  

### <a name="getting-the-url"></a>Få URL:en
När du lägger till [!INCLUDE[d365fin](includes/d365fin_md.md)] till Power BI måste du ange en URL, så att Power BI kan komma åt data från företaget. I anslutningsfönstret kommer URL:en att hänvisas till som **OData Feed URL** och måste ha följande format:

         https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
I det här exemplet är *mybusiness* namnet på din Financials-tjänst och *CRONUS US* är namnet på demonstrationsföretaget med *%20* som representerar utrymmet i namnet.   
Om du vill få URL:en söker du efter och öppnar i [!INCLUDE[d365fin](includes/d365fin_md.md)], fönstret **Webbtjänster**. I det här fönstret visas webbtjänsterna som för närvarande finns tillgängliga och du kan kopiera länken från fältet **OData-URL** för en av de standardinställda OData-webbtjänsterna.  

### <a name="getting-the-user-name-and-the-web-service-access-key"></a>Hämtar användarnamnet och åtkomstnyckeln för webbtjänst
Om du vill använda data från [!INCLUDE[d365fin](includes/d365fin_md.md)]i Power BI, måste du i fönstret **Anslut till Financials** ange ett användarnamn och ett lösenord. Användarnamnet är ditt namn som visas för ditt konto i [!INCLUDE[d365fin](includes/d365fin_md.md)] så att Power BI kan logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lösenordet är webbtjänståtkomstnyckeln som är konfigurerad för ditt användarkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

För att hitta denna information i [!INCLUDE[d365fin](includes/d365fin_md.md)], söker du efter fönstret **användare** och öppnar kortet för ditt användarkonto. På snabbfliken **allmänt** kopierar du innehållet i fältet **användarnamn** och på snabbfliken **Webbtjänståtkomst** kopierar du innehållet i fältet **Webbtjänståtkomstnyckel**. Om fältet **Webbtjänståtkomstnyckel** är tomt väljer du **Ändra webbtjänståtkomstnyckel** i menyfliken, väljer fältet **Nyckeln upphör aldrig att gälla** och trycker sedan på OK-knappen. Du kan sedan kopiera nyckeln.  

## <a name="getting-data-from-included365finincludesd365finmdmd"></a>Hämta data från [!INCLUDE[d365fin](includes/d365fin_md.md)]
Instrumentbrädan för [!INCLUDE[d365fin](includes/d365fin_md.md)] visar de vanligaste rapporterna som du kommer att behöva använda för att spåra verksamheten. Data extraheras från ditt [!INCLUDE[d365fin](includes/d365fin_md.md)]-företag med webbtjänster för att läsa realtidsdata. I [!INCLUDE[d365fin](includes/d365fin_md.md)], anger fönstret **Webbtjänster** webbtjänsterna som har konfigurerats för dig, inklusive följande som förbrukas av innehållspaketet i Power BI:  

* ItemSalesAndProfit  
* ItemSalesByCustomer  
* powerbifinance  
* SalesDashboard  
* SalesOpportunities  
* SalesOrdersBySalesPerson  
* TopCustomerOverview  

> [!NOTE]  
>   Om du ändrar namnet på någon av dessa webbtjänster, kommer data inte att visas i Power BI.  
Om du vill lägga till i andra data i Power BI, måste du hitta tabellerna i [!INCLUDE[d365fin](includes/d365fin_md.md)], och exponera dem som webbtjänster och sedan lägga till dem i innehållspaketet. Detta är ett avancerat scenario och vi rekommenderar att du börjar med data som redan är tillgängliga i Power BI.  

## <a name="troubleshooting"></a>Felsökning
Instrumentbrädan för Power BI förlitar sig på de publicerade webbtjänsterna som visas ovan, och kommer att innehålla data från demonstrationsföretaget eller ditt eget företag om du importerar data från den aktuella finanslösningen. Men om något går fel kommer denna sektion att ge en tillfällig lösning för de vanligaste problemen.  

**"Parametervalidering misslyckades. Se till att alla parametrar är giltiga"**  
Om du ser det här felet efter att du har angett [!INCLUDE[d365fin](includes/d365fin_md.md)]-URL:en ska du se till att följande krav är uppfyllda:  

* URL:en följer exakt deta mönster:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Ta bort all text efter företagsnamnet i parentesen  
* Se till att det inte finns något avslutande snedstreck i slutet av URL:en.  
* Se till att det finns en säker anslutning som anges av URL:en som börjar med *https*.  

**"Inloggningen misslyckades"**  
Om du får felet Inloggningen misslyckades när du loggar in på instrumentbrädan med dina autentiseringsuppgifter för [!INCLUDE[d365fin](includes/d365fin_md.md)] kan detta orsakas av ett följande problem:

* Kontot som du använder har inte behörighet att läsa data från [!INCLUDE[d365fin](includes/d365fin_md.md)] från ditt konto.

    Kontrollera ditt användarkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)], och se till att du har använt rätt webbtjänståtkomstnyckel som lösenord och försök sedan igen.  
* Instansen [!INCLUDE[d365fin](includes/d365fin_md.md)] som du försöker att ansluta till har inte ett giltigt SSL-certifikat. I så fall visas en mer detaljerat felmeddelande ("det går inte att upprätta betrott SSL-förhållande").

    > [!NOTE]  
>   Självsignerade certifikat stöds inte.  

**"Hoppsan"**  
Om du ser feldialogen "Hoppsan" när du har passerat autentiseringdialogen, orsakas den oftast av ett problem vid anslutning av data för innehållspaketet.

* Kontrollera att URL:en följer mönstret som angavs tidigare:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Ett vanligt fel är att ange den fullständiga URL:en för en viss webbtjänst:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')/powerbifinance  
* Eller så har du glömt att ange företagsnamnet:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/  

## <a name="see-also"></a>Se även
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Migrera verksamhetsdata från andra finanssystem](upload-data.md)  
[Med hjälp av [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] som en Power BI-datakälla](across-how-use-financials-data-source-powerbi.md)  
[Med hjälp av [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] som en PowerApps-datakälla](across-how-use-financials-data-source-powerapps.md)  
[Med hjälp av [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]för Microsoft Flow](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
