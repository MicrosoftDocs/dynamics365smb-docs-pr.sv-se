---
title: Hållbarhet ekonomisk rapportering
description: Beskriver hur du använder ekonomiska rapporter för att skapa olika vyer och rapporter för att analysera data om hållbarhetsprestanda.
author: altotovi
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: '104, 108, 490'
ms.date: 08/22/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Analysera hållbarhetstransaktioner med finansiella rapporter 

Funktionen *Ekonomiska rapporter* ger dig insikter i de ekonomiska data som visas i din kontoplan (COA). Du kan ställa in ekonomiska rapporter till att analysera siffror för redovisningskonton och jämför redovisningstransaktioner med budgettransaktioner. Men du kan också analysera statistiska data och hållbarhetsdata med samma funktion och till och med kombinera alla tre typerna av data.  

## Förutsättningar för ekonomisk rapportering  

Att skapa ekonomiska rapporter kräver förståelse för strukturen på de data som du vill analysera. Dit är några viktiga begrepp som du förmodligen måste vara uppmärksam på innan du utformar dina finansiella rapporter: 

1. Relaterat till kontoplanen: 
   1. Koppla redovisningsbokföringskonton till redovisningskontokategorier. 
   2. Utforma hur dimensioner ska användas.
   3. Ställ in redovisningsbudgetar  
2. Relaterat till hållbarhet:   
   1. Lägg upp dina hållbarhetskonton. 
   2. Ställ in dina koldioxidavgifter och CO2e i **utsläppsavgifterna**.
   3. Utforma hur dimensioner ska användas.  
3. När det gäller statistikräkenskaperna: 
   1. Skapa statistikkonton. 
   2. Utforma hur dimensioner ska användas.  

> [!NOTE]
> Finansiella rapporter fungerar inte direkt med CO2-, CH4- eller N2O-utsläpp. Istället för att den använder CO2-ekvivalentmodellen och det betyder att du först måste konfigurera **CO2e**  (koldioxidekvivalent) på **sidan Utsläppsavgifter** .  

> [!NOTE]
> Fler detaljer om hur du använder ekonomiska rapporter med ekonomiska data och kontoplan finns Hit [Skapa ekonomiska rapporter med hjälp av ekonomiska data och kontokategorier](bi-how-work-account-schedule.md).   

## Skapa en ny ekonomisk rapport  

Du kan snabbt skapa dina egna finansiella rapporter, starta genom att kopiera en befintlig, som beskrivs i steg 3 nedan. 

1. Välj ![glödlampan som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.  
2. På sidan **Ekonomiska rapporter** väljer du åtgärden **Nytt** för att skapa ett nytt namn på ekonomisk rapport.  
3. Fyll i rapportens kortnamn i **fältet Namn**  (du kan inte ändra namnet senare) och ange **Beskrivning**.  
4. Välj en raddefinition och en kolumndefinition.   
5.  **Välj åtgärden Redigera rapportdefinition**  om du vill komma åt fler boenden i den ekonomiska rapporten.  
6. På snabbfliken **Alternativ** kan du redigera rapportbeskrivningen, ändra rad- och kolumndefinitionerna och definiera hur datum ska visas. Datum kan vara en hierarki för dag/vecka/månad/kvartal/år, eller använda bokföringsperioder. För mer information, gå till [Jämföra bokföringsperioder med hjälp av periodformler](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas). 
7. På snabbfliken **Dimensioner** kan du definiera dimensionsfilter för rapporten.  
8. Du kan förhandsgranska rapporten i området under snabbfliken **Dimensioner**.   

Om du vill analysera dina hållbarhets- eller statistiska data kan du uppnå detta genom att ställa in **raddefinition**.  

Så här skapar eller redigerar du en raddefinition:

1. På sidan **Ekonomiska rapporter** väljer du den relevanta ekonomiska rapporten och väljer sedan åtgärden **Redigera raddefinition**. 
2. Ställ in rader som i följande steg.  

> [!NOTE]
> **Radnr.** fältet visar de första 10 tecknen i en identifierare, t.ex. ett kontonummer. Om du lägger till element med identifierare som börjar med samma tio tecken kommer du att ha dubbletter i fältet **Radnr.** . Om det behövs kan du redigera identifierare manuellt när du har infogat elementen. Alla identifierare visas i fältet **Summeringsintervall** .

> [!NOTE]
> Du kan kombinera alla **summeringstyper**, dvs. bokföringskonton, Sust. Konton, statistiska konton.

> [!NOTE]
> Raddefinitioner versionshanteras inte. När du ändrar en raddefinition ersätts den gamla versionen och ändringarna sparas i databasen. 

### Analysera hållbarhetsdata  

1.  **Ange radnumret.** För att identifiera din råa och lägga till **Beskrivning** som en text som kommer att visas på den ekonomiska rapportraden. 
2. I kolumnen Summeringstyp väljer du Sust **. Alternativet Konton** .   
3. Välj ett eller flera hållbarhetskonton med hjälp av alla tillämpliga filter i fältet Summeringsintervall. 
4. Välj ett av följande alternativ i fältet **Beloppstyp** :   
   1. **CO2e** om du vill rapportera CO2-ekvivalentvärde från **fältet CO2e-utsläpp** i **hållbarhetstransaktionerna**. 
   2. **Koldioxidavgift** om du vill rapportera ekonomisk ekvivalent (koldioxidavgift) från **fältet Koldioxidavgift** i **hållbarhetstransaktionerna**. 
5. Om du väljer Formel som summeringstyp **kan du använda matematiska formler i** kolumnen Summeringsintervall **.**  **·**   

### Analysera statistiska data

1.  **Ange radnumret.** För att identifiera raden och lägga till **Beskrivning** som en text som visas på den ekonomiska rapportraden. 
2. Välj alternativet Statistikkonton i kolumnen **Summeringstyp**  **.**    
3. Välj ett eller flera hållbarhetskonton med hjälp av **alla tillämpliga filter i fältet Summeringsintervall** . 
4. Om du väljer **Formel** som **summeringstyp** kan du använda matematiska formler i kolumnen **Summeringsintervall** .  

## Se även

[Översikt över hållbarhetshantering](finance-manage-sustainability.md)    
[Hållbarhetsrapport och analys i Business Central](sustainability-reports.md)   
[Hållbarhets-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Förbered ekonomisk rapportering](bi-how-work-account-schedule.md)    
[raddefinition i ekonomisk rapportering](bi-row-definitions.md)    
[kolumndefinition i ekonomisk rapportering](bi-column-definitions.md)    
[Ekonomi](finance.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
