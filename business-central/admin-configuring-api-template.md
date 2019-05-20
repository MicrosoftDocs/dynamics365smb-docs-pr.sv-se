---
title: Konfigurera API-mallar | Microsoft Docs
description: Beskriver stegen du måste göra för att konfigurera API-mallar för Dynamics 365 Business Central.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: ef6b6d89ccea59de6a87c062cc6e29a27abe2c88
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245484"
---
# <a name="configuring-api-templates"></a>Konfigurera API-mallar
API-bibliotek för [!INCLUDE[d365fin_md](includes/d365fin_md.md)] ger en förenklad representation av de underliggande enheterna. Alla egenskaper i programmet är inte tillgängliga via den associerade API. Sidan **API-inställningar** låter dig definiera mallar som används för att fylla i tomma egenskaper på en enhet när du skapar en POST-åtgärd via API. 

Till exempel en konfigurationsmall har definierats för artikelenheten när en ny post skapas genom artiklarnas API, alla egenskaper för ny artikel som inte har definierats i API får fyllas på från den valda mallen. Om till exempel inget värde har angetts för fältet **Produktbokföringsmall** via API:n, men värdet som definieras i den valda mallen och sedan används den bokföringsmall som definierats i mallen till det nya objektet. 

## <a name="setting-up-the-entity-template"></a>Konfigurera enhetsmall
Om du vill använda mallar med API-biblioteket, måste du först ställa in och ange egenskaper för mallarna. Du kan ställa in dessa mallar på sidan **Konfigurationsmallar**. Mer information finns också i [Så här förbereder du migrering av kunddata](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>Tilldela mallen till en API

Om du vill tilldela en mall till en API måste du gå igenom följande steg.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **API-inställningar** och välj sedan relaterad länk.
2. Välja **nytt**, och välj sedan värdet **Order** för posten.  
Om det finns mer än en mall som har valts för en API (Sid-ID), tillämpas mallarna i den ordning som definieras i kolumnen **Order**.   
När varje mall används, används bara fältvärden som definieras i mallen för fält som inte redan har ett värde som definierats, antingen uttryckligen i API eller i en tidigare använd mall i ordern. 
3. Välj ett värde för **Sid-ID**.  
Detta är sidan för API som mallen ska användas. Sökning **Sid-ID** visar en lista över alla API:er i biblioteket.
4. Välj ett värde i fältet **Mallkod**.  
Mallkod är koden för den mall som definierats på sidan **Konfigurationsmallar**. Mallvärdena som är definierade som är kopplade till API. 
5. I fältet **villkor** anger du vilken mall som ska användas.  
Definierad mall kopplas till en ny post som skapas via API och bara om de villkor som anges i fältet **villkor** uppfylls av de värden som redan har angetts för den nya instansen av enheten.

## <a name="see-also"></a>Se även
[API-dokumentation](/dynamics-nav/fin-graph)  
[Utveckla anslutningsprogram för[!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Aktivera API:er](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Slutpunkter för API:er](/dynamics-nav/endpoints-apis-for-dynamics)  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)