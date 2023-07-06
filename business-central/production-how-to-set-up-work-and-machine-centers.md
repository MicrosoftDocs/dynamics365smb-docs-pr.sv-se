---
title: Ställa in produktionsgrupper och maskingrupper
description: På ett produktionsgruppkort ordnar du fasta värden och behov för produktionsresursen. På så sätt kan du styra utdata från den produktion som utförs i produktionsgruppen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000754, 99000755, 99000756, 99000758, 99000760, 99000761, 99000762'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-work-centers-and-machine-centers"></a><a name="set-up-work-centers-and-machine-centers"></a><a name="set-up-work-centers-and-machine-centers"></a>Ställa in produktionsgrupper och maskingrupper

Programmet skiljer mellan tre typer av kapaciteter. Dessa är ordnade i hierarkisk ordning. Varje nivå innehåller underordnade nivåer.  

Den översta nivån är produktionsavdelningen. Till produktionsavdelningarna är produktionsgrupper kopplade. Varje produktionsgrupp kan endast tillhöra en produktionsavdelning.

Olika maskingrupper kan kopplas till varje produktionsgrupp. En maskingrupp kan endast tillhöra en produktionsgrupp.  

En produktionsgrupps planerade kapacitet består av motsvarande maskingrupps disposition och ytterligare planerad produktionsgruppsdisposition. Den planerade dispositionen i produktionsavdelningen är alltså summan av alla motsvarande maskin- och produktionsgruppsdispositioner.  

Dispositionen lagras i kalendertransaktioner.  

> [!IMPORTANT]
> Innan du ställer in produktions- eller maskingrupper, måste du lägga upp fabrikskalendrar. För mer information, se [Så här skapar du Fabrikskalendrar](production-how-to-create-work-center-calendars.md).

## <a name="to-set-up-a-work-center"></a><a name="to-set-up-a-work-center"></a><a name="to-set-up-a-work-center"></a>Så här skapar du produktionsgrupper:

Nedan beskrivs hur du ställer in produktionsgrupp Stegen för att ställa in maskingruppkalender är liknande förutom snabbfliken **verksamhetsföljdinställningar**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **produktionsgrupper** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I fältet **Produktionsavdelning** väljer du den resursgrupp på högre nivå som produktionsgruppen är underordnad. Välj åtgärden **Ny** i listrutan.  
5. I fältet **alternativ produktionsgrupp** väljer du den produktionsgrupp som ska användas om produktionsgruppen inte är tillgänglig eller om behovet överskrider sin kapacitet. Den alternativa produktionsgruppen är endast avsedd för information och ingår inte automatiskt i planeringsprocessen.
6. Välj fältet **Spärrad** om du vill förhindra att produktionsgruppen används i någon behandling. Detta innebär att produktionen inte kan bokföras för en artikel som produceras i produktionsgruppen. För mer information, se [Så här bokför du produktionsutflöde](production-how-to-post-output-quantity.md).
7. I fältet **Inköpspris** anger du kostnaden för att producera en enhet i denna produktionsgrupp, exklusive alla andra kostnadselement. Denna kostnad kallas ofta för *direkt arbetskostnad*.  
8. I fältet **Indirekt kostnad %** anger du de allmänna verksamhetskostnaderna för att använda produktionsgruppen som en procentandel av inköpspriset. Denna procentandel läggs till inköpspriset vid beräkningen av styckkostnaden.  
9. I fältet **Omkostnad** anger du icke-operationella kostnader för produktionsgruppen, till exempel underhållsutgifter, som ett absolut belopp.  

    I fältet **Styckkostnad** visas den beräknade styckkostnaden för att producera en enhet i denna produktionsgrupp, inklusive alla kostnadselement.  

    Styckkostnad = Inköpspris + (Inköpspris x Indirekt kostnad %) + Omkostnad.  

10. I fältet **Styckkost. beräkningstyp** anger du om beräkningen ovan ska bygga på mängden tid som använts: **Tid** eller antalet enheter som har producerats: **Enheter**.  
11. Markera fältet **Specifik styckkostnad** om du vill definiera styckkostnaden för produktionsgruppen på den operationsföljdrad där den används. Detta kan vara användbart för operationer där kapacitetskostnaden skiljer sig markant från vad som är normalt för produktionsgruppen.  
12. I fältet **Bokföringsmetod** anger du om bokföring av utflöde i produktionsgruppen ska beräknas och bokföras manuellt eller om det ska ske automatiskt med någon av följande metoder.

    |Alternativ|Beskrivning|
    |------|-----------|
    |**Manuell**| Använd tid, produktion och kassation bokförs manuellt i utflödesjournalen eller produktionsjournalen.|
    |**Framåt**|Utflöde bokförs automatiskt när produktionsordern släpps.|
    |**Bakåt**|Utflöde bokförs automatiskt när produktionsordern är slutförd.|

    > [!NOTE]
    > Om det behövs kan bokföringsmetoden som markeras här åsidosättas för enskilda operationer genom att inställningen för en operationsföljdrad ändras.

13. I fältet **Enhetskod** anger du den tidsenhet som ska användas för beräkning av kostnad och kapacitetsplanering för produktionsgruppen.
    För att kunna övervaka kapacitetsförbrukningen kontinuerligt måste du först ange en mätmetod. Enheterna som du anger är grundläggande enheter. Exempelvis mäts bearbetningstiden i timmar och minuter.

    > [!NOTE]  
    > Om du väljer att använda Dagar är det vktigt att komma ihåg att 1 dag = 24 timmar – inte 8 (arbetstimmar).

14. I fältet **Kapacitet** anger du om fler än en person eller maskin arbetar samtidigt i produktionsgruppen. (Om din [!INCLUDE[prod_short](includes/prod_short.md)]-installation inte innehåller modulen Maskingrupp måste värdet i det är fältet vara **1**.)  
15. I fältet **Effektivitet** anger du den procentandel av förväntade standardutdata som faktiskt uppnås av produktionsgruppen. Genom att ange **100** kan du ange att produktionsgruppens faktiska utdata är samma som standardutdata.  
16. Markera kryssrutan **Konsoliderad kalender** om du också använder maskingrupper. På så sätt uppsummeras kalendertransaktioner maskingruppkalender.  
17. I fältet **Fabrikskalenderkod** väljer du en fabrikskalender. För mer information, se [Så här skapar du Fabrikskalendrar](production-how-to-create-work-center-calendars.md).  
18. I fältet **Kötid** anger du ett tidsintervall som måste gå innan tilldelat arbete kan påbörjas i produktionsgruppen. 

> [!NOTE]
> Använd kötider för att tillhandahålla en buffert mellan den tidpunkt då en komponent anländer till en maskin eller en produktionsgrupp och när operationen verkligen startar. Exempelvis levereras en del till en maskingrupp kl. 10:00, men det tar en timme att montera den på maskinen, varför åtgärden inte påbörjas förrän kl. 11:00. För att redovisa för den timmen är kötiden en timme. Värdet i fältet **Kötid** på en maskin eller i en produktionsgrupp, plus summan av värdena i **Konfigurationstid**, **Bearbetningstid**, **Väntetid** och **Transporttid** på artikelns verksamhetsföljdrad kombineras i syfte att tillhandahålla artikelns produktionsledtid. På så sätt får du exakta totala produktionstider.  

## <a name="considerations-about-capacity"></a><a name="considerations-about-capacity"></a><a name="considerations-about-capacity"></a>Överväganden om kapacitet

Kapaciteten och effektiviteten som anges för en produktions- och maskingrupp påverkar inte bara den tillgängliga kapaciteten. De påverkar också den totala produktionstiden som består av installationstiden och körtiden som båda definieras på verksamhetsföljdsraden.  

När en specifik verksamhetsföljdsraden fördelas till en produktions- och maskingrupp, beräknar systemet hur mycket kapacitet som behövs och hur lång tid det tar att slutföra operationen.  

### <a name="run-time"></a><a name="run-time"></a><a name="run-time"></a>Bearbetningstid

Vid beräkning av bearbetnings tiden, tilldelar systemet den exakta tid som definieras i fältet **bearbetningstid** för verksamhetsföljdsraden. Varken effektivitet eller kapacitet påverkar den allokerade tiden. Om bearbetnings tiden exempelvis definieras som 2 timmar kommer den allokerade tiden att vara 2 timmar, oavsett värdena i fälten effektivitet och kapacitet i produktionsgruppen.  

> [!NOTE]
> Kapaciteten som används i beräkningarna definieras som det minsta värdet mellan den kapacitet som har definierats i produktions- eller maskingruppen och den samtidiga kapacitet som definierats för verksamhetsföljdsraden. Om en produktionsgrupp har kapacitet 100, men den samtidiga kapaciteten för verksamhetsföljdsraden är 2, kommer *2* att användas i beräkningarna.

*Varaktigheten* för en operation i motsatsen är både effektivitet och kapacitet. Varaktigheten beräknas som *körningstid/effektivitet/kapacitet*. I följande lista visas några exempel på beräkning av varaktigheten för samma bearbetningstid, som definieras som 2 timmar för verksamhetsföljdrad:

- Effektivitet 80 % innebär att du behöver 2,5 timmar i stället för två timmar  
- Effektivitet 200 % betyder att du kan slutföra arbetet på en timme – du kan göra hål två gånger snabbare om du har en grävmaskin som är dubbelt så stor som den mindre storleken  

    Du kan uppnå samma resultat om du använder två mindre grävmaskiner istället för en stor – använd *2* som kapacitet och *100 %* som effektivitet  

Det kan vara knepigt att diskutera delarnas kapacitet senare. 

### <a name="setup-time"></a><a name="setup-time"></a><a name="setup-time"></a>Omställningstid

Tidsallokeringen för omställningstiden beror på kapaciteten och beräknas som *omställningstid * kapacitet*. Om kapaciteten till exempel är *2* , så dubbleras den allokerade omställningstiden, eftersom du måste upprätta två maskiner för operationen.  

*Varaktighet* för omställningstiden beror på effektivitet och beräknas som *omställningstid/effektivitet*. 

- Effektivitet 80 % innebär att du behöver 2,5 timmar att konfigurera  
- Effektivitet 200 % betyder att du kan slutföra installationen i 1 timme i stället för två timmar definierade på operationsföljdraden  

Fraktalkapaciteten är inte lätt att ta till sig, och den används i mycket specifika fall.

### <a name="work-center-processing-multiple-orders-simultaneously"></a><a name="work-center-processing-multiple-orders-simultaneously"></a><a name="work-center-processing-multiple-orders-simultaneously"></a>Bearbeta flera order samtidigt i produktionsgruppen

Nu ska vi använda en sprutlackeringsbås som exempel. Den har samma inställnings- och körtid för varje bearbetat parti. Varje parti kan dock innehålla flera enskilda order som målas samtidigt.  

I det här fallet hanteras tid och kostnad som fördelas på order av omställningstiden och den samtidiga kapaciteten. Vi rekommenderar att du inte använder körtid i operationsföljdsraderna.  

Den allokerade omställningstiden för varje enskild order kommer i omvänd ordning efter det antal order (kvantiteter) som körs samtidigt. Här följer några exempel på hur du kan beräkna omställningstid när den definieras som två timmar för operationsföljdsraden:

- Om det finns två order ska den samtidiga kapaciteten på operationsföljdsraden ha värdet 0,5.

    Resultatet blir att den allokerade kapaciteten för var och en timme, men varaktigheten för varje order kommer att bli två timmar.
- Om det finns två order med kvantiteten en och fyra, är den samtidiga kapaciteten för operationsföljdsraden för den första ordern 0,2 och 0,8 för den andra.  

    Det innebär att den allokerade kapaciteten för den första ordern blir 24 min och för den andra 96. Varaktigheten för båda orderna blir då två timmar.  

I båda fallen är den totala fördelade tiden för alla order två timmar.


### <a name="efficient-resource-can-dedicate-only-part-of-their-work-date-to-productive-work"></a><a name="efficient-resource-can-dedicate-only-part-of-their-work-date-to-productive-work"></a><a name="efficient-resource-can-dedicate-only-part-of-their-work-date-to-productive-work"></a>Effektiv resurs kan endast avsätta en del av sitt arbetsdatum för att producera arbete

> [!NOTE]
> Detta scenario rekommenderas inte. Vi rekommenderar att du använder effektivitet i stället. 

En av dina produktionsgrupper representerar en erfaren arbetare som arbetar med 100 % effektivitet på aktiviteter. Men de kan bara spendera 50 % av sin arbetstid på aktiviteterna eftersom resten av tiden löser de administrativa uppgifter. När den här arbetaren kan slutföra en två timmars uppgifter på exakt två timmar måste du i genomsnitt vänta ytterligare två timmar medan personen arbetar med andra uppgifter.  

Den allokerade körtiden är två timmar och varaktigheten är fyra timmar.  

Använd inte omställningstid för sådana scenarier, eftersom systemet endast tilldelar 50 % av tiden. Om omställningstiden är *2*, är den allokerade omställningstiden en timme och varaktigheten två timmar.

### <a name="consolidated-calendar"></a><a name="consolidated-calendar"></a><a name="consolidated-calendar"></a>Konsoliderad kalender

När fältet **konsoliderad kalender** är markerat har produktionsgruppen inte en egen kapacitet. I stället är dess kapacitet lika med summan av kapaciteten hos alla maskingrupper som är kopplade till produktionsgruppen.  

> [!NOTE]
>  Maskingruppens effektivitet omvandlas till produktionsgruppens kapacitet.

Om du till exempel har två maskingrupper med en effektivitet på 80 och 70, kommer den konsoliderade kalendertransaktionen att ha en effektivitet på 100, kapacitet 1,5 och en total kapacitet som 12 timmar (åtta timmars skift * 1,5 kapacitet). 

> [!NOTE]
>  Använd fältet **konsoliderad kalender** när du strukturerar operationsföljder för att tidsplanera produktions operationer på maskingruppsnivå, inte på produktionsgruppsnivån. När du konsoliderar kalendern blir sidan med **Produktionsgruppbeläggning** en översikt över den samlade beläggningen i alla maskingrupper som har kopplats till produktionsgruppen.

### <a name="example---different-machine-centers-assigned-to-a-work-center"></a><a name="example---different-machine-centers-assigned-to-a-work-center"></a><a name="example---different-machine-centers-assigned-to-a-work-center"></a>Exempel – Olika maskingrupper kan kopplas till en produktionsgrupp

Det är viktigt att planera vad som ska utgöra den totala kapaciteten när maskin- och produktionsgrupper skapas.

Om olika maskingrupper (till exempel 210 Packbord, 310 Målningshytt...) kopplats till en produktionsgrupp är det viktigt att beakta varje maskingrupps kapacitet eftersom ett fel i en enda maskingrupp kan avbryta hela processen. Maskingrupperna kan anges enligt kapacitet men kan inte inkluderas i planeringen. Om fältet **Konsoliderad kalender** inaktiveras kopplas endast produktionsgruppens men inte maskingruppens kapacitet till planeringen.

Om däremot identiska maskingrupper (till exempel 210 Packbord 1 och 220 Packbord 2) kombineras i en produktionsgrupp, beaktas produktionsgruppen som summan av de kopplade maskingrupperna. Därför visas produktionsgruppen i detta fall med nollkapacitet. Om fältet **Konsoliderad kalender** aktiveras så kopplas den gemensamma kapaciteten till produktionsgruppen.

Om produktionsgruppernas kapacitet inte ska läggas till i den totala kapaciteten anger du effektivitet = 0.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a><a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a><a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Om du vill ställa in en kapacitetsbegränsad maskin- eller produktionsgrupp

Du måste skapa produktionsresurser som du anser är kritiska och markera dem för att acceptera en bestämd beläggning i stället för den obestämda beläggning som är standard och som andra produktionsresurser accepterar. Ett kapacitetsbegränsad resurs kan vara en produktions- eller maskingrupp som du har identifierat som en flaskhals och för vilken du vill skapa en begränsad (bestämd) beläggning.

[!INCLUDE[prod_short](includes/prod_short.md)] har inte stöd för detaljerad fabrikskontroll. Den planerar för ett möjligt utnyttjande av resurser genom att ange grovt schema, men det skapar och underhåller inte automatiskt detaljerade scheman som baseras på prioriteter eller optimeringsregler.

På sidan **kapacitetsbegränsade resurser** kan du göra inställningar som undviker överbelastning av specifika resurser och säkerställa att ingen kapacitet blir ej fördelad om den kan öka produktionstiden för en produktionsorder. I fältet **Dämpare (% totalkapacitet)** kan du lägga till dämpartiden för resurser för att minimera åtgärdsdelning. Det gör att systemet kan schemalägga laddning till den sista möjliga dagen genom att överskrida den kritiska beläggningsprocenten något om det kan minska antalet operationer som delas.

När du ska planera med kapacitetsbegränsade resurser ser systemet till att ingen resurs beläggs över sin definierade kapacitet (kritisk beläggning). Det ske genom att tilldela varje operation till den närmaste tillgängliga tidsluckan. Om tidsluckan inte är tillräckligt stor för att slutföra hela åtgärden kommer åtgärden att uppdelas i två eller flera delar som placeras i de närmaste tidsluckorna.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kap.begränsning för resurs** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs.

> [!NOTE]
> Operationer på produktions- eller maskingrupper, som definierar begränsade resurser ska alltid planeras i nummerserie. Det innebär att även om en begränsad resurs har flera kapaciteter, ska operationer som utförts av de kapaciteterna bara planeras i sekvens inte i parallell, vilket är fallet om maskingruppen inte har lagts upp som en begränsad resurs. I en begränsad resurs är fältet Kapacitet för produktionsgruppen eller maskingruppen större än 1.

> I händelse av åtgärdsdelning tilldelas inställningstiden bara en gång, eftersom det antas att vissa manuella justeringen sker för att optimera schemat.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Skapa fabrikskalendrar](production-how-to-create-work-center-calendars.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Planerad](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
