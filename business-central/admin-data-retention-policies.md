---
title: Rensa data med lagringsprinciper
description: Du kan ange hur ofta du vill ta bort vissa typer av data.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'delete, data, retention, policy, policies'
ms.search.form: '3903, 3901'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Definiera bevarandeprinciper
Administratörer kan definiera bevarandeprinciper för att ange hur ofta de vill att [!INCLUDE[prod_short](includes/prod_short.md)] tar bort gamla data i tabeller som innehåller loggposter och arkiverade poster. Att rensa loggposter kan t. ex. göra det enklare för dig att arbeta med data som faktiskt är relevanta. Principer kan omfatta alla data i tabellerna som har passerat utgångsdatumet, eller så kan du lägga till filterkriterier som endast tar med vissa utgångna data i principen. 

## Nödvändiga konfigurationer och behörigheter
Innan du kan skapa bevarandeprinciper måste du ställa in följande.

|Konfiguration  |Beskrivning  |
|---------|---------|
|**Tillåtna tabeller**     |Vi tillhandahåller en lista över de tabeller som kan ingå i bevarandeprinciper. Om du däremot vill lägga till tabeller från ett tillägg till en bevarandeprincip, måste utvecklaren lägga till tabellerna i listan. Mer information finns i [Inkludera tillägget i en bevarandeprincip](admin-data-retention-policies.md#including-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Kvarhållningsperioder**     |Ange tidsperioder för vilka data ska behållas i tabellerna i en princip. Perioderna bestämmer hur ofta data ska tas bort.         |

Dessutom måste du ha behörigheten SUPER-användare eller behörighetsuppsättningen för bevarandeprincip. Användare som har tilldelats behörighetsuppsättningen Konfigurera bevarandeprincip kan definiera bevarandeprinciper för tabeller, även om de inte har behörighet att läsa och ta bort för dessa tabeller. Projektköposten måste köras som en användare med behörighet att läsa och ta bort data. Vi rekommenderar att du inte beviljar behörighetsuppsättningen Konfigurera bevarandeprincip till användare som inte bör tillåtas ta bort data.

> [!NOTE]
> Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt och vill prova att använda bevarandeprinciper i demonstrationsdatabasen Cronus, finns det några saker du måste göra. Demonstrationsföretaget innehåller inga tabeller som du kan använda med bevarandeprinciper, så du måste lägga till dem. Det gör du genom att skapa ett nytt, tomt företag i demonstrationsdatabasen. I det nya företaget importerar du konfigurationspaketet RapidStart för ditt land/din region som motsvarar standardpaketet NAV17.0.W1.ENU.STANDARD.rapidstart. Konfigurationsdata för bevarandeprinciper kommer att vara tillgängliga i det nya företaget.

### Så här skapar du perioder för lagring
Du kan begränsa lagringsperioderna så länge du vill. Om du vill skapa lagringsperioder går du till sidan **Bevarandeprinciper** och använder åtgärden **Lagringsperiod**. De perioder som du definierar kommer att vara tillgängliga för alla policyer.

> [!NOTE]
> Vi har definierat en minsta lagringsperiod för vissa tabeller på grund av regelefterlevnad. Om du anger en lagringsperiod som är kortare än minimikravet visas ett meddelande om den obligatoriska perioden.

### Konfigurera en bevarandeprincip
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **bevarandeprinciper** och väljer sedan relaterad länk.
2. Välj tabellen som du vill ta med i principen i fältet **Tabell-ID**.
3. I fältet **Lagringsperiod** anger du hur länge informationen i tabellen ska bevaras.
4. Valfritt: Om du vill använda principen för specifika data i en tabell inaktiverar du reglaget Tillämpa på alla poster. Snabbfliken Policy för postbevarande visas, där du kan ange filter för att skapa delmängder av data för varje rad. Mer information finns i [Filtrering](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Varje rad har sin egen lagringsperiod. Om du anger olika lagringsperioder för samma data används den längsta perioden. Vissa tabeller innehåller också filter som du inte kan ändra eller ta bort. För att identifiera dessa filter visas de i ett teckensnitt med ljusare färg.

## Tillämpa bevarandeprinciper
Du kan använda en jobbköpost för att tillämpa bevarandeprinciper för att automatiskt ta bort data eller så kan du manuellt tillämpa principer.

Om du vill tillämpa en bevarandeprincip automatiskt skapar och aktiverar du bara en princip. När du aktiverar en princip skapar vi en jobbköpost som tillämpar bevarandeprinciper enligt den lagringsperiod som du anger. Alla bevarandeprinciper kommer att använda samma jobbköpost. Som standard tillämpar jobbköposten principen varje dag vid 0200. Du kan ändra standardvärdet, men om du gör det rekommenderar vi att det körs utanför kontorstid. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md). 

Du kan tillämpa en princip manuellt med hjälp av åtgärden **Tillämpa manuellt** på sidan **Bevarandeprinciper**. Om du alltid vill tillämpa en princip manuellt aktiverar du reglaget **Manuellt**. Projektköposten ignorerar principen när den körs.

## Visa loggposter för bevarandeprincip
Du kan visa aktiviteter som är relaterade till bevarandeprinciper på sidan **Logg för bevarandeprincip**. Poster skapas t. ex. när en princip tillämpas, eller om fel uppstod när det skedde. 

## Inkludera tillägget i en bevarandeprincip (kräver hjälp från en utvecklare)
Som standard täcker bevarandeprinciper endast tabeller som ingår i listan över [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller som vi tillhandahåller. Du kan ta bort standardtabeller från listan och du kan lägga till tabeller som du äger. Det innebär att du inte kan lägga till en tabell som du inte har skapat själv. Du kan till exempel inte lägga till andra tabeller från [!INCLUDE[prod_short](includes/prod_short.md)] eller från ett tillägg som du har köpt.

Om du vill lägga till tabeller i listan över tillåtna tabeller måste utvecklaren lägga till kod, till exempel installationens codeunit för tillägget (en codeunit med undertypen *installera*). 

När en utvecklare lägger till en tabell kan de ange obligatoriska filter och standardfilter. Obligatoriska filter kan inte tas bort eller ändras senare när du lägger till tabeller för att definiera en bevarandeprincip. Standardfilter är vänliga förslag.

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