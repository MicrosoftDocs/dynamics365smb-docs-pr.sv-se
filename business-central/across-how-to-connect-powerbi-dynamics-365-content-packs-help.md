---
title: "Så här ansluter du Power BI till Business Central | Microsoft Docs"
description: "Det är enkelt att få insikter, affärsinformation och KPI:er från dina Business Central-data med Power BI och innehållspaketet för Business Central."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 48c57e03f4679ea05792304fe13bdf896be2f1e3
ms.contentlocale: sv-se
ms.lasthandoff: 11/22/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a>Ansluta Power BI till innehållspaket för Dynamics 365 Business Central
Att få insikter om dina Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data är enkelt med Power BI och Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innehållspaketen. Power BI hämtar dina data och skapar sedan en förinstallerad instrumentbräda och rapporter baserade på den data.

Du måste ha ett giltigt konto med Dynamics 365 och med Power BI. Du måste även hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) om du vill skapa egna Power BI-rapporter. Innehållspaket för Power BI kräver behörighet till de tabeller som data ska hämtas ifrån. Mer information om kraven beskrivs nedan.  

## <a name="how-to-connect"></a>Så här ansluter du
1. Välj **Hämta Data** längst ned i den vänstra navigeringsrutan.  
![Navigera för att hämta data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

Du kan också starta från Dynamics 365 Business Edition. Från Rollcentret navigerar du till **Rapportval** i rollcenterdelen för Power BI. Välj antingen **Service** eller **Min organisation** i menyfliken. När något av ovanstående åtgärder är markerade förs du till antingen galleriet Organisation i Power BI eller till tjänstebiblioteket i Power BI, vilket även filtreras att bara visa innehållspaket relaterade till [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

2. I rutan **Tjänster**, markera **Hämta**. Då öppnas en sida med **AppSource** och **Program för Power BI-program**.  
![Välj innehållspaket bland onlinetjänsterna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Markera **Program** i fliken **Program för Power BI-program**, välj det innehållspaket för **Microsoft Dynamics 365 Business Central** som du vill använda och välj sedan **Hämta nu**.  
![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Ange namnet på *ditt företag* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] när du uppmanas att göra så. Detta är inte visningsnamnet. Företagsnamnet finns på sidan ”Företag” i din [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-instans. 
![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. När anslutningen har genomförts kommer instrumentpanel, rapport och datauppsättning automatiskt att laddas till din Power BI-arbetsyta. När hämtningen är slutförd kommer panelerna att uppdateras med information från ditt [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-företag.
![Välj Dynamics 365 Business Central och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Vad nu?

- Försök med att [ställa en fråga i rutan Frågor och svar](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) högst upp i instrumentpanelen.
- [Ändra panelerna](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) på instrumentpanelen.  
- [Välj en panel](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) för att öppna den underliggande rapporten.  
- Din datauppsättning schemaläggs att uppdateras dagligen, men du kan ändra uppdateringsschemat eller uppdatera det på begäran med hjälp av **Uppdatera nu**.

## <a name="system-requirements"></a>Systemkrav
För att importera dina [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data i Power BI måste du ha behörighet till de webbtjänster som används för att hämta data. De webbtjänster som krävs för respektive innehållspaket är:

## <a name="role-center-reports"></a>Rollcenter-rapporter

**Microsoft Dynamics 365 Business Central – CRM**
- Försäljningsmöjligheter
- Excel-mallen för Visa företag
- Rapportetiketter för Power BI

**Microsoft Dynamics 365 Business Central – Finance**
- Power BIFinance
- Excel-mallen för Visa företag
- Rapportetiketter för Power BI

**Microsoft Dynamics 365 Business Central – Jobs**
- Projektlista
- Projektplaneringsrader
- Projektaktivitetsrader
- Rapportetiketter för Power BI
- Excel-mallen för Visa företag

**Microsoft Dynamics 365 Business Central - Sales**
- Instrumentbräda för försäljning
- Excel-mallen för Visa företag
- Rapportetiketter för Power BI

## <a name="list-page-reports"></a>Rapporter för listsida 

**Microsoft Dynamics 365 Business Central – Customers List**
- Artikelförsäljning efter kund
- Power BI artikelinköpslista
- Power BI artikelförsäljningslista
- Instrumentbräda för försäljning
- Power BI kundlista
- ExcelTemplateViewCompany
- Rapportetiketter för Power BI 

**Microsoft Dynamics 365 Business Central - General Ledger Entries List**
- Power BI redovisningsbelopplista
- Power BI budgeterat redovisningsbelopp
- ExcelTemplateViewCompany
- Rapportetiketter för Power BI

**Microsoft Dynamics 365 Business Central – Items List**
- Artikelförsäljning efter kund
- Power BI artikelinköpslista
- Power BI artikelförsäljningslista
- Instrumentbräda för försäljning
- ExcelTemplateViewCompany
- Rapportetiketter för Power BI

**Microsoft Dynamics 365 Business Central – Jobs List**
- Power BI projektlista
- ExcelTemplateViewCompany
- Rapportetiketter för Power BI

**Microsoft Dynamics 365 Business Central – Purchase Invoices List**
- Power BI inköpslista
- ExcelTemplateViewCompany
- Rapportetiketter för Power BI

**Microsoft Dynamics 365 Business Central – Sales Orders List**
- Power BI försäljningslista
- ExcelTemplateViewCompany
- Rapportetiketter för Power BI


**Microsoft Dynamics 365 Business Central – Vendors List**
- Power BI artikelinköpslista
- Power BI artikelförsäljningslista
- Power BI leverantörslista
- ExcelTemplateViewCompany
- Rapportetiketter för Power BI

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
[Kom igång med Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Grundläggande koncept](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[Affärsstöd](bi.md)  
[Komma igång](product-get-started.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  
[Ställa in rapportering för [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)  

