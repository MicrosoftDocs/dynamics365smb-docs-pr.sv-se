---
title: Inspektera sidor i Business Central
description: Använd funktionen sidinspektion för att zooma in detaljer om sidans design och datakälla. Sidinspektören är perfekt för att felsöka problem med dina data.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
ms.service: dynamics365-business-central
author: jswymer
ms.author: jswymer
ms.date: 10/01/2020
ms.openlocfilehash: d7731c9fa7c6ac8bdcc87c918da8ffb93544f7f5
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379204"
---
# <a name="inspecting-pages-in-business-central"></a>Inspektera sidor i Business Central

Funktionen för sidinspektion låter dig hämta information om en sida, ge insikt i sidans design, de olika element som utgör grunden för sidan och källan för de data som visas. Sidinspektion är särskilt utformad för administratörer, privilegierade användare, supportpersonal och utvecklare. Den är perfekt för att lära sig datamodellen bakom en sida och felsökning. Om det till exempel uppstår problem med en sida, kan du använda granskning på sidan för att hämta information som vidarebefordras till systemadministratören eller supportpersonal.

## <a name="working-with-page-inspection"></a>Arbeta med sidinspektion

Du startar sidgranskning från sidan **hjälp och support**. Välj frågetecknet i övre högra hörnet, välj **hjälp och support** och välj **Kontrollera sidor och data**. Du kan bara använda kortkommandot **Ctrl + Alt + F1**.

Rutan **sidinspektion** visas på sidan. I följande figur visas rutan **Sidinspektion** på sidan **försäljningsorder**.

![Sidinspektion](media/page-inspection-example.png)

När rutan **Sidinspektion** först öppnats, visas information som tillhör objektet på huvudsidan.

Använd tangentbord eller pekdon för att flytta markeringen till olika element på sidan. När du väljer en faktabox eller en del av huvudsidan markeras markeringsområdet med en ram och rutan **Sidinspektion** visar information om det valda elementet. Till exempel föregående bild visar information om listan som en del på sidan **försäljningsorder**. När du navigerar mellan sidorna i programmet kommer rutan **Sidinspektion** att uppdateras automatiskt med sidinformation allt eftersom.

För mer information om vad som ska visas i sidisnpektionen, se [Inspektera och felsöka sidor](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) i hjälpavsnittet för Business Central-utvecklare och IT-proffs.

Om du inte kan se de information som borde finnas i rutan **Sidinspektion** har du förmodligen inte behörighet, som beskrivs i nästa avsnitt.

## <a name="controlling-access-to-page-inspection-details"></a>Kontrollera åtkomst till information om sidinspektion

Som administratör kan du styra åtkomsten till alla detaljer som visas i rutan **Sidinspektion** genom att konfigurera de behörigheter som användaren har. Om du vill ge en användarbehörighet till alla detaljer, ge användarna behörigheten **Utföra** i **System** objekt **5330**. Du kan bevilja behörighet med hjälp av en behörighetsuppsättning (som **felsöka D365**) eller en användargrupp (som **felsöka D365**). Mer information om behörigheter finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).

Användare som inte har beviljats behörighet för **systemobjekt 5330** kan fortfarande få åtkomst till rutan **sidinspektion**, men de kommer endast att se fälten **Sida** och **Tabell** som visar grundläggande information att de kan vidarebefordra till deras supportteam.

## <a name="see-also"></a>Se även

[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]