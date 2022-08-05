---
title: Felsöka synkroniseringen av Shopify och Business Central
description: Lår dig vad du ska göra om något går fel under synkroniseringen av data mellan Shopify och Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: bebdf73fd1b01a3c750a3d91496a8f5bb87f8db4
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129647"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Felsöka synkroniseringen mellan Shopify och Business Central

Det kan hända att du behöver felsöka problem när du synkroniserar data mellan Shopify och [!INCLUDE[prod_short](../includes/prod_short.md)]. På den här sidan beskrivs åtgärder för att felsöka vanliga scenarier som kan uppstå.

## <a name="logs"></a>Loggar

Om en synkroniseringsuppgift misslyckas kan du aktivera loggning genom att aktivera reglaget **Aktivera logg** på **Shopify-butikskortet**. Utlösa synkroniseringsuppgift och granska loggar manuellt.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och anger **Shopify-loggposter** och väljer sedan relaterad länk.
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

## <a name="request-the-access-token"></a>Kräv åtkomsttoken

Om [!INCLUDE[prod_short](../includes/prod_short.md)] inte kan ansluta till ditt Shopify konto kan du prova att återställa åtkomsttoken från Shopify. Denna begäran kan behövas om det finns en rotation för säkerhetsnycklar eller ändringar i begärda behörigheter (omfattningar).

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill hämta åtkomsttoken för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Begär åtkomst**.
4. Om du uppmanas att logga in på ditt Shopify-konto.

Växlas **Har AccessKey** kommer att aktiveras.

### <a name="verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment"></a>Kontrol lera och aktivera behörigheter för att göra HTTP-begäranden när de körs i en miljö utan produktions miljön

Anslutnings tillägget kräver Shopify behörighet att göra HTTP-begäranden för att det ska fungera korrekt. Vid testning i sand lådor är HTTP-begäranden förbjudna för alla tillägg.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Tilläggshantering** och väljer sedan relaterad länk.
2. Välj tillägget *Shopify Connector*.
3. På sidan **Konfigurera** väljer du åtgärden **Tilläggsinställningar**.
4. Kontrollera att växlingsknappen **Tillåt HTTPClient-begäranden** är aktiverat.

## <a name="rotate-the-shopify-access-key"></a>Rotera Shopify snabbtangenten

I följande procedurer beskrivs hur du roterar den åtkomsttoken som används av Shopify Connector för att komma åt din Shopify onlinebutik.

### <a name="in-shopify"></a>I Shopify

1. Gå till **Shopify administratör** i din [appar](https://www.shopify.com/admin/apps).
2. I raden med **Dynamics 365 Business Central** app, välj **Ta bort**.
3. Välj **Ta bort** i meddelandet.

### <a name="in-prod_short"></a>I [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill rotera åtkomsttoken för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Begär åtkomst**.
4. Om du uppmanas till det, loggar du in på ditt Shopify-konto, granskar sekretess och behörigheter och trycker sedan på knappen **Installera app**.

## <a name="see-also"></a>Se även

[Kom igång med kopplingen för Shopify](get-started.md)  