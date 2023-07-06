---
title: Söka efter specifika data
description: Du kan använda sökfunktionen om du vill hitta en specifik post.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'data, search, record'
ms.search.form: null
ms.date: 09/20/2022
ms.author: bholtorf
---

# <a name="search-for-a-record-in-your-data"></a><a name="search-for-a-record-in-your-data"></a><a name="search-for-a-record-in-your-data"></a>Söka efter en post i dina data

När du vill söka efter en viss post eller ett visst värde använder du funktionen **Sök efter data** för att söka efter den. Starta en sökning i rollcentret på följande sätt:

* Använd åtgärden **Sök efter data**
* Använd kortkommandot <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>F</kbd>.

## <a name="how-search-works"></a><a name="how-search-works"></a><a name="how-search-works"></a>Hur sökningen fungerar

När du har angett nyckelorden startar [!INCLUDE[prod_short](includes/prod_short.md)] sökningen i bakgrunden och går igenom en tabell i taget. Sökresultaten börjar visas när du har avslutat varje tabell. 

Om du anger fler än ett nyckelord kommer resultatet att inkludera endast poster som innehåller alla ord i något av de markerade fälten.

På resultatsidan visas de tre senast uppdaterade posterna. Om det finns fler än tre kan du välja **Visa alla** för att visa dem.

Varje gång du väljer ett sökresultat ökar du tabellens popularitet och den kommer att visas högre upp i resultatet. Dessutom går det snabbare att hitta posten om du söker efter den i framtiden.

> [!NOTE]
> Rubriker på försäljnings-, inköps-och servicedokument representerar olika dokumenttyper, t.ex. offerter, fakturor och order. Rubriker behandlas som om de vore tabeller. Om nyckelordet hittas på en rad i ett av dessa dokument visas sidan för dokumentet när du väljer sökresultatet, och inte bara raden.

## <a name="getting-started"></a><a name="getting-started"></a><a name="getting-started"></a>Kom i gång

Du kan göra resultatet snabbare genom att välja de fält i tabellerna som du vill ta med i dina sökningar. Vilka tabeller och fält du kan välja bland varierar beroende på ditt rollcenter. Som standard är alla tabeller och fält valda, vilket kan göra att sökningen går långsammare. Vi rekommenderar att du utesluter så många tabeller och fält som möjligt.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Söka efter sidor och information med berätta](ui-search.md)  
[Ange data](ui-enter-data.md)  
