---
title: Spåra artiklar med artikelspårning
description: Det går att se i vilket sammanhang den artikelspårade artikeln har använts, d.v.s. hur och när den togs emot eller tillverkades, överfördes, såldes, förbrukades eller returnerades. Du kan också söka efter alla aktuella instanser av ett visst serie- eller partinummer i databasen. Det gör du med funktionerna Artikelspårning och Hitta transaktioner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbfe0237beb58f22d3be7bc388d7b2726f05d4ba
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214759"
---
# <a name="trace-item-tracked-items"></a>Spåra artiklar med artikelspårning
Det går att se i vilket sammanhang den artikelspårade artikeln har använts, d.v.s. hur och när den togs emot eller tillverkades, överfördes, såldes, förbrukades eller returnerades. Du kan också söka efter alla aktuella instanser av ett visst serie- eller partinummer i databasen. Det gör du med funktionerna Artikelspårning och [Hitta transaktioner](ui-find-entries.md).  

Funktionerna kan vara särskilt användbara när det gäller kvalitetskontrollen i följande fall: när användaren vill få information om vilka kunder som tog emot produkter med ett visst partinummer eller när användaren vill få information om vilket parti en defekt komponent har sitt ursprung i.  

 På sidan **Artikelspårning** kan du spåra framåt och bakåt i en serie bokförda lagertransaktioner efter serie- eller partinummer.  

 På sidan **Hitta transaktioner** kan du inte se sekvensen av transaktioner, men du kan se alla transaktioner av serie- eller partinummer, både bokförda transaktioner och öppna transaktioner.  

 De två funktionerna kan användas tillsammans genom att överföra ett spårat serie- eller partinummer till sidan **Hitta transaktioner** för att slutföra ett spårningsscenario. <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## <a name="to-trace-item-tracked-items"></a>Se spårade artiklar  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Artikelspårning** och välj sedan relaterad länk.  
2.  I filterfälten längst upp på sidan ska de specifika artikelnumren anges eller ett filter för artikelnumren som ska spåras.  
3.  I fältet **Visa komponenter** väljer om ursprunget för artiklarnas komponenter dessutom ska visas. Dina alternativ i det här fältet är följande.  

    |Fält|Description|  
    |----------------------------------|---------------------------------------|  
    |**Nej**|Genom att välja detta alternativ visas inga komponenter.|  
    |**Endast artikelspårade**|Genom att välja detta alternativ visas endast komponenterna med parti- eller serienummer.|  
    |**Allt**|Genom att välja detta alternativ visas alla komponenter.|  

4.  I fältet **Spårningsmetod** väljer du den metod som ska användas för att spåra artikeln. Alternativen är följande  

    |Fält|Description|  
    |----------------------------------|---------------------------------------|  
    |**Förbrukning-> Ursprung**|Med den här metoden börjar artikelspårningen från platsen där artikeln användes till platsen som den kom ifrån. Till exempel om en tillverkad artikel har sålts till en kund, visar sidan **Artikelspårning** detta med utleveransraden först, som du kan därefter kan expandera för att visa från vilken produktionsorder artikeln har sitt ursprung.|  
    |**Förbrukning-> Ursprung**|Med den här metoden börjar artikelspårningen från platsen där artikeln lagerfördes till platsen där den användes. Till exempel om en tillverkad artikel har sålts till en kund, visar sidan **Artikelspårning** detta med den färdiga produktionsordern först, som du kan därefter kan expandera för att visa på vilken utleveransrad artikeln användes.|  

5.  Välj åtgärden **Spåra** för att utföra spårningen.  

> [!NOTE]  
>  Om du har tagit emot samma parti i flera transaktioner, kanske sidan **Artikelspårning** inte visar alla transaktioner. Endast kopplade transaktioner visas.  

> [!NOTE]  
>  Om ytterligare transaktionshistorik under en artikelspåringsrad redan har spårats av en annan rad ovanför denna, är kryssrutan **Redan spårad** markerad. För att förenkla vyn och göra den tydligare visas inte sådana underliggande rader.  
>   
>  Välj **Gå till redan spårat** om du vill söka efter artikelspårningsrader där transaktionshistoriken redan har spårats. Den aktuella artikelspårnings raden är markerad, och alla underliggande rader expanderade.  

## <a name="to-find-item-tracked-items-with-find-entries"></a>Så här hittar du spårade artiklar med Hitta transaktioner  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Hitta transaktioner** och välj sedan relaterad länk.  
2. Välj **Åtgärder** > **Sök efter** > **Sök efter artikelreferens**.
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