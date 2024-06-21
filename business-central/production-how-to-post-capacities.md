---
title: Bokför kapaciteter
description: Bokföra förbrukade kapaciteter som inte har tilldelats produktions ordern i kapacitetsjournalen och visa bokförda kapaciteter på sidan kapacitetstransaktioner.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '5832, 99000802, 99000820'
ms.date: 03/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Bokför kapaciteter

I kapacitetsjournalen bokför du förbrukade kapaciteter som inte kopplats till produktionsordern. Underhållsarbete måste till exempel kopplas till kapacitet, men inte till en produktionsorder.  

## Så här bokför du kapaciteter  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **kapacitetsjournal** och väljer sedan relaterad länk.  
2. Fyll i fälten **Bokföringsdatum** och **Verifikationsnummer** .  
3. I fältet **Typ** anger du kapacitetstypen, endera **Maskingrupp** eller **Produktionsgrupp**, som du bokför.  
4. I fältet **Nr.** skriv numret på den artikel som har beställts.  
5. Ange relevanta uppgifter i övriga fält, t. ex. **Starttid**, **Sluttid**, **Antal** och **Kassation**.  
6. Välj åtgärden **Bokför** om du vill bokföra fakturan.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Så här visar du produktionsgruppstransaktioner  

På sidan **produktionsgruppkort** och **maskingruppkort** kan du se bokförd kapacitet till följd av avslutade produktionsorder.    
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **produktionsgrupper** och väljer sedan relaterad länk.  
2. Öppna relevant **produktionsgrupp**kort i listan och klicka på åtgärden **Kapacitetstransaktioner**.  

    På sidan **Kapacitetstransaktioner** visas de transaktioner som bokförts från produktionsgruppen i den ordning de bokförts i.   

## Se även  

[Produktion](production-manage-manufacturing.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]