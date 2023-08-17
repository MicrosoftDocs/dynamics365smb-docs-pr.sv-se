---
title: Använd statistiska konton för att analysera icke-transaktionella data
description: Beskriver hur du använder statistiska konton som en annan datakälla för analyserna.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/07/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, financial report'
ms.search.form: '2632, 2631, 2633, 2623, 2634'
---
# <a name="analyze-data-with-statistical-accounts"></a>Analysera data med statistiska konton

Använda statistiska konton för att komplettera information i ekonomiska rapporter. Med statistiska konton kan du lägga till mått som bygger på icke-transaktionella data. Du lägger till icke-transaktionella data som nummerbaserade enheter, till exempel:

* Personal
* Kvadratmeterantalet
* Antalet kunder med förfallna konton

Du kan t.ex. mäta intäkter eller kostnader baserat på antalet personer på en avdelning. Personal för avdelningen är den statistiska enheten för kontot. I följande bild visas ett exempel på en rapport där ett statistik konto används för att visa intäkt per medarbetare.

:::image type="content" source="media/statistical account report example.png" alt-text="Ett exempel på en rapport som innehåller data från ett statistik konto.":::

I fråga om hur de fungerar är statistiska konton likartade bokföringskonton. De lagrar transaktioner som du bokför med statistiska kontojournaler, så att du kan använda transaktionerna som data för ekonomiska rapporter. Läs mer om ekonomiska rapporter i [Förbereda Financial Reporting med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md). 

Det finns några huvudskillnader mellan statistiska konton och bokföringskonton. Statistiska konton är separata entiteter och ingår inte i råbalansen. Du behöver inte heller balansera debet- och kreditbelopp när du använder statistiska kontojournaler för att bokföra transaktioner på ett statistik konto. Du bokför bara beloppet.

## <a name="set-up-a-statistical-account"></a>Skapa ett statistiskt konton

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Statistiska konton** och väljer sedan relaterad länk.
1. På snabbfliken **Allmänt** fyller du i fälten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="post-amounts-to-a-statistical-account"></a>Bokföra belopp till ett statistik konto

1. Om du vill bokföra de belopp som du vill spåra väljer du tabellen **Statistiska konton** på sidan **Journal för statistiskt konto**.
1. I fältet **Bokföringsdatum**, ange sista datum för den bokföringsperiod som du vill bokföra belopp för.
1. Valfritt: Om du vill spåra belopp för ett specifikt dokument, i fältet **Dokumentnummer** anger du dokument-ID.
1. I fältet **Nummer på statistiskt konto** väljer du statistiska konto som du vill bokföra beloppen på.
1. Skriv in en kort beskrivning av vad du mäter i fältet **Beskrivning**.  
1. Ange det belopp som ska bokföras i fältet **Belopp**. 
1. Valfritt: Om du vill inkludera statistiska kontot i mer avancerade analyser, ange dimensioner i fälten **Avdelningskod** och **Kundgruppkod**. Om du vill lära dig mer om dimensioner går du till [Analysera data per dimension](bi-how-analyze-data-dimension.md).

## <a name="verify-statistical-account-amounts"></a>Verifiera belopp till ett statistik konto

På sidan **statistiska konton** använder du åtgärden **statistiskt kontosaldo** för att kontrollera att de registrerade beloppen är korrekta för varje period.  

## <a name="include-the-statistical-account-in-a-financial-report"></a>Ta med statistiskt kontot i en finansiell rapport

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
1. Skapa en ny finansiell rapport på något av följande sätt:
    1. Välj **nytt** om du vill börja från början. Om du vill ha mer information om hur du skapar ekonomiska rapporter går du till [Skapa en ny ekonomisk rapport](bi-how-work-account-schedule.md#create-a-new-financial-report).
    1. Om du vill använda inställningar från en liknande rapport som du redan har, väljer du den rapport som du vill kopiera och väljer sedan åtgärden **Kopiera ekonomisk rapport**. Du kan redigera de inställningar som du kopierar i den nya rapporten.
1. Lägg till statistiskt konto:
    1. Om du börjar från början väljer du åtgärden **redigera raddefinition**.
    1. För att använda en raddefinition från en befintlig rapport, välj rapporten att kopiera från och välj sedan **Kopiera raddefinition**.
1. I fältet **Raddefinition** i **Radnr.** anger du var raden ska visas i serien med rader i rapporten.
1. Ange text som indikerar vad du mäter i fältet **Beskrivning**.
1. I fältet **Summeringstyp**, välj **Statistiska konton**.
1. I fältet **Summering**, välj ett statistiskt konto.
1. I fältet **Radtyp** väljer du om du vill visa saldot på bokföringsdatumet eller början av bokföringsperioden eller om du vill visa ändringen av beloppet under perioden.
1. Fyll i resterande fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se även

[Financial Business Intelligence](bi.md)  
[Ekonomisk rapportering och analys i Business Central](finance-reports.md)
