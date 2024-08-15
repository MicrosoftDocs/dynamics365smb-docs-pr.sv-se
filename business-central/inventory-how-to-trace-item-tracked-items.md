---
title: Spåra artikelspårade artiklar
description: 'Du kan se var en artikelspårad artikel har använts, inklusive hur och när den togs emot, tillverkades eller returnerades med funktionerna Artikelspårning och Sök transaktioner.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.forms: '6520,'
ms.date: 05/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="trace-item-tracked-items"></a>Spåra artikelspårade artiklar

Det går att se i vilket sammanhang den artikelspårade artikeln har använts, d.v.s. hur och när den togs emot eller tillverkades, överfördes, såldes, förbrukades eller returnerades. Du kan också söka efter alla aktuella instanser av ett visst serie- eller partinummer i databasen. Det gör du med funktionerna Artikelspårning och [Hitta transaktioner](ui-find-entries.md).  

Dessa funktioner kan vara användbara vid kvalitetskontroll när du behöver ta reda på vilka kunder som har tagit emot produkter med ett visst partinummer eller när du behöver ta reda på vilket parti en defekt komponent kommer från.  

 På sidan **Artikelspårning** kan du spåra framåt och bakåt i en serie bokförda lagertransaktioner efter serie- eller partinummer.  

  **På sidan Sök transaktioner** kan du inte se ordningsföljden för transaktioner, men du kan visa alla poster med serie- eller partinumret, både bokförda transaktioner och öppna poster.  

 De två funktionerna kan användas tillsammans genom att överföra ett spårat serie- eller partinummer till sidan **Hitta transaktioner** för att slutföra ett spårningsscenario. <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## <a name="to-trace-item-tracked-items"></a>Se spårade artiklar

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **artikelspårning** och väljer sedan relaterad länk.  
2.  I filterfälten längst upp på sidan ska de specifika artikelnumren anges eller ett filter för artikelnumren som ska spåras.  
3.  I fältet **Visa komponenter** väljer du om ursprunget för artiklarnas komponenter dessutom ska visas. Alternativen beskrivs i tabellen nedan.  

    |Fält|Description|  
    |----------------------------------|---------------------------------------|  
    |**Nej**|Visa inte komponenter.|  
    |**Endast artikelspårade**|Visa endast komponenter som har parti- eller serienummer.|  
    |**Alla**|Visa alla komponenter.|  

4.  I fältet **Spårningsmetod** väljer du den metod som ska användas för att spåra artikeln. Alternativen beskrivs i tabellen nedan.  

    |Fält|Beskrivning|  
    |----------------------------------|---------------------------------------|  
    |**Förbrukning-> Ursprung**|Spåra artikeln från platsen där artikeln användes till platsen som den kom ifrån. Till exempel om en tillverkad artikel har sålts till en kund, visar sidan **Artikelspårning** detta med utleveransraden först, som du kan därefter kan expandera för att visa från vilken produktionsorder artikeln har sitt ursprung.|  
    |**Förbrukning-> Ursprung**|Spåra artikeln från platsen där den kom in i lagret till platsen där den användes. Till exempel om en tillverkad artikel har sålts till en kund, visar sidan **Artikelspårning** detta med den färdiga produktionsordern först, som du kan därefter kan expandera för att visa på vilken utleveransrad artikeln användes.|  

5.  Välj åtgärden **Spåra** för att utföra spårningen.  

> [!NOTE]  
>  Endast kopplade transaktioner visas. Om du har tagit emot samma parti i flera transaktioner, kanske sidan **Artikelspårning** inte visar alla transaktioner.   

> [!NOTE]  
>  Om ytterligare transaktionshistorik under en artikelspåringsrad redan har spårats av en annan rad ovanför denna, är kryssrutan **Redan spårad** markerad. För att förenkla vyn och göra den tydligare visas inte sådana underliggande rader.  
>   
>  Välj **Gå till redan spårat** om du vill söka efter artikelspårningsrader där transaktionshistoriken redan har spårats. Den aktuella artikelspårnings raden är markerad, och alla underliggande rader expanderade.  

## <a name="to-find-item-tracked-items-with-find-entries"></a>Så här hittar du spårade artiklar med Hitta transaktioner

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **hitta transaktioner** och väljer sedan relaterad länk.  
2. Välj **Sök efter artikelreferenser**.
3. I fälten **Serienr** och **Partinr** anger du artikelspårningsnumren som du vill spåra.  
4. Välj åtgärden **Sök** för att hitta alla instanser av serie- eller partinumret i databasen.  

## <a name="see-also"></a>Se även

[Lager](inventory-manage-inventory.md)  
[Arbeta med serienummer, partinummer och paketnummer](inventory-how-work-item-tracking.md)  
[Designdetaljer: Artikelkoppling](design-details-item-tracking.md)  
[Designdetaljer: Artikelkoppling och reservationer](design-details-item-tracking-and-reservations.md)  
[Reservera artiklar](inventory-how-to-reserve-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[Hitta transaktioner](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
