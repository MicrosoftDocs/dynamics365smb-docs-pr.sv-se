---
title: Power BI-integreringskomponent och arkitekturöversikt för Business Central| Microsoft Docs
description: Använda insikter, business intelligence och KPI:er från dina Business Central-data är enkelt med Business Central-apparna för Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 23a0c72775dbddc89a81105de3b2ed79d1f09432
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753776"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a>Power BI-integreringskomponent och arkitekturöversikt för [!INCLUDE[prod_short](includes/prod_short.md)]

I denna artikel lär du dig mer om olika aspekter av Power BI-integreringen med [!INCLUDE[prod_short](includes/prod_short.md)] i syfte att hjälpa dig förstå dess implementering och användning.

## <a name="components"></a>Komponenter

Följande tabell beskriver de större komponenter som är involverade i Power BI-integreringen.

|Komponent|Beskrivning|
|---------|-----------|
|Power BI|En molnbaserad tjänst för att lagra och hantera rapporter.|
|Power BI Desktop|Ett auktoriseringsverktyg för att skapa rapporter och instrumentpaneler som dessutom gör det möjligt för dig att köra rapporter. Det finns tillgängligt som kostnadsfri nedladdning från Microsoft Store oh installeras lokalt.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Online- eller lokal lösning med anslutningsprogram synliga för Power BI och möjlighet för att bädda in en Power BI-del.|

## <a name="whats-available-from-the-start"></a>Vad finns tillgängligt från början?

Följande tabell beskriver tillgängliga funktioner.

|Funktion|[!INCLUDE[prod_short](includes/prod_short.md)]-support online eller lokalt|
|-------|---------------------|
|Power BI-anslutningsprogram|Båda. Olika anslutningsprogram för online och lokalt. Samma anslutningsprogram används för Power BI Desktop och Power BI Service |
|Inbäddad upplevelse för att visa en specifik rapport inuti en FactBox i [!INCLUDE[prod_short](includes/prod_short.md)]|Båda. Kräver konfigurering för att visa rapporter för lokala versioner.|
|Hantering av Power BI-rapporter från [!INCLUDE[prod_short](includes/prod_short.md)]|Online|
|Power BI-standardrapporter om rollcentran som distribuerats till Power BI|Online|
|Power BI-appar i Microsoft AppSource|Online.|

## <a name="architecture"></a>Arkitektur

[!INCLUDE[prod_short](includes/prod_short.md)] integreras med Power BI via ett anslutningsprogram som använder OData. Datakällan för Power BI-rapporter anges som OData-webbtjänster.

![Power BI-arkitektur för integrering med Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a>Allmänt flöde

Följande diagram illustrerar det grundläggande arbetsflödet för användare när [!INCLUDE[prod_short](includes/prod_short.md)] ansluts till Power BI.

![Power BI-arbetsflöde för integrering med Business Central](./media/power-bi-flow.png)

1. Användare registrerar sig för ett Power BI-konto.
2. Användare ansluter till Power BI från [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] bekräftar licensen.
4. [!INCLUDE[prod_short](includes/prod_short.md)] distribuerar standardrapporter till Power BI-tjänsten. Detta steg sker enbart för [!INCLUDE[prod_short](includes/prod_short.md)] online.
5. [!INCLUDE[prod_short](includes/prod_short.md)] gör rapporter i Power BI tillgängliga för val i [!INCLUDE[prod_short](includes/prod_short.md)]. Standardrapporter visas automatiskt i Power BI-delar.
6. Användaren skapar en rapport i Power BI Desktop.
7. Användaren publicerar rapporten i Power BI-tjänsten. Rapporterna blir därefter tillgängliga för urval i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Business Central och Power BI](admin-powerbi.md)  
[Power BI för konsumenter](/power-bi/consumer/end-user-consumer)  
[Power BI-tjänstens "nya utseende"](/power-bi/service-new-look)  
[Snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Dokumentation om Power BI](/power-bi/)  
[Affärsstöd](bi.md)  
[Komma igång](product-get-started.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI datakälla](across-how-use-financials-data-source-powerbi.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps datakälla](across-how-use-financials-data-source-powerapps.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
