---
title: Revision av ändringar
description: Du kan aktivera en användarlogg så att du har en historik över alla ändringar som gjorts i spårade tabeller. Du kan även spåra aktiviteter med vissa typer av aktivitetsloggar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 05/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="auditing-changes"></a>Revision av ändringar

En vanlig utmaning i många affärshanteringsprogram är att undvika oönskade ändringar i data. Det kan vara allt från ett felaktigt kundtelefonnummer till en felaktig bokföring i redovisningen. I den här artikeln beskrivs möjligheterna att ta reda på vad som har förändrats, vem som ändrat det och när ändringen gjordes.

## <a name="about-the-change-log"></a>Om ändringsloggen

Med ändringsloggen kan du spåra alla direkta ändringar som användare gör av data i databasen. Du anger vad du vill att systemet ska logga för varje tabell och fält och därefter måste du aktivera ändringsloggen. Ändringsloggen är baserad på ändringar av data i tabeller som du spårar. På sidan **Poster i ändringslogg** sorteras poster kronologiskt och visar alla ändringar som har gjorts av värden i fälten i de tabeller du anger.

Spårningsändringarna kan påverka prestanda, vilket kan ta tid och öka databasens storlek, vilket kostar pengar. För att minska dessa kostnader ha följande i åtanke:

- Var noggrann när du väljer tabeller och åtgärder.
- Lägg inte till transaktioner och bokförda dokument. Prioritera i stället systemfält som Skapades av och Skapades den.
- Använd inte spårningstypen **Alla fält**. Välj i stället **Vissa fält** och spåra bara de viktigaste fälten.

> [!NOTE]
> Ändringsloggen spårar inte ändringar för fält som använder `autoIncrement property`. Ett exempel på ett fält där egenskapen används är fältet Heltal i tabellerna Felmeddelanden och Momsrapportrad.

Av prestandaskäl inaktiveras ändringsloggen vid uppgraderingen av [!INCLUDE [prod_short](includes/prod_short.md)] till nästa version. Förutom att snabba på uppgraderingsprocessen minskas också oredan i ändringsloggen om du stänger av loggen. Så snart uppgraderingen är klar börjar loggningen spåra ändringar igen.

> [!Important]
> Ändringar visas endast i **Poster i ändringslogg** när användarens session har startats om, vilket inträffar på följande sätt:
>
> - Sessionen har upphört att gälla och har uppdaterats.
> - Användaren valde ett annat företag eller rollcenter.
> - Användaren loggade ut och loggade in igen.

## <a name="setting-up-the-change-log"></a>Ställer in ändringslogg

På sidan **Ändringslogginställningar** kan du aktivera eller inaktivera ändringsloggen. När du gör det loggas aktiviteten så att du alltid kan se vem som har gjort ändringen.

På sidan **Ändringslogginställningar** om du väljer åtgärden **Tabeller** kan du ange vilka tabeller som du vill spåra ändringar för och vilka ändringar som ska spåras. [!INCLUDE[prod_short](includes/prod_short.md)] spårar också flera systemtabeller.

> [!NOTE]
> Du kan övervaka specifika fält för ändringar, till exempel fält som innehåller känslig information, genom att skapa fältövervakning. Om du gör undviks redundans genom att tabellen som innehåller fältet inte är tillgänglig för konfigurationen av ändringslogg. Mer information finns i [Övervaka känsliga fält](across-log-changes.md#monitor-sensitive-fields).

När du har skapat ändringsloggen och aktiverat den, och gjort en ändring av data, kan du visa och filtrera ändringen på sidan **Ändringsloggtransaktioner**. Om du vill ta bort poster skapar du en kvarhållningsprincip där du kan ange filter som baseras på datum och tid. Mer information om kvarhållningsprinciper i [Definiera kvarhållningsprincip](admin-data-retention-policies.md).  

## <a name="analyze-data-in-the-change-log"></a>Analysera data i ändringsloggen

Du kan använda funktionen **Dataanalys** för att analysera data i ändringsloggen från sidan [Ändringsloggtransaktioner](https://businesscentral.dynamics.com/?page=595). Du behöver inte köra en rapport eller öppna till ett annat program, till exempel Excel. Funktionen ger ett interaktivt och mångsidigt sätt att beräkna, sammanfatta och undersöka data. I stället för att köra rapporter med alternativ och filter kan du lägga till flera flikar som representerar olika uppgifter eller vyer för informationen. Några exempel är "Vem ändrade vilka data och när" eller "Data ändras efter tabell/fält" eller någon annan vy du kan tänka dig. Mer information om hur du använder funktionen **Dataanalys** finns i [Analysera lista och frågedata med analysläge](analysis-mode.md).

### <a name="change-log-ad-hoc-analysis-scenarios"></a>Ändra scenarier för logga ad hoc-analys

Följande avsnitt innehåller exempel på scenarier där analys av ändringsloggen kan hjälpa dig att övervaka och granska viktiga ändringar.

| Yta | Till... | Öppna sidan i analysläge | Använda dessa fält |
| ---- | ----- | ------------------------------- |------------------- |
| [Vem ändrade vilka data och när](#example-who-changed-what-data-and-when) | Se vem som ändrade vilka data. | [Poster i ändringslogg](https://businesscentral.dynamics.com/?page=595) | **Användar-ID**, **Datum och tid**, **Tabellrubrik**, **Fältrubrik**, **Primärnyckelvärde 2**, **Primärnyckelvärde 3**, **Typ av ändring**, **Gammalt värde** och **Nytt värde**. |
| [Dataändringar efter tabell/fält](#example-data-changes-by-tablefield) | Visa dataändringar per tabell/fält och vem som har gjort ändringen. | [Poster i ändringslogg](https://businesscentral.dynamics.com/?page=595) | **Tabellrubrik**, **Fältrubrik**, **Användar-ID**, **Datum och tid**, **Primärnyckelvärde 2**, **Primärnyckelvärde 3**, **Typ av ändring**, **Gammalt värde** och **Nytt värde**. |

### <a name="example-who-changed-what-data-and-when"></a>Exempel: Vem ändrade vilka data och när

Så här analyserar du Vem som ändrade vilka data när:

1. Öppna listan [Ändringsloggtransaktioner](https://businesscentral.dynamics.com/?page=595) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: ikon för att aktivera analysläget.
1. På menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet** till höger).
1. Dra fältet **Användar-ID** (vem som gjorde det) till området **Radgrupper**.
1. Välj nu följande fält:
   - Om du vill visa när det hände väljer du **Datum och tid**.
   - Om du vill visa tabellen var det hände väljer du **Tabellrubrik**. 
   - Om du vill visa vilket fält väljer du **Fältrubrik**.
   - Om du vill visa fältkoden väljer du **Primärnyckelvärde 2**. 
   - Om du vill visa företagsnamnet väljer du **Primärnyckelvärde 3**.
   - Välj **Typ av ändring** om du vill visa om ändringen var en infognings-, uppdaterings- eller borttagningsåtgärd.
   - Om du vill visa ändringen väljer du **Gammalt värde** och **Nytt värde**.
1. Byt namn på analysfliken till **Vem ändrade vilka data och när** eller något som beskriver den här analysen.

Följande bild visar resultatet av de här stegen.

:::image type="content" source=" media/data-analysis-change-log-entries-Who-changed-What-data-When.png" alt-text="Exempel på hur du gör dataanalyser på sidan Ändringsloggtransaktioner (Vem ändrade vilka data när)." lightbox="media/data-analysis-change-log-entries-Who-changed-What-data-When.png":::

### <a name="example-data-changes-by-tablefield"></a>Exempel: Dataändringar efter tabell/fält

Så här analyserar du dataändringar per tabell/fält:

1. Öppna listan [Ändringsloggtransaktioner](https://businesscentral.dynamics.com/?page=595) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: ikon för att aktivera analysläget.
1. På menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet** till höger).
1. Dra fälten **Tabellrubrik** (i vilken tabell) och **Fältrubrik** (i vilket fält) till området **Radgrupper**.
1. Välj nu följande fält:
   - Om du vill visa när det hände väljer du **Datum och tid**
   - Om du vill visa vem som har gjort ändringen väljer du **Användar-ID**.
   - Om du vill visa koden för fältet väljer du **Primärnyckelvärde 2**.
   - Om du vill visa företagsnamnet väljer du **Primärnyckelvärde 3** (vanligtvis företagets namn), 
   - Välj **Typ av ändring** om du vill visa om ändringen var en infognings-, uppdaterings- eller borttagningsåtgärd.
   - Om du vill visa ändringen väljer du **Gammalt värde** och **Nytt värde**.
1. Byt namn på analysfliken till **Dataändringar efter tabell + fält** eller något som beskriver den här analysen.

Följande bild visar resultatet av de här stegen.

:::image type="content" source=" media/data-analysis-change-log-entries-data-changes-by-table-field.png" alt-text="Exempel på hur du gör dataanalyser på sidan Ändringsloggtransaktioner (dataändringar efter tabell/fält)." lightbox="media/data-analysis-change-log-entries-data-changes-by-table-field.png":::

## <a name="about-activity-logs"></a>Om aktivitetsloggar

På vissa sidor i [!INCLUDE [prod_short](includes/prod_short.md)] kan du visa en aktivitetslogg som visar status och eventuella fel från filer som du exporterar från eller importerar till [!INCLUDE [prod_short](includes/prod_short.md)].  

### <a name="work-with-activity-logs"></a>Arbeta med aktivitetsloggar

Informationen visas på sidan **Aktivitetslogg** enligt kontexten du öppnade den från. Du kan till exempel öppna sidan från sidorna **Inställning av dokumentutbytestjänst**, **Inkommande dokument**, **Bokförd försäljningsfaktura** och **Bokförd försäljningskreditnota**. Du kan tömma listan över loggposter eller bara rensa listan över poster som är äldre än sju dagar.  

## <a name="monitor-sensitive-fields"></a>Övervaka känsliga fält

Att hålla känslig information säker och privat är en grundläggande angelägenhet för de flesta företag. Om du vill lägga till ett säkerhetsskikt kan du övervaka viktiga fält och meddelas via e-post när någon ändrar ett värde. Du kanske till exempel vill få ett meddelande om någon ändrar IBAN-numret för ditt företag.

> [!NOTE]
> Om du vill skicka meddelanden via e-post måste du ställa in e-postfunktionen i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Konfigurera e-post](admin-how-setup-email.md).

### <a name="set-up-field-monitoring"></a>Konfigurera fältövervakning

Du kan använda guiden **Konfigurera övervakning av fältändringar** för assisterad konfiguration för att ange vilka fält du vill övervaka baserat på filterkriterier, till exempel klassificering av datakänslighet för fälten. Mer information finns i [Klassificera datakänslighet](admin-classifying-data-sensitivity.md). Med guiden kan du också ange vilken person som ska få ett e-postmeddelande när en ändring sker och vilket e-postkonto som ska användas för att skicka e-postmeddelandet. Du måste ange både användarmeddelandet och kontot som meddelandet ska skickas från. När du har slutfört guiden kan du hantera inställningarna för fältövervakning på sidan **Konfigurera fältövervakning**.

> [!NOTE]
> När du anger vilket e-postkonto du vill skicka meddelanden från måste du lägga till kontotypen **Microsoft 365** eller **SMTP**. Meddelanden ska skickas från ett konto som inte är associerat med en faktisk användare. Därför kan du inte välja **aktuell användare** kontotyp. Om du gör det kommer meddelandena inte att skickas.

Med tiden kommer listan över poster på sidan **Poster i loggen med övervakade fält** att växa. Om du vill minska antalet poster kan du skapa en bevarandeprincip som tar bort poster efter en viss tidsperiod. Mer information finns i [Definiera bevarandeprinciper](admin-data-retention-policies.md).

När du ställer in fältövervakning, eller ändrar någonting i inställningarna, skapas poster för dina ändringar. Du kan ange om du vill visa poster som är relaterade till övervakningsinställningarna genom att visa eller dölja dem.

Du kan hantera inställningar för fältövervakning, t. ex. om ett e-postmeddelande ska skickas eller om ändringar bara ska loggas, för varje fält på sidan **Kalkylark med övervakade fält**. Du kan också lägga till eller ta bort fält för övervakning på sidan.

> [!NOTE]
> När du har lagt till ett eller flera fält och startat övervakning måste du logga ut från [!INCLUDE[prod_short](includes/prod_short.md)] och logga in igen för att tillämpa inställningarna.

### <a name="work-with-field-monitoring"></a>Arbeta med fältövervakning

Poster för alla ändrade värden för övervakade fält är tillgängliga på sidan **Poster i loggen med övervakade fält**. Ange till exempel följande information:

- Det fält som värdet ändrades för.
- De ursprungliga och nya värdena.
- Som gjorde ändringen och när de gjorde det.

Om du vill granska en ändring ytterligare kan du välja ett värde för att öppna sidan där den gjordes. Om du vill se en lista över alla poster väljer du **Poster för fältändringar**.

### <a name="view-field-monitoring-telemetry"></a>Visa telemetri för fältövervakning

Du kan konfigurera [!INCLUDE[prod_short](includes/prod_short.md)] för att skicka fältövervakningsaktiviteter till en Application Insights-resurs i Microsoft Azure. Med hjälp av Azure Monitor kan du sedan skapa rapporter och aviseringar för insamlade data. Mer information finns i följande artiklar i [!INCLUDE[prod_short](includes/prod_short.md)]-hjälpen för utvecklare och IT-proffs:

- [Övervaka och analysera telemetri – Aaktivera Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview?toc=/dynamics365/business-central/toc.json#enable)
- [Analysera telemetri för fältövervakning](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)

## <a name="define-retention-policies"></a>Definiera bevarandeprinciper

Du kan skapa bevarandeprinciper för att ta bort data som inte behövs i loggarna efter en tidsperiod som du anger. Till exempel kan antalet poster i en logg ökas med tiden. Genom att rensa bort gamla poster kan du göra det enklare att fokusera på nyare, och troligen mer relevanta, poster. Mer information om kvarhållningsprinciper i [Definiera kvarhållningsprincip](admin-data-retention-policies.md).

## <a name="see-also"></a>Se även

[Övervaka känsliga fält](across-log-changes.md#monitor-sensitive-fields)  
[Analysera telemetri för fältövervakning](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)  
[Definiera kvarhållningsprinciper](admin-data-retention-policies.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Sortera, söka och filtrera](ui-enter-criteria-filters.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Tilldela användare och grupper behörigheter](ui-define-granular-permissions.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
