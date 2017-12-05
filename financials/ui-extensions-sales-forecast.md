---
title: "Med hjälp av tillägget försäljning och lagerprognos för att hantera lager | Microsoft Docs"
description: "Det här tillägget låter dig förutse försäljning, få en tydlig översikt över förväntat slut i lager och du kan till och med skapa återanskaffningsförfrågningar till leverantörer."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: b4f49d7d103bebeb6512d825a68c5941c8835214
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---
# <a name="sales-and-inventory-forecast-for-dynamics-365-business-edition"></a>Prognos för försäljning och lager för Dynamics 365 Business edition 
Lagerhantering är en kompromiss mellan kundservice och hantering av din kostnad. Å ena sidan kräver ett lågt lager mindre rörelsekapital, men å andra sidan leder eventuellt slut i lager till missade försäljningar. Tilläggen för Försäljning och Lagerprognos förutsäger potentiella försäljningar med hjälp av historiska data och ger en tydlig översikt av förväntade slut i lager. Baserat på prognosen hjälper tilläggen till att skapa påfyllningförfrågningar till dina leverantörer, vilket sparar tid.  

## <a name="setting-up-forecasting"></a>Konfigurera prognoser
I [!INCLUDE[d365fin](includes/d365fin_md.md)], har anslutningen till [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) redan ställts in åt dig. Men du kan konfigurera prognosen till att använda en annan typ av period att rapportera efter, t.ex ändra från prognos per månad till prognos per kvartal. Du kan även välja antal perioder att beräkna prognosen efter, beroende på hur många detaljnivåer du vill att prognosen ska vara. Vi föreslår att du gör prognoser per månad och med en 12 månaders horisont för prognosen.  

## <a name="using-the-forecasts"></a>Att använda prognoserna
Detta tillägg använder funktionerna i Cortana Intelligence för att förutsäga framtida försäljningar som baseras på din försäljninghistorik för att undvika lagerbrist. När du till exempel väljer en artikel i fönstret **Artiklar** visar diagrammet i fönstret **Prognostiserad artikel** de beräknade försäljningarna av artikeln i den kommande perioden. På så sätt kan du se om du förmodligen kommer att få slut på lagret av artikeln snart.  

Du kan också använda tillägget för att föreslå när du ska fylla på lagret. Om du till exempel skapar en inköpsorder för Fabrikam eftersom du vill köpa deras nya skrivbordstol, kommer tillägget Prognos för försäljning och lager att föreslå att du fyller i distributionslagret även på den LONDON snurrstol som du brukar köpa från leverantören. Detta beror på att tilläggprognoserna att du kommer att få slut i lager av LONDON snurrstol de kommande två månaderna, vilket innebär att det kan hända att du vill beställa fler stolar redan nu.  

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  

