---
title: Raddefinitioner i ekonomiska rapporter
description: Beskriver hur raddefinitioner i ekonomiska rapporter fungerar.
author: kennieNP
ms.author: kepontop
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# <a name="row-definitions-in-financial-reporting"></a>Raddefinitioner i ekonomiska rapporter

Raddefinitioner i ekonomiska rapporter är en plats för beräkningar som inte kan göras direkt i kontoplanen. Du kan t. ex. skapa delsummor för grupper av konton och sedan ta med denna summa i andra summor. Du kan också beräkna mellanliggande steg som inte visas i slutrapporten.

## <a name="create-or-edit-a-row-definition"></a>Skapa eller redigera en raddefinition

Följ dessa steg för att skapa eller redigera en raddefinition:

1. På sidan **Ekonomiska rapporter** väljer du den relevanta ekonomiska rapporten och väljer sedan åtgärden **Redigera raddefinition**.
1. Välj åtgärderna **Infoga redovisningskonton**, **Infoga kassaflödeskonton** och **Infoga kostnadstyper** för att skapa en rad för varje ekonomiskt element som du vill analysera. Du kan till exempel ha en rad för omsättningstillgångar och en annan rad för anläggningstillgångar. För inspiration, utforska ekonomiska rapporter i demonstrationsföretaget CRONUS.

    > [!NOTE]
    > **Radnr.** fältet visar de första 10 tecknen i en identifierare, t.ex. ett kontonummer. Om du lägger till element med identifierare som börjar med samma tio tecken kommer du att ha dubbletter i fältet **Radnr.** . Om det behövs kan du redigera identifierare manuellt när du har infogat elementen. Alla identifierare visas i fältet **Summeringsintervall** .

> [!NOTE]
> Kolumnerna som du anger på varje rad i raddefinitionen representerar kolumnerna tre och uppåt på sidan **Ekonomisk rapport**. De två första kolumnerna **Radnr** och **beskrivning** korrigeras.  

## <a name="built-in-row-definitions"></a>Inbyggda raddefinitioner

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller exempel på raddefinitioner som hjälper dig att snabbt komma igång med att skapa ekonomirapporter som passar dina behov.

<!-- update this when we release the new templates in 24.1
| Row definition code | Description | How to use this row definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 | 
-->

> [!NOTE]
> De ekonomiska exempelrapporterna i [!INCLUDE[prod_short](includes/prod_short.md)] är inte färdiga att användas direkt. Beroende på hur du konfigurerar redovisningskonton, dimensioner, redovisningskontokategorier och budgetar måste du justera exempelrad- och kolumndefinitionerna och de ekonomiska rapporter som de används i så att de matchar dina inställningar.

## <a name="use-gl-account-categories-to-change-the-layout-of-your-financial-statements"></a>Använda kontokategorier för att ändra layout på din redovisning

Du kan använda kontokategorier för att ändra layout på din redovisning. När du har upprättat dina kontokategorier på sidan **Redovisningskontokategorier** kan du välja åtgärden **Skapa ekonomiska rapporter** och uppdatera de underliggande ekonomiska rapporterna för de centrala ekonomiska rapporterna. Nästa gång du kör någon av dessa rapporter, till exempel rapporten **Kontoavstämning** kommer nya summor och underposter att läggas till.

En annan fördel med att använda redovisningskontokategorier framför de råa redovisningskontona i raddefinitionerna är att en ändring i kontoplanens struktur inte påverkar de ekonomiska rapporterna.

> [!NOTE]
> Kontokategorierna på den högsta nivån, till exempel noden **Skulder**, är fasta och du kan inte lägga till egna. Du kan emellertid ta bort och lägga till kontokategorier på lägre nivåer och definiera hur den relaterade ekonomiska rapporten ska visas i rapporter.
>
> Du bör skapa och strukturera egna redovisningskontokategorier från grunden, i en hierarki vid behov, i stället för att försöka omarrangera de befintliga. Du kan t. ex. strukturera om **Skulder** så att de innehåller en nod **Eget kapital** följ **Kortfristiga skulder** och **Långfristiga skulder**. Läs mer i [Mappa redovisningskonton till kontokategorier](finance-general-ledger.md#account-categories).

## <a name="best-practices-for-working-with-row-definitions"></a>Metodtips för att arbeta med raddefinitioner

Raddefinitioner versionshanteras inte. När du ändrar en raddefinition ersätts den gamla versionen när ändringen sparas i databasen. Följande lista innehåller några metodtips för hur du arbetar med raddefinitioner:

- Om du lägger till raddefinitioner väljer du en bra kod och fyller i beskrivningsfältet med en meningsfull text samtidigt som du vet vad du använder raddefinitionen till. Den här informationen hjälper dina medarbetare (och ditt framtida jag) att arbeta med ekonomiska rapporter och kanske ändra raddefinitionen.
- Innan du ändrar en raddefinition bör du överväga att ta en kopia av den som säkerhetskopia, ifall ändringen inte fungerar som förväntat. Du kan antingen bara kopiera definitionen (ge den ett bra namn) eller exportera den. För mer information går du till [Importera eller exportera raddefinitioner](#import-or-export-financial-reporting-row-definitions).
- Om du behöver en ny kopia av en definition som [!INCLUDE[prod_short](includes/prod_short.md)] tillhandahåller är ett enkelt sätt att skapa ett nytt företag som bara innehåller inställningsdata. Exportera sedan definitionen och importera den till det företag där definitionen behöver uppdateras.

## <a name="import-or-export-financial-reporting-row-definitions"></a>Importera eller exportera raddefinitioner för ekonomiska rapporter

Du kan importera och exportera raddefinitioner som RapidStart-konfigurationspaket. Till exempel är konfigurationspaket användbara för att dela information med andra företag. Paketet skapas i en .rapidstart-fil, vilket komprimerar innehållet.

> [!NOTE]
> När du importerar raddefinitioner för ekonomiska rapporter kommer befintliga poster som har samma namn som de som importeras att bytas ut med de nya definitionerna. Konfigurationspaketet för en rapportdefinition skriver inte över befintliga rad- eller kolumndefinitioner som används i rapportdefinitionen.

Så här importerar eller exporterar du raddefinitioner för ekonomiska rapporter:

1. Välj ![glödlampan som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Raddefinitioner** och välj relaterad länk.
1. Välj raddefinition och välj sedan åtgärden **Importera raddefinition** eller **Exportera raddefinition**, beroende på vad du vill göra.

## <a name="see-also"></a>Se även

[Kolumndefinitioner i ekonomiska rapporter](bi-column-definitions.md)  
[Förbereda ekonomisk rapportering](bi-how-work-account-schedule.md)  
[Ekonomisk business intelligence](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
