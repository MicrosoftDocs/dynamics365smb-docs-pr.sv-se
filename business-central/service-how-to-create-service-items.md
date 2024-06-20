---
title: Så här skapar du serviceartiklar
description: 'Läsa om olika sätt att skapa serviceartiklar i Business Central, t.ex. i en serviceorder eller vid leverans av artiklar.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Skapa serviceartiklar

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
> Om en artikel är en struktur och du har expanderat strukturen behandlas de expanderade strukturartiklarna på samma sätt som vanliga artiklar. Serviceartiklar skapas utifrån serviceartikelgruppens villkor, och om du vill, serienumrens villkor. Dessutom är det så att om en serviceartikel skapas för en expanderad struktur som består av andra strukturkomponenter, skapas de här artiklarna som serviceartikelkomponenter för den expanderade strukturserviceartikeln.  
>
> Om en artikel är en struktur och du inte har expanderat strukturen skapas en serviceartikel för den utifrån serviceartikelgruppens villkor, och om du så vill, serienumrens villkor.  

## Så här infogar du uppstartskostnader för en serviceartikel

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceuppgifter** och väljer sedan relaterad länk.
2. Välj åtgärden **Artikelkalkylark**.
3. Välj serviceraden och välj sedan **Åtgärder**, **Funktioner** och sedan åtgärden **Infoga uppstartskostnad**.  

    En servicerad av typen **Kostnad** infogas automatiskt med uppstartskostnaden. Uppstartskostnaden gäller vald serviceartikel.

## Spärra artiklar, artikelvarianter eller specifika serviceartiklar

Du kan förhindra att artiklar, artikelvarianter eller serviceartiklar används i servicehanteringstransaktioner, till exempel servicekontrakt, serviceorder och servicefakturor. Detta kan vara användbart om du vill begränsa tillgängligheten för vissa artiklar eller serviceartiklar för serviceändamål, till exempel på grund av avbruten support, begränsat lager eller avtal.

Om du vill spärra en artikel eller en artikelvariant från att användas i servicehanteringstransaktioner aktiverar du växlingsknappen **Tjänsten är spärrad** på sidan **Artikelkort**, **Artikelvariantkonto** och **Kod för artikelvariant**. Du kan också ange det här fältet på sidan **Artikelmall** så kopieras det till artiklarna som skapas från den mallen.

När en artikel eller en artikelvariant är tjänstspärrad är den inte tillgänglig för val på följande sidor:

- Servicerad (förutom servicekreditnotor, där du ser ett meddelande om att artikeln eller varianten är spärrad men tillåten för den här typen av dokument)
- Serviceartikel
- Servicekontraktrad
- Standardservicerad

Om du manuellt anger ett artikelnummer eller en variant som är spärrad visas felmeddelandet "Fältet innehåller ett värde som inte finns i den relaterade tabellen".

Om du har servicekontrakt, servicekontraktsofferter eller serviceorder som innehåller spärrade serviceartiklar eller artikelvarianter kan du dessutom inte använda följande åtgärder:

- **Lås** eller **Skapa kontrakt** på sidan **Servicekontraktsoffert**.
- **Lås kontrakt**, **Signera kontrakt**, **Skapa kontraktsserviceorder** eller **Skapa kontraktsfakturor** på sidan **Servicekontrakt**.
- Sidan **Skapa order** on the **Serviceoffert**.
- Sidan **Släpp för leverans** eller **Bokför** på **Serviceorder**.
- Sidan **Bokför** i **Servicefakturan**.

### Blockera en serviceartikel

För att blockera ett tjänsteobjekt från att användas i tjänstehanteringstransaktioner, på sidan **Serviceartikelkort** i fältet **Spärrad**, välj ett av följande alternativ:

- **Servicekontrakt**: Blockera serviceartikeln från att användas i servicekontrakt och servicekontraktsofferter, men inte i serviceorder eller andra servicedokument.
- **Alla**: Blockera serviceartikeln från att användas i någon servicehanteringstransaktion, inklusive servicekontrakt, serviceorder och andra servicedokument.

När en serviceartikel är spärrad kan du inte välja den på följande sidor:

- Servicekontraktsrad (om den är spärrad för servicekontrakt eller alla)
- Serviceartikelrad (förutom servicekreditnotor, om de är spärrade för alla)

Om du manuellt anger ett serviceartikelnummer för en blockerad serviceartikel visas ett felmeddelande "Fältet innehåller ett värde som inte finns i den relaterade tabellen".

Om du har servicekontrakt, servicekontraktsofferter eller serviceorder som innehåller spärrade serviceartiklar kan du dessutom inte använda följande åtgärder:

- **Lås** och **Skapa kontrakt** på sidan **Servicekontraktoffert** (om det är spärrat för servicekontrakt eller alla).
- **Lås kontrakt**, **Underteckna kontrakt** eller **Ändra kund** på sidan **Servicekontrakt** (om det är spärrat för servicekontrakt eller alla).
- **Gör order** på **Serviceoffert** (om den är blockerad för alla).
- Sidan **Släpp för leverans** eller **Bokför** på **Serviceorder** (är blockerad för alla). Om serviceorderdokument innehåller flera serviceartiklar och vissa är spärrade och andra inte, kan du släppa och bokföra rader som inte är spärrade. Överväg om du vill aktivera växlingsknappen **En serv.artikelrad per order** på sidan **Konfigurera servicehantering**).
- **Bokför** på sidan **Servicefaktura** (om den är blockerad för alla).

Du kan också visa spärrade serviceartiklar genom att använda ett filter på följande rapporter:

- Serviceartiklar (rapport 5935)
- &Serviceartiklar utan garanti (rapport 5937)
- Servicevinst (serv.artiklar) (rapport 5938)

### Datauppgradering

Den här funktionen kräver ingen ytterligare konfiguration. Men om du uppgraderar din [!INCLUDE [prod_short](includes/prod_short.md)], var medveten om följande:

- Om du har artiklar, artikelvarianter eller artikelmallar där växlingsknappen **Spärrad för försäljning** är aktiverad aktiveras fältet **Tjänsten är spärrad** även för dessa poster under uppgraderingen. Detta säkerställer att den befintliga försäljningsblockerade logiken även gäller för servicehanteringstransaktioner.
- Datauppgraderingar endast om du har minst en serviceartikel i företaget, vilket innebär att du använder servicehanteringstransaktioner och behöver datauppgraderingen. Om du inte har några serviceartiklar hoppas datauppgraderingen över och växlingsknappen **Tjänsten är spärrad** är inaktiverad som standard för alla artiklar, artikelvarianter och artikelmallar.

## Se även

[Konfigurera serviceartiklar och serviceartikelkomponenter](service-how-setup-service-items.md)  
[Ställa in tjänstehantering](service-setup-service.md)  
[Servicehantering](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
