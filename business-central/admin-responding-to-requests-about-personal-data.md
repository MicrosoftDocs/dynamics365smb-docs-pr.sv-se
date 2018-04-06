---
title: "Svara på begäranden om personuppgifter"
description: "Du måste svara på begäranden från uppgiftssubjekt."
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 03/13/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 89f53f24f74401ce384b54d04fbeb473aedad96d
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Svara på begäranden om personuppgifter  
Uppgiftssubjekt kan begära olika typer av åtgärder avseende deras personuppgifter. Om du har klassificerat känsligheten i dina uppgifter och är säker på att de är korrekta, kan en administratör svara på begäranden med hjälp av kalkylarket Dataklassificiering i rollcentret **Hantera användare, användargrupper och behörigheter** eller, om du använder Windows-klienten, i rollcentret **IT-chef**. Läs mer om klassificering av data och klassificering av datakänslighet i [Klassificering av Data](/dynamics-nav/classifying-data) och [Klassificering av datakänslighet](admin-classifying-data-sensitivity.md).

Följande tabell innehåller exempel på olika typer av förfrågningar som du kan svara på.

> [!Note]
> Även om vi tillhandahåller funktioner för att svara på den här typen av begäran och därmed erbjuder tillgång till personuppgifter, så är det ditt ansvar att se till att personliga och känsliga data finns och klassificeras på rätt sätt.

|Förfrågan - typ|Beskrivning och föreslagna svar|
|-----|-----|
|Begäranden för portabilitet|Ett datasubjekt kan göra en begäran om dataportabilitet, vilket bland annat betyder att man måste exportera datasubjektets personuppgifter från ditt system och tillhandahålla dem i ett strukturerat format som ofta används. Om du vill svara på förfrågningarna använder du verktyget Dataintegritet för att exportera personuppgifter till en Excel-fil. Med Excel kan du redigera personuppgifterna och spara dem i ett format som används ofta och som är maskinläsbart, som CSV- eller XML. Administratörer kan också exportera data med hjälp av snabb RapidStart-konfigurationspaket och sedan konfigurera huvuddatatabeller och relaterade tabeller som innehåller personuppgifter. |
|Begäranden om borttagning|En person kan begära att du tar bort deras personuppgifter. Det finns flera sätt att ta bort personlig information med hjälp av anpassningsfunktionerna, men du bär ansvaret för beslut och genomförande. I vissa fall kan du välja att redigera data direkt, till exempel ta bort en kontakt och sedan köra batch-jobbet Ta bort avbruten för att ta bort interaktioner för kontakten. <br><br> **Obs:** Om du har angett ett datum i fältet **Dokumentet kan tas bort före** på sidan **Försäljningsinställningar** eller **Inköpsinställningar** sidor kan du behöva ändra datumet så att du kan ta bort bokförda försäljnings- och inköpsdokument som du har skrivit ut och som har bokföringsdatum som infaller på eller före detta datum.|
|Begäranden om rättning|En person kan begära att du korrigerar felaktiga personuppgifter. Detta kan göras på olika sätt. I vissa fall kan du exportera listor till Excel för att snabbt massredigera flera poster och sedan importera den uppdaterade informationen. Mer information finns i [Exportera dina affärsdata till Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data). Du kan även manuellt redigera fält som innehåller personuppgifter, till exempel redigera information om en kund på kundkortet. Transaktionsposter som till exempel Allmänt, Kund och Redovisning av skattetransaktioner är emellertid nödvändiga för integriteten i företagets resursplaneringssystem. Om du lagrar personuppgifter i affärstransaktionsposter, överväg då att du använda anpassningsfunktionerna för att ändra dessa personuppgifter.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Begränsa databearbetning för datasubjekt
Ett datasubjekt kan begära att du tillfälligt slutar bearbeta deras personuppgifter. Om du vill tillgodose en sådan begära, kan du markera posten som blockerad av sekretesskäl i syfte att sluta bearbeta deras data. När en post har markerats som spärrad kan du inte skapa nya transaktioner som använder posten. Du kan till exempel inte skapa en ny faktura för en kund när antingen kunden eller säljaren är spärrad. För att markera ett datasubjekt som blockerat. öppna datasubjektets kort, till exempel kund-, leverantörs- eller kontaktkort, och välj kryssrutan **Sekretessblockerad**. Du kan behöva välja **Visa fler** för att visa fältet.

## <a name="handling-data-about-minors"></a>Hantera data om minderåriga
Om en kontaktperson ålder understiger åldern för juridiskt godkännande enligt lagstiftningen i din region, anger du detta genom att välja kryssrutan **Minderårig** på kortet **Kontakt**. När du gör detta väljs kryssrutan **Sekretessblockerad** automatiskt. När du får samtycke från minderårigs förälder eller vårdnadshavare kan du välja kryssrutan **Föräldrarnas samtycke mottaget** om du vill låsa upp kontakten. Även om du kan behandla personuppgifter för minderåriga kan du inte använda profileringsfunktionen i Microsoft Dynamics 365 for Sales.

> [!Note]
> Ändringsloggen kan registrera information som till exempel när och av vem kryssrutan **Föräldrarnas samtycke mottaget** har valts. En administratör kan konfigurera detta genom att välja guiden **Ändra logginställning** och även välja kryssrutan **Loggändringar för föräldrars samtycke har mottagits** på kortet **Kontakt**. Mer information finns i [Logga ändringar](/dynamics-nav-app/across-log-changes).  

## <a name="see-also"></a>Se även
[Klassificering av Data](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
[Klassificera datakänslighet](admin-classifying-data-sensitivity.md)  
[Exportera dina affärsdata till Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data)  

