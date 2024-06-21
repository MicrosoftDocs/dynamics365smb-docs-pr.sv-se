---
title: Uppdatera standardkostnader
description: Du måste regelbundet uppdatera standardkostnader för komponenter och överföra de nya kostnaderna till den överordnade artikeln.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5841
ms.date: 10/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="update-standard-costs"></a>Uppdatera standardkostnader
Du måste regelbundet uppdatera standardkostnader för komponenter och överföra de nya kostnaderna till den överordnade artikeln. Processen består typiskt av följande fyra steg:  

1.  Uppdatera kostnader på komponent- och kapacitetsnivå. Mer information finns i batch-jobbet **Föreslå artikelstandardkostnad**.  
2.  Konsolidera och summera komponent- och kapacitetskostnader för att beräkna den totala produktions- eller monteringskostnaden för artiklarna.  
3.  Använd standardkostnaderna som angavs när du körde de föregående batch-jobben. Standardkostnaderna börjar inte gälla förrän de implementeras. Använd batch-jobbet **Implementera ändringar av standardkostnad**, som uppdaterar ändringarna av standardkostnaden för artiklar med de i tabellen Standardkostnadsformulär.  
4.  Inför ändringarna för att uppdatera fältet **Styckkostnad** för artikelkortet och utföra lageromvärderingen. Mer information finns i [Omvärdera lager](inventory-how-revalue-inventory.md).  

Mer information finns i [Om att beräkna standardkostnad](finance-about-calculating-standard-cost.md).
  
## <a name="to-update-standard-costs"></a>Uppdatera standardkostnader

1.  Kör batch-jobbet **Justera kost. – artikeltrans.** För att starta batch-jobbet, välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Justera kostn. – artikeltrans.** och välj sedan relaterad länk. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Granska resultaten och gör nödvändiga ändringar.  
2.  Kör batch-jobbet **Bokför lagerkostnad i redov.** För att starta batch-jobbet, välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokför lagerkostnad i redov.** och väljer sedan relaterad länk. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Granska resultaten och gör nödvändiga ändringar.  
3.  Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") öppna **Standardkostnadsformulär** och använd en eller flera av följande åtgärder:

    1.  Kör batch-jobbet **Föreslå artikelstandardkostnad**.  
    2.  Granska resultaten och gör nödvändiga ändringar.  
    3.  Kör batch-jobbet **Föreslå standardkostnad för kapacitet**.  
    4.  Granska resultaten och gör nödvändiga ändringar.
    5. Kör batch-jobbet **Uppsummerad standardkostnad**.
    6.  Granska resultaten och gör nödvändiga ändringar.
    7.  Kör batch-jobbet **Implementera standardkostnadsändringar**.  
4.  Granska och bokför sidan **Omvärderingsjournal** , vilken har fyllts på med transaktioner från föregående steg i den här processen.  

## <a name="see-also"></a>Se även

 [Om beräkning av standardkostnad](finance-about-calculating-standard-cost.md)   
 [Hantera lagerkostnader](finance-manage-inventory-costs.md)   
 [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)   
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
