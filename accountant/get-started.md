---
title: Revisorupplevelse i Dynamics 365 | Microsoft Docs
description: Läs mer om Accountant Hub för Dynamics 365.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/23/2018
ms.author: edupont
ms.openlocfilehash: 0c4dadb15c9756c49f94839236766432844088c8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807144"
---
# <a name="get-started-with-include-d365acclongincludesd365acclongmdmd"></a>Kom igång med [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Alla företag måste göra sin redovisning och godkänna redovisningen. Vissa företag använder en extern revisor och andra har en revisor bland personalen. Om du är en revisor med flera klienter, använd [!INCLUDE [d365acc](includes/d365acc_md.md)] som din instrumentpanel för en bättre överblick över dina kunder.  

Du kan få tillgång till [!INCLUDE [d365acc](includes/d365acc_md.md)] genom att logga in från [Dynamics 365 — Accountant Hub på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants).  

> [!TIP]
>  När du registrerar dig för [!INCLUDE [d365acc](includes/d365acc_md.md)] måste du ange din e-postadress för arbete som <em>me@accountant.com</em>. Vi rekommenderar att du använder samma e-postadress när du arbetar i klientens [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)], så att du kan växla mellan klienter. E-postadressen måste vara en arbetsadress som baseras på ett Active Directory.

## <a name="working-with-individual-clients"></a>Arbeta med enskilda kunder
Instrumentpanelen visar den viktigaste informationen om varje klient.  

> [!div class="mx-imgBorder"]
> ![Accountant Hub](./media/accountant-get-started/accountant-dashboard.png)

Kolumnen **klientnamn** visar namnen på kunder och kolumnen **företagsnamn** visar alla företag om klienten har mer än ett företag i [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]. Det finns också fält som visar dig uppgifter som har tilldelats dig i kundens företag, inklusive förfallna aktiviteter.  

Du kan anpassa instrumentpanelen att visa de datapunkter som du vill ska visas genom att lägga till eller ta bort kolumner. Du kanske vill visa moms som har förfallit till betalning, hur många öppna försäljningsdokument varje klient har eller antalet inköpsfakturor som förfaller nästa vecka. Du kan konfigurera vyn så att den passar dina behov. Om du har många klienter kan använda du filter för att sortera vyn.  

Bredvid klienten visar tre punkter en kort meny:

- Uppdatera det aktuella företaget och hämta nya data för klienten  
- Gå till klientens [!INCLUDE [d365fin](includes/d365fin_md.md)]  
- Välj fler klienter  

På samma sätt kan du använda listrutan **klientsammanfattning** för att uppdatera alla företag.  

> [!TIP]
>  För att få åtkomst till en klients [!INCLUDE [d365fin](includes/d365fin_md.md)], väljer du menyobjektet **gå till klient** - du loggas in automatiskt.

## <a name="company-details"></a>Företagsdetaljer
Mer information om klientens data ser du genom att välja namnet på det företag som du vill veta mer om. Då öppnar rutan **Företagsdetaljer** där du kan visa ytterligare information, till exempel följande:  

* Saldon på kassakonto  
* Kassaflödesprognos  
* Förfallna inköpsfakturor  
* Förfallna försäljningsfakturor  

> [!div class="mx-imgBorder"]
> ![Klientens företagsinformation på revisorns instrumentpanel.](./media/accountant-get-started/accountant-company-details.png)

Tekniskt sett är du nu inloggad i kundens [!INCLUDE [d365fin](includes/d365fin_md.md)], och informationen du ser är aktuella data. Om du vill titta närmare på data, till exempel förfallna inköpsfakturor väljer du länken och tas till kundföretaget.  

> [!TIP]
> Du kan starta en fördefinierad Excel-arbetsbok från fliken **rapporter** i menyfliksområdet. Dessa arbetsböcker är utformade som viktiga ekonomiska rapporter som är klara att skrivas ut och du kan också ändra dem efter behov. Mer information finns i [analys av finansiella rapporter i Microsoft Excel](/dynamics365/business-central/finance-analyze-excel?toc=/dynamics365/accountants/toc.json) i hjälpavsnittet för [!INCLUDE [d365fin](includes/d365fin_md.md)].  

I annat fall stänger du av informationsfönstret och fortsätter till nästa klient.  

## <a name="assigned-tasks"></a>Tilldelade uppgifter
I klientens [!INCLUDE [d365fin](includes/d365fin_md.md)] kan du tilldela aktiviteter till dig och andra och andra kan tilldela aktiviteter till dig. Instrumentpanelen i [!INCLUDE [d365acc](includes/d365acc_md.md)] ger dig en översikt över tilldelade uppgifter för varje klient och du öppnar en lista med alla fördelningar genom att välja **Mina användaruppgifter** på sidan **Start**.  

I klientföretaget har du också stack-ikonerna som anropar arbetsuppgifter som har tilldelats dig i denna särskilda klient.

> [!div class="mx-imgBorder"]
> ![Uppgifter som har tilldelats revisorn i klientföretaget](./media/accountant-get-started/accountant-company-details-tasks.png)

### <a name="my-user-tasks"></a>Mina användaruppgifter
Listan **Mina användaruppgifter** i [!INCLUDE [d365acc](includes/d365acc_md.md)] kan du prioritera din arbetsdag genom att visa mer information om uppgifter som har tilldelats på alla klienter.  

> [!div class="mx-imgBorder"]
> ![Lista över uppgifter som har tilldelats mig som en extern revisor](./media/accountant-get-started/accountant-tasklist.png)

Du kan sortera efter förfallodatum, till exempel eller någon annan typ av data som hjälper dig att prioritera din dag. I listan visas alla uppgifter som har tilldelats dig som standard, men du kan ställa in filter för att endast visa uppgifter som är markerade med hög prioritet, till exempel.

Om du vill välja en uppgift, väljer du den bara från listan över väntande användaruppgifter. I menyfliken öppnar länken **Gå till uppgiftsobjekt** sidan där du kan utföra arbetet.  

När du har slutfört en uppgift bara markerar du den som slutförd.  

## <a name="see-also"></a>Se även

[Lägga till klienter i instrumentpanelen i [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)  
[Välkommen till [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](index.md)  
[Analysera bokslut i Microsoft Excel](/dynamics365/business-central/finance-analyze-excel?toc=/dynamics365/accountants/toc.json)  
[Revisorupplevelse i [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json)  
[Dynamics 365 — Accountant Hub på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
