---
title: Konfigurera din webbläsare
description: Beskriver hur du konfigurerar webbläsare så att dessa fungerar med Business Central och produkter som är integrerade med det.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 01/08/2021
ms.author: jswymer
ms.openlocfilehash: 17b41653b1b5934e98c82ce8a35430e7b6a5c0d0
ms.sourcegitcommit: 1aac2c5f6773151c011dc1e4069c84d79fe5bda8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839970"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a>Ställa in och felsöka webbläsaren så att den fungerar med webb klienten för Business Central

I den här artikeln beskrivs hur du konfigurerar din webbläsare så att [!INCLUDE[web_client](includes/web_client.md)] och dess funktioner fungerar korrekt. Läs den här artikeln om du har problem med att öppna [!INCLUDE[web_client](includes/web_client.md)], detta eftersom vissa problem kan orsakas av webbläsarens inställningar.

Artikeln innehåller information om hur du konfigurerar Microsoft Edge, men kraven för JavaScript, cookies och popup-fönster är desamma för alla webbläsare som stöds. Mer information om andra webbläsare finns i tillverkarens instruktioner.  

## <a name="use-a-supported-browser"></a>Använd en webbläsare som stöds

Se till att du använder en av de webbläsare som stöds. Se [Minimikrav för att använda Business Central](product-requirements.md#recommended-browsers).  

## <a name="allow-javascript-from-business-central"></a>Tillåt JavaScript från Business Central

*Problem:*

Om webbläsaren inte tillåter JavaScript visas **NotSupported/DisabledJavaScript** i adressfältet och ett **HTTP-fel 404.0 – meddelandet hittades inte** när du försöker öppna [!INCLUDE[prod_short](includes/prod_short.md)], och 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

*Lösningen*

1. I Microsoft Edge går du till **Inställningar** > **Cookies och webbplatsbehörigheter** > **JavaScript**.
2. Gör något av följande. Välj det steg som rekommenderas av organisationen:

    - Flytta reglaget **Tillåtet** åt vänster (Av). Välj sedan **Lägg till** och skriv in webbadressen (URL) för [!INCLUDE[prod_short](includes/prod_short.md)] i rutan **Webbplats**. Välj **Lägg till** när du är klar.
    - Flytta reglaget **Tillåtet** åt höger (På).

## <a name="allow-cookies-from-business-central"></a>Tillåt cookies från Business Central

*Problem:*

Om webbläsaren inte tillåter cookies visas följande felmeddelande:

**Det gick tyvärr inte att hitta sidan. Kontrollera adressen och försök igen.** 

*Lösningen*

1. I Microsoft Edge går du till **Inställningar** > **Cookies och webbplatsbehörigheter** > **Cookies och webbplatsdata**.
2. Flytta reglaget för **Tillåt webbplatser att spara och läsa cookiedata** åt höger (På).  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a>Tillåt popup-fönster från Business Central

[!INCLUDE[prod_short](includes/prod_short.md)] integreras med flera produkter. I vissa fall, t. ex. när Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] eller "popup-fönster" öppnas i produkten. Denna funktion kräver att webbläsaren tillåter popup-fönster från [!INCLUDE[prod_short](includes/prod_short.md)].

*Problem:*

Om popup-fönster för [!INCLUDE[prod_short](includes/prod_short.md)] blockeras visas ett meddelande som påminner om följande:

**Något gick fel. Din webbläsare kanske blockerar popup-fönster som krävs av Business Central.**

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
*Lösningen*

1. I Microsoft Edge går du till **Inställningar** > **Cookies och webbplatsbehörigheter** > **Popup-fönster och omdirigeringar**.
2. Flytta reglaget **Blockerat** åt höger (På).
3. Välj **Lägg till**. I rutan **Webbplats** anger du `https://businesscentral.dynamics.com` och väljer sedan **Lägg till**.

## <a name="see-also"></a>Se även

[Felsöka Teams](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]