---
title: Svara på begäranden om personuppgifter
description: I det här avsnittet beskrivs hur du svarar på förfrågningar om personuppgifter. Detta kallas registrerades begäran.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 06/14/2021
ms.reviewer: na
ms.topic: conceptual
ms.openlocfilehash: 0d1ead6fc36df5b06f9ab995bbc30ce04d24c622
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8148856"
---
# <a name="responding-to-requests-about-users-personal-data"></a>Svara på begäranden om användarens personuppgifter  
Uppgiftssubjekt kan begära olika typer av åtgärder avseende deras personuppgifter. Exempelvis under de Allmänna dataskyddsbestämmelserna (GDPR), har bosatta inom EU rätt att begära export, borttagning och ändring av deras personuppgifter. Detta kallas *registrerades begäran*. Om du har klassificerat känsligheten i dina data och är säker på att de är korrekta, kan en administratör svara på begäranden med hjälp av alternativen under fliken **Datasekretess** u rollcentret **IT-chef**. Läs mer om klassificering av data och klassificering av datakänslighet i [!INCLUDE[prod_long](includes/prod_long.md)], se [Klassificering av data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) och [Klassificering av datakänslighet](admin-classifying-data-sensitivity.md).  

## <a name="types-of-requests"></a>Typer av begäranden

Följande tabell innehåller exempel på olika typer av förfrågningar som du kan svara på.

> [!Note]
> Även om vi tillhandahåller funktioner för att svara på den här typen av begäran och därmed erbjuder tillgång till personuppgifter, så är det ditt ansvar att se till att personliga och känsliga data finns och klassificeras på rätt sätt.

|Förfrågan – typ|Beskrivning och föreslagna svar|
|-----|-----|
|Begäranden för portabilitet|Ett datasubjekt kan göra en begäran om dataportabilitet, vilket bland annat betyder att man måste exportera datasubjektets personuppgifter från ditt system och tillhandahålla dem i ett strukturerat format som ofta används. Om du vill svara på förfrågningarna använder du **Verktyg för datasekretess** för att exportera personuppgifter till en Excel-fil eller ett RapidStart-konfigurationspaket. Med Excel kan du redigera personuppgifterna och spara dem i ett format som används ofta och som är maskinläsbart, som CSV- eller XML. För RapidStart-konfigurationspaket kan du konfigurera huvuddatatabeller och relaterade tabeller som innehåller personuppgifter. <br><br> **Obs!** när du exporterar data anger du en lägsta känslighetsnivå. Exporten omfattar minsta och alla känslighetsnivåer ovanför. Till exempel om du vill exportera data som klassificeras som personliga omfattar även exporten data som klassificeras som känsliga data. <br><br>När du exporterar data för den registrerade, letar **Verktyg för datasekretess** efter direkta relationer mellan den registrerade och data som är relaterad till den berörda personen. Indirekta samband mellan data som är relaterade till den berörda personen och övriga data exporteras inte automatiskt av **Verktyg för datasekretess**. Exempelvis tabellen Kontakt innehåller en direkt relaterad Kontaktprofilsvarsdata och tabellen Kontaktprofilsvar är information som rör data från profilfrågor. Om du vill exportera profilfrågor måste du också lägga till den här tabellen manuellt som en rad med lämpliga filter i konfigurationspaketet som **Verktyg för datasekretess** skapar.|
|Begäranden om borttagning|En person kan begära att du tar bort deras personuppgifter. Det finns flera sätt att ta bort personlig information med hjälp av anpassningsfunktionerna, men du bär ansvaret för beslut och genomförande. I vissa fall kan du välja att redigera data direkt, till exempel ta bort en kontakt och sedan köra batch-jobbet Ta bort avbruten för att ta bort interaktioner för kontakten. <br><br> **Obs:** Om du har angett ett datum i fältet **Dokumentet kan tas bort före** på sidan **Försäljningsinställningar** eller **Inköpsinställningar** sidor kan du behöva ändra datumet så att du kan ta bort bokförda försäljnings- och inköpsdokument som du har skrivit ut och som har bokföringsdatum som infaller på eller före detta datum.|
|Begäranden om rättning|En person kan begära att du korrigerar felaktiga personuppgifter. Detta kan göras på olika sätt. I vissa fall kan du exportera listor till Excel för att snabbt massredigera flera poster och sedan importera den uppdaterade informationen. Mer information finns i [Exportera dina affärsdata till Excel](about-export-data.md). Du kan även manuellt redigera fält som innehåller personuppgifter, till exempel redigera information om en kund på kundkortet. Transaktionsposter som till exempel Allmänt, Kund och Redovisning av skattetransaktioner är emellertid nödvändiga för integriteten i företagets resursplaneringssystem. Om du lagrar personuppgifter i affärstransaktionsposter, överväg då att du använda anpassningsfunktionerna för att ändra dessa personuppgifter.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Begränsa databearbetning för datasubjekt
Ett datasubjekt kan begära att du tillfälligt slutar bearbeta deras personuppgifter. Om du vill tillgodose en sådan begära, kan du markera posten som blockerad av sekretesskäl i syfte att sluta bearbeta deras data. När en post har markerats som spärrad kan du inte skapa nya transaktioner som använder posten. Du kan till exempel inte skapa en ny faktura för en kund när antingen kunden eller säljaren är spärrad. För att markera ett datasubjekt som blockerat. öppna datasubjektets kort, till exempel kund-, leverantörs- eller kontaktkort, och välj kryssrutan **Sekretessblockerad**. Du kan behöva välja **Visa fler** för att visa fältet.  

## <a name="handling-data-subject-requests-while-in-trial"></a>Hantera begäranden av registrerade i test
Vissa typer av personuppgifter ingår i ditt Microsoft 365-konto och kräver administrativ behörighet för att exportera om du får en begäran om persondata från en användare för den här typen av personuppgifter enligt allmänna dataskyddsförordningen (GDPR). Processen för att hantera begäranden från registrerade är olika beroende på vilken typ av [!INCLUDE[prod_short](includes/prod_short.md)]-innehavare.  

Om du har en betald prenumeration för [!INCLUDE[prod_short](includes/prod_short.md)], måste du kontakta företagets innehavaradministratör om du vill göra en registrerades begäran. Administratören har administratörsrättigheter och verktygen för att uppfylla begäran.  

Om du har registrerat dig för [!INCLUDE[prod_short](includes/prod_short.md)] från de [test](https://trials.dynamics.com/), och du inte har flyttat från denna testversion till en betald prenumeration av administratörsinnehavare och du kan uppfylla en registrerades begäran i [Arbets- och skolsekretess i Azure -portalen](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade). Här kan du exportera och hämta dina personuppgifter.

Du kan avsluta ditt konto på sidan Arbete- och skolsekretess och du kan även avsluta ditt konto. Vi rekommenderar emellertid att du ser till att du har exporterat och tagit bort alla data först eftersom om du tar bort ditt konto förlorar du åtkomst till [!INCLUDE[prod_short](includes/prod_short.md)].  

Du kan fortfarande markera personer som blockerats på grund av sekretess- och export, redigera eller ta bort transaktioner enligt beskrivningen på annat ställe i den här artikeln.  

## <a name="exporting-data-from-tables-not-classified-by-data-subject"></a>Exportera Data från tabeller som inte klassificeras av registrerade
Om det finns en situation där du måste exportera data som inte klassificeras på ett sätt så att den exporteras automatiskt, till exempel data från tabellen profilsvar måste du göra följande:
-   Beakta om du verkligen vill eller behöver exportera dessa ytterligare data som inte är relaterad till kontakten, vilket innebär att den har någon direkt inverkan på den
-   Lägg till den här tabellen och relationen manuellt till snabbstartpaketet och exportera direkt från snabbstartpaketet – det är därför vi skapar ett snabbstartpaketet åt dig, så att du kan ändra den i situationer som den här.

## <a name="handling-data-about-minors"></a>Hantera data om minderåriga
Om en kontaktperson ålder understiger åldern för juridiskt godkännande enligt lagstiftningen i din region, anger du detta genom att välja kryssrutan **Minderårig** på kortet **Kontakt**. När du gör detta väljs kryssrutan **Sekretessblockerad** automatiskt. När du får samtycke från minderårigs förälder eller vårdnadshavare kan du välja kryssrutan **Föräldrarnas samtycke mottaget** om du vill låsa upp kontakten. Även om du kan behandla personuppgifter för minderåriga kan du inte använda profileringsfunktionen i Dynamics 365 Sales.

> [!Note]
> Ändringsloggen kan registrera information som till exempel när och av vem kryssrutan **Föräldrarnas samtycke mottaget** har valts. En administratör kan konfigurera detta genom att välja guiden **Ändra logginställning** och även välja kryssrutan **Loggändringar för föräldrars samtycke har mottagits** på kortet **Kontakt**. Mer information finns i [Logga ändringar](across-log-changes.md).  

## <a name="see-also"></a>Se även
[Klassificering av Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Klassificera datakänslighet](admin-classifying-data-sensitivity.md)  
[Exportera dina affärsdata till Excel](about-export-data.md)  
[Logga ändringar](across-log-changes.md)  
[Registrerades begäran för GDPR](/microsoft-365/compliance/gdpr-data-subject-requests)  


[!INCLUDE[footer-include](includes/footer-banner.md)]