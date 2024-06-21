---
title: 'Spåra dina affärs-KPI: er med Power BI-mått'
description: 'Få en användningsöversikt för Power BI i syfte att få business intelligence och KPI:er från dina Business Central-data.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.date: 04/24/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="track-your-business-kpis-with-power-bi-metrics"></a>Spåra dina affärs-KPI: er med Power BI-mått

Om du använder Power BI i [!INCLUDE[prod_short](includes/prod_short.md)] data, är det enkelt att spåra KPI:er eller mått som är viktiga för dig.

Med mått i Power BI kan du granska dina egna mått och följa upp dem i ett enda fönster. Denna funktion förbättrar datakulturen genom att främja ansvar, justering och synlighet för grupper och initiativ inom organisationer.

Använd den här fyrstegsproceduren för att ange Power BI mått:

1. Skapa ett styrkort i Power BI. Läs mer på [Skapa styrkort i Power BI](/power-bi/create-reports/service-goals-create).  
2. Lägg till mått du vill följa upp genom att ansluta till din Power BI-rapport om telemetri. Läs mer på [Skapa anslutna mått](/power-bi/create-reports/service-goals-create-connected).  
3. Lägg till aviseringar om det behövs för att definiera statusregler för dina mätvärden. Läs mer på [Skapa automatiska statusregler för mått](/power-bi/create-reports/service-metrics-status-rules).  

    Det här steget automatiserar statusuppdateringar baserat på regler som styr det måttet. Regler utlöser ändringar baserat på värde, procent av målvärde som uppfylls, datum villkor eller en kombination av de tre, vilket gör reglerna mångsidiga. För sammankopplade mått uppdateras dessa status regler varje gång data i styrkortet uppdateras.
4. Följer du mått för att få aviseringar i Teams eller via e-post. Läs mer på [Följa följa dina mått](/power-bi/create-reports/service-metrics-follow).  

Läs mer på Power BI mått finns i [Komma igång med mått i Power BI](/power-bi/create-reports/service-goals-introduction).

> [!NOTE]
> Från och med Business Central utgivningscykel 2 för 2023 är det möjligt att bädda in styrkort från Power BI-mått i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Se även

[Använda nyckeltal (KPI:er) för att uppfylla dina verksamhetsmål](analytics-about-kpis.md)  
[Introduktion till Business Central och Power BI](admin-powerbi.md)  
[Arbeta med Power BI-rapporter](across-working-with-powerbi.md)  
[Översikt över analyser](reports-bi-reporting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
