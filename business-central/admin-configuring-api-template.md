---
title: Konfigurera API-mallar
description: Beskriver stegen du måste göra för att konfigurera API-mallar för Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.search.form: 5469
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 63793ca9907d0b2c58df7f82dae88783ba0fcbc7
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136355"
---
# <a name="configuring-api-templates"></a>Konfigurera API-mallar

API-bibliotek för [!INCLUDE[prod_short_md](includes/prod_short.md)] ger en förenklad representation av de underliggande enheterna. Alla egenskaper i programmet är inte tillgängliga via den associerade API. Sidan **API-inställningar** låter dig definiera mallar som används för att fylla i tomma egenskaper på en enhet när du skapar en POST-åtgärd via API. 

Till exempel en konfigurationsmall har definierats för artikelenheten när en ny post skapas genom artiklarnas API, alla egenskaper för ny artikel som inte har definierats i API får fyllas på från den valda mallen. Om till exempel inget värde har angetts för fältet **Produktbokföringsmall** via API:n, men värdet som definieras i den valda mallen och sedan används den bokföringsmall som definierats i mallen till det nya objektet. 

## <a name="setting-up-the-entity-template"></a>Konfigurera enhetsmall
Om du vill använda mallar med API-biblioteket, måste du först ställa in och ange egenskaper för mallarna. Du kan ställa in dessa mallar på sidan **Konfigurationsmallar**. Mer information finns också i [Så här förbereder du migrering av kunddata](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>Tilldela mallen till en API

Om du vill tilldela en mall till en API måste du gå igenom följande steg.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **API-inställningar** och väljer sedan relaterad länk.
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
[Utveckla anslutningsprogram för[!INCLUDE[prod_short_md](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Aktivera API:er](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Slutpunkter för API:er](/dynamics-nav/endpoints-apis-for-dynamics)  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]