---
title: Skapa anpassade färgindikatorer för en stack-aktivitet
description: Som administratör kan du skapa stack-ikoner som visas i användarens rollcenter för att inkludera en indikator som ändrar färg baserat på datavärdena i stack-ikonerna.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9701, 9702'
ms.date: 04/01/2021
ms.author: jswymer
---
# Skapa en färglagd indikator på stack-ikoner för företaget eller enskilda användare

Som administratör kan du skapa stack-ikoner som visas i användarens rollcenter för att inkludera en indikator som ändrar färg baserat på datavärdena i stack-ikonerna.  

Indikatorn visas som en kulört stapel längs den övre kanten på stack-ikon-panelen. Den ger en visuell signal över statusen för stack-ikonaktivitet, som kan ange gynnsamma eller ofördelaktiga förhållanden för att meddela användaren att vidta åtgärd. Om t. ex. en stack-ikon visar pågående försäljningsfakturor kan du ställa in indikatorn för att visa grönt (positivt) när totala antalet pågående försäljningsfakturor är under 10, och röd (negativt) när antalet är större än 20.  

Från sidan **Inställning av stack-ikon** ställer du in indikatorer för alla stack-ikoner som är tillgängliga i företagsdatabasen. Du kan ställa in indikatorerna för att gälla alla användare i företaget eller en individuell användare endast. Indikatorinställningarna på sidan **Inställning av stack-ikon** fungerar som standardindikatorinställningarna. Om sidan **Inställning av stack-ikon för slutanvändare** görs tillgängligt för användare kan de anpassa indikatorinställningarna som du definierar på sidan **Inställning av stack-ikon**.  

För att ställa in indikatorn, anger du upp till två tröskelvärden som definierar tre intervall av datavärden (låg, medel och hög) som du kan koppla en annan färg (eller stil).  

### Så här ställer du in kulörta indikatorer på stack-ikoner  
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inställning av stack-ikon** och väljer sedan relaterad länk.  

     Sidan **Inställning av stack-ikon** visas. Sidan anger indikatorerna som närvarande är inställda på stack-ikoner. Indikatorer som gäller för alla användare i företaget har ett tomt **Användarnamn**-fält. Indikatorer som är kopplade till en viss användare innehåller användarens namn i **Användarnamn**-fältet.  

    > [!NOTE]  
    >  Om du skapar indikator för hela företaget och en användare ändrar indikatorn senare, visas en separat transaktion för indikatorn i listan för den användaren.  

2. Välj åtgärden **Redigera lista**.  
3. Om du vill skapa en indikator för en stack-ikon som inte specificerats på sidan, väljer du åtgärden **Ny** och sedan fyll i fälten enligt beskrivningen som följer. Om du vill ändra en befintlig indikator går du vidare till nästa steg.  

    |  Fält  |  Description  |    
    |---------|---------------|  
    |**Användarnamn**|Om du vill ställa in indikatorn för alla användare låter du fältet vara tomt.<br /><br /> Om du vill ställa in indikatorn för en specifik användare, anger du fältet till användarnamnet.|  
    |**Tabellnr.**|Anger ID för tabellobjektet som innehåller stack-ikonen. Använd listrutan för att hitta tabellen. Listrutan innehåller alla stack-ikontabeller i företagsdatabasen.<br /><br /> Fältet **Tabellnamn** fylls i automatiskt baserat på ditt val.|  
    |**Fältnr**|Anger ID för stack-ikonen som du vill ange en indikator på. Använd listrutan för att hitta stack-ikonen som du vill ha. **Obs!**  Stack-ikon-ID motsvarar fältnumret som tilldelats stack-ikonen i tabellen. <br /><br /> Fältet **Fältnamn** fylls i automatiskt baserat på ditt val|  

4. Ange fälten enligt följande tabell för att skapa indikatorn för en stack-ikon.  

    |  Fält  |  Description  |    
    |---------|---------------|  
    |**LowStyle**|Anger färgen på indikatorn när stack-ikonens värde är under värdet i fältet **Gränsvärde 1**.|  
    |**LowThreshold**|Anger värdet vid eller över vilket indikatorn ändrar färg till den färg som anges i fältet **Medelintervallformat**.|  
    |**MiddleStyle**|Anger färgen på indikatorn när stack-ikonens värde är större än eller lika med värdet i fältet **Gränsvärde 1** men mindre än eller lika med värdet i fältet **Gränsvärde 2**.|  
    |**HighThreshold**|Anger värdet över vilket indikatorn ändrar färg till den färg som anges i fältet **Högt intervallformat**.|  
    |**HighStyle**|Anger färgen som ska användas när stack-ikonens värde är över värdet i fältet **Gränsvärde 2**.|  

     Efterföljande tabeller listar de bakgrundsfärger som motsvarar alternativen för fälten **LowStyle**, **MiddleStyle** och **HighStyle**.  

    |  Alternativ  |  Färg  |  
    |----------|---------|  
    |**Ingen**|Ingen färg (samma färg som stack-ikonen)|  
    |**Positiv**|Grön|  
    |**Negativ**|Röd|  
    |**Tvetydigt**|Gul|  
    |**Underordnad**|Grått|  

## Se även


[!INCLUDE[footer-include](includes/footer-banner.md)]