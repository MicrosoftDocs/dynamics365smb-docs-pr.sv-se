---
title: Fördelningsstatus och reparationsstatus | Microsoft Docs
description: Lär dig mer om sambandet mellan reparationsstatus för serviceartiklar och fördelningsstatus för fördelningsposterna för dessa.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resources, allocation, status, repairs
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 9cf3349d654a4e007079075c64e9e56654619810
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772410"
---
# <a name="allocation-status-and-repair-status-of-service-items"></a>Fördelningsstatus och reparationsstatus för serviceartiklar
Det finns ett visst samband mellan serviceartiklarnas reparationsstatus och fördelningsstatus för fördelningsposterna till serviceartiklarna i modulen Service. Fördelningsstatusen ändras när du ändrar serviceartikelns reparationsstatus till **Avslutad** eller **Delvis servad** och när du omvandlar en serviceoffert till en serviceorder. En serviceartikels reparationsstatus ändras när du avbryter fördelningen av serviceartiklar eller flyttar serviceartikeln till en annan resurs. Du kan visa serviceartiklarnas reparationsstatus på sidan **Serviceuppgifter** och uppdatera reparationsstatus i fältet **Reparationsstatuskod** på sidan **Serviceartikeldokument**. Du kan visa fördelningsstatus på sidan **Status** på sidan **Resursfördelningar**.  
  
## <a name="changing-repair-status"></a>Ändra reparationsstatus  
När du ändrar en serviceartikels reparationsstatus på en serviceartikelrad, görs en sökning efter motsvarande fördelningspost för serviceartikeln som har statusen **Aktiv**. Om en sådan fördelningspost hittas uppdateras dess status på något av följande sätt:  
  
* Om du ändrar reparationsstatus till **Avslutad** ändras fördelningsstatus från **Aktiv** till **Avslutad**.  
* Om du ändrar reparationsstatus till **Delvis servad** (viss service har avslutats) eller **Hänvisad** (ingen service har utförts) ändras fördelningsstatus i programmet från **Aktiv** till **Omfördelning nödvändig**.  
* När en fördelningstransaktion för en serviceorder skapas, vilket innebär att ingen resurs har fördelats, anges värdet **Ej aktiv** för fältet **Status** på sidan till **Resursfördelning**.  
* Fördelningstransaktionens status blir **Avbruten** när du omfördelar den serviceartikel som nämns i fördelningstransaktionen för serviceordern, vilket innebär att den fördelade resursen eller resursgruppen inte har använts för serviceuppgiften.  
  
Fördelningsstatusen visar därmed när serviceprocessen är avslutad eller när en annan resurs krävs för att avsluta service av serviceartikeln.  
  
## <a name="converting-service-quotes-to-service-orders"></a>Omvandla serviceofferter till serviceorder  
När du omvandlar en serviceoffert till en serviceorder uppdateras serviceordern, serviceartiklarna i ordern och deras fördelningsposter så här:  
  
* Serviceartiklarnas reparationsstatus ändras till **Initial**.  
* Tjänsteorderstatus ändras till **Förestående**.  
* En sökning görs efter fördelningstransaktioner för alla serviceartiklar i serviceordern som har statusen **Aktiv**. Om sådana fördelningsposter hittas ändras deras fördelningsstatus från **Aktiv** till **Omfördelning nödvändig**.  
  
## <a name="canceling-allocations"></a>Rätta fördelningar  
När du avbryter fördelningen av en serviceartikel uppdaterar [!INCLUDE[prod_short](includes/prod_short.md)] fördelningsstatusen för motsvarande fördelningspost från **Aktiv** till **Omfördelning nödvändig**.

Reparationsstatus uppdateras för serviceartikeln i fördelningsposten så här:  
  
* Om fördelningsstatus är **Initial** ändras reparationsstatus till **Hänvisad** (ingen service har inletts).  
* Om reparationsstatus är **Pågående** ändras reparationsstatus till **Delvis servad** (viss service har utförts).  
  
## <a name="reallocating-an-active-allocation-entry"></a>Omfördela en fördelningspost som är aktiv  
När du omfördelar en serviceartikel i en fördelningspost som är **Aktiv** uppdateras fördelningsposten så här:  
  
* Om servicen startade när fördelningen var **Aktiv** (det vill säga om serviceartikelns reparationsstatus ändrats till **Pågående**), ändras fördelningsstatus från **Aktiv** till **Avslutad**.  
* Om servicen inte påbörjades när fördelningen var **Aktiv**, ändras fördelningsstatus från **Aktiv** till **Inställt**.  
  
Reparationsstatus för serviceartikeln i fördelningsposten uppdateras på samma sätt som om du hade ställt in fördelningen:  
  
* Om fördelningsstatus är **Initial** ändras reparationsstatus till **Hänvisad** (ingen service har inletts).  
* Om reparationsstatus är **Pågående** ändras reparationsstatus till **Delvis servad** (viss service har utförts).  
  
En ny fördelningspost skapas som innehåller den nya resursen med statusen **Aktiv**.  
  
## <a name="reallocating-a-service-item"></a>Omfördela en serviceartikel  
När du omfördelar en serviceartikel i en fördelningspost med statusen **Omfördelning nödvändig** uppdateras fördelningsposten så här:  
  
* Om servicen startade när fördelningen var **Aktiv**, dvs. om serviceartikelns reparationsstatus ändrats till **Pågående**, ändras fördelningsstatus från **Omfördelning nödvändig** till **Avslutad**.  
* Om servicen inte påbörjades när fördelningen var **Aktiv**, ändras fördelningsstatus från **Omfördelning nödvändig** till **Inställt**.  
  
En ny fördelningspost skapas som innehåller den nya resursen med statusen **Aktiv**.  
  
## <a name="see-also"></a>Se även  
[Så här skapar du resursfördelningar](service-how-setup-resource-allocation.md)  
[Så här tilldelar du resurser](service-how-to-allocate-resources.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]