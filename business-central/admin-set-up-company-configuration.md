---
title: Ställa in företagskonfiguration | Microsoft Docs
description: Implementeringsprocessen börjar med det Business Central-lösningen kräver. Samla sedan ihop all denna information i konfigurationspaket.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3eefa0fcb40b4e925ca653f223f2d97ed10f370e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777247"
---
# <a name="set-up-company-configuration"></a>Ställa in företagskonfiguration
Implementeringsprocessen börjar med Microsoft-partnern. Partnern är ansvarig för att tänka igenom konfigurationdetaljerna och för att skapa ett paket som en kund enkelt kan använda. Innan du skapar ett nytt företag bör du planera hur det ska konfigureras. Du måste beakta grundläggande inställningsdata och vilka slags data din [!INCLUDE[prod_short](includes/prod_short.md)]-lösning kräver. Samla sedan ihop all denna information i konfigurationspaket.

RapidStart Services ger dig också de verktyg som du använder för att migrera bakåtkompatibla data, t. ex. kunder och leverantörer.  

Vi rekommenderar att du skapar konfigurationspaket där de flesta inställningstabellerna redan är ifyllda så att kunder bara behöver ändra några få inställningar när paketet används. När du till exempel skapar ett nytt företag kommer tabellerna **Nr-serier** och **Nr-serierad** att fyllas i med en uppsättning nummerserier och startnummer. Motsvarande **Nr-serie** i inställningstabellerna fylls också i automatiskt. Du måste inte att göra arbetet med att specificera nummerserier och andra grundläggande inställningsdata. Du kan också ändra alla standarddata manuellt för RapidStart Services genom att använda konfigurationsförslaget.  

Konfigurationspaketen skapas utifrån ett förkonfigurerat företag. När du har skapat ett företag som uppfyller dina behov kan du skapa ett konfigurationspaket som innehåller viktig information från det här företaget. Då kan du använda den när du skapar ett nytt företag som ska konfigureras på samma sätt.  

Om du vill underlätta importen av huvuddata, som kund- och leverantörsinformation, kan du använda konfigurationsmallar. Konfigurationsmallar innehåller en uppsättning standardinställningar som automatiskt tilldelas de transaktioner som importeras till [!INCLUDE[prod_short](includes/prod_short.md)].

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

|**För att**|**Gå till**|  
|------------|-------------|  
|Planera en företagskonfiguration genom att fylla i konfigurationskalkylarket.|[Så här hanterar du företagskonfigurationen i ett kalkylark](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Skapa ett konfigurationspaket, anpassa ett paket, tilldela tabeller till ett paket, granska eller ändra kunddata, skapa det nya företaget och flytta testdata till produktionsmiljön.|[Förbered ett konfigurationspaket](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a>Se även  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]