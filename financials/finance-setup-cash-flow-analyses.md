---
title: "Ställa in analysvy för kassaflöde | Microsoft Docs"
description: "Beskriver hur du ställer in kontantcykel, intäkter och kostnader, kassaflöde och kassaflödesprognosdiagrammet för att analysera tidigare och framtida föflyttning av likvida medel från och till ditt företag."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.date: 03/28/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e07f32dcc3a50e07c5dea48600f7e3dbcd6088a9
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-cash-flow-analysis"></a>Ställa in analysvy för kassaflöde
Om du vill ha hjälp att bestämma vad som ska ske med dina likvida medel kan du titta på diagrammen i rollcentret Revisor:  

* **Kassacykel**  
* **Inkomst och utgift**  
* **Kassaflöde**  
* **Kassaflödesprognoser**  

Det här avsnittet beskriver var informationen i diagrammen kommer från och, vid behov, vad du gör om du vill börja använda diagrammen.  

## <a name="the-cash-cycle-and-income--expense-charts"></a>Kassacykeln och diagram för inkomster och utgifter
Diamgrammen **Kassacykel** och **inkomster och utgifter** är klara, beroende på kontoplan och kontouppställningar. Kontona är var informationen kommer från och kontouppställningar beräknar förhållandet mellan försäljning och kundfordringar. Vissa konton och kontouppställningar tillhandahålls. Du kan använda dem som de är, ändra dem och lägga till nya. Om du lägger till redovisningskonton i kontoplanen, till exempel genom att importera dem från QuickBooks, behöver du mappa till kontona på sidan **kontouppställningar** för följande Kontouppställningsnamn:  

| Kontouppställningsnamn | Där den används |
| --- | --- |
| **I_CACYCLE** |Kassacykel |
| **I_CASHFLOW** |Kassaflöde |
| **I_INCEXP** |Inkomst och utgift |
| **I_MINTRIAL** |Som en resultaträkning om du inte använder kontoplanen |

**Obs!** Det är det en bra idé att hålla beräkningarna som ges för kontouppställningen.  

Ange konton i fältet **Summeringsintervall** för **Totala intäkter**, **Totala kundfordringar**, **Totala leverantörsskulder**, och **Totalt lager**. Om du vill mappa till flera olika konton eller mer än ett visst konto, anger du kontonumren åtskilda med ".." eller med en lodrät stapel. Till exempel **1111..4444** eller **2222|3333|5555**.  

**Tips:** Kontrollera en mappning genom att välja åtgärdem **översikt**.  

## <a name="set-up-the-cash-flow-chart"></a>Konfigurera kassaflödesdiagrammet
Kassaflödesdiagrammet baseras på följande:  

* Ett diagram med kassaflödeskonton
* En eller flera kassaflödeinstallationer. Dessa anger kontona som ska användas för redovisning, inköp, försäljning, tjänster och anläggningstillgångar.  

För att hjälpa dig att komma igång, finns vissa konto- och kassaflödeinstallationer. Du kan lägga till, ändra eller ta bort dem.  

Du anger dessa inställningar genom att söka efter **kassaflödeskonton**, väljer länken och fyller sedan i fälten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Upprepa stegen för **Kassaflödesinställningar**.  

## <a name="set-up-cash-flow-forecasts"></a>Konfigurera kassaflödesprognoser.
Diagrammet **kassaflödesprognos** använder kassaflödeskonton, kassaflödesinställningar för kassaflödesprognoser. Vissa tillhandahålls, men du kan ställa in egna med hjälp av en assisterade konfigurationsguiden. Guiden hjälper dig att ange saker som till exempel hur ofta du uppdaterar prognosen, kontona som du vill basera den på, information om när du betalar skatter och om du ska använda [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite).  

Kassaflödesprognoser kan använda Cortana Intelligence-dokument med förfallodatum senare ska inkluderas. Resultatet blir en mer omfattande prognos. Anslutningen till Cortana Intelligence har redan ställts in åt dig. Du måste aktivera den. När du loggar in i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], visas ett meddelande i en blå stapel och innehåller en länk till standardinställning för kassaflödesinställningen. Meddelandet visas endast en gång. Om du stänger den och bestämmer dig för att aktivera Cortana Intelligence använder du den assisterade inställningsguiden eller en manuell process.  

**Obs:** du kan alternativt använda förebyggande webbtjänsten. Mer information finns i [skapa och använda egna förebyggande webbtjänsten för kassaflödesprognoser](#AnchorText).  

Så här använder du guiden för assisterad installation:  

1. I rollcentret Revisor, under diagrammet **kassaflödesprognos** väljer du åtgärden **Öppna assisterad installation**.  
2. Fyll i fälten som behövs i varje steg i guiden.  
3. På startsidan väljer du **kassaflödesprognos** ovanför diagrammet, och sedan **Omberäkna prognos**.  

Så här använder du en manuell process:  

1. I rollcentret revisor söker du **Kassaflödesinställningar**, och väljer sedan relaterad länk.  
2. Expandera snabbfliken **Cortana Intelligence** och välj sedan kryssrutan **Cortana Intelligence aktiverad**.  
3. På startsidan väljer du **kassaflödesprognos** ovanför diagrammet, och sedan **Omberäkna prognos**.  

**Tips:** Beakta längden för perioderna som tjänsten ska använda i dess beräkningar. Ju mer information som du anger, desto mer exakta kommer prognoserna att vara. Se upp för stora avvikelser i perioder. De kommer också att påverka prognoserna. Om Cortana Intelligence inte hittar tillräckligt med data, eller om data varierar mycket, kommer tjänsten inte att utföra någon prognos.  

## <a name="AnchorText"> </a>Skapa och använda egna förebyggande webbtjänsten för kassaflödesprognoser
Du kan också skapa egna förebyggande webbtjänsten som bygger på en allmän modell med namnet **Prognosmodellen för Microsoft Dynamics 365 for Financials**. Den här förebyggande modellen finns online i galleriet Cortana Intelligence. För att använda modellen gör du följande:  

1. Öppna en webbläsare och gå du till [Cortana Intelligence-galleriet](https://go.microsoft.com/fwlink/?linkid=828352)  
2. Sök efter **Prognosmodellen för Microsoft Dynamics 365 för Ekonomi** och öppna sedan modellen i Azure Machine Learning Studio.  
3. Använd ditt Microsoft-konto för att registrera dig för en arbetsyta och kopiera sedan modellen.  
4. Kör modellen och publicera den som en webbtjänst.  
5. Gör en anteckning av API-URL och API-nyckel. Du använder denna information för en kassaflödesinställningar.  
6. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger **Kassaflödesinställningar** och väljer sedan relaterad länk.  
7. Expandera snabbfliken **Cortana Intelligence** och fyll sedan i fälten.  

## <a name="see-also"></a>Se även
[Analysera kassaflödet i företaget](finance-analyze-cash-flow.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

