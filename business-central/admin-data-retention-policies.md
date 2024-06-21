---
title: Rensa data med lagringsprinciper
description: Du kan ange hur ofta du vill ta bort vissa typer av data.
author: brentholtorf
ms.topic: conceptual
ms.author: bholtorf
ms.search.keywords: 'delete, data, retention, policy, policies'
ms.search.form: '3903, 3901'
ms.date: 12/15/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Definiera kvarhållningsprinciper

Denna artikel beskriver hur administratörer kan definiera kvarhållningsprinciper för att ange hur ofta de vill ta bort gamla data i tabeller som innehåller loggposter och arkiverade poster. Att rensa loggposter kan t. ex. göra det enklare för dig att arbeta med mer relevanta data. Policyer kan radera data baserat på ett utgångsdatum, eller så kan du lägga till filter som bara inkluderar vissa utgångna data.

## Nödvändiga konfigurationer och behörigheter

Innan du kan skapa kvarhållningsprinciper måste du ställa in tabellerna som ska inkluderas och tidsperioderna för att spara data.

|Konfigurera  |Beskrivning  |
|---------|---------|
|**Tillåtna tabeller**     |Vi tillhandahåller en lista över de tabeller som du kan inkludera i kvarhållningsprinciper. Om du vill lägga till tabeller från ett tillägg till en kvarhållningsprincip, måste utvecklaren lägga till tabellerna i listan. Mer information finns i [Inkludera tillägget i en kvarhållningsprincip](admin-data-retention-policies.md#include-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Kvarhållningsperioder**     |Ange tidsperioder för vilka data ska behållas i tabellerna i en princip. Perioderna bestämmer hur ofta data ska tas bort.         |

Dessutom måste du ha behörigheten **SUPER**-användare eller behörighetsuppsättningen **konfigurera kvarhållningsprincip**. Användare som har behörighetsuppsättningen konfigurera kvarhållningsprincip kan definiera kvarhållningsprinciper för tabeller. Det är sant, även om de inte har läs- och borttagningsbehörigheter för tabellerna. Projektköposten måste köras som en användare med behörighet att läsa och ta bort data. Bevilja inte behörighetsuppsättningen konfigurera kvarhållningsprincip till användare som inte bör tillåtas ta bort data.

> [!NOTE]
> Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt och vill prova att använda kvarhållningsprinciper i demonstrationsdatabasen Cronus, finns det några saker du måste göra. Demonstrationsföretaget innehåller inga tabeller som du kan använda med kvarhållningsprinciper, så du måste lägga till dem. Det gör du genom att skapa ett nytt, tomt företag i demonstrationsdatabasen. I det nya företaget importerar du konfigurationspaketet RapidStart för ditt land/din region som motsvarar standardpaketet NAV17.0.W1.ENU.STANDARD.rapidstart. Konfigurationsdata för kvarhållningsprinciper kommer att vara tillgängliga i det nya företaget.

### Skapa perioder för lagring

Du kan begränsa lagringsperioderna så länge du vill. Om du vill skapa lagringsperioder går du till sidan **kvarhållningsprinciper** och använder åtgärden **Lagringsperiod**. De perioder som du definierar är tillgängliga för alla policyer.

> [!NOTE]
> Vi har definierat en minsta lagringsperiod för vissa tabeller på grund av regelefterlevnad. Om du anger en lagringsperiod som är kortare än minimikravet visas ett meddelande om den obligatoriska perioden.

### Konfigurera en bevarandeprincip

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **kvarhållningsprinciper** och väljer sedan relaterad länk.
2. Välj tabellen som du vill ta med i principen i fältet **Tabell-ID**.
3. I fältet **Lagringsperiod** anger du hur länge informationen i tabellen ska bevaras.
4. Valfritt: Du kan tillämpa principen på specifika data i en tabell, snarare än alla poster, genom att filtrera data för varje rad. Policyn gäller endast för de poster som filtren returnerar. För att ange filterkriterierna, inaktivera växeln **Tillämpa på alla poster**. Snabbfliken **Post för kvarhållningsprincip** visas, där du kan ställa in filterkriterier. Om du vill lära dig mer om filter fungerar går du till [Filtrering](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Varje rad har sin egen lagringsperiod. Om du anger olika lagringsperioder för samma data används den längsta perioden. Vissa tabeller innehåller också filter som du inte kan ändra eller ta bort. För att identifiera dessa filter visas de i ett teckensnitt med ljusare färg.

#### Videovägledning

Den här videon ger ett exempel på hur du ställer in en kvarhållningsprincip.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fLeJ]

## Tillämpa kvarhållningsprinciper

Du kan använda en jobbköpost för att tillämpa kvarhållningsprinciper för att automatiskt ta bort data eller så kan du manuellt tillämpa principer.

Om du vill tillämpa en bevarandeprincip automatiskt skapar och aktiverar du bara en princip. När du aktiverar en princip skapar,, [!INCLUDE [prod_short](includes/prod_short.md)] en jobbköpost som tillämpar den enligt dess lagringsperiod. Alla kvarhållningsprinciper kommer att använda samma jobbköpost. Som standard tillämpar jobbköposten principen varje dag vid 0200. Du kan ändra standardvärdet, men om du gör det rekommenderar vi att det körs utanför kontorstid. Mer information finns i [Använda projektköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md). 

Du kan tillämpa en princip manuellt med hjälp av åtgärden **Tillämpa manuellt** på sidan **kvarhållningsprinciper**. Om du alltid vill tillämpa en princip manuellt aktiverar du reglaget **Manuellt**. Projektköposten ignorerar principen när den körs.

## Visa loggposter för kvarhållningsprincip

Du kan visa aktiviteter som är relaterade till kvarhållningsprinciper på sidan **Logg för bevarandeprincip**. Poster skapas t. ex. när en princip tillämpas, eller om fel uppstod.

## Inkludera tillägget i en kvarhållningsprincip (kräver hjälp från en utvecklare)

Som standard täcker kvarhållningsprinciperna endast [!INCLUDE[prod_short](includes/prod_short.md)] i listan vi tillhandahåller. Du kan ta bort standardtabeller från listan och du kan lägga till tabeller som du äger. Det innebär att du inte kan lägga till en tabell som du inte har skapat själv. Du kan till exempel inte lägga till andra tabeller från [!INCLUDE[prod_short](includes/prod_short.md)] eller från ett tillägg som du har köpt.

För att lägga till dina tabeller i listan över tillåtna tabeller måste en utvecklare lägga till lite kod. Till exempel till installationsprogrammets codeunit för tillägget (en codeunit med undertypen *installera* ).

När en utvecklare lägger till en tabell kan de ange obligatoriska filter och standardfilter. Obligatoriska filter kan inte tas bort eller ändras senare när du lägger till tabeller för att definiera en bevarandeprincip. Standardfilter är bara förslag.

Nedan följer exempel på hur du lägger till en tabell i listan över tillåtna tabeller med, och utan, obligatoriska filter eller standardfilter. Ett mer komplext exempel finns i codeunit 3999 "reten. Pol. Installera – BaseApp".

```al
 trigger OnInstallAppPerCompany()
    var
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
    begin
        RetenPolAllowedTables.AddAllowedTable(Database::"Retention Policy Log Entry");
    end;
```

I följande exempel finns ett obligatoriskt filter.

```al
 trigger OnInstallAppPerCompany()
    var
        ChangeLogEntry: Record "Change Log Entry";
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
        RetentionPeriod: Enum "Retention Period Enum";
        RecRef: RecordRef;
        TableFilters: JsonArray;
        Enabled: Boolean;
        Mandatory: Boolean;
    begin
        ChangeLogEntry.Reset();
        ChangeLogEntry.SetFilter("Field Log Entry Feature", '%1|%2', ChangeLogEntry."Field Log Entry Feature"::"Monitor Sensitive Fields", ChangeLogEntry."Field Log Entry Feature"::All);
        RecRef.GetTable(ChangeLogEntry);
        Enabled := true;
        Mandatory := true;
        RetenPolAllowedTables.AddTableFilterToJsonArray(TableFilters, RetentionPeriod::"28 Days", ChangeLogEntry.FieldNo(SystemCreatedAt), Enabled, Mandatory, RecRef);
        RetenPolAllowedTables.AddAllowedTable(Database::"Change Log Entry", ChangeLogEntry.FieldNo(SystemCreatedAt), TableFilters);
    end;
```

När en utvecklare har lagt till tabeller i listan kan en administratör inkludera dem i en bevarandeprincip. 

## Se även

[Analysera telemetri för spårning av bevarandeprincip](/dynamics365/business-central/dev-itpro/administration/telemetry-retention-policy-trace)  
[Revision av ändringar i Business Central](across-log-changes.md)  
[Filtrering](ui-enter-criteria-filters.md#filtering)  
[Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]