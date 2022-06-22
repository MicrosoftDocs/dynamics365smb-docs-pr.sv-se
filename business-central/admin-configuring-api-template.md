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
ms.date: 06/07/2022
ms.author: solsen
ms.openlocfilehash: e38c8143cfad1fc4b0c7bbc4bd2995e0e48d264f
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950414"
---
# <a name="configure-api-templates"></a>Konfigurera API-mallar

API-bibliotek för [!INCLUDE[prod_short_md](includes/prod_short.md)] ger en förenklad representation av de underliggande enheterna. Alla egenskaper i programmet är inte tillgängliga via den associerade API. Sidan **API-inställningar** låter dig definiera mallar som används för att fylla i tomma egenskaper på en enhet när du skapar en POST-åtgärd via API. 

Till exempel en konfigurationsmall har definierats för artikelenheten när en ny post skapas genom artiklarnas API, alla egenskaper för ny artikel som inte har definierats i API får fyllas på från den valda mallen. Om till exempel inget värde har angetts för fältet **Produktbokföringsmall** via API:n, men värdet som definieras i den valda mallen och sedan används den bokföringsmall som definierats i mallen till det nya objektet. 

## <a name="setting-up-the-entity-template"></a>Konfigurera enhetsmall

Om du vill använda mallar med API-biblioteket, måste du först ställa in och ange egenskaper för mallarna. Du kan ställa in dessa mallar på sidan **Konfigurationsmallar**. Mer information finns i [Migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) (endast på engelska) i administrationsinnehållet.  

## <a name="assign-the-template-to-an-api"></a>Tilldela mallen till en API

Om du vill tilldela en mall till en API måste du gå igenom följande steg.

> [!NOTE]  
> API-mallar kan bara konfigureras med följande API-sidor: kontakter, countriesRegions, valutor, kunder, anställda, itemCategories, paymentMethods, paymentTerms, shipmentMethods, unitsOfMeasure och leverantörer.

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **API-inställningar** och väljer sedan relaterad länk.
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
[Utveckla Connect Apps för [!INCLUDE[prod_short_md](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Aktivera API:er](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Slutpunkter för API:er](/dynamics-nav/endpoints-apis-for-dynamics)  
[Administration](admin-setup-and-administration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]