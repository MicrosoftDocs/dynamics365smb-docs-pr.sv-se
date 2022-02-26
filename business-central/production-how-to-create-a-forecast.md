---
title: Skapa en efterfrågeprognos
description: Lära dig mer om funktionen för efterfrågeprognos och hur du kan skapa försäljnings- och produktionsprognoser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9245, 99000919, 99000921, 99000922
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: f966b73f4917bf803c0f8c4c92eefcd222aeeea7
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971385"
---
# <a name="create-a-demand-forecast"></a>Skapa en efterfrågeprognos

Du kan skapa försäljnings- och produktionsprognoser på sidan **efterfrågeprognos**.  

Prognosfunktionen används för att skapa prognostiserat behov, faktiskt behov skapas från försäljnings – och produktionsorder. Under tiden som produktionsprogrammet skapas nettoberäknas prognosen mot försäljnings – och produktionsorder. Alternativet *Komponent* på prognosen avgör vilken typ av krav som bör beaktas i nettoberäkningen. Om prognosen gäller en försäljningsartikel, nettoberäknas endast försäljningsorder för prognosen. Om den är för komponenter, nettoberäknas bara den härledda efterfrågan från produktionsorderkomponenter i prognosen.  

Med prognoser kan företaget skapa hypotetiska scenarier och på ett kostnadseffektivt sätt planera för och tillgodose behov. Exakt och korrekt prognostisering kan vara avgörande för nivån av kundtillfredsställelse med hänsyn till orderlöften och punktliga leveranser.  

## <a name="sales-forecasts-and-production-forecasts"></a>Försäljningsprognoser och produktionsprognoser

Funktionen för produktionsprognos kan användas för att skapa försäljnings- eller produktionsprognoser, i olika kombinationer eller var för sig. De flesta företag som tillverkar mot order har t. ex. inga färdiga varor i lager eftersom varje artikel tillverkas när den beställs. Det är viktigt att kunna förutse order (försäljningsprognos) för att få en rimlig genomloppstid på de färdiga varorna (produktionsprognos). Komponentdelar med långa leveranstider kan t. ex. försena produktionen om dessa inte har beställts eller finns i lager.  

- Försäljningsprognosen är försäljningsavdelningens bästa gissning om vad som kommer att säljas i framtiden, och anges efter artikel och period. Försäljningsprognoser lämpar sig inte alltid för produktion.  
- Produktionsprognosen är produktionsplanerarens bedömning av hur många slutartiklar och härledda delprodukter som ska produceras under en viss period för att uppfylla försäljningsprognosen.  

I de allra flesta fall ändrar produktionsplanerare försäljningsprognosen så att denna stämmer med produktionsvillkoren, men ändå uppfyller försäljningsprognosen.  

Du skapar prognoser manuellt på sidan **efterfrågeprognos**. Flera prognoser kan särskiljas i systemet med hjälp av namn och typ. Prognoser kan kopieras och redigeras efter behov. Observera att endast en prognos i taget gäller för planering.  

Prognosen består av ett antal poster som motsvarar artikelnummer, prognosdatum och prognostiserat antal. Prognosen för en artikel täcker en period som definieras av prognosdatumet och prognosdatumet för nästa (efterföljande) prognospost. Med hänsyn till planering bör det prognostiserade antalet vara tillgängligt vid behovsperiodens start.  

Du måste ange en prognos av typen *Försäljningsartikel*, *Komponent* eller *Både och*. Prognostypen *Försäljningsartikel* används för försäljningsprognoser. Produktionsprognosen skapas med hjälp av typen *Komponent*. Prognostypen *Både och* används endast för att ge planeraren en översikt över både försäljnings- och produktionsprognosen. Prognostransaktioner kan inte redigeras med det här alternativet. När du anger prognostyperna här, kan du använda samma kalkylblad för att ange försäljningsprognosen som du använder för att ange en produktionsprognos, och använda samma blad för att visa båda prognoser samtidigt. Observera att dessa olika indata (försäljning och produktion) bearbetas olika i systemet vid beräkning av planering, beroende på artikel-, tillverknings- och produktionsinställningarna.  

## <a name="component-forecast"></a>Komponentprognos

Komponentprognosen kan ses som en alternativ prognos med hänsyn till en överordnad artikel. Detta kan t. ex. vara användbart om planeraren kan uppskatta behovet av en komponent.  

Eftersom komponentprognosen är utformad för att definiera alternativ för en överordnad artikel, bör komponentprognosen vara mindre än eller lika med försäljningsartikelns prognoskvantitet. Om komponentprognosen är större än prognosen för försäljningsartikeln behandlas skillnaden mellan dessa två typer av prognoser som oberoende behov.  

## <a name="forecasting-periods"></a>Prognosperioder

Prognosperioden är giltig från startdatumet fram till det datum då nästa prognos börjar. Det här tidsintervallet ger dig flera alternativ för att infoga behov på ett särskilt datum i en period. Du rekommenderas därför att inte ändra prognosperiodens omfattning om du inte vill flytta alla prognostransaktioner till startdatumet för den här perioden.  

## <a name="forecast-by-locations"></a>Prognos efter lagerställen

På sidan **Produktionsinställningar** kan du ange om du vill beakta de platser som definieras i prognoser när du beräknar planer. 

### <a name="use-forecast-by-locations"></a>Använd prognos efter lagerställen

Om du aktiverar växlingen **Använd prognos efter lagerställe** kommer [!INCLUDE[prod_short](includes/prod_short.md)] att följa de lagerställekoder som anges för respektive post för efterfrågeprognos och beräkna den återstående prognosen för respektive lagerställe.  

Överväg följande exempel: Ditt företag köper och säljer artiklar på två lagerställen: ÖST och VÄST. För båda lagerställen har du konfigurerat en omorganisationspolicy för parti-till-parti. Du skapar en prognos för de två lagerställena:

- 10 enheter för lagerplats ÖST
- 4 enheter för lagerplats VÄST

Därefter skapar du en försäljningsorder med kvantiteten 12 på lagerställe VÄST. Planeringssystemet föreslår att du gör följande:

- Återanskaffning av 10 enheter för lagerställe ÖST, baserat på data från prognosen.  
- Återanskaffning av 12 enheter för lagerställe VÄST, baserat på försäljningsordern. De fyra delar som angavs i prognosen förbrukas helt med det faktiska behov som anges i försäljningsordern. Mer information finns i [Prognostiserad efterfrågan minskas av försäljningsorder](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

> [!NOTE]  
> Om platsbaserade prognoser visas separat kanske den övergripande prognosen inte är representativ.

### <a name="do-not-use-forecast-by-locations"></a>Använd inte prognos efter lagerställen

Om du avaktiverar **Använd prognos efter plats** kommer [!INCLUDE[prod_short](includes/prod_short.md)] att ignorera platskoder som anges för respektive behovsprognospost och samla prognoserna till en prognos för tomma platser.  

Överväg följande exempel: Ditt företag köper och säljer artiklar på två lagerställen: ÖST och VÄST. För båda lagerställen har du konfigurerat en omorganisationspolicy för parti-till-parti. Du skapar en prognos för de två lagerställena:

- 10 enheter för lagerplats ÖST
- 4 enheter för lagerplats VÄST

Därefter skapar du en försäljningsorder med kvantiteten 12 på lagerställe VÄST. Planeringssystemet föreslår att du gör följande:

- Återanskaffning av 12 enheter för lagerställe VÄST, baserat på försäljningsordern.  
- Återanskaffning av två delar för tom plats. De 10 och fyra delar som angavs i prognosen förbrukas delvis av det faktiska behov som anges i försäljningsordern. [!INCLUDE[prod_short](includes/prod_short.md)] ignorerade de lagerställekoder som har angetts av användaren och använder en tom plats i stället.  

> [!NOTE]  
> Du kan ange ett filter efter lagerställen, men det kan hända att de platsbaserade resultaten inte matchar planeringsresultaten utan filter.

## <a name="to-create-a-demand-forecast"></a>Att skapa en efterfrågeprognos

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **efterfrågeprognos** och väljer sedan relaterad länk.  
2. På snabbfliken **Allmänt**, välj en prognos i fältet **efterfrågeprognosnamn**. Flera prognoser kan särskiljas med hjälp av namn och prognostyp.  
3. Gå till fältet **Lagerställefilter** och markera den plats som den här prognosen ska gälla för.
4. I fältet **Visa efter** för att ändra perioden som visas i varje kolumn. Du kan välja mellan följande intervall: **Dag**, **Vecka**, **Månad**, **Kvartal**, **År** eller **Bokföringsperiod** som ställs in i ditt ekonomiområde.

> [!NOTE]  
> Det kan vara värt att fundera på vilket tidsintervall du vill använda för framtida prognoser så att tidsintervallen är konsekventa. När du anger ett prognosantal börjar detta prognosantal att gälla på den första dagen i det tidsintervall som du väljer. Om du till exempel väljer månad som tidsintervall, anger du prognosantalet på den första dagen i månaden. Om du väljer kvartal, anger du antalet på den första dagen i den första månaden i kvartalet.

5. I fältet **Visa som** väljer du hur prognosantalet ska visas för tidsintervallet. Om du väljer **Nettoförändring** visas nettoförändringen i saldot för tidsintervallet. Om du väljer **Saldo t.o.m. datum** visar sidan saldot per den sista dagen i tidsintervallet.  
6. Gå till fältet **Prognostyp** och markera **Försäljningsartikel**, **Komponent** eller **Både och**. Om du väljer **Försäljningsartikel** eller **Komponent** kan du redigera antalet utifrån period. Om du väljer **Både och** kan du inte redigera antalet, men du kan klicka på listpilen och granska efterfrågeprognostransaktionerna.  
7. Ange ett **datumfilter** om du vill begränsa mängden information som visas.  
8. På snabbfliken **Matris för efterfrågeprognos** anger du prognostiserade kvantiteter genom att skriva in en kvantitet i cellen som representerar en artikel på ett visst datum eller en viss period. Observera att uppslagsknappen i tomma celler öppnar en tom sida som anger att du måste ange ett värde manuellt.   

> [!NOTE]  
> Du kan också redigera en befintlig prognos. På sidan **Matris för efterfrågeprognos** väljer du åtgärden **Kopiera efterfrågeprognos** och fyller i sidan **efterfrågeprognos** med en befintlig prognos. Du kan sedan redigera antalet.  

## <a name="see-also"></a>Se även

[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
