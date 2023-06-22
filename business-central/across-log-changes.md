---
title: Revision av ändringar
description: Du kan aktivera en användarlogg så att du har en historik över alla ändringar som gjorts i spårade tabeller. Du kan även spåra aktiviteter med vissa typer av aktivitetsloggar.
author: edupont04
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 03/24/2022
ms.author: edupont
---
# <a name="auditing-changes-in-business-central" />Revision av ändringar i Business Central

En vanlig utmaning i många affärshanteringsprogram är att undvika oönskade ändringar i data. Det kan vara allt från ett felaktigt kundtelefonnummer till en felaktig bokföring i redovisningen. I det här avsnittet beskrivs möjligheterna att ta reda på vad som har förändrats, vem som ändrat det och när ändringen gjordes.

## <a name="about-the-change-log" />Om ändringsloggen

Med ändringsloggen kan du spåra alla direkta ändringar som användare gör av data i databasen. Du anger vad du vill att systemet ska logga för varje tabell och fält och därefter måste du aktivera ändringsloggen. Ändringsloggen är baserad på ändringar av data i tabeller som du spårar. På sidan **Poster i ändringslogg** sorteras poster kronologiskt och visar alla ändringar som har gjorts av värden i fälten i de tabeller du anger. 

Spårningsändringarna kan påverka prestanda, vilket kan ta tid och öka databasens storlek, vilket kostar pengar. För att minska dessa kostnader ha följande i åtanke:

- Var noggrann när du väljer tabeller och åtgärder.
- Lägg inte till transaktioner och bokförda dokument. Prioritera i stället systemfält som Skapades av och Skapades den.
- Använd inte spårningstypen Alla fält. Välj i stället Vissa fält och spåra bara de viktigaste fälten.

Av prestandaskäl inaktiveras ändringsloggen vid uppgraderingen av [!INCLUDE [prod_short](includes/prod_short.md)] till nästa version. Förutom att snabba på uppgraderingsprocessen minskas också oredan i ändringsloggen. Så snart uppgraderingen är klar börjar loggningen spåra ändringar igen.

> [!Important]
> Ändringar visas endast i **Poster i ändringslogg** när användarens session har startats om, vilket inträffar på följande sätt:
>
> * Sessionen har upphört att gälla och har uppdaterats.
> * Användaren valde ett annat företag eller rollcenter.
> * Användaren loggade ut och loggade in igen.

### <a name="work-with-the-change-log" />Arbeta med ändringsloggen
Du aktiverar och avaktiverar ändringsloggen på sidan **Ändringslogg inställning**. När en användare aktiverar eller inaktiverar ändringsloggen, loggas denna aktivitet så du kan alltid se vilken användare som har inaktiverat respektive återaktiverat ändringsloggen.

På sidan **Ändringslogginställningar** om du väljer åtgärden **Tabeller** kan du ange vilka tabeller som du vill spåra ändringar för och vilka ändringar som ska spåras. [!INCLUDE[prod_short](includes/prod_short.md)] spårar också flera systemtabeller.

> [!NOTE]
> Du kan övervaka specifika fält för ändringar, till exempel fält som innehåller känslig information, genom att skapa fältövervakning. Om du gör undviks redundans genom att tabellen som innehåller fältet inte är tillgänglig för konfigurationen av ändringslogg. Mer information finns i [Övervaka känsliga fält](across-log-changes.md#monitoring-sensitive-fields).

När du har skapat ändringsloggen och aktiverat den, och gjort en ändring av data, kan du visa och filtrera ändringen på sidan **Ändringslogg transaktioner**. Om du vill ta bort transaktioner kan du göra det på sidan **ta bort ändringsloggtransaktioner**, där du kan ange filter baserat på datum och tider.  

## <a name="about-activity-logs" />Om aktivitetsloggar

På vissa sidor i [!INCLUDE [prod_short](includes/prod_short.md)] kan du visa en aktivitetslogg som visar status och eventuella fel från filer som du exporterar från eller importerar till [!INCLUDE [prod_short](includes/prod_short.md)].  

### <a name="work-with-activity-logs" />Arbeta med aktivitetsloggar
Informationen visas på sidan **Aktivitetslogg** enligt kontexten den öppnas från. Du kan till exempel öppna sidan från sidorna **Inställning av dokumentutbytestjänst**, **Inkommande dokument**, **Bokförd försäljningsfaktura** och **Bokförd försäljningskreditnota**. Du kan tömma listan över loggposter eller bara rensa listan över poster som är äldre än sju dagar.  

## <a name="monitoring-sensitive-fields" />Övervaka känsliga fält

Att hålla känslig information säker och privat är en grundläggande angelägenhet för de flesta företag. Om du vill lägga till ett säkerhetsskikt kan du övervaka viktiga fält och meddelas via e-post när någon ändrar ett värde. Du kanske till exempel vill få ett meddelande om någon ändrar IBAN-numret för ditt företag.

> [!NOTE]
> Om du vill skicka meddelanden via e-post måste du ställa in e-postfunktionen i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Konfigurera e-post](admin-how-setup-email.md).

### <a name="setting-up-field-monitoring" />Konfigurera fältövervakning

Du kan använda guiden **Konfigurera övervakning av fältändringar** för assisterad konfiguration för att ange vilka fält du vill övervaka baserat på filterkriterier, till exempel klassificering av datakänslighet för fälten. Mer information finns i [Klassificera datakänslighet](admin-classifying-data-sensitivity.md). Med guiden kan du också ange vilken person som ska få ett e-postmeddelande när en ändring sker och vilket e-postkonto som ska användas för att skicka e-postmeddelandet. Du måste ange både användarmeddelandet och kontot som meddelandet ska skickas från. När du har slutfört guiden kan du hantera inställningarna för fältövervakning på sidan **Konfigurera fältövervakning**. 

> [!NOTE]
> När du anger vilket e-postkonto du vill skicka meddelanden från måste du lägga till kontotypen **Microsoft 365** eller **SMTP**. Meddelanden ska skickas från ett konto som inte är associerat med en faktisk användare. Därför kan du inte välja **aktuell användare** kontotyp. Om du gör det kommer meddelandena inte att skickas. 

Med tiden kommer listan över poster på sidan **Poster i loggen med övervakade fält** att växa. Om du vill minska antalet poster kan du skapa en bevarandeprincip som tar bort poster efter en viss tidsperiod. Mer information finns i [Definiera bevarandeprinciper](admin-data-retention-policies.md).

När du ställer in fältövervakning, eller ändrar någonting i inställningarna, skapas poster för dina ändringar. Du kan ange om du vill visa poster som är relaterade till övervakningsinställningarna genom att visa eller dölja dem. 

Du kan hantera inställningar för fältövervakning, t. ex. om ett e-postmeddelande ska skickas eller om ändringar bara ska loggas, för varje fält på sidan **Kalkylark med övervakade fält**. Du kan också lägga till eller ta bort fält för övervakning på sidan.

> [!NOTE]
> När du har lagt till ett eller flera fält och startat övervakning måste du logga ut från [!INCLUDE[prod_short](includes/prod_short.md)] och logga in igen för att tillämpa inställningarna.

### <a name="work-with-field-monitoring" />Arbeta med fältövervakning

Poster för alla ändrade värden för övervakade fält är tillgängliga på sidan **Poster i loggen med övervakade fält**. Ange till exempel följande information:

* Det fält som värdet ändrades för.
* De ursprungliga och nya värdena.
* Som gjorde ändringen och när de gjorde det. 

Om du vill granska en ändring ytterligare kan du välja ett värde för att öppna sidan där den gjordes. Om du vill se en lista över alla poster väljer du **Poster för fältändringar**.

### <a name="viewing-field-monitoring-telemetry" />Visa telemetri för fältövervakning

Du kan konfigurera [!INCLUDE[prod_short](includes/prod_short.md)] för att skicka fältövervakningsaktiviteter till en Application Insights-resurs i Microsoft Azure. Med hjälp av Azure Monitor kan du sedan skapa rapporter och aviseringar för insamlade data. Mer information finns i följande artiklar i [!INCLUDE[prod_short](includes/prod_short.md)]-hjälpen för utvecklare och IT-proffs:

- [Övervaka och analysera telemetri – Aaktivera Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analysera telemetri för fältövervakning](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace)

## <a name="defining-retention-policies" />Definiera bevarandeprinciper

Du kan skapa bevarandeprinciper för att ta bort data som inte behövs i loggarna efter en tidsperiod som du anger. Till exempel kan antalet poster i en logg ökas med tiden. Genom att rensa bort gamla poster kan du göra det enklare att fokusera på nyare, och troligen mer relevanta, poster. Mer information finns i [Definiera bevarandeprinciper](admin-data-retention-policies.md).

## <a name="see-also" />Se även

[Ändra grundinställningar](ui-change-basic-settings.md)  
[Sortera, söka och filtrera](ui-enter-criteria-filters.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definiera bevarandeprinciper](admin-data-retention-policies.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
