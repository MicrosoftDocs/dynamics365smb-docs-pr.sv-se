---
title: Ange datumintervall i Business Central | Microsoft Docs
description: "Lära dig hur du får en rapport med data från specifika tidsperioder med datumintervall i Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: sv-se
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a>Ange datumintervall
Du kan ange filter som innehåller ett startdatum och ett slutdatum om du vill visa enbart de data som finns i datumintervallet eller tidsintervallet. Speciella regler gäller för hur du kan ange datumintervall. Ta **10 högsta kund** som exempel:

![Ange ett datumintervall på sidan för begäran för listan över 10 högsta kund](./media/ui-enter-date-ranges/customer-top10-list.png)

Här kan du begränsa rapporten till ett datumintervall, till exempel de två senaste veckorna eller totalt 6 veckor eller det intervall du vill använda. Om du vill ange datumintervall, ange datum och använda någon **...** Eller **|** för att ange projektintervall. I vårt exempel, om du vill visa de 10 främsta kunderna för de första två veckorna ställer du in datumfiltret på *05 01 17..05 14 17*.
Här följer några andra exempel:

| Betydelse | Exempel | Inkluderade transaktioner |
|---|---|---|
|Lika med| 12 15 16 |Endast de som bokförts 15 december 2016.|
|Intervall| 12 15 16..01 15 17<br /><br />..12 15 16|De som bokförts på datum mellan och inklusive 15 december 2016 och 15 januari 2017.<br /><br />De som bokförts 02-12-15 eller tidigare.|
|Antingen eller|12 15 16&#124;12 16 16|Transaktioner registrerade antingen den 15 December eller 16 December 2016. Om det finns transaktioner som bokförs båda dagarna kommer alla att visas.|

Du kan också kombinera formattyperna.

| Exempel | Inkluderade transaktioner |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Transaktioner som bokförts antingen den 15 december 2016, eller på datum mellan och inklusive 01 december 2016 och 31 maj 2017. |
|..12 14 16&#124;12 30 16.. | Transaktioner bokförda 14 December eller tidigare, eller transaktioner bokförda 30 December eller senare – d.v.s. alla transaktioner utom de som bokförts på datum mellan och inklusive 15 December och 29. |

Observera att vi har använt Amerikanskt datumformat MMDDÅÅ här. När [!INCLUDE[d365fin](includes/d365fin_md.md)] blir tillgängliga för andra marknader, kommer du att kunna använda de format som används.

## <a name="using-date-formulas"></a>Använda datumformler
En datumformel är en kort kombination av förkortningar med bokstäver och siffror som anger hur datum ska beräknas. Du kan ange datumformler i olika beräkningsfält för datum och i fält för återkomstfrekvens i återkommande journaler.

> [!NOTE]
>  I alla dataformulärfält inkluderas automatiskt en dag att täcka i dag som dagen när perioden börjar. Om du till exempel anger **1V** är perioden därefter faktiskt åtta dagar eftersom idag inkluderas. För att ange en period om sju dagar (en exakt vecka) inklusive perioden för startdatum måste du ange **6D** eller **1V\-1D**.

Här följer några exempel på hur datumformler kan användas:

-   Datumformeln i fält för återkommande frekvens i återkommande journaler bestämmer hur ofta posten på journalraden ska bokföras.

-   Datumformeln i fältet **Betalningsfrist** för en viss påminnelsenivå bestämmer vilken tidsperiod som ska förflyta från förfallodatumet (eller från förfallodatumet för den föregående påminnelsen) innan en påminnelse ska skapas.

-   Datumformeln i fältet **Förfallodatumformel** bestämmer hur förfallodatumet på påminnelsen beräknas.

Formeln för datumberäkning kan bara omfatta högst 20 tecken, både siffror och bokstäver. Du kan använda följande bokstäver som förkortningar för tidsangivelser.

|  Bokstav  |  Tidsspecifikation  |
|----------|----------------------|
|S|Löpande (innevarande)|
|D|Dag\(ar\)|
|V|Vecka\(veckor\)|
|M|Månad\(er\)|
|K|Kvartal|
|Å|År|

Du kan bygga upp en datumformel på tre sätt.

Följande exempel visar hur du använder **L** för löpande, plus en tidsenhet.

|  Uttryck  |  Betydelse  |
|--------------|-----------|
|LV|Löpande (innevarande) vecka|
|LM|Löpande (innevarande) månad|

Följande exempel visar hur du använder ett tal och en tidsenhet. Ett nummer får inte vara högre än 9 999.

|  Uttryck  |  Betydelse  |
|--------------|-----------|
|10D|Tio dagar från dagens datum.|
|2V|Två veckor från dagens datum|

Följande exempel visar hur du använder en tidsenhet och ett tal.

|  Uttryck  |  Betydelse  |
|--------------|-----------|
|D10|Den tionde dagen varje månad.|
|VD4|Den nästa fjärde dagen i en vecka \(torsdag\)|

Följande exempel visar hur du kombinera dessa tre metoder om så behövs.

|  Uttryck  |  Betydelse  |
|--------------|-----------|
|LM\+10D|Löpande månad \+ 10 dagar|

Följande exempel visar hur du använder ett minustecken för att ange ett datum i det förflutna.

|  Uttryck  |  Betydelse  |
|--------------|-----------|
|-1Å|1 år sedan från idag|

> [!IMPORTANT]
>  Om lagerstället använder en baskalender, tolkas datumformeln som du anger i t.ex. fältet **Leveranstid** enligt kalenderarbetsdagar. Till exempel betyder **1V** sju arbetsdagar.

## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Datumberäkning för inköp](purchasing-date-calculation-for-purchases.md)  
[Ange villkor i filter](ui-enter-criteria-filters.md)  

