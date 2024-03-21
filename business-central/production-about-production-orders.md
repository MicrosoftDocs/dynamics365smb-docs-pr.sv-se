---
title: Om produktionsorder
description: Läs produktionsorder används för att hantera omvandlingen av inköpt material till producerade artiklar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000813, 99000814, 99000815, 99000816, 99000829, 99000830, 99000831, 99000832, 99000833, 99000838, 99000839, 99000867, 99000868, 99000882, 99000897, 99000898, 99000900, 99000912, 99000913, 99000914, 99000917'
ms.date: 06/22/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="about-production-orders"></a>Om produktionsorder

Produktionsorder används för att hantera omvandlingen av inköpt material till producerade artiklar. Produktionsorder dirigerar arbete via olika produktions- eller maskingrupper i fabriken.  

Före produktion utför de flesta företag inköpsplanering, vanligtvis en gång i veckan, för att beräkna hur många produktionsorder och inköpsorder som ska köras för att uppfylla veckans försäljningsbehov. Inköpsorder motsvarar komponenter som krävs enligt produktionsstrukturen för att producera slutartiklarna.

Produktionsorder är centrala komponenter i programmets produktionsfunktion och de innehåller följande information:  

- Produkter planerade för produktion  
- Material som krävs för planerade produktionsorder  
- Produkter som precis har tillverkats  
- Material som redan har valts ut  
- Produkter som tillverkats tidigare  
- Material som har använts i tidigare produktionsoperationer  

Produktionsorder är startpunkter för:  

- Planering av framtida produktion  
- Kontroll av aktuell produktion  
- Spårning av slutförd produktion  

## <a name="production-order-creation"></a>Skapa produktionsorder
Du kan skapa produktionsorder manuellt på orderbasis på sidan **Produktionsorder**. Produktionsorder kan även skapas på sidan **Förs.orderplanering** eller **Orderplanering**. Flera order skapas på sidan **Planeringsförslag**.  

Produktionsorder kan skapas med hjälp av information från:  

- Artiklar  
- Artikelstrukturer
- Operationsföljder  
- Maskingrupper  
- Produktionsgrupper  

## <a name="limitations-on-production-order-creation"></a>Begränsningar vid skapande av produktionsorder
Produktionsorder reserveras automatiskt och spåras till deras ursprung när:  

- Skapas från **[planeringsförslaget](production-how-to-run-mps-and-mrp.md)**.  
- Skapas från sidan **[Försäljningsorderplanering](production-how-to-create-production-orders-from-sales-orders.md)**  
- Skapas från sidan **[Orderplanering](production-how-to-plan-for-new-demand.md)**  
- Använda funktionen **[Omplanering](production-how-to-replan-refresh-production-orders.md)** på produktionsorder  

Mer information finns i [Spåra relationer mellan tillgång och efterfrågan](production-how-track-demand-supply.md).

Produktionsorder som skapas på annat sätt reserveras och spåras inte automatiskt.   

## <a name="production-order-status"></a>Status för produktionsorder
Statusen för en produktionsorder styr hur den bearbetas i programmet. Formen på och innehållet i produktionen föreskrivs av orderns status. Produktionsorder visas i olika sidor beroende på status. Du kan inte ändra statusen för en produktionsorder manuellt. Du måste använda funktionen **Ändra status** i den enskilda produktionsordern eller i fönstret **Ändra produktionsorderstatus**.  

### <a name="simulated-production-order"></a>Simulerad produktionsorder
Den simulerade produktionsorder är unik på grund av följande egenskaper:  

- Precis som namnet antyder är denna produktionsorder en simulering, som huvudsakligen används för anbudsgivning och kostnadskalkylering, till exempel när avdelningen för forskning och utveckling vill ha en kostnadsberäkning på en föreslagen artikel. En simulerad produktionsorder fungerar som ett exempel på en produktionsorder.  
- En simulerad produktionsorder påverkar inte planeringen av order. I planeringen (prod.program och nettobehov) beaktas inte simulerade produktionsorder, och de påverkar inte heller planeringen. Simulerade produktionsorder kan inte heller användas som mall eftersom de försvinner när du ändrar deras status.  

### <a name="planned-production-order"></a>Planerad produktionsorder
Den planerade produktionsordern är unik på grund av följande egenskaper:  

- Du kan automatiskt skapa en planerad produktionsorder från en försäljningsorder.  
- Planerade produktionsorder är som släppta produktionsorder, och tillhandahåller indata för planering av kapacitetsbehov genom att visa det totala kapacitetsbehovet efter produktionsgrupp eller maskingrupp.  
- En planerad produktionsorder representerar den bästa uppskattningen av framtida beläggning för produktionsgruppen eller maskingruppen baserat på tillgänglig information. Planerade produktionsorder genereras från planering, men kan också skapas manuellt. Det är inte särskilt praktiskt att skapa planerade produktionsorder manuellt eftersom dessa tas bort under efterföljande planeringsgenerering.  
- Genereringen av planerade produktionsorder i planeringen resulterar i ett föreslaget "planerat orderutsläpp" som inkluderar antal, utsläppsdatum och förfallodatum. Logiken för planeringssystemet baseras på återanskaffningssystemet, beställningsprinciper och orderändringar som påträffas i planeringsprocessen för nettobehov.  
- Du kan granska beläggningen för varje produktions- eller maskingrupp i operationsföljden för den planerade produktionsordern om du vill se vilken effekt en planerad produktionsorder har.  

### <a name="firm-planned-production-order"></a>Fast planerad produktionsorder
Den fast planerade produktionsordern är unik på grund av följande egenskaper:  

- Du kan automatiskt skapa en fast planerad produktionsorder från en försäljningsorder.  
- En fast planerad produktionsorder fungerar som platshållare i planeringsschemat för framtida arbete som släpps ut till fabriken.  
- En fast planerad produktionsorder kan genereras från planering eller skapas manuellt från försäljningsorder. Den tas inte bort under efterföljande planering.  
- Genereringen av fast planerade produktionsorder i planeringen resulterar i ett föreslaget "planerat orderutsläpp" som inkluderar antal, utsläppsdatum och förfallodatum. Logiken för planeringssystemet baseras på återanskaffningssystemet, beställningsprinciper och orderändringar som påträffas i planeringsprocessen för nettobehov.  
- Du kan granska beläggningen för varje produktions- eller maskingrupp i operationsföljden för den fast planerade produktionsordern om du vill se vilken effekt en planerad produktionsorder har.  

### <a name="released-production-order"></a>Släppt produktionsorder
Den släppta produktionsordern är unik på grund av följande egenskaper:  

- Du kan automatiskt skapa en släppt produktionsorder från en försäljningsorder.  
- När en produktionsorder har släppts ut innebär det inte nödvändigtvis att material har plockats eller att arbetet fysiskt har flyttats till den första operationen.  
- I de fall produktionstypen Tillverka-mot-order används, är det inte ovanligt att en släppt produktionsorder skapas direkt efter registreringen av försäljningsordern.  
- Faktisk materialförbrukning och produktutflöde kan registreras manuellt med en släppt produktionsorder. Dessutom sker rensning av förbrukning och produktutflöde endast automatiskt för släppta produktionsorder.  

### <a name="finished-production-order"></a>Färdiga produktionsorder
Den färdiga produktionsordern är unik på grund av följande egenskaper:  

- En färdig produktionsorder är vanligtvis en produktionsorder som redan har tillverkats.  
- Att färdigställa produktionsordern är en viktig uppgift när det gäller att slutföra livscykeln för kostnadsberäkning för artikeln som tillverkas. Kostnadsberäkningen kan justeras och stämmas av när du färdigställer en produktionsorder.  
- Färdiga produktionsorder används för rapportering av statistik och för att stödja möjligheten att gå tillbaka till andra order (t. ex. försäljnings-, produktions- och inköpsorder). Med möjligheten att gå tillbaka till en färdig produktionsorder kan du granska den detaljerade historiken.  
- Färdiga produktionsorder kan inte ändras.  

## <a name="production-order-execution"></a>Utföra en produktionsorder
När du har skapat och planerat en produktionsorder måste den släppas ut till fabriken för att utföras. När ordern utförs registrerar du:  

- Material som plockas eller förbrukas  
- Hur lång tid det tog att bearbeta ordern  
- Antal av den tillverkade överordnade artikeln  

Den här informationen kan registreras manuellt, eller via automatisk rapportering, enligt inställningarna i fältet Bokföringsmetod för artikeln och produktionsgruppen.  

### <a name="material-consumption"></a>Materialförbrukning
I programmet finns en mängd olika alternativ för hur ett tillverkningsföretag kan vilja registrera materialförbrukning. Materialförbrukning kan till exempel registreras manuellt, vilket kan vara önskvärt om det ofta förekommer komponentersättningar eller kassation som är större än förväntat.  

Förbrukningen av material kan bearbetas via [förbrukningsjournalen](production-how-to-post-consumption.md), men kan även registreras automatiskt i programmet, även kallat för automatisk rapportering (bokföring). Rapporteringsmetoderna är:  

- Manuell  
- Framåt  
- Bakåt  

Manuell rapportering av förbrukning använder förbrukningsjournalen för att specificera plockning av material.  

Framåt rapportering av förbrukning förutsätter att den förväntade kvantiteten av allt material för hela ordern förbrukas när en produktionsorder släpps, om inte verksamhetsföljdslänkkoder används. Om du använder operationsföljdslänkkoder, förbrukas materialet när starten på operationssteget registreras i utflödesjournalen. Om du vill använda metoden Framåt för hela produktionsordern måste du göra två saker:  

- Du måste markera metoden Framåt på respektive artikelkort för alla artiklar på toppnivån i produktionsstrukturen.  
- Du måste ta bort alla verksamhetsföljdslänkkoder i produktionsstrukturen.  

Bakåt rapportering av förbrukning registrerar den faktiska kvantiteten av allt material som plockas eller förbrukas när statusen för en produktionsorder ändras till *Färdig*, om inte verksamhetsföljdslänkkoder används. Om du använder verksamhetsföljdslänkkoder, förbrukas materialet efter det att ett antal av den överordnade artikeln registreras för verksamhetssteget i utflödesjournalen.  

Bokföringsmetoden kopieras från artikelkortet när produktionsordern uppdateras. Eftersom bokföringsmetoden för varje produktionsorderkomponent styr hur och när förbrukningen registreras, är det viktigt att observera att du kan ändra bokföringsmetoden för särskilda artiklar direkt i produktionsordern. 

Mer information finns i [Bokför komponenter enligt verksamhetens utflöde](production-how-to-flush-components-according-to-operation-output.md)

### <a name="production-output"></a>Produktionsutflöde
Med hjälp av programmet kan du spåra hur mycket tid som läggs ned på arbetet med en produktionsorder, förutom att registrera det antal som tillverkas. Den här informationen kan hjälpa dig att mer exakt fastställa produktionskostnaden. Detta är även användbart för tillverkare som använder ett standardsystem för kostnadsberäkning och som kanske vill registrera faktisk information för att hjälpa dem att utveckla bättre riktlinjer.  

Utflöde kan bearbetas via [utflödesjournalen](production-how-to-post-output-quantity.md), men kan även registreras automatiskt i programmet. Bokföringsprogrammet kopieras då automatiskt från produktionsgrupps- eller maskingruppskortet till verksamhetsföljden för produktionsordern när du uppdaterar. Precis som för materialförbrukning, finns det tre rapporteringsmetoder för utflöde:  

- Manuell  
- Framåt  
- Bakåt  

Metoden Manuell använder utflödesjournalen för att ange den tid som har förbrukats och producerat antal.  

Metoden Framåt registrerar det förväntade utflödet (och tid), som automatiskt registreras när en produktionsorder släpps. Operationsföljdslänkkoder används inte när utflödet bokförs framåt.  

Metoden Bakåt registrerar det förväntade utflödet (och tid), som automatiskt registreras när en produktionsorder färdigställs. Operationsföljdslänkkoder används inte när utflödet bokförs bakåt.  

### <a name="posting-consumption-and-output"></a>Bokföra förbrukning och utflöde
Du kan använda valfri kombination av automatisk bokföring och manuellt registrerad information för både förbrukning och utflöde. Exempelvis kanske du vill bokföra komponenter framåt automatiskt, men ändå använda förbrukningsjournalen för att registrera kassation. På liknande sätt kanske du vill registrera utflöde automatiskt, men använda utflödesjournalen för att registrera kassation för den överordnade artikeln eller extra tid som har lagts ned på ordern.  

Om du anger förbrukning och utflöde manuellt måste du bestämma den sekvens i vilken du kommer att registrera den här informationen. Du kan registrera förbrukningen först och använda en genvägsmetod för att registrera informationen som baseras på det förväntade utflödeantalet. Eller så kan du ange utflödet först med hjälp av funktionen **Expandera oper.följd** . Du skulle sedan registrera förbrukning baserat på faktiskt utflödeantal.  

### <a name="production-journal"></a>Produktionsjournal
I [produktionsjournalen](production-how-to-register-consumption-and-output.md) kombineras funktionerna hos förbrukningsjournalen och utflödesjournalen i en enda journal. Produktionsjournalen kan öppnas direkt från den släppta produktionsordern.  

Syftet med produktionsjournalen är att tillhandahålla ett enda gränssnitt som du använder för att registrera förbrukning och utflöde från en produktionsorder.  

Produktionsjournalen innehåller en enkel vy och ger dig möjlighet att:  

- På ett enkelt sätt registrera utflöde och förbrukning relaterat till en produktionsorder.  
- Koppla komponenterna till operationer.  
- Koppla faktiska data för operationen till standardkostnadsförslag i operationsföljden och komponentraderna i produktionsordern.  
- Bokföra och skriva ut en översikt över registrerade operationsdata för produktionsordern.  

Med produktionsjournalen kan du utföra många av de funktionerna som du kan med förbruknings- och utflödesjournalen. Dimensioner, artikelspårning och lagerställesinnehåll hanteras på samma sätt som i förbruknings- och utflödesjournalen.  

Produktionsjournalen skiljer sig från förbruknings- och utflödesjournalerna på följande sätt:  

- Den anropas direkt från en släppt produktionsorderrad och är förinställd med relevanta data.  
- Du tillåts definiera vilka typer av komponenter som ska hanteras utifrån ett bokföringsmetodfilter i journalen.  
- Antal och tid som redan har bokförts för ordern, visas längst ned i journalen som faktiska transaktioner.  
- Fält där du inte behöver registrera information är tomma och kan inte redigeras.  
- Användaren kan ange hur utflödeantal ska förinställas i journalen, till exempel att den sista operationen måste ha värdet noll för utflödeantalet.  
- Om du stänger journalen utan att bokföra ändringarna, visas ett begärandemeddelande som tillåter att du stannar kvar i journalen.  
- I produktionsjournalen visas operationer och komponenter tillsammans i en logisk struktur som ger en översikt över produktionsprocessen.  

I produktionsjournalen bokförs förbrukningsantal som negativa artikeltransaktioner, utflödeantal bokförs som positiva transaktioner och tidsinsats bokförs som kapacitetstransaktioner.  

## <a name="see-also"></a>Se även
[Produktion](production-manage-manufacturing.md)
[Konfigurera produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
