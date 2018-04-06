---
title: "Så här ställer du in produktions- och maskingrupper | Microsoft Docs"
description: "På ett **Produktionsgruppkort** ordnar du fasta värden och behov för produktionsresursen. På så sätt kan du styra utdata från den produktion som utförs i produktionsgruppen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 545ad2e348ba4acc3a1c4cde741acaa2a9b824ed
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-work-centers-and-machine-centers"></a>Ställa in produktionsgrupper och maskingrupper
Programmet skiljer mellan tre typer av kapaciteter. Dessa är ordnade i hierarkisk ordning. Varje nivå innehåller underordnade nivåer.  

Den översta nivån är produktionsavdelningen. Till produktionsavdelningarna är produktionsgrupper kopplade. Varje produktionsgrupp kan endast tillhöra en produktionsavdelning.

Olika maskingrupper kan kopplas till varje produktionsgrupp. En maskingrupp kan endast tillhöra en produktionsgrupp.  

En produktionsgrupps planerade kapacitet består av motsvarande maskingrupps disposition och ytterligare planerad produktionsgruppsdisposition. Den planerade dispositionen i produktionsavdelningen är alltså summan av alla motsvarande maskin- och produktionsgruppsdispositioner.  

Dispositionen lagras i kalendertransaktioner. Innan du ställer in produktions- eller maskingrupper, måste du lägga upp fabrikskalendrar. För mer information, se [Så här skapar du Fabrikskalendrar](production-how-to-create-work-center-calendars.md).  

## <a name="to-set-up-a-work-center"></a>Så här skapar du produktionsgrupper:
Nedan beskrivs hur du ställer in produktionsgrupp Stegen för att ställa in maskingruppkalender är liknande förutom snabbfliken **verksamhetsföljdinställningar**.  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Arbetsskift** och välj sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  I fältet **Produktionsavdelning** väljer du den resursgrupp på högre nivå som produktionsgruppen är underordnad. Välj åtgärden **Ny** i listrutan.  
5.  Välj fältet **Spärrad** om du vill förhindra att produktionsgruppen används i någon behandling. Detta innebär att produktionen inte kan bokföras för en artikel som produceras i produktionsgruppen. För mer information, se [Så här bokför du produktionsutflöde](production-how-to-post-output-quantity.md).
6.  I fältet **Inköpspris** anger du kostnaden för att producera en enhet i denna produktionsgrupp, exklusive alla andra kostnadselement. Denna kostnad kallas ofta för *direkt arbetskostnad*.  
7.  I fältet **Indirekt kostnad %** anger du de allmänna verksamhetskostnaderna för att använda produktionsgruppen som en procentandel av inköpspriset. Denna procentandel läggs till inköpspriset vid beräkningen av styckkostnaden.  
8.  I fältet **Omkostnad** anger du icke-operationella kostnader för produktionsgruppen, till exempel underhållsutgifter, som ett absolut belopp.  

    I fältet **Styckkostnad** visas den beräknade styckkostnaden för att producera en enhet i denna produktionsgrupp, inklusive alla kostnadselement.  

    Styckkostnad = Inköpspris + (Inköpspris x Indirekt kostnad %) + Omkostnad.  

9.  I fältet **Styckkost. beräkningstyp** anger du om beräkningen ovan ska bygga på mängden tid som använts: **Tid** eller antalet enheter som har producerats: **Enheter**.  
10.  Markera fältet **Specifik styckkostnad** om du vill definiera styckkostnaden för produktionsgruppen på den verksamhetsföljdrad där den används. Detta kan vara användbart för operationer där kapacitetskostnaden skiljer sig markant från vad som är normalt för produktionsgruppen.  
11.  I fältet **Bokföringsmetod** anger du om bokföring av utflöde i produktionsgruppen ska beräknas och bokföras manuellt eller om det ska ske automatiskt med någon av följande metoder.  

    |Alternativ|Beskrivning|  
    |----------------------------------|---------------------------------------|  
    |**Manuell**|Förbrukning bokförs manuellt i utflödesjournalen eller produktionsjournal.|
    |**Framåt**|Förbrukning beräkna och bokförs automatiskt när produktionsordern släpps.|  
    |**Bakåt**|Förbrukning beräkna och bokförs automatiskt när produktionsordern är färdig.|  

    > [!NOTE]  
    >  Om det behövs kan bokföringsmetoden som markeras här och på **artikelkortet** åsidosättas för enskilda operationer genom att inställningen för en verksamhetsföljdrad ändras.

12.  I fältet **Enhetskod** anger du den tidsenhet som ska användas för beräkning av kostnad och kapacitetsplanering för produktionsgruppen.
    För att kunna övervaka kapacitetsförbrukningen kontinuerligt måste du först ange en mätmetod. Enheterna som du anger är grundläggande enheter. Exempelvis mäts bearbetningstiden i timmar och minuter.

    > [!NOTE]  
    > Om du väljer att använda Dagar är det vktigt att komma ihåg att 1 dag = 24 timmar - inte 8 (arbetstimmar).

13.  I fältet **Kapacitet** anger du om fler än en person eller maskin arbetar samtidigt i produktionsgruppen. (Om din [!INCLUDE[d365fin](includes/d365fin_md.md)]-installation inte innehåller modulen Maskingrupp måste värdet i det är fältet vara **1**.)  
14.  I fältet **Effektivitet** anger du den procentandel av förväntade standardutdata som faktiskt uppnås av produktionsgruppen. Genom att ange **100** kan du ange att produktionsgruppens faktiska utdata är samma som standardutdata.  
15. Markera kryssrutan **Konsoliderad kalender** om du också använder maskingrupper. På så sätt uppsummeras kalendertransaktioner maskingruppkalender.  
16.  I fältet **Fabrikskalenderkod** väljer du en fabrikskalender. För mer information, se [Så här skapar du Fabrikskalendrar](production-how-to-create-work-center-calendars.md).  
17.  I fältet **Kötid** anger du ett tidsintervall som måste gå innan tilldelat arbete kan påbörjas i produktionsgruppen. Observera att värdet för Kötid läggs till utöver andra icke-produktiva tidselement som till exempel Väntetid och Transporttid, som du kan ange på verksamhetsföljdrader som använder produktionsgruppen.  

## <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Exempel – Olika maskingrupper kan kopplas till en produktionsgrupp
Det är viktigt att planera vad som ska utgöra den totala kapaciteten när maskin- och produktionsgrupper skapas.

Om olika maskingrupper (till exempel 210 Packbord, 310 Målningshytt...) kopplats till en produktionsgrupp är det viktigt att beakta varje maskingrupps kapacitet eftersom ett fel i en enda maskingrupp kan avbryta hela processen. Maskingrupperna kan anges enligt kapacitet men kan inte inkluderas i planeringen. Om fältet **Konsoliderad kalender** inaktiveras kopplas endast produktionsgruppens men inte maskingruppens kapacitet till planeringen.

Om däremot identiska maskingrupper (till exempel 210 Packbord 1 och 220 Packbord 2) kombineras i en produktionsgrupp, beaktas produktionsgruppen som summan av de kopplade maskingrupperna. Därför visas produktionsgruppen i detta fall med nollkapacitet. Om fältet **Konsoliderad kalender** aktiveras så kopplas den gemensamma kapaciteten till produktionsgruppen.

Om produktionsgruppernas kapacitet inte ska läggas till i den totala kapaciteten anger du effektivitet = 0.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Om du vill ställa in en kapacitetsbegränsad maskin- eller produktionsgrupp
Du måste skapa produktionsresurser som du anser är kritiska och markera dem för att acceptera en bestämd beläggning i stället för den obestämda beläggning som är standard och som andra produktionsresurser accepterar. Ett kapacitetsbegränsad resurs kan vara en produktions- eller maskingrupp som du har identifierat som en flaskhals och för vilken du vill skapa en begränsad (bestämd) beläggning.

[!INCLUDE[d365fin](includes/d365fin_md.md)] har inte stöd för detaljerad fabrikskontroll. Den planerar för ett möjligt utnyttjande av resurser genom att ange grovt schema, men det skapar och underhåller inte automatiskt detaljerade scheman som baseras på prioriteter eller optimeringsregler.

I fönstret **kapacitetsbegränsade resurser** kan du göra inställningar som undviker överbelastning av specifika resurser och säkerställa att ingen kapacitet blir ej fördelad om den kan öka produktionstiden för en produktionsorder. I fältet **Dämpare (% totalkapacitet)** kan du lägga till dämpartiden för resurser för att minimera åtgärdsdelning. Det gör att systemet kan schemalägga laddning till den sista möjliga dagen genom att överskrida den kritiska beläggningsprocenten något om det kan minska antalet operationer som delas.

När du ska planera med kapacitetsbegränsade resurser ser systemet till att ingen resurs beläggs över sin definierade kapacitet (kritisk beläggning). Det ske genom att tilldela varje operation till den närmaste tillgängliga tidsluckan. Om tidsluckan inte är tillräckligt stor för att slutföra hela åtgärden kommer åtgärden att uppdelas i två eller flera delar som placeras i de närmaste tidsluckorna.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kap.begränsning för resurs** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs.

> [!NOTE]
> Operationer på produktions- eller maskingrupper, som definierar begränsade resurser ska alltid planeras i nummerserie. Det innebär att även om en begränsad resurs har flera kapaciteter, ska operationer som utförts av de kapaciteterna bara planeras i sekvens inte i parallell, vilket är fallet om maskingruppen inte har lagts upp som en begränsad resurs. I en begränsad resurs är fältet Kapacitet för produktionsgruppen eller maskingruppen större än 1.

> I händelse av åtgärdsdelning tilldelas inställningstiden bara en gång, eftersom det antas att vissa manuella justeringen sker för att optimera schemat.

## <a name="see-also"></a>Se även  
[Skapa fabrikskalendrar](production-how-to-create-work-center-calendars.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planerad](production-planning.md)   
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

