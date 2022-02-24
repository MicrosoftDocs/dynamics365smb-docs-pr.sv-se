---
title: Genomgång - Planera leveranser manuellt | Microsoft Docs
description: Den här genomgången demonstrerar processen för att planera leveransorder som uppfyller efterfrågan. Du kan inleda leveransplaneringen vid fasta tidpunkter, exempelvis varje morgon eller varje måndag, eller när du får ett meddelande från försäljningsavdelningen eller produktionen, beroende på typen av efterfrågan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0da12af6eb5a165c717cd112735a91aebe3ae85d
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876973"
---
# <a name="walkthrough-planning-supplies-manually"></a>Genomgång: Planera leveranser manuellt

**Obs**! i den här genomgången måste utföras på ett demonstrationsföretag, med alternativet **Fullständig utvärdering - fullständig exempeldata** som är tillgängliga i begränsat läge. Mer information finns i [Skapa en miljö för begränsat lägel](across-how-create-sandbox-environment.md).

Den här genomgången demonstrerar processen för att planera leveransorder som uppfyller efterfrågan. Du kan inleda leveransplaneringen vid fasta tidpunkter, exempelvis varje morgon eller varje måndag, eller när du får ett meddelande från försäljningsavdelningen eller produktionen, beroende på typen av efterfrågan. I den här genomgången använder du sidan **Orderplanering**, som är ett enkelt leveransplaneringsverktyg som bygger på manuellt beslutsfattande snarare än parameterbaserad automatisk planering.  

## <a name="about-this-walkthrough"></a>Om den här genomgången  
 I den här genomgången tas följande aktiviteter upp:  

-   Planera en inköpsorder för komponenter till produktionen.  
-   Planera en överföringsorder för att uppfylla försäljningsbehov.  
-   Planera en produktionsorder för en artikel med flera nivåer.  

## <a name="roles"></a>Roller  
 Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:  

-   Produktionsplanerare  
-   Inköpsagent  
-   Försäljningsorderhandläggare  

## <a name="prerequisites"></a>Förutsättningar  
 Innan du påbörjar genomgången måste du installera [!INCLUDE[d365fin](includes/d365fin_md.md)]. Följande ändringar måste göras i databasen:  

-   Ta bort alla befintliga försäljningsorder på cyklar.  
-   Skapa en försäljningsorder på tio cyklar på lagerstället BLÅ.  
-   Ta bort alla planerade och fast planerade produktionsorder. Ta inte bort påbörjade order med transaktioner som redan har bokförts.  

 En regel är att de data som föreslås i genomgången ska användas eftersom dessa data har alla nödvändiga poster.  

## <a name="story"></a>Situation  
 Eduardo är produktionsplanerare på ett litet tillverkande företag och håller på att planera produktions- och inköpsorder för att uppfylla behov.  

 Eftersom produkternas produktstrukturer har få nivåer och orderflödet är relativt lågt använder Eduardo sidan **Orderplanering** för att manuellt skapa leveransorder, en produktnivå i taget.  

 I en mer komplex produktionsmiljö används planeringsförslaget för att planera leveranser baserat på parametrar som omplaneringsperiod, säkerhetsledtid, beställningspunkt och batch-beräkningar av den sammanställda efterfrågan på alla produktnivåer.  

## <a name="setting-up-the-sample-data"></a>Ställa in exempeldata  
 Standarddemonstrationsföretaget CRONUS har för närvarande en stor mängd oplanerad efterfrågan. Under de olika planeringsaktiviteterna i den här genomgången måste du avvika från det realistiska verksamhetsflödet genom att ignorera efterfrågan med tidiga förfallodatum och i stället använda efterfrågan med senare förfallodatum.  

## <a name="using-the-order-planning-page"></a>Använda sidan Orderplanering  

Du kommer åt sidan **Orderplanering** från flera olika platser:  

-   Produktion, Planering  
-   Försäljning och marknadsföring, Orderbearbetning  
-   Inköp, Planering  
-   Du kan dessutom öppna den här sidan för en viss produktionsorder genom att välja åtgärden **Planering**.

### <a name="to-use-the-order-planning-page"></a>Så här använder du sidan Orderplanering  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Orderplanering** och välj sedan relaterad länk.  

     När sidan **Orderplanering** har öppnats måste en plan beräknas för att visa den nya efterfrågan sedan den senaste beräkningen.  

2.  Välj åtgärden **Skapa inköpsförslag**.  

     Planeringssystemet analyserar alla ny behov som har tillkommit, exempelvis ny försäljning, förändrad försäljning och produktionsorder.  

     Den kvantitet som behövs för respektive efterfrågerad beräknas utifrån den totala tillgången. Beräkningen görs per order. Det betyder att den order som innehåller efterfrågan med det tidigaste förfallodatumet eller utleveransdatumet beräknas först. Därefter beräknas ytterligare efterfrågerader i samma ordning, oavsett förfallodatum eller utleveransdatum.  

3.  Se till att sidan **Orderplanering** är maximerad och att kolumnfälten har lagom storlek för att alla standardfältnamn ska synas.  

     När beräkningen är slutförd visas alla ej uppfyllda behov i sidan som reducerade orderrader sorterade efter behovsdatum.  

     Lägg märke till att CRONUS har flera order med ej uppfyllda behov. Varje planeringsrad i fetstil motsvarar en order, försäljningsorder eller produktionsorder, inklusive minst en orderrad med otillräcklig tillgång.  

4.  I fältet **Visa behov som** väljer du filtret **Alla behov**.  

     I fältet **Behovstyp** kan du välja vilka ordertyper som du vill visa.  

     Order som inte har några problem med tillgången visas inte. Om det inte finns några order när en plan beräknas visas ett meddelande och inga planeringsrader visas.  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a>Planera en inköpsorder för att uppfylla behov av komponenter  
 I den här proceduren skapar du en inköpsorder på komponenter som behövs för produktionen.  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a>Så här planerar du en inköpsorder för att uppfylla komponentbehovet i produktionen  

1.  Expandera den första raden (välj +-symbolen).  
2.  Välj den första behovsraden med artikel **LSU-15**, och välj sedan åtgärden **visa dokument**.  
3.  Stäng produktionsordern och återgå till sidan **Orderplanering**.  
4.  I fältet **Återanskaffningssystem** väljer du **Inköp**.  

     Standardvärdet är från artikelkortet, eller lagerställeenhetskortet, men det går att ändra till något av följande tre alternativ:  

    -   **Inköp** – Om du vill skapa en inköpsorder.  
    -   **Överföring** – Om du vill skapa en överföringsorder.  
    -   **Prod.order** – Om du vill skapa en produktionsorder.  

5.  I fältet **Leverera från** måste du välja något av följande alternativ enligt det återanskaffningssystem som du har markerat:  

    -   **Leverantör** – För inköp  
    -   **Lagerställe** – för överföringar  

     Om inte fältet fylls i visas ett felmeddelande när du försöker skapa leveransorderna.  

    > [!NOTE]  
    >  Om komponenterna har ett standardleverantörsnummer på artikelkorten är raderna förinställda.  

6.  Välj fältet **Leverera från**.  
7.  På sidan **Artikelns leverantörskatalog** väljer du åtgärden **Ny** och sedan leverantör **30000**.  
8.  Välj knappen **OK** om du vill återvända till sidan **Orderplanering**.  
9. Kopiera leverantörsnummer **30000** till de andra raderna för högtalarkomponenterna på den här produktionsordern.  

     Du är nu redo att skapa en inköpsorder.  

10. Välj åtgärden **Skapa order**. Sidan **Skapa leveransorder** öppnas.  
11. På snabbfliken **Orderplanering**, i fältet **Skapa order för** väljer du alternativet **Aktiv order**.  
12. På snabbfliken **Alternativ**, i fältet **Skapa inköpsorder**, väljer du alternativet **Skapa inköpsorder**.  
13. Välj knappen **OK** för att skapa inköpsorder för alla komponenterna på ordern.  

     Inköpsorder skapas och sparas som de sista orderna i listan över inköpsorder.  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a>Planera en överföringsorder för att uppfylla försäljningsbehov  
 I den här proceduren planerar du för behov från en försäljningsorder. Behovsraderna motsvarar försäljningsrader och inte komponentrader som vid efterfrågan från produktion.  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a>Så här planerar du en överföringsorder för att uppfylla försäljningsbehov  

1.  Flytta markören till planeringsraden för order **2008**.  
2.  Expandera raden och flytta markören till behovsraden.  

     Försäljningsorder **2008** avser tio högtalare, artikel **LS-120** som har beställts av John Haddock Insurance Co.  

     Artikelns definierade återanskaffningssystem och standardleverantör visas.  

    > [!NOTE]  
    >  Längst ned på sidan finns fyra informationsfält. I fältet **Tidigast disponibelt den** syns det att de tio delar som behövs kommer att vara disponibla, genom en ankommande leveransorder, nio dagar senare än det aktuella förfallodatumet. Om det är för sent för kunden innehåller fältet **Disponibelt för överföring** tretton enheter av samma artikel på ett annat lagerställe. Det betyder att du behöver planera för artikeltillgången.  

3.  Välj fältet **Disponibelt för överföring** för att öppna sidan **Hämta alternativ leverans**.  
4.  Välj knappen **OK** för att boka de tio artiklar som är tillgängliga.  

    > [!NOTE]  
    >  På behovsraden har det föreslagna inköpet bytts ut mot en överföring från lagerstället GRÖN. Med funktionen **Skapa order** skapas en överföringsorder från GRÖN till det lagerställe där behovet finns. Fältet **Ersättningar finns** fungerar på samma sätt.  

5.  Välj åtgärden **Skapa order**. Sidan **Skapa leveransorder** öppnas.  
6.  På snabbfliken **Orderplanering**, i fältet **Skapa order för** väljer du alternativet **Aktiv order**.  
7.  På snabbfliken **Alternativ**, i fältet **Skapa överföringsorder**, väljer du alternativet **Skapa överföringsorder**.  
8.  Välj knappen **OK** för att skapa överföringsordern som gör att försäljningsordern kan uppfyllas.  

     Överföringsordern skapas och sparas i listan som den sista ordern i listan över öppna överföringsorder.  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a>Planera en produktionsorder med flera nivåer för att uppfylla försäljningsbehov  
 I den här proceduren planerar du att uppfylla försäljningsbehovet av en tillverkad artikel med flera produktnivåer som var och en ger upphov till beroende produktionsbehov.  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a>Så här planerar du produktion i flera nivåer för att uppfylla försäljningsbehov  

1.  Markera planeringsraden med försäljningsbehov för order **1001** som skapades tidigare under förutsättningar.  

     Det här behovet är en försäljningsrad, men artikeln har ett definierat återanskaffningssystem, **Prod.order**. Fortsätt genom att lägga till en extra klocka i varje cykels komponentbehov.  

2.  På sidan **Komponenter** väljer du åtgärden **Planeringskomponenter**.  
3.  På raden för klockan (Bell) ändrar du fältet **Antal per** från **1** till **2**.  
4.  På sidan **Orderplanering** kan du överväga planeringsalternativen. I det här fallet har du inga alternativ, ingen överföring, ersättning eller sen leverans. Du måste skapa den föreslagna leveransordern, en produktionsorder.  
5.  Välj åtgärden **Skapa order** för att skapa produktionsordern.  

     På sidan **Orderplanering** kan du lägga märke till att planeringsraden för försäljningsordern **1001** inte längre finns och att det ursprungliga försäljningsbehovet är uppfyllt.  

6.  Stäng sidan **Orderplanering**.  

     Nu kan du välja att stanna kvar i den här vyn och slutföra alla planeringsaktiviteter. Istället ska du nu ikläda dig rollen som produktionsplanerare genom att gå till produktionsordern som du skapade, och öppna sidan **Orderplanering**.  

 Som produktionsplanerare måste du planera en särskild produktionsorder.  

### <a name="to-plan-a-specific-production-order"></a>Så här planerar du en särskild produktionsorder  

1.  Öppna produktionsordern **101001** på tio cyklar som du precis har skapat med funktionen **Skapa order**.  
2.  Öppna sidan **Prod.order - komponenter** för att kontrollera att den extra klockan återges i produktionsordern.  
3.  Välj åtgärden **Planerad**.  

     Sidan **Orderplanering** öppnas i en vy som är alltid filtrerad efter specifika produktionsbehov. Det går inte att göra ändringar i fönstret. Du måste beräkna en plan innan du kan se ytterligare behov.  

4.  Välj åtgärden **Skapa inköpsförslag**.  

     Lägg märke till att fyra nya produktionsorder visas som oplanerat produktionsbehov härlett från order **101001**. De nya raderna representerar nytt produktionsbehov från de delprodukter som måste skapas för att producera ordern.  

5.  Välj åtgärden **Expandera alla** för att visa en översikt över allt produktionsbehov för produktionsordrarna.  

     Om du vill ha mer information om behovsraderna kan du lägga till fälten **Efterfrågekvantitet** och **Disponibelt efterfrågat antal** i din vy.  

     Nu måste du leverera tio enheter av varje komponent.  

     Lägg märke till att fyra av behovsraderna har återanskaffningssystemet Prod.order. Dessa fyra delprodukter representerar cykelns andra produktnivå.  

     Standardinställningarna för återanskaffning är redan ifyllda och du kan fortsätta med att skapa order.  

6.  Välj åtgärden **Skapa order**.  

     Innan du klickar på **OK** bör du notera texten på snabbfliken **Orderplanering**. Den här texten är viktig eftersom du vet att cykeln har flera producerade komponenter, delmontage, i sin produktstruktur som kan behövas när du skapar produktionsordern.  

7.  På sidan **Skapa leveransorder**, i fältet **Skapa order för**, väljer du alternativet **Alla rader** och väljer sedan **OK** för att skapa produktionsorder för den andra produktnivån.  

     Lägg märke till att produktionsbehovet på högsta nivån för produktionsorder 101001 inte längre finns. Det innebär att det ursprungliga produktionsbehovet av delprodukterna har åtgärdats genom planeringen.  

     På sidan **Orderplanering** kan du beräkna en plan igen för att planera för cykelstrukturen.  

8.  Välj åtgärden **Skapa inköpsförslag** för att Skapa inköpsförslagen på nytt enligt instruktionerna i den inbäddade hjälptexten.  

     De två nya raderna representerar ytterligare produktionsbehov härlett från de delprodukter som planerades i föregående steg. Vi rekommenderar att du skapar två produktionsorder för att leverera hjulnaven, en för 10 framnav och en för 10 baknav.  

9. Välj åtgärden **Expandera alla** för att visa en översikt över allt produktionsbehov för de två produktionsordrarna.  

     Den föreslagna leveransplanen anger att totalt fyra inköpsorder kommer att skapas för komponenterna. Du bestämmer dig för att skapa de föreslagna orderna.  

10. Välj åtgärden **Skapa order**.  
11. I fältet **Skapa order för**, markera alternativet **Alla rader** och välj sedan **OK**. Kontrollera om det finns ytterligare behov för produktion av den överordnade artikeln, cykeln, som säljs på försäljningsorder 1001.  
12. Välj åtgärden **Skapa inköpsförslag**.  

     Meddelandet tyder på att alla artiklar som behövs nu är levererade. Kontrollera de fast planerade produktionsorder som skapas.  

13. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Fast planerad prod.order** och välj sedan relaterad länk.  

     Stäng sidan **Fasta planerade prod.order** för att se hur starttider och sluttider för enskilda order har planerats enligt produktstrukturen. Komponenterna på den lägsta nivån tillverkas först. Därför måste du planera order i flera nivåer, vilket framgår av den här planeringsprocessen.  

## <a name="see-also"></a>Se även  
 [Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)   
 [Genomgång: Planera leveranser automatiskt](walkthrough-planning-supplies-automatically.md)
