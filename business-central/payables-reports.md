---
title: Leverantörsskulder, rapporter och analyser
description: Se vilka produktionsrapporter och analyser som är tillgängliga i standardversionen av Business Central så att du kan hålla reda på dina leverantörsreskontra.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 347
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: edb3b32f88198d8e21aa2bfddafc1b7f319be9de
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953390"
---
# <a name="accounts-payable-reports-and-analytics-in-business-central"></a>Leverantörsreskontrarapporter och analys i Business Central

För att hjälpa dig att hantera dina leverantörsreskontra i [!INCLUDE [prod_short](includes/prod_short.md)] är standardrapporter och analyser inbyggda. Det överskrider traditionella rapporteringsbegränsningar för att hjälpa dig att effektivt utforma olika typer av rapporter.  

## <a name="reports"></a>Rapporter

I följande tabell beskrivs några av de viktigaste rapporterna inom leverantörsreskontrarapportering.

| Rapportera | Objekt-ID | Beskrivning |
|--|--|--|
| **Lev.skulder – ålder** | 322|Visar förfallna saldon för leverantörer i förfallna tidsintervall. Förfallna belopp kan visas som förfallo datum, bokföringsdatum eller efter dokumentdatum efter behov. Du kan välja att visa beloppen i lokal valuta (BVA) och skriva ut information om de förfallna dokumenten. Tidsintervallen kan ha rubriker med datum eller så är antalet förfallna i relation till den angivna åldern efter typ.<br>Den här rapporten är huvudrapport för avstämning av leverantörsreskontra till redovisning. Om du inte har tillåtit direkt bokföring på de konton som används i leverantörsbokföringsmallen för konto för kundreskontra, är den här rapporten en specifikation av de belopp som finns i redovisningen.|
| **Leverantörsreskontralista** | 321 | Visar leverantörens saldo per slutdatumet för angivet datumintervall. Du kan välja att visa leverantörssaldo i lokal valuta (BVA). Markera fältet **Ta bort borttagna transaktioner** för att visa de transaktioner som har stängts av slutdatumet, men som har avslutats (öppnats) vid ett senare datum. Markera **Visa transaktioner med noll saldo** om du vill visa leverantörer med saldon noll på datum filtrets slutdatum. Datum filtret gäller för de detaljerade leverantörsreskontratransaktionerna för transaktionerna i rapporten. Det innebär att om du har gjort en senare betalning än slutdatumet som har kopplats till fakturor inom datumintervallet, visas fakturorna i rapporten som de stängts av per slutdatum. |
| **Leverantörsråbalans** | 329 | Visar nettoförändringar för leverantörer under den period som anges i datum filtret samt nettoförändringen för räkenskapsåret innevarande år för det räkenskapsår som motsvarar perioden som valdes. Rapporten är grupperad efter leverantörsbokföringsmallar och ger en annan vy av leverantörredovisningen än rapporten **Lev.skulder – ålder**. **Obs!** om du inte har angett någon bokföringsperiod, kommer systemet inte att veta vilket räkenskapsår som ska användas och visar antingen år till datum från det senaste räkenskapsåret som definierats eller så väljer du den period som eventuellt kan vara från början av ett år.|
| **Lev. – huvudbok** | 304 | Visar alla leverantörsreskontratransaktioner i det angivna datumfiltret. Rapporten visar leverantörens ingående saldon i förhållande till datumfiltret. |
| **Inköpsstatistik** |312 |[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]<br>Den här rapporten kan även användas i leverantörsreskontra eftersom det är enklare att snabbt söka efter bokförda betalningar, rabatter och andra transaktioner för en viss leverantör.|
|**Lev.saldo - Ålderssammandrag**|305| Äldre rapport för lev.skulder - ålder. Vi rekommenderar att du använder rapporten **Kundfordringar - ålder** istället. Du kan välja en period och ett datum som ska användas som *förfallet* per datum.|
|**Stoppade betaln.**|319|Visar leverantörs reskontra transaktioner där fältet **Stoppad** inte är tomt.|
|**Förskottsbetalningsjournal för leverantör**|317|Visar utbetalningsjournal med information om kassarabatt och tolerans. Rapporten kan användas för att kontrollera betalningar innan betalningsfiler skapas och journalen bokförs. **Obs!** rapporten visar felaktigt kassarabatter när flera kreditnotor har använts i ett program. I det här fallet visas kassarabatten för de extra kreditnotorna som ett borttaget belopp.|
|**Leverantörslista**|301|Visar olika typer av grundläggande information om leverantören, såsom leverantörsbokföringsmall, rabatt- och betalningsinformation, prioritetsnivå och leverantörens standardvaluta samt leverantörens aktuella saldo (i BVA). Rapporten kan t.ex. användas för att underhålla informationen i tabellen Leverantör.|

## <a name="see-also"></a>Se även

[Analysera bokslut i Microsoft Excel](finance-analyze-excel.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Hantera anläggningstillgångar](fa-manage.md)  
[Översikt över lokala funktioner](about-localization.md)  
[Revisorupplevelse i [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
