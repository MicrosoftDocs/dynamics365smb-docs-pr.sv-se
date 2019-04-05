---
title: Business Central- och Power BI-innehållspaket | Microsoft Docs
description: Det är enkelt att få insikter, affärsinformation och KPI:er från dina Business Central-data med Power BI och innehållspaketet för Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 26fe722a863ada2bcd017e2bc614b976a7119a25
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "806951"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivera affärsdata för Power BI
Att få insikter om dina [!INCLUDE[d365fin](includes/d365fin_md.md)]-data är enkelt med Power BI och [!INCLUDE[d365fin](includes/d365fin_md.md)]-innehållspaketen. Power BI hämtar dina data och skapar sedan en förinstallerad instrumentbräda och rapporter baserade på den data.  

Du måste ha ett giltigt konto med Dynamics 365 och med Power BI. Dessutom måste du hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) om du vill skapa dina egna Power BI-rapporter. Power BI innehållspaket kräver behörighet till de tabeller som data ska hämtas ifrån. Mer information om kraven beskrivs nedan.  

Microsoft har publicerat följande innehållspaket:

| App | Description |
| --- | --- |
| Microsoft Business Central | Ger en instrumentpanel med viktiga ekonomiska data över tid, till exempel intäkter och kostnader, rörelsemarginal och kontantcykeln.|
| Microsoft Business Central - CRM | Ger en instrumentpanel med viktig information om potentiella kunder och kontakter.  |
| Microsoft Business Central - Försäljning | Ger en instrumentpanel med viktig information om försäljning och lager. |

## <a name="using-the-dashboards"></a>Använda instrumentpanelerna
Varje innehållspaket ger rapporter som du kan söka i:

* Välj något visuellt på instrumentbrädan för att få upp en av de underliggande rapporterna.  
* Filtrera rapporten eller lägg till fält som du vill övervaka.  
* Sätt fast den här vyn på instrumentbrädan om du vill fortsätta spårningen.  
  Du kan uppdatera data manuellt och du kan ställa in ett schema för uppdatering. Mer information finns i [konfigurera schemalagd uppdatering](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Innehållspaketet är förkonfigurerat för att arbeta med data från demonstrationsföretaget som du får när du registrerar dig på förhandsgranskningen av [!INCLUDE[d365fin](includes/d365fin_md.md)]. När du installerar appar i Power BI och du ansluter till dina egna data, fungerar inte vissa rapporter eftersom de använder data som företaget inte har. I så fall kan du bara ta bort rapporten från instrumentpanelen.  

> [!NOTE]  
>   Du kan också skapa egna rapporter och instrumentpaneler i Power BI utifrån dina [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Mer information finns i [ansluta din affärsdata till Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="how-to-connect"></a>Så här ansluter du
1. Välj **Hämta Data** längst ned i den vänstra navigeringsrutan.  
![Navigera för att hämta data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

Du kan också komma igång från Dynamics 365 Business Edition. Från Rollcentret navigerar du till **Rapportval** i rollcenterdelen för Power BI. Välj antingen **Service** eller **Min organisation** i menyfliken. När något av ovanstående åtgärder är markerade förs du till antingen galleriet Organisation i Power BI eller till tjänstebiblioteket i Power BI, vilket även filtreras att bara visa innehållspaket relaterade till [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

2. I rutan **Tjänster**, markera **Hämta**. Då öppnas en sida med **AppSource** och **program för Power BI-program**.  
![Välj innehållspaket bland onlinetjänsterna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Markera **Program** i fliken **Program för Power BI-program** välj innehållspaket för **Microsoft Dynamics 365 Business Central** som du vill använda och välj sedan **Hämta nu**.  
![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Ange namnet på *ditt företag* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] när du uppmanas att göra så. Detta är inte visningsnamnet. Företagsnamnet finns på sidan ”Företag” i din [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-instans.  
![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. När anslutningen har genomförts kommer instrumentpanel, rapport och datauppsättning automatiskt att laddas till din Power BI-arbetsyta. När hämtningen är slutförd kommer panelerna att uppdateras med information från ditt [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-företag.
![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Vad nu?

- Försök med att [ställa en fråga i rutan Frågor och svar](https://docs.microsoft.com/en-us/power-bi/service-q-and-a-tips) högst upp i instrumentpanelen.
- [Ändra panelerna](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) på instrumentpanelen.  
- [Välj en panel](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) för att öppna den underliggande rapporten.  
- Din datauppsättning schemaläggs att uppdateras dagligen, men du kan ändra uppdateringsschemat eller uppdatera det på begäran med hjälp av **Uppdatera nu**.

## <a name="system-requirements"></a>Systemkrav
För att importera dina [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data i Power BI måste du ha behörighet till de webbtjänster som används för att hämta data. De webbtjänster som krävs för respektive innehållspaket är:

## <a name="role-center-reports"></a>Rollcenter-rapporter

**Microsoft Dynamics 365 Business Central – CRM**
- Försäljningsmöjligheter
- Excel-mallen för Visa företag
- Power BI Rapportetiketter

**Microsoft Dynamics 365 Business Central – Ekonomi**
- Power BIFinance
- Excel-mallen för Visa företag
- Power BI Rapportetiketter

**Microsoft Dynamics 365 Business Central – projekt**
- Projektlista
- Projektplaneringsrader
- Projektaktivitetsrader
- Power BI Rapportetiketter
- Excel-mallen för Visa företag

**Microsoft Dynamics 365 Business Central - försäljning**
- Instrumentbräda för försäljning
- Excel-mallen för Visa företag
- Power BI Rapportetiketter

## <a name="list-page-reports"></a>Rapporter för listsida

**Microsoft Dynamics 365 Business Central – kundlista**
- Artikelförsäljning efter kund
- Power BI inköpslista för artiklar
- Power BI försäljningslista för artiklar
- Instrumentbräda för försäljning
- Power BI kundlista
- ExcelTemplateViewCompany
- Power BI Rapportetiketter

**Microsoft Dynamics 365 Business Central - Lista för redovisningstransaktioner**
- Power BI redovisningsbelopplista
- Power BI budgeterat redovisningsbelopp
- ExcelTemplateViewCompany
- Power BI Rapportetiketter

**Microsoft Dynamics 365 Business Central - Artikellista**
- Artikelförsäljning efter kund
- Power BI inköpslista för artiklar
- Power BI försäljningslista för artiklar
- Instrumentbräda för försäljning
- ExcelTemplateViewCompany
- Power BI Rapportetiketter

**Microsoft Dynamics 365 Business Central – projektlista**
- Power BI projektlista
- ExcelTemplateViewCompany
- Power BI Rapportetiketter

**Microsoft Dynamics 365 Business Central – lista över inköpsfakturor**
- Power BI inköpslista
- ExcelTemplateViewCompany
- Power BI Rapportetiketter

**Microsoft Dynamics 365 Business Central – Försäljningsorderlista**
- Power BI försäljningslista
- ExcelTemplateViewCompany
- Power BI Rapportetiketter


**Microsoft Dynamics 365 Business Central - leverantörslista**
- Power BI inköpslista för artiklar
- Power BI försäljningslista för artiklar
- Power BI leverantörslista
- ExcelTemplateViewCompany
- Power BI Rapportetiketter

## <a name="web-services"></a>Webbtjänster
Ett enkelt sätt att hitta webbtjänsterna är att söka efter webbtjänster via [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Se till att rutan Publicera markeras i lista för de webbtjänster som anges ovan.

## <a name="troubleshooting"></a>Felsökning
Instrumentbrädan för Power BI förlitar sig på de publicerade webbtjänsterna som visas ovan, och kommer att innehålla data från demonstrationsföretaget eller ditt eget företag om du importerar data från den aktuella finanslösningen. Men om något går fel kommer denna sektion att ge en tillfällig lösning för de vanligaste problemen.

### <a name="incorrect-company-name"></a>Felaktigt företagsnamn  
Ett vanligt fel är att ange företagets visningsnamn i stället för namnet på företaget. Söka efter **Företag** för att hitta företagsnamnet. Använda fältet **Namn** när du anger företagets namn.

### <a name="incorrect-user-name-and-password"></a>Felaktigt användarnamn och lösenord  
Användarnamn och lösenord som används för att ansluta blir desamma som används för att ansluta till ditt Microsoft Office 365-konto.  

Innehållspaketen kräver också att du har ett Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto. När du har angett dina autentiseringsuppgifter upptäcker vi automatiskt eventuella Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innehavare som du har tillgång till. Om du inte har ett licensierat eller Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto eller en utvärderingsversion visas ett felmeddelande.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Nyckeln matchade inte några rader i tabellen
Om du anger ogiltiga företagsnamn i samband med anslutningsprocessen kan du få felmeddelandet ”Nyckeln matchar inga rader i tabellen”. Ange rätt företagsnamn och försök ansluta igen.

## <a name="see-also"></a>Se även
[Komma igång med Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI- Grundläggande begrepp](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[Affärsstöd](bi.md)  
[Komma igång](product-get-started.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] som en Power BI datakälla](across-how-use-financials-data-source-powerbi.md)  
[Med hjälp av [!INCLUDE[d365fin](includes/d365fin_md.md)] som en PowerApps-datakälla](across-how-use-financials-data-source-powerapps.md)  
[Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
