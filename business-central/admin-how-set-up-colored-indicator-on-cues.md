---
title: "Ange färgindikatorer för att anpassa visuella signaler om en stack-ikons aktivitet för företaget eller enskilda användare | Microsoft Docs"
description: "Som administratör kan du skapa stack-ikoner som visas i användarens rollcenter för att inkludera en indikator som ändrar färg baserat på datavärdena i stack-ikonerna."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f68bd92456ccab6d4bade8f5545d5c715a0c35bd
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-a-colored-indicator-on-cues-for-the-company-or-individual-users"></a>Skapa en färglagd indikator på stack-ikoner för företaget eller enskilda användare
Som administratör kan du skapa stack-ikoner som visas i användarens rollcenter för att inkludera en indikator som ändrar färg baserat på datavärdena i stack-ikonerna.  
  
Indikatorn visas som en kulört stapel längs den övre kanten på stack-ikon-panelen. Den ger en visuell signal över statusen för stack-ikonaktivitet, som kan ange gynnsamma eller ofördelaktiga förhållanden för att meddela användaren att vidta åtgärd. Om t.ex. en stack-ikon visar pågående försäljningsfakturor kan du ställa in indikatorn för att visa grönt (positivt) när totala antalet pågående försäljningsfakturor är under 10, och röd (negativt) när antalet är större än 20.  
  
Från fönstret **Inställning av stack-ikon** ställer du in indikatorer för alla stack-ikoner som är tillgängliga i företagsdatabasen. Du kan ställa in indikatorerna för att gälla alla användare i företaget eller en individuell användare endast. Indikatorinställningarna i fönstret **Inställning av stack-ikon** fungerar som standardindikatorinställningarna. Om fönstret **Inställning av stack-ikon för slutanvändare** görs tillgängligt för användare kan de anpassa indikatorinställningarna som du definierar i fönstret **Inställning av stack-ikon**.  
  
För att ställa in indikatorn, anger du upp till två tröskelvärden som definierar tre intervall av datavärden (låg, medel och hög) som du kan koppla en annan färg (eller stil).  
  
### <a name="to-set-up-colored-indicators-on-cues"></a>Så här ställer du in kulörta indikatorer på stack-ikoner  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inställning av stack-ikon** och välj sedan relaterad länk.  
  
     Fönstret **Inställning av stack-ikon** visas. Fönstret anger indikatorerna som närvarande är inställda på stack-ikoner. Indikatorer som gäller för alla användare i företaget har ett tomt **Användarnamn**-fält. Indikatorer som är kopplade till en viss användare innehåller användarens namn i **Användarnamn**-fältet.  
  
    > [!NOTE]  
    >  Om du skapar indikator för hela företaget och en användare ändrar indikatorn senare, visas en separat transaktion för indikatorn i listan för den användaren.  
  
2. Välj åtgärden **Redigera lista**.  
3. Om du vill skapa en indikator för en stack-ikon som inte specificerats i fönstret, väljer du åtgärden **Ny** och sedan fyll i fälten enligt beskrivningen som följer. Om du vill ändra en befintlig indikator går du vidare till nästa steg.  
  
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
  
## <a name="see-also"></a>Se även  
[Skapa en färglagd indikator på stack-ikoner i din arbetsyta](ui-how-setup-colored-indicator-cues.md)  
