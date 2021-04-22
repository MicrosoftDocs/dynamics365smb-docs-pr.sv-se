---
title: Affärsstöd | Microsoft Docs
description: Fånga och analysera affärsdata, som t. ex. försäljningssiffror, inköp, driftskostnader, löner och budgetar, kan bli värdefull information, eller business intelligence, för beslutsfattare.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6a3d3e9aec61b3dab7673c7b99b482f80501a919
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786568"
---
# <a name="business-intelligence"></a>Affärsstöd
Företag skapar och hanterar oerhörda mängder data under sin dagliga verksamhet. Dessa data, som återspeglar till exempel organisationens försäljningssiffror, inköp, driftskostnader, löner och budgetar, kan bli värdefull information, eller business intelligence, för beslutsfattare. [!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett antal funktioner som hjälper dig att samla, analysera och dela med dig av dina företagsdata.

Funktionen för dimensioner spelar en viktig roll i affärsstöd. En dimension är data som du kan lägga till en transaktion som en sorts markör. Dessa data används för att gruppera transaktioner med liknande egenskaper, till exempel kunder, regioner, produkter och säljare, och enkelt hämta dessa grupper för analys. Bland annat kan du använda dimensioner när du definierar aktiviteter och när du skapar kontouppställningar för rapportering. Mer information finns i [Arbeta med](finance-dimensions.md).

> [!TIP]
> Som ett snabbt sätt att analysera transaktionsdata med dimensioner kan du filtrera summorna i kontoplanen och posterna på alla sidor för **Transaktioner** per dimension. Sök efter åtgärden **Ange dimensionsfilter**.  

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

| Till | Gå till |
| --- | --- |
|Visa faktiska belopp i jämförelse med budgeterade belopp för alla konton och för flera perioder.|[Analysera faktiska belopp kontra budgeterade belopp](bi-how-analyze-actual-versus-budget.md)|
|Skapa nya kontouppställningar för att ange finansiella rapporter för att rapportera eller för att visa som diagram.|[Förbereda ekonomiska rapporter, kontouppställningar och kategorier](bi-how-work-account-schedule.md)|
|Analysera den ekonomiska kapacitet, genom att ställa in KPIs baserat på kontouppställningar, som du sedan publicerar som webbtjänster. De publicerade kontouppställnings-KPI:erna kan visas på en webbplats eller importeras till Microsoft Excel med hjälp av OData webbtjänster.|[Skapa och publicera KPI-webbtjänster som baseras på kontouppställningar](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md)|
|Skapa aktiviteter för att analysera data med dimensioner.|[Analysera data efter dimensioner](bi-how-analyze-data-dimension.md)|
|skapa nya analysrapporter för försäljning, inköp och lager, och skapa analysmallar.|[Skapa analysrapporter](bi-how-create-analysis-views-reports.md)|
|Aktivera global ekonomisk rapportering som står till internationella organisationer i redovisning med standarden eXtensible Business Reporting Language.|[Skapa rapporter med XBRL](bi-create-reports-with-xbrl.md)|
|Ändra åtkomstmetoden för databaser gällande rapporter, sidor av typen API och frågor för att minska belastningen och förbättra prestandan.|[Hantera åtkomstmetod för databas](admin-data-access-intent.md)|

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)    
[Använda Business Central som en Power BI-datakälla](across-how-use-financials-data-source-powerbi.md)  
[Stänga räkenskapsperioder](year-close-years-periods.md)  
[Importera data från andra finanssystem](across-import-data-configuration-packages.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]