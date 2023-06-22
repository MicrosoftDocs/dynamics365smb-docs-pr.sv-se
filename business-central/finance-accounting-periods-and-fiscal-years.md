---
title: Arbeta med bokföringsperioder och räkenskapsår
description: Lär dig hur du arbetar med bokföringsperioder för att definiera när företaget rapporterar resultat.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 100
ms.date: 08/25/2022
ms.author: bholtorf
---
# <a name="work-with-accounting-periods-and-fiscal-years" />Arbeta med bokföringsperioder och räkenskapsår

Bokföringsperioder, även kallade rapporteringsperioder, är perioder som ett företag eller en organisation rapporterar resultat, exempelvis genom att generera deras resultat- eller balansräkning. Bokföringsperioder avser vanligtvis företagets räkenskapsår, som kan innehålla flera bokföringsperioder, till exempel månader eller kvartal.

För många företag bokförs räkenskapsåret inte med kalender året, t.ex. när räkenskapsåret slutar den 30 juni i stället för 31 december. För nyskapade företag kan räkenskapsåret vara längre än tolv månader.  

[!INCLUDE[prod_short](includes/prod_short.md)] kräver endast bokföringsperioder om du vill avsluta en resultaträkning eller köra aktiviteter för datakomprimering.

Du kan använda bokföringsperioder i rapportering, till exempel när du granskar bokförda transaktioner på sidan **Saldo/budget** där rapporteringsintervallet kan anges. Ett av alternativen du kan ange är att rapportera efter bokföringsperiod. Du kan också skapa en ekonomisk rapport som jämför resultaten för olika bokföringsperioder.

## <a name="creating-a-new-fiscal-year" />Skapa ett nytt räkenskapsår

Du kan skapa bokföringsperioder i bulk genom att använda batchjobbet **Skapa räkenskapsår**, eller genom att skapa dem manuellt.

### <a name="how-to-create-accounting-periods-in-bulk" />Så här skapar du flera bokföringsperioder samtidigt

Använd batch-jobbet **skapa räkenskapsår** om du vill dela upp ett räkenskapsår i lika långa perioder.  

1. Välj ![Sök efter sida eller rapport.](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport") anger du **Bokföringsperioder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Skapa år**.
3. I fältet **Startdatum** anger du det datum när räkenskapsåret börjar.  
4. I fältet **Antal perioder** ange antalet bokföringsperioder som räkenskapsåret ska innehålla. Det kan finnas upp till 365 perioder per år.  
5. I fältet **periodlängd** anger du en varaktighet för varje period. Varaktighetsidentifierare inbegriper 1M för en månad, 1Q för ett kvartal och 1Y för ett år.  
6. Välj **OK**.  

### <a name="how-to-create-accounting-periods-manually" />Så här skapar du flera redovisningsperioder manuellt

Om bokföringsperioder för räkenskapsåret har olika varaktighet, såsom 4-4-5-kalendern som används i detaljhandeln, kan du manuellt ställa in den.  
  
1. Välj ![Sök efter sida eller rapport.](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport") anger du **Bokföringsperioder** och väljer sedan relaterad länk.  
2. I fältet **Startdatum** anger du det datum när räkenskapsåret börjar. Fältet **Namn** visar namnet på månaden.  
3. Markera kryssrutan **Nytt räkenskapsår** för att indikera att detta är den första perioden under året. [!INCLUDE[prod_short](includes/prod_short.md)] kommer att använda denna period för att bestämma vilka perioder som avslutas vid årets slut.
4. Upprepa steg 2 och 3 för varje återstående period.  

## <a name="closing-a-fiscal-year" />Avsluta ett räkenskapsår

Avsluta räkenskapsåret är en av åtgärderna för att avsluta böckerna. Efter att du avslutar ett räkenskapsår markeras kryssrutorna **Avslutat** och **Låst datum** för samtliga perioder i året. Du kan inte öppna ett år igen eller avmarkera kryssrutorna.

> [!NOTE]  
> Du måste alltid ha minst ett oavslutat räkenskapsår. När du avslutar ett år, försäkra dig om att ett nytt år har skapats. Notera även att efter att du avslutat ett år kan du inte ändra startdatumet för det följande året.

1. Välj ![Sök efter sida eller rapport.](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport") anger du **Bokföringsperioder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Avsluta år**.  

## <a name="posting-entries-to-a-closed-fiscal-year" />Bokföra transaktioner till ett avslutat räkenskapsår

Även om ett räkenskapsår har avslutats kan du fortfarande bokföra redovisningstransaktioner på året. När du gör det markeras transaktionerna som bokförda på ett avslutat räkenskapsår och kryssrutan **Föregående års transaktion** markeras. Som standard visas inte kryssrutan på sidan, men du kan lägga till den. Nästa steg är att avsluta resultaträkningskontona och överföra årets resultat till ett konto i balansräkningen. Upprepa dessa steg varje gång du bokför transaktioner i ett avslutat räkenskapsår.

## <a name="see-also" />Se även

[Avsluta böckerna](year-close-books.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med ekonomiska rapporter](bi-how-work-account-schedule.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
