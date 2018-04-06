---
title: Ansluta Power BI till Finance and Operations, Business edition | Microsoft Docs
description: "Att få insyn, affärslogik och KPI:er från dina Finance and Operations, Business edition-data är enkelt med Power BI och innehållspaketen för Finance and Operations, Business edition."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 02/05/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: aff8d95b13f795fa12d3146e5613712fb3baf9b4
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-finance-and-operations-business-edition-content-packs"></a>Ansluta Power BI till innehållspaket för Finance and Operations, Business edition
Att få insikter om dina Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data är enkelt med Power BI och Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innehållspaketen. Power BI hämtar dina data och skapar sedan en förinstallerad instrumentbräda och rapporter baserade på den data.

> [!NOTE]  
>  Du måste ha ett giltigt konto med Dynamics 365 och med Power BI. Dessutom måste du hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  
>  Innehållspaket för Power BI kräver behörighet till de tabeller som data ska hämtas ifrån. Mer information om kraven beskrivs nedan.  

## <a name="how-to-connect"></a>Så här ansluter du
1. Välj **Hämta Data** längst ned i den vänstra navigeringsrutan.  
![Navigera för att hämta data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)
2. I rutan **Tjänster**, markera **Hämta**. Då öppnas ett fönster med **AppSource** och **Program för Power BI-program**.  
![Välj innehållspaket bland onlinetjänsterna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Markera **Program** i fliken **Program för Power BI-program**, välj det innehåll för **Microsoft Dynamics 365 for Finance and Operations** som du vill använda och välj sedan **Hämta nu**.  
![Välj Dynamics 365 for Finance and Operations, Business edition och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Ange namnet på *ditt företag* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] när du uppmanas att göra så. Detta är inte visningsnamnet.  
![Välj Dynamics 365 for Finance and Operations, Business edition och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. När anslutningen har genomförts kommer instrumentpanel, rapport och datauppsättning automatiskt att laddas till din Power BI-arbetsyta. När laddningen är slutförd kommer panelerna att uppdateras med information från ditt konto.
![Välj Dynamics 365 for Finance and Operations, Business edition och välj Hämta nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Vad nu?

- Försök med att [ställa en fråga i rutan Frågor och svar](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) högst upp i instrumentpanelen.  
- [Ändra panelerna](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) på instrumentpanelen.  
- [Välj en panel](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) för att öppna den underliggande rapporten.  
- Din datauppsättning schemaläggs att uppdateras dagligen, men du kan ändra uppdateringsschemat eller uppdatera det på begäran med hjälp av **Uppdatera nu**.

## <a name="system-requirements"></a>Systemkrav
För att importera dina [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data i Power BI måste du ha behörighet till de webbtjänster som används för att hämta data. De webbtjänster som krävs för respektive innehållspaket är:

**Microsoft Dynamics 365 for Finance and Operations, Business edition – CRM**
- SalesOpportunities
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Sales**
- ItemSalesbyCustomer
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Finance**
- Power BIFinance
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Jobs**
- Projektlista
- Projektplaneringsrader
- Projektaktivitetsrader

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Customers List**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- SalesDashboard
- Power BI kundlista
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Items List**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- Artiklar
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Vendors List**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- Artiklar
- SalesDashboard
- Power BI kundlista
- ItemSalesbyCustomer
- Power BI leverantörslista
- ExcelTemplateViewCompany

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
Om du anger ogiltiga företagsnamn i samband med anslutningsprocessen kan du få felmeddelandet ”nyckeln matchar inte har några rader i tabellen”. Ange rätt företagsnamn och försök ansluta igen.

## <a name="see-also"></a>Se även
[Kom igång med Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Grundläggande begrepp](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  
[Ställa in rapportering för [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)  

