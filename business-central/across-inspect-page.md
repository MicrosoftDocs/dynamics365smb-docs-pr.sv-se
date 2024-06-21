---
title: Inspektera sidor i Business Central
description: Använd funktionen sidinspektion för att zooma in detaljer om sidans design och datakälla. Sidinspektören är perfekt för att felsöka problem med dina data.
ms.topic: conceptual
author: jswymer
ms.author: jswymer
ms.date: 09/15/2023
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# Inspektera sidor i Business Central

Funktionen för sidinspektion låter dig hämta information om en sida, ge insikt i sidans design, de olika element som utgör grunden för sidan och källan för de data som visas. Sidinspektion är särskilt utformad för administratörer, privilegierade användare, supportpersonal och utvecklare. Den är perfekt för att lära sig datamodellen bakom en sida och felsökning. Om det till exempel uppstår problem med en sida, kan du använda granskning på sidan för att hämta information som vidarebefordras till systemadministratören eller supportpersonal.

> [!NOTE]  
> Med [!INCLUDE [prod_short](includes/prod_short.md)] utgivningscykel 2 för 2023 kan du via sidinspektion starta Visual Studio Code inifrån webbklienten för att ytterligare undersöka och felsöka källkoden för ett tillägg. Mer information finns i [Felsöka i Visual Studio Code direkt från webbklienten](/dynamics365/business-central/dev-itpro/developer/devenv-troubleshoot-vscode-webclient) i hjälpen för Business Central utvecklare och IT-proffs.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]

## Arbeta med sidinspektion

Du startar sidgranskning från sidan **hjälp och support**. Välj frågetecknet i övre högra hörnet, välj **hjälp och support** och välj **Kontrollera sidor och data**. Du kan bara använda kortkommandot <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>F1</kbd>.

Rutan **sidinspektion** visas på sidan. När rutan först öppnas visas information som tillhör objektet på huvudsidan.

Använd tangentbord eller pekdon för att flytta markeringen till olika element på sidan. När du väljer en faktabox eller en del av huvudsidan markeras markeringsområdet med en ram och rutan **Sidinspektion** visar information om det valda elementet. Till exempel föregående bild visar information om listan som en del på sidan **försäljningsorder**. När du navigerar mellan sidorna i programmet kommer rutan **Sidinspektion** att uppdateras automatiskt med sidinformation allt eftersom.

För mer information om vad som ska visas i sidisnpektionen, se [Inspektera och felsöka sidor](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) i hjälpavsnittet för Business Central-utvecklare och IT-proffs.

Om du inte kan se de information som borde finnas i rutan **Sidinspektion** har du förmodligen inte behörighet, som beskrivs i nästa avsnitt.

## Kontrollera åtkomst till information om sidinspektion

Som administratör kan du styra åtkomsten till alla detaljer som visas i rutan **Sidinspektion** genom att konfigurera de behörigheter som användaren har. Om du vill ge en användarbehörighet till alla detaljer, ge användarna behörigheten **Utföra** i **System** objekt **5330**. Du kan bevilja behörighet med hjälp av en behörighetsuppsättning (som **felsöka D365**) eller en användargrupp (som **felsöka D365**). Mer information om behörigheter finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).

Användare som inte har beviljats behörighet för **systemobjekt 5330** kan fortfarande få åtkomst till rutan **sidinspektion**, men de kommer endast att se fälten **Sida** och **Tabell** som visar grundläggande information att de kan vidarebefordra till deras supportteam.

## Se även

[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
