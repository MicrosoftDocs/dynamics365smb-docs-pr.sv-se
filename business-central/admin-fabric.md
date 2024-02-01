---
title: Introduktion till Microsoft Fabric och Business Central
description: 'Få en användningsöversikt för Microsoft Fabric i syfte att få insikter, business intelligence och KPI:er från dina Business Central-data.'
author: kennienp
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 10/10/2023
ms.author: kepontop
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="introduction-to-microsoft-fabric-and-business-central"></a>Introduktion till Microsoft Fabric och Business Central

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] är en heltäckande analyslösning med fullständiga servicefunktioner, inklusive dataförflyttning, datasjöar, datateknik, dataintegrering, datavetenskap, realtidsanalys och business intelligence&mdash;allt uppbackat av en delad plattform som ger robust datasäkerhet, styrning och efterlevnad. Ditt företag behöver inte längre sy ihop individuella analystjänster från olika leverantörer. Använd istället en strömlinjeformad lösning som är enkel att ansluta, registrera och använda.

> [!NOTE]
> [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] finns för tillfället som förhandsversion. För mer information om Microsoft Fabric viktig information, se [aka.ms/FabricRoadmap](https://aka.ms/FabricRoadmap)
> 
> Den regelbundna publiceringen av denna färdplan hjälper dig att hålla dig informerad om hur [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] kommer att tillgodose dina behov.

## <a name="where-does--fit-into-includeprod_short-analytics"></a>Var passar [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] in i [!INCLUDE[prod_short](includes/prod_short.md)] analys

[!INCLUDE[prod_short](includes/prod_short.md)] levereras med många färdiga rapporter och dataanalysfunktioner som ekonomisk rapportering, öppen i Excel och analysläge på listor och frågor. Utöver detta är det enkelt att definiera Power BI rapporter som läser data från standard- och anpassade API:er, definierar Power BI måttstyrkort och bäddar in alla dessa direkt i klienten [!INCLUDE[prod_short](includes/prod_short.md)]. Men för kunder med mer avancerade datavetenskaps- eller Business Intelligence-scenarier som kräver mer omfattande datateknik eller dataintegrering kan [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] vara ett bra alternativ. 

## <a name="onelake"></a>OneLake

En viktig del av [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] erbjudandet är OneLake. OneLake är en enda, enhetlig, logisk datasjö för hela organisationen. Du kan tänka på OneLake som OneDrive för data. Den ger dig datasjö som en tjänst utan att behöva skapa den själv. OneLake levereras automatiskt med varje [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] klientorganisation utan infrastruktur att hantera. Alla data som hamnar i OneLake deltar automatiskt i förkonfigurerad datahantering, inklusive datalinje, dataskydd, certifiering och katalogintegration. Den bryter ner datasilor genom att göra det möjligt för olika delar av organisationen att arbeta oberoende av varandra samtidigt som de bidrar till samma datasjö.

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] objekt lagrar dina data i OneLake i ett öppet filformat. För strukturerade tabelldata är det här formatet *delta parquet*. Med delta parquet-formatet kan varje analysmotor i [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] komma åt data från andra analysmotorer. På så sätt möjliggör det flexibilitet för datautövare att använda de verktyg du väljer.

> [!NOTE]
> Vi förväntar oss att med en av våra framtida utgåvor [!INCLUDE[prod_short](includes/prod_short.md)] kommer data också att göras tillgängliga i OneLake för de kunder som använder både [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] och [!INCLUDE[prod_short](includes/prod_short.md)] och har unika krav inom de områden som [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] stöder. Tidslinjen beror på tidslinjen för allmän tillgänglighet av [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] och dess komponenter som krävs för att möjliggöra den här upplevelsen. Vi kommer att uppdatera den här artikeln med en mer exakt tidslinje när vi vet mer.

## <a name="see-also"></a>Se även
[Använda Power BI med Business Central](admin-powerbi.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
