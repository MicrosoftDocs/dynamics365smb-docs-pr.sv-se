---
title: Power BI-integreringskomponent och arkitekturöversikt för Business Central| Microsoft Docs
description: Lär dig mer om olika aspekter av Power BI-integreringen med Business Central.
author: jswymer
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 63aa8e6b23c2977e8e44c6f346f33c1c33fe3c2a
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533220"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-"></a><a name="power-bi-integration-component-and-architecture-overview-for-"></a><a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a>Power BI-integreringskomponent och arkitekturöversikt för [!INCLUDE[prod_short](includes/prod_short.md)]

I denna artikel lär du dig mer om olika aspekter av Power BI-integreringen med [!INCLUDE[prod_short](includes/prod_short.md)] i syfte att hjälpa dig förstå dess implementering och användning.

## <a name="components"></a><a name="components"></a><a name="components"></a>Komponenter

Följande tabell beskriver de större komponenter som är involverade i Power BI-integreringen.

|Komponent|Beskrivning|
|---------|-----------|
|Power BI|En molnbaserad tjänst för att lagra och hantera rapporter.|
|Power BI Desktop|Ett auktoriseringsverktyg för att skapa rapporter och instrumentpaneler som dessutom gör det möjligt för dig att köra rapporter. Det finns tillgängligt som kostnadsfri nedladdning från Microsoft Store oh installeras lokalt.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Online- eller lokal lösning med anslutningsprogram synliga för Power BI och möjlighet för att bädda in en Power BI-del.|

## <a name="whats-available-from-the-start"></a><a name="whats-available-from-the-start"></a><a name="whats-available-from-the-start"></a>Vad finns tillgängligt från början?

Följande tabell beskriver tillgängliga funktioner.

|Funktion|[!INCLUDE[prod_short](includes/prod_short.md)]-support online eller lokalt|
|-------|---------------------|
|Power BI-anslutningsprogram|Båda. Olika anslutningsprogram för online och lokalt. Samma anslutningsprogram används för Power BI Desktop och Power BI Service |
|Inbäddad upplevelse för att visa en specifik rapport inuti en FactBox i [!INCLUDE[prod_short](includes/prod_short.md)]|Båda. Kräver konfigurering för att visa rapporter för lokala versioner.|
|Hantering av Power BI-rapporter från [!INCLUDE[prod_short](includes/prod_short.md)]|Online|
|Power BI-standardrapporter om rollcentran som distribuerats till Power BI|Online|
|Power BI-appar i Microsoft AppSource|Online|

## <a name="architecture"></a><a name="architecture"></a><a name="architecture"></a>Arkitektur

[!INCLUDE[prod_short](includes/prod_short.md)] integreras med Power BI via ett anslutningsprogram som använder OData. Datakällan för Power BI-rapporter anges som API-sidor och OData-webbtjänster.

:::image type="content" source="./media/power-bi-architecture.png" alt-text="Alternativtext för bild" lightbox="./media/power-bi-architecture.png":::

Från och med februari 2022 hämtas Power BI-rapporter för [!INCLUDE[prod_short](includes/prod_short.md)] online från en sekundär, skrivskyddad databaskopia. Databaskopian är en del av möjligheten till [läsningsskalning](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) i [!INCLUDE[prod_short](includes/prod_short.md)] online. Den här konfigurationen frigör huvuddatabasen för transaktioner, vilket förbättrar systemets prestanda. Anslutning till den skrivskyddade databaskopian är en viktig del av Business Central Online-anslutningsprogrammet och kräver ingen extra installation från din sida. Alla nya rapporter kopplas till den skrivskyddade databaskopian som standard. I gamla rapporter används fortfarande huvuddatabasen. Mer information finns i [Plan för Business Central 2021 utgivningscykel 2](/dynamics365-release-plan/2021wave2/smb/dynamics365-business-central/use-secondary-read-only-database-power-bi-reporting).

## <a name="general-flow"></a><a name="general-flow"></a><a name="general-flow"></a>Allmänt flöde

Följande diagram illustrerar det grundläggande arbetsflödet för användare när [!INCLUDE[prod_short](includes/prod_short.md)] ansluts till Power BI.

![Power BI-arbetsflöde för integrering med Business Central.](./media/power-bi-flow.png)

1. Användare registrerar sig för ett Power BI-konto.
2. Användare ansluter till Power BI från [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] bekräftar licensen.
4. [!INCLUDE[prod_short](includes/prod_short.md)] distribuerar standardrapporter till Power BI-tjänsten. Detta steg sker enbart för [!INCLUDE[prod_short](includes/prod_short.md)] online.
5. [!INCLUDE[prod_short](includes/prod_short.md)] gör rapporter i Power BI tillgängliga för val i [!INCLUDE[prod_short](includes/prod_short.md)]. Standardrapporter visas automatiskt i Power BI-delar.
6. Användaren skapar en rapport i Power BI Desktop.
7. Användaren publicerar rapporten i Power BI-tjänsten. Rapporterna blir därefter tillgängliga för urval i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Business Central och Power BI](admin-powerbi.md)  
[Power BI för konsumenter](/power-bi/consumer/end-user-consumer)  
[Power BI-tjänstens "nya utseende"](/power-bi/service-new-look)  
[Snabbstart: Anslut till data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Dokumentation om Power BI](/power-bi/)  
[Affärsstöd](bi.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Importera affärsdata från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakälla](across-how-use-financials-data-source-powerbi.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakälla](across-how-use-financials-data-source-powerapps.md)  
[Använda [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
