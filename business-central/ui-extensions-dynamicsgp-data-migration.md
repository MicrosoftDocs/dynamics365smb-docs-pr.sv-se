---
title: Migrera Data från Dynamics GP med tillägget Data Migration | Microsoft Docs
description: Använda tillägget Dynamics GP-datamigrering för att flytta över kunder, leverantörer, lagerartiklar, redovisningskonton, öppna leverantörs- och kundreskontratransaktioner från Dynamics GP till Business Central.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: c5798baec1130c3fc662a8751aee87bb8b438146
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311290"
---
# <a name="the-dynamics-gp-data-migration-extension"></a>Tillägget Dynamics GP datamigrering 
Detta tillägg gör det enkelt att flytta över kunder, leverantörer, lagerartiklar, redovisningskonton, öppna leverantörs- och kundreskontratransaktioner från Dynamics GP [!INCLUDE[prodshort](includes/prodshort.md)]. Om ditt företag använder Dynamics GP i dag, kan du exportera nödvändiga poster och sedan öppna guiden för assisterad konfiguration för att överföra data till [!INCLUDE[prodshort](includes/prodshort.md)]. Tillägget Migrering fungerar för alla versioner av Microsoft Dynamics GP. Mer information finns i [Importera företagsdata från ett annat finanssystem](across-import-data-configuration-packages.md).

## <a name="exporting-data-from-dynamics-gp"></a>Exportera data från Dynamics GP
Du måste ha exporterat några av dina befintliga kunder, leverantörer, lagerartiklar och redovisningskonton med hjälp av funktionen dataexport i Dynamics GP. Du kan välja följande typer när du väljer data som ska exporteras:

* Konto  
* Kund  
* Artikel  
* Leverantör  

När exportfilen har skapats har du en zip-fil som innehåller flera txt-filer som bestäms av vad du har valt under exporten av data.  Dessutom visas ytterligare txt-filer som skapats med extra information som behövs för att inställningarna i ditt nya [!INCLUDE[prodshort](includes/prodshort.md)]-företag.

Tillägget Datamigrering för Dynamics GP mappas automatiskt den exporterade informationen så att dina data är snabbt tillgängliga i ditt nya [!INCLUDE[prodshort](includes/prodshort.md)]-företag.

## <a name="whats-new-in-the-october-2018-release"></a>Vad är nytt i oktober 2018 versionen

I den här versionen har vi utökat mängden data som vi tillföra [!INCLUDE[prodshort](includes/prodshort.md)] från Dynamics GP.

I migreringsguiden kan du nu välja hur du vill överföra kontoplanen i Dynamics GP. Du kan flytta över den befintliga kontoplanen eller skapa en ny kontoplan utifrån den befintliga kontoplanen.  

Om du vill använda den befintliga kontoplanen kontona ska ställas in som ett segment för huvudkontot från Dynamics GP och ytterligare segment ska fungera som dimensioner i [!INCLUDE[prodshort](includes/prodshort.md)].  

Om du väljer att skapa en ny kontoplan får du en ytterligare kontoinformationssida i guiden så att du kan hämta arbetsboken, göra vissa ändringar och sedan importera arbetsboken igen om du vill ändra dina konton.  

Du måste hämta Excel-arbetsboken och kartlägga ett nytt kontonummer till varje kontonummer i Excel-kalkylbladet. Varje konto måste ha sitt eget nummer eller migreringen kommer att bli fel. När du har slutfört mappningen kan du fortsätta du med migreringsguiden genom att importera Excel-arbetsboken som du just har uppdaterat. Guiden verifierar att varje rad har en unik kontonummer och att inga rader har ett nytt tomt kontonummer i dem.  

Med ändringen i mappningen för kontoplansalternativ ser du även en ändring av typen av data kommer in i redovisningsjournalen för kontonumren.  

- Om du vill använda de befintliga kontonumren för vi över ingående saldo på huvudsegmentet (nytt kontonumret) som en summering av huvudkontonumret vid tidpunkten för migreringen.  
- Om du väljer att skapa nya kontonummer medför vi översiktsinformation för motsvarande två räkenskapsår baserat på de räkenskapsperioder som du har ställt in i Dynamics GP.

I tidigare versioner av [!INCLUDE[prodshort](includes/prodshort.md)], migrerade guiden en samlingstransaktion för kunden/leverantöresn saldo i Dynamics GP. Nu hämtar vi de detaljerade öppna transaktionerna för kunder och leverantörer vid tidpunkten för migreringen. Vad innebär detta? Om din kund har 3 utestående transaktioner registrerade i modulen Kundreskontra för guiden in dessa transaktioner i [!INCLUDE[prodshort](includes/prodshort.md)] med utestående belopp som dokumentbelopp. Detta är samma för Leverantörsreskontramodulen för leverantörer.  

Lagerartiklar importeras med den kostnadsvärderingsmetod som valdes när företagets installationsguide kördes. Serviceartiklar kan automatiskt tilldelas FIFO-värderingsmetoden. För närvarande tar vi in Lagersaldo för artiklarna vid tidpunkten för migrationen.  Denna kvantitet hämtas till tomt lagerställe.  

Det sista alternativet som visas i datamigreringsguiden för Dynamics GP är möjligheten att ange bokföringsalternativ. Den här inställningen anger om du vill bokföra alla transaktioner automatiskt i redovisningsjournaler när migreringen flyttar data i [!INCLUDE[prodshort](includes/prodshort.md)], eller om du vill bokföra manuellt så att alla transaktioner kommer att bli journaler inne på sidan Redovisningsjournal så att du kan kontrollera informationen innan du bokför. Detta alternativ visas på sidan Alternativ för kontoplan.


## <a name="see-also"></a>Se även
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Anpassa [!INCLUDE[prodshort](includes/prodshort.md)] med tillägg](ui-extensions.md)  
