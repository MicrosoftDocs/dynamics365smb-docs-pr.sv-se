---
title: "Olika sätt att felsöka och lösa problem | Microsoft Docs"
description: "Lär dig hur du kan lösa eventuella problem i Accountant Hub för Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: e4f739e13123054527bf3116aec2c8c4133537e6
ms.contentlocale: sv-se
ms.lasthandoff: 04/16/2018

---
# <a name="troubleshooting-include-d365acclongincludesd365acclongmdmd"></a>Felsökning [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Det går enkelt och snabbt att registrera sig för [!INCLUDE [d365acc](includes/d365acc_md.md)]. Lägga till klienter på instrumentpanelen är också lätt, men den här artikeln innehåller lösningar på problem som kan uppstå på vägen.

## <a name="what-email-address-can-i-use-with-include-d365accincludesd365accmdmd"></a>Vilken e-postadress kan jag använda med [!INCLUDE [d365acc](includes/d365acc_md.md)]?
[!INCLUDE [d365acc](includes/d365acc_md.md)] kräver att du använder en e-postadress från ditt arbete eller skola för att registrera dig. [!INCLUDE [d365acc](includes/d365acc_md.md)] har inte stöd för e-postadresser som tillhandahålls av e-posttjänster för konsumenter eller telekommunikationsleverantörer. Dessa omfattar outlook.com, hotmail.com, gmail.com, etc..  

Om du försöker att registrera dig med en personlig e-postadress kommer du att få ett meddelande som indikerar att du använder en e-postadress från arbete eller skola.  

## <a name="why-cant-i-connect-to-my-clients-data"></a>Varför kan jag inte ansluta till min klients data?
Det kan finnas ett par anledningar, bland annat följande:

- URL i fältet **Klient-URL** är inte giltig:  

  Gå till **hantera klienter**, öppna klienten som du inte kan ansluta till och välj **Testa klient-URL**.  
- Klientens företag är offline, till exempel om den uppgraderas

  I instrumentpanelen, väljer du menyposten **verktyg** och väljer **kontrollera fel**. Då öppnas en lista med teknisk information, så du kanske vill kontakta administratören om du ser fel. Felmeddelandet ”servern godkände inte klientens referenser” innebär till exempel att du inte har tillgång.  
- Du inte har fått ett e-postmeddelande från klienten som bjuder in dem till deras [!INCLUDE [d365fin](includes/d365fin_md.md)], eller om du inte öppnade länken i e-postmeddelandet eller om du inte accepterade inbjudan

  Du måste öppna länken i inbjudan och acceptera de steg som lägger till dig i kundens [!INCLUDE [d365fin](includes/d365fin_md.md)]. Till dess kan har du inte tillgång till deras data.  
- Du har inte tillgång till alla företag i din klients [!INCLUDE [d365fin](includes/d365fin_md.md)]

  Klienten kan ha flera affärsenheter eller företag i [!INCLUDE [d365fin](includes/d365fin_md.md)], och din inbjudan innehåller inte alltid alla företag. Arbeta med klienten för att se till att du har tillgång till företagen som klienten vill att du arbetar i.  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a>Varför uppdateras inte informationen på min instrumentpanel?
När du lägger till en klient eller begär en uppdatering av data hämtar [!INCLUDE [d365acc](includes/d365acc_md.md)] data. Men du måste uppdatera fönstret, till exempel om du väljer åtgärden ”Visa alla företag”, uppdatera webbläsarfönstret, navigera från instrumentpanelen och sedan tillbaka igen, eller liknande. Detta är ett känt problem som vi arbetar på att förbättra i en senare uppdatering.  

## <a name="see-also"></a>Se även
[Komma igång med [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Lägga till klienter i instrumentpanelen i [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)  

