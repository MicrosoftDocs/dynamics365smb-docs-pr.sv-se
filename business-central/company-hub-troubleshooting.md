---
title: Felsöka företagsnavet
description: Lär dig mer om hur du kringgår eventuella problem när du kör företagsnavet i Dynamics 365 Business Central för att hantera arbete i flera olika företag.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.search.form: 1151
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 988e59cd953339c305b704caf42d3b1c31372e50
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/26/2022
ms.locfileid: "8028883"
---
# <a name="troubleshooting-your-company-hub"></a>Felsöka företagsnavet

Lägga till företag på instrumentpanelen för företagsnavet är också lätt, men den här artikeln innehåller lösningar på problem som kan uppstå på vägen.  

## <a name="check-errors"></a>Kontrollera fel

Använd åtgärden **Kontrollera fel** om du vill visa en lista över de senaste felen. Du kan visa ytterligare information om varje fel och rensa loggen genom att ta bort äldre poster.  

## <a name="connection-failed"></a>Anslutning misslyckades

Det kan finnas en par olika orsaker till att du inte kan ansluta till ett företag, däribland följande:

- URL i fältet **Miljölänk** är inte giltig  

  Gå till sidan **Miljölänkar**, öppna den miljö som du inte kan ansluta till och välj sedan åtgärden **Testa anslutningen**.  
- Klientens företag är offline, till exempel om den uppgraderas

  I instrumentpanelen, väljer du menyposten **verktyg** och väljer **kontrollera fel**. Då öppnas en lista med teknisk information, så du kanske vill kontakta administratören om du ser fel. Felmeddelandet ”*Servern godkände inte klientens referenser*” innebär till exempel att du inte har tillgång.  
- Du har inte tillgång till alla företag i miljön som du försöker ansluta till

  I [!INCLUDE [prod_short](includes/prod_short.md)] kan en organisation ha flera affärsenheter som kallas företag, och du kanske inte har tillgång till alla företag. Arbeta med administratören eller klienten för att se till att du har tillgång till företagen som du arbetar i.  

## <a name="data-does-not-refresh"></a>Data uppdateras inte

När du lägger till ett företag eller begär en uppdatering av data hämtar [!INCLUDE [prod_short](includes/prod_short.md)] data. Men du måste uppdatera sidan, till exempel om du väljer åtgärden **Läs in alla företag igen**, uppdatera webbläsarsidan, navigera från instrumentpanelen och sedan tillbaka igen, eller liknande.  

Om du har lagt till ett företag men det inte visas i listan kan du också använda åtgärden **Läs in alla företag igen** för att uppdatera listan.

## <a name="see-also"></a>Se även

[Hantera arbete i flera företag med företagsnavet](company-hub.md)  
[Lägg till företag till företagsnavet](company-hub-add-company.md)  
[Revisorlösningar i Business Central](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]