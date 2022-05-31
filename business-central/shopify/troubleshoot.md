---
title: Felsöka synkroniseringen av Shopify och Business Central
description: Lår dig vad du ska göra om något går fel under synkroniseringen av data mellan Shopify och Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 01ff5ab1c5e6f132098f914f6bfe97e097cc88b0
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768220"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Felsöka synkroniseringen mellan Shopify och Business Central

Det kan hända att du behöver felsöka problem. På den här sidan beskrivs åtgärder för att felsöka vanliga scenarier som kan uppstå.

## <a name="logs"></a>Loggar

Om en synkroniseringsuppgift misslyckas kan du aktivera loggning genom att aktivera reglaget **Aktivera logg** på **Shopify-butikskortet**. Utlösa synkroniseringsuppgift och granska loggar manuellt.

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och anger **Shopify-loggposter** och väljer sedan relaterad länk.
2. Välj den berörda loggposten och öppna fönstret **Shopify-loggpost**.
3. Kontrollera begäran, statuskod och beskrivning och svar.

Glöm inte att inaktivera loggning för att undvika negativ inverkan på prestanda och öka databasstorleken.

Från fönstret **Shopify-loggposter** kan du utlösa borttagning av alla loggposter eller de som är äldre än sju dagar.

## <a name="data-capture"></a>Datainsamling

Oavsett inställningar för **Logg aktiverad** loggas alltid vissa svar från Shopify, som du kan inspektera eller ladda ner från fönstret **Datainsamlingslista**.

Välj åtgärden **Hämtade Shopify-data** på en av följande sidor:

- **Shopify-order**
- **Shopify-orderuppfyllelse**
- **Leveranskostnader för Shopify-order**
- **Shopify-ordertransaktioner**
- **Shopify-utbetalningar**
- **Shopify-betalningstransaktioner**
- **Shopify-transaktioner**

## <a name="reset-sync"></a>Återställ synkronisering

För optimala prestanda importerar kopplingen endast kunder, produkter och ordrar som har skapats eller ändrats sedan den senaste synkroniseringen. På **Shopify-butikskortet** finns funktioner för att ändra datum och tid för den senaste synkroniseringen eller för att återställa den helt. Med den här funktionen ser du till att alla data synkroniseras och inte bara de ändringar som gjorts sedan den senaste synkroniseringen utfördes.

Den här funktionen kan endast användas för synkroniseringar från Shopify till [!INCLUDE[prod_short](../includes/prod_short.md)] och kan vara användbar om du behöver återställa borttagna data, såsom produkter, kunder eller borttagna ordrar.

## <a name="update-the-access-token"></a>Uppdatera åtkomsttoken

Om [!INCLUDE[prod_short](../includes/prod_short.md)] inte kan ansluta till ditt Shopify-konto kan du prova att återställa åtkomsttoken.

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Shopify-butik** och välj relaterad länk.
2. Välj den butik som du vill hämta åtkomsttoken för och öppna sidan **Shopify-butikskort**.
3. Ange koden i fältet **Kod**.  
4. Välj åtgärden **Begär åtkomst**.
5. Om du uppmanas att logga in på ditt Shopify-konto.

## <a name="see-also"></a>Se även

[Kom igång med kopplingen för Shopify](get-started.md)  
