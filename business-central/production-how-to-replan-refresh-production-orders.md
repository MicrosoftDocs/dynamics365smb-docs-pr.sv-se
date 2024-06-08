---
title: Omplanera eller uppdatera produktionsorder direkt
description: I det här avsnittet beskrivs procedurerna för omplanering av produktionsorder och uppdatering av tillverkningsorder direkt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000842, 99000843, 99000861, 99000862, 99000863'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="replan-or-refresh-production-orders-directly"></a>Omplanera eller uppdatera produktionsorder direkt

Funktionen **Omplanera** på produktionsorder används vanligtvis när du har lagt till eller ändrat komponenter som utgör underliggande produktionsorder. Funktionen beräknar de ändringar som gjorts på komponent- och verksamhetsföljdsrader, och artiklar på lägre produktionsstrukturnivåer beaktas. Detta innebär att nya produktionsorder kan skapas för dessa artiklar.  

Funktionen Omplanera utgår ifrån de ändringar som du har gjort på komponent- och verksamhetsföljdsrader, och beräknar och planerar för eventuella nya behov för produktionsordern.  

Funktioen **uppdatera** för produktionsorder används vanligtvis när du har gjort något av följande:

- Skapat ett produktionsorderhuvud manuellt för att beräkna och skapa radinformation för första gången.
- Gjort ändringar i produktionsorderhuvudet för att beräkna om all radinformation.

Uppdateringsfunktionen beräknar de ändringar som gjorts i ett produktionsorderhuvud, och produktionsstrukturnivåer beaktas inte. Funktionen beräknar och initialiserar värdena på komponent- och verksamhetsföljdsrader utifrån de standarduppgifter som har angetts i den tilldelade produktionsstrukturen och verksamhetsföljden, och enligt den orderkvantitet och förfallodatum som har angetts i produktionsorderhuvudet.

Du kan antingen infoga produktionsorderraderna manuellt eller använda en funktion som beräknar produktionsorderraderna från huvudet.  

> [!NOTE]
> Om du använder funktionen Uppdatera för att omberäkna produktionsorderraderna kommer de gamla produktionsorderraderna tas bort och nya beräknas.  

## <a name="to-replan-a-production-order"></a>Så här planerar du om en produktionsorder

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Fast planerad prod.order** och väljer sedan relaterad länk.  
2. Öppna den produktionsorder som du vill omplanera.  
3. På snabbfliken **Rader** väljer du åtgärden **Rader** och väljer sedan åtgärden **Komponenter**.  
4. Lägg till en komponent som är en producerad artikel eller halvfabrikat.  
5. Från produktionsordern väljer du åtgärden **Omplanera**.  

    På sidan **Omplanera produktionsorder** anger du vad som ska omplaneras och hur:  
6. I fältet **Planeringsriktning**, välj ett av följande alternativ.  

    | Alternativ | Description |
    |--|--|
    | **Tillbaka** | Beräknar verksamhetssekvensen baklänges från det tidigaste möjliga slutdatumet, som definieras genom förfallodatumet och/eller andra planerade ordrar, till det senaste möjliga startdatumet. **Obs!**  Det här är standardalternativet, som fungerar i de flesta situationer. |
    | **Framåt** | Beräknar verksamhetssekvensen framåt från det senaste möjliga startdatumet, som definieras genom förfallodatumet och/eller andra planerade ordrar, till det tidigaste möjliga slutdatumet. **Obs!**  Detta alternativ fungerar endast för snabborder. |

7. I fältet **Planera** anger du om produktionsbehov för producerade artiklar i produktionsstrukturen ska beräknas:  

    |Alternativ|Description|  
    |----------------------------------|---------------------------------------|  
    |**Inga nivåer**|Produktion på lägre nivåer beaktas inte. Detta innebär att endast artikelns plan uppdateras (som vid en uppdatering).|  
    |**En nivå**|Planera för produktionsbehov på en nivå. Produktionsorder kan skapas på första nivån.|  
    |**Alla nivåer**|Planera för produktionsbehov på alla nivåer. Produktionsorder kan skapas på alla nivåer.|  

8. Välj **En nivå** och klicka på **OK** om du vill omplanera produktionsordern samt beräkna och skapa en ny underliggande produktionsorder för det nya halvfabrikatet, om det inte är helt tillgängligt.  

> [!NOTE]  
> De ändringar som genomförs via funktionen **Omplanering** ändrar förmodligen kapacitetsbehovet i produktionsordern, och du kan därför behöva planera om operationer när du har uppdaterat.  

## <a name="to-refresh-a-production-order"></a>Så här uppdaterar du en produktionsorder

Om du har ändrat produktionsorderrader, komponenter eller verksamhetsföljdrader måste du också uppdatera informationen i produktionsordern. I följande procedur beräknas komponenterna för en fast planerad produktionsorder. Momenten är liknande för verksamhetsföljdsrader.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 2.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Fast planerad prod.order** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. För mer information, se [Skapa produktionsorder](production-how-to-create-production-orders.md).  
3. Välj åtgärden **Uppdatera**.
4. Du kan välja en av följande alternativ på sidan **Uppdatera produktionsorder**:

    |Fält|Alternativ|Beskrivning|  
    |----------------------------------|---------------|---------------------------------------|  
    |**Planeringsriktning**|**Framåt**|Planeringen börjar vid startdatumet och fortsätter framåt till slutdatumet. Du måste fylla i startdatumet om du vill använda det här alternativet.|  
    ||**Bakåt**|Planeringen börjar vid slutdatumet och fortsätter bakåt till startdatumet.|  
    |**Beräkna**|**Rader**|Markera det här fältet om du vill beräkna produktionsorderrader.|  
    ||**Operationsföljder**|Det här fältet påverkar inte beräkningen av produktionsrader.|  
    ||**Komponentbehov**|Det här fältet påverkar inte beräkningen av produktionsrader.|  
    |**Dist.lager**|**Skapa ingående rekvisition**|Det här fältet påverkar inte beräkningen av produktionsrader.|  

5. Klicka på knappen **OK** för att bekräfta ditt val. Nu har produktionsorderraderna beräknats.

> [!NOTE]  
> När du beräknar produktionsorderkomponenter tas tidigare gjorda ändringar i komponenterna bort.

## <a name="see-also"></a>Se även

[Planerad](production-planning.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
