---
title: Visa tabellinformation
description: Lär dig mer om hur du kan visa information om databaslås i Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 8700
ms.date: 08/23/2022
ms.author: jswymer
---

# <a name="viewing-table-information"></a>Visa tabellinformation

På sidan **8700 tabellinformation** finns information om antalet poster i alla system- och affärstabeller i [!INCLUDE[prod_short](includes/prod_short.md)] och hur mycket data varje tabell innehåller.

Den här informationen är användbar för att felsöka prestandaproblem, eftersom du kan se fördelningen av datastorlek över tabeller.

## <a name="view-table-information"></a>Visa tabellinformation

Om du vill öppna sidan markerar du ![Sök på sidan eller rapporten.](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport") anger du **Tabellinformation** och väljer sedan relaterad länk.

I följande tabell beskrivs de olika tabellerna som anges:

|Kolumn|Beskrivning|
|------|-----------|
|Företagsnamn|Namnet på företaget, om det finns något, som tabellen tillhör.|
|Tabellnamn|Tabellens namn.|
|Tabellnr.|ID:t för tabellen.|
|Antal av poster|Det totala antalet poster som lagras i tabellen.|
|Poststorlek|Den genomsnittliga poststorleken i KB/post. Värdet beräknas med hjälp av följande formel: 1024 (storlek)/(No. av poster). |
|Storlek (kB)|Den totala mängden utrymme som tabellen upptar i databasen. Detta värde är summan av värdena i fälten Datastorlek och Indexstorlek.|
|Datastorlek (kB)|Hur mycket utrymme data i tabellen upptar i databasen.|
|Indexstorlek (kB)|Hur mycket utrymme tabellindexen (nycklarna) upptar i databasen.|
|Komprimering|Typen av komprimering, **rad**, **sida** eller **inget** som tillämpas på tabellen i databasen. Mer information finns i [datakomprimering](/sql/relational-databases/data-compression/data-compression?).|

> [!NOTE]
> Om du tar bort data i en tabell [!INCLUDE[prod_short](includes/prod_short.md)] startas flera processer i bakgrunden för att se till att allting rensas i databasen. Värdena på sidan Tabellinformation uppdateras inte förrän dessa processer är klara, vilket kan ta ett tag. Hur lång tid du ska vänta kan variera beroende på databasens storlek.

## <a name="see-also"></a>Se även

[Kontrollera sidor](across-inspect-page.md)  
[Prestandaartiklar för utvecklare](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
