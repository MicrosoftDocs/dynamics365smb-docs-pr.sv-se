---
title: Så här skapar du serviceartiklar
description: 'Läsa om olika sätt att skapa serviceartiklar i Business Central, t.ex. i en serviceorder eller vid leverans av artiklar.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# Skapa tjänsteartiklar

I [!INCLUDE[prod_short](includes/prod_short.md)] avser termen ”serviceartikel” den utrustning eller de artiklar som kräver service. När du skapar en serviceorder kan du ange de artiklar som behöver service. I ordern kan du länka en serviceartikel till en artikel i lagret eller en serviceartikelgrupp.    

När du tar emot en artikel för service kan du registrera den som serviceartikel. Detta kan göras på olika sätt. Du kan till exempel skapa en serviceartikel på sidan **serviceartiklar** eller som en del av en annan process, som t. ex. när du arbetar med en serviceorder.   

## Så här skapar du en serviceartikel

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **serviceartiklar** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Så här skapar du serviceartiklar inom serviceorder

När du tar emot artiklar som du vill registrera som serviceartiklar kan du skapa dem som serviceartiklar på sidan **Serviceorder** eller **Serviceoffert**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Välj åtgärden **Skapa serviceartikel**.  

    Ett nummer tilldelas serviceartikeln, och ett serviceartikelkort skapas. I fältet **Serviceartikelnr** fylls numret på den nya serviceartikeln i.

## Så här skapar du en serviceartikel vid artikelutleverans

När du levererar artiklar genom att bokföra antingen försäljningsorder eller försäljningsfakturor registreras de levererade artiklarna automatiskt som serviceartiklar om följande villkor uppfylls. Artiklarna måste höra till en serviceartikelgrupp och ha kryssrutan **Skapa serviceartikel** markerad. Om artiklarnas serienummer har registrerats på sidan Artikelspårningsrader kopieras informationen automatiskt till fältet **Serienr** på serviceartikelkortet när serviceartiklar skapas.  

Nedan förklaras hur du skapar serviceartiklar när du levererar artiklar på försäljningsorder.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Öppna den aktuella försäljningsordern.  
3. Välj åtgärden **Bokför** eller **Bokför och skriv ut**.  
4. Välj åtgärden **leverera** eller **leverera och fakturera**.  
5. Serviceartiklarna skapas automatiskt för artiklarna på ordern, förutsatt att de tillhör en serviceartikelgrupp som har definierats för att skapa serviceartiklar. Om du har registrerat serienummer på sidan **Artikelspårningsrader** kommer de att tilldelas till motsvarande serviceartiklar.  

> [!NOTE]  
>  Om en artikel är en struktur och du har expanderat strukturen behandlas de expanderade strukturartiklarna på samma sätt som vanliga artiklar. Serviceartiklar skapas utifrån serviceartikelgruppens villkor, och om du vill, serienumrens villkor. Dessutom är det så att om en serviceartikel skapas för en expanderad struktur som består av andra strukturkomponenter, skapas de här artiklarna som serviceartikelkomponenter för den expanderade strukturserviceartikeln.  
>   
>  Om en artikel är en struktur och du inte har expanderat strukturen skapas en serviceartikel för den utifrån serviceartikelgruppens villkor, och om du så vill, serienumrens villkor.  

## Så här infogar du uppstartskostnader för en serviceartikel

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceuppgifter** och väljer sedan relaterad länk.
2. Välj åtgärden **Artikelkalkylark**.
3. Välj serviceraden och välj sedan **Åtgärder**, **Funktioner** och sedan åtgärden **Infoga uppstartskostnad**.  

    En servicerad av typen **Kostnad** infogas automatiskt med uppstartskostnaden. Uppstartskostnaden gäller vald serviceartikel.

## Se relaterad [Microsoft utbildning](/training/modules/create-items/)

## Se även

[Ställa in tjänsteartiklar och tjänsteartikelkomponenter](service-how-setup-service-items.md)  
[Ställa in tjänstehantering](service-setup-service.md)  
[Servicehantering](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
