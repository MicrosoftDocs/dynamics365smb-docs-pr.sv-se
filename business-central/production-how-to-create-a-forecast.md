---
title: Så här skapar du en efterfrågeprognos | Microsoft Docs
description: Du kan skapa försäljnings- och produktionsprognoser på sidan **efterfrågeprognos**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8ae3e142946ff968a1b1357df1a1634734c0392c
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2883388"
---
# <a name="create-a-demand-forecast"></a>Skapa en efterfrågeprognos
Du kan skapa försäljnings- och produktionsprognoser på sidan **efterfrågeprognos**.  

Prognosfunktionen används för att skapa prognostiserat behov, faktiskt behov skapas från försäljnings - och produktionsorder. Under tiden som produktionsprogrammet skapas nettoberäknas prognosen mot försäljnings - och produktionsorder. Alternativet *Komponent* på prognosen avgör vilken typ av krav som bör beaktas i nettoberäkningen. Om prognosen gäller en försäljningsartikel, nettoberäknas endast försäljningsorder för prognosen. Om den är för komponenter, nettoberäknas bara den härledda efterfrågan från produktionsorderkomponenter i prognosen.  

Med prognoser kan företaget skapa hypotetiska scenarier och på ett kostnadseffektivt sätt planera för och tillgodose behov. Exakt och korrekt prognostisering kan vara avgörande för nivån av kundtillfredsställelse med hänsyn till orderlöften och punktliga leveranser.  

## <a name="sales-forecasts-and-production-forecasts"></a>Försäljningsprognoser och produktionsprognoser  
Funktionen för produktionsprognos kan användas för att skapa försäljnings- eller produktionsprognoser, i olika kombinationer eller var för sig. De flesta företag som tillverkar mot order har t.ex. inga färdiga varor i lager eftersom varje artikel tillverkas när den beställs. Det är viktigt att kunna förutse order (försäljningsprognos) för att få en rimlig genomloppstid på de färdiga varorna (produktionsprognos). Komponentdelar med långa leveranstider kan t.ex. försena produktionen om dessa inte har beställts eller finns i lager.  

-   Försäljningsprognosen är försäljningsavdelningens bästa gissning om vad som kommer att säljas i framtiden, och anges efter artikel och period. Försäljningsprognoser lämpar sig inte alltid för produktion.  
-   Produktionsprognosen är produktionsplanerarens bedömning av hur många slutartiklar och härledda delprodukter som ska produceras under en viss period för att uppfylla försäljningsprognosen.  

I de allra flesta fall ändrar produktionsplanerare försäljningsprognosen så att denna stämmer med produktionsvillkoren, men ändå uppfyller försäljningsprognosen.  

Du skapar prognoser manuellt på sidan **efterfrågeprognos**. Flera prognoser kan särskiljas i systemet med hjälp av namn och typ. Prognoser kan kopieras och redigeras efter behov. Observera att endast en prognos i taget gäller för planering.  

Prognosen består av ett antal poster som motsvarar artikelnummer, prognosdatum och prognostiserat antal. Prognosen för en artikel täcker en period som definieras av prognosdatumet och prognosdatumet för nästa (efterföljande) prognospost. Med hänsyn till planering bör det prognostiserade antalet vara tillgängligt vid behovsperiodens start.  

Du måste ange en prognos av typen *Försäljningsartikel*, *Komponent* eller *Både och*. Prognostypen *Försäljningsartikel* används för försäljningsprognoser. Produktionsprognosen skapas med hjälp av typen *Komponent*. Prognostypen *Både och* används endast för att ge planeraren en översikt över både försäljnings- och produktionsprognosen. Prognostransaktioner kan inte redigeras med det här alternativet. När du anger prognostyperna här, kan du använda samma kalkylblad för att ange försäljningsprognosen som du använder för att ange en produktionsprognos, och använda samma blad för att visa båda prognoser samtidigt. Observera att dessa olika indata (försäljning och produktion) bearbetas olika i systemet vid beräkning av planering, beroende på artikel-, tillverknings- och produktionsinställningarna.  

## <a name="component-forecast"></a>Komponentprognos  
Komponentprognosen kan ses som en alternativ prognos med hänsyn till en överordnad artikel. Detta kan t.ex. vara användbart om planeraren kan uppskatta behovet av en komponent.  

Komponentprognosen ska vara lika med eller mindre än det prognostiserade antalet försäljningsartiklar eftersom komponentprognosen är utformad för att definiera alternativ för en överordnad artikel. Om komponentprognosen är större än prognosen för försäljningsartikeln behandlas skillnaden mellan dessa två typer av prognoser som oberoende behov.  

## <a name="forecasting-periods"></a>Prognosperioder  
 Prognosperioden är giltig från startdatumet fram till det datum då nästa prognos börjar. Det här tidsintervallet ger dig flera alternativ för att infoga behov på ett särskilt datum i en period. Du rekommenderas därför att inte ändra prognosperiodens omfattning om du inte vill flytta alla prognostransaktioner till startdatumet för den här perioden.  

## <a name="forecast-by-locations"></a>Prognos efter lagerställen  
Detta kan anges i produktionsinställningarna om du vill filtrera prognos efter lagerställe när en plan beräknas. Observera dock att den övergripande prognosen kanske inte är representativ om du granskar lagerställebaserade prognoser var för sig.

## <a name="to-create-a-demand-forecast"></a>Att skapa en efterfrågeprognos

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **efterfrågeprognos** och välj sedan relaterad länk.  
2.  På snabbfliken **Allmänt**, välj en prognos i fältet **efterfrågeprognosnamn**. Flera prognoser kan särskiljas med hjälp av namn och prognostyp.  
3.  Gå till fältet **Lagerställefilter** och markera den plats som den här prognosen ska gälla för.  
4.  Gå till fältet **Prognostyp** och markera **Försäljningsartikel**, **Komponent** eller **Både och**. Om du väljer **Försäljningsartikel** eller **Komponent** kan du redigera antalet utifrån period. Om du väljer **Både och** kan du inte redigera antalet, men du kan klicka på listpilen och granska efterfrågeprognostransaktionerna.  
5.  Ange ett **datumfilter** om du vill begränsa mängden information som visas.  
6.  Gå till snabbfliken **Matris för efterfrågeprognos** och ange prognosantalet för **Försäljningsartikel** eller **Komponent** för olika perioder.  
7.  Gå till snabbfliken **Matrisalternativ** och ange tidsintervallet i fältet **Visa per** för att ändra perioden som visas i respektive kolumn. Du kan välja mellan följande intervall: **Dag**, **Vecka**, **Månad**, **Kvartal**, **År** eller **Bokföringsperiod** som ställs in i Ekonomihantering.  

    > [!NOTE]  
    >  Det kan vara värt att fundera på vilket tidsintervall du vill använda för framtida prognoser så att tidsintervallen är konsekventa. När du anger ett prognosantal börjar detta prognosantal att gälla på den första dagen i det tidsintervall som du väljer. Om du till exempel väljer månad som tidsintervall, anger du prognosantalet på den första dagen i månaden. Om du väljer kvartal, anger du antalet på den första dagen i den första månaden i kvartalet.  

8.  I fältet **Visa som** väljer du hur prognosantalet ska visas för tidsintervallet. Om du väljer **Nettoförändring** visas nettoförändringen i saldot för tidsintervallet. Om du väljer **Saldo t.o.m. datum** visar sidan saldot per den sista dagen i tidsintervallet.  

> [!NOTE]  
>  Du kan också redigera en befintlig prognos. På sidan **Matris för efterfrågeprognos** väljer du åtgärden **Kopiera efterfrågeprognos** och fyller i sidan **efterfrågeprognos** med en befintlig prognos. Du kan sedan redigera antalet.  

## <a name="see-also"></a>Se även  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
